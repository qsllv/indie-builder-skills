---
name: analytics-and-feedback-loop
description: Plan product analytics, activation metrics, event tracking, feedback collection, user interview prompts, retention signals, funnel analysis, and iteration decisions after launching an indie product or feature. Use when Codex needs to define what to measure, what events to implement, how to interpret user behavior, or how to turn feedback into product decisions.
---

# Analytics And Feedback Loop

## Purpose

Use this skill to help an indie developer learn from real usage. The goal is not to track everything; it is to measure whether users reach value and where they drop off.

## Workflow

1. Define the product's activation event.
2. Map the funnel from visit to first value.
3. Choose a small set of events that answer product questions.
4. Define feedback capture points.
5. Create an iteration decision rule: improve, cut, double down, or ask users.
6. Specify implementation notes for analytics without collecting sensitive data.

## Required Output

Return:

- North-star or core value metric.
- Activation event.
- Funnel events.
- Retention or repeat-use signal.
- Feedback questions and capture points.
- Event properties.
- Privacy notes.
- Decision rules.
- Implementation checklist.

## Measurement Rules

- Track actions that reveal value, not vanity activity.
- Every event should answer a product question.
- Avoid tracking sensitive user content unless necessary and consented.
- Name events consistently: object_action_result or user_action_object.
- Add enough properties to segment behavior without leaking private data.

Read `references/events-and-feedback.md` for examples.
