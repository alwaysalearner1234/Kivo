# KIVO — Train. Progress. Become.


Demo video : https://www.youtube.com/watch?v=icUHj963zWY

> **An AI-powered athletic development platform for kids ages 5–16.**

KIVO turns physical activity into a measurable, personalized progression system.

Instead of comparing children against one another, KIVO helps each child understand their own development through **challenges, performance data, progression, gamification, and AI-powered coaching**.

**Train → Measure → Improve → Progress.**

---

## 🚀 What is KIVO?

KIVO is the **digital intelligence layer** of a larger physical-digital athletic ecosystem.

The platform connects:

**Child Activities → Performance Data → Scoring → AI Analysis → Personalized Training → Progress**

The current hackathon build focuses on the software intelligence layer. Future KIVO hardware products can feed physical performance data directly into the same system.

---

## 🎯 The Problem

Children's fitness experiences often fall into two categories:

* **Passive products** — fun to use, but provide little meaningful measurement.
* **Adult-focused fitness platforms** — designed around metrics and comparisons that aren't appropriate for younger athletes.

This creates a gap.

Parents need a simple way to understand development.

Children need feedback that makes improvement visible and motivating.

KIVO addresses that gap with a **personal-progress-first athletic development system**.

---

## 💡 The KIVO Approach

KIVO measures development across four areas:

| Area            | Focus                                       |
| --------------- | ------------------------------------------- |
| 💪 **STRONGER** | Grip, power, body control                   |
| 🌀 **FITTER**   | Stamina, endurance, coordination            |
| ⚡ **FASTER**    | Speed, agility, reaction                    |
| 🎯 **CHAMPS**   | Challenges, goals, consistency, progression |

### The core philosophy

> **A child's biggest competition is their own previous performance.**

KIVO focuses on **personal improvement**, rather than ranking children against each other.

---

# ✨ Key Features

### 🏠 Child-First Experience

* Premium animated onboarding
* One-click Demo Mode
* Pre-populated demo athlete
* Responsive mobile-first interface
* Keyboard navigation
* Reduced-motion support

### 👪 Profiles & Roles

* Parent
* Child
* Coach
* Child profiles
* Athlete performance history

### 📋 Athletic Assessment

A four-test baseline assessment establishes an initial performance profile.

Results are transformed into measurable development areas that power future recommendations.

### 🌀 Rope Rush

A jump-rope challenge featuring:

* Tap-based jump counter
* 20 / 30 / 60 second rounds
* Consistency tracking
* Pause and resume
* Performance measurement

### ⚡ Reaction Rush

A reaction challenge using four interactive pods.

Measures:

* Reaction time
* Accuracy
* Successful responses
* Performance progression

Keyboard controls are supported for desktop testing.

### 🎯 Agility Command

A sequence-based agility challenge that progressively increases difficulty.

Tracks:

* Completion time
* Errors
* Sequence performance
* Personal records

### 🎉 Results & Progression

Every completed challenge produces a personalized results experience containing:

* Animated performance score
* Personal-best detection
* XP earned
* Progress information
* Next-step recommendations
* Performance insights

### 🏅 Gamification

KIVO includes:

* XP
* Levels
* Streaks
* Personal records
* 7 achievement badges
* Level-up celebrations
* Challenge progression

### 🤖 AI Coach

The AI Coach transforms performance data into child-friendly coaching.

It can provide:

* Encouragement
* Strongest area
* Area to focus on
* Recommended next challenge
* Difficulty recommendation
* Personalized workout plan

The coaching system is designed around **encouragement and progression**, not medical advice.

### 📋 Today's Plan

KIVO automatically generates an adaptive training plan based on the athlete's current performance.

The plan prioritizes areas that need additional development while maintaining progression across the athlete's broader profile.

### 📈 Progress Analytics

The platform provides:

* Performance history
* Personal records
* Challenge history
* Progress charts
* Filters
* Outcome scores
* Weekly parent insights

### 👨‍👩‍👧 Parent Dashboard

Parents can see development through simple, non-technical insights rather than raw performance data alone.

---

# 🧠 How KIVO Works

