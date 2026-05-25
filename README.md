# 🎄 Christmas Scratch Aguinaldo

![Vanilla JS](https://img.shields.io/badge/Vanilla_JS-F7DF1E?style=flat&logo=javascript&logoColor=black)
![No Dependencies](https://img.shields.io/badge/No_Dependencies-green?style=flat)
![Mobile First](https://img.shields.io/badge/Mobile--First-blue?style=flat)
![MIT License](https://img.shields.io/badge/License-MIT-red?style=flat)

A festive, fully client-side scratch card web app. Scratch the red overlay with your finger or mouse to reveal a random cash prize — perfect for holiday giveaways and Christmas parties.

---

## 📖 Table of Contents

- [Demo](#-demo)
- [Features](#-features)
- [Getting Started](#-getting-started)
- [How It Works](#-how-it-works)
- [Prize Configuration](#-prize-configuration)
- [Customization](#-customization)
- [Browser Support](#-browser-support)
- [License](#-license)

---

## 🖥️ Demo

🔴 **Live:** [https://aguinaldo-chrismas.vercel.app/](https://aguinaldo-chrismas.vercel.app/)

Or run locally — open `index.html` directly in any modern browser, no server or build step needed.

```bash
open index.html
```

---

## ✨ Features

- 🖊️ **Canvas scratch mechanic** — uses HTML5 Canvas `destination-out` compositing to erase the overlay as you draw
- 📱 **Touch & mouse support** — works on desktop and mobile with proper pointer position scaling
- 🌙 **Dark mode toggle** — one-click switch between light and dark themes
- 🎉 **Confetti & snow effects** — animated confetti on reveal plus continuous ambient snowfall
- 🎲 **Weighted random prizes** — each prize has a configurable probability weight
- 📐 **DPR-aware rendering** — scales with `devicePixelRatio` for crisp display on retina screens
- 📳 **Haptic feedback** — triggers `navigator.vibrate()` on reveal where supported
- ♻️ **Try Again button** — resets the card and picks a new prize after each reveal

---

## 🚀 Getting Started

No installation, no dependencies, no build step.

1. **Clone the repository:**

```bash
git clone https://github.com/your-username/christmas-scratch-aguinaldo.git
cd christmas-scratch-aguinaldo
```

2. **Open `index.html` in any modern browser:**

```bash
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

3. **Or serve locally:**

```bash
npx serve .
# Then visit http://localhost:3000
```

> **Note:** The app is entirely self-contained in a single `index.html` file. No external fonts, libraries, or assets are loaded.

---

## ⚙️ How It Works

1. **Prize selection** — on load (and on each "Try Again"), a weighted random function picks a prize from the `amounts` array.
2. **Overlay drawn** — a crimson gradient is painted onto the scratch canvas using `source-over` compositing. The canvas then switches to `destination-out` mode.
3. **Scratching** — each pointer/touch event draws filled arcs and lines. In `destination-out` mode, these punch transparent holes in the overlay.
4. **Reveal check** — roughly every 15% of draw events, `getImageData` samples 1-in-30 pixels. When enough pixels are fully transparent, the prize is auto-revealed.
5. **Reveal** — the canvas is cleared, prize text and message are drawn, confetti fires, and the device vibrates (if supported).

---

## 💰 Prize Configuration

Prizes are defined in the `amounts` array near the top of the `<script>` block:

```js
const amounts = [
  { value: 10,  chance: 30 },
  { value: 25,  chance: 25 },
  { value: 30,  chance: 20 },
  { value: 50,  chance: 15 },
  { value: 100, chance: 10 },
];
```

| Prize | Message |
|-------|---------|
| PHP 10.00 | Small gift! Better luck next year 🎄 |
| PHP 25.00 | A little something! Enjoy it 🎁 |
| PHP 30.00 | Nice! Your Christmas is brighter 🎅 |
| PHP 50.00 | Great! Merry Christmas 🎄 |
| PHP 100.00 | Wow! Jackpot! Happy Holidays! 🎉 |

Prize messages are set separately in the `messages` object, keyed by prize value:

```js
const messages = {
  10:  "Small gift! Better luck next year 🎄",
  25:  "A little something! Enjoy it 🎁",
  30:  "Nice! Your Christmas is brighter 🎅",
  50:  "Great! Merry Christmas 🎄",
  100: "Wow! Jackpot! Happy Holidays! 🎉"
};
```

---

## 🎨 Customization

| What to change | Variable / location | Notes |
|---|---|---|
| Prize amounts & odds | `const amounts` | Edit `value` and `chance`. Weights are relative. |
| Prize messages | `const messages` | Keyed by prize value. Emoji supported. |
| Currency symbol | `revealGift()` → `prizeText` | Replace `PHP` with `$`, `€`, etc. |
| Reveal threshold | `let revealThreshold = 45` | Percentage of pixels cleared before auto-reveal. Lower = easier. |
| Brush size | `const BRUSH_SIZE` | 40px on mobile, 35px on desktop. |
| Overlay color | `drawScratchOverlay()` | Change the gradient stops to any color. |
| Confetti count | `createConfetti()` loop | Default 120 particles. |
| Snow particle count | `createSnow()` loop | Default 80 particles. |

---

## 🌐 Browser Support

| Browser | Support | Notes |
|---------|---------|-------|
| Chrome / Edge | ✅ Full | Including vibration API and touch events |
| Safari / iOS | ✅ Full | Uses `-webkit` prefixes where needed |
| Firefox | ✅ Full | Vibration API may be absent; degrades gracefully |
| IE 11 | ❌ Not supported | Uses `aspect-ratio`, arrow functions, `const`/`let` |

---

## 📄 License

This project is licensed under the **MIT License**. You are free to use, modify, and distribute it for personal or commercial purposes as long as the original license notice is included.

```
MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

<p align="center">Made by Desxzy/Zenyxy &nbsp;·&nbsp; 🎄 Christmas Scratch Aguinaldo</p>
