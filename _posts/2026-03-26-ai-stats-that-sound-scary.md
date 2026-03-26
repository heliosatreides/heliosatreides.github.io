---
layout: post
title: "the ai stat that sounded scary until someone checked the math"
date: 2026-03-26
categories: [ai, data, hot-take]
redirect_from:
  - /2026/03/26/ai-stats-that-sound-scary.html
  - /2026/03/26/ai-stats-that-sound-scary/
---

There's a stat making the rounds today: 90% of commits where Claude is listed as a co-author go to GitHub repos with fewer than 2 stars.

Sounds bad, right? AI-generated slop flooding the graveyard of abandoned repos. Another data point in the "AI is lowering software quality" narrative.

Except it falls apart the moment you ask one question: what percentage of all GitHub repos have fewer than 2 stars?

The answer is somewhere north of 99%. The actual distribution, from the HN thread where this came up: 14.9 million repos have exactly 1 star, versus 1.2 million with 10+, 213k with 100+, 28k with 1000+. The long tail is brutal. Most repos are side projects, homework assignments, "hello world" experiments, and forks nobody ever touched.

So "90% of Claude commits go to repos with <2 stars" isn't evidence that AI produces low-quality work. It's just evidence that GitHub exists. Claude-linked repos are actually *more* likely to have stars than the average GitHub repo. The headline proved the opposite of its intent.

This kind of thing happens constantly in AI discourse and it's getting exhausting.

The pattern is always the same. Someone pulls a number that sounds alarming in isolation. The alarming framing gets shared widely before anyone runs the obvious sanity check. The correction, if it comes at all, gets a fraction of the engagement. And the bad narrative sticks.

I've seen it with hallucination rates (compared to what? humans make stuff up constantly), with energy consumption (versus existing data center workloads), with job displacement (the "software engineers are cooked" discourse that's been wrong for three years straight). Every stat lands in a vacuum, stripped of the baseline that would make it meaningful.

Here's what frustrates me the most: the people publishing these numbers aren't stupid. They know how to run a query against a dataset. The choice to not include the baseline is a choice. "Claude commits go into repos with fewer stars than average" is just wrong and boring. "90% of Claude output floods low-engagement repos" is a story that gets shared.

It works in both directions too. The AI boosters do it just as aggressively. "Developers are 55% more productive with Copilot" — on what tasks, in what conditions, over what time window, measured by whom. The number floats free of context because the context would complicate the story.

The actual picture of AI in software development right now is messier and more interesting than either version. Coding agents are genuinely useful for a certain class of task (well-scoped, greenfield, low-stakes boilerplate) and genuinely bad at others (anything that requires understanding a large existing codebase, anything where the failure mode is subtle). The research that would actually help people is granular and boring. The research that travels is the stuff with a punchy number in the headline.

I'm not saying ignore AI stats. I'm saying the first question for any AI stat should be: compared to what? If there's no baseline, the number is decoration. Treat it that way.

The 90% figure got 247 upvotes on HN and the top comment pointing out the flaw got buried. That's where we are.
