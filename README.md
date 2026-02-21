# Aegis: Adaptive Emergency Triage and Dispatch Interface

Aegis is a cognitive decision-support interface that analyzes emergency call transcripts in real time, extracts critical biomarkers, and recommends optimal responder deployment while providing pre-arrival preparation guidance to first responders.

The system reduces cognitive load, accelerates dispatch decisions, and improves responder readiness through adaptive human-computer interaction.

---

## Overview

Emergency response is a time-critical process where seconds can determine outcomes. Dispatchers and responders must rapidly interpret incomplete, chaotic information and make high-stakes decisions under preshoiwsure.

Aegis augments emergency response workflows by transforming raw emergency call transcripts into structured, actionable intelligence, enabling responders to prepare effectively and ensuring optimal unit deployment based on severity, proximity, and required skill level.

Instead of static dispatch interfaces, Aegis dynamically adapts information presentation based on incident urgency, prioritizing critical signals and reducing cognitive overhead.

---

## Key Features

### Real-Time Transcript Intelligence Extraction

Aegis processes emergency call transcripts and extracts structured incident intelligence, including:

* Emergency type classification
* Severity assessment
* Biomarker and symptom detection
* Confidence scoring and rationale

This enables rapid situational awareness without requiring manual interpretation.

---

### Pre-Arrival Preparation Guidance

Aegis proactively prepares responders before they arrive on scene by recommending:

* Required medical equipment
* Suggested intervention protocols
* Scene risk considerations

This reduces preparation time and improves response effectiveness.

Example output:

```
Emergency: Cardiac Arrest  
Severity: CRITICAL  

Prepare immediately:
• Defibrillator
• Oxygen kit
• Airway equipment

Suggested protocol:
• Assess airway, breathing, circulation
• Begin CPR if indicated
```

---

### Intelligent Responder Deployment Optimization

Aegis evaluates available responder units based on:

* Distance from incident
* Skill level and certification (EMT, paramedic, advanced life support)
* Incident severity and required capabilities

The system recommends optimal responder deployment to maximize survival probability and response efficiency.

---

### Adaptive Command Interface (Human-Computer Interaction Innovation)

Aegis dynamically adjusts interface complexity based on incident severity and responder needs.

Critical incidents surface prioritized preparation guidance and deployment recommendations, while lower-priority incidents present simplified views.

This adaptive interface reduces cognitive load and improves decision clarity during high-stress scenarios.

---

### Interactive Map Visualization

Aegis provides a real-time visual map displaying:

* Incident location
* Nearby responder units
* Recommended deployment selections

This improves situational awareness and dispatch transparency.

---

## System Architecture

```
Emergency Call Transcript
          ↓
AI Triage Engine (Biomarker Extraction + Severity Assessment)
          ↓
Deployment Optimization Engine
          ↓
Adaptive Command Interface
          ↓
Responder Preparation Guidance + Deployment Recommendations
```

---

## Tech Stack

### Frontend

* Next.js (App Router)
* TypeScript
* Tailwind CSS
* Mapbox GL JS (or Google Maps API)

### Backend

* Next.js API Routes
* Claude API (Anthropic) for structured triage intelligence extraction

### Data

* Simulated responder location dataset
* Real-time incident intelligence generation

---

## Repository Structure

```
aegis/
├── app/
│   ├── page.tsx                # Main dashboard interface
│   └── api/
│       ├── triage/route.ts    # Transcript analysis endpoint
│       └── deploy/route.ts    # Deployment recommendation endpoint
│
├── components/
│   ├── Dashboard/             # Command interface panels
│   └── Map/                   # Map visualization components
│
├── lib/
│   ├── triage/                # Transcript analysis logic
│   ├── deploy/                # Unit selection and scoring logic
│   └── data/                  # Simulated responder datasets
│
├── types/                     # TypeScript data models
└── README.md
```

---

## Getting Started

### Prerequisites

* Node.js 18+
* npm or yarn
* Claude API key (Anthropic)

---

### Installation

Clone the repository:

```
git clone https://github.com/your-username/aegis.git
cd aegis
```

Install dependencies:

```
npm install
```

Create environment file:

```
.env.local
```

Add:

```
ANTHROPIC_API_KEY=your_api_key_here
MAPBOX_ACCESS_TOKEN=your_mapbox_token_here
```

Run development server:

```
npm run dev
```

Open:

```
http://localhost:3000
```

---

## Example Workflow

1. Input emergency call transcript:

```
"My father collapsed and isn't breathing."
```

2. Aegis extracts incident intelligence:

* Cardiac arrest detected
* Severity: CRITICAL
* Biomarkers: unconscious, not breathing

3. Aegis recommends:

* Prepare defibrillator and airway equipment
* Dispatch paramedic-level EMS unit
* Shows recommended unit on map

4. Responders arrive better prepared and informed.

---

## Motivation

Emergency dispatch systems today rely heavily on manual interpretation and static interfaces. This introduces delays, cognitive overload, and inconsistent decision-making.

Aegis demonstrates a new paradigm in human-computer interaction: adaptive, intelligent interfaces that dynamically prioritize information and support decision-making in high-stakes environments.

This approach has the potential to improve emergency response efficiency, responder preparedness, and ultimately, patient outcomes.

---

## Inspiration

Inspired by early dispatch automation research and prototypes such as TriageAI, which explored automated triage extraction and dispatch assistance.

Aegis extends this concept into a real-time adaptive command interface focused on responder preparation, deployment optimization, and cognitive workload reduction.

---

## Disclaimer

Aegis is a research prototype created for demonstration and hackathon purposes.

It is not intended for real-world emergency deployment or medical decision-making.

All outputs should be treated as decision-support suggestions requiring human verification.

---

## Future Work

* Real-time speech-to-text integration
* Live responder tracking integration
* Hospital availability and routing optimization
* Multi-incident resource allocation
* Mobile responder interface

---

## Authors

Built by: Steven Ngo, Howard Lin, Elliott Yaroslavsky, Aarav Trivedi

---

## Demo

Coming soon.

