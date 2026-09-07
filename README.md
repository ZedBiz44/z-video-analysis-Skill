# z-video-analysis Skill

ZedBiz's reusable workflow for understanding videos and video-led webpages. It separates spoken and visible evidence from presenter claims, adds useful timestamps, reports limits honestly, and routes creative or still-graphic follow-up to the correct companion skill.

## Source of Truth

- Skill: [`SKILL.md`](SKILL.md)
- Live Gemini MCP service and deployment files: [ZedBiz OpenClaw infrastructure repository](https://github.com/ZedBiz44/ZedBiz-openclaw-ai-agents-vps1-vps2)
- Build and pilot record: [GitHub issue 1](https://github.com/ZedBiz44/z-video-analysis-Skill/issues/1)
- Human operating guide: stored in the ZedBiz Notion Skills database

## Companion Skills

- [z-video-critique](https://github.com/ZedBiz44/z-video-critique-Skill) owns creative-quality and readiness judgments.
- [z-graphic-production](https://github.com/ZedBiz44/z-graphic-production-Skill) owns requested still-graphic creation, export, storage, and delivery.

## Structure

- `SKILL.md` contains the portable operating workflow.
- `references/` contains source routing, output patterns, visual checks, browser use, companion handoffs, and the current OpenClaw mapping.
- `tests/` contains trigger, boundary, safety, and companion test prompts.
- `governance/` contains the ZedBiz implementation, security, and rollback rules.
- `tracking/` contains dated finite rollout evidence after live testing.

