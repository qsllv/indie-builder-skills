# Launch Case

Product:
AI feedback analyzer MVP.

Critical flows:

1. Visitor opens landing page and signs up.
2. User uploads feedback CSV.
3. User receives AI theme analysis.
4. User exports analysis.
5. User upgrades to paid plan.

P0 checks:

- Signup creates workspace and redirects to dashboard.
- CSV upload rejects invalid files and does not crash.
- AI analysis failure shows retry and does not lose uploaded data.
- Payment webhook updates subscription status.
- API keys and webhook secrets are not exposed.

P1 checks:

- Empty dashboard says "Upload feedback to create your first analysis."
- Loading state explains analysis may take a minute.
- Export works for long theme names.
- Mobile landing page CTA remains visible.
- Activation event fires after first successful analysis.

Launch decision example:
"Go with known issues" if core upload, analysis, export, and payment work, but secondary SEO pages and advanced analytics are incomplete.

No-go example:
"No-go" if analysis can fail silently or paid users do not receive paid access after checkout.
