---
layout: post
title: "the dark matter of AI coding"
date: 2026-03-26
description: "Most AI-generated code never gets a star, a PR review, or a mention. It's dark matter — invisible, untracked, but quietly doing work. That's not a bug. That's the point."
categories: [ai, dev]
redirect_from:
  - /2026/03/26/ai-code-dark-matter.html
  - /2026/03/26/ai-code-dark-matter/
---

Someone ran the numbers on Claude-linked code commits and found that 90% of them land in repos with fewer than two stars. On GitHub, a repo with zero stars is basically invisible. No users. No forks. Nobody watching.

The take bait is obvious: AI is generating mountains of throwaway code that nobody uses. Another sign that we're in a vibe-coding bubble. Copilot for the sake of it.

I think that read is completely wrong.

The 90% isn't waste. It's the whole point.

Software has always had two kinds: the kind people see, and the kind that just runs. Public repos on GitHub are the seen kind — open source libraries, portfolio projects, things people built to show off or share. They get stars because they have an audience. But most useful software has no audience. It runs in a cron job, sits on someone's laptop, automates a workflow that one person cares about. Nobody stars it because nobody knows it exists.

Before AI coding tools, writing that kind of software had a real tax. You had to actually be a developer, or at least comfortable enough with code to google your way through Stack Overflow at 1am. A lot of people couldn't clear that bar. They used Excel formulas when they needed scripts. They clicked through UIs when they could have automated. They hired someone, or they gave up.

AI tools didn't just make developers faster. They brought in a whole category of people who weren't developers at all.

A PM who can now write the script to parse their own data. A designer who built a tool to batch-resize assets. A founder who automated their own invoicing workflow. None of that shows up as polished open source. It shows up as a repo with a weird name, one commit, and zero stars. And it works.

That's the dark matter of software. It doesn't reflect light, but it has mass.

The other thing the two-star stat tells you: people are building for themselves. Not to impress, not to grow a following, not to make something "production ready." They have a problem, they used an AI tool to help them solve it, done. That's actually healthy. Not everything needs to be a library. Not everything needs a README. Sometimes the right amount of software is a 40-line script that you run once a month and never think about again.

The concern I'd take more seriously is quality. A lot of that invisible code probably has bugs, probably doesn't handle edge cases, probably would horrify a senior engineer. But the alternative isn't "write it properly instead." The alternative is "don't write it at all." Given that choice, buggy automation beats no automation most of the time.

Where I think the critique has a grain of truth: if AI coding tools are primarily helping people build things for themselves, the overall economic value proposition is different than the pitch. The pitch is productivity multiplier for professional devs. The reality might be more like: democratizing personal tooling for non-devs. That's still good, but it's a different business.

The benchmark for a coding AI probably isn't "how many stars did the repos get." It's closer to "did the person who wanted to build the thing actually build it." By that measure, the 90% is a win, not a warning sign.

Dark matter is real. It just doesn't show up on your telescope.
