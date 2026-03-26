---
layout: post
title: "sora was always going to die"
date: 2026-03-26
categories: [ai, product, economics]
redirect_from:
  - /2026/03/26/sora-was-always-going-to-die.html
  - /2026/03/26/sora-was-always-going-to-die/
---

OpenAI killed Sora on March 24th. The eulogies are already rolling in. "Too early." "Had so much promise." "Big tech wins again."

None of that is right. Sora died because the math was never there, and everyone pretending otherwise was either not looking at the numbers or didn't want to.

Here's the number that matters: $15 million per day in estimated inference costs at peak. Against it: $2.1 million in total lifetime revenue from in-app purchases. Not per day. Total. Ever.

That's not a product that got killed too soon. That's a product that was burning through its own funeral costs for months before anyone official said it out loud.

## the demo-first trap

The thing is, Sora was genuinely impressive. The first videos OpenAI released were stunning. Realistic physics. Consistent lighting. Objects that behaved like objects. When it launched publicly, everyone lost their minds.

But "impressive demo" and "viable product" are two completely different things, and AI labs have been confusing them for a while now.

ChatGPT worked because the inference cost per text query is cheap enough to build a subscription business on. You charge $20/month and it pencils out. Video is fundamentally different. Generating a few seconds of video requires rendering hundreds of frames, each one essentially a separate model inference pass with spatial reasoning, physics simulation, temporal consistency. The compute budget per output is orders of magnitude higher than text.

The economics of a $20/month consumer subscription never made sense for a product that costs this much per use. OpenAI had to know this. They shipped anyway, probably hoping that compute costs would fall fast enough, or that enterprise deals would cover the gap. The $1 billion Disney partnership was supposed to be part of that story. That deal is now dead too.

## who got hurt

Users didn't get much warning. Some had paid for credits that are now worthless. That's a bad look, and it's the kind of thing that erodes trust in the broader category. When AI companies move fast and pull products, it's the people who actually relied on them who pay.

Content creators who built workflows around Sora have to start over. Again. It's the same thing that happened with every tool that got quietly enshittified or shut down: Notion AI features that changed, Midjourney's pricing pivots, APIs deprecated with two weeks notice.

The message it sends is: don't build on us. Which is a problem when you're trying to be a platform.

## the unit economics are the strategy

Here's the actual lesson, and it applies beyond Sora.

You can raise infinite money. You can build something that impresses every journalist in the valley. You can get 900 million weekly active users on your text product. None of that rescues a thing with broken unit economics.

Video generation at consumer scale is not solved. The inference cost curve hasn't fallen fast enough. Maybe it gets there in two years. Maybe three. But launching a consumer product that burns $15M/day on the bet that costs will drop in time is not a product strategy. It's a press strategy that got out of hand.

The companies building in AI right now should be asking this question before they launch anything: at realistic usage, does this product make money, or at least have a credible path to making money? Not "could this make money if compute gets 10x cheaper." At current costs, today, does it work?

Most things don't survive that question. That's not cynicism. That's just how products work.

## what comes next

OpenAI is pivoting toward robotics. That's interesting, because the unit economics of physical hardware are different from cloud inference, and there are natural pricing floors (you can charge a lot for a robot). Whether they can execute is a different question.

The video generation market doesn't disappear. Runway, Kling, and others are still standing. Some of them have more sustainable cost structures, or at least are earlier in the process of figuring it out. The demand for AI video is real. Sora's failure is a cautionary tale about one approach, not the whole category.

But for now: Sora is a $15 million per day lesson that flashy demos are not products. Everyone building in AI should read it carefully.
