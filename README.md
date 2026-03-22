# 🚑 Real-Time AI Emergency Triage System

## Overview

This project is built for one purpose: **help medical teams make fast, critical decisions in chaotic situations**.

Unlike typical health apps, this system doesn’t try to be “smart” in a general sense. It focuses on **speed, clarity, and extracting only what matters** — especially when input is messy, incomplete, or coming from distressed patients.

The goal is simple:

> **Turn noisy input into clear, actionable decisions in under 30 seconds (ideally under 2 seconds).**

---

## 💡 What Makes This Different

Most AI systems:

* Take full input
* Generate long explanations
* Aim for completeness

This system:

* **Cuts noise aggressively**
* **Extracts only critical signals**
* **Prioritizes life-threatening conditions**
* **Responds with immediate actions, not essays**

---

## 🚀 Core Features

### 1. Multi-Input Handling

Supports:

* Voice input (distressed, broken speech)
* Text input
* Optional structured data (age, vitals)

The system is designed to work even when:

* Sentences are incomplete
* Information is missing
* Input is chaotic

---

### 2. Intelligent Context Pruning (Core Logic)

Instead of sending everything to AI, the system:

* Filters irrelevant details
* Extracts only:

  * Symptoms
  * Duration
  * Severity indicators
  * Risk factors

This keeps responses:

* Faster
* More accurate for emergencies
* Less hallucination-prone

---

### 3. Emergency Severity Engine

Each case is classified into:

* 🟢 **Non-Urgent**
* 🟡 **Urgent**
* 🔴 **Critical**

Classification is based on:

* Symptom combinations
* Known emergency triggers
  (e.g., chest pain + sweating → high risk)

---

### 4. Protocol Matching System

The system maps extracted data to predefined medical protocols stored in a database.

Output includes:

* Likely condition
* Immediate action steps (clear and practical)

No vague advice. No long explanations.

---

### 5. Real-Time Performance

Target response time:

> **< 2 seconds**

Achieved using:

* Rule-based shortcuts for common emergencies
* Pre-processed logic before AI calls
* Minimal payload sent to the model

---

## 🧠 Smart Add-ons

### ✅ Explainability Layer

Shows *why* a case is flagged:

Example:

> Chest pain + shortness of breath → Possible cardiac event

---

### ✅ Doctor Mode vs Public Mode

**Doctor Mode**

* Detailed reasoning
* Full extracted signals

**Public Mode**

* Simple instructions
* Clear next steps

---

### ✅ Fail-Safe Logic

If confidence is low:

> “Seek immediate medical attention”

No guessing. No risky assumptions.

---

### ✅ Offline Backup

If AI fails:

* Falls back to rule-based triage
* Handles common emergencies reliably

---

## 🛠 Tech Stack

* **Frontend:** React (fast, minimal UI)
* **Backend:** Node.js + Express
* **AI:** OpenAI API (structured prompting)
* **Speech:** Whisper / Web Speech API
* **Database:** MongoDB (protocols + logs)

---

## ⚠️ Design Principles

* Works with incomplete input
* Prioritizes **speed over perfection**
* Avoids long responses
* Focuses on **decision support, not diagnosis replacement**

---

## 🧪 Example Flow

**Input (messy):**

> “uh chest pain… like heavy… sweating… since 10 mins…”

**System Output:**

* Severity: 🔴 Critical
* Possible Condition: Cardiac event
* Action: Call emergency services immediately

## ▶️ Demo & Reproducibility

### 🔧 Setup Instructions

Follow these steps to run the project locally:

```bash
# 1. Clone the repository
git clone https://github.com/your-username/your-repo-name.git

# 2. Navigate into the project
cd GenAi-main

# 3. Install dependencies
npm install

# 4. Start the development server
npm run dev
```

Open in browser:

```
http://localhost:5173
```

---

### ⚠️ Environment Variables (if using Supabase)

Create a `.env` file in root:

```
VITE_SUPABASE_URL=your_url_here
VITE_SUPABASE_ANON_KEY=your_key_here
```

---

### 🎯 Example Demo Case

**Input (voice/text):**

```
"chest pain... sweating... breathing heavy... 10 minutes"
```

**System Output:**

```
Severity: 🔴 Critical  
Condition: Possible cardiac event  
Action: Call emergency services immediately  
Reason: Chest pain + sweating + shortness of breath
```

---

### ⚡ Performance

* Average response time: < 2 seconds
* Handles incomplete / noisy input
* Uses context pruning before AI call

---

### 🧪 Test Scenarios

Try these:

1. **Stroke-like symptoms**

```
"can't move left side... slurred speech"
```

2. **Low priority case**

```
"mild headache since morning"
```

3. **Accident case**

```
"bleeding heavily from leg after fall"
```

---

### 🧯 Fail-safe Behavior

If system confidence is low:

```
"Seek immediate medical attention"
```

---

### 📴 Offline Mode

If AI/API fails:

* Rule-based triage still works
* Covers common emergency patterns

---

### 📌 Notes

* Designed for emergency triage, not diagnosis
* Optimized for speed over completeness
* Works even with broken or incomplete input


Thank You 

