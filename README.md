<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>README — Christmas Scratch Aguinaldo</title>
<style>
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    font-size: 16px;
    line-height: 1.7;
    color: #24292f;
    background: #ffffff;
    margin: 0;
    padding: 0;
  }
  .markdown-body {
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 32px 80px;
  }
  h1, h2, h3, h4 {
    font-weight: 600;
    line-height: 1.25;
    margin-top: 24px;
    margin-bottom: 16px;
    color: #1f2328;
  }
  h1 { font-size: 2em; padding-bottom: 0.3em; border-bottom: 1px solid #d0d7de; margin-top: 0; }
  h2 { font-size: 1.5em; padding-bottom: 0.3em; border-bottom: 1px solid #d0d7de; }
  h3 { font-size: 1.25em; }
  p { margin-top: 0; margin-bottom: 16px; }
  strong { font-weight: 600; }
  em { font-style: italic; }
  a { color: #0969da; text-decoration: none; }
  a:hover { text-decoration: underline; }
  hr { border: none; border-top: 1px solid #d0d7de; margin: 24px 0; }
  code {
    font-family: ui-monospace, SFMono-Regular, "SF Mono", Menlo, Consolas, monospace;
    font-size: 85%;
    background: rgba(175,184,193,0.2);
    border-radius: 6px;
    padding: 0.2em 0.4em;
  }
  pre {
    background: #f6f8fa;
    border-radius: 6px;
    padding: 16px;
    overflow-x: auto;
    font-size: 85%;
    line-height: 1.6;
    margin-bottom: 16px;
    border: 1px solid #d0d7de;
  }
  pre code {
    background: none;
    padding: 0;
    border-radius: 0;
    font-size: 100%;
  }
  blockquote {
    margin: 0 0 16px;
    padding: 0 1em;
    color: #656d76;
    border-left: 4px solid #d0d7de;
  }
  ul, ol {
    margin-top: 0;
    margin-bottom: 16px;
    padding-left: 2em;
  }
  li { margin-bottom: 4px; }
  li > ul, li > ol { margin-top: 4px; margin-bottom: 0; }
  table {
    border-collapse: collapse;
    width: 100%;
    margin-bottom: 16px;
    display: block;
    overflow-x: auto;
  }
  th, td {
    border: 1px solid #d0d7de;
    padding: 6px 13px;
    font-size: 14px;
  }
  th { background: #f6f8fa; font-weight: 600; }
  tr:nth-child(even) { background: #f6f8fa; }
  .badges { margin-bottom: 16px; display: flex; flex-wrap: wrap; gap: 6px; }
  .badge {
    display: inline-block;
    font-size: 12px;
    font-weight: 600;
    padding: 3px 10px;
    border-radius: 4px;
    line-height: 1.4;
  }
  .badge-red   { background: #fff0f0; color: #b91c1c; border: 1px solid #fca5a5; }
  .badge-green { background: #f0fdf4; color: #15803d; border: 1px solid #86efac; }
  .badge-blue  { background: #eff6ff; color: #1d4ed8; border: 1px solid #93c5fd; }
  .badge-gray  { background: #f6f8fa; color: #57606a; border: 1px solid #d0d7de; }
  .note {
    background: #ddf4ff;
    border-left: 4px solid #0969da;
    border-radius: 0 6px 6px 0;
    padding: 12px 16px;
    margin-bottom: 16px;
    font-size: 14px;
    color: #0550ae;
  }
  .note strong { color: #0550ae; }
  @media (max-width: 600px) {
    .markdown-body { padding: 24px 16px 60px; }
    h1 { font-size: 1.6em; }
  }
</style>
</head>
<body>
<div class="markdown-body">

<h1>🎄 Christmas Scratch Aguinaldo</h1>

<div class="badges">
  <span class="badge badge-gray">Vanilla JS</span>
  <span class="badge badge-gray">Single File</span>
  <span class="badge badge-green">No Dependencies</span>
  <span class="badge badge-blue">Mobile-First</span>
  <span class="badge badge-red">MIT License</span>
</div>

<p>A festive, fully client-side scratch card web app. Scratch the red overlay with your finger or mouse to reveal a random cash prize — perfect for holiday giveaways and Christmas parties.</p>

<hr>

<h2>📖 Table of Contents</h2>
<ul>
  <li><a href="#demo">Demo</a></li>
  <li><a href="#features">Features</a></li>
  <li><a href="#getting-started">Getting Started</a></li>
  <li><a href="#how-it-works">How It Works</a></li>
  <li><a href="#prize-configuration">Prize Configuration</a></li>
  <li><a href="#customization">Customization</a></li>
  <li><a href="#browser-support">Browser Support</a></li>
  <li><a href="#license">License</a></li>
</ul>

<hr>

<h2 id="demo">🖥️ Demo</h2>

<p>🔴 <strong>Live:</strong> <a href="https://aguinaldo-chrismas.vercel.app/">https://aguinaldo-chrismas.vercel.app/</a></p>

<p>Or run locally — open <code>index.html</code> directly in any modern browser, no server or build step needed.</p>

<pre><code>open index.html</code></pre>

<hr>

<h2 id="features">✨ Features</h2>

<ul>
  <li>🖊️ <strong>Canvas scratch mechanic</strong> — uses HTML5 Canvas <code>destination-out</code> compositing to erase the overlay as you draw</li>
  <li>📱 <strong>Touch &amp; mouse support</strong> — works on desktop and mobile with proper pointer position scaling</li>
  <li>🌙 <strong>Dark mode toggle</strong> — one-click switch between light and dark themes</li>
  <li>🎉 <strong>Confetti &amp; snow effects</strong> — animated confetti on reveal plus continuous ambient snowfall</li>
  <li>🎲 <strong>Weighted random prizes</strong> — each prize has a configurable probability weight</li>
  <li>📐 <strong>DPR-aware rendering</strong> — scales with <code>devicePixelRatio</code> for crisp display on retina screens</li>
  <li>📳 <strong>Haptic feedback</strong> — triggers <code>navigator.vibrate()</code> on reveal where supported</li>
  <li>♻️ <strong>Try Again button</strong> — resets the card and picks a new prize after each reveal</li>
</ul>

<hr>

<h2 id="getting-started">🚀 Getting Started</h2>

<p>No installation, no dependencies, no build step.</p>

<ol>
  <li><strong>Download or clone</strong> the repository:
<pre><code>git clone https://github.com/your-username/christmas-scratch-aguinaldo.git
cd christmas-scratch-aguinaldo</code></pre>
  </li>
  <li><strong>Open</strong> <code>index.html</code> in any modern browser:
<pre><code>open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux</code></pre>
  </li>
  <li><strong>Or serve locally</strong> if you prefer a local server:
<pre><code>npx serve .
# Then visit http://localhost:3000</code></pre>
  </li>
</ol>

<div class="note"><strong>Note:</strong> The app is entirely self-contained in a single <code>index.html</code> file. No external fonts, libraries, or assets are loaded.</div>

<hr>

<h2 id="how-it-works">⚙️ How It Works</h2>

<ol>
  <li><strong>Prize selection</strong> — on load (and on each "Try Again"), a weighted random function picks a prize from the <code>amounts</code> array.</li>
  <li><strong>Overlay drawn</strong> — a crimson gradient is painted onto the scratch canvas using <code>source-over</code> compositing. The canvas then switches to <code>destination-out</code> mode.</li>
  <li><strong>Scratching</strong> — each pointer/touch event draws filled arcs and lines. In <code>destination-out</code> mode, these punch transparent holes in the overlay.</li>
  <li><strong>Reveal check</strong> — roughly every 15% of draw events, <code>getImageData</code> samples 1-in-30 pixels across the canvas. When enough pixels are fully transparent, the prize is auto-revealed.</li>
  <li><strong>Reveal</strong> — the canvas is cleared, prize text and message are drawn, the Try Again button appears, confetti fires, and the device vibrates (if supported).</li>
</ol>

<hr>

<h2 id="prize-configuration">💰 Prize Configuration</h2>

<p>Prizes are defined in the <code>amounts</code> array near the top of the <code>&lt;script&gt;</code> block:</p>

<pre><code>const amounts = [
  { value: 10,  chance: 30 },
  { value: 25,  chance: 25 },
  { value: 30,  chance: 20 },
  { value: 50,  chance: 15 },
  { value: 100, chance: 10 },
];</code></pre>

<table>
  <thead>
    <tr><th>Prize</th><th>Message</th></tr>
  </thead>
  <tbody>
    <tr><td><code>PHP 10.00</code></td><td>Small gift! Better luck next year 🎄</td></tr>
    <tr><td><code>PHP 25.00</code></td><td>A little something! Enjoy it 🎁</td></tr>
    <tr><td><code>PHP 30.00</code></td><td>Nice! Your Christmas is brighter 🎅</td></tr>
    <tr><td><code>PHP 50.00</code></td><td>Great! Merry Christmas 🎄</td></tr>
    <tr><td><code>PHP 100.00</code></td><td>Wow! Jackpot! Happy Holidays! 🎉</td></tr>
  </tbody>
</table>

<p>Prize messages are set separately in the <code>messages</code> object, keyed by prize value:</p>

<pre><code>const messages = {
  10:  "Small gift! Better luck next year 🎄",
  25:  "A little something! Enjoy it 🎁",
  30:  "Nice! Your Christmas is brighter 🎅",
  50:  "Great! Merry Christmas 🎄",
  100: "Wow! Jackpot! Happy Holidays! 🎉"
};</code></pre>

<hr>

<h2 id="customization">🎨 Customization</h2>

<table>
  <thead>
    <tr><th>What to change</th><th>Variable / location</th><th>Notes</th></tr>
  </thead>
  <tbody>
    <tr><td>Prize amounts &amp; odds</td><td><code>const amounts</code></td><td>Edit <code>value</code> and <code>chance</code>. Weights are relative.</td></tr>
    <tr><td>Prize messages</td><td><code>const messages</code></td><td>Keyed by prize value. Emoji supported.</td></tr>
    <tr><td>Currency symbol</td><td><code>revealGift()</code> → <code>prizeText</code></td><td>Replace <code>PHP</code> with <code>$</code>, <code>€</code>, etc.</td></tr>
    <tr><td>Reveal threshold</td><td><code>let revealThreshold = 45</code></td><td>Percentage of pixels that must be cleared. Lower = easier.</td></tr>
    <tr><td>Brush size</td><td><code>const BRUSH_SIZE</code></td><td>Currently 40px on mobile, 35px on desktop.</td></tr>
    <tr><td>Overlay color</td><td><code>drawScratchOverlay()</code></td><td>Change the gradient stops to any color.</td></tr>
    <tr><td>Confetti count</td><td><code>createConfetti()</code> loop</td><td>Default 120 particles. Reduce for lower-end devices.</td></tr>
    <tr><td>Snow particle count</td><td><code>createSnow()</code> loop</td><td>Default 80 particles.</td></tr>
  </tbody>
</table>

<hr>

<h2 id="browser-support">🌐 Browser Support</h2>

<table>
  <thead>
    <tr><th>Browser</th><th>Support</th><th>Notes</th></tr>
  </thead>
  <tbody>
    <tr><td>Chrome / Edge</td><td>✅ Full</td><td>Including vibration API and touch events</td></tr>
    <tr><td>Safari / iOS</td><td>✅ Full</td><td>Uses <code>-webkit</code> prefixes where needed</td></tr>
    <tr><td>Firefox</td><td>✅ Full</td><td>Vibration API may be absent; degrades gracefully</td></tr>
    <tr><td>IE 11</td><td>❌ Not supported</td><td>Uses <code>aspect-ratio</code>, arrow functions, <code>const</code>/<code>let</code></td></tr>
  </tbody>
</table>

<hr>

<h2 id="license">📄 License</h2>

<p>This project is licensed under the <strong>MIT License</strong>. You are free to use, modify, and distribute it for personal or commercial purposes as long as the original license notice is included.</p>

<pre><code>MIT License

Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.</code></pre>

<hr>

<p style="text-align:center;">Made by Desxzy/Zenyxy &nbsp;·&nbsp; 🎄 Christmas Scratch Aguinaldo</p>

</div>
</body>
</html>
