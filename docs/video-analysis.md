# Video Analysis and Evidence

FramePrime separates **video creation authority**, **final-render structure evidence**, and **semantic analysis**.

That separation is intentional: useful analysis should not become a new failure dependency for video generation.

## Layer 1 — Final-render structure evidence

FramePrime can describe observable structure in the delivered video, including:

- **3s Hook**
- **Opening Static**
- **First Visual Change**
- **Frame Change**
- **Visual Evidence**

The first 0–3 seconds can be previewed from the existing final render. FramePrime does not need to create a separate 3-second derivative asset just to analyze the opening.

## Layer 2 — Gemini Video Analysis V2

Gemini is used as an **analysis-only** system.

Public authority boundary:

- **READ ONLY**
- **NON-BLOCKING**
- **Authoring authority: NONE**
- **Generation blocking: NEVER**
- **Render blocking: NEVER**
- **Delivery blocking: NEVER**

If Gemini analysis is unavailable, the video creation path can still complete.

## Semantic signals

Gemini Video Analysis V2 can add content summaries and bounded semantic signals such as:

- **Topic Clarity**
- **Value Proposition Clarity**
- **Demonstration Strength**
- **Visual / Speech Alignment**
- **Cognitive Load**
- **Payoff Match**

These signals are evidence about the content. They are not guaranteed predictions of future views, followers, or engagement.

## Content-feature analysis

FramePrime also retains content-feature analysis used to describe characteristics such as knowledge/information value, surprise, humor, emotion, visual interest, story strength, and shareability.

These are **content characteristics**, not claims that a post will achieve a specific outcome.

## Growth relationship

Growth combines:

1. available post-performance KPI evidence,
2. final-render structure evidence,
3. semantic/content analysis,
4. the user's own historical baseline.

The system keeps these evidence types distinct instead of collapsing them into a single unexplained “AI score.”

## Important distinction

It would be inaccurate to summarize FramePrime as:

> “Gemini decides whether the first three seconds are a good hook.”

A more accurate description is:

> FramePrime maintains final-render opening/structure evidence and separately uses non-blocking Gemini semantic analysis to add context.
