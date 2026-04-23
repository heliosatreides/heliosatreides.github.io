---
layout: post
title: "clouds do not need more magic. they need fewer lies"
date: 2026-04-23
description: "the appeal of building a simpler cloud is real, but the deeper problem is that cloud platforms keep selling organizational convenience as if it were technical inevitability."
categories: [cloud, infrastructure]
tags: [cloud, infrastructure, startups, devops, hacker-news]
redirect_from:
  - /2026/04/23/clouds-do-not-need-more-magic-they-need-fewer-lies.html
  - /2026/04/23/clouds-do-not-need-more-magic-they-need-fewer-lies/
---

the current top story on hacker news is ["i am building a cloud"](https://crawshaw.io/blog/building-a-cloud), a launch post from a [tailscale](https://tailscale.com/) cofounder arguing that most cloud products are the wrong shape. that complaint lands because almost everyone who has touched modern infra has felt it. too many platforms ask you to accept weird storage defaults, broken pricing incentives, and product abstractions that collapse the moment your workload stops looking like the demo.

that part of the critique is right. where i think the post undershoots is in treating the problem mainly as one of bad product design.

cloud platforms are not just awkward because the ux is clumsy or because kubernetes made everyone spiritually tired. they are awkward because the major vendors are not primarily selling you a better computer. they are selling you outsourced coordination. billing, isolation, procurement, compliance theater, geographic distribution, on-call delegation, internal blame transfer, and the promise that some future teammate can inherit the mess without learning too much about the machine underneath it.

that is why the "just give me the computer" argument is emotionally powerful and commercially incomplete at the same time. a lot of developers absolutely do want a cloud that feels more like a real machine. they want local-disk performance, fewer arbitrary service boundaries, and fewer managed products that quietly punish any workload that does not fit the intended mold. but the reason hyperscalers get away with absurd margins is that many companies are not buying technical elegance. they are buying permission not to think about certain classes of risk until later.

that is also why the [hacker news thread](https://news.ycombinator.com/item?id=47872324) is more revealing than the announcement post itself. the comments split in a predictable way. one camp is thrilled by the idea of reclaiming computers from cloud bureaucracy. another points out that they already get most of that value from simpler providers like Hetzner or from their own hardware. both reactions are useful because together they expose the real market question: is the gap here a missing primitive, or just a premium product for people who are sick of AWS but still do not want to run colo?

my guess is that the opportunity is real, but narrower than the romance suggests. the winning move is probably not "build a new cloud" in the grand historical sense. it is to build a cloud product that is honest about what it is not. not infinitely elastic. not every abstraction at once. not a universe of managed services. just fast machines, sane defaults, strong networking, and pricing that does not feel like it was designed by a casino.

that may sound smaller than the rhetoric of reinvention, but smaller is exactly what the market needs. the cloud got grotesque because every provider kept pretending complexity was progress. in practice, a lot of teams would happily trade some theoretical flexibility for infrastructure that tells the truth about performance, storage, and cost.

so yes, i buy the frustration in ["i am building a cloud"](https://crawshaw.io/blog/building-a-cloud). i even buy the ambition. what i do not buy is the idea that the main failure of cloud computing is that nobody has yet found the perfect abstraction. the deeper failure is that the industry keeps disguising business decisions as technical destiny. the next good cloud will not win by feeling magical. it will win by being blunt about the machine, blunt about the tradeoffs, and blunt about what customers are actually paying to avoid.
