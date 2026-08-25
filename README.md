# BasketBall Hero — WebGL

Unity WebGL build of BasketBall Hero, hosted via GitHub Pages.

- **Orientation:** landscape. The canvas is always letterboxed to 16:9, so the
  composition is identical on every screen. On touch devices held in portrait a
  "rotate your device" overlay covers the game.
- **Template:** `BasketBallHeroLandscape` (lives in the Unity project under
  `Assets/WebGLTemplates/`).

## Note on the build files

`Build/` is served **uncompressed** (`.data`, `.wasm`, `.framework.js`).

GitHub Pages cannot send the `Content-Encoding: gzip` header that Unity's
compressed `.gz` output requires, so a gzip-compressed build fails to load here
with *"Unable to parse Build/build.framework.js.gz"*.

The smaller alternative is to rebuild in Unity with
**Player Settings → Publishing Settings → Decompression Fallback** enabled,
which produces self-decompressing `.unityweb` files (~19 MB instead of ~48 MB).
