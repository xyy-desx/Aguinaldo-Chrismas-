<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>README — Christmas Scratch Aguinaldo</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --red: #c62828;
    --red-dark: #8e0000;
    --red-light: #ffebee;
    --gold: #f9a825;
    --gold-light: #fff9e6;
    --green: #2e7d32;
    --green-light: #e8f5e9;
    --ink: #1a1a1a;
    --muted: #5c5c5c;
    --border: #e0e0e0;
    --surface: #fff8f0;
    --white: #ffffff;
    --radius: 12px;
    --mono: 'DM Mono', monospace;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--surface);
    color: var(--ink);
    line-height: 1.7;
    font-size: 15px;
  }

  /* ── HERO ── */
  .hero {
    background: var(--red);
    color: #fff;
    padding: 64px 32px 56px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image:
      radial-gradient(circle at 15% 20%, rgba(255,255,255,0.06) 0%, transparent 50%),
      radial-gradient(circle at 85% 75%, rgba(255,255,255,0.05) 0%, transparent 45%);
    pointer-events: none;
  }

  .hero-badge {
    display: inline-block;
    background: rgba(255,255,255,0.15);
    border: 1px solid rgba(255,255,255,0.3);
    color: #fff;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 5px 14px;
    border-radius: 999px;
    margin-bottom: 20px;
  }

  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(32px, 6vw, 52px);
    font-weight: 900;
    line-height: 1.1;
    margin-bottom: 16px;
    letter-spacing: -0.02em;
  }

  .hero p {
    font-size: 16px;
    opacity: 0.85;
    max-width: 480px;
    margin: 0 auto;
    line-height: 1.6;
  }

  .hero-tree {
    font-size: 56px;
    margin-bottom: 16px;
    display: block;
    filter: drop-shadow(0 4px 12px rgba(0,0,0,0.2));
  }

  /* ── LAYOUT ── */
  .page {
    max-width: 800px;
    margin: 0 auto;
    padding: 48px 24px 80px;
  }

  /* ── SECTION HEADINGS ── */
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
    color: var(--red-dark);
    margin: 48px 0 16px;
    padding-bottom: 10px;
    border-bottom: 2px solid var(--red-light);
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-title .icon { font-size: 20px; }

  /* ── OVERVIEW CARD ── */
  .overview-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 24px 28px;
    margin-top: 32px;
  }

  .overview-card p {
    color: var(--muted);
    font-size: 15px;
    line-height: 1.8;
  }

  /* ── FEATURES GRID ── */
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px;
    margin-top: 20px;
  }

  .feature-card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 20px;
  }

  .feature-card .feat-icon {
    font-size: 26px;
    margin-bottom: 10px;
    display: block;
  }

  .feature-card h3 {
    font-size: 14px;
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 6px;
  }

  .feature-card p {
    font-size: 13px;
    color: var(--muted);
    line-height: 1.6;
  }

  /* ── PRIZES TABLE ── */
  .prize-table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
    background: var(--white);
    border-radius: var(--radius);
    overflow: hidden;
    border: 1px solid var(--border);
  }

  .prize-table thead {
    background: var(--red);
    color: #fff;
  }

  .prize-table th {
    padding: 12px 16px;
    text-align: left;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }

  .prize-table td {
    padding: 12px 16px;
    font-size: 14px;
    border-bottom: 1px solid var(--border);
    color: var(--ink);
  }

  .prize-table tbody tr:last-child td { border-bottom: none; }
  .prize-table tbody tr:hover { background: var(--surface); }

  .prize-badge {
    display: inline-block;
    font-family: var(--mono);
    font-size: 13px;
    font-weight: 500;
    padding: 3px 10px;
    border-radius: 6px;
    background: var(--gold-light);
    color: #7a5c00;
    border: 1px solid #f9d96a;
  }

  .chance-bar-wrap {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .chance-bar {
    height: 6px;
    border-radius: 999px;
    background: var(--red);
    opacity: 0.8;
  }

  .chance-label {
    font-size: 13px;
    color: var(--muted);
    white-space: nowrap;
  }

  /* ── CODE BLOCKS ── */
  .code-block {
    background: #1e1e1e;
    color: #d4d4d4;
    border-radius: var(--radius);
    padding: 20px 24px;
    font-family: var(--mono);
    font-size: 13px;
    line-height: 1.7;
    overflow-x: auto;
    margin-top: 16px;
  }

  .code-block .comment { color: #6a9955; }
  .code-block .key { color: #9cdcfe; }
  .code-block .val { color: #ce9178; }
  .code-block .num { color: #b5cea8; }
  .code-block .kw { color: #c586c0; }

  /* ── HOW IT WORKS STEPS ── */
  .steps {
    display: flex;
    flex-direction: column;
    gap: 0;
    margin-top: 20px;
    position: relative;
  }

  .steps::before {
    content: '';
    position: absolute;
    left: 19px;
    top: 24px;
    bottom: 24px;
    width: 2px;
    background: var(--border);
    z-index: 0;
  }

  .step {
    display: flex;
    gap: 18px;
    align-items: flex-start;
    padding: 16px 0;
    position: relative;
    z-index: 1;
  }

  .step-num {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: var(--red);
    color: #fff;
    font-size: 15px;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }

  .step-content h3 {
    font-size: 15px;
    font-weight: 600;
    margin-bottom: 4px;
    color: var(--ink);
  }

  .step-content p {
    font-size: 13px;
    color: var(--muted);
    line-height: 1.6;
  }

  /* ── TAGS ── */
  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 16px;
  }

  .tag {
    font-size: 12px;
    font-weight: 500;
    padding: 4px 12px;
    border-radius: 999px;
    border: 1px solid var(--border);
    background: var(--white);
    color: var(--muted);
  }

  .tag.red { background: var(--red-light); color: var(--red-dark); border-color: #f5c6cb; }
  .tag.green { background: var(--green-light); color: var(--green); border-color: #a5d6a7; }
  .tag.gold { background: var(--gold-light); color: #7a5c00; border-color: #f9d96a; }

  /* ── CUSTOMIZATION TABLE ── */
  .custom-table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 20px;
    background: var(--white);
    border-radius: var(--radius);
    overflow: hidden;
    border: 1px solid var(--border);
  }

  .custom-table thead { background: #f5f5f5; }

  .custom-table th {
    padding: 10px 14px;
    text-align: left;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.05em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .custom-table td {
    padding: 11px 14px;
    font-size: 13px;
    border-bottom: 1px solid var(--border);
    color: var(--ink);
    vertical-align: top;
  }

  .custom-table tbody tr:last-child td { border-bottom: none; }

  .custom-table code {
    font-family: var(--mono);
    font-size: 12px;
    background: #f0f0f0;
    padding: 2px 6px;
    border-radius: 4px;
    color: var(--red-dark);
  }

  /* ── FOOTER ── */
  .footer {
    background: var(--white);
    border-top: 1px solid var(--border);
    padding: 32px 24px;
    text-align: center;
    font-size: 13px;
    color: var(--muted);
    margin-top: 48px;
  }

  .footer strong { color: var(--ink); }

  /* ── RESPONSIVE ── */
  @media (max-width: 600px) {
    .page { padding: 32px 16px 60px; }
    .hero { padding: 48px 20px 40px; }
    .features-grid { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <span class="hero-tree">🎄</span>
  <div class="hero-badge">Open Source · Vanilla JS · Mobile-First</div>
  <h1>Christmas Scratch Aguinaldo</h1>
  <p>A festive, fully client-side scratch card web app — reveal your holiday cash gift with a swipe of your finger.</p>
</div>

<div class="page">

  <!-- OVERVIEW -->
  <h2 class="section-title"><span class="icon">📖</span> Overview</h2>
  <div class="overview-card">
    <p>
      <strong>Christmas Scratch Aguinaldo</strong> is a zero-dependency, single-file HTML web app that simulates a scratch card lottery experience for the holidays. Users scratch a red overlay with their finger or mouse to uncover a cash prize. It is designed for mobile-first use, supports dark mode, and runs entirely in the browser — no server, no build step, no frameworks required.
    </p>
    <div class="tags" style="margin-top: 16px;">
      <span class="tag red">HTML5 Canvas</span>
      <span class="tag red">Vanilla JS</span>
      <span class="tag green">Mobile-First</span>
      <span class="tag green">No Dependencies</span>
      <span class="tag gold">Dark Mode</span>
      <span class="tag gold">Touch Support</span>
    </div>
  </div>

  <!-- FEATURES -->
  <h2 class="section-title"><span class="icon">✨</span> Features</h2>
  <div class="features-grid">
    <div class="feature-card">
      <span class="feat-icon">🖊️</span>
      <h3>Canvas Scratch Mechanic</h3>
      <p>Uses HTML5 Canvas with <code>destination-out</code> compositing to erase the red overlay as the user draws.</p>
    </div>
    <div class="feature-card">
      <span class="feat-icon">📱</span>
      <h3>Touch &amp; Mouse Support</h3>
      <p>Handles both <code>touchstart/move</code> and <code>mousedown/move</code> events with proper pointer position scaling.</p>
    </div>
    <div class="feature-card">
      <span class="feat-icon">🌙</span>
      <h3>Dark Mode Toggle</h3>
      <p>One-click toggle switches between light and dark themes with smooth CSS transitions.</p>
    </div>
    <div class="feature-card">
      <span class="feat-icon">🎉</span>
      <h3>Confetti &amp; Snow</h3>
      <p>Animated falling confetti on reveal plus continuous ambient snowfall rendered on a separate effects canvas.</p>
    </div>
    <div class="feature-card">
      <span class="feat-icon">🎲</span>
      <h3>Weighted Random Prizes</h3>
      <p>Each prize has a configurable probability weight. Lower-value prizes appear more often than jackpots.</p>
    </div>
    <div class="feature-card">
      <span class="feat-icon">📐</span>
      <h3>Responsive &amp; DPR-Aware</h3>
      <p>Canvas scales with <code>devicePixelRatio</code> for crisp rendering on retina screens of any size.</p>
    </div>
  </div>

  <!-- HOW IT WORKS -->
  <h2 class="section-title"><span class="icon">⚙️</span> How It Works</h2>
  <div class="steps">
    <div class="step">
      <div class="step-num">1</div>
      <div class="step-content">
        <h3>Prize is selected on load</h3>
        <p>A weighted random algorithm picks a prize from the <code>amounts</code> array. Higher-value prizes have lower <code>chance</code> weights, making them rarer.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">2</div>
      <div class="step-content">
        <h3>Red overlay is drawn on the canvas</h3>
        <p>A rich crimson-to-dark-red gradient fills the canvas using <code>source-over</code> compositing. The canvas then switches to <code>destination-out</code> mode so any subsequent drawing erases the overlay.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">3</div>
      <div class="step-content">
        <h3>User scratches with finger or mouse</h3>
        <p>Each pointer/touch move event draws filled arcs and line strokes — which, in <code>destination-out</code> mode, punch holes in the red layer to reveal the card beneath.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">4</div>
      <div class="step-content">
        <h3>Reveal is detected via pixel sampling</h3>
        <p>Every ~15% of draw calls, <code>getImageData</code> samples 1-in-30 pixels. When &gt;45% of sampled pixels have alpha = 0 (fully transparent), the prize is revealed automatically.</p>
      </div>
    </div>
    <div class="step">
      <div class="step-num">5</div>
      <div class="step-content">
        <h3>Prize is displayed and confetti fires</h3>
        <p>The canvas is cleared, the prize amount and message are drawn in large text, the Try Again button appears, and 120 confetti particles begin falling.</p>
      </div>
    </div>
  </div>

  <!-- PRIZE ODDS -->
  <h2 class="section-title"><span class="icon">💰</span> Prize Odds</h2>
  <table class="prize-table">
    <thead>
      <tr>
        <th>Prize</th>
        <th>Message</th>
        <th>Chance Weight</th>
        <th>Approx. Probability</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="prize-badge">PHP 10.00</span></td>
        <td>Small gift! Better luck next year 🎄</td>
        <td>
          <div class="chance-bar-wrap">
            <div class="chance-bar" style="width: 90px;"></div>
            <span class="chance-label">30</span>
          </div>
        </td>
        <td>30%</td>
      </tr>
      <tr>
        <td><span class="prize-badge">PHP 25.00</span></td>
        <td>A little something! Enjoy it 🎁</td>
        <td>
          <div class="chance-bar-wrap">
            <div class="chance-bar" style="width: 75px;"></div>
            <span class="chance-label">25</span>
          </div>
        </td>
        <td>25%</td>
      </tr>
      <tr>
        <td><span class="prize-badge">PHP 30.00</span></td>
        <td>Nice! Your Christmas is brighter 🎅</td>
        <td>
          <div class="chance-bar-wrap">
            <div class="chance-bar" style="width: 60px;"></div>
            <span class="chance-label">20</span>
          </div>
        </td>
        <td>20%</td>
      </tr>
      <tr>
        <td><span class="prize-badge">PHP 50.00</span></td>
        <td>Great! Merry Christmas 🎄</td>
        <td>
          <div class="chance-bar-wrap">
            <div class="chance-bar" style="width: 45px;"></div>
            <span class="chance-label">15</span>
          </div>
        </td>
        <td>15%</td>
      </tr>
      <tr>
        <td><span class="prize-badge">PHP 100.00</span></td>
        <td>Wow! Jackpot! Happy Holidays! 🎉</td>
        <td>
          <div class="chance-bar-wrap">
            <div class="chance-bar" style="width: 30px;"></div>
            <span class="chance-label">10</span>
          </div>
        </td>
        <td>10%</td>
      </tr>
    </tbody>
  </table>

  <!-- GETTING STARTED -->
  <h2 class="section-title"><span class="icon">🚀</span> Getting Started</h2>
  <div class="overview-card">
    <p>No installation required. Just open the file in any modern browser.</p>
  </div>
  <div class="code-block">
<span class="comment"># Clone or download the file</span>
git clone https://github.com/your-username/christmas-scratch-aguinaldo.git

<span class="comment"># Open directly — no server needed</span>
open index.html

<span class="comment"># Or serve locally</span>
npx serve .
  </div>

  <!-- CUSTOMIZATION -->
  <h2 class="section-title"><span class="icon">🎨</span> Customization</h2>
  <table class="custom-table">
    <thead>
      <tr>
        <th>What to change</th>
        <th>Where to find it</th>
        <th>Notes</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Prize amounts &amp; odds</strong></td>
        <td><code>const amounts = [...]</code></td>
        <td>Edit <code>value</code> for the amount and <code>chance</code> for relative weight. Weights are totaled automatically.</td>
      </tr>
      <tr>
        <td><strong>Prize messages</strong></td>
        <td><code>const messages = {...}</code></td>
        <td>Each key maps a prize value to a display string. Emoji are supported.</td>
      </tr>
      <tr>
        <td><strong>Reveal threshold</strong></td>
        <td><code>let revealThreshold = 45</code></td>
        <td>Percentage (0–100) of pixels that must be cleared before auto-reveal. Lower = easier to reveal.</td>
      </tr>
      <tr>
        <td><strong>Overlay color</strong></td>
        <td><code>--scratch-overlay</code> CSS var + <code>drawScratchOverlay()</code></td>
        <td>Change the gradient stops in <code>drawScratchOverlay</code> to any color.</td>
      </tr>
      <tr>
        <td><strong>Brush size</strong></td>
        <td><code>const BRUSH_SIZE = ...</code></td>
        <td>Larger values make it easier to scratch. Currently responsive: 40px on mobile, 35px on desktop.</td>
      </tr>
      <tr>
        <td><strong>Confetti count</strong></td>
        <td><code>createConfetti()</code> — loop count</td>
        <td>Default is 120 particles. Reduce for lower-end devices.</td>
      </tr>
      <tr>
        <td><strong>Currency symbol</strong></td>
        <td><code>revealGift()</code> — <code>const prizeText</code></td>
        <td>Replace <code>PHP</code> with <code>$</code>, <code>€</code>, etc.</td>
      </tr>
    </tbody>
  </table>

  <!-- FILE STRUCTURE -->
  <h2 class="section-title"><span class="icon">📁</span> File Structure</h2>
  <div class="code-block">
<span class="key">index.html</span>          <span class="comment">← entire app (single file)</span>
│
├── &lt;style&gt;          <span class="comment">← all CSS including dark mode &amp; responsive rules</span>
│
├── &lt;body&gt;
│   ├── #darkToggle  <span class="comment">← fixed top-right theme button</span>
│   ├── .container   <span class="comment">← centered layout: heading, subtext, card, button</span>
│   │   ├── #scratchCardContainer  <span class="comment">← positions canvas over prize text</span>
│   │   │   ├── #scratchCard       <span class="comment">← scratch canvas (DPR-scaled)</span>
│   │   │   └── #scratchText       <span class="comment">← "SCRATCH ME" label (hidden after reveal)</span>
│   │   └── #tryAgainBtn           <span class="comment">← shown after reveal</span>
│   └── #effects     <span class="comment">← full-screen fixed canvas for snow &amp; confetti</span>
│
└── &lt;script&gt;         <span class="comment">← all JS: prize logic, canvas drawing, effects</span>
  </div>

  <!-- BROWSER SUPPORT -->
  <h2 class="section-title"><span class="icon">🌐</span> Browser Support</h2>
  <div class="features-grid" style="margin-top: 20px;">
    <div class="feature-card">
      <span class="feat-icon">✅</span>
      <h3>Chrome / Edge</h3>
      <p>Full support including touch events, DPR scaling, and vibration API.</p>
    </div>
    <div class="feature-card">
      <span class="feat-icon">✅</span>
      <h3>Safari / iOS</h3>
      <p>Full support. Uses <code>-webkit</code> prefixes for tap highlight and touch callout suppression.</p>
    </div>
    <div class="feature-card">
      <span class="feat-icon">✅</span>
      <h3>Firefox</h3>
      <p>Full support. Vibration API may not be available but degrades gracefully.</p>
    </div>
    <div class="feature-card">
      <span class="feat-icon">⚠️</span>
      <h3>IE 11</h3>
      <p>Not supported. Uses <code>aspect-ratio</code>, <code>const</code>/<code>let</code>, and arrow functions.</p>
    </div>
  </div>

  <!-- LICENSE -->
  <h2 class="section-title"><span class="icon">📄</span> License</h2>
  <div class="overview-card">
    <p>This project is released under the <strong>MIT License</strong>. You are free to use, copy, modify, merge, publish, and distribute this code — including for commercial projects — as long as the original license notice is retained.</p>
  </div>

</div>

<!-- FOOTER -->
<div class="footer">
  Built with ❤️ for the holidays · <strong>Christmas Scratch Aguinaldo</strong> · MIT License
</div>

</body>
</html>
