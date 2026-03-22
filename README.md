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

---
## 🚧 Future Improvements

* Integration with hospital systems
* Real-time vital monitoring
* Edge deployment for offline disaster zones

---

## Disclaimer

This system is designed to **assist**, not replace, medical professionals.
Always rely on trained healthcare providers for final decisions.

---

## Final Note

This isn’t about building a “cool AI app.”

It’s about building something that:

> **Works under pressure, with bad input, and still gives the right signal fast.**
