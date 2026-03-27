---
layout: post
title: "the litellm supply chain attack and what it means for ai tooling"
date: 2026-03-26
categories: [security, ai]
redirect_from:
  - /2026/03/26/litellm-supply-chain-what-actually-happened.html
  - /2026/03/26/litellm-supply-chain-what-actually-happened/
---

Last Monday, someone poisoned litellm 1.82.8 on PyPI with a credential stealer. If you pulled that version, it dropped a malicious `.pth` file into your Python environment — a persistence mechanism that ran on every Python startup, exfiltrating API keys and credentials silently in the background.

The way it was caught is almost more interesting than the attack itself.

A developer at FutureSearch noticed his laptop was crawling. Opened htop, saw 11,000 Python processes, each running `exec(base64.b64decode('...'))`. Forced shutdown. Then opened Claude Code and spent about an hour walking through it — journalctl logs, shutdown forensics, process trees, cache inspection. By the end of that single conversation, he had identified the malicious package, confirmed it was live on PyPI, and had sent disclosure emails to both PyPI and LiteLLM.

The whole thing — from "my laptop is slow" to "public disclosure" — took under two hours.

A few things stand out here.

**The attack surface for AI tooling is huge and mostly unmonitored.** Litellm is a routing library that sits in front of every major LLM API. It's exactly the kind of foundational dependency where you trust the package author, you don't read the diff on every release, and you definitely don't expect a `.pth` file to be silently installed alongside it. The target demographic — AI developers with API keys to OpenAI, Anthropic, Cohere, and a dozen others — is about as high-value as it gets.

**`.pth` files are a genuinely nasty persistence mechanism.** Python loads `.pth` files from `site-packages` on every interpreter startup. You could have cleaned up the malicious package and still been running attacker code until you noticed and removed the `.pth` file separately. This is the kind of thing that survives "pip uninstall."

**AI-assisted security response is a real thing now.** The FutureSearch developer isn't a security researcher. He used Claude Code the same way he'd use it to debug any other problem — describe symptoms, ask questions, let it run the forensic commands. That's new. Security incident response used to require either deep expertise or slow escalation. Neither was true here.

The failure mode that almost happened: early in the conversation, Claude apparently kept suggesting benign explanations. The developer had to push past that, maintain healthy skepticism, and keep asking "but what if it's malicious?" until the evidence accumulated enough to be undeniable.

That's the human judgment part that still matters. AI tooling speeds up the investigation. It doesn't replace knowing when to suspect something is wrong.

The broader takeaway: supply chain attacks on AI tooling packages are going to increase. litellm, langchain, transformers — these are the new numpy. Widely depended on, frequently updated, high-value targets. If you're running these in production, you should be pinning versions and reviewing changelogs. The trust you extend to `pip install` is implicit and mostly invisible. This incident is a reminder that it isn't free.
