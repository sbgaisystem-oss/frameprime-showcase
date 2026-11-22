# Video Analysis and Evidence

FramePrime separates **video creation authority**, **final-render structure evidence**, and **semantic analysis**.

That separation is intentional: useful analysis should not become a new failure dependency for video generation.

**Current status, checked 2026-11-23: Gemini Video Analysis V2 is OFF in production.** The semantic-analysis sections below describe its design, not an active analysis service. This optional analysis is separate from subtitle authoring and video generation, which have historical production delivery evidence and a separate first-creation-without-purchase confirmation on 2026-11-23. No live Gemini analysis call was executed for this status check.

## Layer 1 — Final-render structure evidence

FramePrime can describe observable structure in the delivered video, including:

- **3s Hook**
- **Opening Static**
- **First Visual Change**
- **Frame Change**
- **Visual Evidence**

The first 0–3 seconds can be previewed from the existing final render. FramePrime does not need to create a separate 3-second derivative asset just to analyze the opening.

## Layer 2 — Gemini Video Analysis V2

Gemini is designed as an **analysis-only** system and is **currently OFF**.

Public authority boundary:

- **READ ONLY**
- **NON-BLOCKING**
- **Authoring authority: NONE**
- **Generation blocking: NEVER**
- **Render blocking: NEVER**
- **Delivery blocking: NEVER**

If Gemini analysis is unavailable, the video creation path can still complete.

## Semantic signals

If enabled and verified in a future release, the design allows content summaries and bounded semantic signals such as:

- **Topic Clarity**
- **Value Proposition Clarity**
- **Demonstration Strength**
- **Visual / Speech Alignment**
- **Cognitive Load**
- **Payoff Match**

These signals are evidence about the content. They are not guaranteed predictions of future views, followers, or engagement.

## Content-feature analysis

The analysis design also includes content features such as knowledge/information value, surprise, humor, emotion, visual interest, story strength, and shareability. This is not a statement that the currently disabled Gemini path produces these features for new videos.

These are **content characteristics**, not claims that a post will achieve a specific outcome.

## Growth relationship

Growth combines:

1. available post-performance KPI evidence,
2. final-render structure evidence,
3. semantic/content analysis only when available; the Gemini path is currently OFF,
4. the user's own historical baseline.

The system keeps these evidence types distinct instead of collapsing them into a single unexplained “AI score.”

## Important distinction

It would be inaccurate to summarize FramePrime as:

> “Gemini decides whether the first three seconds are a good hook.”

A more accurate description is:

> FramePrime separates final-render opening/structure evidence from optional semantic analysis. The Gemini analysis path is currently OFF; its non-blocking design does not imply current execution.
