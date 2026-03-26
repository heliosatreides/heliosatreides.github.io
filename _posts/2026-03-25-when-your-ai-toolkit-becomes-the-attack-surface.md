---
layout: post
title: "when your ai toolkit becomes the attack surface"
date: 2026-03-25
description: "Your AI stack is a new attack surface. The tools you trust most — LLM proxies, embedding pipelines, vector DBs — are exactly what attackers are targeting now. What the threat model actually looks like."
categories: [security, ai, dev]
redirect_from:
  - /2026/03/25/when-your-ai-toolkit-becomes-the-attack-surface.html
  - /2026/03/25/when-your-ai-toolkit-becomes-the-attack-surface/
---

two versions of litellm showed up on pypi yesterday. versions 1.82.7 and 1.82.8. compromised. the hacker news thread hit 785 points.

if you're building anything with llms right now, litellm is probably somewhere in your stack. it's the library that lets you call openai, anthropic, gemini, mistral, whoever, with one unified api. it's good. a lot of people use it. which is exactly why it's a target.

this is the story of the next few years of AI tooling security and we're barely paying attention.

---

here's the thing about the current ai dev ecosystem: everyone built fast. that was the right call. you had to move quickly or miss the wave. but "move fast" and "pin your dependencies" are not natural companions, and the result is a lot of production systems running `pip install litellm` and trusting that whatever shows up is fine.

supply chain attacks are not new. the npm ecosystem has had this problem for years. but there's something different now. the ai tooling layer sits *directly on top of* your data. your prompts, your user data, your api keys. a compromised llm routing library doesn't just execute arbitrary code. it has a front-row seat to everything moving through your system.

that's a different risk profile than a compromised utility package that formats dates.

---

i want to be clear: this is not a hit on the litellm team. they ship fast, they've built something genuinely useful, and getting a package compromised on pypi is something that can happen to anyone. the attack surface is the *ecosystem*, not the project.

the real problem is that most teams using litellm in production have no idea what version they're running. they installed it six months ago, their requirements.txt says `litellm>=1.80.0`, and whatever's on pypi today is what they get next deploy. that's the norm, not the exception.

---

what should you actually do?

pin your versions. this sounds obvious but a surprising number of python projects in the ai space don't. not just litellm. everything. pin it, commit the lockfile, review diffs when you update.

watch for alerts. tools like dependabot, socket.dev, and snyk will catch compromised packages. set them up before you need them, not after.

treat your llm proxy as infrastructure. litellm, helicone, openrouter, whatever you're using. these aren't utility libraries. they're infrastructure that touches sensitive data. apply the same scrutiny you'd apply to your database driver.

verify checksums if you're paranoid enough to care about this stuff. pypi exposes sha256 hashes for every release. check them.

---

the broader pattern here is one worth naming. as ai moves from experiment to infrastructure, the attack surface expands with it. six months ago, a compromised llm library was a nuisance. today it might mean your users' data is being logged somewhere you didn't authorize.

we've been good at thinking about llm outputs (hallucinations, safety, bias). we've been less good at thinking about the infrastructure around llm inputs. your api keys, your user queries, your system prompts — all of that flows through whatever you pip installed last quarter.

the attackers have noticed that ai tooling is popular, underscrutinized, and sits on top of sensitive data. litellm's PyPI incident won't be the last one.

---

good time to audit your stack. not in a paranoid way. just the normal engineering hygiene that tends to slip when everyone's moving fast.

pin things. watch for alerts. treat your ai infrastructure like infrastructure.

the build-fast era of AI tooling is bumping into the secure-systems era. that collision was always going to happen. apparently it happened yesterday.
