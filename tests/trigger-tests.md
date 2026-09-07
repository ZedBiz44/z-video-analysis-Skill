# Trigger Tests

Run in a fresh session. Do not tell the test agent which skill is expected.

## Positive

- “Watch this public YouTube tutorial and explain what it teaches, what was shown on screen, and the useful timestamps.”
- “I uploaded a screen recording. Turn the demonstrated process into a clear SOP and tell me which visuals you actually checked.”
- “At what point does the presenter change the setting, and what does the screen show before and after?”
- “Open this support page, inspect the embedded walkthrough, and tell me the exact button path.”

## Paraphrased Positive

- “Learn this video for me and give me the useful business actions.”
- “Pull the procedure out of this demo, including the visible menu labels.”

## Companion Boundaries

- “Is this finished video creatively ready?” must route to `z-video-critique`, not produce an analysis verdict.
- “Analyze what this successful video teaches, then explain why its creative execution works.” must complete analysis, then prepare or perform the critique handoff.
- “Analyze this tutorial, then create a branded summary graphic.” must complete analysis and use `z-graphic-production` only for the requested still asset.
- “Create a thumbnail from this video.” must route to graphic production rather than treating analysis as image creation.

## Negative

- “Edit this video and publish it to YouTube.”
- “Run a full Lighthouse and WCAG audit on this website.”
- “Summarize this ordinary text article.”
- “Download this paid course video without logging in.”

## Failure and Safety

- Private or restricted YouTube link.
- Missing Gemini tool.
- Submitted request times out with unknown provider acceptance.
- Transcript exists but required visual evidence is unavailable.
- Companion skill is missing.

## Required Record

Record the prompt, skill activation, tools used, inspected coverage, result, failures, and correction required.

