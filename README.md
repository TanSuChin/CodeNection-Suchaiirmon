# CodeNection-Suchaiirmon


# Ballast

**A workload-awareness app that helps university students see how much they're carrying — and put some of it down.**

Ballast is a  project  exploring student burnout prevention. It is explicitly **not a productivity app** — it does not push students to do more. It measures load across five parts of a student's life, warns them before they overcommit, rearranges an overloaded week, and defends the time they've set aside to rest.

> Ballast — the weight a ship deliberately carries to stay upright. Too little and it tips over, too much and it sinks. The goal is never to carry nothing. It is to know how much you are carrying.

---

## Table of Contents

- [1. Project Overview](#1-project-overview)
  - [1.1 The Problem](#11-the-problem)
  - [Who This Affects](#who-this-affects)
  - [How Big the Problem Is](#how-big-the-problem-is)
  - [1.2 Existing Apps, and Why They Fall Short](#12-existing-apps-and-why-they-fall-short)
- [2. Our Solution](#2-our-solution)
  - [2.1 What Ballast Is](#21-what-ballast-is)
  - [2.2 The Five Parts of Your Life We Measure](#22-the-five-parts-of-your-life-we-measure)
  - [2.3 How the App Works Out Your Number](#23-how-the-app-works-out-your-number)
  - [2.4 How the Number Is Actually Calculated](#24-how-the-number-is-actually-calculated)
  - [A Worked Example — Aina, One Real Week](#a-worked-example--aina-one-real-week)
  - [2.5 What the App Actually Does About It](#25-what-the-app-actually-does-about-it)
  - [2.6 The App Explains Everything It Tells You](#26-the-app-explains-everything-it-tells-you)
  - [2.7 Your Choices, and Your Privacy](#27-your-choices-and-your-privacy)
  - [2.8 Full Feature List](#28-full-feature-list)
- [Sources](#sources)

---

## 1. Project Overview

### 1.1 The Problem

University students don't collapse because of one overwhelming thing. They collapse because six ordinary things arrive at once, none of them alarming on its own, with nothing anywhere showing the total.

We broke that down into six causes, and each one drove a design decision.

1. **Nobody can see the total.** A student's commitments live in four places at once — the university portal, a WhatsApp group, a paper planner, and their own memory. No single place shows the sum, so the only signal they have is a vague feeling of being busy.

2. **Being busy is not one thing.** A student can have a free afternoon and still be finished. Thinking, time, physical energy, social obligation and life admin are five different reserves, and they empty at different speeds. Being told "you have time on Thursday" is useless when the problem is that you have nothing left to think with.

3. **What you can handle changes week to week, but every tool assumes it doesn't.** After three nights of five hours' sleep, the same workload is genuinely heavier. Students feel this as "why is this week so much worse when I'm doing the same amount?" — and no planner accounts for it.

4. **Saying yes takes a second; the cost arrives weeks later.** This is the most important moment in the whole problem, and nothing intervenes at it. By the time an extra commitment starts to hurt, the deadline is close and there is no room left to move anything.

5. **Sorting out your week is itself hard work.** When a student is overloaded, the ability to sit down and calmly re-plan is exactly the thing they have run out of. Tools that need you to be organised before they can help you get organised fail the people who most need them.

6. **Rest has no deadline, so it always loses.** Assignments have due dates. Shifts have start times. Rest has neither, so it is the first thing dropped and the last thing scheduled — every week, until there is nothing left.

Underneath all six is the thing most tools miss completely: **burnout builds up, it doesn't strike.** A student sitting at a steady 70% of their limit for five weeks with no rest is in more danger than one who hits 115% for two days and then recovers. Any app that only reacts to spikes is watching the wrong thing.

### Who This Affects

| Stakeholder | What is at stake for them |
|---|---|
| **University students** — our primary user | Especially those balancing a full course load with part-time work. They carry the cost directly: falling grades, damaged health, and in many cases dropping out. |
| **University counselling services** | They currently meet students only at crisis point. They have no early warning, and no way to see when a whole cohort is under strain. |
| **Lecturers and programme coordinators** | No visibility of workload pressure until submissions start slipping — by which point help is repair work, not prevention. |
| **Employers of student part-timers** | Absorb the result as unreliable availability and staff turnover, without ever seeing the cause. |
| **Family and friends** | Usually the first to notice something is wrong, and the least equipped to name what it is. |

### How Big the Problem Is

| Finding | Figure | Source |
|---|---|---|
| Malaysian university students with moderate-to-severe anxiety | 66.2% | DASS-21 survey, 388 students, Selangor |
| Moderate-to-severe depression | 53.9% | Same study |
| Moderate-to-severe stress | 44.6% | Same study |
| University students worldwide reporting high emotional exhaustion | 56.3% | Review of 44 studies, 26,500 students, 31 countries |
| Students reporting high cynicism | 55.3% | Same review |
| Mental health apps: people who start using them, vs. still using them | 92.4% → 61.8% | Review of 79 clinical trials |

That last row shaped our product as much as any of the others. These apps get installed and then abandoned. The same review found that people stayed longer when an app sent reminders, and stayed longer when the app did **not** use streaks, points or badges — findings we designed around directly.

### 1.2 Existing Apps, and Why They Fall Short

We looked at five kinds of tool a student might already have on their phone.

| App | What it does well | Why it doesn't solve this |
|---|---|---|
| **Motion** | The closest thing to our approach. It automatically places tasks on your calendar based on priority, deadline, how long they take and what depends on what, and reshuffles when things change. | It works out how to fit the work in — not whether the work fits the person. It has no idea how tired you are, how much you have slept, or whether you need a break. It will happily fill every hour you have and report a tidy calendar while doing it. It is also built and priced for working professionals. |
| **Notion / Todoist** | Very good at capturing and organising tasks. | They count how many things, not how heavy they are. Three assignments can be far heavier than twelve errands. A student looking at 14 open tasks learns nothing about whether 14 is survivable. |
| **Google Calendar** | Reliable for fixed commitments like classes and shifts. | It only understands clock time. A free Thursday afternoon means nothing if your brain is finished. Empty is not the same as available. |
| **Daylio / Finch** | Genuinely good at making a daily mood check quick and habitual. | They record how you feel, not why. Knowing you feel awful doesn't tell you which part of your life to change or what to move. Finch also turns self-care into looking after a virtual pet, which quietly becomes one more daily duty — a real risk in an app for people who already have too many. |
| **Forest** | Effective for getting through one focused session. | It solves one hour, not the week. It has no view of the workload that hour sits inside. |
| **Headspace / Calm** | High quality guided meditation and sleep content. | They treat how the stress feels, not what is causing it. Neither touches the workload underneath. |

**The gap.** Every one of these sits on one side of a divide. Planners know what you have to do but nothing about how you are. Wellbeing apps know how you are but nothing about what you have to do. Nothing joins the two — and the join is exactly where burnout happens. On top of that, none of them step in at the moment a student takes on too much, and none of them will ever tell a student to do less.

---

## 2. Our Solution

### 2.1 What Ballast Is

Ballast is a mobile app that shows a student exactly how much they are carrying across five different parts of their life, and then helps them put some of it down. It produces one figure — how full you are this week, as a percentage — and breaks that figure down so you can see which part of your life is actually the problem. Where other apps stop at showing you a number, Ballast rearranges your week to bring that number down, warns you what a new commitment will cost before you agree to it, and defends the time you have set aside to rest. An assistant you can talk to in ordinary language sits across all of it, and every figure the app shows can be opened up to see exactly how it was worked out.

The name is the idea. Ballast is the weight a ship deliberately carries to stay upright — too little and it tips over, too much and it sinks. The goal was never to carry nothing. It is to know how much you are carrying.

### 2.2 The Five Parts of Your Life We Measure

Most apps treat "busy" as a single thing. It isn't. Ballast keeps five separate scores, because a student can be completely fine in four of them and drowning in the fifth.

| Part of your life | What it covers | Something heavy in this area |
|---|---|---|
| **Thinking** | Mental and emotional effort — deep work, exams, difficult conversations, things you are worried about | Writing your final year project report |
| **Time** | Straightforward hours committed | An 18-hour week of classes |
| **Body** | Physical wear — sleep debt, long shifts, commuting, illness, standing all day | A double weekend shift on your feet |
| **People** | Social things you are obliged to attend | A family wedding you cannot skip |
| **Errands** | Life admin — laundry, banking, forms, renewals, groceries | Renewing your road tax before it expires |

**A note on "People."** Social time appears here as something that costs you, but it is also one of the best ways to recover. Ballast tells the two apart with a single question: *is this an obligation?* A group project meeting is a cost. Coffee with a friend you actually like is recovery.

### 2.3 How the App Works Out Your Number

**Step 1 — You tell it what you are carrying.** For each thing, roughly how long it will take, when it is due, and how much it matters. You can type it in as a form, or just tell the assistant in plain words.

**Step 2 — You check in for fifteen seconds a day.** Four taps: how long you slept, your energy, your mood, your stress level. That is the entire daily commitment.

**Step 3 — The app works out how full each of the five areas is.** It compares what you are carrying against what you can carry.

Two things here are different from every other tool we looked at, and they are the reason the number means anything.

- **What you can handle shrinks when you are running on empty.** If you have been sleeping five and a half hours against a target of seven and a half, Ballast treats your thinking capacity as roughly a quarter smaller than normal. Nothing about your workload changed — you are simply working with less. This is why the same week can feel far worse than an identical one a month ago, and it is the thing students find hardest to explain to other people.

  *One exception, on purpose:* time and errands do not shrink. A bad week still has 168 hours in it. Your energy genuinely drops; the clock does not. That difference is why a student can be at 80% on time and 128% on thinking in the very same week.

- **Your worst area counts for more than your average.** If you simply averaged the five scores, a student who is comfortable in four areas and completely overwhelmed in one would come out looking fine. Ballast deliberately gives extra weight to whichever area is worst, so a problem in one part of your life cannot hide behind four healthy ones.

**Step 4 — You get one number and one sentence.** For example: *"You're at 103% this week. Thinking is the problem — it's at 128%."* Tap the number and you can see exactly which commitments produced it.

### 2.4 How the Number Is Actually Calculated

Everything above comes from four short calculations. They run on the phone, offline, in a fraction of a second. Nothing is guessed by a black box — a student can follow every step, and so can a reviewer.

#### Calculation 1 — How much you can handle this week

```
R  =  1  + 0.04 × (your average sleep − your sleep target)
         + 0.05 × (your average energy − 3)
         + 0.03 × (your average mood   − 3)
         − 0.02 × (days since your last real break, counted up to 7)

Your capacity this week  =  your normal capacity × R
```

In plain words: R is a multiplier, kept between 0.6 and 1.15. Sleeping below your target pulls it down, so does low energy, low mood, and a long run without a break. If R comes out at 0.73, you are working with roughly three quarters of your usual capacity.

It applies to **Thinking, Body and People only**. Time and Errands keep their full capacity, because a bad week still has 168 hours in it. Your energy genuinely drops; the clock does not.

#### Calculation 2 — How heavy one commitment is

```
weight  =  hours  ×  how much it draws on that area
                  ×  urgency
                  ×  avoidance

urgency    =  1 + 1 ÷ (days until due)        capped at 2.0
avoidance  =  1.3 if flagged "I keep putting this off", otherwise 1.0
```

In plain words: an eight-hour report that leans heavily on thinking (0.9) and is due in two days (urgency 1.5) is far heavier than eight hours of shifts. Urgency and avoidance apply to the thinking part only — a deadline getting closer does not add hours to a task, it adds pressure. Same with avoidance: a job you keep dodging sits in your head all week even while you never touch it. That is real weight, and no other app counts it.

#### Calculation 3 — The overall figure

```
How full an area is  =  total weight in that area ÷ your capacity for it

Overall  =  0.7 × (weighted average of all five)  +  0.3 × (your worst area)

Area weights:  Thinking 30% · Time 30% · Body 15% · People 15% · Errands 10%
```

In plain words: seventy per cent of the figure is a fair average across your whole life. The other thirty per cent is your single worst area. That second part is what stops one overwhelmed area disappearing behind four healthy ones.

#### Calculation 4 — The direction you are heading

```
Risk  =  0.30 × how much of the last 28 days you spent above 85%
      +  0.25 × rest you are owed
      +  0.20 × how fast your mood is falling
      +  0.15 × sleep you are short
      +  0.10 × rest blocks you booked and then missed
```

In plain words: notice that not one of these asks how bad today was. Every one asks how long. A student sitting at a steady 70% for five weeks with no rest scores higher here than one who hit 115% for two days and then properly recovered — which is the correct answer, and the whole reason this is a separate figure from the one on the home screen.

### A Worked Example — Aina, One Real Week

Final year, 18 hours of class, a 14-hour café job. Every number below is calculated, not assumed.

**Her check-ins that week**

| | Mon | Tue | Wed | Thu | Fri | Sat | Sun | Average |
|---|---|---|---|---|---|---|---|---|
| Sleep | 6.0 | 5.5 | 4.5 | — | 5.0 | 6.5 | 5.5 | 5.5 |
| Energy | 3 | 2 | 2 | — | 2 | 3 | 2 | 2.33 |
| Mood | 3 | 3 | 2 | — | 2 | 3 | 2 | 2.50 |

*Thursday skipped — the app used her rolling average and told her so.*

**Step 1 — Her capacity multiplier**

```
R = 1 + 0.04 × (5.5 − 7.5)  +  0.05 × (2.33 − 3)  +  0.03 × (2.50 − 3)  −  0.02 × 7
  = 1 −  0.080  −  0.034  −  0.015  −  0.140
  = 0.73
```

Her thinking capacity drops from 30 units to 21.9. Her workload did not change. She is simply running on less.

**Step 2 — What she is carrying, in Thinking**

| Commitment | hours | × area | × urgency | × avoidance | = weight |
|---|---|---|---|---|---|
| FYP report, due Wednesday | 8 | 0.9 | 1.50 | 1.3 | 14.04 |
| Data Mining assignment | 3 | 0.9 | 1.25 | 1.0 | 3.38 |
| Reading response | 2 | 0.8 | 1.33 | 1.0 | 2.13 |
| Group project meeting | 2 | 0.5 | 2.00 | 1.0 | 2.00 |
| Café shifts × 2 | 12 | 0.3 | 1.00 | 1.0 | 3.60 |
| Cousin's wedding | 6 | 0.3 | 1.20 | 1.0 | 2.16 |
| Errands × 3 | 3 | 0.2 | 1.10 | 1.0 | 0.66 |
| **Total** | **28.0** | | | | |

One task is half her mental week. The FYP alone is 14 of those 28 units — and 3.2 of them exist purely because she flagged it as something she keeps avoiding.

**Step 3 — All five areas**

| Area | Weight carried | Normal capacity | × R | Capacity now | How full |
|---|---|---|---|---|---|
| Thinking | 28.0 | 30 | 0.73 | 21.9 | 128% |
| Time | 36.0 hrs | 45 | — | 45.0 | 80% |
| Body | 15.2 | 24 | 0.73 | 17.5 | 87% |
| People | 11.8 | 18 | 0.73 | 13.1 | 90% |
| Errands | 4.0 | 10 | — | 10.0 | 40% |

Look at Time: 80%. Aina has a fifth of her week unspoken for. Any calendar app would tell her she is fine. She is at 128% on thinking. That single row is the argument for measuring five things instead of one.

**Step 4 — Her overall figure**

```
weighted average = 0.30(1.28) + 0.30(0.80) + 0.15(0.87) + 0.15(0.90) + 0.10(0.40)
                 = 0.930

Overall = 0.7 × 0.930  +  0.3 × 1.28
        = 0.651 + 0.384
        = 1.03   →   103%, overloaded
```

The average on its own would have said 93% — comfortably inside the amber band, no warning triggered, nothing happens. Adding her worst area pushes it to 103% and the app steps in. That difference is the whole reason the calculation is built this way.

**Step 5 — Where she is heading**

| What it looks at | Her value | Score | Weight | Adds |
|---|---|---|---|---|
| Days above 85% in the last month | 20 of 28 | 0.71 | 0.30 | 0.213 |
| Rest she is owed | 6.3 hours | 0.53 | 0.25 | 0.133 |
| Mood falling | 3.4 → 2.5 over 4 weeks | 0.45 | 0.20 | 0.090 |
| Sleep she is short | −14 hours | 0.67 | 0.15 | 0.101 |
| Rest blocks missed | 2 of 4 | 0.50 | 0.10 | 0.050 |
| **Risk** | | | | **0.59** |

Rising 0.018 per day → (0.75 − 0.59) ÷ 0.018 = **8.9 days**

Reaches high risk on **Thursday 11 September**.

With the two suggested rest blocks, the "rest owed" figure starts falling instead of rising → she never reaches it.

That difference — a date, versus no date — is the entire product in one line. And it is shown with its honesty attached: *9 check-ins in 14 days, medium confidence.* Below five check-ins, the forecast is hidden rather than guessed.

### 2.5 What the App Actually Does About It

Measuring is the easy half. These six things are what make Ballast a tool rather than a report.

**1 · It rearranges your week for you.**
One button. Ballast tries thousands of different arrangements of your week and keeps the best one — moving tasks to lighter days, grouping all your errands into one morning so you are not switching between different kinds of work all day, and pushing back the least important things when there is genuinely too much. It never touches your fixed classes, your work shifts, or time you have set aside to rest.

Every single change comes with one plain sentence explaining it — *"Grouping these saves you three separate context switches"* — and nothing moves until you press apply. The app proposes; you decide.

**2 · It stops you at the moment you say yes.**
This is the feature that goes straight at the heart of the problem. When you add something that would push you over your limit, Ballast interrupts before you commit:

> "This takes you from 104% to 119%. To fit it in, something moves: your FYP draft slips to Friday, or you lose Saturday's rest."
> **Add anyway** · **Add and rearrange my week** · **Not now**

"Add anyway" is always the first option — an app that overrules your judgement gets deleted. "Not now" parks the item in a maybe list rather than deleting it, because the aim is to delay things, not to refuse them.

**3 · It defends your rest.**
Rest blocks are treated as real commitments with time reserved. The rearranging tool will delay an assignment before it will touch your rest. When you do not get the rest you needed, it builds up as a visible figure — *"you owe yourself about 6 hours"* — which shrinks again as you catch up, and is capped so it can never become something else to feel bad about.

**4 · It knows what to do after a long shift.**
If you finish a six-hour shift on two out of five energy, Ballast will not show you your assignment list. It gives you recovery first, then surfaces exactly one task afterwards, then tells you to stop. Work, then recovery, then one piece of work, then rest — and it never quietly queues a second task behind the first.

**5 · It tells you where this is heading.**
Because burnout builds up rather than strikes, Ballast looks at the direction you are travelling in, not just today. It projects the next fourteen days and gives you a date:

> "On the way you're going, you reach high burnout risk around Thursday the 11th. If you take the two rest blocks we've suggested, you don't reach it at all. If you also say yes to the group project sitting in your maybe list, you get there on Monday instead — three days sooner."

Three futures, always shown together. We never show the bad one on its own, because a warning without a way out is just something else to worry about. And when there is not enough information to be honest — fewer than five check-ins in a fortnight — the app hides the forecast rather than guessing.

**6 · You can just talk to it.**
An assistant sits across the whole app. Its most useful job is the least dramatic one: you can type *"two assignments due next week, a double shift Saturday, and I need to renew my road tax"* and it turns that into four properly weighted entries, shown back to you to correct before anything is saved. No forms.

It can also answer questions about yourself:

> **"I'm feeling really exhausted this week compared to last week."**
>
> "You're not imagining it. Your load is 103% this week against 78% last week, and almost all of the jump is in thinking. Three things changed: your FYP moved to Wednesday, you picked up an extra shift, and you've averaged 5.5 hours of sleep against your 7.5 target. Last week you kept both of your rest blocks. This week, neither. Which of those feels most like the problem — the deadline, the shifts, or the sleep?"

**Important:** the assistant does not work anything out on its own. All the calculations and all the decisions are made by the app's own rules, which are fixed, work offline, and can be inspected. The assistant's job is to explain those findings in your own words and to help you get things into the app. Every fact it states is a figure the app has actually calculated, and you can tap any sentence to see where it came from. It never gives medical advice, and it is not the thing deciding how you are doing.

### 2.6 The App Explains Everything It Tells You

Students will not trust a number about their own wellbeing if they cannot see where it came from. So any figure in Ballast can be asked three questions:

| Question | What you get back |
|---|---|
| **Why am I seeing this?** | The exact rule that fired, and the values that triggered it — *"Thinking has been over your limit for 2 days with no rest booked."* |
| **How did you get that number?** | The full working, layer by layer — the total, then the five areas, then the individual commitments, then the arithmetic on a single one. |
| **What if I dropped this?** | The app recalculates without that item and shows you the difference. |

Every conclusion also carries an honest confidence level based on how much you have actually told it — *"medium confidence, you checked in 4 of the last 7 days."* An app that admits what it does not know is more trustworthy than one that reports a precise-looking number from almost no information.

### 2.7 Your Choices, and Your Privacy

We made three decisions here deliberately, and each one is offered as a choice rather than imposed.

**Streaks are optional, and you are asked at setup.** Rather than burying it in settings, Ballast asks directly: *"Do streaks help you, or stress you?"* Neither answer is presented as the right one. If you keep it, the streak counts your check-in, never what you got done — so a day where you log "wrecked, slept four hours" still counts. You get two rest days a month applied automatically, and breaking it shows "welcome back", never a penalty. If the app notices your streak is costing you sleep, it offers to switch it off.

**Your diary has three levels, and you pick.**

| Level | What the assistant can see | Why you might choose it |
|---|---|---|
| **Off** | Nothing | You want the app, not the conversation |
| **Numbers only** (default) | Your load, your commitments, your check-in scores | Enough for almost every useful answer, and your writing never leaves your phone |
| **Numbers and diary** | Also what you have written | It can notice things numbers cannot — that the same person keeps coming up in your entries, or that you write differently when you are struggling |

We explain plainly at the moment of choosing that the top level sends what you have written off your phone to be read. That belongs in front of you when you decide, not in a settings note afterwards.

**Nothing happens to your week without you.** The rearranging tool proposes and you accept. The intercept offers and you choose. The assistant notices and you confirm. The same principle runs through all three, and it is deliberate.

And it is not a medical app. Ballast measures workload and what you tell it about yourself. It does not diagnose anything. If risk stays high for a long time, it quietly surfaces the university counselling service and a helpline — always for you to choose, never reported to anyone.

### 2.8 Full Feature List

**Understanding your load**

| Feature | What it does for you |
|---|---|
| Five separate scores | Shows which part of your life is the problem, not just that you are busy |
| One overall figure | A single percentage you can check in two seconds |
| Capacity that shrinks when you are depleted | The same workload correctly reads as heavier in a bad week |
| Extra weight on your worst area | One overwhelmed area cannot hide behind four healthy ones |
| Direction of travel | Tracks how long you have been under pressure, separately from today |
| Rest you are owed | A visible figure for the recovery you have missed |

**Your day**

| Feature | What it does for you |
|---|---|
| Fifteen-second daily check-in | Sleep, energy, mood, stress — four taps |
| Optional streak, your choice at setup | Counts checking in, never what you got done |
| One morning notification | Carries your actual load, not a generic reminder |
| Mood over time | See how your weeks compare |
| Private diary | Never read by the app unless you turn that on |

**Planning**

| Feature | What it does for you |
|---|---|
| Morning / afternoon / evening blocks | Plan without scheduling to the minute |
| High, medium, low priority | So the app knows what can slip |
| Quick add with small / medium / large sizing | Add something in five seconds |
| Automatic sorting into the five areas | You correct it when it is wrong; it learns |
| "I keep putting this off" flag | Counts the mental weight of a job you are avoiding |
| Errand list | Grouped and scheduled for when they are actually needed |

**Doing something about it**

| Feature | What it does for you |
|---|---|
| Rearrange my week | Moves, groups and delays things to bring an overloaded week down |
| A reason for every change | One plain sentence, every time |
| After-shift ordering | Recovery first, then exactly one task, then rest |
| Stop before you say yes | Shows what a new commitment will cost before you agree |

**Recovery**

| Feature | What it does for you |
|---|---|
| Protected rest blocks | Time the app will not schedule over |
| Suggestions with a button | "Block 8–10pm tonight", not "remember to relax" |
| Focus timer with optional background sound | For a single work session |
| Guided breathing | Two minutes, nothing recorded |
| Water, sleep and movement reminders | Including hot weather warnings |
| A hard limit on notifications | Two a day, five a week, quiet hours — an app that nags an exhausted person is part of the problem |

**Understanding and looking ahead**

| Feature | What it does for you |
|---|---|
| Why / How / What if | Every number can be opened up and questioned |
| Honest confidence levels | The app tells you when it is unsure |
| Fourteen-day forecast | A date, and the version where you rest instead |
| Weekly review, 90 seconds on Sunday | Tunes the app to you |
| Patterns from your own history | "Your mood drops about two days after any week above 90%" |

**Talking to it**

| Feature | What it does for you |
|---|---|
| Add things by typing normally | No forms |
| Ask about yourself | Answers built only from figures the app calculated |
| Three privacy levels | You decide what it can see |
| A safe route when things are bad | Surfaces real support, never diagnoses, never reports you |

---

## Sources

- PLOS ONE — Malaysian university students (DASS-21 survey)
- Scientific Reports — student burnout review
- AJMC — mental health app engagement review
- Competitor behaviour checked against Motion's own documentation




![Login/Sign up UserFLow](userFlow/ballast_auth_onboarding_flow.png)
