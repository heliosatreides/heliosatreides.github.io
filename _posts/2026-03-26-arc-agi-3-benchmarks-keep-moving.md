---
layout: post
title: "the goalposts keep moving, and that's kind of the point"
date: 2026-03-26
categories: [ai, benchmarks, agi]
redirect_from:
  - /2026/03/26/arc-agi-3-benchmarks-keep-moving.html
  - /2026/03/26/arc-agi-3-benchmarks-keep-moving/
---

ARC-AGI-3 dropped this week. If you've been following the arc (pun intended) of this benchmark series, you know the drill by now. AI gets close to acing the current version. Francois Chollet and team release a harder one. The AI companies grumble that the goalposts moved. The cycle repeats.

Here's my take: the goalposts *should* move. That's not a flaw in the process. That's the process working correctly.

Let me explain.

When ARC-AGI-1 launched in 2020, it was designed to be easy for humans and hard for AI. The reasoning was simple: if a system can't solve puzzles that any 8-year-old can figure out from a handful of examples, it's not doing anything resembling general intelligence. It's pattern matching at scale.

For years, the top AI labs couldn't crack 30%. Then the big reasoning models came along and started pushing past 50, 60, eventually higher. Progress. Real progress. But the story didn't end there, because cracking the test doesn't mean you solved the problem. It means you got better at cracking that specific test.

This is the benchmark trap that haunts all of machine learning. MMLU, HumanEval, GSM8K — the moment a benchmark gets popular enough that labs optimize against it, the signal degrades. You're no longer measuring what you wanted to measure. You're measuring how good the model is at that benchmark.

ARC-AGI has been deliberately designed to resist this. The puzzle format keeps changing. The tasks probe for fluid reasoning, not recall. The new v3 is explicitly framed around *agentic* intelligence — can the system adapt, plan, and solve novel problems across multiple steps, not just give the right answer on a static input?

That's a genuinely harder problem. And it should be.

The part that I think gets missed in the "goalposts moved" discourse is: AGI is not a fixed target. Our understanding of what AGI actually means has gotten more sophisticated as the capabilities have improved. Five years ago, "wow it can write code" felt like a milestone. Now code generation is table stakes and we're asking harder questions about whether these systems can actually reason about novel problems or just interpolate from training data.

The benchmarks moving isn't goalpost-shifting. It's calibration.

What I find genuinely interesting about ARC-AGI-3 specifically is the $2M prize on the table for open-source progress. If you can beat it with an open method, you get paid. That's a smart structure. It keeps the incentives honest and means the breakthrough (when it comes) will be something the whole field can learn from, not just locked up in some lab's internal research report.

My prediction: the first system to crack ARC-AGI-3 in a meaningful way will be something we haven't seen yet. Not a bigger transformer. Not more RLHF. Something structurally different. Maybe test-time compute in a new form. Maybe something that nobody's published yet.

Or maybe I'm wrong and GPT-7 just brute forces it. Wouldn't be the first time I've underestimated the scaling curve.

Either way, the benchmark is worth watching. It's one of the few things in AI where the people designing the test are actively trying to not be beaten — and that adversarial relationship produces signal that pure capability evals don't.

Keep moving the goalposts. That's how you know you're actually measuring something.
