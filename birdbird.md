---
title: birdbird
description: Detects bird species from the audio and video of bird feeder clips, then publishes a highlights reel that jumps straight to the best sighting of each.
---
> [!aside-left]
> [![[birdbird-highlights.png|Screenshot from birdbird: highlights video player, with a list of detected species beside it linking to the best sighting of each]]](https://birdbird.rossarnold.uk/)
> [![[birdbird-video-stats.png|Screenshot from birdbird: bar chart of bird species detected from video, each with confidence %]]](https://birdbird.rossarnold.uk/)
> [![[birdbird-audio-stats.png|Screenshot from birdbird: bar chart of bird vocalisations detected from audio, each with confidence %]]](https://birdbird.rossarnold.uk/)
> [![[birdbird-pipeline.png|Diagram from birdbird: how it works, showing the parallel video and audio processing pipelines]]](https://birdbird.rossarnold.uk/)
> [![[birdbird-credits.png|Screenshot from birdbird: credits and acknowledgments page listing models, frameworks, and licenses used]]](https://birdbird.rossarnold.uk/)

>
>### What?
> See it in action at [birdbird](https://birdbird.rossarnold.uk/).  Detects bird species from both the audio and video of motion-captured bird feeder clips, then publishes the results as an interactive site - a highlights reel that bookmarks the best sighting of each species, so one click jumps straight to it, plus browsable charts of every detection and its confidence.  
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
