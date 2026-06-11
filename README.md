# Indie Builder Skills

Practical AI skills for indie developers to plan, build, launch, and improve software products.

This repository is a collection of Codex-compatible skills designed for solo builders and small teams using AI coding agents. The goal is to make AI assistance more reliable across the full product-building workflow: idea clarification, MVP scoping, product design, feature planning, coding review, launch checks, monetization, analytics, and iteration.

## Why This Exists

AI coding agents can write code quickly, but indie products often fail because of problems around the code:

- The product idea is vague.
- The MVP scope becomes too large.
- User flows are incomplete.
- Empty, loading, error, and permission states are missing.
- AI-generated code changes are accepted without review.
- Launch readiness is checked too late.
- Pricing, analytics, and feedback loops are not planned.

These skills turn repeated product-development decisions into reusable workflows that an AI agent can follow.

## Skills Included

### Product Planning

- `product-requirements-planner`: Turn an idea into an MVP PRD, user flow, scope, and acceptance criteria.
- `mvp-scope-guard`: Reduce feature lists to a focused MVP using Must / Manual / Later / Remove decisions.
- `user-flow-designer`: Design complete user flows, alternate paths, states, and screen maps.
- `feature-spec-to-code-plan`: Convert a feature request into an implementation plan with files, states, tests, and risks.

### Product Design

- `product-design-principles`: Guide product UX decisions while building real software.
- `ux-state-checker`: Check missing product states such as empty, loading, error, success, permission, and retry.
- `product-copy-and-microcopy`: Write product UI copy for buttons, errors, empty states, confirmations, onboarding, and upgrade prompts.

### Landing Pages And Growth

- `landing-page-design-review`: Design or audit product landing pages for clarity, perceived value, proof, and conversion.
- `pricing-and-monetization`: Design pricing, packaging, free limits, upgrade triggers, and billing states.
- `analytics-and-feedback-loop`: Plan activation metrics, product events, feedback capture, and iteration decisions.
- `competitor-analysis`: Analyze competitors, alternatives, positioning, pricing, and differentiation opportunities.

### Engineering Quality

- `ai-coding-review`: Review AI-generated code for bugs, scope creep, missing states, security risks, and verification gaps.
- `bug-triage-and-fix`: Reproduce, diagnose, fix, and verify bugs with an evidence-first workflow.
- `launch-checklist`: Inspect products or features before launch across flows, auth, payments, SEO, analytics, config, and monitoring.

## How To Use

Copy the skill folders you want into your Codex skills directory, for example:

```powershell
Copy-Item -Recurse .\product-requirements-planner "$env:USERPROFILE\.codex\skills\"
```

Then invoke a skill by name in your prompt:

```text
Use $product-requirements-planner to turn this idea into a scoped MVP PRD.
```

```text
Use $ai-coding-review to review these AI-generated code changes before I merge them.
```

```text
Use $launch-checklist to check whether this app is ready to launch.
```

## Recommended Workflow

For a new indie product:

1. Use `product-requirements-planner` to clarify the idea.
2. Use `mvp-scope-guard` to cut unnecessary scope.
3. Use `user-flow-designer` to define the first-value path.
4. Use `product-design-principles` and `ux-state-checker` while implementing.
5. Use `feature-spec-to-code-plan` before large code changes.
6. Use `ai-coding-review` after AI-generated code changes.
7. Use `landing-page-design-review` for the public page.
8. Use `pricing-and-monetization` before charging.
9. Use `launch-checklist` before release.
10. Use `analytics-and-feedback-loop` after launch.

## Repository Structure

Each skill lives in its own folder:

```text
skill-name/
  SKILL.md
  agents/
    openai.yaml
  references/
    ...
```

- `SKILL.md` contains the trigger description and core workflow.
- `references/` contains deeper templates, checklists, and examples loaded only when needed.
- `agents/openai.yaml` provides UI metadata for compatible environments.

## Design Principles

These skills are intentionally practical:

- Workflow first, theory second.
- Clear outputs an AI agent can act on.
- Checklists and cases where they improve reliability.
- Strong bias toward shipping narrow, useful MVPs.
- Explicit handling of states, errors, trust, and verification.

## License

MIT
