---
title: "An Honest Account"
datePublished: 2026-05-29T09:40:44.540Z
cuid: cmpqqeovw009d1sqkatzr9p9r
slug: an-honest-account
cover: https://cdn.hashnode.com/uploads/covers/69c5034110e664c5da98e1d7/40a5fadf-baec-4d40-8b3c-10ae4dd77869.jpg

---

I want to write this one differently, because I think there's more value in being honest about where something didn't go to plan than in pretending everything was smooth.

The goal was straightforward enough, i thought. the plan was to build a home lab environment that would let me get hands-on with Microsoft Sentinel, Microsoft's cloud-based security information and event management platform. A SIEM, in practical terms, is where security teams collect logs from across an organisation's environment, detect anomalies, and investigate potential threats. Getting comfortable with one before walking into a SOC role made sense to me. I set up a Windows 11 Pro virtual machine using UTM on my Mac. That part worked. The VM runs, it's functional, and getting there taught me more about virtualisation than I expected it to.

Then I hit the wall. The problem, which took me longer than I'd like to admit to properly diagnose, is that a virtual machine sitting locally on your laptop has no inherent relationship with Azure. Sentinel doesn't know it exists. For logs to flow into Sentinel, the machine needs to be onboarded — connected to a Log Analytics workspace via an agent that ships data to the cloud. That's the bridge I was missing, and understanding why it was missing required me to learn what I didn't know, which is its own kind of progress.

I'm still working through it. The honest answer is that I haven't completed what I set out to build yet. But I've learned that hitting a wall and diagnosing why it's there is a different skill from simply following a guided walkthrough and probably a more useful one for the actual work.

This post isn't a success story, and probably would have been suited more linkedin but alas. It's a work in progress, and I'll write the follow-up when I have more to show.