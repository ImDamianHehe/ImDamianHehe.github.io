<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ImBatman Shop — Minecraft Products</title>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Rajdhani:wght@400;600;700&family=Share+Tech+Mono&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --black:    #0a0a0a;
      --dark:     #111114;
      --card:     #16161c;
      --border:   #2a2a35;
      --gold:     #f5c518;
      --gold-dim: #a8860f;
      --white:    #e8e8e8;
      --muted:    #888;
      --danger:   #c0392b;
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--black);
      color: var(--white);
      font-family: 'Rajdhani', sans-serif;
      font-size: 17px;
      line-height: 1.5;
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* ── BAT SIGNAL HERO ── */
    .hero {
      position: relative;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      overflow: hidden;
      padding: 2rem;
    }

    .bat-signal {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -60%);
      width: m(700px, 110vw);
      opacity: 0.06;
      pointer-events: none;
      animation: pulse 6s ease-in-out infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 0.06; transform: translate(-50%, -60%) scale(1); }
      50%       { opacity: 0.10; transform: translate(-50%, -60%) scale(1.04); }
    }

    .hero-eyebrow {
      font-family: 'Share Tech Mono', monospace;
      font-size: 0.75rem;
      letter-spacing: 0.25em;
      color: var(--gold);
      text-transform: uppercase;
      margin-bottom: 1.2rem;
    }

    .hero h1 {
      font-family: 'Bebas Neue', sans-serif;
      font-size: clamp(3.5rem, 12vw, 9rem);
      line-height: 0.9;
      letter-spacing: 0.04em;
      color: var(--white);
      position: relative;
    }

    .hero h1 span {
      color: var(--gold);
      display: block;
    }

    .hero-sub {
      margin-top: 1.4rem;
      font-size: 1.1rem;
      color: var(--muted);
      letter-spacing: 0.05em;
      max-width: 480px;
    }

    .hero-cta {
      margin-top: 2.5rem;
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
      justify-content: center;
    }

    .btn {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.1rem;
      letter-spacing: 0.12em;
      padding: 0.75rem 2.2rem;
      border: none;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
      transition: all 0.2s;
    }

    .btn-gold {
      background: var(--gold);
      color: var(--black);
      clip-path: polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%);
    }
    .btn-gold:hover { background: #ffd740; transform: translateY(-2px); }

    .btn-outline {
      background: transparent;
      color: var(--gold);
      border: 1.5px solid var(--gold);
      clip-path: polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%);
    }
    .btn-outline:hover { background: rgba(245,197,24,0.08); transform: translateY(-2px); }

    .scroll-hint {
      position: absolute;
      bottom: 2rem;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.4rem;
      color: var(--muted);
      font-size: 0.72rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      animation: bounce 2s ease-in-out infinite;
    }
    .scroll-hint svg { width: 18px; }
    @keyframes bounce {
      0%, 100% { transform: translateX(-50%) translateY(0); }
      50%       { transform: translateX(-50%) translateY(6px); }
    }

    /* ── DIVIDER ── */
    .divider {
      width: 100%;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--gold), transparent);
      opacity: 0.3;
    }

    /* ── SECTION ── */
    section {
      padding: 5rem 1.5rem;
      max-width: 1100px;
      margin: 0 auto;
    }

    .section-label {
      font-family: 'Share Tech Mono', monospace;
      font-size: 0.7rem;
      letter-spacing: 0.3em;
      color: var(--gold);
      text-transform: uppercase;
      margin-bottom: 0.6rem;
    }

    .section-title {
      font-family: 'Bebas Neue', sans-serif;
      font-size: clamp(2rem, 5vw, 3.5rem);
      letter-spacing: 0.05em;
      line-height: 1;
      margin-bottom: 1rem;
    }

    .section-sub {
      color: var(--muted);
      max-width: 520px;
      font-size: 1rem;
    }

    /* ── PACKAGES ── */
    .packages-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 1.25rem;
      margin-top: 3rem;
    }

    .pkg-card {
      background: var(--card);
      border: 1px solid var(--border);
      padding: 2rem 1.5rem;
      position: relative;
      transition: border-color 0.2s, transform 0.2s;
      clip-path: polygon(0 0, calc(100% - 16px) 0, 100% 16px, 100% 100%, 16px 100%, 0 calc(100% - 16px));
    }
    .pkg-card:hover {
      border-color: var(--gold-dim);
      transform: translateY(-4px);
    }

    .pkg-card.featured {
      border-color: var(--gold);
      background: #1a1a0f;
    }

    .featured-badge {
      position: absolute;
      top: -1px;
      right: 1.5rem;
      background: var(--gold);
      color: var(--black);
      font-family: 'Share Tech Mono', monospace;
      font-size: 0.65rem;
      letter-spacing: 0.15em;
      padding: 0.25rem 0.75rem;
      text-transform: uppercase;
    }

    .pkg-icon {
      font-size: 2.2rem;
      margin-bottom: 0.8rem;
    }

    .pkg-name {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.5rem;
      letter-spacing: 0.08em;
      color: var(--white);
    }

    .pkg-coins {
      font-family: 'Share Tech Mono', monospace;
      font-size: 0.85rem;
      color: var(--gold);
      margin: 0.3rem 0 1rem;
    }

    .pkg-price {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 2.8rem;
      color: var(--gold);
      line-height: 1;
    }
    .pkg-price sup { font-size: 1.2rem; vertical-align: top; margin-top: 0.4rem; display: inline-block; }
    .pkg-price sub { font-size: 1rem; color: var(--muted); }

    .pkg-perks {
      list-style: none;
      margin: 1.2rem 0 1.5rem;
      font-size: 0.9rem;
      color: var(--muted);
    }
    .pkg-perks li { padding: 0.25rem 0; }
    .pkg-perks li::before { content: "— "; color: var(--gold); }

    .pkg-buy {
      width: 100%;
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.05rem;
      letter-spacing: 0.12em;
      padding: 0.8rem;
      border: none;
      cursor: pointer;
      background: var(--gold);
      color: var(--black);
      transition: background 0.2s, transform 0.2s;
      clip-path: polygon(6px 0%, 100% 0%, calc(100% - 6px) 100%, 0% 100%);
    }
    .pkg-buy:hover { background: #ffd740; transform: scale(1.02); }

    .pkg-card.featured .pkg-buy {
      background: var(--gold);
    }

    /* ── HOW IT WORKS ── */
    .steps {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
      margin-top: 3rem;
    }

    .step {
      position: relative;
      padding-left: 1rem;
      border-left: 2px solid var(--border);
    }
    .step-num {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 3rem;
      color: var(--border);
      line-height: 1;
      margin-bottom: 0.3rem;
    }
    .step-title {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.2rem;
      letter-spacing: 0.06em;
      color: var(--white);
      margin-bottom: 0.4rem;
    }
    .step p { font-size: 0.9rem; color: var(--muted); }

    /* ── ORDER FORM ── */
    #order {
      background: var(--card);
      border: 1px solid var(--border);
      padding: 3rem 2rem;
      clip-path: polygon(0 0, calc(100% - 24px) 0, 100% 24px, 100% 100%, 24px 100%, 0 calc(100% - 24px));
      margin-top: 4rem;
    }

    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.25rem;
      margin-top: 2rem;
    }
    @media (max-width: 600px) { .form-grid { grid-template-columns: 1fr; } }

    .field { display: flex; flex-direction: column; gap: 0.4rem; }
    .field.full { grid-column: 1 / -1; }

    label {
      font-family: 'Share Tech Mono', monospace;
      font-size: 0.7rem;
      letter-spacing: 0.2em;
      color: var(--gold);
      text-transform: uppercase;
    }

    input, select, textarea {
      background: #0d0d10;
      border: 1px solid var(--border);
      color: var(--white);
      font-family: 'Rajdhani', sans-serif;
      font-size: 1rem;
      padding: 0.7rem 1rem;
      outline: none;
      transition: border-color 0.2s;
      width: 100%;
    }
    input:focus, select:focus, textarea:focus { border-color: var(--gold); }
    select option { background: var(--dark); }
    textarea { resize: vertical; min-height: 90px; }

    .payment-methods {
      grid-column: 1 / -1;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 1rem;
      margin-top: 0.5rem;
    }

    .pay-option {
      border: 1.5px solid var(--border);
      padding: 1rem;
      cursor: pointer;
      transition: border-color 0.2s, background 0.2s;
      display: flex;
      flex-direction: column;
      gap: 0.3rem;
    }
    .pay-option:hover { border-color: var(--gold-dim); background: rgba(245,197,24,0.04); }
    .pay-option input[type="radio"] { display: none; }
    .pay-option.selected { border-color: var(--gold); background: rgba(245,197,24,0.06); }

    .pay-name {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.1rem;
      letter-spacing: 0.08em;
    }
    .pay-detail {
      font-family: 'Share Tech Mono', monospace;
      font-size: 0.72rem;
      color: var(--gold);
    }
    .pay-placeholder {
      font-size: 0.75rem;
      color: var(--danger);
      font-style: italic;
    }

    .form-submit {
      grid-column: 1 / -1;
      margin-top: 1rem;
    }

    .btn-submit {
      width: 100%;
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.3rem;
      letter-spacing: 0.15em;
      padding: 1rem;
      border: none;
      cursor: pointer;
      background: var(--gold);
      color: var(--black);
      transition: background 0.2s, transform 0.2s;
      clip-path: polygon(10px 0%, 100% 0%, calc(100% - 10px) 100%, 0% 100%);
    }
    .btn-submit:hover { background: #ffd740; transform: scale(1.01); }

    /* ── PAYMENT INSTRUCTIONS (shown after submit) ── */
    #pay-instructions {
      display: none;
      margin-top: 2rem;
      border: 1px solid var(--gold);
      padding: 2rem;
      background: rgba(245,197,24,0.04);
    }
    #pay-instructions h3 {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.6rem;
      letter-spacing: 0.06em;
      color: var(--gold);
      margin-bottom: 1rem;
    }
    #pay-instructions p { font-size: 0.95rem; color: var(--muted); margin-bottom: 0.5rem; }
    #pay-instructions strong { color: var(--white); }

    .instruction-box {
      background: var(--dark);
      border: 1px solid var(--border);
      padding: 1.2rem 1.5rem;
      margin-top: 1rem;
      font-family: 'Share Tech Mono', monospace;
      font-size: 0.85rem;
      color: var(--gold);
      line-height: 1.8;
    }

    /* ── FOOTER ── */
    footer {
      border-top: 1px solid var(--border);
      padding: 2rem 1.5rem;
      text-align: center;
      color: var(--muted);
      font-size: 0.85rem;
      letter-spacing: 0.05em;
    }
    footer .bat { font-size: 1.4rem; display: block; margin-bottom: 0.5rem; }

    /* ── NAV ── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 1rem 2rem;
      background: rgba(10,10,10,0.85);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
    }

    .nav-logo {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.4rem;
      letter-spacing: 0.1em;
      color: var(--gold);
      text-decoration: none;
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
    }
    .nav-links a {
      font-family: 'Share Tech Mono', monospace;
      font-size: 0.72rem;
      letter-spacing: 0.2em;
      color: var(--muted);
      text-decoration: none;
      text-transform: uppercase;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--gold); }

    @media (max-width: 500px) { .nav-links { display: none; } }

    /* success toast */
    .toast {
      position: fixed;
      bottom: 2rem;
      right: 2rem;
      background: var(--gold);
      color: var(--black);
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1rem;
      letter-spacing: 0.1em;
      padding: 0.8rem 1.5rem;
      display: none;
      z-index: 999;
      clip-path: polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%);
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">🦇 ImBatman.shop</a>
  <ul class="nav-links">
    <li><a href="#packages">Packages</a></li>
    <li><a href="#how">How It Works</a></li>
    <li><a href="#order">Order</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="hero">
  <!-- Bat SVG Signal -->
  <svg class="bat-signal" viewBox="0 0 500 300" fill="var(--gold)" xmlns="http://www.w3.org/2000/svg">
    <ellipse cx="250" cy="220" rx="240" ry="70" fill="none" stroke="var(--gold)" stroke-width="3"/>
    <path d="M250 50 C180 50 130 100 100 130 C130 110 170 120 190 150 C200 130 220 110 250 110 C280 110 300 130 310 150 C330 120 370 110 400 130 C370 100 320 50 250 50Z"/>
    <path d="M100 130 C80 150 60 180 70 210 C90 180 120 170 150 180 C140 160 120 140 100 130Z"/>
    <path d="M400 130 C420 150 440 180 430 210 C410 180 380 170 350 180 C360 160 380 140 400 130Z"/>
  </svg>

  <p class="hero-eyebrow">🦇 Minecraft BATMAN Shop</p>
  <h1>IM<span>BATMAN</span></h1>
  <p class="hero-sub">Purchase Custom Prefix, Ranks, etc.</p>
  <div class="hero-cta">
    <a class="btn btn-gold" href="#packages">View Packages</a>
    <a class="btn btn-outline" href="#order">Place Order</a>
  </div>

  <div class="scroll-hint">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 5v14M5 12l7 7 7-7"/></svg>
    Scroll
  </div>