```text
                    CHILD
                      │
                      ▼
              ┌───────────────┐
              │   Challenge   │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ Raw Metrics   │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ Scoring Engine│
              └───────┬───────┘
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
      Personal      XP &        Outcome
       Best        Badges        Scores
          │           │           │
          └───────────┼───────────┘
                      ▼
                AI Coach
                      │
                      ▼
             Personalized Plan
                      │
                      ▼
                 Next Challenge
                      │
                      └──────────► PROGRESS
```

---

# ⚙️ Technical Architecture

```text
┌──────────────────────────────────────────┐
│                 FRONTEND                 │
│                                          │
│ React + TypeScript + Tailwind + Vite    │
│ Framer Motion + Recharts + React Router  │
└────────────────────┬─────────────────────┘
                     │
                     ▼
┌──────────────────────────────────────────┐
│                  API                     │
│                                          │
│       Node.js + Express + TypeScript     │
└──────────────┬───────────────┬───────────┘
               │               │
               ▼               ▼
      ┌────────────────┐  ┌────────────────┐
      │ Scoring Engine  │  │   AI Services  │
      │                │  │                │
      │ Normalize      │  │ Coach          │
      │ Improvement    │  │ Workout        │
      │ Personal Best  │  │ Validation     │
      │ XP             │  │ Fallback       │
      └────────────────┘  └───────┬────────┘
                                  │
                                  ▼
                         OpenAI-Compatible API
                                  │
                                  ▼
                         Deterministic Fallback

              Optional
                  │
                  ▼
        ┌──────────────────┐
        │ Supabase Postgres│
        └──────────────────┘

              Future
                  │
                  ▼
        ┌──────────────────┐
        │ ESP32 KIVO Pods   │
        └──────────────────┘
```

---

# 🛠️ Tech Stack

### Frontend

* React 18
* TypeScript
* Vite 5
* Tailwind CSS
* React Router 6
* Framer Motion
* Lucide
* Recharts

### Backend

* Node.js
* Express 4
* TypeScript
* Vitest

### Database

* Supabase PostgreSQL
* Seeded in-memory store for development/demo mode

### AI

* OpenAI-compatible chat API
* Structured AI responses
* Deterministic fallback when no API key is configured
* Response validation
* Coaching-focused prompt system

---

# 📁 Project Structure

```text
kivo/
├── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── ...
│
├── backend/
│   └── src/
│       ├── services/
│       │   ├── ai/
│       │   └── ...
│       └── ...
│
├── hardware/
│   └── react-pod/
│       └── ESP32/
│
├── docs/
│   └── screenshots/
│
├── .env.example
├── package.json
└── README.md
```

---

# 🚀 Getting Started

## Requirements

* Node.js 18+
* npm
* Git

No physical KIVO hardware is required to run the software demo.

---

## Installation

Clone the repository:

```bash
git clone <YOUR-REPOSITORY-URL>
cd kivo
```

Install the project dependencies:

```bash
npm run setup
```

---

## Environment Configuration

KIVO works in demo mode without external services.

For optional AI/database functionality:

```bash
cp .env.example backend/.env
```

Then configure the appropriate variables:

```env
OPENAI_API_KEY=
OPENAI_BASE_URL=
OPENAI_MODEL=

SUPABASE_URL=
SUPABASE_ANON_KEY=
```

The frontend API URL can be configured with:

```env
VITE_API_URL=http://localhost:5000/api
```

---

# ▶️ Run KIVO

Run frontend and backend together:

```bash
npm run dev
```

Or run them separately:

```bash
npm run dev:backend
```

```bash
npm run dev:frontend
```

Then open:

```text
http://localhost:5173
```

---

# 🧪 Recommended Demo Flow

For the quickest demonstration:

```text
1. Launch KIVO
       ↓
2. Continue as Demo
       ↓
3. Open an athletic challenge
       ↓
4. Complete Reaction Rush
       ↓
5. View Results
       ↓
6. Open AI Coach
       ↓
7. View Today's Plan
       ↓
8. Open Progress
       ↓
9. View Achievements
       ↓
10. Return to Dashboard
```

The complete judge journey is designed to take approximately **4 minutes**.

### Demo account

```text
Email:    demo@kivo.app
Password: demo1234
```

---

# 🧮 Scoring System

KIVO uses a centralized scoring pipeline.

```text
Raw Performance
       ↓
Normalization
       ↓
Personal Improvement
       ↓
Personal Best Detection
       ↓
XP Calculation
       ↓
Badge / Streak Updates
       ↓
Outcome Score
       ↓
AI Coaching Context
```

