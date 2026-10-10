# Decision Provenance and Shadow Evaluation

FramePrime separates production authority from evaluation and observability.

## Jev / P1 decision provenance

Jev is used in designated decision / evaluation provenance workflows.

P1 / Jev evidence can be used to inspect or evaluate bounded decisions, while the current production-routing authority remains separately governed.

This public repository does not expose private questions, internal state projections, credentials, or decision payloads.

## Langfuse shadow evaluation

FramePrime has a **Langfuse × Jev/P1 shadow-evaluation** lane.

Its current public boundary is:

- **READ ONLY**
- **NON-AUTHORITATIVE**
- no production-routing authority,
- no production write-back,
- no output mutation authority,
- no requirement for the production request path to depend on the evaluation mirror.

The mirror exists to observe, compare, evaluate, aggregate, and analyze evidence without becoming the product authority.

## Fail-isolated observability

A useful evaluator should not create a new production outage path.

Examples of evaluation-side failures — evaluator timeout, rate limits, mirror mapping errors, or mirror-worker failure — are designed to remain evaluation failures rather than product-delivery failures.

## Why this matters

This creates a clean distinction:

```text
Production decision / safety authority
        ≠
Shadow evaluation / observability authority
```

A score in an evaluation system does not automatically become permission to change production behavior.
