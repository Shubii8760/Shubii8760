<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Shubham Sharma – PHP & WordPress Expert</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@700;800&display=swap');

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: #0a0a0f;
    color: #e8e6f0;
    font-family: 'Space Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── HERO ── */
  .hero {
    position: relative;
    padding: 60px 40px 50px;
    border-bottom: 1px solid #1e1e2e;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(99,60,255,0.18) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero::after {
    content: '';
    position: absolute;
    bottom: -60px; left: 200px;
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(0,210,180,0.1) 0%, transparent 70%);
    pointer-events: none;
  }

  .location-tag {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: #1a1a2e;
    border: 1px solid #2a2a4a;
    border-radius: 20px;
    padding: 5px 14px;
    font-size: 11px;
    color: #8888bb;
    letter-spacing: 0.08em;
    margin-bottom: 20px;
  }

  .dot-live {
    width: 6px; height: 6px;
    background: #00d2b4;
    border-radius: 50%;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }

  .name {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: clamp(36px, 6vw, 64px);
    line-height: 1;
    letter-spacing: -0.02em;
    background: linear-gradient(135deg, #ffffff 0%, #c8b8ff 50%, #00d2b4 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 12px;
  }

  .role-line {
    font-size: 12px;
    color: #5a5a7a;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 28px;
  }

  .role-line span { color: #7c5cfc; }

  .tagline {
    font-size: 14px;
    color: #9090b0;
    line-height: 1.7;
    max-width: 520px;
    border-left: 2px solid #7c5cfc;
    padding-left: 16px;
  }

  .tagline strong { color: #00d2b4; font-weight: 400; }

  /* ── SECTIONS ── */
  .section {
    padding: 40px 40px;
    border-bottom: 1px solid #1a1a2a;
  }

  .sec-label {
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #7c5cfc;
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .sec-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, #2a2a4a, transparent);
  }

  /* ── STACK CHIPS ── */
  .stack-grid { display: flex; flex-wrap: wrap; gap: 8px; }

  .chip {
    padding: 6px 14px;
    border-radius: 4px;
    font-size: 11px;
    letter-spacing: 0.05em;
    border: 1px solid;
    transition: transform 0.2s;
    cursor: default;
  }

  .chip:hover { transform: translateY(-2px); }

  .chip-php    { background: #1c1240; border-color: #4a2cff; color: #a08cff; }
  .chip-green  { background: #0c2020; border-color: #00b894; color: #00d2b4; }
  .chip-red    { background: #200c10; border-color: #c0392b; color: #ff6b6b; }
  .chip-gray   { background: #161620; border-color: #3a3a5a; color: #8888bb; }
  .chip-orange { background: #201408; border-color: #d4590e; color: #ff8c42; }

  /* ── EXPERTISE CARDS ── */
  .expertise-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 16px;
  }

  .exp-card {
    background: #0e0e1a;
    border: 1px solid #1e1e30;
    border-radius: 8px;
    padding: 20px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s;
  }

  .exp-card:hover { border-color: #7c5cfc; }

  .exp-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
  }

  .exp-card.purple::before { background: linear-gradient(to right, #7c5cfc, transparent); }
  .exp-card.teal::before   { background: linear-gradient(to right, #00d2b4, transparent); }
  .exp-card.orange::before { background: linear-gradient(to right, #ff8c42, transparent); }
  .exp-card.pink::before   { background: linear-gradient(to right, #ff6b9d, transparent); }

  .exp-icon  { font-size: 20px; margin-bottom: 10px; }

  .exp-title {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 700;
    color: #e0deff;
    margin-bottom: 8px;
    letter-spacing: 0.02em;
  }

  .exp-list { list-style: none; }

  .exp-list li {
    font-size: 10px;
    color: #6666aa;
    padding: 3px 0;
    display: flex;
    align-items: center;
    gap: 6px;
    letter-spacing: 0.02em;
  }

  .exp-list li::before { content: '—'; color: #3a3a5a; font-size: 9px; }

  /* ── MISSION BOX ── */
  .mission-box {
    background: linear-gradient(135deg, #0e0c1e 0%, #0c1a18 100%);
    border: 1px solid #1e1e30;
    border-radius: 8px;
    padding: 28px 32px;
    position: relative;
    overflow: hidden;
  }

  .mission-box::after {
    content: '{ }';
    position: absolute;
    right: 32px;
    top: 50%;
    transform: translateY(-50%);
    font-size: 80px;
    color: #ffffff06;
    font-family: 'Space Mono', monospace;
    pointer-events: none;
  }

  .mission-item {
    display: flex;
    align-items: flex-start;
    gap: 16px;
    padding: 10px 0;
    border-bottom: 1px solid #1a1a2a;
  }

  .mission-item:last-child { border-bottom: none; }

  .mi-key {
    font-size: 10px;
    color: #7c5cfc;
    letter-spacing: 0.1em;
    min-width: 90px;
    padding-top: 2px;
  }

  .mi-val { font-size: 12px; color: #9090b0; line-height: 1.6; }
  .mi-val .highlight { color: #00d2b4; }

  /* ── CONNECT ── */
  .connect-row { display: flex; gap: 12px; flex-wrap: wrap; }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 20px;
    border-radius: 4px;
    font-size: 11px;
    font-family: 'Space Mono', monospace;
    letter-spacing: 0.08em;
    cursor: pointer;
    border: 1px solid;
    text-decoration: none;
    transition: all 0.2s;
  }

  .btn-primary { background: #7c5cfc; border-color: #7c5cfc; color: #fff; }
  .btn-primary:hover { background: #9070ff; border-color: #9070ff; }

  .btn-outline { background: transparent; border-color: #2a2a4a; color: #7070a0; }
  .btn-outline:hover { border-color: #7c5cfc; color: #c0b0ff; }

  /* ── QUOTE ── */
  .quote-bar {
    background: #0a0a14;
    padding: 24px 40px;
    display: flex;
    align-items: center;
    gap: 16px;
  }

  .quote-mark {
    font-size: 40px;
    color: #7c5cfc;
    font-family: Georgia, serif;
    line-height: 1;
    opacity: 0.4;
  }

  .quote-text { font-size: 12px; color: #5a5a7a; font-style: italic; line-height: 1.6; }
  .quote-text strong { color: #7070a0; font-style: normal; font-weight: 400; }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="location-tag">
    <span class="dot-live"></span>
    Shimla, Himachal Pradesh · Available for hire
  </div>
  <div class="name">Shubham<br>Sharma</div>
  <div class="role-line">PHP Developer · <span>WooCommerce Expert</span> · Laravel Specialist</div>
  <p class="tagline">
    Crafting <strong>custom WooCommerce plugins</strong>, Laravel applications, and server architectures —
    from the mountains of HP to production servers worldwide.
  </p>
</div>

<!-- STACK -->
<div class="section">
  <div class="sec-label">// tech stack</div>
  <div class="stack-grid">
    <span class="chip chip-php">PHP 8.x</span>
    <span class="chip chip-red">Laravel</span>
    <span class="chip chip-green">WooCommerce</span>
    <span class="chip chip-gray">WordPress</span>
    <span class="chip chip-green">MySQL</span>
    <span class="chip chip-gray">REST API</span>
    <span class="chip chip-orange">Nginx</span>
    <span class="chip chip-php">Laravel Forge</span>
    <span class="chip chip-orange">DigitalOcean</span>
    <span class="chip chip-gray">Ubuntu Server</span>
    <span class="chip chip-gray">JavaScript</span>
    <span class="chip chip-php">jQuery</span>
    <span class="chip chip-gray">Bootstrap 5</span>
    <span class="chip chip-orange">Redis</span>
    <span class="chip chip-gray">Git</span>
    <span class="chip chip-green">Stripe · Razorpay · PayU</span>
  </div>
</div>

<!-- EXPERTISE -->
<div class="section">
  <div class="sec-label">// expertise</div>
  <div class="expertise-grid">

    <div class="exp-card purple">
      <div class="exp-icon">🛒</div>
      <div class="exp-title">WooCommerce</div>
      <ul class="exp-list">
        <li>Custom plugins &amp; product types</li>
        <li>Multi-step checkout flows</li>
        <li>Payment gateway integration</li>
        <li>WooCommerce Subscriptions</li>
        <li>REST API &amp; headless backends</li>
        <li>Performance &amp; query tuning</li>
      </ul>
    </div>

    <div class="exp-card teal">
      <div class="exp-icon">🔥</div>
      <div class="exp-title">Laravel Forge</div>
      <ul class="exp-list">
        <li>Ubuntu/Nginx provisioning</li>
        <li>Zero-downtime deployments</li>
        <li>SSL, daemons, cron jobs</li>
        <li>Queue workers &amp; Redis</li>
        <li>DO · Linode · AWS</li>
      </ul>
    </div>

    <div class="exp-card orange">
      <div class="exp-icon">⚡</div>
      <div class="exp-title">Laravel / PHP</div>
      <ul class="exp-list">
        <li>Eloquent ORM &amp; relationships</li>
        <li>Service &amp; repository pattern</li>
        <li>JSON:API REST endpoints</li>
        <li>Livewire &amp; Blade components</li>
        <li>PHPUnit + Pest testing</li>
        <li>Custom package development</li>
      </ul>
    </div>

    <div class="exp-card pink">
      <div class="exp-icon">📦</div>
      <div class="exp-title">Services Offered</div>
      <ul class="exp-list">
        <li>Custom WooCommerce dev</li>
        <li>Laravel SaaS &amp; dashboards</li>
        <li>Server setup via Forge</li>
        <li>WordPress performance audit</li>
        <li>Security hardening</li>
        <li>Mobile &amp; headless APIs</li>
      </ul>
    </div>

  </div>
</div>

<!-- MISSION -->
<div class="section">
  <div class="sec-label">// current_mission.json</div>
  <div class="mission-box">
    <div class="mission-item">
      <span class="mi-key">leveling_up</span>
      <span class="mi-val"><span class="highlight">Headless WooCommerce + React storefront</span></span>
    </div>
    <div class="mission-item">
      <span class="mi-key">2025_goal</span>
      <span class="mi-val">Launch <span class="highlight">3 WooCommerce SaaS products</span></span>
    </div>
    <div class="mission-item">
      <span class="mi-key">open_to</span>
      <span class="mi-val">Freelance · Consulting · Remote roles</span>
    </div>
    <div class="mission-item">
      <span class="mi-key">fun_fact</span>
      <span class="mi-val">Customized WooCommerce checkout more times than eaten lunch 😄</span>
    </div>
    <div class="mission-item">
      <span class="mi-key">philosophy</span>
      <span class="mi-val">"Write code that your future self won't curse"</span>
    </div>
  </div>
</div>

<!-- CONNECT -->
<div class="section" style="border-bottom: none;">
  <div class="sec-label">// ping_shubham</div>
  <div class="connect-row">
    <a href="https://github.com/Shubii8760" class="connect-btn btn-primary">⌥ GitHub</a>
    <a href="mailto:your@email.com" class="connect-btn btn-outline">✉ Email</a>
    <a href="https://linkedin.com/in/yourprofile" class="connect-btn btn-outline">in LinkedIn</a>
  </div>
</div>

<!-- QUOTE -->
<div class="quote-bar">
  <div class="quote-mark">"</div>
  <p class="quote-text">
    Any fool can write code that a computer can understand. Good programmers write code humans can understand.
    <br><strong>— Martin Fowler</strong>
  </p>
</div>

</body>
</html>
