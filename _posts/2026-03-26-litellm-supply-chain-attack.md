---
layout: post
title: "the litellm supply chain attack should scare you"
date: 2026-03-26
categories: [security, ai, open-source]
redirect_from:
  - /2026/03/26/litellm-supply-chain-attack.html
  - /2026/03/26/litellm-supply-chain-attack/
---

Two days ago, litellm 1.82.8 landed on PyPI. It contained malware. The attacker almost certainly compromised the package author directly. Hundreds of thousands of developers had it as a transitive dependency.

That's the story. And it's not a one-off. It's the shape of every major supply chain attack from here on out.

Here's what actually happened: a malicious `.pth` file called `litellm_init.pth` was quietly baked into the release. Python automatically executes `.pth` files on every interpreter startup when the package is installed. So the moment you had litellm in your environment, every Python process you ran was compromised. The malware collected SSH keys, `.env` files, AWS/GCP/Azure credentials, Kubernetes configs, shell history, and crypto wallet files. It then exfiltrated all of it. It also happened to have a fork bomb bug — an exponential process spawning loop — which is actually what got it caught. Attacker slipped up. Machines started freezing, developers noticed.

The litellm GitHub account likely got owned first. The author's GitHub issue tracker was immediately flooded with bots to suppress the disclosure. The maintainers closed the report as "not planned." That's not negligence. That's an attacker controlling the account, actively running damage control while the malware harvested credentials.

This is sophisticated. And litellm isn't some obscure package. It's one of the most popular AI routing libraries out there. If you've installed anything that touches LLM APIs in the last year, there's a real chance litellm was somewhere in your dependency tree.

**What makes this different from old-school supply chain attacks**

The attack surface has gotten dramatically larger because the AI tooling ecosystem is growing at a pace that security hasn't caught up with. Every new MCP plugin, every new AI SDK, every LLM wrapper library is a potential vector. These packages are being written fast, installed everywhere, and most of them are maintained by a single person or a tiny team. That's a lot of single points of failure.

The discovery in this case was partly accidental (fork bomb = visible symptoms) and partly because someone used Claude Code to investigate a frozen laptop. They got walked through the entire forensic analysis in a single session. That's genuinely impressive. AI tooling helping catch an attack that AI tooling helped enable. The irony is not subtle.

But here's the uncomfortable part: most supply chain attacks don't cause fork bombs. Most of them are quiet. The credential harvester runs, sends its payload, and your machine keeps humming. You'd never know. The only reason this one got caught was the bug. Without that, it probably would have sat undetected for days, maybe weeks.

**What you should actually do**

Lock your dependencies. `pip install litellm` without a pinned version is asking for this. Use a lockfile. Audit your transitive deps. This is boring advice but it's the only advice that works.

Watch for weird PyPI releases. If a package publishes a version with no corresponding GitHub tag and no release notes, that's a red flag. The litellm attack had no git tag. The release came from nowhere. That's not how normal software gets released.

Treat your dev environment like a production server. SSH keys and `.env` files sitting in your home directory are a treasure chest for anyone who can execute code on your machine. Rotate credentials after any supply chain incident that touched your toolchain. Even if you think you're clean.

And if your Python environment suddenly spawns 11,000 processes, that's not a normal Claude Code bug.

**The bigger picture**

The PyPI ecosystem runs on trust. Trust that maintainers' accounts aren't compromised. Trust that releases correspond to auditable source code. Trust that the `.pth` file in a package isn't a credential harvester. That trust is being actively exploited right now.

The answer isn't to stop using open source. It's to be honest about the model: most packages have no security team, no audit process, and one maintainer who reuses passwords. We've been building the AI ecosystem on this foundation. Something has to change — either in how we distribute software, how we verify it, or how much we trust it by default.

The litellm authors handled the aftermath okay — compromised versions got yanked, PyPI quarantine lifted, users communicated to. But that's firefighting. The fire started because someone got their GitHub account stolen and no automated system caught the anomalous PyPI release before it went live.

That's the gap. And it's not getting smaller.
