# Subtitle Quality and Source-grounded Audio Safety

FramePrime separates subtitle generation from subtitle presentation quality and from audio-evidence safety.

## Subtitle coverage

FramePrime includes a **coverage completeness** contract intended to reduce missing trusted linguistic content in the final presentation.

The goal is not merely to generate subtitle text, but to verify that required trusted content is represented in the delivered presentation.

## Collision avoidance

FramePrime also includes **collision avoidance** for subtitle / telop presentation.

When a preferred subtitle position conflicts with important visual content, the presentation layer can move the text to a safer lane rather than treating one fixed position as mandatory.

This is a rendering/presentation concern and remains separate from semantic authoring.

## Source-grounded audio safety

FramePrime uses source-grounded audio / transcript safety boundaries rather than assuming every audio window can safely become subtitle text.

At a high level, the system distinguishes evidence classes such as:

- SPEECH
- SONG
- NONE / insufficient supported content

The important public principle is:

**When source evidence is insufficient or ambiguous, FramePrime prefers fail-closed behavior over fabricating unsupported subtitles.**

## Why this matters

A subtitle system can fail in two different ways:

1. **semantic failure** — writing text the source does not support,
2. **presentation failure** — placing valid text poorly or omitting required content.

FramePrime treats these as separate quality problems.

## Public disclosure boundary

This document intentionally does not publish private classifier thresholds, provider-routing details, challenge budgets, prompt text, or internal safety payloads.
