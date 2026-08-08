# 🤖 PROMPTS.md

<div align="center">

# InterviewOS AI — AI Usage Log

### **Don't Build the Interview. Build the Interviewer.**

**VicoDathon — Problem Statement 2: The Interview Agent**

</div>

---

## 📌 Purpose

This document records how AI-assisted development was used while building **InterviewOS AI**.

The project was developed iteratively using AI as a development assistant for:

* Product planning
* Architecture decisions
* UI/UX improvements
* React and TypeScript development
* Interview-engine logic
* Adaptive follow-up design
* API design
* Debugging
* Validation
* Documentation
* README generation
* Testing and refinement

AI was used as an **engineering assistant**, while implementation decisions, integration, testing, verification, and final project direction remained part of the development process.

> **No API keys, passwords, private credentials, or secrets are included in this document.**

---

# 🧠 01 — Project Ideation

### Objective

Define the core concept for the hackathon problem:

> **"Don't Build the Interview. Build the Interviewer."**

### Prompt

```text
I am building a hackathon project for:

Problem Statement 2 — The Interview Agent

Core idea:
"Don't Build the Interview. Build the Interviewer."

I want to build an adaptive technical interview platform.

The interviewer should:
- ask technical questions
- understand candidate responses
- maintain conversation context
- generate follow-up questions
- adapt based on answer quality
- cover multiple curriculum days
- evaluate the candidate
- provide actionable feedback

Help me define the product architecture, user flow, core features, and technical approach.

The product should feel like a real interviewer rather than a static question bank.
```

### Result

The project direction was established around:

```text
Candidate
    ↓
Interview Setup
    ↓
AI Interviewer
    ↓
Question
    ↓
Candidate Answer
    ↓
Analysis
    ↓
Adaptive Follow-up
    ↓
Context
    ↓
Evaluation
```

---

# 🏗️ 02 — Product Architecture

### Objective

Design a system where the interviewer can maintain context across multiple turns.

### Prompt

```text
Design an architecture for an adaptive multi-turn interview system.

Requirements:

1. Candidate profiles
2. Curriculum data
3. Interview sessions
4. Questions
5. Candidate answers
6. Answer analysis
7. Follow-up questions
8. Conversation memory
9. Curriculum coverage
10. Interview completion rules
11. Structured assessment

The system should support a POST /api/interview endpoint.

The core interview logic should be deterministic enough to work without requiring an external API key.

Separate:
- frontend
- API
- session state
- interview engine
- curriculum data
- candidate data
- provider/phrasing layer
```

### Result

The architecture evolved into:

```text
React Frontend
       ↓
POST /api/interview
       ↓
Session Store
       ↓
Interview Engine
       ↓
Curriculum + Candidate Data
       ↓
Adaptive Decision
       ↓
Next Question
       ↓
Assessment
```

---

# 📚 03 — Curriculum Data

### Objective

Create a curriculum-aware interview system instead of a generic question generator.

### Prompt

```text
Design a curriculum structure for a 31-day AI Cohort.

The interview engine should be able to identify:

- day
- day title
- topic
- difficulty level
- question type
- primary questions
- follow-up questions
- context probes

The curriculum should cover modern AI topics such as:

RAG
Vector Databases
Prompt Engineering
Agentic AI
MCP
AI Deployment
Production AI Systems

The data should be easy for a TypeScript interview engine to consume.
```

### Result

The project introduced curriculum data that could be connected to:

* candidate progress
* completed days
* attempted days
* skipped days
* topics
* learning signals

---

# 👤 04 — Candidate Profiles

### Objective

Create realistic candidate journeys so that different candidates can receive different interview contexts.

### Prompt

```text
Create a candidate data model for an AI interview platform.

Each candidate should have:

- id
- name
- title
- avatar initials
- learning track
- mission history
- completed curriculum days
- attempted curriculum days
- skipped curriculum days
- strengths
- risks

Create several sample candidates with different learning journeys.

The data should be suitable for a TypeScript / JSON based demo application.
```

### Result

The demo introduced four candidate profiles:

