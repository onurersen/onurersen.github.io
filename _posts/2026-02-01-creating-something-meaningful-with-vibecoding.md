---
layout: page
title: "Creating Something Meaningful with Vibe Coding"
author: "Berat Onur Ersen"
date: 2026-02-01
draft: false
permalink: /2026-02-01-creating-something-meaningful-with-vibecoding/
tags: [tech, personal, motivation]
---

As a musician playing in multiple acts, I spend a lot of time learning new material. Honestly, the standard workflow—struggling with recordings or scrubbing through YouTube videos to hear a particular part of a composition—has always been a frustration.

That personal pain point is what led me to build a simple tool, serving a simple purpose: Practice. I went hands-on to create a tool called **Musicurious AI**.

Sharing my process here is important because it was fundamentally different from how I’ve built software in the past.

---

### The "Vibe-Coding" Shift
I used an AI coding agent to handle the heavy lifting of the implementation. This "vibe-coding" approach allowed me to act more like a **Product Manager and Architect**, focusing on the "what" and "why" of the build, rather than getting bogged down in every line of syntax.

### The Problem
The idea came from a simple observation: practicing with static sound files or YouTube videos is deeply limiting.
* You cannot hear individual instruments clearly.
* You cannot shift the tone easily.
* You cannot slow down the drums without distorting the sound.
* You lack a visual map of the song structure.

I spoke with fellow musicians early on, and their feedback aligned perfectly. They didn't just want a better audio player; they wanted to take their practice sessions several steps further.

---

### Building for Production
Even with AI assistance, I ensured this wasn't just a prototype. It had to be **production-ready**.

* **AI Integration:** I designed a pipeline using **Demucs** (a specialized AI model) to separate audio stems and filter them cleanly.
* **Architecture:** I architected it to be **server-less and scalable** from day one, handling heavy media processing without the headache of managing servers.
* **Deployment-Ready:** I made the app deployable on the **Vercel** platform from the start, ensuring cloud and deployment readiness immediately.

### The Outcome
It’s been an interesting experiment. By offloading the coding grunt work to AI, I could focus entirely on talking to users and ensuring the architecture and implementation were solid.

If you’re curious about the code or the stack, the project is open-source here:
[https://github.com/onurersen/musicurious-ai](https://github.com/onurersen/musicurious-ai)

----
![picture alt](/img/creating-something-meaningful-with-vibecoding/musicurious.jpeg)