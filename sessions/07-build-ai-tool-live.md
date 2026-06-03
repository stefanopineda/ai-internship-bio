# How I Cloned Myself With Claude
### Building a Real AI Tool, Live, From Scratch

**Format:** ~60 min (45 min talk + live build + 15 min Q&A)
**One-liner:** I'm a mechanical engineer, not a software engineer. I used Claude to automate most of my Navy recruiting job. If I can do it, the only thing standing between you and building is starting.
**Placement:** This is the capstone — run it *after* the value, sales, and incentives sessions so students build something that's actually worth building.

---

## Hook (4 min)
- I have zero formal computer-science training. Two mechanical-engineering degrees and a nuclear background — that's it. Yet I built working apps that took over the tedious, manual parts of my recruiting job.
- The myth I want to kill in this room: *"I'm not technical enough to build with AI."* That sentence is now false. The terminal, databases, deployment — Claude does almost all of it. Your job became *knowing what to build and describing it well.*

## Part 1 — The Real Walkthrough: gonupoc.com (15 min)
The centerpiece — a live walkthrough of a real tool I built and shipped (I already made a **YouTube video** about it; I'll show the build and the video):
- **The problem it solves:** the tedious, repetitive interview/intake workflow in recruiting — exactly the kind of manual task that eats hours.
- **What it does:** walk the actual flow end to end so students see a *finished, working* product, not a toy.
- **How it was built:** described in plain English to Claude, iterated, shipped. Show the unglamorous middle — the parts that didn't work the first time and how I fixed them by just... asking.
- **The takeaway:** this isn't a demo of a genius. It's a demo of a *process* anyone in the room can copy.

## Part 2 — What's Actually Under the Hood (10 min)
Demystify the stack so it stops being intimidating. I'm proficient with these, and I'll name them plainly:
- **Building the app / the site** — the front door users see.
- **Databases** — where the data lives; how to think about storing and retrieving it.
- **Backups** — for databases and remote servers, so a mistake isn't fatal (boring, essential, the nuclear-Navy reliability mindset applied to software).
- **Hosting & domains** — buying a domain, putting a site on the internet.
- **Continuous deployment** — ship changes automatically and safely.
- **Tools I actually use:** Tailscale (secure networking between machines), Resend (sending email from your app), remote servers.
- **The terminal** — I'm comfortable navigating it, but here's the honest truth: **with Claude, you barely touch it.** I use it directly for maybe two things now — updating Claude itself and spinning up tmux sessions. Everything else, I describe and Claude does.
- **The reframe:** you don't need to *memorize* this stack. You need to know it *exists* so you can ask for it by name.

## Part 3 — The Build Loop (the transferable skill) (6 min)
The exact loop I teach, the same one from the AI-automation framework:
> **Spot a tedious task → describe it precisely → iterate with the AI → ship → measure the time saved.**
- The bottleneck is no longer coding ability — it's **problem selection and clear description.** Engineering judgment (which I got from MIT/Navy) matters more than syntax.
- *Ready, Fire, Aim (Masterson):* get a rough version in front of reality fast, then refine. Don't design for a year.

## Part 4 — Build Something Live (10 min)
- Take a tedious task **the students name on the spot** and build a small working tool for it in front of them — data cleanup, an email drafter, a simple intake form, whatever the room suggests.
- Narrate every decision out loud so they see the thinking, including the dead ends. The goal is for someone to leave thinking *"I'm doing that tonight."*

## Part 5 — Why This Is a "House" Game (4 min)
- Tie back to the calculated-risk session: the bottleneck in the economy right now is *people who can actually ship with these tools.* Building that capacity early makes you the house, not the gambler.
- I automated my own job not to be lazy but to **buy back time** — the most valuable asset there is.

## Close + Q&A (15 min)
- **Homework:** every student picks one tedious task in their life and builds a first version this week. Share results next session.
- Open floor: tools, "where do I start," "what do I build first," the gonupoc.com video link.

---
**Referenced:** my gonupoc.com build + YouTube video; *Ready, Fire, Aim* (Masterson).
**Live-demo checklist:** have gonupoc.com open, the YouTube video queued, Claude ready, and a throwaway project/domain prepared so the live build doesn't stall.
