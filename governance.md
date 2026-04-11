# Governance

Rules for maintaining the IDX Content Vocabulary.

## Roles

| Role | Holder | Responsibility |
|------|--------|----------------|
| **Schema owner** | Simon Heath | Approves structural changes. Resolves escalated ambiguities. Reviews spine health reports. |
| **Spine controller** | Claude (plugin) | Applies governance rules consistently. Classifies content. Decides routine additions, retirements, and merges. Escalates to owner when rules don't resolve. Maintains the decision log. |

## The three-question test

Every proposal to add, retire, or merge a node must pass all three:

1. **Distinct?** Does this concept require a definition that no existing node provides?
2. **General?** Does it apply across two or more clients or service lines?
3. **Stable?** Is it a durable concept, not a trend or campaign?

All three must pass for a canonical node. Proposals passing only the first question may be registered as **extension nodes** beneath an existing canonical parent.

## Change process

1. **Propose** — Submit via `/spine:governance add` with a one-sentence proposal, one example, and one rationale.
2. **Evaluate** — The spine controller applies the three-question test and returns a decision within minutes: Approved, Rejected (with existing node cited), Approved as extension, or Escalated to owner.
3. **Record** — Approved changes are committed to this repository. The spine version increments. Every ruling is recorded in `decisions.md` with date, reasoning, and version.
4. **Propagate** — Changes are reflected in CMS metadata dropdowns, BigQuery reference tables, and Mercury audit frameworks.

## Node types

| Type | Governance | Scope |
|------|-----------|-------|
| **Canonical node** | Owner approval required | Shared across the portfolio |
| **Extension node** | Controller may approve | Client-specific, registered beneath a canonical parent |

Extension nodes use the format `{parent_id}x{n}` — e.g. `E3.7x1` for a client-specific extension of Responsible products and services.

## Version history

| Version | Date | Nodes | Change |
|---------|------|-------|--------|
| 1.0 | March 2026 | 104 | Initial codification |
| 1.1 | April 2026 | 105 | Added B6.1 Operations and business units |

## AEO priority definitions

| Priority | Meaning |
|----------|---------|
| **Critical** | AI misrepresentation is high risk. Schema markup mandatory. Content must be current. |
| **High** | Important for AI discoverability. Schema markup recommended. |
| **Standard** | Lower AI query frequency. Schema markup optional. |

## Freshness thresholds

Each node specifies the maximum acceptable age for its content:

- **Continuous** — Must reflect current state at all times (e.g. regulatory announcements, share price)
- **6 mo** — Update at least twice per year (e.g. financial results, guidance)
- **12 mo** — Annual refresh (most nodes)
- **24 mo** — Biennial review acceptable (e.g. company history, governance narrative)
- **36 mo** — Slow-moving content (e.g. brand heritage)

## Source provenance rules

- **External**: The node maps to a concept required by a named regulatory framework, reporting standard, or governance code. The framework must be cited in the node's documentation.
- **Portfolio**: The node exists because portfolio traffic data shows material AI or human engagement with a concept not covered by any external standard. Traffic evidence must be documented.
- **Market**: The node reflects widespread market practice (e.g. analyst consensus pages) without formal regulatory requirement. Market convention must be cited.
