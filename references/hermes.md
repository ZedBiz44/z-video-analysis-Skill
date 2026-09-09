# Hermes Runtime Reference

Use this reference when the active agent runs on Hermes. Keep the shared analysis decisions and output contract unchanged, but use Hermes-native skill, media, browser, and MCP discovery.

## Choose the Available Route

- Run `hermes skills list` to confirm this skill and any media helper are enabled.
- Run `hermes mcp list` before promising a named MCP tool.
- Prefer an approved Gemini video MCP when it is configured and passes `hermes mcp test`.
- When no direct full-video tool is available, use the enabled YouTube-content, transcript, media, browser, and vision routes that fit the source.
- Use `ffprobe` for technical media facts and `ffmpeg` for authorized audio, clip, or frame extraction when those commands are present.
- Use the Hermes browser or computer-use capability only when the task needs rendered page state or interaction.

Do not copy OpenClaw tool names, service commands, paths, or restart instructions into a Hermes task.

## Report Coverage Honestly

- Direct audio-and-visual video analysis may support complete source coverage when the tool actually processes the full source.
- A transcript, metadata, page text, thumbnail, or sampled frames provide partial coverage unless the request only needs those parts.
- Name the actual tools used and the portion inspected.
- If a required route is unavailable, provide the useful partial result and state the missing capability.

## Discovery and Behaviour Check

- Confirm `z-video-analysis` is enabled in `hermes skills list`.
- Confirm `z-video-critique` is enabled before promising a creative-review handoff.
- Run a fresh Hermes one-shot or session with a representative request.
- For analysis, confirm the agent selects an available source route and labels its coverage.
- For critique, confirm the agent requests a complete playable video when none was supplied and does not claim a review occurred.

## Current ZedBiz Deployment Shape

Ruby's local skills are mounted into the Hermes runtime under `/opt/data/skills/`. Treat the maintained host source and its mounted runtime copy as one deployment, not two separate skill installations. Recheck this path before future rollouts.

## Rollback

Before replacing an existing skill, save its current folder under the approved Hermes backup location. If discovery or behaviour fails, restore that folder, confirm ownership remains with the Hermes runtime user, and repeat the native skill-list and fresh-session checks.
