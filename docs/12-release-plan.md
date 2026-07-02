# 12. Release Plan

[← Compliance, Privacy & Security](11-compliance-privacy-security.md) · [Home](../README.md) · Next: [Open Questions →](13-open-questions.md)

Dates are placeholders relative to project kickoff (T0). Adjust once staffing is confirmed.

## MVP cut line

The MVP delivers the **core discovery journey** end to end for patients and caregivers:

- Guided intake with plain-language condition entry ([A1](05-user-stories.md), [FR-1–FR-5](06-functional-requirements.md))
- Ranked shortlist from ClinicalTrials.gov ([B1](05-user-stories.md), [FR-6–FR-8](06-functional-requirements.md))
- Plain-language summaries ([B2](05-user-stories.md), [FR-11–FR-13](06-functional-requirements.md))
- Eligibility snapshot with disclaimers ([B3](05-user-stories.md), [FR-16–FR-20](06-functional-requirements.md))
- Save + connect ([C1, C3](05-user-stories.md), [FR-21, FR-23](06-functional-requirements.md))
- Consent, export/delete for any stored health data ([FR-28, FR-29](06-functional-requirements.md))

**Explicitly deferred from MVP:** compare view, saved-search alerts, accounts beyond basic
persistence, multilingual beyond English, coordinator hand-off.

## Milestones

| Milestone | Target | Contents |
|-----------|--------|----------|
| **M0 — Discovery & design** | T0 → T0+4w | Validate problem metrics, terminology-mapping spike, UX flows, legal/privacy review kickoff |
| **M1 — Ingestion & search** | T0+4w → T0+8w | ClinicalTrials.gov ingestion, normalized store, ranked search |
| **M2 — Comprehension & eligibility** | T0+8w → T0+12w | Plain-language summaries, eligibility snapshot, disclaimers |
| **M3 — Save/connect & consent** | T0+12w → T0+15w | Save, guided outreach, consent + export/delete |
| **M4 — Private beta** | T0+15w → T0+18w | Hardening, accessibility audit, closed pilot |
| **M5 — Public MVP launch** | T0+18w | Launch (English), monitoring, feedback loop |

## Post-MVP roadmap

| Phase | Theme | Highlights |
|-------|-------|-----------|
| **P1** | Depth & retention | Compare view, accounts, saved searches + alerts, filters ([B4, C2, D1, D2](05-user-stories.md)) |
| **P1** | Reach | Spanish support; accessibility deepening |
| **P2** | Coverage | Additional registries (WHO ICTRP, EU CTIS) |
| **P2** | Sites | Coordinator hand-off / structured referrals ([E1](05-user-stories.md)) |
| **Exploratory** | Context | Consent-based EHR/portal import |

## Launch readiness checklist

- [ ] Accessibility audit passed (WCAG 2.2 AA)
- [ ] Legal/privacy sign-off (consent, retention, disclaimers)
- [ ] Data freshness monitoring + alerting live
- [ ] False-hope guardrail instrumented ([Goals & Metrics](03-goals-and-metrics.md))
- [ ] Analytics funnel + micro-surveys wired
- [ ] Incident response + reporting channel ready

## Dependencies & risks

- Terminology-mapping accuracy (spike in M0).
- Legal/privacy timeline could gate M3/M4.
- LLM summary/eligibility quality must clear the guardrail before beta.

See [Open Questions](13-open-questions.md).

---

[← Compliance, Privacy & Security](11-compliance-privacy-security.md) · [Home](../README.md) · Next: [Open Questions →](13-open-questions.md)
