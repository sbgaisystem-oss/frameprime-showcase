# Dual Surface / Single Core

FramePrime's current architecture direction is **Dual Surface / Single Core**.

## Surface A — FramePrime GUI

The GUI remains a first-class product for users who do not use external agent environments.

Users can work through FramePrime without needing MCP, Claude, Codex, Cursor, or another agent host.

## Surface B — Future Agent Interface

A future agent-facing surface is planned for users who already operate through MCP-capable hosts such as Claude, Codex, Cursor, or other agent environments.

**MCP / Agent Interface status: `FUTURE_NOT_IMPLEMENTED`.**

The architectural direction is that an agent should invoke stable FramePrime capabilities rather than remote-control the website or bypass business rules.

## Same Core

Both surfaces are intended to terminate in the same FramePrime capability core.

Shared invariants include:

- same capability contracts,
- same authoritative project state,
- same credit semantics,
- same safety / validation rules,
- same ownership boundaries,
- durable attributable receipts.

The future agent surface is not intended to create a second, privileged FramePrime.

## Human and agent shared state

The design direction supports a workflow such as:

```text
AI proposes
  ↓
Human reviews / edits in Studio
  ↓
Confirmed state persists
  ↓
Agent reads the updated authoritative state
  ↓
Agent performs the next authorized action
```

Silent last-write-wins is not the intended model for user-visible creative state.

## HyperFrames / external authoring boundary

HyperFrames or another external production environment may exist upstream of FramePrime in a creative workflow.

That is an allowed workflow, not a required FramePrime core dependency.

## Status

- GUI: active product surface
- Single-core rule: active architecture direction
- MCP / Agent Interface: `FUTURE_NOT_IMPLEMENTED`
