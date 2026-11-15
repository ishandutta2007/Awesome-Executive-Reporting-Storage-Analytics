# Awesome-Executive-Reporting-Storage-Analytics

## Top Executive Reporting & Storage Analytics Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Backup Infrastructure Reporting, Capacity Forecasting & Self-Hosted BI Dashboards*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Executive Reporting & Storage Analytics**. These tools help IT and backup administrators monitor storage consumption, track backup job health, forecast capacity needs, and generate executive-ready reports across hybrid and multi-cloud environments—covering everything from native backup analytics consoles to general-purpose BI platforms that query infrastructure data.

**Examples** include Druva Analytics, Veeam ONE, Commvault Command Center, Cohesity Analytics, Rubrik Security Cloud, Apache Superset, Metabase, and Grafana (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted BI, open-source infrastructure dashboards, and community-driven storage analytics—ideal for organizations seeking data sovereignty and avoiding per-host or per-TB enterprise reporting licensing. The open-source landscape is genuinely mature: **Apache Superset** provides enterprise-grade dashboards with a SQL editor and no-code chart builder [citation:18], **Metabase** offers the fastest path to storage reporting for non-technical admins [citation:19], and **Grafana** excels at time-series metrics from Prometheus and Loki [citation:20].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Company Size (Revenue/Valuation) | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|----------------------------------|-------------|-------------------|--------------------------|
| **[Rubrik Security Cloud](https://www.rubrik.com/)** | Revenue: **$1.32B** (FY Jan 2026); Market Cap: **~$18B** [citation:5][citation:15] | Cyber resilience platform with reporting on workload metrics including storage usage, compliance status, SLA assignment, and backup activity. API-driven dashboards integrate with Grafana via community plugins. | Quote-only (enterprise contract) | No free tier; trial via sales |
| **[Veeam ONE](https://www.veeam.com/)** | Valuation: **~$15B** (Dec 2024); ARR: **$2B+** (June 2026) [citation:2][citation:12] | Monitoring and analytics suite with 340+ prebuilt alarms, 150+ reports, capacity planning for backup storage, chargeback billing, and ransomware anomaly alerts. | Quote-only (bundled with Veeam ecosystem) | **Free (Community Edition)**: limited monitoring for up to 10 workloads |
| **[Cohesity Analytics](https://www.cohesity.com/)** | Valuation: **$5–10B**; Revenue: **$1–5B** [citation:4][citation:14] | Unified IT analytics with dashboards for backup/storage insights, predictive capacity planning, SLA/RTO/RPO compliance, and chargeback/showback. Cohesity Copilot for natural-language report generation. | Quote-only (enterprise contract) | No free tier; trial via sales |
| **[Commvault Command Center](https://www.commvault.com/)** | Revenue: **$1.10B ARR** (Q3 CY2026); Market Cap: **~$6.95B** [citation:3] | Centralized reporting with predefined reports for backup/restore summaries, SLA compliance, storage utilization, and audit trails. Automated scheduled report delivery across multi-CommCell environments. | Quote-only (enterprise contract) | No free tier; trial via sales |
| **[Druva Analytics](https://www.druva.com/)** | Valuation: **$1–2.5B**; Revenue: **$100–500M** [citation:1] | Cloud platform reports covering backup/restore operations, storage consumption, license usage, and workload health. Supports granular insights, chargeback analysis, and up to two years of historical trend data. | Quote-only (per TB/month after deduplication) | No free tier; trial via sales |
| **[Datadog Dashboards](https://www.datadoghq.com/)** | Revenue: **$3.43B** (FY2025); ARR: **$3.6B+** [citation:6] | General-purpose observability platform with infrastructure monitoring, log management, and custom dashboards. Can ingest backup telemetry via integrations for unified monitoring alongside application metrics. | Infrastructure: **$15/host/month** (annual); APM: $31/host/month | **Free infrastructure plan**: 5 hosts, 1-day retention; no free APM |
| **[Tableau Cloud](https://www.tableau.com/)** | Valuation: **$16B** (market cap); Revenue: **$2.10B** [citation:7] | Visual analytics platform for building custom backup capacity and compliance dashboards from extracted CSV/API data. Commonly paired with backup vendor exports for executive-level reporting. | Quote-only (per-user Creator/Explorer/Viewer) | **Tableau Public**: free for publicly shared dashboards; 14-day trial |
| **[Microsoft Power BI](https://powerbi.microsoft.com/)** | Bundled with Microsoft (M365/ Azure ecosystem); no standalone valuation disclosed | Business analytics platform for interactive backup reporting dashboards from Commvault, Veeam, or custom data sources. Supports scheduled refresh and row-level security for departmental chargeback views. | Pro: **$14/user/month**; Premium Per User: $24/user/month | **Free**: Power BI Desktop (authoring only); 60-day trial |
| **[Looker (Google Cloud)](https://looker.com/)** | Acquired by Google; Valuation: **$2.5–5B** (last recorded); Revenue: **$100–500M** [citation:9] | Enterprise BI with LookML semantic modeling. Governed self-service with consistent metric definitions—useful for standardizing storage KPIs across IT, finance, and operations. | Quote-only (enterprise contract) | No free tier; trial via Google Cloud |
| **[Domo](https://www.domo.com/)** | Market Cap: **$145–289M**; Revenue: **$315–319M** [citation:16][citation:22][citation:28] | Cloud BI platform with drag-and-drop dashboard builder and pre-built connectors. Positioned for business users with AI assistance and embedded analytics. | Quote-only (consumption-based) | No free tier; demo via sales |
| **[Sisense](https://www.sisense.com/)** | Valuation: **$1–2.5B**; Revenue: **$184.8M** (GetLatka) or **$500M–$1B** (LeadIQ est.) [citation:17][citation:23][citation:29] | BI platform focused on embedded analytics for product teams. Allows embedding backup dashboards directly into internal or customer-facing applications with white-labeling. | Quote-only (custom enterprise pricing) | No free tier; demo via sales |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Apache Superset](https://github.com/apache/superset)** | [![Stars](https://img.shields.io/github/stars/apache/superset?style=social&color=white)](https://github.com/apache/superset/stargazers) | **The most enterprise-ready open-source BI platform for storage analytics.** Apache-2.0. **~70,975 GitHub stars, 1,212 contributors, 15,780 commits** [citation:18]. **No-code chart builder plus SQL Editor** for advanced storage queries. **40+ chart types** and a lightweight semantic layer for defining storage KPIs. **Configurable caching** eases load on production backup databases. **Extensible security roles** and API for customization. **Trade-off**: operational complexity—production deployments typically require Docker, Celery, and Python expertise; no native embedded analytics [citation:27]. **Best for organizations with engineering capacity** wanting a self-hosted BI platform that can query backup data directly without per-user licensing. |
| **[Metabase](https://github.com/metabase/metabase)** | [![Stars](https://img.shields.io/github/stars/metabase/metabase?style=social&color=white)](https://github.com/metabase/metabase/stargazers) | **The fastest path to backup reporting for business users.** Open-source edition is **free with unlimited users** [citation:27]. **~49,830 GitHub stars, 429 contributors** [citation:19]. **Question builder lets non-technical admins build storage reports without SQL**. **20+ database connectors** including PostgreSQL, MySQL, BigQuery, Snowflake, and Redshift. **Trade-off**: **white-labeling and embedded analytics require the Pro plan at $575/month**; open-source and Starter tiers display Metabase branding [citation:27]. **Best for teams wanting internal storage dashboards quickly** without engineering involvement. |
| **[Grafana](https://github.com/grafana/grafana)** | [![Stars](https://img.shields.io/github/stars/grafana/grafana?style=social&color=white)](https://github.com/grafana/grafana/stargazers) | **The standard for time-series infrastructure and observability dashboards.** **~67,410–72,674 GitHub stars, 2,657 contributors** [citation:20][citation:26]. **Designed for metrics from Prometheus, Loki, InfluxDB, and OpenTelemetry**—ideal for backup job success rates, storage growth trends, and alerting. **Trade-off**: **not designed for self-service business intelligence**—non-technical users find it harder than Metabase, and it lacks a drag-and-drop report builder for SQL-heavy relational queries [citation:27]. **Best for engineering teams** wanting storage growth and backup health monitoring alongside existing observability infrastructure. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Lightdash](https://github.com/lightdash/lightdash)** | [![Stars](https://img.shields.io/github/stars/lightdash/lightdash?style=social&color=white)](https://github.com/lightdash/lightdash/stargazers) | **BI platform built for dbt.** Turns existing dbt models into dashboards without SQL—uses dbt YAML as the semantic layer. **Best for teams already modeling backup data in dbt** and wanting governed storage metrics as code [citation:21]. |

**Frameworks for building custom systems**: Choose **Apache Superset** for enterprise-grade storage dashboards with SQL flexibility and no per-user licensing [citation:18], **Metabase** for the fastest path to internal storage reporting with non-technical users [citation:19][citation:27], or **Grafana** for time-series backup health monitoring alongside existing observability [citation:20]. **Lightdash** fills the gap for dbt-native teams wanting storage metrics as code [citation:21].

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Executive reporting and storage analytics platforms handle sensitive infrastructure metrics and potentially business-critical capacity data; enforce role-based access and audit logging for dashboard queries.
- **Company size data reflects publicly available financials and estimates.** Private companies (Druva, Cohesity, Sisense) have estimated valuations and revenue ranges from Dealroom and other sources; public companies (Rubrik, Commvault, Domo) have reported financials. **Domo's market cap has declined significantly** (~$145–289M) despite ~$315M revenue, reflecting market skepticism about its growth trajectory [citation:16][citation:28].
- **Open-source BI has different trade-offs.** **Apache Superset** is the most capable but requires operational expertise (Docker, Celery, Python) [citation:27]. **Metabase** is the easiest to adopt but gates embedded analytics behind the $575/month Pro plan [citation:27]. **Grafana** excels at time-series monitoring but is not a self-service BI tool for business users [citation:27]. **Validate whether you need SQL flexibility (Superset), non-technical accessibility (Metabase), or time-series monitoring (Grafana)** before committing.

---

**Made for backup administrators, IT operations teams, and executives seeking storage insights.**  
Let's make executive reporting and storage analytics more open, observable, and actionable.
