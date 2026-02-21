# 🎲 RafflePro — Live Event Raffle System

A professional, cinema-grade interactive raffle web application with 4 game modes, PWA support, and live-event production quality.

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🎬 Cinematic Mode | 5-second countdown, name shuffle, winner reveal with confetti |
| 🎡 Fortune Wheel | Canvas-based spinning wheel with physics deceleration |
| ⚔ Battle Tournament | Automatic bracket system, round progression, champion reveal |
| 📱 PWA App | Installable, offline-capable, standalone display |
| 🔒 Crypto Random | Uses `crypto.getRandomValues()` for provably fair draws |
| 📥 CSV Export | Export all winners with prize tier and timestamps |
| 🔊 Sound Engine | Web Audio API — drumroll, countdown, win sounds |
| 🎊 Confetti | Canvas particle animation on every winner reveal |
| ⛶ Fullscreen | Projector-ready presentation mode |

## 🚀 Quick Start

### Option 1: Open Directly (Zero Setup)
```bash
# Just open index.html in any modern browser
open index.html
```

### Option 2: Local Server (Required for PWA/Service Worker)
```bash
# Python
python3 -m http.server 8080

# Node.js (npx)
npx serve .

# Node.js (http-server)
npx http-server . -p 8080 -c-1
```

Then visit: `http://localhost:8080`

### Option 3: Deploy to Production
Upload all files to any static hosting service:
- **Netlify**: Drop the folder into netlify.com/drop
- **Vercel**: `vercel deploy`
- **GitHub Pages**: Push to `gh-pages` branch
- **Cloudflare Pages**: Connect repo, auto-deploy

## 📂 File Structure

```
raffle-app/
├── index.html          # Main application (all modes included)
├── manifest.json       # PWA manifest
├── sw.js               # Service worker (offline support)
├── icons/
│   ├── icon.svg        # Source SVG icon
│   ├── icon-192.png    # PWA icon (small)
│   └── icon-512.png    # PWA icon (large)
├── generate-icons.js   # Icon generation utility
└── README.md           # This file
```

## 🎮 How to Use

### Adding Players
1. Type names in the **ADD PLAYERS** text area (one per line, or comma-separated)
2. Click **+ ADD** to add them
3. Use **⇌** to shuffle order
4. Use **📋** to load 12 sample players

### Game Modes

**🎬 Cinematic Mode**
- Press **DRAW** or `Spacebar`
- Watch the 3-second countdown
- Names shuffle across screen with drumroll
- Winner revealed with spotlight and confetti

**🎡 Fortune Wheel**
- Press **SPIN**
- Wheel spins with physics deceleration
- Winner highlighted at pointer, then removed

**⚔ Battle Tournament**
- Press **FIGHT** to start the tournament
- Each press resolves the next match automatically
- Click a player card manually to override the winner
- Bracket advances through rounds until Grand Champion

**📱 PWA Install**
- Shows install instructions and prompts
- On supported browsers, click **Install RafflePro**
- iOS: Safari → Share → Add to Home Screen

### Controls
| Action | Shortcut |
|--------|----------|
| Draw/Spin/Fight | `Space` |
| Toggle Fullscreen | `F` |
| Close/Exit | `Escape` |

### Admin Controls
- **Prize Tier**: Select Consolation / Minor / Major / Grand Prize before drawing
- **🔊 Sound**: Toggle sound effects
- **📥 Export**: Download winners as CSV
- **↺ Reset**: Clear winners (players remain)

## 🎯 Live Event Setup

For **projector/stage use**:
1. Press `F` or click **⛶** for fullscreen
2. Use **🎬 Cinematic Mode** for maximum drama
3. The control panel auto-hides during reveal
4. Large typography scales to any screen size

For **mobile/tablet**:
- Fully touch-friendly
- Responsive layout adapts automatically
- Install as PWA for best experience

## 🔒 Fairness & Transparency

- Uses `crypto.getRandomValues()` — cryptographically secure randomness
- **CRYPTOSECURE** indicator shown in header
- Players are shuffled before each session
- Eliminated players cannot be drawn again
- All winners logged with timestamps

## 🛠 Customization

Edit CSS variables in `index.html` (`<style>` block):

```css
:root {
  --gold: #f0c040;           /* Primary accent color */
  --bg-void: #050507;        /* Background color */
  --font-display: 'Bebas Neue'; /* Headline font */
}
```

## 📱 PWA Requirements

For full PWA functionality (offline support + install prompt):
- Must be served over **HTTPS** or **localhost**
- Service worker requires a server (not `file://` protocol)
- Tested in Chrome, Edge, Firefox, Safari

## 🌐 Browser Support

| Browser | Cinematic | Wheel | Battle | PWA Install |
|---------|-----------|-------|--------|-------------|
| Chrome 90+ | ✅ | ✅ | ✅ | ✅ |
| Edge 90+ | ✅ | ✅ | ✅ | ✅ |
| Firefox 90+ | ✅ | ✅ | ✅ | ⚠ Limited |
| Safari 15+ | ✅ | ✅ | ✅ | ✅ (iOS) |

---

**RafflePro** — Built for professional live event production 🎲✨
