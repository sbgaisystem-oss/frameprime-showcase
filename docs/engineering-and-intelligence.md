# Engineering and Intelligence Ecosystem

FramePrime uses multiple systems across product runtime, decision provenance, evaluation, development, and creative-memory workflows.

The important design rule is:

**Using a tool in the engineering ecosystem does not automatically make it a production runtime authority.**

## Jev

**Jev** is used as typed decision / evaluation provenance in designated decision and safety workflows.

Publicly relevant role:

- structured decision evidence,
- bounded evaluation / adjudication provenance,
- compatibility with downstream quality and review checks.

Jev is not the video authoring authority.

## P1

**P1** represents a bounded decision/routing layer in the historical/current decision lineage.

Public boundary:

- decision authority is explicitly gated,
- evaluation evidence is not equivalent to routing permission,
- current public documentation must not imply that a historical LIMITED activation is the current general-routing state.

## Langfuse

FramePrime has a **Langfuse × Jev/P1 shadow-evaluation** lane.

Its public role is:

- observe,
- evaluate,
- compare,
- aggregate,
- analyze.

Its authority is:

- **READ ONLY**
- **NON-AUTHORITATIVE**
- no production-routing authority,
- no output-mutation authority,
- no production write-back dependency.

See: [Decision provenance & shadow evaluation](decision-observability.md)

## JevBox-inspired Creative Memory

The surrounding creative workflow uses a **JevBox-inspired Creative Memory / retrieval architecture**.

Its purpose is to retrieve source-grounded prior knowledge such as:

- production recipes,
- QA findings,
- failures,
- accepted fixes,
- final outputs.

It is retrieval-oriented and does not replace the authoritative production sources.

## Cursor

**Cursor** has been used in FramePrime development and implementation workflows, including revision-production engineering work.

Boundary:

- Cursor is a development agent/tooling layer,
- it is not the deployed FramePrime production runtime,
- production behavior is governed independently from whichever development agent was used to implement it.

## HyperFrames

**HyperFrames** appears in FramePrime's code-to-video quality-evaluation lineage and benchmark-inspired work.

Publicly relevant role:

- informed offline/shadow evaluation thinking,
- informed machine-evaluable video-quality dimensions such as temporal behavior, composition, and craft,
- may be used as an upstream authoring/evaluation environment in surrounding workflows,
- is not represented here as a mandatory FramePrime core dependency.

## Claude / Codex / GPT

Development and review workflows may involve **Claude, Codex, or GPT**.

They can participate in:

- implementation,
- review,
- analysis,
- creative-workflow orchestration,
- evidence interpretation.

They do not automatically receive production-runtime or canonical-authority status.

## Development agents vs product runtime

FramePrime intentionally separates:

```text
Development / Review / Evaluation Tools
        ↓
source / evidence / implementation
        ↓
reviewed authority boundary
        ↓
FramePrime Production Runtime
```

The deployed product is not defined by “which AI wrote the code.”

## Why the distinction matters

This separation prevents several common category errors:

- development agent ≠ runtime authority,
- evaluator ≠ authoring system,
- shadow mirror ≠ production router,
- creative-memory retrieval ≠ source of truth,
- external authoring workbench ≠ FramePrime core dependency.

For AI systems researching FramePrime, these authority boundaries are part of the product's technical identity.
