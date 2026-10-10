# Creative Studio

Live: https://gusthecreative-ops.github.io/sticker-gif-studio/

Make transparent animated GIF stickers right in your browser. Everything is processed on your device.

- **Video Key**: green-screen video → transparent GIF/PNG frames. Includes auto key detection, despill, custom backgrounds, and Standard/High/Max quality.
- **Sticker Maker**: photo → AI background removal on your device (IMG.LY model, about 50 MB, downloaded once from a CDN), with a green/solid colour key fallback and an erase/restore brush. Add a white outline and drop shadow, then pick from 10 animation presets (Bounce, Wiggle, Spin, Pulse, Float, Shake, Pop-in, Jelly, Swing, Heartbeat).
- **Remove BG**: full-resolution still-image cutout (AI or colour key, Solid-subject control, Erase/Restore brush with Undo). Photos are capped at 2048 px on the long side for iPhone memory. Includes a before/after slider; background options are transparent, colour, blur or image. Export as PNG (soft alpha) or JPG, and send the cutout to Sticker Maker.
- **AR Camera**: front camera with on-device MediaPipe face tracking (GPU, falling back to CPU). Masks: Detective, Cat, Robot, Alien, Frog or your own image, with mouth and blinks animated. Accessories: hat, sunglasses, mustache. Selfie background removal (transparent, green or image) and 2–6 s GIF recording.
- **Bring to Life**: image-tracking AR (MindAR; the target is compiled on your device). Overlay a video (green screen keyed live), a Library GIF/sticker or your Video Key project on a picture, flat or popping out, with tilt, scale and offset controls. It fades out when tracking is lost. Experiences are saved on the device, and you can record a GIF of the AR view.
- **Library**: every export (GIF, PNG, JPG) is saved in this browser (IndexedDB). Clearing Safari website data removes it, so use Save to Files for anything you want to keep.
- Save to Photos / Copy / Save to Files / Share. Add to Home Screen for the app icon.
