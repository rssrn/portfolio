---
title: Labro
---
> [!aside-left]
> [![[labro-mobile.png|Screenshot from Labro: mobile layout showing recent agent tasks with project, source, and outcome indicators]]](https://labro.rossarnold.uk/)
> [![[labro-dashboard.png|Screenshot from Labro: full dashboard table view showing runs with agent, model, cost, turns, and summary columns]]](https://labro.rossarnold.uk/)

>### What?
> An orchestrator that runs AI coding agents on a schedule - picking or raising GitHub 
> Issues, prompting an agent, and recording the result directly in the GitHub issue.
> Configurable: define which labels or conditions trigger pickup, the agent prompt, agent permissions 
> (comment, open a PR, merge), and how often to run.
> 
> See a sample live metrics dashboard at [labro.rossarnold.uk](https://labro.rossarnold.uk/) and source/docs at [github.com/rssrn/labro](https://github.com/rssrn/labro).
> 
> I use Labro conservatively, with human review in the loop.  But it's flexible:
> if you prefer more agent autonomy: just add merge or deploy permissions and configure your prompts accordingly.
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
