---
name: launch-checklist
description: Inspect a product, SaaS app, landing page, feature, or release before launch. Use when Codex needs to verify readiness across core user flows, authentication, payments, email, states, error handling, mobile responsiveness, accessibility basics, analytics, SEO, legal pages, environment variables, security, deployment, monitoring, and rollback.
---

# Launch Checklist

## Purpose

Use this skill before shipping a product, feature, or public release. The goal is to find launch blockers and high-risk gaps, not to create a perfect enterprise process.

## Launch Review Workflow

1. Identify what is launching and who will use it.
2. List critical flows that must work.
3. Inspect code, configuration, and UI paths relevant to those flows.
4. Check product states, data safety, security, analytics, SEO, and deployment readiness.
5. Classify issues as P0, P1, or P2.
6. Produce a launch decision: Go, Go with known issues, or No-go.

## Severity

P0:
Blocks launch. Core flow broken, payment/auth broken, data loss risk, security leak, missing required legal or privacy handling, production config missing.

P1:
Should fix before broader launch. Major UX gap, missing error recovery, weak mobile experience, missing analytics for core funnel, incomplete emails.

P2:
Can ship with follow-up. Polish, non-critical copy, secondary SEO, nice-to-have metrics.

## Required Output

Return:

- Launch scope.
- Critical flows checked.
- Launch decision.
- P0 blockers.
- P1 fixes.
- P2 follow-ups.
- Manual verification checklist.
- Rollback plan.
- Post-launch monitoring plan.

## Core Areas

Always check:

- Authentication and account access.
- Primary product flow.
- Payment or subscription flow if applicable.
- Email or notification flow if applicable.
- Empty, loading, error, success, and permission states.
- Mobile and common desktop viewport.
- Basic accessibility and keyboard use.
- Analytics for activation and conversion.
- SEO metadata for public pages.
- Legal/privacy pages when collecting user data.
- Environment variables and production secrets.
- Error logging and monitoring.
- Backup, rollback, or recovery path.

Read `references/launch-audit.md` for the detailed checklist.
Read `references/launch-case.md` for a concrete launch review example.