</div>

<div class="divider"></div>

<!-- PACKAGES -->
<section id="packages">
  <p class="section-label">Purchase your product</p>
  <h2 class="section-title">Products</h2>
  <p class="section-sub">Pick one, purchase it, and make a ticket on discord to get your product.</p>

  <div class="packages-grid">

    <div class="pkg-card">
      <div class="pkg-icon">⚔️</div>
      <div class="pkg-name">Custom Prefix</div>
      <div class="pkg-coins">30-Days</div>
      <div class="pkg-price"><sup>$</sup>3<sub>/month</sub></div>
      <ul class="pkg-perks">
        <li>Custom In-game Prefix Display</li>
        <li>Custom Color</li>
        <li>Custom Name</li>
      </ul>
      <button class="pkg-buy" onclick="selectPackage('Custom Prefix — 30-Days — $3')">Buy Now</button>
    </div>

    <div class="pkg-card">
      <div class="pkg-icon">🦇</div>
      <div class="pkg-name">Donator Rank</div>
      <div class="pkg-coins">30-Days</div>
      <div class="pkg-price"><sup>$</sup>4<sub>/month</sub></div>
      <ul class="pkg-perks">
        <li>Donator Rank Badge</li>
        <li>Donator Display</li>
        <li>Few In-game Commands</li>
      </ul>
      <button class="pkg-buy" onclick="selectPackage('Donator Rank — 30-Days — $4')">Buy Now</button>
    </div>

    <div class="pkg-card">
      <div class="pkg-icon">🌑</div>
      <div class="pkg-name">Custom Prefix+</div>
      <div class="pkg-coins">60-Days</div>
    <div class="pkg-price"><sup>$</sup>5<sub>/month</sub></div>
      <ul class="pkg-perks">
        <li>Custom In-game Prefix Display</li>
        <li>Custom Color</li>
        <li>Custom Name</li>
      </ul>
      <button class="pkg-buy" onclick="selectPackage('Custom Prefix+ — 60-Days — $5')">Buy Now</button>
    </div>

    <div class="pkg-card">
      <div class="pkg-icon">👑</div>
      <div class="pkg-name">Donator Rank+</div>
      <div class="pkg-coins">60-Days</div>
      <div class="pkg-price"><sup>$</sup>6<sub>/month</sub></div>
      <ul class="pkg-perks">
        <li>Donator Rank Badge</li>
        <li>Donator Display</li>
        <li>Few In-game Commands</li>
      </ul>
      <button class="pkg-buy" onclick="selectPackage('Donator Rank+ — 60-Days — $6')">Buy Now</button>
    </div>

   <div class="pkg-card featured">
      <div class="featured-badge">⭐ Most Popular</div>
      <div class="pkg-icon">🦇</div>
      <div class="pkg-name">Custom Prefix-</div>
      <div class="pkg-coins">15-Days</div>
      <div class="pkg-price"><sup>$</sup>2<sub>/month</sub></div>
      <ul class="pkg-perks">
        <li>Custom in-game Prefix Display</li>
        <li>Custom Color</li>
        <li>Custom Name</li>
      </ul>
      <button class="pkg-buy" onclick="selectPackage('Custom Prefix- — 15-Days — $2')">Buy Now</button>
    </div>

  </div>
