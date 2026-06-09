---
marp: true
theme: stef
paginate: true
footer: "How I Cloned Myself With Claude · Stefano Pineda"
---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _footer: "" -->

# How I Cloned Myself With Claude

## Building a real AI tool, live, from scratch

<!--
This is the capstone — everything before this was about what's worth building. Now I show you that you can actually build it.
One line to open: "I'm a mechanical engineer, not a software engineer. I used Claude to automate most of my Navy recruiting job — and if I can do it, the only thing standing between you and building is starting."
Set the run order: a real walkthrough, a tour under the hood, the transferable loop, and then we build something live in this room.
-->

---

## Who's talking

- **Zero** formal computer-science training
- Two **mechanical-engineering** degrees
- A **nuclear-Navy** background

<!--
I want to be precise about my credentials here, because they matter for the point. I have zero formal CS training. None.
What I do have: two mechanical-engineering degrees and a nuclear background from the Navy. That's engineering judgment and a reliability mindset — not software.
Yet I built working apps that took over the tedious, manual parts of my recruiting job. Hold that contradiction in your head for the next hour.
-->

---

<!-- _class: statement -->

> "I'm not technical enough to build with AI." That sentence is now false.

<!--
This is the myth I came here to kill. Say it slowly and let it land.
The terminal, databases, deployment — Claude does almost all of it now. The barrier that existed two years ago is gone.
Your job changed. It's no longer "can you code." It's "do you know what to build, and can you describe it well." That's it.
-->

---

<!-- _class: statement -->

# I cloned the tedious parts of my job.

<!--
"Cloned myself" isn't a metaphor for ego — it's literal. I took the repetitive, manual parts of my recruiting work and handed them to software I built.
Not to be lazy. To buy back time — which I'll come back to at the end as the whole point.
Everything I'm about to show you started as a task I was sick of doing by hand.
-->

---

## The new job description

- Old skill: **write the code**
- New skill: **know what to build** + **describe it well**
- The machine handles the rest

<!--
Let me make the reframe concrete before the demo. The skill that mattered for fifty years was: can you write the code.
That skill is now largely automated. The new job description is two things — knowing what to build, and describing it clearly enough.
Hold that lens through the gonupoc.com walkthrough: watch how little of it is "coding" and how much is "deciding and describing."
-->

---

<!-- _class: divider -->

### The centerpiece

# gonupoc.com

<!--
This is the heart of the talk. A real tool I built and shipped — not a toy, not a demo app that does nothing.
I already made a YouTube video about it, so I'll show you both the live product and that video.
Watch for three things: the problem it solves, the actual flow, and how unglamorous the build really was.
LIVE DEMO: have gonupoc.com open in a tab right now.
-->

---

## The problem it solves

- Recruiting has a **tedious, repetitive** intake/interview workflow
- Exactly the kind of manual task that **eats hours**
- The boring stuff nobody wants to do by hand

<!--
Every job has a part that's pure repetition — for me in recruiting it was the intake and interview workflow.
It's the same handful of steps, over and over, eating hours of my week. That's the signal you're looking for: repetition + time.
gonupoc.com exists for exactly one reason — to take that off my plate. Pick your own equivalent as I talk.
-->

---

## What it does

- A **finished, working** product — not a prototype
- Walk the **actual flow**, end to end
- Real users, real data, on the internet

<!--
Let me walk the real flow end to end so you see a finished product, not a slide about one.
DEMO BEAT: click through gonupoc.com live — show the entry point, the core action, and the output a real user gets.
The point of showing the whole thing is that it works. This is shipped software doing a real job, built by a non-engineer.
-->

---

## How it was built

- **Described it in plain English** to Claude
- **Iterated** — fixed what didn't work
- **Shipped** it

<!--
Here's the entire method, and it's almost insultingly simple. I described what I wanted in plain English. Claude built it.
Then I iterated — told it what was wrong, what to change, what to add — until it was right.
Then I shipped it. No CS degree was consulted at any point in that sentence.
-->

---

## The unglamorous middle

- It **didn't work** the first time
- I fixed it by **just... asking**
- No genius — a **conversation**

<!--
I want to be honest about the part demos usually hide: it didn't work the first time. Things broke. I got things wrong.
And the fix every single time was to describe the problem to Claude and ask it to fix it. That's the unglamorous middle.
That's the most important slide in this section — because that loop is the thing you can copy, and it requires zero brilliance.
-->

---

## Watch the build

![w:760](images/gonupoc-youtube.png)

<!--
DROP IN: a screenshot/thumbnail of your gonupoc.com YouTube video — save as slides/images/gonupoc-youtube.png
DEMO BEAT: play a short clip of the YouTube video here, or just point them to it.
This is the receipt — a recorded, public walkthrough of the whole build so nobody thinks I cherry-picked the demo.
-->

---

<!-- _class: statement -->

# This is a demo of a *process*, not a genius.

<!--
The takeaway from the entire gonupoc.com section, and the line I want them to remember.
I'm not smarter than the people in this room. I just ran a process — describe, iterate, ship — that anyone here can copy.
Now let me pull the back off the machine so the stack stops being scary.
-->

