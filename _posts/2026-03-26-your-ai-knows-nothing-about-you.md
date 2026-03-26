---
layout: post
title: "your ai knows less about you than a wikipedia stub"
date: 2026-03-26
categories: [ai, personal-context, productivity]
redirect_from:
  - /2026/03/26/your-ai-knows-nothing-about-you.html
  - /2026/03/26/your-ai-knows-nothing-about-you/
---

There's a piece blowing up on Hacker News today about [personal encyclopedias](https://whoami.wiki/blog/personal-encyclopedias). The author documents their grandmother's wedding photos using MediaWiki — full infobox, linked stubs for every person, citations. 700+ upvotes and climbing.

The reaction is "that's beautiful." Mine is: why do we find it so easy to document a 50-year-old wedding in exquisite detail, but we can't get our own AI assistant to remember that we're a software engineer who hates standups and works on a side project every Sunday morning?

This isn't really about memory. It's about context. And we have almost no infrastructure for it.

---

Here's the thing about personal encyclopedias. The reason the grandmother's wedding becomes a proper documented artifact is because someone sat down and *decided it mattered*. They gave it structure. They connected it to the wider world. They made it queryable.

Your present-day self generates just as much contextually rich information every day. Your calendar, your open tabs, your half-finished todos, the budget spreadsheet you glanced at this morning, the Slack thread you agreed to follow up on. All of it is signal. None of it is structured. And critically, none of it flows anywhere.

Every AI assistant you open starts cold. You type "help me write a reply to this email" and the model has no idea:

- Who you are
- What company you work at
- What your relationship with this person is
- Whether you're behind on a deadline they mentioned last week
- What tone you actually use when you write

So you either re-explain yourself (again) or you get a generic reply that sounds like it was written for no one.

This is not a model capability problem. GPT-5 isn't going to fix this. The models are already smart enough. The problem is that nothing connects your life to the tools you're using.

---

The personal encyclopedia impulse is compelling because it imagines a version of you that's fully legible. Every person you know is a stub page. Every event you've lived through has a section header and a citation. It's Wikipedia for your own life.

That sounds insane until you realize: corporations already do this. Salesforce is basically a personal encyclopedia of every customer interaction your company has ever had. Every call, every deal, every note from every rep. The context is there because someone decided it was worth capturing and made a system for it.

Your life doesn't have a CRM. It has a notes app you stopped using in February.

---

I think the reason that HN post resonates is that people feel the absence of this. We've outsourced memory to our phones, but our phones don't synthesize. They store. Scroll through your camera roll and you'll find 4,000 photos you haven't looked at in three years. Scroll through your notes and you'll find fragments that made sense when you wrote them and mean nothing now.

The information exists. The structure doesn't.

And that gap is felt most acutely when you're trying to get help from an AI tool that could, theoretically, do a lot — if it only knew who you were.

---

The move isn't to retroactively document your past like a personal wiki (though that's genuinely cool). The move is to build persistent, living context about your present. What's on your plate right now. What you care about. What your patterns are.

That's a much smaller, more tractable problem. You don't need to catalog your grandmother's wedding. You need to tell your tools: here's who I am, here's what I'm working on, here's what matters this week.

Most tools aren't built to hold that. They open fresh every time. You get a smart model with amnesia.

That's the actual problem worth solving.

---

If you want an assistant that actually knows your context. what's on your calendar, where your finances are, what you were working on last session. [helios](https://helios-app-opal.vercel.app) is worth a look.
