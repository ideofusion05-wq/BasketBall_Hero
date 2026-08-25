# BasketBall Hero — WebGL

Unity WebGL build of BasketBall Hero, hosted via GitHub Pages.

- **Orientation:** landscape. The canvas is always letterboxed to 16:9, so the
  composition is identical on every screen. On touch devices held in portrait a
  "rotate your device" overlay covers the game.
- **Template:** `BasketBallHeroLandscape` (lives in the Unity project under
  `Assets/WebGLTemplates/`).

## Build settings this deployment depends on

`Build/` is gzip-compressed (`.unityweb`) with **Decompression Fallback enabled**, so the
payload decompresses in the browser and needs nothing from the server.

Do not turn that setting off for this host. Without it Unity emits `.gz` files that require
the server to send `Content-Encoding: gzip` — a header GitHub Pages does not send — and the
build dies during load with *"Unable to parse Build/build.framework.js.gz"*.

Player Settings → Publishing Settings → Decompression Fallback.
