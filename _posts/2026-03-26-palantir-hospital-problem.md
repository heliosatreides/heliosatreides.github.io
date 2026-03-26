---
layout: post
title: "palantir's hospital problem"
date: 2026-03-26
categories: [ai, privacy, health]
redirect_from:
  - /2026/03/26/palantir-hospital-problem.html
  - /2026/03/26/palantir-hospital-problem/
---

NYC Health + Hospitals just announced it won't renew its contract with Palantir. The deal expires in October and they're moving everything in-house. Meanwhile, Palantir just landed a £330m NHS contract in the UK. Same company, same controversy, two very different bets.

That tells you something about how institutions actually make decisions around sensitive data. It's less about principles and more about who's watching.

The NYC contract was ostensibly about revenue cycle optimization. Recovering money from insurance claims. Fine. But buried in the agreement was a line that said Palantir could "de-identify" patient health information and use it for "purposes other than research." With permission from the city agency, sure. But that clause is in there. Someone put that in there. Someone signed it.

Dr. Mitchell Katz, the hospital system president, testified that there was an "absolute firewall" between Palantir and ICE. No incidents, he said. I'll take him at his word. But the reason he had to say that in a city council hearing at all is the problem. That's not a normal sentence for a hospital administrator to have to say. You don't have to build "absolute firewalls" around your billing software unless your billing software vendor has a complex relationship with immigration enforcement.

Palantir is a data company that grew up on surveillance contracts. That's not a smear, it's their origin story. They were built on CIA funding, their tools have been used by ICE, and Peter Thiel's politics aren't subtle. None of this is secret. The question isn't whether Palantir is trustworthy. The question is why hospitals keep signing deals with them and then quietly exiting when the contract term is up.

The answer, probably, is that Palantir is genuinely good at what it does. Healthcare billing is a nightmare. Insurance denials, underpayments, and claim gaps cost hospital systems real money. If Palantir's software finds $4m in missed revenue on a $4m contract, that's a break-even at worst. And hospital IT is notoriously bad. Legacy systems, understaffed teams, decades of technical debt. An outside vendor promising to fix your revenue cycle is tempting even when that vendor comes with baggage.

But there's a reason NYC is moving in-house after this, and there's a reason the UK rollout is stalling. It's not that the software doesn't work. It's that nobody trusts the wrapper around it. The institution, the contracts, the business model, the politics. You can't separate Palantir the software from Palantir the company.

The UK situation is actually stranger. Not even half of NHS health authorities had started using Palantir's system as of last summer, despite a nationwide rollout push from Keir Starmer. Doctors and community groups are pushing back. The government wants speed. The people responsible for patients want caution. Classic implementation gap. But the interesting thing is the concern isn't that the technology is bad. It's that they don't know what Palantir does with what they see.

That's the core issue with all of this. When you hand your patient data to a third-party AI company, the contract is not the relationship. The contract is a piece of paper. The relationship is: you gave them access, they have your data, and your leverage after that point is mostly theoretical.

Hospitals are figuring this out the slow way. NYC is building in-house. Some NHS trusts are dragging their feet. And Palantir keeps signing new contracts because there's always another institution that hasn't learned this lesson yet.

The pattern here isn't unique to Palantir. It's what happens any time you solve a real operational problem with a vendor whose interests aren't fully aligned with yours. The tool works. The relationship is messy. Eventually you decide the mess isn't worth it.

If you want a personal data dashboard that you actually own and control, no third-party access, no "de-identification" clauses buried in contracts, [helios](https://helios-app-opal.vercel.app) is built exactly for that.
