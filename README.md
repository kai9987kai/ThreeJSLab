# ThreeJSLab

![HTML](https://img.shields.io/badge/HTML-100%25-orange)
![Three.js](https://img.shields.io/badge/Three.js-0.184.0-black)
![License: MIT](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/status-experimental%20WebGL%20lab-blueviolet)

**ThreeJSLab** is an advanced single-file Three.js experiment currently centred on **Quantum Bloom Geometry Lab** — a real-time WebGL playground for procedural geometry, bloom lighting, particles, material tuning, diagnostics, screenshots, and fast visual experimentation.

The project is designed as a browser-first creative coding lab: open one HTML file, mutate the scene, explore shapes, tune rendering controls, and capture visual results without a build system.

---

## ✨ Features

- **Single-file WebGL app** — everything runs from `index.html`.
- **Three.js module import map** using Three.js `0.184.0`.
- **Procedural geometry system** with multiple shape modes:
  - Box
  - Sphere
  - Cone
  - Cylinder
  - Torus
  - Torus Knot
  - Dodecahedron
  - Icosahedron
  - Octahedron
  - Capsule
  - Random mode
- **High-impact rendering pipeline**
  - WebGL renderer
  - ACES filmic tone mapping
  - Soft shadows
  - Room environment lighting
  - Fog and atmospheric background
  - Optional bloom post-processing
- **Post-processing fallbacks**
  - Uses `EffectComposer`, `RenderPass`, `UnrealBloomPass`, and `OutputPass` when available.
  - Falls back to direct rendering if optional post-processing modules fail.
- **Interactive orbit camera**
  - Drag to orbit
  - Scroll to zoom
  - Damped camera movement
- **Live control console**
  - Geometry selector
  - Visual preset selector
  - Rotation speed
  - Metalness
  - Roughness
  - Bloom strength
  - Exposure
  - Echo clone count
  - Pixel ratio cap
  - Primary colour picker
  - Particle count
- **Scene toggles**
  - Auto evolve
  - Wireframe
  - Grid
  - Particles
- **Creative action buttons**
  - Randomise
  - Energy pulse
  - Screenshot export
  - Pause
  - Reset
- **Built-in diagnostics**
  - FPS display
  - Draw call counter
  - Triangle counter
  - WebGL mode display
  - Debug log panel
  - Fatal error screen with troubleshooting hints
- **Persistence**
  - Stores settings in `localStorage` so visual preferences can survive reloads.
- **Accessibility-aware motion**
  - Detects `prefers-reduced-motion` and reduces automatic camera motion.

---

## 🎛️ Presets

The lab includes several visual material and colour presets:

| Preset | Style |
|---|---|
| `Aurora Metal` | Cool metallic glow with cyan/orange contrast |
| `Solar Core` | Warm fiery bloom and energetic exposure |
| `Obsidian Neon` | Dark reflective neon look |
| `Ice Crystal` | Bright glassy cold tones |
| `Signal Matrix` | Green digital signal-inspired palette |

---

## ⌨️ Shortcuts

| Shortcut | Action |
|---|---|
| `Space` | Pause / resume animation |
| `R` | Randomise scene |
| `E` | Toggle auto evolve |
| `S` | Export screenshot |

Mouse / trackpad controls:

| Input | Action |
|---|---|
| Drag | Orbit around the object |
| Scroll | Zoom in / out |

---

## 🧱 Tech Stack

- **HTML5**
- **CSS3**
- **JavaScript ES Modules**
- **Three.js `0.184.0`**
- Three.js addons:
  - `OrbitControls`
  - `EffectComposer`
  - `RenderPass`
  - `UnrealBloomPass`
  - `OutputPass`
  - `RoomEnvironment`

No bundler, framework, package manager, or server is required for the basic demo.

---

## 🚀 Quick Start

### Option 1: Open directly

Clone the repository and open `index.html` in a modern browser.

```bash
git clone https://github.com/kai9987kai/ThreeJSLab.git
cd ThreeJSLab
```

Then open:

```text
index.html
```

### Option 2: Run a local static server

Some browsers are stricter with ES modules and CDN imports. For the most reliable experience, run a small local server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

---

## 📁 Project Structure

```text
ThreeJSLab/
├── index.html              # Main Three.js WebGL lab
├── README.md               # Project documentation
├── LICENSE                 # MIT license
├── CODE_OF_CONDUCT.md      # Contributor Covenant Code of Conduct
└── SECURITY.md             # Security policy
```

---

## 🧪 What This Lab Is Good For

ThreeJSLab is useful for:

- experimenting with real-time 3D visual design
- testing Three.js materials and lighting
- generating abstract procedural artwork
- exploring bloom, exposure, and tone mapping
- learning how a single-file Three.js app is structured
- prototyping interactive WebGL UI controls
- capturing screenshots of generated 3D forms

---

## 🖥️ Browser Requirements

A modern browser with WebGL support is required.

Recommended browsers:

- Chrome / Chromium
- Microsoft Edge
- Firefox
- Safari with WebGL enabled

If the scene does not load, check:

1. Your internet connection, because Three.js modules are loaded from a CDN.
2. Browser WebGL support.
3. Console errors in developer tools.
4. Whether browser privacy or security settings are blocking module imports.

---

## 🛠️ Development Notes

This project intentionally keeps the app in one file to make it easy to copy, remix, host, and experiment with. The current architecture is ideal for rapid visual prototyping, but future versions could split the app into modules.

Possible future structure:

```text
src/
├── main.js
├── scene/
│   ├── createScene.js
│   ├── geometry.js
│   ├── materials.js
│   └── particles.js
├── ui/
│   ├── controls.js
│   └── diagnostics.js
└── utils/
    ├── storage.js
    └── screenshots.js
```

---

## 🔮 Roadmap Ideas

Potential improvements for future releases:

- [ ] Preset save/load manager
- [ ] Export scene settings as JSON
- [ ] Import custom preset JSON
- [ ] More procedural shape families
- [ ] Shader-based displacement modes
- [ ] Audio-reactive bloom and particles
- [ ] Timeline-based animation recording
- [ ] GIF or WebM export
- [ ] Mobile-optimised compact controls
- [ ] WebGPU experimental branch
- [ ] Performance quality presets
- [ ] Shareable URL parameters for scene state
- [ ] Gallery mode for generated screenshots
- [ ] Modular source layout for larger experiments

---

## 🤝 Contributing

Contributions, experiments, fixes, and feature ideas are welcome.

Good contribution areas include:

- new geometry modes
- new presets
- shader experiments
- UI improvements
- accessibility improvements
- mobile layout refinements
- performance optimisation
- documentation updates

Suggested workflow:

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test in at least one modern WebGL browser.
5. Open a pull request with a clear explanation of what changed.

Please follow the included Code of Conduct.

---

## 🔒 Security

This is a client-side visual experiment, but security issues can still matter, especially around external scripts, CDN imports, browser APIs, and exported files.

If you find a vulnerability or unsafe behaviour, please report it through the repository security process described in `SECURITY.md`.

---

## 📄 License

This project is licensed under the **MIT License**.

Copyright © 2026 Kai Piper.

See [`LICENSE`](LICENSE) for details.

---

## 🙌 Credits

Created by **Kai Piper / kai9987kai** as an experimental Three.js visual lab.

Built with [Three.js](https://threejs.org/).
