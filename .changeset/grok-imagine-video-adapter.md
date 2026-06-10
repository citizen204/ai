---
'@tanstack/ai-grok': minor
---

Add a `grokVideo` adapter for the grok-imagine video models (`grok-imagine-video`, `grok-imagine-video-1.5-preview`) via xAI's Imagine API. Follows the experimental `generateVideo()` jobs/polling architecture: `createVideoJob` posts to `/v1/videos/generations`, status polling reads `/v1/videos/{request_id}`, and the completed result carries the hosted video URL plus usage (`unitsBilled` seconds and exact `cost` in USD). Sizing uses the aspect-ratio template consistent with the grok-imagine image models (`size: '16:9_720p'` → `aspect_ratio` / `resolution`), durations are 1–15 integer seconds, and image-to-video starting frames can be passed via `modelOptions.image: { url }`.
