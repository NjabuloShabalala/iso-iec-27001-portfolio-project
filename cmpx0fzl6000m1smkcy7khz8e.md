---
title: "KC7"
datePublished: 2026-06-02T19:08:18.282Z
cuid: cmpx0fzl6000m1smkcy7khz8e
slug: kc7
cover: https://cdn.hashnode.com/uploads/covers/69c5034110e664c5da98e1d7/baded30e-1e72-4a75-9dcc-336ce64cee22.jpg

---

Most of what I'd learned about threat detection and advanced threat hunting up to this point had been conceptual, and I'm thankful that I found KC7 because it changed that.

KC7 is a platform built by Microsoft's threat intelligence team, and the premise is simple. You're given a simulated breach. Real-world attack scenarios, fictional companies, and actual data. And you have to figure out what happened using KQL, which has been quite interesting. The same query language that analysts use in Microsoft Sentinel day to day. No hints beyond what the data itself tells you. I'm currently halfway through the Security Analyst 2 track, three modules into seven, and I can't even pretend I've been breezing through it.

KQL itself has a logic to it that took me a little longer than I thought to internalise. The basic idea is that you're querying tables of data logs, events, and network connections and asking "them" questions to get you a step closer to the bigger picture such as who connected to this IP address? What files were accessed in this window of time? Did this user's behaviour change after this event? The queries start simple and get progressively more demanding as the scenarios get more complex, which is actually really interesting. I'm enjoying threat hunting a lot more than I thought I would.

What I've found genuinely interesting is how investigative the work actually is. You're not just running queries, you're building a picture, following a thread, deciding what matters and what's noise. There's a moment in each scenario where something clicks, and the shape of what happened becomes visible in the data. That moment is what I imagine draws people to this kind of work long-term. I'll hopefully write a follow-up when I've completed the full track. For now, halfway through feels like exactly the right place to be far enough in to know what I'm doing, close enough to the end to know what I still have to learn. I know that sounds generic and extremely LinkedIn, but please be patient with me, I'm still figuring all of this out.