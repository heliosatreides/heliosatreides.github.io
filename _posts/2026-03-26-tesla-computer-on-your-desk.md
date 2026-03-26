---
layout: post
title: "tesla built a computer. they just don't think you own it."
date: 2026-03-26
categories: [tech, hardware, right-to-repair]
redirect_from:
  - /2026/03/26/tesla-computer-on-your-desk.html
  - /2026/03/26/tesla-computer-on-your-desk/
---

Someone on HN this week ran a Tesla Model 3's onboard computer on their desk. Not a simulation. Not an emulator. The actual MCU pulled from crashed cars, booted on a bench with some spare parts and a lot of patience.

670 upvotes. Thousands of people losing their minds over it. And honestly? That reaction tells you everything about how people feel about the relationship between car companies and the hardware they sell you.

Here's the thing. Tesla is fundamentally a software company that ships hardware. The whole pitch — OTA updates, autopilot improvements, range tuning, feature unlocks — is built on the premise that software is the real product and the car is just the delivery mechanism. That framing has worked beautifully for them for years.

Until someone grabs a wrecked Model 3 from a salvage yard, strips out the MCU, and proves that the "delivery mechanism" is actually a surprisingly capable Linux box that you can run anywhere.

And now you get to watch the contradiction in real time.

Tesla wants to be a software company when it means they can push features remotely, charge you a subscription for your heated seats, or brick a car they claim was stolen. They want to be a hardware company when it means locking down repair options, tying components to VINs, and making sure your independent mechanic can't touch the thing.

The guy who did this project — David Hu — wasn't even trying to make a political statement. He just wanted to see if he could do it. Reverse engineered the boot process, figured out how to fake enough of the car's sensor signals to keep the system happy, and got it running. Classic hacker mentality. Cool thing exists, wonder if I can poke it.

The reason 670 people upvoted it is because there's genuine hunger for this. People want to know what they actually bought. They want to repair it, understand it, repurpose it when the car is totaled. They want to know that a $60,000 vehicle isn't going to become e-waste the moment Tesla decides the component is "out of support."

Right to repair has been a software fight for years. Apple vs. independent repair shops. John Deere vs. farmers who just want to fix their own tractors. Now it's becoming a car fight, and Tesla is an interesting case study because they've been so aggressive about it in both directions. Their cars are legitimately impressive engineering. Their repair policies are genuinely hostile.

What strikes me about the Tesla MCU project is how unsurprising the actual hardware is once you see it. A custom NVIDIA chip, some standard connectors, a Linux kernel underneath. Nothing magic. The magic was in making it all talk to each other in a moving vehicle, but that's solvable. One guy in his garage proved it.

That's not a security vulnerability. That's just... a computer. Running on a desk. Because computers do that.

The auto industry spent a century treating software as an afterthought — some code to run the infotainment, some more to manage the engine. Tesla inverted that. Software first, hardware second. Great for innovation. Not so great when the software company instincts kick in and they decide that shipping the hardware doesn't mean you get to own what runs on it.

You bought a car. You own the steel, the battery, the seats. But the software? The ability to actually make it do what it's capable of? That's licensed to you. Conditionally. Revocably. Until Tesla decides otherwise.

David Hu just ran the computer on his desk. He didn't need Tesla's permission. He didn't need to log in. He just needed the hardware, some time, and the kind of curiosity that car companies have been trying to engineer out of their customers for years.

Good luck with that.
