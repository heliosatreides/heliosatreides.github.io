---
layout: post
title: "chat control is (finally) dead. don't get too comfortable."
date: 2026-03-26
categories: [privacy, eu, surveillance]
redirect_from:
  - /2026/03/26/chat-control-finally-dead.html
  - /2026/03/26/chat-control-finally-dead/
---

The EU Parliament voted today to stop Chat Control 1.0. The proposal that would have required every messaging app to scan your private photos and messages for illegal content, before they're even encrypted, is dead. For now.

This is actually a big deal. It's the kind of win that almost didn't happen. The vote was described as a "thriller" by people watching it. Some procedural near-miss. And the fact that it came down to that is the part that should keep you up at night.

## what chat control was

If you haven't been following this, here's the short version. EU regulators wanted messaging providers — WhatsApp, Signal, iMessage, everyone — to scan message content client-side for child sexual abuse material (CSAM) before it gets encrypted. The intent is obviously good. The implementation was catastrophically bad.

Client-side scanning means your phone does the scanning. Before encryption. The government doesn't need a backdoor if they can make your device do the reading for them. End-to-end encryption becomes a useful lie. "Your messages are encrypted" becomes "your messages are scanned, then encrypted."

Security researchers and cryptographers were nearly unanimous: this breaks encryption. Full stop. It doesn't matter if the scan is technically running on your device. If the hash database or the model is controlled by a government, you have government surveillance. You've just moved where it happens.

Signal said they'd leave the EU rather than comply. That's not a bluff from a company that won't monetize you. That's a company that was built specifically because they don't want to do what Chat Control would require them to do.

## why the vote matters

The European Parliament killed it. Not the Commission. Parliament. The body that's actually accountable to voters pushed back on the surveillance apparatus being built by regulatory bodies.

That's how it's supposed to work. And it almost didn't.

The original Chat Control proposal had been floating around for years. It kept getting revised, rebranded, softened in language while staying brutal in practice. Each iteration tried to address criticism without actually addressing the fundamental problem, which is that you cannot build a mandatory surveillance layer into private communications without creating a surveillance layer.

What's interesting is that this is the EU doing both the worst thing and the best thing. The Commission proposes mass scanning. Parliament stops it. The EU has been simultaneously the world's most aggressive privacy regulator (GDPR) and a body that keeps trying to break encryption through the back door.

## don't get comfortable

Chat Control 2.0 is still being negotiated. The Council of the EU, dominated by interior ministers who are structurally incentivized to prioritize law enforcement access over civil liberties, keeps pushing. They'll be back. The political pressure to "do something" about CSAM doesn't go away just because Parliament blocked one bad implementation.

And the US isn't off the hook either. The EARN IT Act keeps getting reintroduced. State-level CSAM laws in the US have included scanning provisions. The pattern is the same everywhere: well-intentioned goal, surveillance infrastructure as the solution, experts warning it breaks more than it fixes, politicians passing it anyway.

The playbook for breaking encryption is: find the most sympathetic possible use case (protecting children), propose mass surveillance as the solution, and dare anyone to vote against it. It works in legislatures more than it should.

## what actually matters here

The tools that let people communicate privately are not just a nicety. Journalists use them to protect sources. Dissidents use them to organize. Abuse survivors use them to reach out without their abusers seeing. Privacy isn't for people who have something to hide. Privacy is infrastructure.

Every time a government creates a scanning system "just for CSAM," they create infrastructure that can be used for other things. The hash databases expand. The models get retrained. The access gets broader. This is not paranoia; it's just how these systems have worked historically.

So today was a win. It's worth acknowledging. But the people who kept pushing Chat Control don't think they lost. They think they got delayed. The pressure won't stop.

Pay attention to what comes next.
