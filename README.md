# NEXUS — AI healthcare platform (prototype)

NEXUS is a prototype for a unified healthcare platform spanning primary, secondary, and
tertiary care. These prototypes focus on the **primary care (GP)** experience.

> ⚠️ **Prototype for discussion only.** Not connected to any live clinical system and not for
> clinical use. All patient data is fictional. A core design principle throughout is that
> **every consequential AI action requires human sign-off before execution.**

## What's here

Each file is a self-contained single-page app (React + Tailwind via CDN, no build step).
Just open it in a browser.

| File | What it is |
|------|------------|
| **`index.html`** | **Front desk** — a live-call switchboard. The AI voice agent handles multiple patient calls at once; staff listen in on a live transcript, see captured data (name, MRN, DOB, symptoms, urgency), and approve/edit/reject the bookings it proposes in a separate "Needs staff action" queue. Includes urgency tiering (Routine / Soon / Urgent / Emergency), red-flag emergency handling (999, no booking), notifications, call-back for missed urgent calls, and a weekly calendar. |
| **`gp.html`** | **GP / clinician app** — dashboard (search + today's clinic), full patient record (Summary, Encounters, Medical History, Medications, Allergies, Problems, Orders, Results, Documents), a clinical encounter flow (Chief Complaint → HPI → ROS → Examination → Assessment → Plan → Orders → Results & Follow-up) with an AI scribe and an ordering copilot, plus Appointments calendar, Messages, Reports and Admin. |
| **`nexus.html`** | **Full platform demo** — role-based views (GP, nurse, receptionist, practice manager), call handling, urgency engine, the unified approval queue, patient/clinical modules, AI admin agents (scheduling, comms, referral, rostering), and an audit log. |

## Running

No install needed — open any of the `.html` files directly in a modern browser
(internet connection required for the React/Tailwind CDNs).

## Concept

- **Front door to consulting room on one platform** — the front-desk AI's triage flows into
  the clinician's record, so patients arrive part-documented.
- **Urgency tiering** drives booking and routing (Routine, Soon, Urgent, Emergency).
- **Human-in-the-loop safety** — the AI drafts and recommends; clinicians and staff approve.
  No autonomous bookings, no AI diagnosis, no admin editing clinical urgency.

## Status

Early UI/UX prototypes for product exploration. Built with Claude Code.
