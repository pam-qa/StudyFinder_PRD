# 6. Functional Requirements

[← User Stories](05-user-stories.md) · [Home](../README.md) · Next: [Non-Functional Requirements →](07-non-functional-requirements.md)

Requirements use **MUST / SHOULD / MAY** ([RFC 2119](https://www.rfc-editor.org/rfc/rfc2119)) and are
IDed `FR-#`. They trace back to [User Stories](05-user-stories.md).

## 6.1 Intake

- **FR-1 (MUST)** Accept a free-text condition and map it to standardized concept(s) (e.g., a medical
  ontology), with a user confirmation step.
- **FR-2 (MUST)** Support optional structured inputs: location, age, sex, and a small set of
  high-signal clinical details relevant to filtering.
- **FR-3 (MUST)** Support a "searching for someone else" mode.
- **FR-4 (SHOULD)** Allow progressive disclosure — return results with minimal input, refine as the
  user answers more.
- **FR-5 (MUST)** Never require an account to run a search.

## 6.2 Search & ranking

- **FR-6 (MUST)** Query the [ClinicalTrials.gov v2 API](10-integrations.md) as the primary source.
- **FR-7 (MUST)** Rank results by a composite of condition relevance, location proximity, recruiting
  status, and estimated eligibility fit.
- **FR-8 (MUST)** Default to **recruiting** and **not-yet-recruiting** studies; allow toggling others.
- **FR-9 (SHOULD)** Provide filters: phase, distance/radius, status, intervention type, age/sex applicability.
- **FR-10 (SHOULD)** De-duplicate and cluster studies that appear across sources.

## 6.3 Study comprehension

- **FR-11 (MUST)** Generate a plain-language summary for each study (purpose, what participation involves).
- **FR-12 (MUST)** Display phase, sponsor, locations, distance, status, and source last-updated date.
- **FR-13 (MUST)** Preserve a link to the authoritative source record.
- **FR-14 (SHOULD)** Offer definitions/tooltips for medical terms ([Glossary](14-glossary.md)).
- **FR-15 (SHOULD)** Support multilingual summaries. See [NFRs](07-non-functional-requirements.md).

## 6.4 Eligibility snapshot

- **FR-16 (MUST)** Produce a per-study eligibility status: **may qualify / needs review / likely not a match**.
- **FR-17 (MUST)** Explain the top contributing factors in plain language.
- **FR-18 (MUST)** Clearly label all eligibility output as non-final and not medical advice.
- **FR-19 (SHOULD)** Let users answer targeted follow-up questions to sharpen the snapshot.
- **FR-20 (MUST NOT)** Present eligibility as a guarantee or as a clinical determination.

## 6.5 Save, compare, connect

- **FR-21 (MUST)** Allow saving studies (session-level for guests, persistent for accounts).
- **FR-22 (SHOULD)** Provide side-by-side comparison for 2–4 studies.
- **FR-23 (MUST)** Expose the study's registered contact and/or a guided outreach template.
- **FR-24 (SHOULD)** Provide a "questions to ask the study team" checklist.
- **FR-25 (MAY)** Generate a shareable shortlist link/PDF.

## 6.6 Accounts, alerts, data control

- **FR-26 (SHOULD)** Support optional accounts (auth) for persistence and alerts.
- **FR-27 (SHOULD)** Allow saved searches with new-match alerts (email/push).
- **FR-28 (MUST)** Provide data export and deletion (self-service). See [Compliance](11-compliance-privacy-security.md).
- **FR-29 (MUST)** Obtain explicit consent before storing any health-related inputs.

## 6.7 Coordinator hand-off (later phase)

- **FR-30 (MAY)** Deliver an opt-in structured referral payload to participating sites.

## Traceability matrix (excerpt)

| Requirement | Story |
|-------------|-------|
| FR-1, FR-3 | A1, A2 |
| FR-7, FR-8 | B1 |
| FR-11–FR-14 | B2 |
| FR-16–FR-20 | B3 |
| FR-21–FR-24 | C1, C2, C3 |
| FR-27 | D1 |
| FR-28, FR-29 | D2 |

---

[← User Stories](05-user-stories.md) · [Home](../README.md) · Next: [Non-Functional Requirements →](07-non-functional-requirements.md)
