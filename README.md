# Ballast by Suchaiirmon

**Team:** [Member 1], [Member 2], [Member 3], [Member 4]
**Problem Statement:** Stress & Workload Manager &nbsp;
**Video Presentation:** [Unlisted YouTube Link](#) &nbsp;
**Presentation Slides:** [Public Link](#)

---

# 1. Project Overview

### 1.1 The Problem

University students don't collapse because of one overwhelming thing. They collapse because six ordinary things arrive at once, none of them alarming on its own, with nothing anywhere showing the total.

&nbsp;

We broke that down into six causes, and each one drove a design decision.

&nbsp;

**1\. Nobody can see the total.** A student's commitments live in four places at once the university portal, a WhatsApp group, a paper planner, and their own memory. No single place shows the sum, so the only signal they have is a vague feeling of being busy.

&nbsp;

**2\. Being busy is not one thing.** A student can have a free afternoon and still be finished. Thinking, time, physical energy, social obligation and life admin are five different reserves, and they empty at different speeds. Being told "you have time on Thursday" is useless when the problem is that you have nothing left to think with.

&nbsp;

**3\. What you can handle changes week to week, but every tool assumes it doesn't.** After three nights of five hours' sleep, the same workload is genuinely heavier. Students feel this as "why is this week so much worse when I'm doing the same amount?" and no planner accounts for it.

&nbsp;

**4\. Saying yes takes a second; the cost arrives weeks later.** This is the most important moment in the whole problem, and nothing intervenes at it. By the time an extra commitment starts to hurt, the deadline is close and there is no room left to move anything.

&nbsp;

**5\. Sorting out your week is itself hard work.** When a student is overloaded, the ability to sit down and calmly re-plan is exactly the thing they have run out of. Tools that need you to be organised before they can help you get organised fail the people who most need them.

&nbsp;

**6\. Rest has no deadline, so it always loses.** Assignments have due dates. Shifts have start times. Rest has neither, so it is the first thing dropped and the last thing scheduled every week, until there is nothing left.

&nbsp;

Underneath all six is the thing most tools miss completely: **burnout builds up, it doesn't strike.** A student sitting at a steady 70% of their limit for five weeks with no rest is in more danger than one who hits 115% for two days and then recovers. Any app that only reacts to spikes is watching the wrong thing.

#### Who this affects

| Stakeholder                              | What is at stake for them                                                                                                                                        |
| :--------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **University students** our primary user | Especially those balancing a full course load with part-time work. They carry the cost directly: falling grades, damaged health, and in many cases dropping out. |
| **University counselling services**      | They currently meet students only at crisis point. They have no early warning, and no way to see when a whole cohort is under strain.                            |
| **Lecturers and programme coordinators** | No visibility of workload pressure until submissions start slipping by which point help is repair work, not prevention.                                          |
| **Employers of student part-timers**     | Absorb the result as unreliable availability and staff turnover, without ever seeing the cause.                                                                  |
| **Family and friends**                   | Usually the first to notice something is wrong, and the least equipped to name what it is.                                                                       |

#### How big the problem is

| Finding                                                                         | Figure            | Source                                              |
| :------------------------------------------------------------------------------ | :---------------- | :-------------------------------------------------- |
| Malaysian university students with moderate-to-severe **anxiety**               | **66.2%**         | DASS-21 survey, 388 students, Selangor              |
| Moderate-to-severe **depression**                                               | **53.9%**         | Same study                                          |
| Moderate-to-severe **stress**                                                   | **44.6%**         | Same study                                          |
| University students worldwide reporting high **emotional exhaustion**           | **56.3%**         | Review of 44 studies, 26,500 students, 31 countries |
| Students reporting high **cynicism**                                            | **55.3%**         | Same review                                         |
| Mental health apps: people who start using them, versus people still using them | **92.4% → 61.8%** | Review of 79 clinical trials                        |

&nbsp;

That last row shaped our product as much as any of the others. These apps get installed and then abandoned. The same review found that people stayed longer when an app sent reminders, and stayed longer when the app did **not** use streaks, points or badges findings we designed around directly.

### 1.2 Existing apps, and why they fall short

We looked at five kinds of tool a student might already have on their phone.

&nbsp;

| App                  | What it does well                                                                                                                                                                              | Why it doesn't solve this                                                                                                                                                                                                                                                                                        |
| :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Motion**           | The closest thing to our approach. It automatically places tasks on your calendar based on priority, deadline, how long they take and what depends on what, and reshuffles when things change. | It works out how to **fit the work in** not whether the work fits the person. It has no idea how tired you are, how much you have slept, or whether you need a break. It will happily fill every hour you have and report a tidy calendar while doing it. It is also built and priced for working professionals. |
| **Notion / Todoist** | Very good at capturing and organising tasks.                                                                                                                                                   | They count **how many things**, not **how heavy they are**. Three assignments can be far heavier than twelve errands. A student looking at 14 open tasks learns nothing about whether 14 is survivable.                                                                                                          |
| **Google Calendar**  | Reliable for fixed commitments like classes and shifts.                                                                                                                                        | It only understands **clock time**. A free Thursday afternoon means nothing if your brain is finished. Empty is not the same as available.                                                                                                                                                                       |
| **Daylio / Finch**   | Genuinely good at making a daily mood check quick and habitual.                                                                                                                                | They record **how you feel**, not **why**. Knowing you feel awful doesn't tell you which part of your life to change or what to move. Finch also turns self-care into looking after a virtual pet, which quietly becomes one more daily duty a real risk in an app for people who already have too many.         |
| **Forest**           | Effective for getting through one focused session.                                                                                                                                             | It solves **one hour, not the week**. It has no view of the workload that hour sits inside.                                                                                                                                                                                                                      |
| **Headspace / Calm** | High quality guided meditation and sleep content.                                                                                                                                              | They treat **how the stress feels**, not what is causing it. Neither touches the workload underneath.                                                                                                                                                                                                            |

&nbsp;

**The gap.** Every one of these sits on one side of a divide. Planners know what you have to do but nothing about how you are. Wellbeing apps know how you are but nothing about what you have to do. Nothing joins the two and the join is exactly where burnout happens. On top of that, none of them step in at the moment a student takes on too much, and none of them will ever tell a student to **do less**.

&nbsp;

---

## 1.3\. Our Solution

### 1.3.1 What Ballast is

**Ballast** is a mobile app that shows a student exactly how much they are carrying across five different parts of their life, and then helps them put some of it down. It produces one figure how full you are this week, as a percentage and breaks that figure down so you can see which part of your life is actually the problem. Where other apps stop at showing you a number, Ballast rearranges your week to bring that number down, warns you what a new commitment will cost **before** you agree to it, and defends the time you have set aside to rest. An assistant you can talk to in ordinary language sits across all of it, and every figure the app shows can be opened up to see exactly how it was worked out.

&nbsp;

The name is the idea. Ballast is the weight a ship deliberately carries to stay upright too little and it tips over, too much and it sinks. The goal was never to carry nothing. It is to know how much you are carrying.

### 1.3.2 The five parts of your life we measure

Most apps treat "busy" as a single thing. It isn't. Ballast keeps five separate scores, because a student can be completely fine in four of them and drowning in the fifth.

&nbsp;

| Part of your life | What it covers                                                                                      | Something heavy in this area             |
| :---------------- | :-------------------------------------------------------------------------------------------------- | :--------------------------------------- |
| **Thinking**      | Mental and emotional effort deep work, exams, difficult conversations, things you are worried about | Writing your final year project report   |
| **Time**          | Straightforward hours committed                                                                     | An 18-hour week of classes               |
| **Body**          | Physical wear sleep debt, long shifts, commuting, illness, standing all day                         | A double weekend shift on your feet      |
| **People**        | Social things you are obliged to attend                                                             | A family wedding you cannot skip         |
| **Errands**       | Life admin laundry, banking, forms, renewals, groceries                                             | Renewing your road tax before it expires |

&nbsp;

> **A note on "People".** Social time appears here as something that costs you, but it is also one of the best ways to recover. Ballast tells the two apart with a single question: is this an obligation? A group project meeting is a cost. Coffee with a friend you actually like is recovery.

### 1.3.3 How the app works out your number

**Step 1 : You tell it what you are carrying.** For each thing, roughly how long it will take, when it is due, and how much it matters. You can type it in as a form, or just tell the assistant in plain words.

&nbsp;

**Step 2 : You check in for fifteen seconds a day.** Four taps: how long you slept, your energy, your mood, your stress level. That is the entire daily commitment.

&nbsp;

**Step 3 : The app works out how full each of the five areas is.** It compares what you are carrying against what you can carry.

&nbsp;

Two things here are different from every other tool we looked at, and they are the reason the number means anything.

&nbsp;

**What you can handle shrinks when you are running on empty.** If you have been sleeping five and a half hours against a target of seven and a half, Ballast treats your thinking capacity as roughly a quarter smaller than normal. Nothing about your workload changed you are simply working with less. This is why the same week can feel far worse than an identical one a month ago, and it is the thing students find hardest to explain to other people.

&nbsp;

_One exception, on purpose:_ time and errands do **not** shrink. A bad week still has 168 hours in it. Your energy genuinely drops; the clock does not. That difference is why a student can be at 80% on time and 128% on thinking in the very same week.

&nbsp;

**Your worst area counts for more than your average.** If you simply averaged the five scores, a student who is comfortable in four areas and completely overwhelmed in one would come out looking fine. Ballast deliberately gives extra weight to whichever area is worst, so a problem in one part of your life cannot hide behind four healthy ones.

&nbsp;

**Step 4 : You get one number and one sentence.** For example: _"You're at 103% this week. Thinking is the problem it's at 128%."_ Tap the number and you can see exactly which commitments produced it.

### 1.3.4 How the number is actually calculated

Everything above comes from four short calculations. They run on the phone, offline, in a fraction of a second. Nothing is guessed by a black box a student can follow every step, and so can a reviewer.

#### Calculation 1 : how much you can handle this week

R \= 1 \+ 0.04 × (your average sleep − your sleep target)

&nbsp;

         + 0.05 × (your average energy − 3)

&nbsp;

         + 0.03 × (your average mood   − 3)

&nbsp;

         − 0.02 × (days since your last real break, counted up to 7)

&nbsp;

Your capacity this week \= your normal capacity × R

&nbsp;

**In plain words.** `R` is a multiplier, kept between 0.6 and 1.15. Sleeping below your target pulls it down, so does low energy, low mood, and a long run without a break. If `R` comes out at 0.73, you are working with roughly three quarters of your usual capacity.

&nbsp;

It applies to **Thinking, Body and People only**. Time and Errands keep their full capacity, because a bad week still has 168 hours in it. Your energy genuinely drops; the clock does not.

#### Calculation 2 : how heavy one commitment is

weight \= hours × how much it draws on that area

&nbsp;

                  ×  urgency

&nbsp;

                  ×  avoidance

&nbsp;

urgency \= 1 \+ 1 ÷ (days until due) capped at 2.0

&nbsp;

avoidance \= 1.3 if flagged "I keep putting this off", otherwise 1.0

&nbsp;

**In plain words.** An eight-hour report that leans heavily on thinking (0.9) and is due in two days (urgency 1.5) is far heavier than eight hours of shifts. Urgency and avoidance apply to the **thinking** part only a deadline getting closer does not add hours to a task, it adds pressure. Same with avoidance: a job you keep dodging sits in your head all week even while you never touch it. That is real weight, and no other app counts it.

#### Calculation 3 : the overall figure

How full an area is \= total weight in that area ÷ your capacity for it

&nbsp;

Overall \= 0.7 × (weighted average of all five) \+ 0.3 × (your worst area)

&nbsp;

Area weights: Thinking 30% · Time 30% · Body 15% · People 15% · Errands 10%

&nbsp;

**In plain words.** Seventy per cent of the figure is a fair average across your whole life. The other thirty per cent is your single worst area. That second part is what stops one overwhelmed area disappearing behind four healthy ones.

#### Calculation 4 : the direction you are heading

Risk \= 0.30 × how much of the last 28 days you spent above 85%

&nbsp;

      +  0.25 × rest you are owed

&nbsp;

      +  0.20 × how fast your mood is falling

&nbsp;

      +  0.15 × sleep you are short

&nbsp;

      +  0.10 × rest blocks you booked and then missed

&nbsp;

**In plain words.** Notice that not one of these asks how bad today was. Every one asks **how long**. A student sitting at a steady 70% for five weeks with no rest scores higher here than one who hit 115% for two days and then properly recovered which is the correct answer, and the whole reason this is a separate figure from the one on the home screen.

#### A worked example : Aina, one real week

Final year, 18 hours of class, a 14-hour café job. Every number below is calculated, not assumed.

&nbsp;

**Her check-ins that week**

&nbsp;

|        | Mon | Tue | Wed | Thu | Fri | Sat | Sun | Average  |
| :----- | :-- | :-- | :-- | :-- | :-- | :-- | :-- | :------- |
| Sleep  | 6.0 | 5.5 | 4.5 | —   | 5.0 | 6.5 | 5.5 | **5.5**  |
| Energy | 3   | 2   | 2   | —   | 2   | 3   | 2   | **2.33** |
| Mood   | 3   | 3   | 2   | —   | 2   | 3   | 2   | **2.50** |

&nbsp;

_Thursday skipped the app used her rolling average and told her so._

&nbsp;

**Step 1 : her capacity multiplier**

&nbsp;

R \= 1 \+ 0.04 × (5.5 − 7.5) \+ 0.05 × (2.33 − 3\) \+ 0.03 × (2.50 − 3\) − 0.02 × 7

&nbsp;

\= 1 − 0.080 − 0.034 − 0.015 − 0.140

&nbsp;

\= 0.73

&nbsp;

Her thinking capacity drops from 30 units to **21.9**. Her workload did not change. She is simply running on less.

&nbsp;

**Step 2 : what she is carrying, in Thinking**

&nbsp;

| Commitment                | hours | × area | × urgency | × avoidance | \= weight |
| :------------------------ | :---- | :----- | :-------- | :---------- | :-------- |
| FYP report, due Wednesday | 8     | 0.9    | 1.50      | **1.3**     | **14.04** |
| Data Mining assignment    | 3     | 0.9    | 1.25      | 1.0         | 3.38      |
| Reading response          | 2     | 0.8    | 1.33      | 1.0         | 2.13      |
| Group project meeting     | 2     | 0.5    | 2.00      | 1.0         | 2.00      |
| Café shifts × 2           | 12    | 0.3    | 1.00      | 1.0         | 3.60      |
| Cousin's wedding          | 6     | 0.3    | 1.20      | 1.0         | 2.16      |
| Errands × 3               | 3     | 0.2    | 1.10      | 1.0         | 0.66      |
|                           |       |        |           | **Total**   | **28.0**  |

&nbsp;

One task is half her mental week. **The FYP alone is 14 of those 28 units and 3.2 of them exist purely because she flagged it as something she keeps avoiding.**

&nbsp;

**Step 3 : all five areas**

&nbsp;

| Area     | Weight carried | Normal capacity | × R  | Capacity now | How full |
| :------- | :------------- | :-------------- | :--- | :----------- | :------- |
| Thinking | 28.0           | 30              | 0.73 | 21.9         | **128%** |
| Time     | 36.0 hrs       | 45              | —    | 45.0         | **80%**  |
| Body     | 15.2           | 24              | 0.73 | 17.5         | **87%**  |
| People   | 11.8           | 18              | 0.73 | 13.1         | **90%**  |
| Errands  | 4.0            | 10              | —    | 10.0         | **40%**  |

&nbsp;

**Look at Time: 80%.** Aina has a fifth of her week unspoken for. Any calendar app would tell her she is fine. She is at 128% on thinking. That single row is the argument for measuring five things instead of one.

&nbsp;

**Step 4 : her overall figure**

&nbsp;

weighted average \= 0.30(1.28) \+ 0.30(0.80) \+ 0.15(0.87) \+ 0.15(0.90) \+ 0.10(0.40)

&nbsp;

                 = 0.930

&nbsp;

Overall = 0.7 × 0.930 \+ 0.3 × 1.28

&nbsp;

        = 0.651 \+ 0.384

&nbsp;

        = 1.03   →   103%, overloaded

&nbsp;

**The average on its own would have said 93%** comfortably inside the amber band, no warning triggered, nothing happens. Adding her worst area pushes it to 103% and the app steps in. That difference is the whole reason the calculation is built this way.

&nbsp;

**Step 5 : where she is heading**

&nbsp;

| What it looks at                 | Her value              | Score | Weight   | Adds     |
| :------------------------------- | :--------------------- | :---- | :------- | :------- |
| Days above 85% in the last month | 20 of 28               | 0.71  | 0.30     | 0.213    |
| Rest she is owed                 | 6.3 hours              | 0.53  | 0.25     | 0.133    |
| Mood falling                     | 3.4 → 2.5 over 4 weeks | 0.45  | 0.20     | 0.090    |
| Sleep she is short               | −14 hours              | 0.67  | 0.15     | 0.101    |
| Rest blocks missed               | 2 of 4                 | 0.50  | 0.10     | 0.050    |
|                                  |                        |       | **Risk** | **0.59** |

&nbsp;

Rising 0.018 per day → (0.75 − 0.59) ÷ 0.018 \= 8.9 days

&nbsp;

Reaches high risk on Thursday 11 September.

&nbsp;

With the two suggested rest blocks, the "rest owed" figure starts falling instead

&nbsp;

of rising → she never reaches it.

&nbsp;

That difference a date, versus no date is the entire product in one line. And it is shown with its honesty attached: **9 check-ins in 14 days, medium confidence.** Below five check-ins, the forecast is hidden rather than guessed.

### 1.3.5 What the app actually does about it

Measuring is the easy half. These six things are what make Ballast a tool rather than a report.

&nbsp;

**1 · It rearranges your week for you.** One button. Ballast tries thousands of different arrangements of your week and keeps the best one moving tasks to lighter days, grouping all your errands into one morning so you are not switching between different kinds of work all day, and pushing back the least important things when there is genuinely too much. It never touches your fixed classes, your work shifts, or time you have set aside to rest.

&nbsp;

Every single change comes with one plain sentence explaining it _"Grouping these saves you three separate context switches"_ and nothing moves until you press apply. The app proposes; you decide.

&nbsp;

**2 · It stops you at the moment you say yes.** This is the feature that goes straight at the heart of the problem. When you add something that would push you over your limit, Ballast interrupts before you commit:

&nbsp;

> _"This takes you from 104% to 119%. To fit it in, something moves: your FYP draft slips to Friday, or you lose Saturday's rest."_ **Add anyway** · **Add and rearrange my week** · **Not now**

&nbsp;

"Add anyway" is always the first option an app that overrules your judgement gets deleted. "Not now" parks the item in a maybe list rather than deleting it, because the aim is to delay things, not to refuse them.

&nbsp;

**3 · It defends your rest.** Rest blocks are treated as real commitments with time reserved. The rearranging tool will delay an assignment before it will touch your rest. When you do not get the rest you needed, it builds up as a visible figure _"you owe yourself about 6 hours"_ which shrinks again as you catch up, and is capped so it can never become something else to feel bad about.

&nbsp;

**4 · It knows what to do after a long shift.** If you finish a six-hour shift on two out of five energy, Ballast will not show you your assignment list. It gives you recovery first, then surfaces exactly one task afterwards, then tells you to stop. Work, then recovery, then one piece of work, then rest and it never quietly queues a second task behind the first.

&nbsp;

**5 · It tells you where this is heading.** Because burnout builds up rather than strikes, Ballast looks at the direction you are travelling in, not just today. It projects the next fourteen days and gives you a date:

&nbsp;

> _"On the way you're going, you reach high burnout risk around Thursday the 11th. If you take the two rest blocks we've suggested, you don't reach it at all. If you also say yes to the group project sitting in your maybe list, you get there on Monday instead three days sooner."_

&nbsp;

Three futures, always shown together. We never show the bad one on its own, because a warning without a way out is just something else to worry about. And when there is not enough information to be honest fewer than five check-ins in a fortnight the app hides the forecast rather than guessing.

&nbsp;

**6 · You can just talk to it.** An assistant sits across the whole app. Its most useful job is the least dramatic one: you can type _"two assignments due next week, a double shift Saturday, and I need to renew my road tax"_ and it turns that into four properly weighted entries, shown back to you to correct before anything is saved. No forms.

&nbsp;

It can also answer questions about yourself:

&nbsp;

> **"I'm feeling really exhausted this week compared to last week."**

&nbsp;

> _"You're not imagining it. Your load is 103% this week against 78% last week, and almost all of the jump is in thinking. Three things changed: your FYP moved to Wednesday, you picked up an extra shift, and you've averaged 5.5 hours of sleep against your 7.5 target. Last week you kept both of your rest blocks. This week, neither. Which of those feels most like the problem the deadline, the shifts, or the sleep?"_

&nbsp;

**Important:** the assistant does not work anything out on its own. All the calculations and all the decisions are made by the app's own rules, which are fixed, work offline, and can be inspected. The assistant's job is to explain those findings in your own words and to help you get things into the app. Every fact it states is a figure the app has actually calculated, and you can tap any sentence to see where it came from. It never gives medical advice, and it is not the thing deciding how you are doing.

### 1.3.6 The app explains everything it tells you

Students will not trust a number about their own wellbeing if they cannot see where it came from. So any figure in Ballast can be asked three questions:

&nbsp;

| Question                         | What you get back                                                                                                                      |
| :------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| **Why am I seeing this?**        | The exact rule that fired, and the values that triggered it _"Thinking has been over your limit for 2 days with no rest booked."_      |
| **How did you get that number?** | The full working, layer by layer the total, then the five areas, then the individual commitments, then the arithmetic on a single one. |
| **What if I dropped this?**      | The app recalculates without that item and shows you the difference.                                                                   |

&nbsp;

Every conclusion also carries an honest confidence level based on how much you have actually told it _"medium confidence, you checked in 4 of the last 7 days."_ An app that admits what it does not know is more trustworthy than one that reports a precise-looking number from almost no information.

### 1.3.7 Your choices, and your privacy

We made three decisions here deliberately, and each one is offered as a choice rather than imposed.

&nbsp;

**Streaks are optional, and you are asked at setup.** Rather than burying it in settings, Ballast asks directly: _"Do streaks help you, or stress you?"_ Neither answer is presented as the right one. If you keep it, the streak counts your **check-in**, never what you got done so a day where you log "wrecked, slept four hours" still counts. You get two rest days a month applied automatically, and breaking it shows _"welcome back"_, never a penalty. If the app notices your streak is costing you sleep, it offers to switch it off.

&nbsp;

**Your diary has three levels, and you pick.**

&nbsp;

| Level                        | What the assistant can see                        | Why you might choose it                                                                                                                         |
| :--------------------------- | :------------------------------------------------ | :---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Off**                      | Nothing                                           | You want the app, not the conversation                                                                                                          |
| **Numbers only** _(default)_ | Your load, your commitments, your check-in scores | Enough for almost every useful answer, and your writing never leaves your phone                                                                 |
| **Numbers and diary**        | Also what you have written                        | It can notice things numbers cannot that the same person keeps coming up in your entries, or that you write differently when you are struggling |

&nbsp;

We explain plainly at the moment of choosing that the top level sends what you have written off your phone to be read. That belongs in front of you when you decide, not in a settings note afterwards.

&nbsp;

**Nothing happens to your week without you.** The rearranging tool proposes and you accept. The intercept offers and you choose. The assistant notices and you confirm. The same principle runs through all three, and it is deliberate.

&nbsp;

**And it is not a medical app.** Ballast measures workload and what you tell it about yourself. It does not diagnose anything. If risk stays high for a long time, it quietly surfaces the university counselling service and a helpline always for you to choose, never reported to anyone.

---

# 2. Ideation & Process

## 2.1 Ideas We Considered

| Idea                                               | Why it was dropped / kept                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| :------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Find User Capacity (Chosen)                        | This is the foundation of Ballast. Instead of focusing only on completing tasks, the team wanted the system to first understand how much workload a student can realistically handle as each student has their own limitations and strengths.&nbsp;                                                                                                                                                                                                                                                                                 |
| Streaks (Chosen)                                   | Streaks were considered as an optional motivation mechanism to encourage regular check-ins. The feature is kept optional because constant streak pressure could become counterproductive for students already experiencing stress.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Notification (Chosen)                              | Notifications provide timely reminders for check-ins and important capacity-related actions.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Rate Daily Sleep, Energy, Mood, Stress (Chosen)    | These inputs help Ballast understand the student's daily condition rather than relying only on scheduled tasks. They provide additional context for changes in capacity and risk.&nbsp;                                                                                                                                                                                                                                                                                                                                                |
| Current Week Capacity (Chosen)                     | Shows the student how demanding their current week is across Mental, Time and Energy capacity. Energy capacity includes academic tasks, errands and social events which allow students to see not only how much time they have available but also how much overall workload they have in one setting. This helps student identify potential overload before the week becomes unmanageable.&nbsp;                                                                                                                                               |
| To do List (Chosen)                                | Gives students a central place to view and manage their academic and personal commitments. It helps students see what they need to complete within their overall weekly workload.&nbsp;                                                                                                                                                                                                                                                                                                                                                   |
| Add Task (Chosen)                                  | Allows students to add a new commitment while providing important information for Ballast's capacity assessment. Students specify how much time the task will take, how important it is (Low / Medium / High) and when it is due. This information helps Ballast understand the task's contribution to the student's workload and determine whether adding it may increase capacity pressure.&nbsp;                                                                                                                                          |
| Add Task \- Warning Capacity Overload (Chosen)     | The team wanted the system to respond when a new commitment pushes the student's capacity too high. This evolved into an important decision-support interaction rather than merely displaying a warning.&nbsp;                                                                                                                                                                                                                                                                                                                         |
| Rebalance Proposal (Chosen)                        | This became one of Ballast's main differentiating features. Instead of simply telling students that they are overloaded, Ballast proposes changes for the plan of the week so the week becomes more manageable.&nbsp;                                                                                                                                                                                                                                                                                                                  |
| Recovery Plan (Chosen)                             | Recovery was included because the concept should not only help students manage workload but also recognise the need to recover after demanding periods.&nbsp;                                                                                                                                                                                                                                                                                                                                                                       |
| Focus Timer (Chosen)                               | The focus timer supports execution after planning. It helps students work on the selected commitment while maintaining a structured focus-and-break cycle.&nbsp;                                                                                                                                                                                                                                                                                                                                                                       |
| Breathing Technique (Chosen)                       | A simple breathing activity provides an immediate low-effort recovery option when students need a short break from demanding tasks.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                              |
| Burnout Forecast (Chosen)                          |The forecast gives students a forward-looking view of potential overload rather than only showing their current state. It is positioned as a risk indicator, not a medical diagnosis.&nbsp;                                                                                                                                                                                                                                                                                                                                            |
| Trend & Risk (Chosen)                              | Tracking changes over time allows students to recognise recurring patterns in their capacity and workload instead of treating every difficult day as an isolated event.&nbsp;                                                                                                                                                                                                                                                                                                                                                          |
| Why/How/What If (Chosen)                           | This was developed to make Ballast's capacity information understandable. Why explains why capacity is high, How shows which factors and commitments contributed to it, and What If explores the possible consequences of continuing at the current load.&nbsp;                                                                                                                                                                                                                                                                     |
| Last Week Review (Chosen)                          | Reviewing the previous week allows students to reflect on workload and capacity patterns and use those observations to make better decisions for the following week.&nbsp;                                                                                                                                                                                                                                                                                                                                                             |
| Diary (Chosen)                                     | The Diary provides students with a private space to record their feelings, thoughts and daily experiences. An optional AI analysis feature can identify patterns or provide insights from diary entries while allowing students to choose whether they want their entries to be analysed.&nbsp;                                                                                                                                                                                                                                          |
| Chat With AI (Chosen)                              | Provides students with a conversational space for emotional support and casual interaction, allowing them to talk about their current concerns and feelings in a more natural, friend-like way. It also helps students stay up to date with current issues, news and trends related to their course or field such as Marketing, Business, or IT. This gives students both emotional support and relevant awareness of what is happening in their area of study.&nbsp;&nbsp;                                                            |
| Settings (Chosen)                                  | Settings allow students to control personalisation, notifications, motivation features and data preferences, supporting a lower-pressure experience.&nbsp;                                                                                                                                                                                                                                                                                                                                                                             |
| Calendar with Google Calendar Integration (Chosen) | Google Calendar integration allows students to synchronise their existing schedules with Ballast, reducing the need to manually enter the same events or commitments into both Ballast and their personal calendar.&nbsp;                                                                                                                                                                                                                                                                                                              |
| Voice Assistant (Chosen)                           |A hands-free Voice Assistant allows students to create tasks and deadlines using voice commands, reducing the effort required for manual task entry and making it more convenient to record commitments immediately.&nbsp;                                                                                                                                                                                                                                                                                                             |
| Visual Burnout Level Representation (Chosen)       | A ship ballast was introduced as a visual representation of the student's burnout level and capacity. The ship ballast sinks deeper as the student's condition approaches burnout, allowing students to understand their current capacity quickly through a simple visual representation rather than relying only on graphs and numerical values.&nbsp;                                                                                                                                                                                             |
| Face Recognition for Mood Detecting&nbsp;          | The team explored automatically detecting mood through facial expressions but it introduced unnecessary privacy, accuracy and technical concerns.&nbsp;                                                                                                                                                                                                                                                                                                    |
| Social To Do List&nbsp;                            | The idea of separating social commitments into a dedicated task list was explored but it could make it inconvenient for students to keep track of different types of responsibilities across multiple sections. Social commitments were instead incorporated into the broader Task feature alongside academic tasks and errands, allowing students to view all their upcoming responsibilities and commitments in one centralized location.&nbsp;                                                                                         |
| Errands To Do List                                 | The idea of separating errands into a dedicated task list was explored but it could make it inconvenient for students to keep track of different types of responsibilities across multiple sections. Errands were instead incorporated into the broader Task feature alongside academic and social tasks, allowing students to view all their upcoming responsibilities in one centralized location.&nbsp;                                                                                                                                |
| Physical Well Being                                | A dedicated physical well-being feature was initially considered but it was dropped to avoid unnecessarily separating sleep from the student's overall well-being. Sleep was instead considered as part of mental well-being as sleep quality can have a significant impact on a student's mental and emotional well-being.&nbsp;                                                                                                                                                                                                         |
| Task Reward                                        | The idea of rewarding students with points after completing tasks and allowing them to redeem rewards such as Tealive vouchers was initially considered. However, implementing real-world vouchers would require integration with third-party services and involve additional legal, regulatory and operational considerations, making it unrealistic for the current scope of the system. This feature is therefore considered a potential scalability feature for future development.&nbsp;&nbsp;                                    |
| New/Article&nbsp;                                  |A dedicated section for course-related news and articles was initially considered to help students stay updated with current trends and developments in their field of study. However, this was removed as a separate feature because similar information can instead be provided through the Chat with AI feature, allowing students to ask for relevant updates within the conversation. This approach also reduces potential copyright concerns associated with directly displaying or reproducing external news articles.&nbsp;&nbsp; |
| Home Screen Widget                                 |A widget could give students quick access to their Ballast information directly from their phone's home screen. However, it was not essential to the core capacity-management experience and would require additional platform-specific development. It was therefore left out of the current prototype to keep the project scope realistic.&nbsp;                                                                                                                                                                                     |
| Focus Lock                                         | This feature was intended to encourage students to reconsider interrupting a Pomodoro focus session before opening a blocked app. However, implementing app blocking and controlling access to other applications would require deeper operating-system-level functionality. Since Ballast's main focus is capacity management rather than strict app restriction, this feature was excluded from the current scope.&nbsp;                                                                                                             |

## 2.2 Ideation Boards

### Mindmap

![Mindmap](mindmap.png)

The mindmap shows the different directions considered during ideation, including productivity, wellbeing, AI assistance, workload tracking and student lifestyle management.

### User Flow

![User Flow](user-flow.png)

The user flow demonstrates the intended journey from onboarding and workload assessment to planning, daily check-ins, workload analysis, intervention and weekly review.

## 2.3 Mentor Consultation

| Date              | Mentor      | Feedback Received                                                                                                                                                                                                                                                                                                                                      | What Was Changed                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| :---------------- | :---------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8 September 2026  | Faris Imran | The mentor indicated that the current UI design is progressing well and remains on track. However, the team should further strengthen the application's unique selling point (USP) and clearly communicate what differentiates Ballast from competing solutions.                                                                                       | The team refined Ballast's Unique Selling Point (USP) to clearly position it as a capacity-management application for students, rather than a conventional to-do list, planner or wellness application.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|                   |             | The mentor noted that Ballast's current target audience is very broad because it is designed generally for students. The team was encouraged to identify a more specific student use case or niche that could make the application more distinctive.                                                                                                   | No changes were made to the current application. As the application is already specifically designed around measuring students' overall capacity to help them manage workload, avoid burnout and place greater emphasis on recovery and well-being.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                      |
|                   |             | Scheduling could account for activities that require preparation time in addition to the stated activity duration. Therefore, the actual time commitment is greater than the event's stated start and end time. The system could potentially account for these additional preparation requirements when calculating the user's overall capacity.&nbsp; | No changes were made to the current design. Ballast already requires students to estimate how long a task will take when creating it by selecting a task size: Small (1 hour), Medium (3 hours) or Large (8 hours). Students can also assign a Low, Medium or High priority to each task. Therefore, the task's estimated duration already provides the system with an indication of the student's required time commitment while the priority level helps reflect the importance of the task when managing their overall capacity.&nbsp;                                                                                                               |
|                   |             | The mentor clarified that the team does not need to follow a fixed set of five elements or categories exactly when developing the concept.&nbsp;                                                                                                                                                                                                       | The team restructured Ballast's original five domains Time, Mental, Physical, Social and Errands into three main domains: Time, Mental and Energy. The Social and Errands domains were consolidated under Energy, allowing students to manage academic tasks, social commitments and errands in one centralized space. The Physical domain was removed from the application as the team determined that sleep and related well-being considerations could be addressed within the Mental Well-Being dimension. This reduced unnecessary separation between categories and created a more focused structure aligned with Ballast's core purpose.&nbsp; |
| 11 September 2026 | Lim Zi Yang | The mentor advised the team to identify and emphasise a small number of standout features rather than presenting every feature in the application. The mentor recommended highlighting approximately four core features in the pitch deck to communicate Ballast's unique value proposition more clearly.&nbsp;                                        | The team identified and prioritised four core features to highlight in the pitch deck. Secondary features are still part of the system but are no longer given equal emphasis, allowing the presentation to communicate Ballast's main value proposition more clearly and concisely.&nbsp;                                                                                                                                                                                                                                                                                                                                                     |
|                   |             | The mentor suggested introducing a hands-free Voice Assistant that allows users to create tasks and deadlines through voice commands. This was proposed as a potential differentiating feature that could reduce the effort required for manual task entry.&nbsp;                                                                                      | The team incorporated a Voice Assistant concept that allows students to create tasks and deadlines through voice commands. This reduces the effort required for manual input and provides an additional convenience-focused feature that can differentiate Ballast from conventional task-management applications.&nbsp;                                                                                                                                                                                                                                                                                                                          |
|                   |             | The mentor advised the team to reconsider the use of strict application-locking mechanisms within the Pomodoro feature. Excessive restrictions may potentially increase user stress, which could conflict with Ballast's objective of helping students manage workload and prevent burnout.                                                            | No changes were made to the current design. The Pomodoro timer is designed as an optional feature, rather than a mandatory part of the student's task workflow.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|                   |             | The mentor recommended developing a specific and clearly defined problem statement rather than relying solely on the broad problem definition provided by the competition track. Each major feature should be clearly connected to an identified student problem or user pain point.                                                                   | The team refined the problem statement to focus specifically on students who have difficulty managing and balancing multiple responsibilities within their available capacity. Major features were then reviewed and connected directly to specific student pain points to ensure that each feature has a clear purpose.&nbsp;                                                                                                                                                                                                                                                                                                                    |
|                   |             | The mentor advised the team to prepare a preliminary technical stack during the design stage.&nbsp;                                                                                                                                                                                                                                                    | The team prepared a preliminary technical stack identifying the proposed technologies, frameworks, development tools and supporting technologies required to implement Ballast.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                   |             | The mentor considered the current Figma prototype to be sufficient for the prototype stage and described the current solution as more than adequate to proceed. The mentor noted that the main challenge in a subsequent development stage would be converting the prototype into a fully functional system.                                           | The team maintained the current Figma prototype while focusing further refinement on functionality, feature logic and technical feasibility rather than making unnecessary visual changes. The team also began considering how the prototype's key interactions and features could be translated into a functional system during development.&nbsp;                                                                                                                                                                                                                                                                                            |

&nbsp;

## 3. Design & Prototype

### UI Prototype

1. **Current Week Capacity**

![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/08%20%C2%B7%20Home%20-%20Load%20RingSHIP.png?raw=true)

Students view their current weekly capacity across Mental, Time and Energy. By adding commitments and completing check-ins, the capacity level updates to show whether their planned workload is manageable or approaching overload.

2. **Rebalance Proposal**

   ![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/12%20%C2%B7%20Rebalance%20proposal.png?raw=true)

   When Ballast detects an overloaded week, students can select “Add and Rebalance” at the Add Task Section. Ballast will then propose a revised schedule by changing when commitments take place while students can either Apply Plan or Tweak It before confirming.
   
3. **Recovery Plan**

   ![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/14%20%C2%B7%20Post-shift%20sequencer.png?raw=true)

   When the student's capacity becomes high, Ballast recommends recovery activities and rest periods based on their current workload and recovery needs. Students can follow the suggested plan or adjust it according to their preference.

4. **Burnout Forecast**

   ![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/18%20%C2%B7%20Burnout%20forecast.png?raw=true)

   Students can view their predicted burnout risk based on their workload, capacity and recent patterns. The forecast helps students identify when their current pace may become unsustainable and encourages earlier action.

5. **Why/How/What If**

   ![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/What%20if.png?raw=true)

   When students reach a high capacity level, they can explore why they are overloaded, how their commitments contributed to the current level and what if they continue at the same pace. This turns Ballast's capacity score into an understandable explanation rather than a simple number.

6. **Diary**

   ![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/22%20%C2%B7%20Private%20diary.png?raw=true)

   Students can privately record their thoughts, experiences and feelings. Ballast's AI can analyse diary entries alongside check-ins and workload patterns to better understand the student's emotional state and provide more personalised insights into their overall capacity. 

7. **Voice Assistant**

   ![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/24%20%C2%B7%20Speaking%20to%20it.png?raw=true)

   Students can speak naturally to Ballast to create commitments, tasks or deadlines instead of entering them manually. This reduces the effort required to capture commitments especially when students are busy or on the move. 

8. **Ballast Representing Burnout Level**

   ![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/08%20%C2%B7%20Home%20-%20Load%20RingSHIP.png?raw=true)
   ![](https://github.com/TanSuChin/CodeNection-Suchaiirmon/blob/main/UI/08%20%C2%B7%20Home%20-%20Load%20Ring.png?raw=true)

   The ballast of the ship provides a simple visual representation of the student's burnout level. As burnout risk increases, the ballast's visual state changes, allowing students to understand their current risk quickly without relying only on numbers or graphs.

## **4\. What Makes It Different**

1. **Current Week Capacity**  
   Ballast does not simply display a calendar or list of tasks. It provides an overview of the student's overall weekly capacity across three dimensions: Mental, Time and Energy.
   
- Mental Capacity represents the mental demand placed on the student.
- Time Capacity represents how much of the student's available time is occupied.
- Energy Capacity represents the overall workload from commitments such as academic tasks, errands and social events.  
  This allows students to understand the intensity of their week rather than only seeing individual deadlines. Traditional planners mainly show what the student has to do whereas Ballast focuses on whether the student has the capacity to handle everything they have planned.  
  &nbsp;

2. **Rebalance Proposal**  
   When the student's workload becomes too high, Ballast does not simply warn the student that they are overloaded. It provides a Rebalance Proposal that suggests a more manageable arrangement of their existing commitments.

- The system proposes changes to when tasks or commitments occur.
- Students can Apply Plan or Tweak It before accepting the changes.
- The student remains in control of the final schedule.  
  Instead of simply identifying an overloaded schedule, Ballast provides a practical way to reorganise the workload while preserving the student's commitments.  
  &nbsp;

3. **Recovery Plan**  
   Recovery is incorporated directly into workload management rather than being treated as a separate wellness activity.

- Ballast considers the student's need for recovery alongside their commitments.
- Recovery activities can be incorporated into the student's schedule.
- This encourages students to treat rest as part of maintaining their capacity rather than something that only happens after completing everything.  
  The application connects productivity and recovery, recognising that continuously adding tasks without allowing recovery can reduce a student's ability to manage future commitments.  
  &nbsp;

4. **Burnout Forecast**  
   Ballast provides a forward-looking indication of burnout risk based on the student's workload and capacity patterns.

- Instead of only showing the student's current workload, it helps students recognise potential problems before they become overwhelming.
- Students can observe changes in their risk over time.
- The forecast is intended as a capacity and risk-awareness tool, not a medical diagnosis.  
  Most productivity tools focus on completing tasks. Ballast focuses on preventing the student's workload from becoming unsustainable.  
  &nbsp;

5. **Why/How/What If**  
   Ballast allows students to understand the reasoning behind their capacity status rather than simply displaying a percentage.

- Why: Explains why the student's capacity is currently high.
- How: Breaks down the factors contributing to the capacity level, including different capacity areas and demanding commitments.
- What If: Shows the potential consequences of continuing with the current workload, such as increasing burnout risk or recovery debt.  
  Instead of presenting a capacity score as a black box, Ballast provides explanations that help students understand their workload and make informed decisions.  
  &nbsp;

6. **Diary**  
   The Diary allows students to privately record their thoughts, experiences and feelings throughout the week.

- Beyond being a reflection tool, the diary can provide additional emotional context for Ballast's AI analysis.
- By analysing patterns in diary entries alongside structured check-ins and workload information, the AI can gain a deeper understanding of the student's emotional state and how it may affect their overall capacity.&nbsp;
- This helps Ballast move beyond simply measuring how much work a student has to understanding how the student is actually coping with that workload.&nbsp;  
  The information can support more personalised capacity assessments, burnout-risk insights and recommendations for recovery or workload adjustment.&nbsp;  
  &nbsp;

7. **Voice Assistant**&nbsp;  
   The Voice Assistant is designed to make task entry more convenient by allowing students to create tasks and deadlines through voice interaction.

- Students can speak instead of manually entering every task.
- This can be particularly useful when students remember a commitment while travelling, studying or performing another activity.
- The feature can make task capture faster and more natural.
  Voice-based task entry provides a more hands-free and accessible method of interacting with the capacity-management system, reducing friction when recording new commitments.  
  &nbsp;

8. **Candle Representing Burnout Level**  
   Ballast uses a ship ballast as a visual representation of the student's burnout level, transforming an abstract risk measurement into an easily understandable visual metaphor.

- The level of sinkness represents the student's current burnout level.
- Changes in the sink level of the ballast provide a simple visual indication of increasing or decreasing burnout level.
- This creates a more memorable and emotionally engaging way of communicating burnout risk than relying only on percentages or graphs.  
  The ship ballast provides Ballast with a distinctive visual identity and metaphor for burnout, making an otherwise abstract concept more intuitive and recognisable to students.

&nbsp;

## **5\. Technical Architecture & Feasibility**

**Tech stack**

Tell us your frontend, backend, database, APIs and services, as well as how and where you will be hosting. For each, try to tell us why you chose that technology, and what constraints you expect to face (For example, you chose Supabase because it’s free but you’ll still need a proxy)

&nbsp;

| Component              | Proposed Technology                | Purpose                                                                                                                                               | Why Chosen                                                                                                                                                                                   | Expected Constraints                                                                                                                                                                                                              |
| ---------------------- | ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Frontend**           | **Flutter**                        | Develop the Ballast mobile application for Android.                                                                                                   | Flutter allows the team to develop for multiple platforms from a single codebase, applications.                                                                                              | The team may require additional time to learn Flutter and Dart. Some platform-specific features may also require additional configuration or native integration.                                                                  |
| **Backend**            | **Python \+ FastAPI**              | Handle capacity calculations, workload analysis, AI-related processing, business logic and communication between the mobile application and database. | Python provides access to extensive AI, NLP and data-analysis libraries while FastAPI is a high-performance Python framework designed for building APIs.                                     | AI and data-processing workloads may require optimisation depending on model complexity and available computing resources.                                                                                                        |
| **Database**           | **Firebase Cloud Firestore**       | Store user profiles, commitments, tasks, capacity data, check-ins, diary entries and other application data.                                          | Firestore is a NoSQL document database that supports structured collections and documents, real-time data synchronisation and integration with Firebase Authentication.                      | Database usage and storage costs may become a constraint as the number of users and amount of stored data increase. Data structure and security rules must also be designed carefully.                                            |
| **Authentication**     | **Firebase Authentication**        | Manage user registration, login and authentication.                                                                                                   | Firebase Authentication provides ready-made authentication services and integrates with other Firebase services, reducing the need to build authentication from scratch.                     | Authentication configuration and security rules must be implemented correctly to protect user accounts and data.                                                                                                                  |
| **AI / Data Analysis** | **Python-based AI / NLP services** | Analyse diary entries, check-in information, workload patterns and other user-provided information to generate personalised insights.                 | Python provides a wide ecosystem of AI, NLP and data-analysis libraries that can be integrated with the FastAPI backend.                                                                     | AI-generated insights must be carefully designed so that the system does not present emotional or burnout analysis as a medical diagnosis. Model availability, processing requirements and API costs may also become constraints. |
| **Notifications**      | **Firebase Cloud Messaging (FCM)** | Send morning check-in reminders and other user-controlled push notifications.                                                                         | Firebase Cloud Messaging supports customised and automated push notifications and integrates well with Firebase-based applications.&nbsp;                                                    | Users must grant notification permissions. Background delivery and scheduling may also require platform-specific handling.                                                                                                        |
| **Hosting**            | **Google Cloud Run**               | Host and run the FastAPI backend so that Ballast's API services can be accessed by the mobile application                                             | Google Cloud provides an official deployment workflow for Python FastAPI applications on Cloud Run, making it suitable for hosting the backend without maintaining a dedicated server.&nbsp; | Cloud resource usage may introduce costs as usage increases. Deployment configuration, resource limits and backend performance will need to be monitored.                                                                         |

&nbsp;

**System architecture diagram**

![][image6]

**Build plan & scope**.

During the building phase, the team will focus on implementing the core capacity-management workflow rather than attempting to build every possible feature at production scale.

The planned implementation will include:

1. **User Account**
   - Registration and login.
   - Basic user profile and preferences.
2. **Capacity Assessment**
   - Daily check-in for sleep, energy, mood and stress.
   - Calculation and display of current capacity.
3. **Commitment Management**
   - Add and manage commitments.
   - Record estimated time, importance and due date.
   - Calculate the effect of commitments on the student's capacity.
4. **Current Week Capacity**
   - Display Mental, Time and Energy capacity.
   - Energy capacity includes academic tasks, errands and social commitments.
   - Display overall load and burnout-risk indicators.
5. **Rebalance Proposal**
   - Detect when the student's planned workload becomes excessive.
   - Generate an alternative schedule by changing when commitments occur.
   - Allow the student to Apply Plan or Tweak It.
6. **Burnout & Recovery Features**
   - Burnout Forecast.
   - Recovery Debt / Recovery Plan.
   - Why / How / What If explanations.
   - Trend and risk information.
7. **Diary & AI Analysis**
   - Allow students to record private diary entries.
   - Use diary information together with check-ins and workload patterns to provide additional emotional context.
   - Use this context to improve personalised capacity insights and recommendations.
8. **Supporting Features**
   - Focus Timer.
   - Breathing technique.
   - Optional check-in streak.
   - Notifications.
   - Settings and user controls.

**Scope Limitation**

Features that increase technical complexity but are not essential to demonstrating Ballast's core value will remain outside the initial build scope or be treated as future enhancements. These include advanced integrations such as face recognition for mood detecting, home-screen widgets, focus lock and task reward.
