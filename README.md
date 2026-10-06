# TQM Analytics Hub

The Hub provides the five existing dashboard destinations, including the COO Area Incidents Dashboard.

## Incident source and access

Incident data and KPIs are viewed in the existing authenticated Power BI report (`14f20afc-1d09-4fc1-bd6c-0e7b41ed69de`). The original dashboard configuration is preserved.

No incident records or incident KPI values are bundled in the public Hub. Incident rows remain excluded from `kpi-summary.csv`; the Hub rejects incident CSV rows if reintroduced. Its incident scorecard tab opens the authenticated report.

The online Knowledge Base has been removed. The separately downloaded offline incident analysis tool remains independent of this repository; local workbooks and exports must not be committed here.

## Deployment

Pushes to `main` trigger `.github/workflows/jekyll-gh-pages.yml`. The read-only Hub verification workflow checks the dashboard destinations and incident source safeguards. Power BI sign-in is required to view report content.
