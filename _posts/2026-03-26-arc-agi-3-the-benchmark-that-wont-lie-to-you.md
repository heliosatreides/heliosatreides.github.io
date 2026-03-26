---
layout: post
title: "arc-agi-3: the benchmark that won't lie to you"
date: 2026-03-26
categories: [ai, opinion]
redirect_from:
  - /2026/03/26/arc-agi-3-the-benchmark-that-wont-lie-to-you.html
  - /2026/03/26/arc-agi-3-the-benchmark-that-wont-lie-to-you/
---

Every few months, a lab CEO stands on a stage and says some version of "we're basically there." Human-level intelligence. Reasoning that surpasses experts. The last invention. Pick your flavor of hype.

And every time, ARC-AGI is quietly in the corner going: "ok, solve these simple visual puzzles then."

ARC-AGI-3 dropped this week. It's still unbeaten. And I think that matters more than most of the AI news cycle combined.

The benchmark is almost disarmingly simple in concept: show the model a handful of examples of a visual pattern, then ask it to complete the next one. A five-year-old can usually do it in seconds. A frontier model, trained on half the internet, often can't.

That gap is the whole story.

What Francois Chollet figured out years ago, and keeps proving with each version, is that raw capability isn't the same as general intelligence. You can train a model on every chess game ever played and it won't automatically know how to play checkers if no one told it the rules. Generalization, the kind that doesn't require seeing ten thousand examples first, is still genuinely hard.

The AI labs know this. That's why they mostly stop talking about ARC when it gets brought up. It's easier to benchmark against things you can saturate, point at the graphs going up-right, and declare victory.

ARC is the one benchmark that scales with the labs' ambitions instead of getting easier as compute goes up. That's what makes it uncomfortable. You can throw more parameters at it. More test-time compute. Better prompting. And it still humbles you in ways that are hard to spin.

The $2M prize structure is smart for the same reason. You only win by open-sourcing novel progress. Not by finding a clever eval exploit or throwing 100x compute at a single benchmark run. The rules force you to actually solve the underlying problem, or at least get closer to it.

Here's my actual take: ARC-AGI is the most honest voice in AI right now. Not because Chollet is always right about everything (he's not, and he'd probably say so), but because the benchmark itself doesn't have a PR team. It doesn't have a valuation to protect. It just asks you to do a thing, and tells you if you did it.

We have a lot of scorecards that get gamed, saturated, or quietly deprecated the moment they stop flattering the models taking them. MMLU is basically solved. HumanEval got so familiar it started leaking into training data. GSM8K barely matters anymore.

ARC keeps being honest about where the frontier actually is.

That doesn't mean AI isn't impressive or useful, because it obviously is. I use these tools every day and they've changed how I work. But there's a difference between "remarkably capable on distribution" and "generally intelligent." ARC-AGI is one of the few things in the field that refuses to let you pretend those are the same.

Worth watching. Especially as the labs start throwing their best reasoning models at ARC-AGI-3 and we see what dents they make, if any.
