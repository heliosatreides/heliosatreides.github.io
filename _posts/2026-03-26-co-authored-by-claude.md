---
layout: post
title: '"co-authored by claude" is now just a commit message'
date: 2026-03-26
description: "'Co-authored by Claude' is now just a commit message. What happened when AI went from assistant to co-author — and what that means for code ownership, review, and accountability."
categories: [ai, dev-culture]
redirect_from:
  - /2026/03/26/co-authored-by-claude.html
  - /2026/03/26/co-authored-by-claude/
---

Ninety percent of Claude's API output is going to GitHub repos. That number hit HN today and people are treating it like a revelation. It's not. Walk through claudescode.dev for thirty seconds and you'll see a live feed of commits — real repos, real code, co-authored by Claude Opus, Claude Sonnet, various flavors — shipping every few seconds.

We passed a threshold somewhere in the last few months. AI tools stopped being autocomplete and became committers.

That's worth sitting with for a second.

---

When Copilot launched, the pitch was "it helps you write code faster." You were still the author. You drove. The AI rode shotgun and occasionally handed you a piece of paper with the right syntax on it.

What's happening now is different. The coding agent loop — read repo, write plan, implement, test, iterate, commit — that's not assistance. That's delegation. The developer reviews the diff and either ships it or steers. But the raw output, the actual keystrokes that became production code, came from the model.

Not everyone is comfortable calling that what it is. There's a lot of hedging. "The developer is still in the loop." Sure. The developer is also "in the loop" when they approve a PR from a junior engineer they trust. We don't pretend that engineer didn't write the code.

---

The interesting question isn't whether this is happening. It clearly is. The interesting question is what happens to software quality now.

The optimistic read: code gets written faster, more tests get written, more edge cases get caught, shipping velocity increases across the board. Small teams suddenly have the output of much larger ones.

The pessimistic read: we're generating an enormous amount of plausible-looking code that mostly works, and the bugs that slip through are going to be the weird ones. The ones where behavior is technically correct but contextually wrong. The ones no automated test catches because you'd need to understand the business to know something's off.

I lean toward something in the middle. AI coding agents are genuinely good at the stuff that's well-defined: auth flows, CRUD endpoints, component boilerplate, docs, tests for known behavior. They're worse at the stuff that requires judgment: what *should* this do, is this architecture going to hurt us in six months, does this feature actually solve the user's problem.

That second category is also where most of the expensive mistakes live.

---

The shift this creates for developers is real. If you're spending most of your time on implementation, your job is changing. Not disappearing — changing. The leverage is moving toward people who can articulate problems clearly, review code well, and make good architecture calls. The people who can give an AI agent a clear brief and know when the output is wrong.

That's not a smaller skill set. It's a different one.

The developers who are struggling with this are the ones who conflate "writing code" with "doing the job." The job was always understanding the system well enough to make it do the right thing. Writing code was just the primary interface for that.

Now there are more interfaces.

---

The other thing the 90% number tells you: Anthropic built a moat by going deep on the coding use case. Claude's context window, its ability to hold a large codebase in mind, its instruction-following on complex multi-step tasks. That's not an accident. That's a product bet that paid off.

OpenAI knows this. Google knows this. Everyone's racing to own the place where developers actually spend their time.

In the meantime, the live feed on claudescode.dev keeps scrolling. Auth flows, bug fixes, data pipelines, feature work. One commit every few seconds.

All of it shipped. Most of it probably works.