</section>

<div class="divider"></div>

<!-- HOW IT WORKS -->
<section id="how">
  <p class="section-label">The Process</p>
  <h2 class="section-title">How It Works</h2>
  <p class="section-sub">Simple, fast, and secure. Four steps to get your product.</p>

  <div class="steps">
    <div class="step">
      <div class="step-num">01</div>
      <div class="step-title">Pick a Product</div>
      <p>Choose the product you want and click Buy Now.</p>
    </div>
    <div class="step">
      <div class="step-num">02</div>
      <div class="step-title">Fill the Form</div>
      <p>Enter your Minecraft username and preferred payment method.</p>
    </div>
    <div class="step">
      <div class="step-num">03</div>
      <div class="step-title">Send Payment</div>
      <p>Pay via PayPal, GCash, or Maya using the details shown.</p>
    </div>
    <div class="step">
      <div class="step-num">04</div>
      <div class="step-title">Get Your Product</div>
      <p>Send a screenshot and send it to a ticket on discord.</p>
    </div>
  </div>
</section>

<div class="divider"></div>

<!-- ORDER FORM -->
<section style="padding-top: 3rem; padding-bottom: 5rem; max-width: 1100px; margin: 0 auto; padding-left: 1.5rem; padding-right: 1.5rem;">
  <div id="order">
    <p class="section-label">Ready to Buy</p>
    <h2 class="section-title">Place Your Order</h2>

    <div class="form-grid">

      <div class="field">
        <label for="ign">Minecraft Username (IGN)</label>
        <input type="text" id="ign" placeholder="e.g. ImDaminaHehe" />
      </div>

      <div class="field">
        <label for="package">Package</label>
        <select id="package">
          <option value="">— Select a package —</option>
          <option value="Custom Prefix — 30-Days — $3">Custom Prefix — 30-Days — $3</option>
          <option value="Donator Rank — 30-Days — $4">Donator Rank — 30-Days — $4</option>
          <option value="Custom Prefix+ — 60-Days — $5">Custom Prefix+ — 60-Days — $5</option>
          <option value="Donator Rank+ — 60-Days — $6">Donator Rank+ — 60-Days — $6</option>
          <option value="Custom Prefix- — 15-Days — $2">Custom Prefix- — 15-Days — $2</option>
        </select>
      </div>

      <div class="field full">
        <label>Payment Method</label>
        <div class="payment-methods">

          <label class="pay-option" id="opt-paypal" onclick="selectPay('paypal')">
            <input type="radio" name="payment" value="paypal"/>
            <div class="pay-name">💳 PayPal</div>
            <div class="pay-detail" id="pp-detail">damina@email.com</div>
          </label>

          <label class="pay-option" id="opt-gcash" onclick="selectPay('gcash')">
            <input type="radio" name="payment" value="gcash"/>
            <div class="pay-name">📱 GCash</div>
            <div class="pay-detail" id="gc-detail">09XX-XXX-XXXX</div>
          </label>

          <label class="pay-option" id="opt-maya" onclick="selectPay('maya')">
            <input type="radio" name="payment" value="maya"/>
            <div class="pay-name">🟢 Maya</div>
            <div class="pay-detail" id="maya-detail">09XX-XXX-XXXX</div>
          </label>

        </div>
      </div>

      <div class="field full">
        <label for="notes">Notes (optional)</label>
        <textarea id="notes" placeholder="Any special instructions or questions..."></textarea>
      </div>

      <div class="form-submit">
        <button class="btn-submit" onclick="submitOrder()">🦇 Confirm Order</button>
      </div>

    </div>

    <!-- PAYMENT INSTRUCTIONS (shown after submit) -->
    <div id="pay-instructions">
      <h3>✅ Order Received — Send Payment Now</h3>
      <p>Your order has been logged. Please send your payment using the details below:</p>
      <div class="instruction-box" id="instruction-content"></div>
      <p style="margin-top:1rem;">After sending, <strong>screenshot your payment and make a ticket on discord.</strong> Send the information given above to verify your purchase.</p>
      <p style="margin-top:0.5rem; color: var(--gold);">🦇 Expected delivery: within the time shown on your package.</p>
    </div>

  </div>
