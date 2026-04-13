---
title: Ross Arnold — Portfolio
---
Samples of personal projects for [Ross Arnold](https://www.linkedin.com/in/rarnold/).  Does not include any paid/work projects.

## birdbird
> [!aside-left]
> [![[index-1.png|Screenshot from birdbird: histogram of bird vocalisations detected, each with confidence %]]](index-1.png)
> [![[index-2.png|Screenshot from birdbird: images and video player showing garden birds]]](index-2.png)

>
>### What?
> Process motion-captured clips from a bird feeder cam, present results on the web.  Includes species detection (audio and video).  See it in action at [birdbird](https://birdbird.rossarn.workers.dev/).
> 
> ### Why?
> Sharpen my AI-assisted development skills.  Provided close direction, requirements clarity, quality oversight, and design decisions - leveraging [Claude Code](https://claude.ai/ ) for implementation while maintaining full project vision and technical governance.  More detail in [[birdbird - Human Contribution Summary]].
> 
> ### Tech
> * FFmpeg for general processing of input clips
> * ML inference using publicly available pre-trained models:
> 	* Trim input clips to keep segments with birds.   YOLOv8 + COCO dataset.
> 	* Identifies bird vocalisations using BirdNET
> 	* Identifies bird visuals using BioClip (optionally, process on remote GPU)
> * Deploys on Cloudflare Workers and R2.
> 
> See [birdbird credits](https://birdbird.rossarn.workers.dev/credits) for full list of dependencies used.
> 




## n8n workflows

> [!aside-left]
> [![[index-3.png]]](index-3.png)
> [![[index-4.png]]](index-4.png)
> [![[index-5.png]]](index-5.png)

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


## NewsChart
> [!aside-left]
> [![[index.png]]](index.png)


>### What?
> Visualise top news items on a world map.  Includes comparison of different approaches for deciding what is "top", and AI agent assistance.
> 
> ### Why?
> Stay sharp with Java / Spring Boot / ReactJS / Typescript.
> 
> ### Tech
> * Java 21 / Spring Boot 4 / React / Typescript




