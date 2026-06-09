# How I Cloned Myself With Claude — Talking Notes

> One section per slide. Bullets to discuss — talk to the room, don't read them. Slide numbers match the deck.

## Slide 1 — How I Cloned Myself With Claude (title)
- Open with the one-liner: "I'm a mechanical engineer, not a software engineer. I used Claude to automate most of my Navy recruiting job. If I can do it, the only thing standing between you and building is starting."
- Frame this as the capstone — every prior session was about *what's worth building* (value, sales, incentives). This one proves you can actually build it.
- Lay out the run of show: a real walkthrough of gonupoc.com, a tour under the hood, the transferable build loop, then a live build the room picks.
- Energy check: this is the session people came for. Promise them they'll leave able to start tonight.

## Slide 2 — Who's talking
- Be precise and a little blunt about credentials: zero formal computer-science training. None.
- What I do have: two mechanical-engineering degrees and a nuclear-Navy background. That's engineering judgment and a reliability mindset — not software.
- The contradiction is the whole point: a non-engineer built and shipped working apps that took over the tedious parts of a real job.
- Tell them to hold that contradiction for the next hour — it's the proof that the old barrier is gone.

## Slide 3 — "I'm not technical enough to build with AI." That sentence is now false.
- This is the kill-the-myth moment. Say it slowly; let the room sit with it.
- The terminal, databases, deployment — Claude does almost all of it. The barrier that existed even two years ago is gone.
- Reframe the job: it's no longer "can you code," it's "do you know what to build, and can you describe it well."
- Transition: "Let me show you exactly what I mean with something real I shipped."

## Slide 4 — I cloned the tedious parts of my job.
- "Cloned myself" is literal, not ego: I took the repetitive, manual parts of recruiting and handed them to software I built.
- Motive matters — not laziness, but buying back time (foreshadow the closing point).
- Every tool I'll show started life as a task I was sick of doing by hand.
- Invite them to start spotting their own equivalent now.

## Slide 5 — The new job description
- Make the reframe concrete before the demo. The skill that mattered for fifty years: can you write the code.
- That skill is now largely automated. The new job description is two things — knowing what to build, and describing it clearly.
- Set the lens for the gonupoc.com walkthrough: watch how little of it is "coding" and how much is "deciding and describing."
- This is the bridge from the abstract myth-busting into a real, concrete example.

## Slide 6 — gonupoc.com (divider)
- This is the centerpiece — the real tool I built and shipped. Not a toy, not a do-nothing demo.
- Mention there's already a YouTube video about it; I'll show both the live product and the video so nobody thinks I cherry-picked.
- Tell them what to watch for: the problem it solves, the actual flow, and how unglamorous the build really was.
- DEMO PREP: gonupoc.com open in a tab before you start this section.

## Slide 7 — The problem it solves
- Recruiting has a tedious, repetitive intake/interview workflow — the same handful of steps over and over.
- It eats hours every week. That's the signal: repetition + time spent = automation candidate.
- This is the kind of manual task the whole AI-automation framework targets.
- Ask them silently to map their own equivalent tedious workflow while I talk.

## Slide 8 — What it does
- Walk the actual flow end to end so they see a *finished, working* product — not a slide describing one.
- DEMO BEAT: click through gonupoc.com live — entry point, the core action, the output a real user gets.
- Emphasize: it works, real users, real data, on the internet. Shipped software doing a real job, built by a non-engineer.
- Contrast with the "AI builds toy demos" skepticism — this is the opposite.

## Slide 9 — How it was built
- The entire method, almost insultingly simple: described what I wanted in plain English; Claude built it.
- Then iterated — told it what was wrong, what to change, what to add — until it was right.
- Then shipped. No CS degree consulted at any point.
- This is the lap of the build loop they'll see formalized in Part 3.

## Slide 10 — The unglamorous middle
- Honesty beat: it did NOT work the first time. Things broke; I got things wrong.
- The fix every time: describe the problem to Claude and ask it to fix it. That's it.
- This is arguably the most important slide in the section — the loop requires zero brilliance, just persistence and clear description.
- Demos usually hide this. I'm showing it on purpose because it's the copyable part.

## Slide 11 — Watch the build (YouTube video)
- DROP IN before the talk: a screenshot/thumbnail of the gonupoc.com YouTube video at slides/images/gonupoc-youtube.png.
- DEMO BEAT: play a short clip here, or point them to the full video and promise the link at the end.
- Frame it as the receipt — a public, recorded walkthrough of the whole build so nobody thinks the live demo was staged.
- Keep it short; don't let the video eat the live energy.

