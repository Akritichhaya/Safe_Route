<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SafeRoute Bengaluru — README</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --blr-magenta: #C2185B;
    --blr-deep: #880E4F;
    --blr-light: #FCE4EC;
    --blr-teal: #00695C;
    --blr-amber: #E65100;
    --blr-ink: #1A1225;
    --blr-muted: #6B5B6E;
    --blr-surface: #FFF8FB;
    --blr-card: #FFFFFF;
    --blr-border: #F0D8E5;
    --blr-green: #2E7D32;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--blr-surface);
    color: var(--blr-ink);
    line-height: 1.7;
    font-size: 16px;
  }

  /* ─── HERO ─── */
  .hero {
    background: var(--blr-ink);
    position: relative;
    overflow: hidden;
    padding: 80px 48px 64px;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 60% 80% at 80% 50%, rgba(194,24,91,0.25) 0%, transparent 60%),
      radial-gradient(ellipse 40% 60% at 10% 80%, rgba(0,105,92,0.15) 0%, transparent 60%);
  }

  .hero-grid {
    position: relative;
    max-width: 860px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: end;
    gap: 40px;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: 'DM Sans', sans-serif;
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--blr-magenta);
    background: rgba(194,24,91,0.12);
    border: 1px solid rgba(194,24,91,0.3);
    border-radius: 100px;
    padding: 5px 14px;
    margin-bottom: 20px;
  }

  .badge .dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--blr-magenta);
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.8); }
  }

  .hero h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(38px, 6vw, 62px);
    font-weight: 800;
    color: #FFFFFF;
    line-height: 1.05;
    letter-spacing: -0.02em;
    margin-bottom: 16px;
  }

  .hero h1 span {
    color: var(--blr-magenta);
  }

  .hero-sub {
    font-size: 17px;
    color: rgba(255,255,255,0.6);
    max-width: 520px;
    margin-bottom: 32px;
    font-weight: 300;
  }

  .hero-actions {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }

  .btn-primary {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: var(--blr-magenta);
    color: #fff;
    text-decoration: none;
    font-family: 'DM Sans', sans-serif;
    font-size: 14px;
    font-weight: 500;
    padding: 12px 24px;
    border-radius: 8px;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-primary:hover { background: var(--blr-deep); transform: translateY(-1px); }

  .btn-outline {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(255,255,255,0.07);
    color: rgba(255,255,255,0.85);
    text-decoration: none;
    font-family: 'DM Sans', sans-serif;
    font-size: 14px;
    font-weight: 500;
    padding: 12px 24px;
    border-radius: 8px;
    border: 1px solid rgba(255,255,255,0.15);
    transition: background 0.2s;
  }
  .btn-outline:hover { background: rgba(255,255,255,0.12); }

  .version-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    border-radius: 12px;
    padding: 20px 24px;
    text-align: center;
    min-width: 120px;
  }
  .version-card .v-num {
    font-family: 'Syne', sans-serif;
    font-size: 32px;
    font-weight: 800;
    color: var(--blr-magenta);
    display: block;
    line-height: 1;
  }
  .version-card .v-label {
    font-size: 11px;
    color: rgba(255,255,255,0.4);
    text-transform: uppercase;
    letter-spacing: 0.08em;
    margin-top: 4px;
    display: block;
  }

  /* ─── CONTENT ─── */
  .content {
    max-width: 860px;
    margin: 0 auto;
    padding: 64px 48px 80px;
  }

  /* ─── SECTION TITLES ─── */
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--blr-magenta);
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--blr-border);
  }

  h2 {
    font-family: 'Syne', sans-serif;
    font-size: 26px;
    font-weight: 700;
    color: var(--blr-ink);
    margin-bottom: 24px;
    letter-spacing: -0.01em;
  }

  /* ─── FEATURE GRID ─── */
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 16px;
    margin-bottom: 56px;
  }

  .feature-card {
    background: var(--blr-card);
    border: 1px solid var(--blr-border);
    border-radius: 12px;
    padding: 22px 20px;
    transition: box-shadow 0.2s, transform 0.2s;
    position: relative;
    overflow: hidden;
  }

  .feature-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: var(--blr-magenta);
    opacity: 0;
    transition: opacity 0.2s;
  }

  .feature-card:hover {
    box-shadow: 0 8px 24px rgba(194,24,91,0.08);
    transform: translateY(-2px);
  }
  .feature-card:hover::before { opacity: 1; }

  .feature-icon {
    width: 36px;
    height: 36px;
    border-radius: 8px;
    background: var(--blr-light);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    margin-bottom: 12px;
  }

  .feature-card h3 {
    font-family: 'Syne', sans-serif;
    font-size: 14px;
    font-weight: 700;
    color: var(--blr-ink);
    margin-bottom: 6px;
  }

  .feature-card p {
    font-size: 13px;
    color: var(--blr-muted);
    line-height: 1.6;
  }

  /* ─── FILE INFO ─── */
  .file-row {
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 16px 20px;
    background: var(--blr-card);
    border: 1px solid var(--blr-border);
    border-radius: 10px;
    margin-bottom: 10px;
  }

  .file-icon {
    width: 38px;
    height: 38px;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    background: var(--blr-light);
    flex-shrink: 0;
  }

  .file-name {
    font-family: 'DM Sans', monospace;
    font-size: 14px;
    font-weight: 500;
    color: var(--blr-ink);
    background: rgba(194,24,91,0.06);
    padding: 2px 8px;
    border-radius: 4px;
    border: 1px solid rgba(194,24,91,0.12);
  }

  .file-desc {
    font-size: 13px;
    color: var(--blr-muted);
  }

  /* ─── CODE BLOCKS ─── */
  .code-block {
    background: #1A1225;
    border-radius: 10px;
    overflow: hidden;
    margin: 16px 0 24px;
  }

  .code-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 16px;
    border-bottom: 1px solid rgba(255,255,255,0.06);
  }

  .code-lang {
    font-size: 11px;
    color: rgba(255,255,255,0.35);
    text-transform: uppercase;
    letter-spacing: 0.08em;
    font-family: 'DM Sans', monospace;
  }

  .code-dots {
    display: flex;
    gap: 5px;
  }
  .code-dots span {
    width: 8px; height: 8px;
    border-radius: 50%;
  }
  .code-dots span:nth-child(1) { background: #FF5F56; }
  .code-dots span:nth-child(2) { background: #FFBD2E; }
  .code-dots span:nth-child(3) { background: #27C93F; }

  pre {
    margin: 0;
    padding: 16px 20px;
    font-family: 'DM Mono', 'Fira Code', monospace;
    font-size: 13px;
    line-height: 1.7;
    color: rgba(255,255,255,0.8);
    overflow-x: auto;
  }

  .comment { color: rgba(255,255,255,0.3); }
  .kw { color: #FF79C6; }
  .str { color: #F1FA8C; }
  .cmd { color: #8BE9FD; }

  /* ─── DEPLOY GRID ─── */
  .deploy-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
    margin-bottom: 48px;
  }

  .deploy-card {
    background: var(--blr-card);
    border: 1px solid var(--blr-border);
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    transition: border-color 0.2s, box-shadow 0.2s;
  }

  .deploy-card:hover {
    border-color: var(--blr-magenta);
    box-shadow: 0 4px 20px rgba(194,24,91,0.08);
  }

  .deploy-logo {
    font-size: 24px;
    margin-bottom: 8px;
  }

  .deploy-name {
    font-family: 'Syne', sans-serif;
    font-size: 14px;
    font-weight: 700;
    color: var(--blr-ink);
    margin-bottom: 4px;
  }

  .deploy-desc {
    font-size: 12px;
    color: var(--blr-muted);
  }

  /* ─── NOTICE BLOCK ─── */
  .notice {
    background: rgba(230,81,0,0.06);
    border: 1px solid rgba(230,81,0,0.2);
    border-left: 3px solid var(--blr-amber);
    border-radius: 8px;
    padding: 16px 20px;
    margin-bottom: 48px;
  }

  .notice p {
    font-size: 14px;
    color: var(--blr-ink);
    display: flex;
    gap: 10px;
    align-items: flex-start;
  }

  .notice strong {
    color: var(--blr-amber);
    font-weight: 600;
  }

  /* ─── TECH STACK ─── */
  .tech-row {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    margin-bottom: 48px;
  }

  .tech-pill {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-size: 13px;
    font-weight: 500;
    padding: 7px 14px;
    border-radius: 100px;
    background: var(--blr-card);
    border: 1px solid var(--blr-border);
    color: var(--blr-ink);
  }

  /* ─── FOOTER ─── */
  .footer {
    background: var(--blr-ink);
    padding: 32px 48px;
    text-align: center;
  }

  .footer p {
    font-size: 13px;
    color: rgba(255,255,255,0.3);
  }

  .footer strong {
    color: var(--blr-magenta);
  }

  /* ─── DIVIDER ─── */
  .section-gap { margin-bottom: 56px; }

  /* ─── STEP LIST ─── */
  .steps {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 8px;
  }

  .step {
    display: flex;
    align-items: flex-start;
    gap: 14px;
  }

  .step-num {
    width: 26px;
    height: 26px;
    border-radius: 50%;
    background: var(--blr-magenta);
    color: #fff;
    font-size: 12px;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    margin-top: 2px;
  }

  .step p {
    font-size: 14px;
    color: var(--blr-muted);
  }

  code {
    font-family: 'DM Mono', monospace;
    font-size: 13px;
    background: rgba(194,24,91,0.07);
    border: 1px solid rgba(194,24,91,0.14);
    padding: 1px 6px;
    border-radius: 4px;
    color: var(--blr-deep);
  }

  @media (max-width: 600px) {
    .hero { padding: 48px 24px 48px; }
    .hero-grid { grid-template-columns: 1fr; }
    .version-card { display: none; }
    .content { padding: 40px 24px 60px; }
    .deploy-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- ═══════════════ HERO ═══════════════ -->
<header class="hero">
  <div class="hero-grid">
    <div>
      <div class="badge"><span class="dot"></span> Static · Open Source · No login required</div>
      <h1>Safe<span>Route</span><br>Bengaluru</h1>
      <p class="hero-sub">A crowd-sourced women's safety webapp for Namma Bengaluru — interactive maps, SOS tools, women-only transport, and smart route planning. All in a single HTML file.</p>
      <div class="hero-actions">
        <a href="https://akritichhaya.github.io/Safe_Route/Saferoute_bengaluru.html" target="_blank" class="btn-primary">
          🚀 Live Demo ↗
        </a>
        <a href="https://github.com/akritichhaya/Safe_Route" target="_blank" class="btn-outline">
          ⭐ View on GitHub
        </a>
      </div>
    </div>
    <div class="version-card">
      <span class="v-num">v2.0</span>
      <span class="v-label">Latest</span>
    </div>
  </div>
</header>

<!-- ═══════════════ CONTENT ═══════════════ -->
<main class="content">

  <!-- OVERVIEW -->
  <div class="section-gap">
    <div class="section-title">Overview</div>
    <p style="font-size:16px; color:var(--blr-muted); max-width:640px; margin-bottom:0;">
      SafeRoute Bengaluru is a browser-based safety tool designed for women and commuters in Bengaluru. It combines real crowd-sourced incident data, WhatsApp-powered alerts, night check-in timers, and women-only transport directories — entirely client-side, no server needed.
    </p>
  </div>

  <!-- FEATURES -->
  <div class="section-gap">
    <div class="section-title">Features</div>
    <div class="features-grid">
      <div class="feature-card">
        <div class="feature-icon">🗺️</div>
        <h3>Live Safety Map</h3>
        <p>Interactive Bengaluru map with crowd-sourced hotspot markers at real coordinates. Filter by time of day.</p>
      </div>
      <div class="feature-card">
        <div class="feature-icon">🚨</div>
        <h3>SOS Emergency Modal</h3>
        <p>One-tap emergency with helplines, fake call trigger, WhatsApp alerts, and live location sharing.</p>
      </div>
      <div class="feature-card">
        <div class="feature-icon">🌙</div>
        <h3>Night Check-In Timer</h3>
        <p>Set a countdown. If you don't check in, an automatic SOS is sent to your contacts via WhatsApp.</p>
      </div>
      <div class="feature-card">
        <div class="feature-icon">🚺</div>
        <h3>Women-Only Transport</h3>
        <p>Sakhi, Vanitha & more — curated women-only cab services with direct WhatsApp booking links.</p>
      </div>
      <div class="feature-card">
        <div class="feature-icon">🏛️</div>
        <h3>City Partner Alerts</h3>
        <p>One-tap official alerts to BBMP, Bengaluru City Police, and BMTC directly from the app.</p>
      </div>
      <div class="feature-card">
        <div class="feature-icon">🧭</div>
        <h3>Safe Route Planner</h3>
        <p>Route suggestions that avoid high-risk zones, with sharing via WhatsApp and Google Maps integration.</p>
      </div>
    </div>
  </div>

  <!-- FILES -->
  <div class="section-gap">
    <div class="section-title">Project Files</div>
    <div class="file-row">
      <div class="file-icon">📄</div>
      <div>
        <div class="file-name">Saferoute_bengaluru.html</div>
        <div class="file-desc" style="margin-top:4px;">Main application — all HTML, CSS, and JavaScript in a single file</div>
      </div>
    </div>
    <div class="file-row">
      <div class="file-icon">📝</div>
      <div>
        <div class="file-name">README.md</div>
        <div class="file-desc" style="margin-top:4px;">Project documentation and setup instructions</div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section-gap">
    <div class="section-title">Tech Stack</div>
    <div class="tech-row">
      <span class="tech-pill">🍃 Leaflet.js</span>
      <span class="tech-pill">🔤 Google Fonts</span>
      <span class="tech-pill">💬 WhatsApp API</span>
      <span class="tech-pill">📍 Geolocation API</span>
      <span class="tech-pill">🗺️ Google Maps</span>
      <span class="tech-pill">🌐 No Backend</span>
    </div>
  </div>

  <!-- LOCAL TESTING -->
  <div class="section-gap">
    <div class="section-title">Local Testing</div>
    <p style="font-size:15px; color:var(--blr-muted); margin-bottom:20px;">Open the file directly in your browser, or run a local server:</p>

    <div class="steps" style="margin-bottom:20px;">
      <div class="step">
        <div class="step-num">1</div>
        <p>Navigate to your project folder</p>
      </div>
      <div class="step">
        <div class="step-num">2</div>
        <p>Start a Python server on port <code>8000</code></p>
      </div>
      <div class="step">
        <div class="step-num">3</div>
        <p>Open <code>http://localhost:8000/Saferoute_bengaluru.html</code> in your browser</p>
      </div>
    </div>

    <div class="code-block">
      <div class="code-header">
        <div class="code-dots"><span></span><span></span><span></span></div>
        <span class="code-lang">PowerShell</span>
      </div>
      <pre><span class="comment"># Navigate to project folder</span>
<span class="cmd">Set-Location</span> <span class="kw">-Path</span> <span class="str">'D:\Safe_Route'</span>

<span class="comment"># Start local server</span>
<span class="cmd">python</span> -m http.server <span class="str">8000</span></pre>
    </div>
  </div>

  <!-- DEPLOYMENT -->
  <div class="section-gap">
    <div class="section-title">Deployment</div>
    <p style="font-size:15px; color:var(--blr-muted); margin-bottom:24px;">This is a static site — deploy anywhere with zero build steps.</p>

    <div class="deploy-grid">
      <div class="deploy-card">
        <div class="deploy-logo">🐙</div>
        <div class="deploy-name">GitHub Pages</div>
        <div class="deploy-desc">Push to repo → enable Pages from settings → live in minutes</div>
      </div>
      <div class="deploy-card">
        <div class="deploy-logo">▲</div>
        <div class="deploy-name">Netlify</div>
        <div class="deploy-desc">Connect GitHub repo, deploy from root — no build command needed</div>
      </div>
      <div class="deploy-card">
        <div class="deploy-logo">◆</div>
        <div class="deploy-name">Vercel</div>
        <div class="deploy-desc">Import repo → deploy instantly from root folder</div>
      </div>
    </div>
  </div>

  <!-- NOTES -->
  <div class="section-gap">
    <div class="section-title">Notes</div>
    <div class="notice">
      <p>⚠️ <span><strong>Test Mode:</strong> All helpline numbers are currently set to <code>9155647042</code> for safe testing. Update these before production use.</span></p>
    </div>
    <ul style="list-style:none; display:flex; flex-direction:column; gap:10px;">
      <li style="font-size:14px; color:var(--blr-muted); display:flex; gap:8px; align-items:flex-start;"><span>✅</span> 100% anonymous — no login, no data stored on any server</li>
      <li style="font-size:14px; color:var(--blr-muted); display:flex; gap:8px; align-items:flex-start;"><span>✅</span> Session-only reports — nothing persists between browser sessions</li>
      <li style="font-size:14px; color:var(--blr-muted); display:flex; gap:8px; align-items:flex-start;"><span>✅</span> Leaflet.js and Google Fonts loaded from CDN</li>
      <li style="font-size:14px; color:var(--blr-muted); display:flex; gap:8px; align-items:flex-start;"><span>✅</span> No backend server required — runs entirely in the browser</li>
    </ul>
  </div>

  <!-- LICENSE -->
  <div>
    <div class="section-title">License</div>
    <p style="font-size:15px; color:var(--blr-muted);">Use and adapt this project freely for safety awareness and testing purposes. Built with 💜 for Bengaluru.</p>
  </div>

</main>

<!-- FOOTER -->
<footer class="footer">
  <p>SafeRoute Bengaluru &nbsp;·&nbsp; <strong>v2.0</strong> &nbsp;·&nbsp; Static · No login · Open source</p>
  <p style="margin-top:8px;">Made for Namma Bengaluru 🌸</p>
</footer>

</body>
</html>
