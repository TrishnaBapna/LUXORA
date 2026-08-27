# LUXORA — Intelligent Guest Service & Staff Coordination Platform

**PS Number:** PU PS 4 · **Theme:** Hospitality · **Organization:** IH

A smart hotel service platform that understands guest requests, categorizes and
prioritizes them, assigns them to the right department and staff member,
tracks SLA deadlines, and gives guests, staff, and supervisors real-time
visibility — with room/location-aware requests, food ordering, an AI chat
assistant, and emergency handling built in.

## Current status

`index.html` is a **working front-end prototype** — a single self-contained
file (HTML/CSS/JS, no build step, no dependencies). Open it directly in any
browser to demo the full flow: guest/staff/supervisor login, tap-to-request,
food ordering with cart, live SLA countdowns, supervisor task reassignment,
and emergency escalation.

**It has no backend or database yet** — all data lives in browser memory and
resets on refresh. That's the next milestone (see Roadmap below).

## Demo logins

| Role | Email | Password |
|---|---|---|
| Guest | guest@luxora.com | guest123 |
| Staff (Maintenance) | priya@luxora.com | staff123 |
| Staff (Transportation) | arjun@luxora.com | staff123 |
| Staff (Concierge) | neha@luxora.com | staff123 |
| Supervisor | admin@luxora.com | super123 |

Or use "Sign in as demo [role]" on the login screen.

## Tech stack (target)

| Layer | Technology |
|---|---|
| Frontend | React |
| Backend | FastAPI |
| Intelligence | Python ML/NLP pipeline |
| Database | MySQL (main) / SQLite (local dev) |

## Roadmap

- [x] Front-end prototype (this file) — all screens, flows, and logic working client-side
- [ ] `schema.sql` — MySQL schema (users, guests, staff, departments, requests, request_assignments, notifications, feedback)
- [ ] FastAPI backend — `/api/auth`, `/api/requests`, `/api/staff`, `/api/analytics`, etc.
- [ ] Replace in-memory JS state with real API calls
- [ ] Trained ML classifier to replace the current keyword-based classifier
- [ ] Real-time push notifications for staff/supervisor (esp. emergencies)

## Project structure (planned, once backend is added)

```
LUXORA/
├── frontend/         # React app (will replace index.html)
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── api/
│   │   ├── models/
│   │   ├── schemas/
│   │   ├── services/
│   │   └── ml/
│   └── requirements.txt
├── database/
│   └── schema.sql
├── index.html        # current standalone prototype (kept for demo purposes)
└── README.md
```