## Slide 12 — This is a demo of a *process*, not a genius.
- The takeaway line for the whole gonupoc.com section. Deliver it with conviction.
- I'm not smarter than anyone here. I ran a process — describe, iterate, ship — that anyone can copy.
- Transition: "Now let me pull the back off the machine so the stack stops being intimidating."

## Slide 13 — What's actually under the hood (divider)
- The intimidation comes from not knowing the names of the parts. We're going to name them.
- I'm genuinely proficient with all of these and will say each one plainly.
- The goal is NOT memorization — it's knowing each thing exists so you can ask Claude for it by name.
- Keep the tone demystifying, not lecturing.

## Slide 14 — The app / the site
- The front door users see — buttons, screens, forms, the thing people click.
- When you describe what a user should see and do, you're describing this layer.
- Everything on the next few slides is invisible plumbing behind this front door.
- gonupoc.com's screens are this layer made concrete.

## Slide 15 — Databases
- Just where the data lives — the memory of your app (user records, intake answers, whatever you track).
- Two motions: how do I store this, how do I get it back later.
- You don't write database code by hand; you need the *word* so you can say "store this in the database."
- Reassure: the scary-sounding part is a vocabulary problem, not a skill problem.

## Slide 16 — Backups
- The most nuclear-Navy thing in the talk: assume things fail, plan for it.
- Back up databases AND servers so a mistake or bad deploy isn't fatal — you can always roll back.
- Boring and essential. It's the difference between an experiment and something you trust with real data.
- Tie to the reliability mindset I brought from the reactor world.

## Slide 17 — Hosting & domains
- How a thing on your laptop becomes a thing on the internet.
- A domain is your address — you buy it, like gonupoc.com. Hosting is the machine serving your site to the world.
- Used to feel like a dark art; now it's a few sentences to Claude plus a credit card for the domain.
- Point back at gonupoc.com as the live example of both.

## Slide 18 — Continuous deployment
- When I make a change, it goes live automatically and safely — no manual ritual each time.
- Edit, push, it's live for users in moments.
- This is what makes the iterate-and-ship loop fast enough to actually use; slow deploys kill momentum.
- Connect: speed of deployment is why Ready, Fire, Aim is even possible.

## Slide 19 — Remote servers
- A remote server is just a computer that isn't your laptop — it lives in a data center and stays on.
- Your app and database run there so they're available 24/7, even when your laptop is closed.
- You don't manage it by hand; you describe what you want and Claude configures it.
- Name it so you can ask for it — that's the whole point of this stack tour.

## Slide 20 — Tools I actually use
- Tailscale — a secure private network between my machines.
- Resend — how my app sends email (confirmations, notifications).
- Remote servers — recap: the always-on machines doing the work instead of my laptop.
- Name-drop on purpose: you only need to know they exist to ask for them by name.

## Slide 21 — The terminal — the honest truth
- The black screen with text that scares people. I'm comfortable in it — but here's the honest truth.
- With Claude, you barely touch it; it does the terminal work, described in plain English.
- I use it directly for maybe two things now: updating Claude itself, and spinning up tmux sessions. Everything else, I describe and Claude does.
- This is the single most liberating fact for non-technical people in the room.

## Slide 22 — You don't memorize the stack. You ask for it by name.
- The reframe for the whole under-the-hood section.
- You'll never memorize all of it and you don't need to — I didn't either. I learned what exists.
- Knowing the name is enough to ask Claude for it. That's the entire technical skill.
- Transition into the loop that ties it all together.

## Slide 23 — The build loop (divider)
- The transferable skill — the one thing I most want them to walk out with.
- Same loop from the AI-automation framework we've built toward all program.
- Once you have the loop, the specific tool doesn't matter — point it at anything.
- Set up the next slide as "here it is, five steps."

## Slide 24 — Spot a tedious task → describe → iterate → ship → measure
- Read it beat by beat: spot a tedious task, describe it precisely, iterate with the AI, ship, then measure time saved.
- gonupoc.com was one full lap; the live build will be another. The loop never changes.
- "Measure the time saved" matters — it's how you prove the thing was worth building (and motivates the next one).
- This is the slide to photograph; tell them so.

## Slide 25 — The bottleneck moved
- The old bottleneck — can you write the code — is gone.
- The new bottleneck: choosing the right problem and describing it clearly. That's judgment, not syntax.
- Judgment is exactly what MIT and the Navy gave me. The non-coding parts of my training turned out to be the valuable parts.
- Reassure the room: your domain expertise IS the moat now, not a deficit.

## Slide 26 — Ready, Fire, Aim
- Michael Masterson's "Ready, Fire, Aim" — fire before you aim. Get a rough version into reality fast, then correct.
- gonupoc.com v1 was rough; I shipped anyway and let real use tell me what to fix.
- The enemy is the year-long perfect plan. Reality gives better feedback in a day than planning gives in a month.
- Hand off into the live build: "So let's stop talking and do exactly that, right now."

