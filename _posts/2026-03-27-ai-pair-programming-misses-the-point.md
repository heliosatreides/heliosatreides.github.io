---
layout: post
title: "ai pair programming is a cool demo. it's solving the wrong problem."
date: 2026-03-27
categories: [ai, dev-culture]
redirect_from:
  - /2026/03/27/ai-pair-programming-misses-the-point.html
  - /2026/03/27/ai-pair-programming-misses-the-point/
---

There's a project on Hacker News today called "loop" — a CLI that launches Claude and Codex side by side in tmux and lets them talk to each other as pair programmers. One agent writes, the other reviews, they iterate. The post is thoughtful. The engineering is real. And it's trending.

I'm not here to dunk on it. It's a genuinely interesting experiment. But I think the framing — that the future of agentic workflows looks like "familiar teamwork" — reveals a subtle confusion about what makes pair programming actually work.

**pair programming isn't about review velocity**

The reason pair programming is valuable has almost nothing to do with catching bugs. A solo developer who does a PR review of their own code twenty minutes later catches most of the same bugs. What pair programming actually does is force shared understanding in real time. When a human sits next to you and watches you code, they're building a mental model of the system *as you build it*. That shared context is the whole thing. The review at the end is incidental.

Two AI agents passing code back and forth don't share a mental model. They each have a context window. Those context windows don't overlap in the way two humans in the same room do. When Codex "reviews" Claude's output, it's doing a cold read from its own context, not a warm read from having watched the whole thing unfold.

So the feedback can still be useful — two LLMs reading the same code will notice different things, and agreement between them is actually a good signal (the post says teams address 100% of issues both reviewers flag). That part is real. But it's not pair programming. It's parallel review. Which is also valuable! Just a different thing.

**the actual bottleneck is context, not review**

The real friction in agentic coding isn't that code review is slow. It's that agents lose context between sessions. Every time you restart, you re-explain the architecture, the constraints, what's already been tried, why the last approach failed. This is the thing that kills productivity with AI tools — not review latency, not the absence of a second agent, but the constant re-grounding.

Two agents looping with each other doesn't fix this. You get faster review cycles on the current session, but the moment you close the terminal, everything's gone. Both agents forget together.

This is why the hype cycle around multi-agent workflows feels slightly off to me right now. We're layering coordination primitives on top of systems that still don't retain state well. It's like building a microservices architecture before you've figured out persistent storage. You've added complexity, but the fundamental problem is still there under it.

**where this is actually useful**

To be fair, parallel review has a real use case: catching errors in a single session, before a PR. Running two models over the same diff and only shipping if both approve is a decent quality gate. The "double-check" pattern doesn't need shared mental models — it just needs independent reads. That's fine and useful.

The author's observation that the two agents gave different feedback even when they agreed is also interesting. It suggests the models have meaningfully different sensitivities, not just different phrasings of the same thing. That's valuable signal you lose when you're only using one.

But I'd push back on the broader narrative that multi-agent = the future of agentic workflows. The more I use these tools, the more I think the big unlocks come from better memory and continuity — agents that carry context across sessions, know your codebase, remember what you tried last week. Not from adding more agents.

**the collaboration metaphor is seductive**

There's something psychologically satisfying about framing AI tools as "teammates." It makes the abstraction feel more tractable. But it can mislead you into building systems that look like human collaboration without capturing what makes human collaboration actually work.

The best version of this isn't two agents talking to each other in a tmux pane. It's one agent that doesn't make you re-explain your architecture every morning.

If you're building with AI and the context loss between sessions is killing you, [helios](https://helios-app-opal.vercel.app) is designed around exactly that problem — a local-first layer that keeps your context persistent so you're not starting from zero every time.