```text
Sarah Chen
Marcus Lee
Priya Nair
Diego Alvarez
```

Each candidate has a distinct learning journey.

---

# 🎙️ 05 — Interview Engine

### Objective

Build the core behaviour of the interviewer.

### Prompt

```text
Design a deterministic interview engine for a multi-turn technical interview.

The engine receives:

- candidate profile
- curriculum
- previous questions
- previous answers
- covered curriculum days
- topics
- answer quality
- strong signals
- areas requiring probing

The engine should decide whether the next question should be:

1. primary
2. followup
3. context-probe

It should avoid repeating the same question.

It should maintain conversation context.

The engine should also ensure the interview eventually covers at least 4 distinct curriculum days and at least 8 questions.
```

### Result

The engine was structured around:

```text
Previous Context
      ↓
Candidate Answer
      ↓
Answer Quality
      ↓
Covered Topics
      ↓
Curriculum Coverage
      ↓
Decision
      ↓
Primary / Follow-up / Context Probe
```

---

# 🔄 06 — Adaptive Follow-up Logic

### Objective

Make the interview conversational rather than sequential.

### Prompt

```text
Design adaptive follow-up behaviour.

If a candidate gives a strong technical answer:
- ask a deeper question
- explore trade-offs
- test architecture reasoning

If the candidate gives a partial answer:
- ask a clarification question
- target the missing concept

If the candidate gives a weak answer:
- return toward fundamentals
- avoid abruptly changing topics

If the candidate previously mentioned an important concept:
- allow a later context-probe question to reference it

Maintain conversation context throughout the session.
```

### Result

Follow-up behaviour became one of the central parts of the interview experience.

---

# 🧠 07 — Interview Memory

### Objective

Give the interviewer a memory model.

### Prompt

```text
Design an interview memory structure for a technical AI interviewer.

The memory should track:

- covered topics
- strong signals
- needs probing
- not assessed
- questions asked
- answers
- curriculum days covered
- difficulty
- answer quality
- strengths
- gaps

Explain how this memory can be updated after every candidate answer.
```

### Result

The UI exposes:

```text
Covered
Strong Signals
Needs Probing
Not Assessed
```

This memory is updated as the interview progresses.

---

# 📊 08 — Interview Progress

### Objective

Make curriculum coverage and interview progress visible.

### Prompt

```text
Design a progress model for an interview that requires:

Minimum questions = 8
Minimum curriculum days = 4

The API should expose:

questionNumber
questionsAsked
minQuestions
daysCovered
minDays

The frontend should show:
- current question
- completed questions
- upcoming questions
- curriculum coverage
- completion readiness
```

### Result

The interview workspace exposes progress and curriculum coverage.

---

# 🏁 09 — Completion Logic

### Objective

Prevent premature interview completion.

### Prompt

```text
Implement interview completion logic.

The interview should only be considered complete when:

questionsAsked >= 8

AND

distinct curriculum days covered >= 4

Return done: false until both requirements are satisfied.

When complete, return:
- feedback
- assessment
- overall score
- dimensions
- learning plan
```

### Result

Completion is controlled by explicit interview gates.

```text
Questions >= 8
       +
Days >= 4
       ↓
Interview Complete
       ↓
Assessment
```

---

# 📈 10 — Assessment System

### Objective

Create structured feedback from the actual interview history.

### Prompt

```text
Design a structured technical interview assessment.

The final assessment should include:

feedback:
- summary
- strengths
- gaps
- next

assessment:
- overallScore
- headline
- dimensions
- learningPlan

The result should be based on the candidate's actual answer history and interview performance.

Avoid random scores or arbitrary feedback.
```

### Result

The final assessment is structured around:

```text
Interview History
      ↓
Performance Signals
      ↓
Overall Score
      ↓
Dimensions
      ↓
Strengths
      ↓
Gaps
      ↓
Learning Plan
```

---

# 🔌 11 — API Design

### Objective

Create one central API endpoint for interview interaction.

### Prompt

