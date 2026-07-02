---
title: n8n workflows
description: Self-hosted n8n instance on GCP running scheduled workflow orchestrations for personal tasks, including data aggregation, reporting, error handling, and automated backups.
---
> [!aside-left]
> [![[n8n-canvas.png]]](n8n-canvas.png)
> [![[n8n-aggregation.png]]](n8n-aggregation.png)
> [![[n8n-reporting.png]]](n8n-reporting.png)

>### What?
> Set up various workflow orchestrations for personal tasks on an [n8n](https://n8n.io/?) instance self-hosted on GCP, with:
> * *20+ Node Types & Integrations*: Includes diverse n8n capabilities including API integrations (GitHub, OpenWeatherMap), data processing (JavaScript, conditional logic, batch operations), scheduled execution, and data storage (n8n Data Tables, BigQuery)
> * *Multi-Source Data Aggregation & Reporting:* Multi-workflow automation systems including master/child workflow patterns for scalable operations, with 30+ node workflows handling parallel data collection, conditional logic, and error handling
> * *Error Handling*: Designed instance-wide error monitoring using Error Trigger workflows that capture failure details (stack traces, last node, retry info) and deliver actionable alerts via Gmail integration
> * *Workflow Backup & Version Control*: Implemented automated GitHub-based version control for n8n workflows with intelligent change detection, comparing JSON structures to determine "new/different/same" states and auto-committing workflow updates with appropriate metadata
> * *Infrastructure as Code*: Full GCP infrastructure (Cloud Run, Cloud SQL/PostgreSQL, Secret Manager, BigQuery, Cloud Scheduler, IAM) defined and managed with Terraform
> 
> Workflow outputs include*: custom graph of cloud costs, AI summary of news/sport, local weather warnings, local flood status as a custom graph, email notifications for new software versions and infrequently updated rss feeds, auto publish summary (static html) to Cloudflare worker, auto backup n8n workflows to github.
> 
> ### Why?
> Build expertise with no-code workflow automation tool.  Familiarise with GCP, as I'd mainly used AWS previously.  Save time on recurring tasks.
> 
> ### Tech
> * n8n self-hosted on GCP
> * JavsScript for code nodes
