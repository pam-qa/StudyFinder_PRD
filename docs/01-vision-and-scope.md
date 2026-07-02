# 1. Vision & Scope

[← Home](../README.md) · Next: [Problem Statement →](02-problem-statement.md)

## Elevator pitch

For patients and caregivers facing a diagnosis, finding a relevant clinical trial is slow,
intimidating, and fragmented. **StudyFinder** turns the world's clinical-trial registries into a
plain-language, personalized search: describe your situation once, and get a ranked, understandable
list of studies you may qualify for — with a clear path to contact the study team.

## Vision

Every patient who could benefit from a clinical trial can find one in minutes, understand whether
it's a fit, and reach the right coordinator — regardless of medical literacy, language, or where
they receive care.

## Who it's for

- **Patients** actively researching treatment options.
- **Caregivers / family members** searching on behalf of a loved one.
- **Referring clinicians** who want to point a patient toward relevant trials quickly.
- **Study coordinators** who want better-qualified inbound interest (secondary, later phase).

See [Personas](04-personas.md) for detail.

## What success looks like

A user lands on StudyFinder, answers a short guided intake (condition, location, key clinical
details), and within one session receives a ranked shortlist of trials with:

- a plain-language summary of each study,
- a personalized "why this might fit you" explanation,
- a clear eligibility snapshot (likely-eligible / needs-review / likely-ineligible),
- and a one-tap way to contact or save the study.

## In scope (this PRD)

- Guided intake and free-text condition entry.
- Search and ranking over public trial registries (starting with [ClinicalTrials.gov](10-integrations.md)).
- Plain-language study summaries and eligibility explanations.
- Saved studies, comparison, and contact/referral hand-off.
- Accounts, saved searches, and notifications for new matching trials.

## Out of scope (for now)

- Determining **final** eligibility or enrolling a patient (owned by the study team).
- Providing medical advice or treatment recommendations.
- E-consent / EDC (electronic data capture) for study conduct.
- Payments, travel, or reimbursement logistics.
- Provider-side CRM / recruitment analytics beyond basic contact hand-off.

## Guiding principles

1. **Clarity over completeness** — a shorter, understandable list beats an exhaustive dump.
2. **Never overstate eligibility** — always frame as "may qualify," confirmed by the study team.
3. **Privacy by default** — collect the minimum needed to match; see [Compliance](11-compliance-privacy-security.md).
4. **Accessible to all** — plain language, multilingual, WCAG 2.2 AA. See [NFRs](07-non-functional-requirements.md).

---

[← Home](../README.md) · Next: [Problem Statement →](02-problem-statement.md)
