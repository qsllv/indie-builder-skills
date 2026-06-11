---
name: mvp-scope-guard
description: Review product ideas, PRDs, feature lists, roadmaps, or AI implementation plans to reduce scope and protect MVP focus. Use when Codex needs to decide what belongs in the first version, what should be deferred, what can be manual, whether a feature supports the core promise, or how to prevent an indie product from becoming too broad before launch.
---

# MVP Scope Guard

## Purpose

Use this skill to cut product scope until the MVP can ship and test one core value proposition. The goal is not to make the product small for its own sake; the goal is to preserve the shortest path to learning whether users value the product.

## Scope Review Workflow

1. State the core user, core problem, and core promise.
2. Identify the first-value event: the moment the user receives useful output or completes the target job.
3. List all proposed features.
4. Classify each feature as Must, Manual, Later, or Remove.
5. Challenge every feature with the guardrail questions below.
6. Return a reduced MVP plan and a deferred backlog.

## Guardrail Questions

For each feature, ask:

- Does this directly enable first value?
- Does the product promise become false without it?
- Is it required for trust, safety, payment, or legal compliance?
- Can the founder do this manually for the first 10 users?
- Can this be replaced by email, CSV, admin script, or manual onboarding?
- Does it introduce a second persona, second workflow, or second product?
- Does it require infrastructure before demand is proven?
- Will removing it block launch or only reduce polish?

## Classification

Must:

- Needed for first value.
- Needed for the core promise.
- Needed for safe operation.

Manual:

- Important, but can be handled by the founder or support process at first.

Later:

- Useful after demand is validated.

Remove:

- Nice-to-have, speculative, or unrelated to the core promise.

## Output Format

Return:

- Core promise.
- First-value event.
- Scope decision table: Feature, Decision, Reason, Simpler alternative.
- Final MVP scope.
- Manual founder tasks.
- Deferred backlog.
- Risks from cutting scope.
- Next build sequence.

## Red Flags

Flag scope creep when:

- The MVP needs roles, permissions, teams, billing, integrations, analytics, and automation before any user sees value.
- A feature serves a hypothetical enterprise buyer but the product has no users yet.
- The plan requires a marketplace, community, or network effect before a single-player use case works.
- The page or app promises a platform but implements no complete workflow.

Read `references/scope-cut-cases.md` for concrete examples.
