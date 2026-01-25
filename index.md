---
title: Ross Arnold — Portfolio
---
Samples of personal projects for [Ross Arnold](https://www.linkedin.com/in/rarnold/).  Does not include any paid/work projects.

## birdbird
> [!aside-left]
> [![[index-1.png]]](index-1.png)
> [![[index-2.png]]](index-2.png)

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
> Set up various workflow automations for personal tasks on an [n8n](https://n8n.io/?) instance self-hosted on GCP, including:
> * AI summary of news/sport
> * local weather warnings
> * local flood status as a custom graph
> * custom graph of cloud costs
> * email notifications for new software versions and infrequently updated rss feeds
> * auto backup n8n workflows to github
> [Sample daily report](https://n8n-daily-report.rossarn.workers.dev/).
> 
> ### Why?
> Familiarise with no-code workflow automation tool.  Familiarise with GCP, as I'd mainly used AWS previously.  Save time on recurring tasks.
> 
> ### Tech
> * n8n self-hosted on GCP


## NewsChart

>[!note]
>### What?
> Set up some workflow automations for personal tasks, for example:
> * summarise news/sport
> * local weather/flood warnings
> * simplified graph of cloud costs
> * email notifications for new software versions
> 
> ### Why?
> Stay sharp with Java / Spring Boot / ReactJS.
> 
> ### Tech
> * Java 21 / Spring Boot 4 / React / Typescript




