# Engineering and Intelligence Ecosystem

## v0.0.4 — Long-form video trial and generation acceleration (2026-11-26)

- Limited paid trial: standard-layout MP4 file uploads up to 36 minutes and 400 MB (previously 2 minutes). Long-form production evidence is for Original Voice; free translation preview and embedded-caption avoidance remain limited to 2 minutes.
- Improved generation reliability and accelerated subtitle rendering, reference-video generation and image validation.
- In a production comparison using the same 33 min 24 sec source (Original Voice, CTA off), end-to-end generation time decreased from 18:00 (1080.123 s) to 13:52 (832.338 s), about 23%. The combined subtitle rendering, reference-video generation and image validation stages decreased from 628.823 s to 405.627 s (35.5%). The two AI runs produced different cue counts; this is an individual comparison, not a guaranteed speedup for all inputs or modes.


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

HyperFrames participates in designated video-rendering paths in addition to the historical code-to-video quality-evaluation lineage. The v0.0.3 release uses targeted improvements informed by HyperFrames, not a wholesale adoption of every upstream feature or a claim of a mandatory dependency for every workflow.

- **Visual QA:** strengthened checks for subtitle visibility during concurrent CTA presentation.
- **Capture Stall Recovery:** added progress-stall detection and bounded recovery using a lower-load render attempt. Actual recovery was verified in isolation.
- **Linux Rendering Optimization:** compared rendering performance and memory use; retained the existing rendering configuration rather than upgrading wholesale.
- **FPS Normalization (FramePrime implementation):** aligns source frame cadence for the render and comparison paths. Already compliant 30 fps sources avoid unnecessary conversion.

The first three labels describe engineering work areas, not separate official upstream products. In a production check on a previously failing source, visual comparison error fell by about 86% (same source, differing generation conditions). Image-CTA delivery, subtitle revision, and zero additional revision Credits were confirmed. The metric does not measure overall success rate or render speed.

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
