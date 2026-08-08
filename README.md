# 🎙️ InterviewOS — Your AI Technical Interviewer

> **Turn your learning journey into interview confidence.**

InterviewOS is an AI-powered technical interview platform designed for learners completing the **31-Day AI Cohort**.

Instead of giving candidates a fixed list of questions, InterviewOS analyzes their learning journey, starts a contextual technical interview, adapts follow-up questions based on their answers, and finishes with structured feedback.

---

## 🚀 Live Product

### [Launch InterviewOS →](https://vico-dathon-pb-2.vercel.app/)

| Resource          | Link                                                                                  |
| ----------------- | ------------------------------------------------------------------------------------- |
| 🌐 Live Demo      | [vico-dathon-pb-2.vercel.app](https://vico-dathon-pb-2.vercel.app/)                   |
| 💻 Source Code    | [VicoDathon-pb-2](https://github.com/dhanush080607/VicoDathon-pb-2)                   |
| 📜 Commit History | [View GitHub Commits](https://github.com/dhanush080607/VicoDathon-pb-2/commits/main/) |
| 👤 Developer      | [H Dhanush](https://www.linkedin.com/in/h-dhanush-189565327/)                         |

---

# 🧠 The Challenge

Completing an AI engineering cohort teaches learners how to build systems.

But there is another skill that is often overlooked:

> **Can you explain what you built and why you built it?**

A learner may understand:

* RAG
* Vector databases
* Prompt engineering
* Agentic AI
* MCP
* AI deployment
* Production AI systems

Yet during an interview, they may struggle to explain their decisions, defend their architecture, or respond to technical follow-ups.

InterviewOS is designed to bridge that gap.

---

# 💡 The Core Idea

InterviewOS doesn't behave like a quiz.

It behaves like an **interviewer**.

```text
                    CANDIDATE
                        │
                        ▼
              ┌──────────────────┐
              │ Learning Journey │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Candidate Model  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Interview Agent  │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Technical Q&A    │
              └────────┬─────────┘
                       │
              ┌────────┴────────┐
              ▼                 ▼
       Candidate Answer    Learning Context
              │                 │
              └────────┬────────┘
                       ▼
              ┌──────────────────┐
              │ Adaptive Follow- │
              │ Up Generation    │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Interview Report │
              └──────────────────┘
```

---

# 🎯 PRODUCT PROMISE

### **Don't memorize interview questions.**

### **Learn to think through technical problems.**

InterviewOS evaluates not only whether a candidate knows an answer, but also how they explain:

* Concepts
* Architecture
* Engineering decisions
* Trade-offs
* Implementation choices
* Real-world applications

---

# 🧩 HOW THE INTERVIEW WORKS

## 01 — Candidate Context

The agent begins with the candidate's learning journey.

It can consider signals such as:

```text
Completed Missions
       +
Attempts
       +
Skipped Topics
       +
Learning Signals
       +
Curriculum Coverage
```

This creates a more relevant interview than asking the same questions to everyone.

---

## 02 — Technical Interview

The interview begins with a question related to the candidate's completed learning.

For example:

> **"You built a RAG pipeline. Explain why you chose retrieval instead of relying entirely on the language model."**

The candidate answers naturally.

There is no predefined "A/B/C/D" questionnaire.

---

## 03 — Adaptive Follow-Ups

This is the core experience.

```text
Candidate Answer
       │
       ▼
Understand Response
       │
       ├───────────────┐
       ▼               ▼
  Strong Answer    Weak Answer
       │               │
       ▼               ▼
   Go Deeper       Clarify Concept
       │               │
       └───────┬───────┘
               ▼
        Next Question
```

A strong answer can trigger a deeper engineering question.

An incomplete answer can trigger clarification.

A confused answer can lead to a simpler conceptual probe.

The interview therefore evolves around the candidate rather than following a rigid script.

---

# 🧠 CONTEXT-AWARE INTERVIEWING

InterviewOS maintains the conversation context throughout the session.

The agent can use:

```text
Previous Questions
        +
Previous Answers
        +
Candidate Profile
        +
Curriculum
        +
Current Interview State
        ↓
Next Question
```

This allows the conversation to feel continuous instead of disconnected.

---

# 📚 CURRICULUM-AWARE QUESTIONING

The AI Cohort covers modern AI engineering.

InterviewOS can explore multiple curriculum areas including:

| Area                  | Example Interview Focus           |
| --------------------- | --------------------------------- |
| 🔎 RAG                | Retrieval pipeline design         |
| 🗄️ Vector Databases  | Embeddings and similarity search  |
| ✍️ Prompt Engineering | Prompt design and reliability     |
| 🤖 Agentic AI         | Agent architecture and tool usage |
| 🔌 MCP                | Context and tool interoperability |
| 🚀 AI Deployment      | Serving AI systems                |
| 🏗️ Production AI     | Scalability and reliability       |

The interview is designed to cover **multiple curriculum days**, rather than repeatedly testing a single topic.

---

# 🎤 INTERVIEW EXPERIENCE

The interface is intentionally focused.

### Candidate sees:

```text
┌───────────────────────────────┐
│        INTERVIEW  •  04/08    │
│                               │
│  AI Engineering Interview     │
│                               │
│  ───────────────────────────  │
│                               │
│  Your Question                │
│                               │
│  Explain how your RAG system  │
│  handles irrelevant results.  │
│                               │
│  ┌─────────────────────────┐  │
│  │ Type your answer...     │  │
│  │                         │  │
│  │                         │  │
│  └─────────────────────────┘  │
│                               │
│       [ Submit Answer ]       │
└───────────────────────────────┘
```

The UI keeps the candidate focused on the conversation rather than overwhelming them with unnecessary controls.

---

# 📊 INTERVIEW PROGRESS

The experience provides clear progress throughout the session.

Example:

```text
QUESTION 04 / 08+

████████████░░░░░░░░

Curriculum Coverage

RAG              ✓
Vector DB        ✓
Prompting        ✓
Agents           →
MCP              🔒
Deployment       🔒
```

The exact conversation can continue beyond the minimum interview requirement when additional probing is valuable.

---

# 🧠 INTELLIGENCE LAYER

The interview engine can reason about candidate responses using several signals.

### Response understanding

```text
Candidate Response
        ↓
Technical Relevance
        ↓
Concept Understanding
        ↓
Depth
        ↓
Confidence
        ↓
Missing Knowledge
        ↓
Follow-Up Strategy
```

Possible follow-up strategies include:

### 🔍 Deep Dive

Used when the candidate demonstrates strong understanding.

### 🧩 Clarification

Used when an explanation is incomplete.

### ⚖️ Trade-Off Probe

Used to test engineering decision-making.

### 🏗️ Architecture Probe

Used to move from theory into system design.

### 🌍 Real-World Scenario

Used to test practical application.

---

# 📝 FINAL INTERVIEW REPORT

The interview ends with structured feedback rather than simply displaying a score.

The candidate receives insight into:

```text
┌──────────────────────────────┐
│      INTERVIEW REPORT        │
├──────────────────────────────┤
│                              │
│ Overall Performance          │
│ ███████████████░░  78%       │
│                              │
│ Strong Areas                 │
│ ✓ RAG fundamentals           │
│ ✓ Prompt engineering         │
│                              │
│ Needs Improvement            │
│ • Vector DB trade-offs       │
│ • Production architecture    │
│                              │
│ Recommended Next Steps       │
│ → Review retrieval strategy  │
│ → Practice system design     │
│ → Explain trade-offs aloud   │
│                              │
└──────────────────────────────┘
```

---

# 🎯 FEEDBACK THAT LEADS TO ACTION

Instead of:

> **"Score: 72%"**

InterviewOS aims to answer:

> **What did I do well?**

> **Where did I struggle?**

> **What should I learn next?**

> **What should I practice before my next interview?**

This turns the interview into a learning loop.

---

# 🔄 THE LEARNING LOOP

```text
       LEARN
         │
         ▼
       BUILD
         │
         ▼
      EXPLAIN
         │
         ▼
     INTERVIEW
         │
         ▼
      RECEIVE
      FEEDBACK
         │
         ▼
      IDENTIFY
        GAPS
         │
         ▼
       LEARN
         │
         └───────────────►
```

InterviewOS closes the gap between **building AI systems and explaining them confidently**.

---

# ✨ PRODUCT DIFFERENTIATORS

## 01 — Learning-Journey Personalization

The candidate isn't treated as a blank profile.

The interview begins with their actual cohort progress.

---

## 02 — Adaptive Conversation

Questions are influenced by previous responses.

The conversation can move deeper, simplify, challenge assumptions, or change direction.

---

## 03 — Technical Depth Over Trivia

The experience focuses on engineering reasoning.

Instead of:

> "What is RAG?"

It can explore:

> "Why did your system retrieve irrelevant chunks, and what would you change?"

---

## 04 — Feedback Becomes a Study Plan

The interview doesn't end with a score.

Weak areas become actionable preparation steps.

---

# 🛡️ REALISTIC INTERVIEW EDGE CASES

InterviewOS is designed to handle different candidate responses.

### 🟢 Strong Response

The agent can increase technical depth.

```text
Strong explanation
       ↓
Architecture question
       ↓
Trade-off question
```

### 🟡 Partial Response

The agent can probe the missing concept.

```text
Partial explanation
       ↓
Clarifying question
       ↓
Deeper verification
```

### 🔴 Weak Response

The interview can investigate fundamentals without immediately terminating the conversation.

```text
Weak explanation
       ↓
Conceptual probe
       ↓
Understanding assessment
```

### 🔁 Follow-Up Scenario

A candidate can be asked to justify a previous technical decision rather than starting an unrelated topic.

---

# 🏗️ SYSTEM ARCHITECTURE

```text
                  ┌──────────────────┐
                  │   Web Interface  │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │ Interview Session│
                  └────────┬─────────┘
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
        Curriculum      Candidate      History
           Data           Data          Context
             │             │             │
             └─────────────┼─────────────┘
                           ▼
                  ┌──────────────────┐
                  │ Interview Agent  │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │ Question Strategy│
                  └────────┬─────────┘
                           │
                           ▼
                    Candidate Answer
                           │
                           ▼
                  ┌──────────────────┐
                  │ Context + Reason │
                  └────────┬─────────┘
                           │
                           ▼
                  Adaptive Follow-Up
                           │
                           ▼
                  ┌──────────────────┐
                  │ Feedback Engine  │
                  └──────────────────┘
```

---

# 🛠️ TECHNOLOGY

The interface is built with a modern React-based frontend and designed to support an AI-driven interview workflow.

| Technology            | Role                             |
| --------------------- | -------------------------------- |
| ⚛️ React              | Application UI                   |
| 🔷 TypeScript         | Type-safe development            |
| ⚡ Vite                | Development and build tooling    |
| 🎨 Tailwind CSS       | UI styling                       |
| 🧩 shadcn/ui          | Reusable interface components    |
| 🎬 Framer Motion      | Interaction and motion           |
| ✨ Lucide React        | Interface icons                  |
| 🧠 AI Interview Logic | Adaptive questioning             |
| 📚 JSON Data          | Curriculum and candidate context |
| 💾 Client State       | Interview session state          |

---

# 📂 PROJECT ORGANIZATION

```text
VicoDathon-pb-2/
│
├── public/
│
├── src/
│   ├── components/
│   ├── pages/
│   ├── hooks/
│   ├── lib/
│   └── ...
│
├── PROMPTS.md
├── README.md
├── package.json
├── vite.config.ts
├── tsconfig.json
└── ...
```

> Project structure may evolve as the interview engine and UI are extended.

---

# 🔗 API & AGENT CONTRACT

The application is designed around the required interview endpoint specified by the challenge.

### Interview endpoint

```text
POST /api/interview
```

The endpoint is responsible for supporting the interview interaction and returning the next interview state according to the required technical specification.

The implementation follows the challenge's provided API contract rather than relying solely on a static frontend questionnaire.

---

# 🧪 REQUIREMENT CHECKLIST

The project targets the core challenge requirements:

```text
[x] Conversational technical interview

[x] Minimum 8 questions

[x] Coverage across 4+ curriculum days

[x] Adaptive follow-up questions

[x] Conversation context

[x] Structured final feedback

[x] Candidate learning journey

[x] Curriculum-aware questioning

[x] Realistic interview experience

[x] HTTP interview endpoint

[x] Responsive interface
```

---

# 📱 RESPONSIVE EXPERIENCE

Although the application is primarily an interview workspace, the interface is designed to remain usable across:

```text
📱 Mobile
   ↓
💻 Laptop
   ↓
🖥️ Desktop
```

The interview screen prioritizes:

* Readability
* Focus
* Comfortable answer input
* Clear progress
* Fast interaction
* Minimal distractions

---

# 🔐 HACKATHON SCOPE

The challenge does not require:

* Voice interaction
* Authentication
* Persistent user accounts
* Long-term conversation history
* Mobile applications

The prototype focuses on the core experience:

> **Personalized technical interviewing powered by learning context.**

---

# 📜 AI DEVELOPMENT LOG

The project was developed using AI-assisted workflows.

Detailed prompts and development instructions are documented in:

### [`PROMPTS.md`](./PROMPTS.md)

This document provides the AI usage history required for hackathon verification.

---

# 📈 DEVELOPMENT APPROACH

The product was developed iteratively around the interview experience.

### Product progression

```text
Concept
  ↓
Candidate Context
  ↓
Interview Interface
  ↓
Question Generation
  ↓
Adaptive Follow-Ups
  ↓
Context Handling
  ↓
Feedback
  ↓
UX Refinement
```

Rather than building a static question bank, development focused on creating an interview loop that can respond to the candidate.

---

# 🚀 RUN LOCALLY

### Clone

```bash
git clone https://github.com/dhanush080607/VicoDathon-pb-2.git
```

### Enter the project

```bash
cd VicoDathon-pb-2
```

### Install dependencies

```bash
npm install
```

or:

```bash
bun install
```

### Start development server

```bash
npm run dev
```

or:

```bash
bun run dev
```

### Open locally

```text
http://localhost:5173
```

---

# 🗺️ EXPERIENCE FLOW

```text
LANDING
   │
   ▼
MEET INTERVIEWOS
   │
   ▼
SELECT / LOAD CANDIDATE
   │
   ▼
START INTERVIEW
   │
   ▼
TECHNICAL QUESTION
   │
   ▼
CANDIDATE ANSWER
   │
   ▼
ADAPTIVE FOLLOW-UP
   │
   ├──── Strong → Go Deeper
   │
   ├──── Partial → Clarify
   │
   └──── Weak → Probe Fundamentals
   │
   ▼
MULTI-TOPIC INTERVIEW
   │
   ▼
FINAL ASSESSMENT
   │
   ▼
PERSONALIZED FEEDBACK
   │
   ▼
NEXT LEARNING ACTIONS
```

---

# 🏆 WHY INTERVIEWOS?

Traditional interview preparation often looks like:

```text
Question Bank
      ↓
Memorize
      ↓
Practice
      ↓
Repeat
```

InterviewOS aims for:

```text
Your Learning Journey
        ↓
Personalized Interview
        ↓
Your Answer
        ↓
AI Follow-Up
        ↓
Technical Reasoning
        ↓
Feedback
        ↓
Targeted Improvement
```

The goal isn't to help learners **memorize better answers**.

The goal is to help them **become better at explaining what they actually built**.

---

# 🔮 FUTURE ROADMAP

### Intelligence

* [ ] Deeper response evaluation
* [ ] More sophisticated interview strategies
* [ ] Difficulty adaptation
* [ ] Skill-gap detection
* [ ] Interviewer personality modes
* [ ] System-design interview mode

### Learning

* [ ] Personalized revision plans
* [ ] Weak-topic recommendations
* [ ] Interview replay
* [ ] Progress analytics
* [ ] Skill confidence tracking

### Platform

* [ ] Authentication
* [ ] Persistent interview history
* [ ] Candidate profiles
* [ ] Cohort analytics
* [ ] Interview benchmarking
* [ ] Mentor dashboard

### Advanced

* [ ] Voice interviews
* [ ] Real-time speech analysis
* [ ] Code interview environment
* [ ] Collaborative mock interviews
* [ ] Recruiter-ready interview reports

---

# 👨‍💻 BUILT BY

## H Dhanush

**CSE — Data Science**

Frontend Developer • UI Designer • AI/ML Enthusiast

[LinkedIn](https://www.linkedin.com/in/h-dhanush-189565327/)

---

# ⚡ THE FINAL IDEA

A learner can build an impressive AI system.

But if they cannot explain:

> **Why this architecture?**

> **Why this model?**

> **Why this retrieval strategy?**

> **What happens when it fails?**

> **How would you scale it?**

Then the learning journey isn't complete.

### InterviewOS turns the question:

> **"What did you learn?"**

into:

# **"Can you defend what you built?"**

**Learn → Build → Explain → Interview → Improve.**

---

## 🎙️ InterviewOS

### **Your learning journey. Your technical story. Your next interview.**

**Built for the VicoDathon Hackathon.**
