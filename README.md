# Ballast by [Team Name]

**Team:** [Member 1], [Member 2], [Member 3], [Member 4]
**Problem Statement:** Stress & Workload Manager
**Video Presentation:** [Unlisted YouTube Link](#)
**Presentation Slides:** [Public Link](#)

---

# 1. Project Overview

## The Problem

University students often experience burnout not because of one overwhelming responsibility, but because multiple ordinary responsibilities accumulate at the same time.

Academic assignments, classes, part-time work, social commitments, physical fatigue, and daily errands compete for a student's limited capacity. However, existing productivity and wellbeing applications generally treat these problems separately.

The main causes we identified are:

1. **Students cannot see their total workload** — commitments are scattered across calendars, university portals, messaging applications, planners, and personal memory.
2. **Workload is not one-dimensional** — mental effort, time, physical energy, social obligations, and errands affect students differently.
3. **Student capacity changes from week to week** — poor sleep, low energy, low mood, and lack of rest can make the same workload feel much heavier.
4. **The cost of new commitments is unclear** — students may accept additional responsibilities without understanding what they will have to sacrifice.
5. **Replanning is difficult when already overwhelmed** — students often need to organise themselves before existing productivity tools can help them.
6. **Rest is easily sacrificed** — assignments and work have deadlines, while rest is often treated as optional.

The underlying problem is that **burnout builds up over time rather than appearing from a single stressful day**. Therefore, students need a system that considers both their workload and their changing capacity.

### Stakeholders

| Stakeholder                            | What is at stake                                                                                    |
| -------------------------------------- | --------------------------------------------------------------------------------------------------- |
| **University Students**                | Academic performance, wellbeing, physical energy, and ability to balance multiple responsibilities. |
| **University Counselling Services**    | Earlier awareness of students experiencing prolonged workload pressure.                             |
| **Lecturers & Programme Coordinators** | Better understanding of workload pressure before it affects attendance and submissions.             |
| **Student Employers**                  | More predictable availability and reduced impact from student burnout.                              |
| **Family & Friends**                   | Better awareness of changes in a student's workload and wellbeing.                                  |

### Existing Solutions

| Existing Solution    | What It Does Well                                                                        | Why It Falls Short                                                                                                          |
| -------------------- | ---------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| **Motion**           | Automatically schedules tasks based on deadlines, priorities, duration and availability. | Focuses on fitting work into the calendar rather than determining whether the workload fits the student's current capacity. |
| **Notion / Todoist** | Good for recording and organising tasks.                                                 | Counts tasks but does not measure how mentally or physically demanding those tasks are.                                     |
| **Google Calendar**  | Useful for classes, appointments and fixed commitments.                                  | Mainly understands time and does not account for fatigue, sleep or mental capacity.                                         |
| **Daylio / Finch**   | Makes mood and wellbeing tracking simple.                                                | Tracks how users feel but does not connect their feelings to the workload causing them.                                     |
| **Forest**           | Helps users focus during individual work sessions.                                       | Focuses on one session rather than the student's overall weekly workload.                                                   |
| **Headspace / Calm** | Provides meditation and relaxation content.                                              | Addresses the feeling of stress rather than the workload contributing to it.                                                |

### The Gap

Existing applications generally fall into two categories:

- **Productivity applications** understand what students have to do.
- **Wellbeing applications** understand how students feel.

However, they rarely connect **workload + personal capacity + wellbeing**.

**Ballast is designed to bridge this gap.**

---

## Our Solution

**Ballast** is a mobile Stress & Workload Manager designed to help university students understand how much they are carrying across different areas of their lives. Instead of measuring workload only through the number of tasks or available hours, Ballast considers five dimensions: **Thinking, Time, Body, People, and Errands**. The application combines commitments with short daily check-ins such as sleep, energy, mood and stress to estimate the student's current capacity. Ballast then helps students make better decisions by suggesting schedule changes, protecting rest, warning about the cost of new commitments, and forecasting where their workload is heading.

> **"The goal was never to carry nothing. It is to know how much you are carrying."**

### Core Feature Set

#### 📊 Workload Management

- Five workload dimensions:
  - Thinking
  - Time
  - Body
  - People
  - Errands

- Overall weekly workload percentage
- Individual workload scores
- Capacity adjustment based on sleep, energy, mood and rest
- Identification of the most overloaded area
- Workload trend tracking
- Rest owed calculation

#### 📝 Daily Check-In

- 15-second daily check-in
- Sleep tracking
- Energy tracking
- Mood tracking
- Stress tracking
- Mood and workload history
- Optional check-in streak

#### 📅 Smart Planning

- Quick task entry
- Morning / afternoon / evening planning
- Priority levels
- Automatic workload categorisation
- Task sizing: Small / Medium / Large
- "I keep putting this off" flag
- Errand grouping

#### 🔄 Workload Intervention

- **Rearrange My Week**
- Automatic schedule optimisation
- Move tasks to lighter days
- Group similar errands
- Delay lower-priority tasks
- Protect scheduled rest
- Explain the reason behind every suggested change

#### ⚠️ Commitment Warning

Before accepting a new commitment, Ballast shows the potential impact on the student's workload.

Example:

> **"This takes you from 104% to 119%. To fit it in, something needs to move."**

Users can choose:

- **Add anyway**
- **Add and rearrange my week**
- **Not now**

#### 🛌 Recovery

- Protected rest blocks
- Rest recommendations
- Focus timer
- Guided breathing
- Water reminders
- Sleep reminders
- Movement reminders
- Notification limits

#### 🤖 AI Assistant

- Add tasks using natural language
- Ask questions about personal workload
- Explain workload calculations
- Explain why a workload warning was triggered
- Help users understand changes between weeks
- Provide responses based on the application's calculated data

#### 🔮 Forecasting

- 14-day workload forecast
- Burnout-risk direction
- Future scenario comparison
- Weekly review
- Personal workload patterns
- Confidence levels for predictions

#### 🔍 Explainable Workload Calculation

Users can ask:

- **Why am I seeing this?**
- **How did you calculate this?**
- **What if I remove this task?**

Ballast provides the calculation and information behind the result instead of presenting an unexplained score.

---

# 2. Ideation & Process

## 2.1 Ideas We Considered

| Idea                                               | Why it was dropped / kept                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| :------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Find User Capacity (Chosen)                        | This is the foundation of Ballast. Instead of focusing only on completing tasks, the team wanted the system to first understand how much workload a student can realistically handle as each student has their own limitations and strengths.&nbsp;                                                                                                                                                                                                                                                                                 |
| Streaks (Chosen)                                   | Streaks were considered as an optional motivation mechanism to encourage regular check-ins. The feature is kept optional because constant streak pressure could become counterproductive for students already experiencing stress.&nbsp;                                                                                                                                                                                                                                                                                            |
| Current Capacity at Log In Process (Chosen)        | Showing the user's current capacity immediately during logging in gives them an instant understanding of their current state and capacity at the starting point of the experience.&nbsp;                                                                                                                                                                                                                                                                                                                                            |
| Notification (Chosen)                              | Notifications provide timely reminders for check-ins and important capacity-related actions.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Rate Daily Sleep, Energy, Mood, Stress (Chosen)    | These inputs help Ballast understand the user's daily condition rather than relying only on scheduled tasks. They provide additional context for changes in capacity and risk.&nbsp;                                                                                                                                                                                                                                                                                                                                                |
| Current Week Capacity (Chosen)                     | Shows the user how demanding their current week is across Mental, Time, and Task capacity. Task capacity includes academic tasks, errands and social events which allow users to see not only how much time they have available but also how much overall workload they have in one setting. This helps users identify potential overload before the week becomes unmanageable.&nbsp;                                                                                                                                               |
| To do List (Chosen)                                | Gives users a central place to view and manage their academic and personal commitments. It helps users see what they need to complete within their overall weekly workload.&nbsp;                                                                                                                                                                                                                                                                                                                                                   |
| Add Task (Chosen)                                  | Allows users to add a new commitment while providing important information for Ballast's capacity assessment. Users specify how much time the task will take, how important it is (Low / Medium / High) and when it is due. This information helps Ballast understand the task's contribution to the user's workload and determine whether adding it may increase capacity pressure.&nbsp;                                                                                                                                          |
| Add Task \- Warning Capacity Overload (Chosen)     | The team wanted the system to respond when a new commitment pushes the user's capacity too high. This evolved into an important decision-support interaction rather than merely displaying a warning.&nbsp;                                                                                                                                                                                                                                                                                                                         |
| Rebalance Proposal (Chosen)                        | This became one of Ballast's main differentiating features. Instead of simply telling users that they are overloaded, Ballast proposes changes for the plan of the week so the week becomes more manageable.&nbsp;                                                                                                                                                                                                                                                                                                                  |
| Recovery Plan (Chosen)                             | Recovery was included because the concept should not only help students manage workload but also recognise the need to recover after demanding periods.&nbsp;                                                                                                                                                                                                                                                                                                                                                                       |
| Focus Timer (Chosen)                               | The focus timer supports execution after planning. It helps users work on the selected commitment while maintaining a structured focus-and-break cycle.&nbsp;                                                                                                                                                                                                                                                                                                                                                                       |
| Breathing Technique (Chosen)                       | A simple breathing activity provides an immediate low-effort recovery option when users need a short break from demanding tasks.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                              |
| Burnout Forecast (Chosen)                          | The forecast gives users a forward-looking view of potential overload rather than only showing their current state. It is positioned as a risk indicator, not a medical diagnosis.&nbsp;                                                                                                                                                                                                                                                                                                                                            |
| Trend & Risk (Chosen)                              | Tracking changes over time allows users to recognise recurring patterns in their capacity and workload instead of treating every difficult day as an isolated event.&nbsp;                                                                                                                                                                                                                                                                                                                                                          |
| Why/How/What If (Chosen)                           | This was developed to make Ballast's capacity information understandable. Why explains why capacity is high, How shows which factors and commitments contributed to it, and What If explores the possible consequences of continuing at the current load.&nbsp;                                                                                                                                                                                                                                                                     |
| Last Week Review (Chosen)                          | Reviewing the previous week allows users to reflect on workload and capacity patterns and use those observations to make better decisions for the following week.&nbsp;                                                                                                                                                                                                                                                                                                                                                             |
| Diary (Chosen)                                     | The Diary provides users with a private space to record their feelings, thoughts and daily experiences. An optional AI analysis feature can identify patterns or provide insights from diary entries, while allowing users to choose whether they want their entries to be analysed.&nbsp;                                                                                                                                                                                                                                          |
| Chat With AI (Chosen)                              | Provides students with a conversational space for emotional support and casual interaction, allowing them to talk about their current concerns and feelings in a more natural, friend-like way. It also helps students stay up to date with current issues, news and trends related to their course or field such as Marketing, Business, or IT. This gives users both emotional support and relevant awareness of what is happening in their area of study.&nbsp;&nbsp;                                                            |
| Settings (Chosen)                                  | Settings allow users to control personalisation, notifications, motivation features and data preferences, supporting a lower-pressure experience.&nbsp;                                                                                                                                                                                                                                                                                                                                                                             |
| Calendar with Google Calendar Integration (Chosen) | Google Calendar integration allows users to synchronise their existing schedules with Ballast, reducing the need to manually enter the same events or commitments into both Ballast and their personal calendar.&nbsp;                                                                                                                                                                                                                                                                                                              |
| Voice Assistant (Chosen)                           | A hands-free Voice Assistant allows users to create tasks and deadlines using voice commands, reducing the effort required for manual task entry and making it more convenient to record commitments immediately.&nbsp;                                                                                                                                                                                                                                                                                                             |
| Visual Burnout Level Representation (Chosen)       | A candle was introduced as a visual representation of the user's burnout level and capacity. The candle's flame decreases as the user's condition approaches burnout, allowing users to understand their current capacity quickly through a simple visual representation rather than relying only on graphs and numerical values.&nbsp;                                                                                                                                                                                             |
| Face Recognition for Mood Detecting&nbsp;          | The team explored automatically detecting mood through facial expressions but it introduced unnecessary privacy, accuracy and technical concerns. Manual self-reporting was considered more appropriate for the prototype.&nbsp;                                                                                                                                                                                                                                                                                                    |
| Social To Do List&nbsp;                            | The idea of separating social commitments into a dedicated task list was explored but it could make it inconvenient for users to keep track of different types of responsibilities across multiple sections. Social commitments were instead incorporated into the broader Task feature alongside academic tasks and errands, allowing users to view all their upcoming responsibilities and commitments in one centralized location.&nbsp;                                                                                         |
| Errands To Do List                                 | The idea of separating errands into a dedicated task list was explored but it could make it inconvenient for users to keep track of different types of responsibilities across multiple sections. Errands were instead incorporated into the broader Task feature alongside academic and social tasks, allowing users to view all their upcoming responsibilities in one centralized location.&nbsp;                                                                                                                                |
| Physical Well Being                                | A dedicated physical well-being feature was initially considered but it was dropped to avoid unnecessarily separating sleep from the user's overall well-being. Sleep was instead considered as part of mental well-being as sleep quality can have a significant impact on a user's mental and emotional well-being.&nbsp;                                                                                                                                                                                                         |
| Task Reward                                        | The idea of rewarding users with points after completing tasks and allowing them to redeem rewards such as Tealive vouchers was initially considered. However, implementing real-world vouchers would require integration with third-party services and involve additional legal, regulatory and operational considerations, making it unrealistic for the current scope of the system. This feature is therefore considered a potential scalability feature for future development.&nbsp;&nbsp;                                    |
| New/Article&nbsp;                                  | A dedicated section for course-related news and articles was initially considered to help users stay updated with current trends and developments in their field of study. However, this was removed as a separate feature because similar information can instead be provided through the Chat with AI feature, allowing users to ask for relevant updates within the conversation. This approach also reduces potential copyright concerns associated with directly displaying or reproducing external news articles.&nbsp;&nbsp; |
| Home Screen Widget                                 | A widget could give users quick access to their Ballast information directly from their phone's home screen. However, it was not essential to the core capacity-management experience and would require additional platform-specific development. It was therefore left out of the current prototype to keep the project scope realistic.&nbsp;                                                                                                                                                                                     |
| Focus Lock                                         | This feature was intended to encourage users to reconsider interrupting a Pomodoro focus session before opening a blocked app. However, implementing app blocking and controlling access to other applications would require deeper operating-system-level functionality. Since Ballast's main focus is capacity management rather than strict app restriction, this feature was excluded from the current scope.&nbsp;                                                                                                             |

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
|                   |             | Scheduling could account for activities that require preparation time in addition to the stated activity duration. Therefore, the actual time commitment is greater than the event's stated start and end time. The system could potentially account for these additional preparation requirements when calculating the user's overall capacity.&nbsp; | No changes were made to the current design. Ballast already requires users to estimate how long a task will take when creating it by selecting a task size: Small (1 hour), Medium (3 hours) or Large (8 hours). Users can also assign a Low, Medium or High priority to each task. Therefore, the task's estimated duration already provides the system with an indication of the user's required time commitment while the priority level helps reflect the importance of the task when managing their overall capacity.&nbsp;                                                                                                               |
|                   |             | The mentor clarified that the team does not need to follow a fixed set of five elements or categories exactly when developing the concept.&nbsp;                                                                                                                                                                                                       | The team restructured Ballast's original five domains Time, Mental, Physical, Social and Errands into three main domains: Time, Mental and Task. The Social and Errands domains were consolidated under Task, allowing users to manage academic tasks, social commitments and errands in one centralized space. The Physical domain was removed from the application as the team determined that sleep and related well-being considerations could be addressed within the Mental Well-Being dimension. This reduced unnecessary separation between categories and created a more focused structure aligned with Ballast's core purpose.&nbsp; |
| 11 September 2026 | Lim Zi Yang | The mentor advised the team to identify and emphasise a small number of standout features rather than presenting every feature in the application. The mentor recommended highlighting approximately four core features in the pitch deck to communicate Ballast's unique value proposition more clearly.&nbsp;                                        | The team identified and prioritised four core features to highlight in the pitch deck. Secondary features are still part of the system but are no longer given equal emphasis, allowing the presentation to communicate Ballast's main value proposition more clearly and concisely.&nbsp;                                                                                                                                                                                                                                                                                                                                                     |
|                   |             | The mentor suggested introducing a hands-free Voice Assistant that allows users to create tasks and deadlines through voice commands. This was proposed as a potential differentiating feature that could reduce the effort required for manual task entry.&nbsp;                                                                                      | The team incorporated a Voice Assistant concept that allows users to create tasks and deadlines through voice commands. This reduces the effort required for manual input and provides an additional convenience-focused feature that can differentiate Ballast from conventional task-management applications.&nbsp;                                                                                                                                                                                                                                                                                                                          |
|                   |             | The mentor advised the team to reconsider the use of strict application-locking mechanisms within the Pomodoro feature. Excessive restrictions may potentially increase user stress, which could conflict with Ballast's objective of helping students manage workload and prevent burnout.                                                            | No changes were made to the current design. The Pomodoro timer is designed as an optional feature, rather than a mandatory part of the user's task workflow.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|                   |             | The mentor recommended developing a specific and clearly defined problem statement rather than relying solely on the broad problem definition provided by the competition track. Each major feature should be clearly connected to an identified student problem or user pain point.                                                                   | The team refined the problem statement to focus specifically on students who have difficulty managing and balancing multiple responsibilities within their available capacity. Major features were then reviewed and connected directly to specific user pain points to ensure that each feature has a clear purpose.&nbsp;                                                                                                                                                                                                                                                                                                                    |
|                   |             | The mentor advised the team to prepare a preliminary technical stack during the design stage.&nbsp;                                                                                                                                                                                                                                                    | The team prepared a preliminary technical stack identifying the proposed technologies, frameworks, development tools and supporting technologies required to implement Ballast.&nbsp;                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                   |             | The mentor considered the current Figma prototype to be sufficient for the prototype stage and described the current solution as more than adequate to proceed. The mentor noted that the main challenge in a subsequent development stage would be converting the prototype into a fully functional system.                                           | The team maintained the current Figma prototype while focusing further refinement on functionality, feature logic and technical feasibility rather than making unnecessary visual changes. The team also began considering how the prototype's key interactions and features could be translated into a functional system during development.&nbsp;                                                                                                                                                                                                                                                                                            |

&nbsp;

## **3\. Design & Prototype**

**UI Prototype:**&nbsp;

1. Current Week Capacity&nbsp;  
   &nbsp;  
   Users view their current weekly capacity across Mental, Time and Task. By adding commitments and completing check-ins, the capacity level updates to show whether their planned workload is manageable or approaching overload.&nbsp;
2. Rebalance Proposal  
   ![][image1]  
   When Ballast detects an overloaded week, users can select “Add and Rebalance” at the Add Task Section. Ballast will then propose a revised schedule by changing when commitments take place while users can either Apply Plan or Tweak It before confirming.&nbsp;
3. Recovery Plan  
   ![][image2]  
   When the user's capacity becomes high, Ballast recommends recovery activities and rest periods based on their current workload and recovery needs. Users can follow the suggested plan or adjust it according to their preference.&nbsp;
4. Burnout Forecast  
   ![][image3]  
   Users can view their predicted burnout risk based on their workload, capacity and recent patterns. The forecast helps users identify when their current pace may become unsustainable and encourages earlier action.&nbsp;
5. Why/How/What If  
   ![][image4]  
   When users reach a high capacity level, they can explore Why they are overloaded, How their commitments contributed to the current level and What If they continue at the same pace. This turns Ballast's capacity score into an understandable explanation rather than a simple number.&nbsp;
6. Diary  
   ![][image5]  
   Users can privately record their thoughts, experiences and feelings. Ballast's AI can analyse diary entries alongside check-ins and workload patterns to better understand the user's emotional state and provide more personalised insights into their overall capacity.&nbsp;
7. Voice Assistant&nbsp;  
   &nbsp;  
   Users can speak naturally to Ballast to create commitments, tasks or deadlines instead of entering them manually. This reduces the effort required to capture commitments especially when users are busy or on the move.&nbsp;
8. Candle Representing Burnout Level  
   &nbsp;  
   The candle provides a simple visual representation of the user's burnout level. As burnout risk increases, the candle's visual state changes, allowing users to understand their current risk quickly without relying only on numbers or graphs.&nbsp;

We recommend you embed or link 4–8 key screens as images, with a caption on each explaining the interaction

## **4\. What Makes It Different**

1. **Current Week Capacity**  
   Ballast does not simply display a calendar or list of tasks. It provides an overview of the user's overall weekly capacity across three dimensions: Mental, Time and Task.

- Mental Capacity represents the mental demand placed on the student.
- Time Capacity represents how much of the student's available time is occupied.
- Task Capacity represents the overall workload from commitments such as academic tasks, errands and social events.  
  This allows students to understand the intensity of their week rather than only seeing individual deadlines. Traditional planners mainly show what the student has to do whereas Ballast focuses on whether the student has the capacity to handle everything they have planned.  
  &nbsp;

2. **Rebalance Proposal**  
   When the user's workload becomes too high, Ballast does not simply warn the user that they are overloaded. It provides a Rebalance Proposal that suggests a more manageable arrangement of their existing commitments.

- The system proposes changes to when tasks or commitments occur.
- Users can Apply Plan or Tweak It before accepting the changes.
- The user remains in control of the final schedule.  
  Instead of simply identifying an overloaded schedule, Ballast provides a practical way to reorganise the workload while preserving the user's commitments.  
  &nbsp;

3. **Recovery Plan**  
   Recovery is incorporated directly into workload management rather than being treated as a separate wellness activity.

- Ballast considers the user's need for recovery alongside their commitments.
- Recovery activities can be incorporated into the user's schedule.
- This encourages students to treat rest as part of maintaining their capacity rather than something that only happens after completing everything.  
  The application connects productivity and recovery, recognising that continuously adding tasks without allowing recovery can reduce a student's ability to manage future commitments.  
  &nbsp;

4. **Burnout Forecast**  
   Ballast provides a forward-looking indication of burnout risk based on the user's workload and capacity patterns.

- Instead of only showing the user's current workload, it helps users recognise potential problems before they become overwhelming.
- Users can observe changes in their risk over time.
- The forecast is intended as a capacity and risk-awareness tool, not a medical diagnosis.  
  Most productivity tools focus on completing tasks. Ballast focuses on preventing the user's workload from becoming unsustainable.  
  &nbsp;

5. **Why/How/What If**  
   Ballast allows users to understand the reasoning behind their capacity status rather than simply displaying a percentage.

- Why: Explains why the user's capacity is currently high.
- How: Breaks down the factors contributing to the capacity level, including different capacity areas and demanding commitments.
- What If: Shows the potential consequences of continuing with the current workload, such as increasing burnout risk or recovery debt.  
  Instead of presenting a capacity score as a black box, Ballast provides explanations that help users understand their workload and make informed decisions.  
  &nbsp;

6. **Diary**  
   The Diary allows students to privately record their thoughts, experiences and feelings throughout the week.

- Beyond being a reflection tool, the diary can provide additional emotional context for Ballast's AI analysis.
- By analysing patterns in diary entries alongside structured check-ins and workload information, the AI can gain a deeper understanding of the user's emotional state and how it may affect their overall capacity.&nbsp;
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
   Ballast uses a candle as a visual representation of the user's burnout level, transforming an abstract risk measurement into an easily understandable visual metaphor.

- The candle represents the user's current burnout level.
- Changes in the candle provide a simple visual indication of increasing or decreasing burnout level.
- This creates a more memorable and emotionally engaging way of communicating burnout risk than relying only on percentages or graphs.  
  The candle provides Ballast with a distinctive visual identity and metaphor for burnout, making an otherwise abstract concept more intuitive and recognisable to users.

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
   - Initial capacity assessment.
   - Daily check-in for sleep, energy, mood and stress.
   - Calculation and display of current capacity.
3. **Commitment Management**
   - Add and manage commitments.
   - Record estimated time, importance and due date.
   - Calculate the effect of commitments on the user's capacity.
4. **Current Week Capacity**
   - Display Mental, Time and Task capacity.
   - Task capacity includes academic tasks, errands and social commitments.
   - Display overall load and burnout-risk indicators.
5. **Rebalance Proposal**
   - Detect when the user's planned workload becomes excessive.
   - Generate an alternative schedule by changing when commitments occur.
   - Allow the user to Apply Plan or Tweak It.
6. **Burnout & Recovery Features**
   - Burnout Forecast.
   - Recovery Debt / Recovery Plan.
   - Why / How / What If explanations.
   - Trend and risk information.
7. **Diary & AI Analysis**
   - Allow users to record private diary entries.
   - Use diary information together with check-ins and workload patterns to provide additional emotional context.
   - Use this context to improve personalised capacity insights and recommendations.
8. **Supporting Features**
   - Focus Timer.
   - Breathing technique.
   - Optional check-in streak.
   - Notifications.
   - Settings and user controls.

**Scope Limitation**

Features that increase technical complexity but are not essential to demonstrating Ballast's core value will remain outside the initial build scope or be treated as future enhancements. These include advanced integrations such as Google Calendar integration, home-screen widgets, focus lock and task reward.
