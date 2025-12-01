# MAD-GAME
<h2># 🚗 Drive Mad – Browser Game (HTML + WebAssembly)<h2>

This repository contains the fully working **WebAssembly (WASM) version of the Drive Mad game**, exported for the browser using Emscripten.  
The project includes all required files such as HTML loader, WASM runtime, assets, and UI resources.

Play it directly in the browser after deployment on **GitHub Pages** or any static hosting.

---

<h2>## 📂 Project Structure<h2>
/ (root)
│── index.html # Main HTML loader for the game
│── webapp/
│ ├── cover.jpg
│ ├── share.png
│ ├── wasmbin_webapp.data
│── assets/ # Game assets (if included)
│── mono/ # Mono runtime files (auto-generated)
│── scripts.js / wasm loader # Emscripten loader included inside HTML


<h2>### Important Files<h2>

| File | Description |
|------|-------------|
| **index.html** | WebAssembly loader (preload plugin, audio context, canvas, Module object, logging, fullscreen handler) |
| **wasmbin_webapp.data** | Packed assets for the WASM runtime |
| **webapp/\*** | Game UI images + metadata |
| **mono/** | Mono WebAssembly runtime files used for C# game code |
| **{{{ SCRIPT }}}** | Auto-generated JS glue code referenced inside HTML |
| **{{{ WASM_FILE }}}** | Actual WASM binary executed by the runtime |



<h2>## 🚀 How to Run the Game Locally<h2>

Because the game uses **WASM + binary asset loading**, direct file open (double-click) may NOT work in some browsers.  
Use a simple local server.

### ✅ Option 1 — Python Server
```bash
python -m http.server

<h2>🌐 Deploying on GitHub Pages (Recommended)<h2>

Upload all files to a GitHub repository

Open: Settings → Pages

Select:

Branch: main

Folder: / (root)

Save changes

Wait 10–20 seconds

<h2>🛠 Technology Used<h2>


Technology	              Purpose
HTML5 Canvas	          Rendering game graphics
WebAssembly (WASM)	      Runs the actual Drive Mad compiled code
Emscripten	              Generates the JS loader, memory config, data preloaders
JavaScript	             Controls loading, logging, audio, and fullscreen
Mono WASM runtime	     Executes C# code inside browser

<h2>🎮 Game Features<h2>

Works fully inside browser

Smooth performance using WASM

Preloaded assets system

Fullscreen support

Audio + haptic feedback

Touch controls for mobile

Clean UI with preloader + progress bar

<h2>🎮 Controls<h2>

Arrow Keys / WASD → Drive

Space / Up → Accelerate

Mobile: On-screen touch controls

Click Canvas: Focus for keyboard controls

<h2>🔧 Important Code Notes<h2>

The loader uses:

{{{ SCRIPT }}} → Emscripten JS glue

{{{ WASM_FILE }}} → Game WebAssembly binary

{{{ INITIAL_MEMORY }}} → Memory allocated for WASM

preloadPlugin → Loads images/assets automatically

Audio uses:

window.AudioContext || window.webkitAudioContext


Canvas resizing & scaling managed by:

Module.preRun.push(updateLoadingBar)


Preloader shows progress while assets load

<h2>📸 Preview Image<h2>
![Game Cover](./webapp/cover.jpg)

<h2>📜 License<h2>

This project is for educational and personal purposes only.
Original Drive Mad game by Martin Magni.

<h2>⭐ Support<h2>

If you like this project, please consider giving it a ⭐ star on GitHub!


---

# ✔ Your README.md is Ready!

Agar chaho to main:

✔ README me **badges**, **screenshots**, **GIF preview**, **live demo link**, **contributor section**, **dark theme banner** bhi add kar sakta hoon.  
✔ Ya README ko **Hindi + Hinglish** version me convert kar sakta hoon.

Just say **“add pro version README”** or send your **GitHub repo URL**.
