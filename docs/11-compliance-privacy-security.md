# 11. Compliance, Privacy & Security

[← Integrations](10-integrations.md) · [Home](../README.md) · Next: [Release Plan →](12-release-plan.md)

> ⚠️ This page states product intent and requirements. It is **not** legal advice. Engage legal,
> privacy, and regulatory counsel before launch. Open items are tracked in
> [Open Questions](13-open-questions.md).

## Regulatory posture

- **Discovery tool, not a covered activity by default.** StudyFinder helps patients *find* trials; it
  does not conduct studies, enroll participants, or provide treatment.
- **Not medical advice.** All summaries and eligibility snapshots are informational and must be
  labeled non-final ([NFR-22](07-non-functional-requirements.md), [FR-18](06-functional-requirements.md)).
- **HIPAA:** StudyFinder is generally *not* a covered entity or business associate when users self-enter
  data for their own discovery. If we later integrate with providers/sites handling PHI, BAAs and HIPAA
  controls apply. **Confirm with counsel** — see [Open Questions](13-open-questions.md).
- **Human-subjects / IRB:** Enrollment, screening, and consent for study participation remain the
  responsibility of each study team and its IRB — explicitly **out of scope** for StudyFinder.

## Privacy principles

1. **Data minimization** — collect only what's needed to match ([SearchProfile](09-data-model.md)).
2. **Consent-first** — explicit, informed consent before storing any health-related input ([FR-29](06-functional-requirements.md)).
3. **Purpose limitation** — health inputs used only for matching, never sold.
4. **User control** — self-service export and deletion ([FR-28](06-functional-requirements.md)).
5. **Coarse by default** — default to coarse location; precise only when the user opts in.

## Consent model

- Search without an account and without persisting sensitive inputs (session-only) is allowed.
- Persisting a [SearchProfile](09-data-model.md), saved studies, or alerts requires explicit consent
  with a clear, plain-language notice.
- Consent state and timestamps are recorded ([Data Model](09-data-model.md)).

## Data handling & retention

| Data class | Retention | Controls |
|------------|-----------|----------|
| Registry/study (public) | While relevant | Cacheable, no restrictions |
| SearchProfile / EligibilitySnapshot (health) | Until user deletes; default TTL for inactive guests | Encrypted, consent-gated, deletable |
| Account/auth (PII) | Life of account | Standard PII controls, deletable |
| Logs with sensitive context | Minimized + short retention | Access-controlled, audited |

## Security controls

- **Encryption:** TLS 1.2+ in transit; encryption at rest ([NFR-14](07-non-functional-requirements.md)).
- **Access:** least-privilege, role-based; audit logs for sensitive-data access ([NFR-16](07-non-functional-requirements.md)).
- **Secrets:** managed via a secrets manager; no credentials in source.
- **Vulnerability management:** dependency scanning, periodic review, responsible-disclosure path.
- **Data isolation:** separate sensitive stores; tokenize/pseudonymize where feasible.

## Regional considerations

- **GDPR (EU/EEA):** if serving EU users — lawful basis, DSAR handling, data-transfer safeguards.
- **State laws (e.g., CCPA/CPRA):** honor access/delete/opt-out rights.
- Applicability depends on launch geography — see [Open Questions](13-open-questions.md).

## Trust & safety commitments

- Always show source and last-updated date for study data.
- Never present eligibility as a guarantee ([FR-20](06-functional-requirements.md)).
- Provide a way to report inaccurate study info ([NFR-24](07-non-functional-requirements.md)).

---

[← Integrations](10-integrations.md) · [Home](../README.md) · Next: [Release Plan →](12-release-plan.md)