```text
Design a POST /api/interview endpoint.

Starting request:

{
  "sessionId": "unique-session-id",
  "candidate": {
    "id": "sarah-chen"
  }
}

Subsequent request:

{
  "sessionId": "unique-session-id",
  "message": "candidate answer"
}

The endpoint should support:

- starting sessions
- submitting answers
- returning questions
- returning progress
- returning memory
- returning candidate information
- returning engine information
- returning feedback when completed

Define useful HTTP error codes.
```

### Result

The central endpoint became:

```text
POST /api/interview
```

with structured in-progress and completed response shapes.

---

# 🛡️ 12 — Error Handling

### Objective

Make API failures predictable and easy for the frontend to handle.

### Prompt

```text
Define API error handling for:

invalid JSON
invalid request
empty answer
invalid session
missing candidate
engine error

Use HTTP status codes:

400
404
500

Return:

{
  "error": "code",
  "message": "human readable"
}
```

### Result

The API uses structured errors:

```text
400 invalid_json
400 invalid_request
400 empty_answer

404 invalid_session
404 missing_candidate

500 engine_error
```

---

# 🎨 13 — UI/UX Direction

### Objective

Make the application feel like a premium AI interview command center.

### Prompt

```text
Design a premium futuristic AI interview interface.

Visual direction:

- deep black background
- charcoal surfaces
- violet / indigo gradients
- electric blue accents
- subtle cyan highlights
- glassmorphism
- cinematic depth
- premium typography
- command-center aesthetic

The UI should communicate:
- AI thinking
- listening
- analysing
- adapting
- progress
- memory
- assessment

Do not make it look like a generic dashboard.
It should feel like a real AI interviewer product.
```

### Result

The visual system was built around:

```text
BLACK
 +
GLASS
 +
VIOLET
 +
BLUE
 +
CYAN
 +
MOTION
```

---

# ✨ 14 — Animation & Motion

### Objective

Use animation to communicate system state.

### Prompt

```text
Improve the interview UI with Framer Motion.

Add animations for:

- landing page entrance
- staggered content reveals
- card transitions
- question transitions
- thinking indicator
- progress changes
- state changes
- feedback transition

Animation should communicate system state rather than simply being decorative.

Keep the experience professional and fast.
```

### Result

Motion was integrated around meaningful product states.

```text
READY
 ↓
ASKING
 ↓
LISTENING
 ↓
ANALYSING
 ↓
ADAPTING
 ↓
FOLLOW-UP
 ↓
COMPLETED
```

---

# 🧩 15 — Interview Components

### Objective

Break the interview workspace into reusable React components.

### Prompt

```text
Create a reusable React component structure for the interview workspace.

Components should include:

- InterviewHeader
- InterviewProgress
- CurriculumCoverage
- InterviewMemoryPanel
- InterviewMessage
- AnswerComposer
- ThinkingIndicator
- CandidateCard
- FeedbackScore
- FeedbackSection
- LearningPlan

Keep components focused and reusable.

Use TypeScript.
```

### Result

The interview UI was organized into reusable components.

---

# 📱 16 — Responsive Design

### Objective

Make the application usable across screen sizes.

### Prompt

```text
Make the InterviewOS interface responsive.

Requirements:

- desktop interview command center
- tablet-friendly layout
- mobile-friendly layout
- avoid horizontal overflow
- preserve question readability
- keep answer composer accessible
- make memory and progress panels adapt to smaller screens

Use Tailwind CSS responsive utilities.
```

### Result

Responsive behaviour was incorporated throughout the interview experience.

---

# 🧪 17 — Testing & Verification

### Objective

Verify the complete interview flow.

### Prompt

```text
Create a testing checklist for an adaptive technical interview application.

Verify:

1. Landing page
2. Candidate selection
3. Session creation
4. First question
5. Answer submission
6. Empty answer rejection
7. Follow-up generation
8. Context preservation
9. Progress updates
10. Curriculum coverage
11. Minimum 8 questions
12. Minimum 4 curriculum days
13. Completion
14. Feedback
15. Assessment
16. Responsive UI
17. API error states
```

### Result

Testing was organized around the complete user journey.

---

# 🐛 18 — Debugging

AI assistance was also used to reason about development issues such as:

