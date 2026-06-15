---
title: Ross Arnold — Portfolio
---
Samples of personal projects for [Ross Arnold](https://www.linkedin.com/in/rarnold/).  Does not include any paid/work projects.

## Labro

> [!aside-left]
> [![[index-7.png|Screenshot from Labro: mobile layout showing recent agent tasks with project, source, and outcome indicators]]](https://labro.rossarnold.uk/)
> [![[index-8.png|Screenshot from Labro: full dashboard table view showing runs with agent, model, cost, turns, and summary columns]]](https://labro.rossarnold.uk/)

>### What?
> See a sample live metrics dashboard at [labro.rossarnold.uk](https://labro.rossarnold.uk/) and source/docs at [github.com/rssrn/labro](https://github.com/rssrn/labro).
> 
> An orchestrator that runs AI coding agents on a schedule - picking tasks from GitHub 
> Issues, prompting an agent, and recording the result directly in the GitHub issue.
> Configurable: define which labels or conditions trigger pickup, the agent prompt, agent permissions 
> (comment, open a PR, merge), and how often to run.
> 
> I use Labro conservatively, with human review in the loop.  But it's flexible enough to adapt to your style
> if you prefer more autonomy: just add merge or deploy permissions and configure your prompts accordingly.
> 
> Supports Claude Code, OpenCode, and Codex as agent backends.  Labro is broadly similar to commercial features emerging in 2026
> such as [Claude's Routine Runs](https://code.claude.com/docs/en/routines),
> [Copilot Cloud Agent](https://github.blog/changelog/2026-05-13-start-copilot-cloud-agent-tasks-via-the-rest-api/) and
> [Cursor Cloud Agent](https://cursor.com/docs/cloud-agent), but has no dependency on these features.
>
> ### Why?
> Labro's configurable asynchronous use of coding agents supports:
> * Produce AI-assisted output in a measured, prioritised stream of work to maintain a reviewable cadence.  Automatically picking all possible work alongside a human-in-the-loop policy can create a bottleneck on the human side.
> * Get occasional suggestions using a [random perspective](https://github.com/rssrn/labro/blob/main/perspectives.toml) to shake up your project!
> * Let AI subscriptions or headless-only subscription budget (example: [Agent SDK Credit](https://support.claude.com/en/articles/15036540-use-the-claude-agent-sdk-with-your-claude-plan)) keep working 24/7
> * Low-friction way to use free or free-tier tokens across multiple providers to monitor and progress your project
> * Configure an appropriate model (=cost) per task complexity - leverage free models for simpler tasks
> * Fall back to alternative models if your first choice is not available or budget exceeded.  Or just retry later automatically.
>
> ### Tech
> * Python 3.12 / Docker / SQLite / GitHub Actions or system cron
> * Agent backends: Claude Code CLI, OpenCode, Codex
> * Metrics dashboard: React 18 + Vite + TypeScript / sql.js (SQLite WASM) / Apache ECharts / Cloudflare R2

## NewsChart
> [!aside-left]
> [![[index.png]]](https://newschart.rossarnold.uk/)
> [![[index-6.png]]](https://newschart.rossarnold.uk/)


>### What?
> See it in action at [NewsChart](https://newschart.rossarnold.uk/).  Each day, several leading AI models (Gemini, Perplexity, ChatGPT) are asked the same question — "what are today's top three international news stories?" — and their answers are plotted on a world map.  Switch between models to see which stories each chose, where they think the action is, and how their editorial judgements compare against each other and a New York Times baseline.  A date timeline lets you look back at how stories broke and where models agreed or diverged.
> 
> ### Why?
> Explore AI / LLM model integrations.  Stay sharp with Java, TypeScript, and end-to-end delivery and support of a live system.  Also a deliberate exercise in agentic AI-assisted development: the Java/Spring Boot backend was written directly, while the React frontend was built by providing close direction to [Claude Code](https://claude.ai/) — combining hands-on backend engineering with AI-assisted frontend delivery under the same technical oversight.  More detail in [[NewsChart - Human Contribution Summary]].
> 
> ### Tech
> * Java 21 / Spring Boot 4 / Spring AI / React 18 / Typescript / MongoDB / OpenRouter
> 
> See [NewsChart credits](https://newschart.rossarnold.uk/credits) for full list of tech and dependencies.

## birdbird
> [!aside-left]
> [![[index-1.png|Screenshot from birdbird: histogram of bird vocalisations detected, each with confidence %]]](https://birdbird.rossarnold.uk/)
> [![[index-2.png|Screenshot from birdbird: images and video player showing garden birds]]](https://birdbird.rossarnold.uk/)

>
>### What?
> See it in action at [birdbird](https://birdbird.rossarnold.uk/).  Process motion-captured clips from a bird feeder cam, present results on the web.  Includes species detection (audio and video).  
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
> See [birdbird credits](https://birdbird.rossarn.workers.dev/credits) for full list of tech and dependencies.
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
