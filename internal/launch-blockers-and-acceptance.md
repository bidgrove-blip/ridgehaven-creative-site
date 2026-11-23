# Ridgehaven Creative — Launch blockers and acceptance checks

Updated 2026-11-23. This file is an internal checklist, not customer-facing marketing.

## Deployment: high priority
Render service srv-dbvrk5ajnfac7387f0d0, repo bidgrove-blip/ridgehaven-creative-site, branch main, autoDeploy=yes, trigger=commit.

Observed: Render deployment history shows latest live deploy at commit fd717616219ce02fdf128288982ff652afeef8ef on Nov 22. All post-initial deployment events show manual=true. GitHub commits after that include the FAQ fix, contact navigation correction, production QA standard, Canva audit, and onboarding claim correction. No corresponding Render deploy events were observed when checked Nov 23.

Hypothesis only: webhook/GitHub app delivery or integration problem. Do not assert root cause without checking GitHub app permissions, repository webhook deliveries, Render connected GitHub account, ignored paths, and branch configuration.

Actions to investigate:
1. In Render dashboard, inspect connected GitHub repository and deploy settings for this exact service.
2. Inspect GitHub repository Settings > Webhooks or installed Render GitHub app and recent delivery attempts, if authorized and accessible.
3. Compare latest GitHub main commit with Render latest deploy commit.
4. After repairing event delivery, push a harmless test commit and verify a new **automatic** deployment event.
5. Verify live HTML on ridgehavencreative.com, including Contact mailto and onboarding FAQ.
6. Do not describe a GitHub commit as live until verified on the public site.

## Customer onboarding
- Verify founding and standard Stripe checkout products, recurring billing amounts, and terms without making a live charge.
- Confirm post-checkout redirect in Stripe settings; until verified, website must provide direct getting-started link.
- Test first-request email instructions and reply handling.
- Confirm cancellation/billing portal setup before promising self-service cancellation.

## Production formats
- PowerPoint: existing sample decks; inspect actual .pptx editability and visual export.
- Canva: pilot DAHbvlXydEY exists but failed first content QA; fix after preview and approval.
- Google Slides: connection available; do not advertise until native-editability and layout checks pass.
- PDF: confirm fonts, charts, links, and no clipping.

## Outreach
- Do not present fictional portfolio samples as paid client work.
- Build segmented, verified prospect lists and personalized outreach. Record permission, contact source, opt-out, and response status.
- Do not claim actual customers, delivery metrics, client ROI, or published results without evidence.