---

<!-- _class: divider -->

### Part 2

# What's actually under the hood

<!--
Time to demystify the stack. The intimidation comes from not knowing the names of the parts.
I'm genuinely proficient with all of these, and I'm going to name each one plainly.
The goal isn't to make you memorize them — it's so you know they exist and can ask Claude for them by name.
-->

---

## The app / the site

- The **front door** users see
- Buttons, screens, the thing people click
- Where the experience lives

<!--
First piece: the app or website itself. This is the front door — the part the user actually sees and touches.
Buttons, forms, screens. When you describe what a user should see and do, you're describing this layer.
Everything else on the next slides is invisible plumbing behind this front door.
-->

---

## Databases

- Where the **data lives**
- How you **store** and **retrieve** it
- The memory of your app

<!--
Databases are just where the data lives — the memory of your app. User records, intake answers, whatever your tool tracks.
You think about it in two motions: how do I store this, and how do I get it back later.
You don't need to write database code by hand. You need to know the word "database" so you can say "store this in the database."
-->

---

## Backups

- For databases **and** remote servers
- So a mistake **isn't fatal**
- The nuclear-Navy reliability mindset

<!--
Backups are boring and essential — the most nuclear-Navy thing in this talk. In the reactor world, you assume things fail and you plan for it.
Same here: you back up your databases and your servers so a mistake, or a bad deploy, isn't fatal. You can always roll back.
It's unglamorous, but it's the difference between an experiment and something you can actually trust with real data.
-->

---

## Hosting & domains

- **Buying a domain** — your address
- **Hosting** — putting the site on the internet
- gonupoc.com is exactly this

<!--
Hosting and domains are how a thing on your laptop becomes a thing on the internet.
A domain is your address — you buy it, like gonupoc.com. Hosting is the machine that serves your site to the world.
This used to feel like a dark art. It's now a few sentences to Claude plus a credit card for the domain.
-->

---

## Continuous deployment

- Ship changes **automatically**
- And **safely**
- Edit, push, it's live

<!--
Continuous deployment means when I make a change, it goes live automatically and safely — no manual ritual every time.
I edit, I push, and the new version is on the internet for users in moments.
This is what makes the iterate-and-ship loop fast enough to actually use. Slow deploys kill momentum.
-->

---

## Remote servers

- A computer **in a data center**, not your laptop
- Always on, doing the work for you
- Where the app and database actually *run*

<!--
Quick one: a remote server is just a computer that isn't your laptop — it lives in a data center and stays on.
Your app and your database run there so they're available 24/7, even when your laptop is closed.
You don't manage it by hand. You describe what you want and Claude configures it. Name it so you can ask for it.
-->

---

## Tools I actually use

- **Tailscale** — secure networking between machines
- **Resend** — sending email from your app
- **Remote servers** — the machines doing the work

<!--
A few named tools so they're not mysterious. Tailscale gives me a secure private network between my machines.
Resend is how my app sends email — confirmation messages, notifications, that kind of thing.
Remote servers are just computers in a data center doing the work instead of my laptop. Name-drop these so you can ask for them by name.
-->

---

## The terminal — the honest truth

- I'm comfortable in it...
- **With Claude, you barely touch it**
- I use it for ~**two** things now

<!--
The terminal is the black screen with text that scares people. Confession: I'm comfortable in it — but here's the honest truth.
With Claude, you barely touch it. It does the terminal work for you, described in plain English.
I use the terminal directly for maybe two things now: updating Claude itself, and spinning up tmux sessions. Everything else, I describe and Claude does it.
-->

---

<!-- _class: statement -->

# You don't memorize the stack. You ask for it *by name.*

<!--
This is the reframe for the whole under-the-hood section.
You will never memorize all of this, and you don't need to. I didn't memorize it either — I learned what exists.
Knowing a thing exists and what it's called is enough to ask Claude for it. That's the entire skill on the technical side.
-->

---

<!-- _class: divider -->

### Part 3

# The build loop

<!--
This is the transferable skill — the one thing I most want you to walk out with.
It's the same loop from the AI-automation framework we've been building toward all program.
Once you have this loop, the specific tool doesn't matter. You can point it at anything.
-->

---

<!-- _class: statement -->

> Spot a tedious task → describe it → iterate → ship → measure the time saved.

<!--
This is the loop. Read it out loud, beat by beat. Five steps.
Spot a tedious task. Describe it precisely. Iterate with the AI. Ship it. Then measure the time you got back.
gonupoc.com is just one full lap around this loop. The live build we're about to do is another. It never changes.
-->

---

## The bottleneck moved

- It's **not coding ability** anymore
- It's **problem selection** + **clear description**
- Engineering judgment **>** syntax

<!--
Here's the strategic point. The bottleneck used to be: can you write the code. That bottleneck is gone.
The new bottleneck is choosing the right problem and describing it clearly. That's judgment, not syntax.
And judgment is exactly what my MIT and Navy background gave me. The non-coding parts of my training turned out to be the valuable parts.
-->

---

## Ready, Fire, Aim

- Get a rough version **in front of reality fast**
- *Then* refine it
- Don't design for a year — *Masterson*

