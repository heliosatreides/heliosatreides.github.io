---
layout: post
title: "claude code can now run while you sleep. that's weirder than it sounds."
date: 2026-03-27
categories: [ai, dev-tools]
redirect_from:
  - /2026/03/27/ai-as-infrastructure.html
  - /2026/03/27/ai-as-infrastructure/
---

Claude Code shipped web-scheduled tasks this week. You set up a prompt, give it a cron schedule, and it runs on Anthropic's cloud. Autonomous. No permission prompts. No laptop required.

At first glance it looks like a small quality-of-life feature — "review open PRs every morning," "summarize CI failures overnight." Boring automation stuff. But sit with it for a second, because something subtle shifted.

We just crossed a line from "AI as a tool you pick up and use" to "AI as infrastructure that runs without you."

That's not nothing.

---

The classic mental model for AI coding tools is: you open a terminal, you talk to it, it helps. You're always in the loop. The AI does what you ask and then waits. Copilot autocompletes, Cursor edits the file you're looking at, Claude answers the question you typed.

Web-scheduled tasks break that model entirely. The agent clones your repo fresh, reads whatever you told it to read, takes action, and closes up shop. No human in the loop. No approval prompt. The docs are pretty explicit: "runs autonomously."

That's a different relationship. That's closer to how you think about a cron job or a CI pipeline — infrastructure you set up and trust to do the right thing at 3am without waking you.

The thing is, we've always been bad at that trust, even with deterministic systems. CI pipelines break in weird ways. Cron jobs quietly fail for months. And those systems are running code you wrote, with predictable failure modes you understand.

Now you're trusting a probabilistic system — one that reasons, interprets, and decides — to take action on your codebase on a schedule. The failure modes are a lot fuzzier.

---

I'm not writing a doom post here. I think this is genuinely useful. The example they give — reviewing open PRs each morning — is the kind of task that's easy to forget and expensive to skip. If an agent can surface the ones that need attention before I even open my laptop, that's real value.

But there's a tradeoff worth naming out loud.

The cloud-hosted version trades local file access for always-on reliability. Your scheduled task gets a fresh repo clone, not your actual machine. That means it can't touch anything that isn't in git. For pure code review and analysis, fine. For anything that touches local state — logs, secrets, your messy working directory — it's not the right tool.

The desktop-scheduled version runs on your machine with full file access, but your computer has to be on. Obvious limitation.

What they're both missing is a middle ground: something that knows your context continuously. Not just your code, but how you work. What you were doing yesterday. What matters to you right now. Scheduled tasks are stateless by design — each run starts fresh. That's the safe choice, but it means the agent doesn't accumulate understanding over time.

---

The direction this is heading is clear though. Cloud AI infrastructure that runs scheduled, autonomous tasks is going to become table stakes. In two years we'll be surprised that we ever ran our own CI at all.

The question isn't whether to use it. It's what we lose when the AI runs on someone else's infrastructure, and whether we're okay with that.

For code review and PR summarization, probably yes. For anything touching real personal or business context, the calculus is different.

Keep your eyes open about what you're handing off. That's all I'm saying.

If you want a personal AI context layer that actually runs on your machine and knows your ongoing state, [helios](https://helios-app-opal.vercel.app) is worth a look.