The system is designed so new physical challenges can use the same progression architecture.

---

# 🤖 AI Coach

The AI layer exposes structured endpoints such as:

```text
POST /api/ai/coach
POST /api/ai/workout
```

Example response:

```json
{
  "encouragement": "Great work today!",
  "strongestArea": "faster",
  "weakestArea": "champs",
  "recommendation": "Keep building consistency.",
  "nextChallenge": "agility-command",
  "difficulty": "Level 3",
  "workout": []
}
```

AI responses are validated before reaching the UI.

The system also includes a deterministic fallback, meaning the core experience can still operate when a live AI provider is unavailable.

---

# 🔌 Hardware Integration

KIVO is designed to eventually connect physical products to the digital platform.

The repository currently includes:

```text
hardware/react-pod/
```

The prototype uses:

* ESP32
* LED reaction pods
* Buttons
* Wi-Fi communication

The planned hardware flow is:

```text
Physical Pod
     ↓
ESP32
     ↓
Wi-Fi
     ↓
POST /api/hardware/tap
     ↓
KIVO Scoring Engine
     ↓
Performance Profile
     ↓
AI Coach
```

Hardware is therefore treated as another source of measurable performance data rather than a separate system.

---

# 🔐 Safety & Privacy Principles

KIVO is designed specifically for children.

Core principles include:

* Personal-progress-focused scoring
* No child-versus-child leaderboard required for progression
* Parent-oriented insights
* Coaching rather than medical diagnosis
* No medical claims from the AI Coach
* Structured AI responses
* Validated AI output
* Child-friendly feedback

> KIVO is an athletic development and coaching platform, not a medical diagnostic system.

---

# 📱 Responsive Experience

KIVO is designed to work across:

* 📱 Mobile
* 💻 Desktop
* 🖥️ Larger displays

Accessibility considerations include:

* Keyboard navigation
* Reduced-motion support
* Clear interaction states
* Loading states
* Error states
* Retry states

---

# 📊 Testing & Build

Build the application:

```bash
npm run build
```

Run tests:

```bash
npm test
```

The backend includes automated tests for the scoring system and core progression logic.

---

# 🖼️ Screenshots

Screenshots will be added here:

```text
docs/screenshots/
├── dashboard.png
├── assessment.png
├── reaction-rush.png
├── results.png
├── ai-coach.png
└── progress.png
```

---

# 🎥 Demo

**Demo video:**
*Add demo video link here.*

Suggested walkthrough:

```text
Splash
  ↓
Demo Mode
  ↓
Athlete Dashboard
  ↓
Challenge
  ↓
Results
  ↓
AI Coach
  ↓
Today's Plan
  ↓
Progress
  ↓
Achievements
```

---

# 🌱 Future Development

### Platform

* Real parent/child authentication
* Supabase Auth
* Row Level Security
* Persistent athlete profiles
* Coach and school dashboards

### Challenges

* Hang test
* Shuttle run
* Balance assessment
* Jump tests
* More reaction challenges
* Expanded athletic assessments

### Hardware

* ESP32 pod pairing
* Automatic challenge detection
* Physical KIVO product integration
* Real-time performance ingestion

### Intelligence

* More adaptive training plans
* Long-term progression modeling
* Athlete development timelines
* Personalized challenge difficulty
* Expanded AI coaching

### Accessibility & Scale

* Offline-first PWA
* Internationalization
* Additional accessibility features
* Multi-school support
* Multi-coach programs

---

# 🏆 Why KIVO?

KIVO connects the physical and digital sides of athletic development.

```text
PHYSICAL ACTIVITY
       ↓
MEASUREMENT
       ↓
PERFORMANCE DATA
       ↓
PERSONAL PROGRESSION
       ↓
AI COACHING
       ↓
PERSONALIZED TRAINING
       ↓
BETTER NEXT SESSION
```

The goal isn't simply to give children another game.

It's to create a system where every challenge produces information, every result creates a next step, and every session contributes to a clearer picture of personal progress.

---

# 👥 Team

**KIVO Hackathon Team**

Digital intelligence system track.

---

## 📄 License

Add the project's applicable license here.

Example:

```text
MIT License
```

If this repository is based on or incorporates third-party code, retain the original licenses and attribution required by those projects.
