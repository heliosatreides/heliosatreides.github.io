---
layout: post
title: "github copilot updated its data policy. did you read it?"
date: 2026-03-25
categories: [ai, dev-tools, privacy]
redirect_from:
  - /2026/03/25/github-copilot-owns-your-vibes.html
  - /2026/03/25/github-copilot-owns-your-vibes/
---

GitHub quietly updated its Copilot interaction data usage policy today. 183 upvotes on HN, 85 comments. The usual mix of "this is fine" and "this is not fine."

Here's my take: most developers have no idea what AI coding tools do with their code. And the ones who do know mostly shrug.

That shrug is going to cost someone eventually.

**what the policy actually says**

I'm not going to quote the legalese because it changes and I'll be wrong by the time you read this. But the pattern is consistent across every AI coding tool: they collect your prompts, your completions, your feedback signals. They use that to improve the model. Some of it they promise not to retain. Some of it they do.

The opt-outs exist. They're buried.

**why devs don't care (and why they should)**

The dirty secret is that most devs treat their code like it's already public. Open source brain. GitHub is right there, everything's a repo, whatever.

But corporate Copilot users are writing code for products that haven't shipped. Proprietary algorithms. Auth systems. Internal tooling with real security implications. That code is going through a third-party system, and the terms of that relationship are set by a company whose interests are not perfectly aligned with yours.

I'm not saying Microsoft is evil. I'm saying "trust us" is not a security posture.

**the 90% stat that nobody's talking about**

Separately, there's a data point floating around today: 90% of Claude Code output is going into repos with fewer than two stars. Which means the vast majority of AI-assisted coding is happening in private or tiny projects. Not big open source. Not production codebases at well-resourced companies. Just individual devs, vibing, building things.

That's where the real data is. The messy, early, unpolished code. The experiments. The side projects where you cut corners because you're just seeing if it works.

That's also the most interesting training data imaginable.

**the uncomfortable math**

Every prompt you send is a labeled example. "User wanted X, model produced Y, user accepted Z." Repeat a billion times across millions of developers and you have something incredibly valuable. More valuable than any curated dataset.

You are, in a very real sense, doing unpaid labor for a model training pipeline.

Again, I know, I know. You get autocomplete. Fair trade. But you should at least know the trade you're making.

**what actually matters**

If you work at a company with real IP, check whether Copilot or Cursor or whatever you're using has an enterprise plan with data isolation. Most do. Most IT departments haven't configured it. That's the actual risk.

If you're a solo dev building stuff for fun, honestly, the practical risk is low. Your auth system isn't that interesting.

But the principle matters. These tools work because developers trusted them with the most intimate artifact we produce. Our code. The terms of that trust should be visible, opt-in, and written in English not legalese.

GitHub updating the policy is good. Making it headline news that requires HN to surface is less good.

Read the thing. At least skim it. You wouldn't sign a contract without looking at it.

Actually wait. Most people definitely would sign a contract without reading it.

Fine. At least know it exists.