<!--
This is Michael Masterson's "Ready, Fire, Aim." Fire before you aim — get a rough version into reality fast, then correct.
gonupoc.com v1 was rough. I shipped it anyway and let real use tell me what to fix.
The enemy is the year-long perfect plan. Reality gives you better feedback in a day than planning gives you in a month.
-->

---

<!-- _class: divider -->

### Part 4

# Let's build something live

<!--
Now we do it together, with no net. This is the part I can't fake.
LIVE DEMO: Claude ready, a throwaway project/domain prepared so we don't stall.
I'm going to narrate every decision out loud — including the dead ends — so you see the real thinking, not a polished result.
-->

---

## You name the task

- Data cleanup?
- An **email drafter**?
- A simple **intake form**?

<!--
DEMO BEAT: ask the room for a tedious task right now. Take whatever they give me.
Good candidates: cleaning up messy data, a tool that drafts repetitive emails, a simple intake form. But I'll build whatever they name.
The whole point is that it's unscripted — they pick, and we build it on the spot.
-->

---

## When it breaks — and it will

- I **describe the problem** to Claude
- I **ask** for the fix
- We keep going

<!--
Set expectations honestly: during a live build, something will break. That's not failure — it's the demo.
DEMO BEAT: when it breaks, narrate it. "Okay, that's wrong — watch what I do." Then describe the problem to Claude in plain English and ask for the fix.
This is the exact moment that converts skeptics. They came expecting magic; what they get is a recoverable conversation anyone could have.
-->

---

## I narrate everything

- Every **decision** out loud
- Including the **dead ends**
- You see the **thinking**, not just the result

<!--
As I build, I'll say everything out loud — why I'm describing it this way, what I'd ask for next, where it breaks.
Especially the dead ends. When it doesn't work, you'll watch me just describe the problem to Claude and ask for the fix.
DEMO BEAT: ship the little tool live if at all possible, even rough. Seeing it actually run is what sells it.
-->

---

<!-- _class: statement -->

# Goal: someone leaves thinking *"I'm doing that tonight."*

<!--
That's the only success metric for the live build. Not that it's impressive — that it's obviously copyable.
If even one person leaves and builds their first thing tonight, this session worked.
That's a perfect handoff into why this skill is such a good bet right now.
-->

---

<!-- _class: divider -->

### Part 5

# Why this is a "house" game

<!--
Tie this straight back to the calculated-risk session — the house versus the gambler.
The house wins because the odds are structurally in its favor. I want you on that side of this trade.
Here's why building with these tools is, right now, a house bet.
-->

---

## The bottleneck is people

- The economy's constraint: **people who can ship** with these tools
- Tools are abundant — **builders are scarce**
- Build that capacity **early**

<!--
The constraint in the economy right now isn't the tools — they're cheap and everywhere. It's people who can actually ship with them.
That scarcity is exactly what makes the skill valuable. You're building supply where there's enormous demand.
Doing it early, while it's still scarce, is what makes you the house and not the gambler. The odds are in your favor.
-->

---

<!-- _class: statement -->

# I automated my job to **buy back time.**

<!--
Come back to the real reason. I didn't automate my recruiting job to be lazy.
I did it to buy back time — and time is the single most valuable asset there is. You can't make more of it.
Every tedious task you hand to software is hours returned to you for the things that actually matter.
-->

---

<!-- _class: divider -->

### Close

# Your homework

<!--
We're landing the plane. One concrete assignment, and then the floor is open.
This is the capstone of the whole program — I want you to leave having committed to an action, not just notes.
Make it specific and make it this week.
-->

---

## This week

- Pick **one** tedious task in your life
- Build a **first version** — rough is fine
- **Share results** next session

<!--
Here's the homework, and it's not optional in spirit. Pick one tedious task in your own life — school, work, anything repetitive.
Build a first version this week. Rough counts. Ready, Fire, Aim — ship something ugly.
Bring it back and share results next session. The act of starting is the entire lesson.
-->

---

## Open floor

- Tools — *what should I use?*
- *Where do I start?*
- *What do I build first?*
- The **gonupoc.com** video link

<!--
Open the floor and let the questions run — this is the 15-minute Q&A.
Anticipate the big four: what tools, where to start, what to build first, and "can I see the gonupoc.com video again."
Steer every answer back to the loop: pick a tedious task, describe it, iterate, ship, measure. Don't let "what tool" become a stall — the tool barely matters.
Drop the gonupoc.com YouTube link in the chat / on the board so everyone leaves with it.
-->

---

<!-- _class: lead -->

# The only thing standing between you and building is starting.

## Open floor: where do I start, what do I build first, the gonupoc.com link

<!--
Final line, said with full conviction: I'm a mechanical engineer with zero CS training, and I cloned the tedious parts of my job. The barrier is gone.
The only thing left is to start. That's not a motivational cliché here — it's literally the last remaining step.
Open the floor: tools, where to start, what to build first, and drop the gonupoc.com YouTube link for everyone.
LIVE-DEMO CHECKLIST recap: gonupoc.com open, video queued, Claude ready, throwaway project/domain prepared.
-->
