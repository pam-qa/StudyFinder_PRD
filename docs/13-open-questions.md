# 13. Open Questions

[← Release Plan](12-release-plan.md) · [Home](../README.md) · Next: [Glossary →](14-glossary.md)

Tracked decisions and unknowns. Update status as they resolve.

| # | Question | Area | Owner | Status |
|---|----------|------|-------|--------|
| Q1 | Which terminology standard for concept mapping — MeSH, SNOMED CT, ICD, or a combination? | [Integrations](10-integrations.md) | Eng/Clinical | Open |
| Q2 | What are the validated baseline figures for the problem statement (enrollment failure, patient awareness)? | [Problem](02-problem-statement.md) | Product/Research | Open |
| Q3 | Are the KPI targets in [Goals](03-goals-and-metrics.md) realistic pre-launch, or should they be provisional? | [Goals](03-goals-and-metrics.md) | Product | Open |
| Q4 | Launch geography — US-only first, or include other regions (affects GDPR/registries)? | [Compliance](11-compliance-privacy-security.md) | Product/Legal | Open |
| Q5 | Does any planned integration bring us into HIPAA covered/BA status? | [Compliance](11-compliance-privacy-security.md) | Legal | Open |
| Q6 | How do we validate eligibility-snapshot accuracy and set the false-hope guardrail threshold? | [Goals](03-goals-and-metrics.md) | Data/Clinical | Open |
| Q7 | LLM provider, model, and evaluation harness for summaries/eligibility? | [Integrations](10-integrations.md) | Eng | Open |
| Q8 | Auth/account provider and guest→account migration approach? | [Data Model](09-data-model.md) | Eng | Open |
| Q9 | Do we need clinician review of generated plain-language content, and at what cadence? | Trust & Safety | Clinical | Open |
| Q10 | Retention TTLs for inactive guest data — exact values? | [Compliance](11-compliance-privacy-security.md) | Legal/Eng | Open |
| Q11 | Which languages beyond English/Spanish, and prioritization? | [NFRs](07-non-functional-requirements.md) | Product | Open |
| Q12 | Coordinator hand-off — which channels do pilot sites actually want? | [User Stories](05-user-stories.md) | Product | Open |

## Assumptions to validate

- Users will trust a plain-language eligibility snapshot if disclaimers are clear.
- ClinicalTrials.gov v2 API coverage + freshness is sufficient for an MVP.
- Free-text → concept mapping can hit acceptable accuracy for common conditions.

## Decisions log

*Record resolved questions here with date and rationale as they close.*

| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-07-02 | StudyFinder scope = clinical/research trial **discovery**, not enrollment | Keeps us out of study-conduct/IRB scope; focuses on the discovery gap |

---

[← Release Plan](12-release-plan.md) · [Home](../README.md) · Next: [Glossary →](14-glossary.md)
