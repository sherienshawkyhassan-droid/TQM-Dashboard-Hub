# TQM Analytics Hub

The Hub retains the five existing dashboard destinations and adds a separate TQM Incidents Knowledge Base card linking to `incident-intelligence.html`.

## Incident source and access

The sole incident-data surface is the existing authenticated Power BI report:
- Report: `14f20afc-1d09-4fc1-bd6c-0e7b41ed69de`
- Tenant: `7a09d8f3-71ea-494a-b504-36d7ece273f3`
- Expected semantic model from prior project context: `721b695a-b728-4cd9-8cd5-00888c666a5a` (binding must be verified in Power BI by an authorized user).

No incident records or incident KPI values are bundled with the knowledge base. Incident rows were removed from `kpi-summary.csv`; the Hub also rejects incident CSV rows if later reintroduced. Its incident scorecard tab opens the authenticated report.

The original COO Area Incidents Dashboard configuration is preserved. The knowledge workspace uses the same report with the filter pane enabled.

## Current capability boundary

Search, slicing and analysis take place inside the existing Power BI report using its available visuals and fields. The Knowledge Assistant gives navigation guidance only. It does not query the semantic model, retrieve records, perform RCA, calculate recurrence or update actions. Dedicated report pages have not been asserted or fabricated.

A static GitHub Pages secure-embed iframe does not provide the parent page with a Power BI access token or model-query capability. Direct model search/chat requires an approved Microsoft Entra application integration, delegated Power BI permissions, verified model schema, and appropriate tenant settings. Do not add credentials, browser tokens, exports or old incident datasets to this public repository.

## Deployment

Pushes to `main` trigger `.github/workflows/jekyll-gh-pages.yml`. Verify the Pages deployment and both the Hub card and the preserved incident dashboard after changes. Authorized Power BI sign-in is required to verify report content and model binding.
