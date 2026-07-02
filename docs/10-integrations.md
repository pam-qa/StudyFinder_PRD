# 10. Integrations

[← Data Model](09-data-model.md) · [Home](../README.md) · Next: [Compliance, Privacy & Security →](11-compliance-privacy-security.md)

## Primary source — ClinicalTrials.gov (v2 API)

- **What:** The U.S. NIH registry of clinical studies; the authoritative primary source.
- **API:** ClinicalTrials.gov **v2 REST API** — <https://clinicaltrials.gov/data-api/api>.
- **Access:** Public; no auth required. Respect rate limits and terms of use.
- **Usage in StudyFinder:**
  - Search by condition, location, status, phase, and other fields.
  - Retrieve full study records including eligibility criteria and contacts.
  - Sync/refresh on a schedule for freshness ([NFR-7/8](07-non-functional-requirements.md)).
- **Fields we rely on:** NCT ID, brief/official title, conditions, eligibility (inclusion/exclusion),
  status, phase, interventions, sponsor, locations, contacts, last-update date.

### Sync strategy
- Scheduled ingestion (≥ daily) into a normalized [Study](09-data-model.md) store.
- Incremental updates via last-update timestamps where possible.
- Cache with a staleness banner as a fallback if the API is unavailable.

## Standardized terminology / concept mapping

- Map free-text conditions to standardized concepts (e.g., a medical ontology such as MeSH / SNOMED /
  ICD — final choice TBD; see [Open Questions](13-open-questions.md)).
- Enables robust matching and synonym handling for [FR-1](06-functional-requirements.md).

## Language model services (plain language & eligibility reasoning)

- **Purpose:** Generate plain-language study summaries ([FR-11](06-functional-requirements.md)) and
  reason about approximate eligibility fit ([FR-16](06-functional-requirements.md)).
- **Constraints:** Output must be labeled non-final / not medical advice
  ([NFR-22](07-non-functional-requirements.md)); track model_version for auditability
  ([Data Model](09-data-model.md)); guard against over-promising ([false-hope guardrail](03-goals-and-metrics.md)).
- **Provider:** Default to the latest, most capable Claude models via the Anthropic API for summary
  generation and eligibility reasoning.

## Geocoding & distance

- Geocode user location and study sites to compute proximity/distance for ranking and filters.

## Notifications

- Email (and optionally push) for saved-search alerts ([FR-27](06-functional-requirements.md)).

## Future / optional integrations

- Additional registries (e.g., WHO ICTRP, EU CTIS) for non-US coverage — later phase.
- EHR/patient-portal context import (with consent) — exploratory.
- Coordinator hand-off channels for structured referrals ([FR-30](06-functional-requirements.md)).

## Integration risks

- Source schema/API changes → isolate behind an ingestion adapter.
- Rate limits / outages → cache + graceful degradation ([NFR-6](07-non-functional-requirements.md)).
- Terminology mapping accuracy → measure and iterate; see [Open Questions](13-open-questions.md).

---

[← Data Model](09-data-model.md) · [Home](../README.md) · Next: [Compliance, Privacy & Security →](11-compliance-privacy-security.md)
