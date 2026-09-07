# Website Interaction

OpenClaw already supplies the Website-Interaction foundation through its browser plugin, Chromium, and bundled `browser-automation` skill. Do not ask for a duplicate package.

## Use Web Search or Page Extraction For

- finding relevant public pages;
- reading accessible page text;
- collecting current outside sources; and
- quickly summarizing non-interactive material.

Tavily, Perplexity, or another configured search provider may fill this role. They do not replace a real browser.

## Use the Real Browser For

- JavaScript-rendered pages;
- clicking, typing, scrolling, selecting, or expanding controls;
- maintaining an authorized browser session;
- screenshots and page-state snapshots;
- console messages and page errors;
- request and response inspection; and
- traces that help explain the interaction sequence.

Use the bundled browser guidance for stable tabs, snapshots, changed references, and manual login, two-factor, or CAPTCHA stops.

## Separate Page and Video Evidence

- Label what came from the video.
- Label what came from the surrounding webpage.
- Do not claim the webpage proves a statement made only in the video.
- Do not claim a browser screenshot proves continuous video behaviour.

## Formal Audit Boundary

The existing browser can collect useful diagnostic facts. A formal performance or accessibility audit may also require the separately approved Lighthouse, axe, repeated-test, manual-review, and reporting method. State when that deeper pack is unavailable.

