---
layout: post
title: "the quality debt nobody warned you about"
date: 2026-03-26
description: "AI coding tools help you ship faster. They also help you accumulate quality debt faster. The code that ships in half the time still has to be maintained by humans — at full speed."
categories: [ai, engineering]
redirect_from:
  - /2026/03/26/the-quality-debt-nobody-warned-you-about.html
  - /2026/03/26/the-quality-debt-nobody-warned-you-about/
---

Amazon had an outage. An AI coding bot apparently caused it. Amazon said nope, not true. Then Amazon quietly announced a 90-day internal reset on how they ship code.

You don't announce a 90-day reset if nothing happened.

The story keeps showing up in different forms. AWS. Big fintech backends. Consumer apps with memory leaks you can measure in gigabytes. Features that clearly nobody ran end-to-end before shipping. The quality bar dropped and most people just... adapted. Called it the new normal. Blamed "fast iteration."

Here's what actually happened: we plugged agents into our CI pipelines before we figured out how to review them.

Tech debt has always existed. You borrow time from the future — ship fast now, refactor later. Agents don't change that math. What they change is the *volume*. You can now generate three times the code in the same sprint. Which means you can also generate three times the hidden complexity, three times the untested edge cases, three times the "I'll figure this out when it breaks in prod."

The bet most teams made: move fast, let the agents handle the volume, review will catch the obvious stuff. What they missed: the things that kill you in production are never the obvious stuff. They're the implicit assumptions baked into a function written by a model that didn't know about your specific infra constraint, your specific database quirk, the subtle race condition that only surfaces under load.

A good senior engineer catches that. Not because they're smarter than the agent, but because they *own* the context. They remember that this service has a 10-second timeout for a reason. They know the auth library does something weird with tokens under refresh. The agent doesn't. It can't.

The way out isn't to stop using agents. It's to stop treating review as a formality.

Slow down the review loop, not the shipping loop. Ship just as fast — but make someone actually responsible for understanding what got shipped. Not signing off on it. *Understanding* it. Able to explain it back. Able to defend the edge cases.

Amazon's 90-day reset is them re-learning something senior engineers have always known: you can write code faster than you can understand it. The gap between those two speeds is where outages live.

The teams that win with AI aren't the ones who generate the most code. They're the ones who stay in control of what they're generating.
