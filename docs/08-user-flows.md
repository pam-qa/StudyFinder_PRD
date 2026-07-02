# 8. User Flows

[← Non-Functional Requirements](07-non-functional-requirements.md) · [Home](../README.md) · Next: [Data Model →](09-data-model.md)

Diagrams use [Mermaid](https://mermaid.js.org/), which renders natively on GitHub.

## Flow 1 — First-time discovery (happy path)

```mermaid
flowchart TD
    A[Land on StudyFinder] --> B[Guided intake: condition in plain words]
    B --> C{Term clear?}
    C -- No --> D[Disambiguate concept]
    C -- Yes --> E[Add location + optional details]
    D --> E
    E --> F[Run search over registries]
    F --> G[Ranked shortlist with summaries + eligibility snapshot]
    G --> H{Interested?}
    H -- Save --> I[Add to saved list]
    H -- Open --> J[Study detail: plain-language + criteria]
    J --> K{Take next step?}
    K -- Contact --> L[Guided outreach to study team]
    K -- Compare --> M[Side-by-side compare]
    K -- Back --> G
```

## Flow 2 — Caregiver searching for someone else

```mermaid
flowchart TD
    A[Choose 'searching for someone else'] --> B[Intake reworded for third person]
    B --> C[Enter loved one's condition + location]
    C --> D[Results shortlist]
    D --> E[Save + compare studies]
    E --> F[Generate shareable shortlist for care team]
```

## Flow 3 — Returning user with saved search & alert

```mermaid
flowchart TD
    A[Sign in] --> B[Open saved search]
    B --> C{New matching trials since last visit?}
    C -- Yes --> D[Highlight new matches]
    C -- No --> E[Show current matches]
    D --> F[Review + connect]
    E --> F
    A2[Receives alert email/push] --> B
```

## Flow 4 — Eligibility snapshot refinement

```mermaid
flowchart TD
    A[Study shows 'needs review'] --> B[Offer targeted follow-up questions]
    B --> C[User answers]
    C --> D{Enough info?}
    D -- Yes --> E[Update snapshot: may qualify / likely not]
    D -- No --> F[Keep 'needs review' + suggest asking study team]
    E --> G[Always: 'not a final determination' notice]
    F --> G
```

## Edge cases & error states

- **No results:** offer to broaden condition, expand radius, or include not-yet-recruiting studies.
- **Source unavailable:** serve cached results with a staleness banner ([NFR-6](07-non-functional-requirements.md)).
- **Ambiguous condition:** always confirm the mapped concept before searching.
- **Guest saves then leaves:** offer account creation to persist the saved list.
- **Contact info missing on source:** fall back to source-record link + generic guidance.

---

[← Non-Functional Requirements](07-non-functional-requirements.md) · [Home](../README.md) · Next: [Data Model →](09-data-model.md)
