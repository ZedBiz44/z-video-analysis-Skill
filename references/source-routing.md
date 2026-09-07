# Source Routing

Choose the smallest approved tool route that can answer the request. Availability must be discovered in the active runtime.

## Public YouTube

- Prefer the approved direct Gemini video tool when available.
- Pass the public HTTPS YouTube URL and the requester's focused business question.
- Ask for full important-source coverage when the request needs a complete analysis.
- Do not download the video when the direct route is sufficient.
- Do not automatically repeat a request when the provider may have accepted it.

## Authorized Supplied Video File

The current ZedBiz Gemini MCP tool accepts public YouTube URLs only. For an authorized local file, use the available supporting routes:

- `ffprobe` for duration, streams, codecs, frame rate, and resolution;
- `ffmpeg` for approved audio, clip, or exact-frame extraction;
- the Video Frame Skill for useful visual samples;
- OpenAI Whisper when a transcript is required and direct transcription is unavailable or unsuitable; and
- an approved vision route to interpret selected frames.

State exactly what was inspected. Transcript plus sampled frames is a partial method and must not be described as continuous full-video visual review.

## Video-Led Webpage

- Use web extraction when readable text alone answers the question.
- Use the real browser when the page requires JavaScript, clicking, scrolling, expanding controls, sign-in, or rendered state inspection.
- If the embedded source resolves to a supported public YouTube URL, route the video itself through the approved direct tool.
- Keep webpage findings separate from video findings.

## Transcript-Only Source

- Summarize the spoken information when the transcript is usable.
- State that the visuals were not checked.
- Do not infer buttons, screen labels, charts, demonstrations, pacing, or visual proof from transcript wording.

## Inaccessible or Restricted Source

- Do not bypass access controls, payment, digital-rights controls, robots rules, or platform restrictions.
- Ask the requester for an authorized playable file or accessible source.
- Return any useful public context separately and label it as outside the unavailable video.

## Current-Fact Check

Use suitable current sources when a video makes time-sensitive claims about prices, laws, products, platform rules, company facts, or performance. Label the result **Checked elsewhere** and cite the supporting source.

