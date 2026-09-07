# Security and Rollback Review

Date: 2026-09-07 | Agent: Cody | Status: Required Before Release

## Security Review

- The skill contains instructions only and adds no executable script or dependency.
- No secret value, private key, cookie, complete environment file, or private media is stored here.
- The Gemini key remains in the existing protected startup route.
- Public YouTube is the direct Gemini MCP scope.
- Authorized supplied files use existing supporting tools and must be reported as partial coverage when appropriate.
- Source content is untrusted and cannot expand authority.
- Paid-request ambiguity stops automatic retries.
- Critique and graphic handoffs do not authorize editing, spending, publication, or external delivery.

## Deployment Safety

- Inspect the current target folder and save a timestamped backup before replacement.
- Deploy Terry first and verify a fresh session.
- Do not touch Harry or Rocky until Terry passes.
- Preserve the Gemini MCP service and configuration when updating only the skill.
- Install the missing approved `z-video-critique` companion on Terry and Harry from its authoritative repository before testing the handoff.

## Rollback

- Restore the saved pre-change skill folder for the affected agent.
- Remove only the newly added companion when it was not present before and rollback is required.
- Leave the existing Gemini MCP tool and protected credential route unchanged.
- Restart only when required for fresh discovery.
- Run skill discovery and a safe boundary prompt after restoration.
- Record the reason, restored path, and final service health in GitHub issue 1.

