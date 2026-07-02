# 2. Problem Statement

[← Vision & Scope](01-vision-and-scope.md) · [Home](../README.md) · Next: [Goals & Metrics →](03-goals-and-metrics.md)

## The problem

Clinical trials are a critical treatment option, yet the path from "I need one" to "I'm talking to a
study team" is broken:

- **Discovery is hard.** Registries like ClinicalTrials.gov are comprehensive but written for
  researchers. Eligibility criteria are dense, jargon-heavy, and hard for patients to interpret.
- **Search is literal, not clinical.** Keyword search returns hundreds of results with no sense of
  which are actually relevant to a specific patient's situation.
- **Eligibility is opaque.** Patients can't easily tell if they meet inclusion/exclusion criteria
  without a clinician's help, so they self-select out — or waste time on studies they can't join.
- **The last mile fails.** Even when a good match exists, contact info is buried and the outreach
  process is unclear, so interested patients never connect.

## Evidence & context

- A large share of trials fail to meet enrollment targets, and slow accrual is a leading cause of
  trial delays and terminations.
- Patients frequently report they were **never told** a relevant trial existed.
- Eligibility criteria are the single biggest source of confusion in the patient discovery journey.

> 📌 *Replace the bullets above with cited figures during research spike — see
> [Open Questions](13-open-questions.md).*

## Why now

- Registry data is available via robust public APIs (ClinicalTrials.gov v2 API).
- Modern language models can translate dense eligibility criteria into plain language and reason
  about approximate fit — enabling the personalized experience that wasn't feasible before.
- Patient expectations for consumer-grade health tools are high.

## Impact of solving it

- **Patients** get faster access to potentially better treatment.
- **Sponsors/sites** get better-qualified inbound interest and faster accrual.
- **The system** benefits from trials that complete on time with representative participants.

## Consequences of not solving it

Patients continue to miss trials they qualify for; trials continue to under-enroll; and the gap
between "eligible" and "enrolled" stays as wide as it is today.

---

[← Vision & Scope](01-vision-and-scope.md) · [Home](../README.md) · Next: [Goals & Metrics →](03-goals-and-metrics.md)
