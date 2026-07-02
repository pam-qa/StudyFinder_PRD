# 3. Goals & Success Metrics

[← Problem Statement](02-problem-statement.md) · [Home](../README.md) · Next: [Personas →](04-personas.md)

## Objectives

1. **Make discovery effortless** — a first-time user reaches a relevant, understandable shortlist in
   a single session.
2. **Make eligibility legible** — users understand *why* a study may or may not fit them.
3. **Close the last mile** — users who find a fitting study take a connection action (contact/save/refer).

## Success metrics (KPIs)

| Objective | Metric | Target (12 mo post-launch) |
|-----------|--------|-----------------------------|
| Effortless discovery | % of intakes that reach a results page | ≥ 85% |
| Effortless discovery | Median time from start → shortlist | ≤ 3 min |
| Legible eligibility | % of users who open at least one study detail | ≥ 60% |
| Legible eligibility | Self-reported "I understood if I qualified" (survey) | ≥ 4.0 / 5 |
| Close the last mile | % of active users who take a connect action | ≥ 25% |
| Retention | % who return within 30 days (saved-search / alerts) | ≥ 20% |

## North-star metric

**Qualified connections** — the number of users who reach a study team for a trial they're plausibly
eligible for. It captures the full funnel: found → understood → connected.

## Guardrail metrics (must not regress)

- **False-hope rate:** share of "likely eligible" flags later contradicted by the study team. Keep
  low; over-promising erodes trust. See [Compliance](11-compliance-privacy-security.md).
- **Accessibility:** WCAG 2.2 AA conformance maintained. See [NFRs](07-non-functional-requirements.md).
- **Latency:** p95 search response time (see NFR targets).
- **Data freshness:** max staleness vs. source registry.

## Non-goals

- Maximizing raw result count (we optimize for *relevant* results).
- Replacing the study team's eligibility screening.
- Becoming a general medical-information portal.

## Measurement plan

- Product analytics on the funnel (intake → results → detail → connect).
- Post-session micro-surveys for comprehension and trust.
- Feedback loop with pilot study sites on lead quality (later phase).

See [Open Questions](13-open-questions.md) for baseline/target validation.

---

[← Problem Statement](02-problem-statement.md) · [Home](../README.md) · Next: [Personas →](04-personas.md)
