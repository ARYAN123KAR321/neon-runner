# 🏃 NEON RUNNER

> *Survive the underground. Outrun the megacity.*

A fully self-contained cyberpunk endless runner game built with pure HTML5 Canvas and Vanilla JavaScript — no frameworks, no dependencies, no build tools. Just one single HTML file.

---

## 🎮 Play Now

👉 **[Play NEON RUNNER](https://aryan123kar321.github.io/neon-runner/)**

---

## 📸 About

NEON RUNNER is a side-scrolling endless runner set in a dystopian rain-soaked megacity. You play as a neon-lit hacker rebel sprinting through underground subway tunnels, elevated rails, and neon-drenched city streets — dodging security drones, electric gates, laser beams, and corrupt enforcement bots while collecting data chips and power-ups.

The game gets faster and harder the longer you survive. How far can you run?

---

## ✨ Features

### Gameplay
- **3 parallel lanes** — Elevated Rail, Platform, Street — each with unique visual detail
- **Jump** with gravity physics, **Slide** to duck under obstacles, **Lane switch** smoothly mid-air
- **7 obstacle types** — Steel Barriers, Ground Cables, Laser Beams, Hover Drones, Concrete Walls, Electric Gates
- **5 power-up types** — Shield, Magnet, Boost, Ghost, Score Multiplier
- **2 enemy types** — Security Bots and Aggressive Tracking Drones
- **Endless difficulty scaling** — speed increases from 5× to 18× over time
- **Score multiplier system** — chain bonuses for higher scores
- **Distance milestone bonuses** — guaranteed power-up every 500m

### Visuals
- **6-layer parallax background** — far skyline, mid city, near buildings, fog, rain, foreground pipes
- **300 rain particles** with wind angle and ground splashes
- **Procedural neon signs** on buildings with unique names
- **Flickering window grids** on all buildings
- **Full particle system** — sparks, explosions, coin pops, landing bursts, steam
- **CRT scanline overlay** for that retro-monitor feel
- **Chromatic aberration** glitch effect on damage
- **Camera shake** on impact
- **Screen flash** on hits and collectibles
- **Motion trail** on player, extends during Boost power-up
- **Animated shield ring** when Shield power-up is active
- **Smart cursor** — visible on menus, hidden during gameplay for full immersion

### Audio
- **100% synthesized** via Web Audio API — zero external audio files
- Jump, coin collect, damage, power-up, game-over sound effects
- Ambient cyberpunk bass drone background music
- Mute toggle with preference saved across sessions

### Technical
- **Single file** — entire game in one `index.html`, ~1,200 lines
- **No dependencies** — pure HTML5 Canvas + Vanilla JavaScript
- **No build step** — open in browser and play
- **Responsive** — scales to any screen size maintaining aspect ratio
- **Mobile support** — swipe gestures + on-screen touch buttons
- **High score persistence** via `localStorage`
- **Particle pool cap** at 500 for smooth performance

---

## 🕹️ Controls

### Keyboard
| Key | Action |
|-----|--------|
| `W` or `↑` | Switch to upper lane |
| `S` or `↓` | Switch to lower lane |
| `Space` | Jump |
| Hold `S` / `↓` | Slide under obstacles |
| `P` or `Esc` | Pause / Resume |

### Mobile / Touch
| Gesture | Action |
|---------|--------|
| Swipe Up | Upper lane |
| Swipe Down | Lower lane / Slide |
| Tap | Jump |
| On-screen buttons | Full touch control |

---

## ⚡ Power-Ups

| Icon | Name | Effect | Duration |
|------|------|--------|----------|
| 🛡 | **SHIELD** | Absorbs one hit without losing a life | 8s |
| 🧲 | **MAGNET** | Auto-collects all data chips within range | 10s |
| ⚡ | **BOOST** | Dramatically increases speed | 5s |
| 👻 | **GHOST** | Phase through all obstacles unharmed | 6s |
| ×5 | **HACK** | Score multiplier becomes ×5 | 12s |

---

## 🏗️ Technical Details

### Architecture
```
index.html
├── <style>        — All CSS inline
├── <body>         — Loading, Menu, HUD, Game Over, Pause overlays
│   └── <canvas>   — Game rendered here (1280×480 logical resolution)
└── <script>       — Complete game logic (~900 lines of JS)
```

### Tech Stack
- **Rendering** — HTML5 Canvas 2D API
- **Audio** — Web Audio API (synthesized, no files)
- **Fonts** — Google Fonts (Orbitron + Share Tech Mono)
- **Storage** — localStorage (high score + mute preference)
- **Language** — Vanilla JavaScript (ES6+)
- **No frameworks. No bundlers. No npm.**

### Game Systems
- State machine with 5 states: `loading → menu → playing → paused → gameover`
- AABB collision detection with inset hitboxes
- Object pool for particles (capped at 500)
- Parallax scrolling at 6 different depth speeds
- Procedural building generation with neon signs and window grids
- Frame-based physics with gravity constant
- Difficulty scaling via speed progression and spawn rate curves

---

## 🚀 Run Locally

No setup needed. Just:

1. Download `index.html`
2. Open it in any modern browser
3. Play

```bash
# Or serve it with any static server
npx serve .
python -m http.server 8000
```

---

## 📁 Project Structure

```
neon-runner/
├── index.html    ← The entire game
└── README.md     ← This file
```

That's it. Two files.

---

## 🌐 Deploy Your Own

### GitHub Pages (Free)
1. Fork or upload `index.html` to a GitHub repository
2. Go to **Settings → Pages → Source → main branch**
3. Your game is live at `https://yourusername.github.io/repo-name`

### Netlify Drop (Instant)
1. Go to **netlify.com/drop**
2. Drag and drop your folder
3. Live URL generated in seconds

### Vercel (Fast CDN)
1. Install: `npm install -g vercel`
2. Run: `vercel` inside your project folder
3. Follow prompts — live URL in under a minute

---

## 🎨 Design

- **Color Palette** — Deep black `#0a0a0f` background with neon cyan `#00fff9`, magenta `#ff00c8`, purple `#7b00ff`, green `#39ff14`, amber `#ffaa00`, red `#ff003c`
- **Typography** — `Orbitron` for all UI, `Share Tech Mono` for data readouts
- **Aesthetic** — Dystopian megacity, CRT monitor simulation, rain-soaked streets, holographic adverts, flickering neon

---

## 📜 License

MIT License — free to use, modify, and distribute.

---

## 🙌 Credits

Built with pure HTML5 Canvas and Web Audio API.
No libraries were harmed in the making of this game.

---

*// MEGACITY TRANSIT AUTHORITY — v2.0.77 // NEURAL OS*
