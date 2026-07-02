# 5. User Stories

[← Personas](04-personas.md) · [Home](../README.md) · Next: [Functional Requirements →](06-functional-requirements.md)

Stories are grouped by epic and prioritized **P0** (MVP), **P1**, **P2**. Each has acceptance
criteria (AC). Personas referenced from [Personas](04-personas.md).

## Epic A — Guided intake

### A1 (P0) — Describe my situation in plain language
*As a patient, I want to enter my condition in my own words so that I don't need medical terminology.*
- **AC:** Free-text condition input maps to standardized concept(s) with a confirm step.
- **AC:** If the term is ambiguous, the user is shown disambiguation options.
- **AC:** User can add location and a few key details (age, sex, key prior treatments) optionally.

### A2 (P0) — Search for someone else
*As a caregiver, I want to indicate I'm searching for another person so the questions make sense.*
- **AC:** A "for someone else" mode adjusts pronouns/wording and does not assume it's the user.

## Epic B — Results & ranking

### B1 (P0) — Get a ranked, relevant shortlist
*As a patient, I want the most relevant trials first so I'm not overwhelmed.*
- **AC:** Results ranked by relevance (condition, location, recruiting status, likely eligibility).
- **AC:** Default view shows a manageable set (e.g., top 20) with clear "load more."
- **AC:** Only **recruiting / not-yet-recruiting** trials shown by default; can toggle others.

### B2 (P0) — Understand each study in plain language
*As a patient, I want a plain-language summary so I know what a study is about.*
- **AC:** Each result shows a plain-language title/summary, phase, location(s), and distance.
- **AC:** Source and last-updated date are visible for trust.

### B3 (P0) — See a personalized eligibility snapshot
*As a patient, I want to know if I might qualify so I don't chase dead ends.*
- **AC:** Each study shows a status: **may qualify / needs review / likely not a match**.
- **AC:** The snapshot lists the top reasons, in plain language.
- **AC:** Copy always states this is not a final determination. See [Compliance](11-compliance-privacy-security.md).

### B4 (P1) — Filter and sort
*As a referring clinician, I want to filter by phase, distance, and status.*
- **AC:** Filters for phase, distance/radius, recruiting status, intervention type.

## Epic C — Save, compare, connect

### C1 (P0) — Save studies
*As a caregiver, I want to save studies so I can revisit and compare them.*
- **AC:** Saved list persists for signed-in users; guests can save for the session.

### C2 (P1) — Compare studies side by side
*As a caregiver, I want to compare saved studies so I can bring a shortlist to the care team.*
- **AC:** Side-by-side view of key attributes for 2–4 studies.

### C3 (P0) — Connect with the study team
*As a patient, I want a clear way to contact a study so I can take the next step.*
- **AC:** Each study exposes the registered contact and/or a guided outreach template.
- **AC:** A "questions to ask" checklist is offered.

## Epic D — Accounts & alerts

### D1 (P1) — Save a search and get alerts
*As a patient, I want to be notified when new matching trials appear.*
- **AC:** Signed-in users can save a search and opt into email/push alerts for new matches.

### D2 (P1) — Manage my data
*As a user, I want to view and delete my data so I stay in control.*
- **AC:** Users can export and delete their profile/search data. See [Compliance](11-compliance-privacy-security.md).

## Epic E — Coordinator hand-off (P2, later phase)

### E1 (P2) — Receive a structured prospect
*As a coordinator, I want interested prospects delivered with structured context.*
- **AC:** Opt-in structured referral payload delivered to the site's chosen channel.

## Prioritization summary

| Epic | P0 | P1 | P2 |
|------|----|----|----|
| A Intake | A1, A2 | | |
| B Results | B1, B2, B3 | B4 | |
| C Save/Connect | C1, C3 | C2 | |
| D Accounts | | D1, D2 | |
| E Coordinator | | | E1 |

---

[← Personas](04-personas.md) · [Home](../README.md) · Next: [Functional Requirements →](06-functional-requirements.md)
