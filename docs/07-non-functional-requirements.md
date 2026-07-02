# 7. Non-Functional Requirements

[← Functional Requirements](06-functional-requirements.md) · [Home](../README.md) · Next: [User Flows →](08-user-flows.md)

## Performance

- **NFR-1** p95 search response ≤ **2.0 s**; p99 ≤ **4.0 s** under expected load.
- **NFR-2** Plain-language summary + eligibility snapshot for the top result rendered within **3 s**
  of results load (may stream/progressively enhance).
- **NFR-3** Time-to-interactive on a mid-range mobile device ≤ **3 s** on a typical connection.

## Scalability & availability

- **NFR-4** Support at least **10k** monthly active users at launch with headroom to 10×.
- **NFR-5** Target **99.5%** monthly availability for the search experience.
- **NFR-6** Degrade gracefully if a data source is unavailable (serve cached results with a staleness banner).

## Data freshness

- **NFR-7** Registry data refreshed at least **daily**; show source last-updated date per study.
- **NFR-8** Max acceptable staleness vs. source: **48 h** (alert if exceeded).

## Accessibility

- **NFR-9** Conform to **WCAG 2.2 AA**.
- **NFR-10** Full keyboard operability and screen-reader support for all core flows.
- **NFR-11** Plain-language target: summaries readable at roughly a **grade 6–8** level.

## Internationalization

- **NFR-12** UI and study summaries support multiple languages (launch: English + Spanish; expandable).
- **NFR-13** Locale-aware distance units, dates, and number formats.

## Security & privacy

- **NFR-14** Encrypt data in transit (TLS 1.2+) and at rest.
- **NFR-15** Health-related inputs stored only with explicit consent; minimize and allow deletion.
- **NFR-16** Follow least-privilege access and maintain audit logs for sensitive data access.
- See [Compliance, Privacy & Security](11-compliance-privacy-security.md) for the full treatment.

## Reliability & observability

- **NFR-17** Structured logging, metrics, and tracing across the request path.
- **NFR-18** Alerting on latency, error rate, and data-staleness SLO breaches.
- **NFR-19** Defined error budgets tied to the availability target.

## Compatibility

- **NFR-20** Mobile-first responsive web; support current + 1 prior major versions of evergreen browsers.
- **NFR-21** Progressive enhancement — core search works without heavy client-side dependencies.

## Trust & safety

- **NFR-22** Every eligibility/summary output carries a non-final, not-medical-advice disclaimer.
- **NFR-23** Track and cap the **false-hope rate** guardrail. See [Goals & Metrics](03-goals-and-metrics.md).
- **NFR-24** Provide a clear channel to report inaccurate study information.

---

[← Functional Requirements](06-functional-requirements.md) · [Home](../README.md) · Next: [User Flows →](08-user-flows.md)
