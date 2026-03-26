---
layout: post
title: "github stars are a dumb metric for whether ai coding works"
date: 2026-03-25
description: "90% of Claude Code output goes to repos with fewer than 2 stars. The take is that this is a problem. The take is wrong — and it reveals something embarrassing about how we measure things in tech."
categories: [ai, dev-culture]
redirect_from:
  - /2026/03/25/github-stars-are-a-dumb-metric.html
  - /2026/03/25/github-stars-are-a-dumb-metric/
---

A stat floating around today: 90% of Claude Code output goes to GitHub repos with fewer than 2 stars. The framing, predictably, is that this is evidence of a problem. AI coding tools are churning out code nobody cares about. All that compute, all that hype, and most of it ends up in the digital void.

This take is wrong, and it reveals something embarrassing about how we measure things in tech.

GitHub stars have always been a terrible proxy for value. They measure virality, not usefulness. A repo with 10,000 stars might be a cute weekend project that everyone forks and forgets. A repo with 0 stars might be the internal tooling that keeps a 50-person company running. One of them shows up in the metrics. The other one doesn't.

The assumption baked into the "90% goes nowhere" framing is that software only matters if it's public and popular. That's not how software works. Most software that actually matters — the stuff that runs hospitals, handles payroll, automates the boring parts of someone's job — was never on GitHub. Or it's there but nobody starred it because why would they.

What Claude Code is doing, based on this data, is exactly what you'd want AI coding tools to do: letting regular people build things for themselves. Internal scripts. Personal projects. Automation for their specific workflow. That stuff doesn't get stars. It also doesn't need them. The person who built it is the person using it, and it works for them.

We called this "democratization of software" when we were excited about it. Now that it's actually happening, we're measuring it by the wrong yardstick and declaring it a failure.

Here's the comparison that matters. Before AI coding tools, what percentage of code written in side projects was "used" in any meaningful way? Most side projects stall out. Most repos stay at 0 stars. That was true in 2015, 2019, and it's true now. The baseline has always been that most code goes nowhere. What's changed is that more people can write it, faster.

If the distribution is 90% low-engagement repos now vs. 90% low-engagement repos before, AI coding tools haven't made the problem worse. They've just increased the total volume. And if even a fraction of the remaining 10% is better software because someone used an AI to help them think through the architecture, fix the bugs, or ship the thing instead of abandoning it, that's a net win.

The thing I'd actually want to know: is the 10% that does get traction *better* than comparable repos from two years ago? Are people shipping more complete, more polished, more functional tools when they have an AI pair programming with them? That would tell you something. Stars on the output that didn't go viral tells you nothing.

There's also a category of code this stat probably can't capture at all: code that never makes it to a public repo. The snippet someone wrote to automate their expense reports. The migration script that ran once. The tiny CLI tool that lives on one laptop and does exactly one job well. None of that shows up in any GitHub metric. None of it needs to.

AI coding tools are useful because they lower the cost of building something to try an idea. Most ideas don't pan out. Most experiments don't ship. That's not waste, that's how exploration works. The question was never "will every repo go viral." The question was "will people be able to build things they couldn't before."

Based on the volume of output going into even the low-star repos, people are clearly building. The fact that most of it stays quiet is fine. Most things stay quiet. That's not a bug.

Stop measuring this with GitHub stars. It's like measuring whether a city has good food by counting Michelin stars. Most good meals happen in places nobody reviewed.
