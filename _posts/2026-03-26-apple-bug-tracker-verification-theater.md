---
layout: post
title: "apple's bug tracker is verification theater"
date: 2026-03-26
categories: [dev, apple]
redirect_from:
  - /2026/03/26/apple-bug-tracker-verification-theater.html
  - /2026/03/26/apple-bug-tracker-verification-theater/
---

Apple quietly closes bug reports if you don't manually confirm the bug still exists. Not because they fixed it. Not because they investigated it. Just because you didn't respond to their "is this still a thing?" prompt in time.

This is verification theater. It protects Apple's metrics more than it serves developers.

Here's how it works in practice: you file a Feedback report, nothing happens for months, then Apple sends an automated nudge asking if the issue is still reproducible. If you miss it (because, you know, you have a job), they close the report. Resolved. Not actually resolved. Closed because you didn't babysit it.

The perverse effect is that the bugs most likely to get closed are the obscure, hard-to-reproduce ones. The ones that only surface under specific conditions. The ones that took you three days to isolate and write up. Those are exactly the reports that need the most follow-up attention, and they're the ones most likely to go stale in a tracker.

**Apple's incentive here is obvious.** Fewer open bugs looks better than more open bugs. Closing reports shifts the accountability burden. If a bug disappears from the tracker, it's not Apple's problem anymore. It's the developer's fault for not following up.

The real insult is that Feedback — Apple's public-facing bug tracker — is already a one-way communication channel most of the time. You file something, you get an automated acknowledgment, and then silence. No status updates. No engineer notes. No ETA. Just a ticket number that sits there aging. So when Apple introduces a mechanism that requires *you* to stay engaged in a conversation that Apple isn't having with you, that's not a partnership. That's a tax on developer time with no corresponding commitment on Apple's side.

Compare this to how serious bug trackers work. When a team actually cares about quality, bugs get triaged, assigned, and linked to commits. The reporter gets a note when someone starts looking at it. When it's fixed, there's a version number attached. You don't have to periodically poke the system to keep your report alive.

I understand the impulse to clean house. Bug trackers accumulate junk. Reporters move on. Issues stop being relevant. Automatic closure has a legitimate use case. But the right signal for closing a bug is "we fixed it and verified" or "we investigated and it's by design." Not "developer didn't reply to our nudge."

**What this tells you about Apple's relationship with developers in 2026:** it's transactional and asymmetric. They need apps in the App Store to make the platform valuable. They don't necessarily need to maintain a good working relationship with the people making those apps. The power dynamic is too lopsided for that.

Third-party developers have been complaining about Feedback since it replaced Radar. The interface is worse. The transparency is worse. And apparently the pipeline for actually getting bugs fixed hasn't improved. Instead, Apple added a mechanism that makes the numbers look better without doing the underlying work.

If you're a developer who has filed Feedback reports: go check your old ones. Set a reminder. Or just accept that some percentage of your work documenting Apple's bugs will quietly disappear into the void. That's the deal right now.

Not a great deal.
