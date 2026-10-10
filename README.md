# Sticker GIF Studio

Turn a green-screen video into a transparent animated GIF sticker, entirely in your browser (nothing is uploaded).

**Live app:** https://gusthecreative-ops.github.io/sticker-gif-studio/

- Auto-detects the green, keys it out cleanly (white/grey/black subjects stay solid), removes green spill
- Trim with a timeline, preview over checker/black/white/colour or your own image
- Export a transparent GIF (or bake in a background image), or a ZIP of PNG frames
- Works on iPhone Safari: open the link, tap the Source tool and choose a video. After exporting, use **Save / Share… → Save to Files** to keep transparency.

`index.html` is a single self-contained file (built with Vite + vite-plugin-singlefile; uses gifenc and jszip).

## Features (latest)
- In-app expanded preview with always-visible close button (iOS-safe)
- Save to Photos / Copy / Save to Files / Share result card
- GIF quality: Standard / High / Max with optional dithering (opaque areas only)
- GIF Library: exports auto-saved on this device (IndexedDB). Clearing Safari website data removes it.
