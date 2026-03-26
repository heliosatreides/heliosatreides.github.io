---
layout: post
title: "video.js got 88% smaller and nobody should be surprised why"
date: 2026-03-25
description: "videojs shrunk its bundle by 88% and it barely made the news. Sometimes the most important engineering work is the kind nobody wants to write a Medium post about."
categories: [open-source, javascript, dev]
redirect_from:
  - /2026/03/25/video-js-got-88-percent-smaller.html
  - /2026/03/25/video-js-got-88-percent-smaller/
---

The creator of Video.js "took it back" after 16 years and rewrote it to be 88% smaller. The HN thread hit 537 points. Which means roughly 537 people thought "yeah, sounds about right."

That reaction says more than the repo does.

Video.js has been around since 2010. It's one of those open source projects that outlived its original purpose, got adopted by corporations, bloated with enterprise feature requests, and slowly became a maintenance burden nobody wanted. The creator eventually left. The project kept going. That's how these things work.

But 16 years later, he came back. Rewrote it. Made it 88% smaller.

That's not a refactor. That's a confession.

88% smaller means the original version was mostly cruft. Years of compatibility shims, plugin architectures that nobody used, features added because a big company filed a ticket. The core of what the library needed to do could be expressed in 12% of the code that shipped. The other 88% was organizational debt dressed up as features.

This happens to every project that gets popular. The original author has a clear vision. The project gets adopted. The issue tracker fills up. Pull requests arrive from people who need edge cases handled. Backward compatibility becomes a religion. The project grows not because the core problem got harder, but because the software absorbed the complexity of every organization that used it.

And then one day you look at the codebase and you don't recognize it.

The interesting part of the Video.js story isn't the 88% reduction. It's that it took 16 years and a full takeback to make it happen. Nobody currently maintaining a project with 50k GitHub stars is going to wake up tomorrow and ship a breaking rewrite that cuts 88% of the codebase. The incentives don't allow for it. Someone will file a bug. A major company will say they're blocked. The PR will sit in review for months and eventually close.

Original founders have a superpower here. They're allowed to make the call that the current maintainers can't. "I built this. The new version is smaller and better. Migrate or fork." Nobody can argue with that the same way they'd argue with a committee.

The web is full of libraries that are 5x larger than they need to be because of this pattern. Each extra kilobyte has a story: a company that needed RTMP support, a polyfill for IE8, a plugin API nobody uses but everyone depends on. The original authors moved on. The libraries stayed.

The fix is always the same: go back to first principles. What does this thing actually need to do? Strip everything else. Ship it.

Most people can't do that because they're afraid of breaking things. The original author is the only one who can say "this is what I intended" and have it mean something.

Video.js 8 is a better library because one person remembered what it was supposed to be.

More projects should get taken back.
