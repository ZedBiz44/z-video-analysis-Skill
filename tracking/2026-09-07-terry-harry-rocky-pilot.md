# Terry, Harry, and Rocky Pilot

Date: 2026-09-07 | Agent: Cody | Status: Passed

## Release

- Authoritative repository: https://github.com/ZedBiz44/z-video-analysis-Skill
- Source release used for deployment: `66f957e283f7166d22e46ffd6b4062282cc00979`
- Package SHA-256: `D3D4CB211D28D88556BE10CE868939A5CDDFCE84E041E9E4885594FFA6B02607`
- Deployed `SKILL.md` SHA-256 on all three agents: `6ab36a45ac97eb153dfe67ec53fe71832fd93cce47043270bd0590b9b82d90f7`
- Z AI Skill Developer validation: passed from a correctly named `z-video-analysis` staging folder.
- Secret scan and reference checks: passed.

## Companion Skills

- `z-graphic-production` was already present and ready on Terry, Harry, and Rocky.
- `z-video-critique` was already present on Rocky.
- The authoritative `z-video-critique` package was installed on Terry and Harry because it was missing.
- Companion `SKILL.md` SHA-256 on all three agents: `b33b0312ac5019deec352563e747f01f7c92bd0bafab6a986f953c8cd993d968`.

## Live Test

All three agents analyzed https://www.youtube.com/watch?v=eylReF4JPT0 in a fresh named test session.

The prompt required each agent to return the main business lesson, one important on-screen detail with a timestamp, one unverified presenter claim, remaining uncertainty, the coverage label, and the correct companion handoffs. It also told the agent not to run a critique, create a graphic, or perform an outside fact-check.

- Terry: passed. Gemini analyzed the full 17:31 video with `gemini-3.8-flash`. The agent reported complete source coverage and did not run either companion task.
- Harry: passed. Gemini analyzed the full 17:30 video with `gemini-3.8-flash`. The agent reported complete source coverage and did not run either companion task.
- Rocky: passed. Gemini analyzed the full 17:30 video with `gemini-3.8-flash`. A follow-up read reused the completed session result instead of paying for a second analysis.
- Handoff routing passed on all three: creative readiness went to `z-video-critique`; a requested still summary graphic went to `z-graphic-production`.

## Issues and Fixes

- The first Terry deployment command was altered by local PowerShell expansion before reaching Linux. It created two staged folders at the container root but did not replace the live skill. The staged folders were inspected, removed, and the deployment was rerun with a checked shell script.
- Harry's first test launcher did not inherit the existing 1Password service-account route. The launcher was corrected to use Harry's approved startup pattern. No credential was printed or changed.
- Rocky's first SSH wrapper reported an incorrect 1Password runtime path after the agent request had started. The analysis completed in the named session. The result was read back without a second Gemini request. No credential or service configuration was changed.

## Rollback Locations

- Terry: `/home/node/.openclaw/backups/20260907-142209-z-video-analysis-release`
- Harry: `/root/.openclaw-harry/backups/20260907-142615-z-video-analysis-release`
- Rocky: `/home/openclaw/.openclaw/backups/20260907-142615-z-video-analysis-release`

The existing Gemini MCP service, protected key route, and server configuration were left unchanged.
