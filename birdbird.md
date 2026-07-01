---
title: birdbird
---
> [!aside-left]
> [![[birdbird-highlights.png|Screenshot from birdbird: highlights video player with detected species list alongside]]](https://birdbird.rossarnold.uk/)
> [![[birdbird-video-stats.png|Screenshot from birdbird: bar chart of bird species detected from video, each with confidence %]]](https://birdbird.rossarnold.uk/)
> [![[birdbird-audio-stats.png|Screenshot from birdbird: bar chart of bird vocalisations detected from audio, each with confidence %]]](https://birdbird.rossarnold.uk/)
> [![[birdbird-pipeline.png|Diagram from birdbird: how it works, showing the parallel video and audio processing pipelines]]](https://birdbird.rossarnold.uk/)
> [![[birdbird-credits.png|Screenshot from birdbird: credits and acknowledgments page listing models, frameworks, and licenses used]]](https://birdbird.rossarnold.uk/)

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