</section>

<!-- FOOTER -->
<footer>
  <span class="bat">🦇</span>
  © 2026 ImBatman.shop — All rights reserved.<br/>
  Not affiliated with Mojang or Microsoft.
</footer>

<div class="toast" id="toast">Order placed!</div>

<script>
  let selectedPayment = '';

  function selectPay(method) {
    selectedPayment = method;
    document.querySelectorAll('.pay-option').forEach(el => el.classList.remove('selected'));
    document.getElementById('opt-' + method).classList.add('selected');
  }

  function selectPackage(pkg) {
    document.getElementById('package').value = pkg;
    document.getElementById('order').scrollIntoView({ behavior: 'smooth' });
  }

  function submitOrder() {
    const ign = document.getElementById('ign').value.trim();
    const pkg = document.getElementById('package').value;

    if (!ign) { alert('Please enter your Minecraft username.'); return; }
    if (!pkg) { alert('Please select a package.'); return; }
    if (!selectedPayment) { alert('Please select a payment method.'); return; }

    const instructions = {
      paypal: `Send payment to: YOUR_PAYPAL@EMAIL.COM\nAmount: ${getAmount(pkg)}\nNote in PayPal: "${ign} — ${pkg.split('—')[0].trim()}"`,
      gcash:  `GCash Number: 09XX-XXX-XXXX\nAmount: ${getAmount(pkg)}\nName: [Your Name]\nMessage: "${ign} — ${pkg.split('—')[0].trim()}"`,
      maya:   `Maya Number: 09XX-XXX-XXXX\nAmount: ${getAmount(pkg)}\nName: [Your Name]\nMessage: "${ign} — ${pkg.split('—')[0].trim()}"`
    };

    document.getElementById('instruction-content').innerText = instructions[selectedPayment];
    document.getElementById('pay-instructions').style.display = 'block';
    document.getElementById('pay-instructions').scrollIntoView({ behavior: 'smooth' });

    const toast = document.getElementById('toast');
    toast.style.display = 'block';
    setTimeout(() => toast.style.display = 'none', 3000);
  }

  function getAmount(pkg) {
    if (pkg.includes('&3')) return '&3';
    if (pkg.includes('&4')) return '&4';
    if (pkg.includes('&5')) return '&5';
    if (pkg.includes('&6')) return '&6';
    return '';
  }
</script>

</body>
</html>