* TypeScript errors
* React component problems
* API response mismatches
* State management issues
* Routing issues
* Responsive layout problems
* Animation behaviour
* Request validation
* Error handling

Typical debugging workflow:

```text
Problem
  ↓
Inspect Error
  ↓
Identify Root Cause
  ↓
Propose Fix
  ↓
Implement
  ↓
Run / Verify
  ↓
Refine
```

AI suggestions were reviewed before being integrated into the application.

---

# 📖 19 — Documentation

### Objective

Create professional project documentation for judges and developers.

### Prompt

```text
Create a professional README for InterviewOS AI.

The README should communicate:

- what the project does
- why it exists
- problem statement
- product philosophy
- core features
- adaptive interview flow
- curriculum intelligence
- interview memory
- assessment
- architecture
- data flow
- API
- tech stack
- project structure
- local setup
- testing
- hackathon requirements
- roadmap
- developer information

Make the README feel like a premium AI startup product rather than a basic college project.
```

### Result

The project README was structured around the product experience rather than only technical documentation.

---

# 🎯 20 — Hackathon Alignment

### Objective

Ensure the implementation directly addresses Problem Statement 2.

### Prompt

```text
Review the InterviewOS implementation against this hackathon requirement:

Problem Statement 2 — The Interview Agent

Requirements:

- conversational technical interview
- minimum 8 questions
- minimum 4 curriculum days
- follow-up questions based on previous responses
- conversation context
- structured feedback
- POST /api/interview

Identify missing requirements and recommend implementation changes without inventing unnecessary features.
```

### Result

The implementation was aligned around the required behaviours:

```text
Conversation
     +
Context
     +
Follow-up
     +
Curriculum Coverage
     +
Evaluation
```

---

# 🔐 21 — Security / Secret Handling

AI assistance was used with an explicit requirement not to expose secrets.

### Rule

```text
Never place:
- API keys
- passwords
- tokens
- private credentials
- environment secrets

inside:
- source code
- README
- PROMPTS.md
- screenshots
- public repository files
```

The repository documentation does not intentionally contain private credentials.

---

# 🧠 22 — AI Development Philosophy

AI was treated as a **development partner**, not as an automatic source of truth.

The general workflow was:

```text
Human Idea
    ↓
AI Exploration
    ↓
Human Decision
    ↓
Implementation
    ↓
Testing
    ↓
AI-assisted Debugging
    ↓
Human Verification
    ↓
Final Product
```

This approach helped accelerate development while keeping the final implementation under developer control.

---

# 📋 23 — Prompt Categories

| Category         | Purpose                         |
| ---------------- | ------------------------------- |
| 💡 Ideation      | Define the product              |
| 🏗️ Architecture | Design system structure         |
| 📚 Data          | Curriculum and candidate models |
| 🧠 AI Logic      | Interviewer behaviour           |
| 🔄 Adaptation    | Follow-ups and context          |
| 📊 Assessment    | Feedback and scoring            |
| 🔌 API           | Endpoint and response design    |
| 🎨 UI/UX         | Visual system                   |
| ✨ Motion         | Animations and transitions      |
| 🧩 Components    | React architecture              |
| 🧪 Testing       | Verification                    |
| 🐛 Debugging     | Error resolution                |
| 📖 Documentation | README and technical docs       |

---

# 🏆 Final Product Concept

The entire AI-assisted development process remained centered around one principle:

```text
        ┌─────────────────────────┐
        │  DON'T BUILD THE        │
        │       INTERVIEW         │
        └────────────┬────────────┘
                     ↓
        ┌─────────────────────────┐
        │  BUILD THE INTERVIEWER  │
        └────────────┬────────────┘
                     ↓
               LISTEN
                     ↓
             UNDERSTAND
                     ↓
               REMEMBER
                     ↓
                ADAPT
                     ↓
               PROBE
                     ↓
              EVALUATE
                     ↓
               IMPROVE
```

---

<div align="center">

# 🎙️ InterviewOS AI

### **Don't Build the Interview. Build the Interviewer.**

**Built for VicoDathon — Problem Statement 2**

</div>
