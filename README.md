# Creative Studio

Live: https://gusthecreative-ops.github.io/sticker-gif-studio/

Make transparent animated GIF stickers right in your browser. Everything is processed on your device.

- **Video Key**: green-screen video → transparent GIF/PNG frames. Includes auto key detection, despill, custom backgrounds, and Standard/High/Max quality.
- **Sticker Maker**: photo → AI background removal on your device (IMG.LY model, about 50 MB, downloaded once from a CDN), with a green/solid colour key fallback and an erase/restore brush. Add a white outline and drop shadow, then pick from 10 animation presets (Bounce, Wiggle, Spin, Pulse, Float, Shake, Pop-in, Jelly, Swing, Heartbeat).
- **Remove BG**: full-resolution still-image cutout (AI or colour key, Solid-subject control, Erase/Restore brush with Undo). Photos are capped at 2048 px on the long side for iPhone memory. Includes a before/after slider; background options are transparent, colour, blur or image. Export as PNG (soft alpha) or JPG, and send the cutout to Sticker Maker.
- **AR Camera**: front camera with on-device MediaPipe face tracking (GPU, falling back to CPU). Masks: Detective, Cat, Robot, Alien, Frog or your own image, with mouth and blinks animated. Accessories: hat, sunglasses, mustache. Selfie background removal (transparent, green or image) and 2–6 s GIF recording.
- **AR Camera › Animoji** (default): full-screen procedural toon 3D heads (Detective, Cat, Alien, Robot, Frog) driven by MediaPipe's 52 blendshapes and the facial transformation matrix, smoothed with a one-euro filter. Backgrounds: gradient, solid, transparent or camera, with an optional picture-in-picture. Record a 2–10 s GIF (transparent option) or a video with sound (MediaRecorder: MP4 on Safari, WebM elsewhere). GIFs have no sound.
- **AR Camera › Full body**: MediaPipe Pose (lite model) drives either the 2D Detective turnaround (front, 3/4, side and back views picked by body yaw, with a crossfade) or a rigged 3D humanoid (three.js + three-vrm). Upload your own .glb (Mixamo rig) / .vrm or your own turnaround images. Works with the front or rear camera and records to GIF.
- **Bring to Life**: image-tracking AR (MindAR; the target is compiled on your device). Overlay a video (green screen keyed live), a Library GIF/sticker or your Video Key project on a picture, flat or popping out, with tilt, scale and offset controls. It fades out when tracking is lost. Experiences are saved on the device, and you can record a GIF of the AR view.
- **Library**: every export (GIF, PNG, JPG) is saved in this browser (IndexedDB). Clearing Safari website data removes it, so use Save to Files for anything you want to keep.
- Save to Photos / Copy / Save to Files / Share. Add to Home Screen for the app icon.

## Credits & licences
- Sample 3D character **"Robert"** (`models/robert.vrm`) from the **100Avatars R1** collection by Polygonal Mind / ToxSam: **CC0 1.0** (public domain, no attribution required). Source: https://github.com/ToxSam/open-source-avatars
- Detective character art: © the app owner (turnaround sheet supplied by the user).
- Libraries loaded from CDNs at runtime: three.js (MIT), @pixiv/three-vrm (MIT), MediaPipe Tasks Vision (Apache-2.0), @imgly/background-removal (AGPL-3.0; check its licence terms for commercial use), MindAR (MIT).

## Making the Detective a rigged 3D character (GLB)
1. **Image → 3D**: upload the FRONT view (or the turnaround sheet) to an image-to-3D tool (e.g. Meshy, Tripo, Rodin or CSM) and generate a textured model in an **A/T-pose**. Export **GLB** or **FBX**.
2. **Auto-rig in Mixamo** (mixamo.com, free Adobe account): upload the FBX/OBJ, place the chin, wrist, elbow, knee and groin markers, and let it rig. Optionally preview an idle animation.
3. **Download** as FBX (T-pose, no animation is fine) and convert to **GLB** in Blender (File › Import FBX › Export glTF 2.0 binary, +Y up). Keep the `mixamorig:` bone names.
4. In Creative Studio: **AR Camera › Full body › ⬆ Your .glb / .vrm** and pick the file. (Optional: in VRoid Studio or the UniVRM Blender add-on you can also export **.vrm** for the best bone mapping.)
Tips: keep it under ~10 MB and ~30k triangles for iPhone; use one texture of 1024–2048 px.
