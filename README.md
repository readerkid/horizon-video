# horizon-video

A single static page that embeds the latest video from **ludovic** ([@lu4ovic](https://www.youtube.com/@lu4ovic)), the author of [Horizon](https://playhorizon.dev/) — Minecraft: Java Edition rewritten in Rust.

- Video: [10,000 people joined my rust minecraft in 36 days](https://www.youtube.com/watch?v=53HgXJqyJtM) — published 9 November 2026
- Site: <https://readerkid.github.io/horizon-video/>

GitHub Pages serves `index.html` from the `main` branch root. No build step, no dependencies.

The player uses `youtube-nocookie.com` plus the `credentialless` iframe attribute, so the embed runs with an empty, throwaway cookie jar and starts signed out instead of picking up the viewer's Google session. `credentialless` is honoured by Chromium browsers 110+; elsewhere the cookie-less domain still applies, and Firefox/Safari block YouTube's third-party cookies anyway.

To point the page at a newer upload, change the video ID in the `<iframe src>` and in the "Watch on YouTube" link, and update the title/date text.