## Slide 27 — Let's build something live (divider)
- We do it together with no net — the part I can't fake.
- LIVE DEMO PREP: Claude ready, a throwaway project/domain prepared so we don't stall.
- I'll narrate every decision out loud, including dead ends, so they see real thinking not a polished result.
- Manage expectations: it might break, and that's the point — watch how I recover.

## Slide 28 — You name the task
- DEMO BEAT: ask the room for a tedious task right now and take whatever they give.
- Good candidates if they're shy: data cleanup, an email drafter, a simple intake form — but build whatever they name.
- The unscripted pick is what makes it believable. Lean into not knowing what's coming.
- Pick something achievable in the time box; steer gently if needed.

## Slide 29 — When it breaks — and it will
- Set expectations honestly: during a live build, something will break. That's not failure — it's the demo.
- DEMO BEAT: when it breaks, narrate it. "Okay, that's wrong — watch what I do," then describe the problem to Claude and ask for the fix.
- This is the moment that converts skeptics: they expected magic; they get a recoverable conversation anyone could have.
- Mirrors the "unglamorous middle" of gonupoc.com — same move, live.

## Slide 30 — I narrate everything
- Say everything out loud: why I describe it this way, what I'd ask next, where it breaks.
- Especially the dead ends — when it fails, show me describing the problem to Claude and asking for the fix.
- DEMO BEAT: ship the little tool live if at all possible, even rough. Seeing it run is what sells it.
- Keep talking through silences while Claude works; narrate the wait.

## Slide 31 — Goal: someone leaves thinking "I'm doing that tonight."
- The only success metric for the live build: not impressive, *obviously copyable*.
- If even one person leaves and builds their first thing tonight, the session worked.
- Use it as the emotional hinge into "why this is such a good bet right now."
- Maybe ask for a show of hands: who has a task in mind already?

## Slide 32 — Why this is a "house" game (divider)
- Tie straight back to the calculated-risk session — the house vs. the gambler.
- The house wins because the odds are structurally in its favor; I want them on that side.
- Set up the next slide: here's specifically why building with these tools is a house bet.
- Keep the through-line tight with the earlier session so it feels like a payoff.

## Slide 33 — The bottleneck is people
- The constraint right now isn't the tools — they're cheap and everywhere. It's people who can actually ship with them.
- That scarcity is what makes the skill valuable: you're building supply where demand is enormous.
- Doing it early, while builders are scarce, is what makes you the house, not the gambler — the odds tilt to you.
- Connect back to Slide 25: the bottleneck moved from code to judgment-plus-shipping, and few people have crossed it yet.

## Slide 34 — I automated my job to buy back time.
- The real reason, stated plainly: not laziness — buying back time.
- Time is the single most valuable asset; you can't make more of it.
- Every tedious task handed to software is hours returned for the things that actually matter.
- Personalize: name what I did with the time I got back, if appropriate.

## Slide 35 — Your homework (divider)
- Landing the plane. One concrete assignment, then open floor.
- This is the capstone of the whole program — I want them to leave committed to an action, not just notes.
- Make it specific and time-boxed: this week.
- Build anticipation for the next slide's exact ask.

## Slide 36 — This week
- Pick one tedious task in your own life — school, work, anything repetitive.
- Build a first version this week. Rough counts. Ready, Fire, Aim — ship something ugly.
- Bring it back and share results next session; the act of starting is the entire lesson.
- Offer to help unstick anyone who can't pick a task — that's the most common failure point.

## Slide 37 — Open floor
- Open the 15-minute Q&A and let the questions run.
- Anticipate the big four: what tools, where to start, what to build first, and "can I see the gonupoc.com video again."
- Steer every answer back to the loop: pick a tedious task, describe it, iterate, ship, measure. Don't let "what tool" become a stall — the tool barely matters.
- Drop the gonupoc.com YouTube link in the chat / on the board so everyone leaves with it.

## Slide 38 — The only thing standing between you and building is starting. (close)
- Final line with full conviction: mechanical engineer, zero CS training, cloned the tedious parts of my job — the barrier is gone.
- The only step left is to start. Not a cliché here — literally the last remaining step.
- Restate the open floor: tools, where to start, what to build first; reshare the gonupoc.com YouTube link.
- LIVE-DEMO CHECKLIST recap to verify before the session even begins: gonupoc.com open, video queued, Claude ready, throwaway project/domain prepared.

---

### Live-demo checklist (verify before you start)
- gonupoc.com open in a browser tab.
- gonupoc.com YouTube video queued; thumbnail saved at slides/images/gonupoc-youtube.png.
- Claude ready and signed in.
- A throwaway project/domain prepared so the live build doesn't stall.
