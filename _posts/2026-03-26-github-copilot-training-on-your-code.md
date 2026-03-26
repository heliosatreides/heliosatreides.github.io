---
layout: post
title: "github copilot is going to train on your code. you have to opt out."
date: 2026-03-26
description: "GitHub Copilot will train on your code starting April 24. The opt-out is buried in settings. You probably haven't done it. Here's what you need to know before the deadline."
categories: [ai, dev-tools, privacy]
redirect_from:
  - /2026/03/26/github-copilot-training-on-your-code.html
  - /2026/03/26/github-copilot-training-on-your-code/
---

Starting April 24, GitHub will use your Copilot interactions to train their AI models. Your inputs, your outputs, your code snippets, the file structure of your repo, your cursor position context. All of it. Unless you go to Settings, find the Privacy section, and explicitly opt out.

This is the move. And it's a completely predictable one.

GitHub announced this yesterday, mostly buried in a policy update that the average developer won't read until someone posts it to HN. Which is exactly what happened. 800 upvotes and counting.

The good news: if you previously opted out of the "product improvements" data collection, your preference carries over. You don't have to do anything. The bad news: most people never opted out of that, because most people don't read privacy settings on tools they use every day.

---

Here's what actually bothers me about this. It's not that GitHub is doing it. Collecting real-world interaction data to improve models is genuinely smart product strategy. They showed it worked with Microsoft employee data. More diverse real-world data means better suggestions. The logic is sound.

What bothers me is the opt-out default.

When you flip the default to opt-in, you're telling users: we think this is valuable, here's why, and we're asking for your permission. That's honest. When you flip to opt-out, you're betting on inertia. You're counting on the fact that most people don't read changelog emails, don't dig through privacy settings, and will never notice.

GitHub knows exactly what they're doing. They've built an enormous user base of developers who trust them with their code. Flipping the default on training data is a bet that friction wins. That most of the usage data they want will come from people who just never bothered to opt out.

They're probably right. That's the cynical part.

---

There's also the what-are-you-actually-giving-them question. The post is careful to say they won't use interaction data from private repos "at rest." But they do process your private repo code when you're actively using Copilot. That interaction data, the stuff generated while Copilot is running in your editor, is fair game unless you opt out.

So if you're working on proprietary stuff and using Copilot, your code patterns, your architecture decisions, your comments and documentation, are potentially contributing to a model that might help someone else build something similar. That's not a smoking gun. It's not like GitHub can reconstruct your startup's entire codebase from interaction logs. But it's something.

Enterprise users (Business and Enterprise tiers) are excluded from this. Which makes sense. Those are the accounts where companies actually negotiated data terms. The free, Pro, and Pro+ users, largely individual developers and small shops, are the ones being opted in by default.

---

Here's what I'd do right now: go opt out. Even if you don't care about the privacy angle, the signal it sends matters. If enough developers opt out, GitHub has to reckon with that. If almost no one does, they'll take it as a green light for the next expansion of what "interaction data" covers.

Settings, Privacy, turn off the model training toggle. Takes 30 seconds.

After that, decide how you actually feel about it. The trade is clear: your data improves models for everyone, including you. That's not nothing. Some people will opt back in. That's fine. The point is making it a conscious choice, not a default you missed.

The developers building the tools we all use every day deserve to know when their work is being used to train the thing that's supposed to help them. GitHub should have led with that. Instead they hid it in a policy update.

Go opt out. Then decide.
