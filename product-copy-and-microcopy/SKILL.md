---
name: product-copy-and-microcopy
description: Write and review in-product UX copy for software products, including button labels, empty states, errors, success messages, confirmations, onboarding prompts, tooltips, form helper text, permission messages, upgrade prompts, AI generation states, and destructive action warnings. Use when Codex needs product UI text that helps users understand, recover, trust, and act.
---

# Product Copy And Microcopy

## Purpose

Use this skill to write product UI copy that helps users complete tasks. Product microcopy should be clear, specific, honest, and actionable.

## Workflow

1. Identify the user state or action.
2. Explain what happened in user language.
3. Tell the user what they can do next.
4. Keep the tone calm and direct.
5. Avoid vague reassurance, blame, and marketing filler.
6. Match copy to the product's actual behavior.

## Required Output

Return:

- Context.
- Recommended copy.
- Alternatives when useful.
- Where the copy appears.
- Notes on behavior required by the copy.

## Copy Rules

- Button copy should describe the action or outcome.
- Error copy should explain cause and recovery.
- Empty states should explain why empty and how to start.
- Success messages should confirm the result.
- Confirmation dialogs should name the object and impact.
- Upgrade prompts should connect the limit to paid value without misleading pressure.
- AI copy should avoid promising certainty.

## Patterns

Weak:
"Something went wrong."

Better:
"We could not import the CSV because the feedback column is missing. Choose a column and try again."

Weak:
"No data."

Better:
"No feedback imported yet. Upload a CSV to group customer messages by theme."

Read `references/microcopy-patterns.md` for state-specific templates.
