# Wretched Lab — NFS Unbound Virtual Car Showroom 🚗

A high-performance, interactive 3D virtual car showroom built with **Three.js** and **WebGL**, featuring four iconic supercars from Need for Speed: Unbound in a real-time rendering environment.

> **Live Preview** → Hosted locally via `http-server` or any static file server.

---

## 🚀 Features

- **Real-time 3D rendering** powered by Three.js + WebGL
- **4 iconic supercars** — McLaren Senna, Lamborghini Gallardo LP560, Nissan Skyline GT-R R35, Ferrari F40
- **Dynamic paint system** — change car paint color in real time
- **Iridescence shader** — subtle color shift effect on car paint
- **Interactive camera** — Cinematic and Free-look modes
- **Door & lighting controls** — open doors, toggle headlights/taillights
- **HDR environment lighting** with KTX2 compressed textures
- **Draco mesh compression** for fast `.glb` model loading
- **Screenshot capture** — export a PNG/JPG of your current view
- **SSAO** — Screen Space Ambient Occlusion for depth realism
- **Sound FX** — car door open/close, camera shutter
- **Floor grid overlay** toggle
- **Fully responsive** across desktop & mobile

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| 3D Rendering | Three.js r163 |
| Framework | Next.js (static export) |
| Styling | Tailwind CSS v3 |
| Model Format | glTF 2.0 / `.glb` |
| Texture Compression | KTX2 + Basis Universal |
| Mesh Compression | Draco |
| Language | TypeScript / JavaScript |

---

## 🚗 Car Models

| Car | File |
|---|---|
| McLaren Senna | `mclaren-senna.glb` |
| Lamborghini Gallardo LP560 | `lamborghini-gallardo-lp560.glb` |
| Nissan Skyline GT-R R35 | `nissan-skyline-gtr-r35.glb` |
| Ferrari F40 | `ferrari-f40.glb` |

---

## 📁 Project Structure

```
public/
└── virtual-car-showroom/
    ├── index.html              # Entry point
    ├── assets/
    │   ├── images/             # Car thumbnail previews
    │   ├── sounds/             # UI sound effects
    │   └── webgl/
    │       ├── models/         # .glb 3D car models
    │       ├── textures/       # KTX2 + PNG textures
    │       └── environments/   # HDR lighting
    ├── lib/
    │   ├── draco/              # Draco WASM decoder
    │   └── basis/              # Basis Universal WASM transcoder
    └── _next/static/           # Compiled JS/CSS bundles
```

---

## 🖥 Running Locally

### Prerequisites
- Node.js ≥ 18

### Install & Serve

```bash
# Install a static file server
npm install -g http-server

# Serve the project (no-cache mode for development)
http-server public -p 3002 --cors -c-1
```

Then open **http://localhost:3002/virtual-car-showroom/** in your browser.

> ⚠️ WebGL requires a modern browser (Chrome, Edge, Firefox). Safari may have limited support.

---

## 🎮 Controls

| Action | Control |
|---|---|
| Rotate camera | Left-click + drag |
| Zoom | Scroll wheel |
| Select car | Car model button (bottom toolbar) |
| Change paint | Paint bucket icon |
| Toggle doors | Door icon |
| Toggle lights | Headlight / Taillight icons |
| Take screenshot | Camera icon |
| Switch camera mode | Camera mode icon |

---

## 📦 Build Notes

This is a **Next.js static export** — all assets are pre-compiled. No server-side code runs at runtime. The `_next/static/` directory contains the production-optimised JS and CSS bundles.

---

## 👤 Author

**Sunil** — [@Sunil56224972](https://github.com/Sunil56224972)

---

## 📄 License

MIT © Sunil56224972
