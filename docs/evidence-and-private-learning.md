# Evidence-first Video Intelligence and Private Learning

FramePrime treats **evidence authority** as a separate problem from AI-generated explanation.

## Evidence Contract

The public model can be summarized as:

```text
Video Identity
  ↓
Time Window / Structural Region
  ↓
Observed Feature
  ↓
Observed Outcome
  ↓
Source Pointer / Provenance
  ↓
Permission / Consent
```

The important rule is:

**AI-written insight text is not itself the factual evidence authority.**

Evidence should be able to point back to the relevant video identity, time range, analyzer/version, source observation, and observed KPI evidence where applicable.

## Private Learning first

FramePrime uses a **private-first / global-hold** learning strategy.

```text
User A videos
  + User A observed KPI
  + User A structural evidence
      ↓
Personal baseline
      ↓
Evidence-linked comparison
      ↓
Growth / Studio recommendation
```

The deployed Private Learning path is owner-scoped. Global cross-user learning, a global video corpus, vector search, or knowledge-graph style aggregation is not implied by this public repository.

## Sample-size restraint

FramePrime does not treat a handful of videos as statistical proof.

The current guardrail distinguishes:

- fewer than 10 matched posted videos: do not assert a personal pattern,
- 10–29: descriptive baseline / median / range,
- 30 or more: exploratory relationship analysis may be shown with sample-size and limitation context.

These thresholds are product guardrails, not guarantees of statistical significance.

## Missing data is not zero

Observed outcomes preserve distinct states rather than collapsing everything into a number:

- MEASURED_VALUE
- NOT_FETCHED
- UNSUPPORTED
- PROVIDER_MISSING
- PERMISSION_FAILURE
- ACQUISITION_FAILURE
- NOT_APPLICABLE

This prevents a missing KPI from becoming a false zero.

## Causality boundary

Allowed language is descriptive or associative.

FramePrime does not treat:

> “Feature X appeared in videos with higher observed KPI Y”

as equivalent to:

> “Feature X caused KPI Y.”

Causal claims require a separate experimental basis.

## Global learning boundary

FramePrime intentionally does **not** present raw customer media as a shared learning corpus by default.

Global aggregation remains a separate future gate with consent, privacy, comparability, and re-identification constraints.
