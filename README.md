# Wretched Lab — NFS Unbound Virtual Car Showroom

A high-performance, interactive 3D virtual car showroom built with **Three.js** and **WebGL**, featuring four iconic supercars from Need for Speed: Unbound in a real-time rendering environment.

---

## Features

- Real-time 3D rendering powered by Three.js and WebGL
- Four iconic supercars — McLaren Senna, Lamborghini Gallardo LP560, Nissan Skyline GT-R R35, Ferrari F40
- Dynamic paint color system with real-time color change
- Iridescence shader — subtle color shift on car paint with every angle
- Interactive camera — Cinematic and Free-look modes
- Door and lighting controls — open doors, toggle headlights and taillights
- HDR environment lighting with KTX2 compressed textures
- Draco mesh compression for fast `.glb` model loading
- Screenshot capture — export PNG or JPG of current view
- Screen Space Ambient Occlusion (SSAO) for depth realism
- UI sound effects — car door, camera shutter
- Floor grid overlay toggle
- Responsive across desktop and mobile

---

## Tech Stack

| Layer | Technology |
|---|---|
| 3D Rendering | Three.js r163 |
| Framework | Next.js (static export) |
| Styling | Tailwind CSS v3 |
| Model Format | glTF 2.0 / .glb |
| Texture Compression | KTX2 + Basis Universal |
| Mesh Compression | Draco |
| Language | TypeScript / JavaScript |

---

## Car Models

| Car | Model File |
|---|---|
| McLaren Senna | `mclaren-senna.glb` |
| Lamborghini Gallardo LP560 | `lamborghini-gallardo-lp560.glb` |
| Nissan Skyline GT-R R35 | `nissan-skyline-gtr-r35.glb` |
| Ferrari F40 | `ferrari-f40.glb` |

---

## Project Structure

```
public/
└── virtual-car-showroom/
    ├── index.html
    ├── assets/
    │   ├── images/             # Car thumbnail previews
    │   ├── sounds/             # UI sound effects
    │   └── webgl/
    │       ├── models/         # .glb 3D car models
    │       ├── textures/       # KTX2 + PNG textures
    │       └── environments/   # HDR lighting maps
    ├── lib/
    │   ├── draco/              # Draco WASM decoder
    │   └── basis/              # Basis Universal WASM transcoder
    └── _next/static/           # Compiled JS and CSS bundles
```

---

## Running Locally

**Prerequisites:** Node.js 18 or higher

```bash
# Install a static file server
npm install -g http-server

# Serve the project
http-server public -p 3002 --cors -c-1
```

Open **http://localhost:3002/virtual-car-showroom/** in your browser.

> WebGL requires a modern browser (Chrome, Edge, Firefox). Use hardware acceleration for best performance.

---

## Controls

| Action | Control |
|---|---|
| Rotate camera | Left-click and drag |
| Zoom | Scroll wheel |
| Select car | Car model button in bottom toolbar |
| Change paint color | Paint bucket icon |
| Toggle doors | Door icon |
| Toggle headlights / taillights | Light icons |
| Take screenshot | Camera icon |
| Switch camera mode | Camera mode icon |

---

## Credits

### 3D Car Models

The car models used in this project are sourced from the NFS Unbound community and public 3D repositories, used here for creative and educational purposes.

| Model | Source |
|---|---|
| McLaren Senna | Sketchfab — NFS Unbound Community |
| Lamborghini Gallardo LP560 | Free3D.com — Community Upload |
| Nissan Skyline GT-R R35 | Sketchfab — NFS Unbound Community |
| Ferrari F40 | Free3D.com — Community Upload |

### Libraries

| Library | Author |
|---|---|
| [Three.js](https://threejs.org) | Mr.doob and contributors |
| [Basis Universal](https://github.com/BinomialLLC/basis_universal) | Binomial LLC |
| [Draco](https://google.github.io/draco/) | Google |
| [Next.js](https://nextjs.org) | Vercel |
| [Tailwind CSS](https://tailwindcss.com) | Tailwind Labs |

All third-party assets are used under their respective licenses. No commercial use is intended.

---

## Author

**Sunil** — [github.com/Sunil56224972](https://github.com/Sunil56224972)

---

## License

MIT License — Copyright (c) 2024 Sunil56224972
