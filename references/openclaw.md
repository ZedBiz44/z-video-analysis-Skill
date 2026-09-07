# OpenClaw Runtime Reference

This file maps the portable skill to the current ZedBiz OpenClaw implementation. Recheck changing tool names and runtime behaviour before deployment.

## Current Primary Route

- MCP server: `gemini-video`
- OpenClaw tool: `gemini-video__analyze_youtube_video`
- Current accepted input: one public HTTPS YouTube URL and an optional business question
- Current provider model: returned by the tool at runtime; do not hard-code it in the answer
- Credential environment name: `GEMINI_API_KEY`
- Secret value: injected through the approved protected startup route; never print or request it
- Provider request: `store: false`

The MCP service source, tests, and deployment scripts currently live in the ZedBiz OpenClaw infrastructure repository. This dedicated skill repository owns the reusable analysis instructions.

## Supporting Routes

Discover the active names before use:

- `yt-dlp` for authorized public retrieval only when direct analysis cannot consume the source;
- `ffmpeg` for audio, clip, and exact-frame extraction;
- `ffprobe` for technical media facts;
- OpenAI Whisper for transcription fallback;
- Video Frame Skill and an approved vision route for visual evidence;
- the OpenClaw browser and bundled `browser-automation` skill for interactive webpages; and
- Tavily or Perplexity for search and page extraction where configured.

## Discovery Check

- Run `openclaw skills list` in the agent's real runtime and confirm `z-video-analysis` is eligible.
- Run the current MCP probe and confirm `gemini-video__analyze_youtube_video` appears with no diagnostics.
- Confirm companion availability before promising a handoff.
- Use a fresh agent session for behaviour tests so cached skill instructions do not hide discovery problems.

## Current Deployment Shapes

- VPS1 Docker agents commonly use `/home/node/.openclaw/workspace/skills/` inside the agent container.
- VPS2 native agents use the active agent state directory, such as `/root/.openclaw-harry/workspace/skills/` for Harry.
- VPS4 Rocky uses `/home/openclaw/.openclaw/workspace/skills/` under the `openclaw` runtime user.

These are current ZedBiz implementation paths, not portable core rules. Verify before another deployment.

## Rollback

Before replacement, save the existing skill folder in the runtime's approved backup location. If the new skill causes discovery or behaviour failure, restore the saved folder, preserve the Gemini MCP configuration, restart only when the platform requires it, and repeat the read-only discovery check.

