---
name: new-user-product-review
description: Review product pages, app screens, onboarding flows, UI states, feature design, interaction design, and product copy from the perspective of an ordinary first-time user. Use when Codex needs to identify confusion, friction, unclear value, weak calls to action, missing feedback states, misleading labels, onboarding gaps, or anything that may block, discourage, or confuse new users, then provide prioritized improvement suggestions.
---

# New User Product Review

## Purpose

Use this skill to review a product experience as a first-time user who has no internal context, no patience for ambiguity, and one practical goal: understand the product and reach first value.

Focus on whether ordinary new users can understand, trust, and act. Do not default to expert design critique or visual polish until the first-use path is clear.

## Review Workflow

1. Identify the likely user, arrival context, product promise, and first meaningful action. If missing, infer reasonable assumptions and state them.
2. Run a 10-second comprehension test:
   - What is this product or screen?
   - Who is it for?
   - What can the user do here?
   - What should the user do next?
   - What visible element gets the most attention, and is it the right one?
3. Trace the first-use path from arrival to first value. Include onboarding, account creation, setup, empty states, permissions, sample data, primary action, result, and recovery paths when relevant.
4. Review the experience across six dimensions:
   - Understanding: Does the user quickly grasp the product, screen purpose, and value?
   - Action: Is the next step obvious, specific, and low-risk?
   - Discovery: Are important features findable without knowing the product's internal model?
   - Feedback: Do clicks, loading, errors, successes, and empty states explain what happened and what to do next?
   - Copy: Are headings, labels, buttons, tooltips, and helper text clear in user language?
   - Trust: Does the product avoid surprises around data, permissions, pricing, AI behavior, publishing, deletion, and irreversible actions?
5. Prioritize findings by the impact on first-time activation, not by aesthetic preference.
6. Recommend concrete fixes at the level of screen structure, flow, UI state, component, or copy.

For a deeper rubric, read `references/review-rubric.md`. For detailed copy review, read `references/copy-clarity-checklist.md`.

## First-Time User Lens

Assume the user:

- Has not read documentation.
- Does not know the product's internal terms.
- May be comparing alternatives.
- Is trying to decide whether the product is worth effort or trust.
- Will abandon the flow if the next step is unclear, risky, or too much work before value appears.
- Needs visible confirmation after meaningful actions.

Do not assume the user understands dashboards, automations, AI agents, integrations, credits, workspaces, projects, pipelines, models, prompts, or configuration unless the interface teaches those concepts in context.

## Severity

- P0: Blocks comprehension, trust, or completion of the first meaningful action.
- P1: Creates strong friction, hesitation, wrong turns, or likely abandonment.
- P2: Causes confusion or extra effort but users can continue.
- P3: Improves polish, consistency, or confidence without changing the core path.

## Issue Rules

Each finding should include:

- What the new user sees.
- What the new user may think or do.
- Why it matters.
- A concrete fix.
- Severity.

Avoid vague feedback like "make it clearer", "improve UX", or "add guidance" unless paired with the exact UI, flow, or copy change.

## Output Format

When reviewing a product page, screen, or flow, return:

- New user verdict: one short judgment on whether a first-time user can understand and reach first value.
- Assumptions: target user, context, and first meaningful action if not provided.
- Top blockers: P0/P1 issues first.
- Findings: grouped by Understanding, Action, Discovery, Feedback, Copy, and Trust.
- First-use journey notes: where the user moves smoothly and where they may hesitate or abandon.
- Copy improvements: original copy, issue, suggested rewrite when relevant.
- Quick wins: 3-5 practical changes that can be made quickly.
- Deeper product questions: unresolved decisions that affect the experience.

When improving rather than auditing, return the revised flow, screen structure, and replacement copy before secondary recommendations.

## Quality Bar

A review is useful only when it helps the product team decide what to change next. Before finishing, verify that:

- The highest-priority issues are about first-use understanding, action, trust, or completion.
- Every major finding is grounded in something visible or inferable from the provided product artifact.
- Recommendations are specific enough for a designer, PM, or engineer to implement.
- Copy rewrites are shorter, clearer, and closer to user language.
- The review distinguishes blockers from polish.
