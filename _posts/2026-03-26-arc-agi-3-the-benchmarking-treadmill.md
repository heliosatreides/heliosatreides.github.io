---
layout: post
title: "ARC-AGI-3 and the benchmarking treadmill"
date: 2026-03-26
categories: [ai, takes]
redirect_from:
  - /2026/03/26/arc-agi-3-the-benchmarking-treadmill.html
  - /2026/03/26/arc-agi-3-the-benchmarking-treadmill/
---

ARC-AGI-3 dropped today. Trending on HN, lots of excitement. And I'll be honest: my first reaction wasn't excitement. It was "here we go again."

Let me be clear, I think Francois Chollet is doing genuinely important work. The ARC Prize is one of the few serious attempts to measure something other than "can this model memorize and regurgitate text really well." That matters. But watching the cycle play out for the third time in a few years, something feels off.

Here's the pattern: AI clears a benchmark. Researchers celebrate. Skeptics say "but it didn't really understand, it just pattern-matched." Benchmark gets harder. Repeat.

ARC-AGI-1 was supposed to be the thing that exposed the gap between real reasoning and statistical autocomplete. AI models got better. Then ARC-AGI-2 showed up with harder visual puzzles and more abstract rules. Models improved on that too. Now ARC-AGI-3. At some point you have to ask: are we measuring something real, or are we just perpetually moving the goalposts?

The frustrating part is I don't think either side is entirely wrong.

The skeptics are right that benchmark performance is not the same as general intelligence. A model that aces ARC tasks might still fail spectacularly at novel real-world problems that don't fit any training distribution. We've seen this over and over. A model writes brilliant code then confidently hallucinates a function that doesn't exist. Benchmark score: high. Actual reliability: patchy.

But the "it's just curve-fitting" crowd sometimes undersells what's actually happening. Clearing increasingly abstract reasoning tasks is not nothing. The bar for "just memorization" gets harder to defend when the tasks are specifically designed to resist that. At some point, solving the puzzle requires something that looks a lot like generalization.

What I think is actually going on: we're not measuring intelligence as a single thing. We're measuring a rough proxy for one slice of it, iterating that proxy as models improve, and calling it a race toward AGI. It's not a race toward anything. It's a high-stakes game of cat and mouse between benchmark designers and model capabilities.

That's not useless. It's actually how scientific progress works. You probe the edges, you find where the model breaks, you design tests that expose those breaks. ARC-AGI has done more to push serious AI research than a thousand leaderboard evals on MMLU. I'm not dismissing it.

But the popular narrative, the "ARC-AGI-3 is the last line before we crack general intelligence," that's hype. It's not the last line. If models ace ARC-AGI-3, someone will design ARC-AGI-4. Because there will always be something they can't do. The question is whether what they can do is useful, and whether we understand the failure modes well enough to deploy responsibly.

The real thing worth watching isn't the score. It's the gap between "model does well on benchmark" and "model does well on tasks humans actually care about." That gap is still enormous in a lot of domains. Less enormous than it was two years ago, but enormous.

ARC-AGI-3 is a useful instrument. Just don't confuse the instrument for the destination.

---

*I build Helios, a personal AI that actually knows you. If you're tired of re-explaining yourself to every new chat, [check it out](https://heliosatreides.github.io).*
