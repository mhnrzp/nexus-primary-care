# HOS — agentic AI operating system for NHS primary care (prototype)

HOS is a prototype for a unified, AI-native healthcare platform for the NHS. This repo
focuses on the **primary care (GP)** experience — from the front-desk phone call to the
consulting room.

🔗 **Live demo:** https://hos-nhs.vercel.app

> ⚠️ **Prototype for discussion only.** Not connected to any live clinical system and not for
> clinical use. All patient data is fictional. A core design principle throughout is that
> **every consequential AI action requires human sign-off before execution.**

## What's here

Each file is a self-contained single-page app (React + Tailwind via CDN, no build step).
Just open it in a browser.

| File | What it is |
|------|------------|
| **`index.html`** | **Front Desk** — a live-call switchboard. The AI voice agent handles multiple patient calls at once; staff listen in on a live transcript, see captured data (name, MRN, DOB, symptoms, urgency), and approve / edit / reject the bookings it proposes in a separate "Needs staff action" queue. Includes urgency tiering (Routine / Soon / Urgent / Emergency), red-flag emergency handling (999, no booking, pinned to top), call-back for missed urgent calls, an overnight **Morning Review**, and a weekly calendar of accepted bookings. |
| **`gp.html`** | **GP Workspace** — dashboard (search + today's clinic), full patient record (Summary, Encounters, Medical History, Medications, Allergies, Problems, Orders, Results, Documents), a clinical encounter flow (Chief Complaint → HPI → Review of Systems → Examination → Assessment → Plan → Orders → Results & Follow-up) with an AI scribe and an ordering copilot, plus an Appointments calendar, Messages, Reports and Admin. |

A profile switcher in each sidebar moves between the two panels.

## Running

No install needed — open the live demo above, or open `index.html` / `gp.html` directly in a
modern browser (internet connection required for the React / Tailwind CDNs).

## Concept

- **Front door to consulting room on one platform** — the front-desk AI's triage flows into
  the clinician's record, so patients arrive part-documented.
- **Two operating modes** — in hours the AI works alongside reception; out of hours it handles
  calls solo, routes emergencies to 999, and queues everything else for the morning review.
- **Urgency tiering** drives booking and routing (Routine · Soon · Urgent · Emergency).
- **Human-in-the-loop safety** — the AI drafts and recommends; clinicians and staff approve.
  No autonomous bookings, no AI diagnosis, no admin editing clinical urgency.

## Status

Early UI/UX prototype for product exploration. Built with Claude Code.
