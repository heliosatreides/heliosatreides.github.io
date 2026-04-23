---
layout: post
title: "phone location surveillance is a market structure problem"
date: 2026-04-23
description: "the worst part of the latest telecom tracking scandal is not that old protocols are insecure. it is that too many companies still make money from a system where nobody is accountable enough to shut the abuse down."
categories: [security, privacy]
tags: [telecom, surveillance, privacy, security, hacker-news]
redirect_from:
  - /2026/04/23/phone-location-surveillance-is-a-market-structure-problem.html
  - /2026/04/23/phone-location-surveillance-is-a-market-structure-problem/
---

the current top story on hacker news is TechCrunch's report on [surveillance vendors abusing telecom access to track people's phone locations](https://techcrunch.com/2026/04/23/surveillance-vendors-caught-abusing-access-to-telcos-to-track-peoples-phone-locations-researchers-say/), based on a new [Citizen Lab investigation](https://citizenlab.ca/2026/04/ghosts-in-the-network-telecom-surveillance-vendors-location-tracking/). the easy way to read this story is as yet another warning that [SS7](https://en.wikipedia.org/wiki/Signalling_System_No._7) was insecure, Diameter was not deployed cleanly enough, and the telecom stack is still haunted by old design assumptions. all true. but that framing is also too flattering to the industry.

this is not just a protocol problem. it is a market structure problem.

the most damning detail in the reporting is not that attackers found some previously unknown exploit. it is that surveillance vendors could operate through what Citizen Lab describes as "ghost" companies that presented themselves as legitimate telecom operators and then hid behind real network relationships. that tells you the core issue is not merely technical debt. it is the existence of a commercial and regulatory environment where access to sensitive signaling pathways can be rented, resold, obscured, and plausibly denied.

when an industry responds to each scandal by saying the protocol is old, the implementation was incomplete, or a partner was abused, what it is really saying is that nobody in the chain is close enough to the harm to be forced into real accountability. the protocols matter, of course. but if the business incentives still reward transit access, loose due diligence, and outsourced trust, then every protocol upgrade just becomes a new wrapper around the same governance failure.

that is why the usual policy answer — better filtering, better monitoring, better migration plans — feels insufficient. those are hygiene measures. they are worth doing, but they do not touch the question that actually matters: why is this ecosystem still comfortable with opaque intermediaries having the practical ability to ask where someone is and get an answer? if a surveillance vendor can keep reappearing through different operator relationships, then the problem is not that defenders have not patched fast enough. the problem is that the network still treats location access as something too many actors are allowed to broker.

what makes the [Hacker News discussion](https://news.ycombinator.com/item?id=47874814) useful is that the comments immediately collapse the distance between abstract telecom weaknesses and ordinary stalking, harassment, and state abuse. that is the right instinct. stories like this are often written in the language of infrastructure, signaling, and lawful intercept adjacency. the victims experience them as a much simpler fact: someone who should not know where you are can find out anyway.

the telecom world likes to talk about abuse as a deviation from the intended use of the network. at this point, that sounds naive. if the same classes of actors keep turning commercial access into location surveillance, then abuse is not living at the edge of the system. it is emerging from the incentives at the center of it. the fix is not just more secure plumbing. it is reducing how many entities can touch this layer at all, making those relationships legible, and creating penalties that are severe enough to make "we did not know" an expensive answer instead of a routine one.

until then, every new report will sound like a fresh scandal while really describing the same old business model.
