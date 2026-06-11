---
name: product-requirements-planner
description: Turn early product ideas into practical product requirements, MVP PRDs, user flows, feature lists, acceptance criteria, release phases, and build-ready product briefs. Use when Codex needs to clarify a product concept, define target users and jobs-to-be-done, scope an MVP, write a PRD for an indie product or SaaS feature, or prepare requirements before implementation.
---

# Product Requirements Planner

## Purpose

Use this skill to convert a vague product idea into a buildable product plan. The output should help an AI coding agent know what to build, what not to build, what the user flow is, and how to verify completion.

Do not produce a generic business plan. Produce a concrete product brief that can drive implementation.

## Workflow

1. Identify the product idea in one sentence.
2. Define target user, trigger moment, current workaround, pain, and desired outcome.
3. State the core product promise: "Help [user] achieve [outcome] when [situation] without [pain]."
4. Define the MVP success path: the shortest path from entry to first value.
5. Split requirements into Must, Should, Later, and Not Now.
6. Map the primary user flow and required states.
7. Draft data objects, permissions, integrations, and side effects if relevant.
8. Write acceptance criteria that an agent can test.
9. List open questions only when the answer materially changes scope.

## Required Output

Return these sections:

- Product summary: one paragraph.
- Target user and job: role, situation, current workaround, desired result.
- Core promise: one sentence.
- MVP scope:
  - Must have
  - Should have
  - Later
  - Not now
- Primary user flow: numbered steps from entry to value.
- Key screens or surfaces.
- Data model draft: main objects and fields, not full schema unless requested.
- Required states: empty, loading, error, success, permission, edge cases.
- Acceptance criteria: testable bullets.
- Risks and open questions.

## Scope Rules

Prefer a narrow product that proves one valuable workflow over a broad platform.

Must-have features must satisfy all:

- Needed for the primary user to reach first value.
- Needed for the product promise to be true.
- Needed for basic trust, safety, or payment if applicable.

Move to Later when:

- It helps power users but is not needed for first value.
- It can be done manually by the founder at first.
- It requires complex infrastructure before demand is proven.
- It adds secondary personas or edge workflows.

## Acceptance Criteria Rules

Write acceptance criteria as observable behavior:

- "When a user uploads a valid CSV, the app creates feedback records and shows an import summary."
- "If import fails, the user sees the failed row count and can download an error file."

Avoid vague criteria:

- "The app should be fast."
- "The UI should be user-friendly."

## References

Read `references/prd-template.md` when the user asks for a full PRD or feature spec.
Read `references/case-guide.md` when a concrete example would help shape an early idea.
