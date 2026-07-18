# Scene Viewer

**A free, open-source tool for rendering simple 3D scenes in the browser.**

Drop in a GLB model, pick a preset or bring your own lighting environment, frame the camera, animate between keyframes, and share or export the result — no install, no account, no build step.

---

## Example

Night scene with a camera move around the example model — [open it live](https://higginsrob.github.io/sceneviewer/?scene=.%2Fscenes%2Fnight.json&targetPosition=0%2C0%2C0&targetScale=1&targetRotation=0%2C0%2C0&cameraPosition=-10.5586%2C3.1715%2C8.7285&zoom=camera&fov=38&shadows=1&target=.%2Fobjects%2Fexample.glb&guide=0&kf=4&keyframes=%5B%7B%22sceneUrl%22%3A%22.%2Fscenes%2Fnight.json%22%2C%22targetUrl%22%3A%22.%2Fobjects%2Fexample.glb%22%2C%22targetPosition%22%3A%5B0%2C0%2C0%5D%2C%22targetScale%22%3A%5B1%2C1%2C1%5D%2C%22targetRotation%22%3A%5B0%2C0%2C0%5D%2C%22cameraPosition%22%3A%5B-6.806582390176324%2C5.684486639046334%2C18.083153215707775%5D%2C%22orbit%22%3A%7B%22distance%22%3A20%2C%22azimuthAngle%22%3A1.930797874522712%2C%22polarAngle%22%3A1.3096221827695107%7D%2C%22fov%22%3A60%2C%22shadows%22%3Atrue%2C%22duration%22%3A0.1%2C%22easing%22%3A%22linear%22%7D%2C%7B%22sceneUrl%22%3A%22.%2Fscenes%2Fnight.json%22%2C%22targetUrl%22%3A%22.%2Fobjects%2Fexample.glb%22%2C%22targetPosition%22%3A%5B0%2C0%2C0%5D%2C%22targetScale%22%3A%5B1%2C1%2C1%5D%2C%22targetRotation%22%3A%5B0%2C0%2C0%5D%2C%22cameraPosition%22%3A%5B-0.7850000000000001%2C1.1158000000000001%2C2.0854%5D%2C%22orbit%22%3A%7B%22distance%22%3A2.3064853688354865%2C%22azimuthAngle%22%3A1.930817114597685%2C%22polarAngle%22%3A1.3096018878260705%7D%2C%22fov%22%3A60%2C%22shadows%22%3Atrue%2C%22duration%22%3A3%2C%22easing%22%3A%22ease-in%22%7D%2C%7B%22sceneUrl%22%3A%22.%2Fscenes%2Fnight.json%22%2C%22targetUrl%22%3A%22.%2Fobjects%2Fexample.glb%22%2C%22targetPosition%22%3A%5B0%2C0%2C0%5D%2C%22targetScale%22%3A%5B1%2C1%2C1%5D%2C%22targetRotation%22%3A%5B0%2C0%2C0%5D%2C%22cameraPosition%22%3A%5B2.5086%2C3.0338999999999996%2C9.0642%5D%2C%22orbit%22%3A%7B%22distance%22%3A9.735068363178236%2C%22azimuthAngle%22%3A1.3007954142751506%2C%22polarAngle%22%3A1.309625026737774%7D%2C%22fov%22%3A10%2C%22shadows%22%3Atrue%2C%22duration%22%3A3%2C%22easing%22%3A%22ease-in%22%7D%2C%7B%22sceneUrl%22%3A%22.%2Fscenes%2Fnight.json%22%2C%22targetUrl%22%3A%22.%2Fobjects%2Fexample.glb%22%2C%22targetPosition%22%3A%5B0%2C0%2C0%5D%2C%22targetScale%22%3A%5B1%2C1%2C1%5D%2C%22targetRotation%22%3A%5B0%2C0%2C0%5D%2C%22cameraPosition%22%3A%5B-2.8689999999999993%2C3.033899999999999%2C8.956599999999998%5D%2C%22orbit%22%3A%7B%22distance%22%3A9.735019516968304%2C%22azimuthAngle%22%3A1.880791736502569%2C%22polarAngle%22%3A1.3096236856590078%7D%2C%22fov%22%3A10%2C%22shadows%22%3Atrue%2C%22duration%22%3A3%2C%22easing%22%3A%22ease-in%22%7D%2C%7B%22sceneUrl%22%3A%22.%2Fscenes%2Fnight.json%22%2C%22targetUrl%22%3A%22.%2Fobjects%2Fexample.glb%22%2C%22targetPosition%22%3A%5B0%2C0%2C0%5D%2C%22targetScale%22%3A%5B1%2C1%2C1%5D%2C%22targetRotation%22%3A%5B0%2C0%2C0%5D%2C%22cameraPosition%22%3A%5B-10.5586%2C3.1715000000000004%2C8.728499999999999%5D%2C%22orbit%22%3A%7B%22distance%22%3A13.95350187687115%2C%22azimuthAngle%22%3A2.4507984996556536%2C%22polarAngle%22%3A1.3796232955411698%7D%2C%22fov%22%3A38%2C%22shadows%22%3Atrue%2C%22duration%22%3A3%2C%22easing%22%3A%22ease-out%22%7D%5D).

---



## What you can do

- Load a **GLB** target object into a lit scene
- Switch among bundled environments: Studio, Noon, Dusk, Night, Overcast
- Orbit, zoom, and frame with a camera viewfinder + composition guides
- Build a **keyframe timeline** (position, orbit, FOV, easing, duration)
- **Share** a URL that restores the exact setup
- **Export** a video of the animation (aspect ratio, resolution, FPS)

Everything runs client-side with [Three.js](https://threejs.org/). Scenes and objects are static assets — point the URL at yours, or fork and add them under `scenes/` and `objects/`.

---



## Quick start

Serve the repo root over HTTP (modules require a local server):

```bash
npx serve .
# or: python3 -m http.server
```

Open the printed URL, then pick a scene and object in the UI — or pass them as query params.

---



## URL parameters


| Param                                               | Description                                                 |
| --------------------------------------------------- | ----------------------------------------------------------- |
| `scene`                                             | Path to a scene JSON (e.g. `./scenes/night.json`)           |
| `target`                                            | Path to a GLB (e.g. `./objects/example.glb`)                |
| `targetPosition` / `targetScale` / `targetRotation` | Comma-separated `x,y,z`                                     |
| `cameraPosition`                                    | Camera position `x,y,z`                                     |
| `fov`                                               | Field of view (10–120)                                      |
| `shadows`                                           | `1` / `0`                                                   |
| `zoom`                                              | `camera` for viewfinder framing, or omit for fullscreen     |
| `guide`                                             | `1` / `0` composition guides                                |
| `keyframes`                                         | JSON array of keyframe poses (from Share / Export workflow) |
| `kf`                                                | Selected keyframe index                                     |


Use **Share** in the app to copy a link for the current frame (and keyframe list when you have more than one).

---



## Project layout

```
index.html          # App (viewer, keyframes, share, export)
scenes/             # Environment presets (JSON)
objects/            # Example GLB models
images/             # Viewfinder / guide SVGs
vendor/             # Bundled Three.js
media/              # README demo assets
```

---



## Adding your own content

1. Put a `.glb` in `objects/` (or host it anywhere CORS allows).
2. Optionally add scene JSON under `scenes/`.
3. Open the viewer with `?target=./objects/your-model.glb&scene=./scenes/night.json`, or enter the paths in the settings UI.

Fork the repo and push to GitHub Pages (workflow included) to host your own copy.

---



## Deploy

Pushing to `main` deploys via GitHub Actions to GitHub Pages. One-time: repo **Settings → Pages → Source: GitHub Actions**.

---



## License

Free to use, fork, and adapt. If you ship something cool with it, a credit or star is appreciated.