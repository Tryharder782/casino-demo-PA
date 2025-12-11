# 🎰 Golden Chip | High-Fidelity iGaming Playable Ad

![Casino Preview](preview.gif)
<!-- УБЕДИСЬ, ЧТО ФАЙЛ preview.gif ЛЕЖИТ В ПАПКЕ public ИЛИ В КОРНЕ -->

[![Live Demo](https://img.shields.io/badge/Live_Demo-Vercel-000?style=for-the-badge&logo=vercel&logoColor=white)](https://casino-playable-demo.vercel.app)
<!-- ЗАМЕНИ ССЫЛКУ ВЫШЕ НА ТВОЮ ФИНАЛЬНУЮ ССЫЛКУ VERCEL -->

## 💎 Overview

A premium **3D Playable Ad prototype** designed for the **iGaming & Social Casino** market.

This project demonstrates how to achieve **high-end visual fidelity** (PBR gold materials, dynamic lighting, particle systems) while maintaining an ultra-low file size for instant user acquisition.

Built with **React Three Fiber** and **Three.js**, bypassing standard engine bloat to deliver a sub-1MB experience.

## 🏆 Key Technical Benchmarks

*   **📉 File Size:** **765 KB** (Total transferred).
    *   *vs Standard Unity Casino Build:* ~5MB - 15MB.
*   **📦 Single-File Delivery:** All assets (3D models, textures, code) are bundled into a single `index.html` via Base64.
*   **✨ Visuals:** Custom PBR Gold Shaders with Environment Mapping for realistic reflections.
*   **⚡ Performance:** Stable 60 FPS on low-end Android devices.

## 🛠 Tech Stack & Features

*   **Engine:** Three.js / React Three Fiber (R3F)
*   **Bundler:** Vite + `vite-plugin-singlefile`
*   **Shaders:** Custom MeshStandardMaterial configuration for realistic metal rendering.
*   **Particles:** Instanced Mesh system for high-performance coin explosions.
*   **Physics:** Procedural "Squash & Stretch" animation logic (no heavy animation clips).

## 🏗 Architecture

### The "Casino Quality" Challenge
iGaming ads require a "premium" look (shiny gold, smooth animations) which usually results in heavy textures and slow load times.

**My Solution:**
1.  **Procedural Materials:** Instead of using heavy baked textures, I utilize Three.js PBR materials with optimized Environment Maps to simulate gold reflections.
2.  **Asset Compression:** The 3D chip model is Draco-compressed and embedded directly into the code.
3.  **Code-Driven Animation:** Animations are calculated mathematically at runtime, saving megabytes of asset data.

## 💻 Local Development

1.  **Clone the repo:**
    ```bash
    git clone https://github.com/Tryharder782/casino-demo-PA.git
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Run dev server:**
    ```bash
    npm run dev
    ```

## 📦 Building for Production

To generate the single-file build (ready for Mintegral/AppLovin/Unity Ads):

```bash
npm run build
