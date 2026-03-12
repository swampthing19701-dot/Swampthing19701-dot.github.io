<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Death Squad Apparel</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg: #000000;
      --bg-alt: #111111;
      --charcoal: #1a1a1a;
      --blood: #8a0000;
      --bone: #e6e6e6;
      --muted: #aaaaaa;
      --accent: #ff1a1a;
      --max-width: 1200px;
      --radius: 6px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #220000 0, #000000 55%);
      color: var(--bone);
      line-height: 1.5;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    .page {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    .container {
      width: 100%;
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    /* HEADER / NAV */

    header {
      position: sticky;
      top: 0;
      z-index: 20;
      background: linear-gradient(to bottom, rgba(0,0,0,0.95), rgba(0,0,0,0.7), transparent);
      backdrop-filter: blur(8px);
      border-bottom: 1px solid rgba(255,255,255,0.05);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.75rem 0;
    }

    .nav-left {
      display: flex;
      align-items: center;
      gap: 1rem;
    }

    .logo-text {
      font-size: 1.1rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--bone);
      display: flex;
      flex-direction: column;
      line-height: 1.1;
    }

    .logo-main {
      font-weight: 800;
      color: var(--accent);
      text-shadow: 0 0 8px rgba(255, 0, 0, 0.8), 0 0 18px rgba(255, 0, 0, 0.6);
    }

    .logo-sub {
      font-size: 0.7rem;
      color: var(--bone);
      opacity: 0.8;
    }

    .nav-links {
      display: flex;
      gap: 1.5rem;
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
    }

    .nav-links a {
      position: relative;
      color: var(--bone);
      opacity: 0.8;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -0.25rem;
      width: 0;
      height: 2px;
      background: var(--accent);
      transition: width 0.2s ease;
    }

    .nav-links a:hover {
      opacity: 1;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-right {
      display: flex;
      align-items: center;
      gap: 1rem;
      font-size: 0.9rem;
    }

    .cart-icon {
      width: 26px;
      height: 26px;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.8rem;
      cursor: pointer;
    }

    /* HERO */

    .hero {
      padding: 3.5rem 0 3rem;
    }

    .hero-inner {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 3rem;
      align-items: center;
    }

    .hero-logo {
      margin-bottom: 1.5rem;
    }

    .hero-logo-text {
      font-size: 2.4rem;
      font-weight: 900;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--accent);
      text-shadow: 0 0 12px rgba(255, 0, 0, 0.9), 0 0 28px rgba(255, 0, 0, 0.7);
      line-height: 1.1;
    }

    .hero-logo-sub {
      font-size: 0.9rem;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      color: var(--bone);
      opacity: 0.9;
      margin-top: 0.25rem;
    }

    .hero-title {
      font-size: 2.6rem;
      font-weight: 800;
      margin-bottom: 0.75rem;
    }

    .hero-sub {
      font-size: 1rem;
      color: var(--muted);
      max-width: 26rem;
      margin-bottom: 1.75rem;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-bottom: 2rem;
    }

    .btn {
      padding: 0.8rem 1.6rem;
      border-radius: 999px;
      border: 1px solid transparent;
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      cursor: pointer;
      transition: background 0.2s ease, color 0.2s ease, transform 0.1s ease, box-shadow 0.1s ease;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--blood), var(--accent));
      color: #ffffff;
      box-shadow: 0 0 18px rgba(255, 0, 0, 0.5);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 0 24px rgba(255, 0, 0, 0.7);
    }

    .btn-ghost {
      background: transparent;
      color: var(--bone);
      border-color: rgba(255,255,255,0.3);
    }

    .btn-ghost:hover {
      background: rgba(255,255,255,0.06);
    }

    .hero-note {
      font-size: 0.8rem;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: 0.16em;
    }

    .hero-art {
      background: radial-gradient(circle at top, rgba(255,0,0,0.18), transparent 55%);
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.08);
      padding: 1.5rem;
      position: relative;
      overflow: hidden;
    }

    .hero-art-inner {
      background: radial-gradient(circle at top, #111111, #000000 70%);
      border-radius: 999px;
      padding: 2rem 1.5rem;
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 1.5rem;
    }

    .hero-shirt {
      background: linear-gradient(145deg, #151515, #050505);
      border-radius: 1rem;
      padding: 1rem;
      border: 1px solid rgba(255,255,255,0.06);
      box-shadow: 0 0 18px rgba(0,0,0,0.9);
      position: relative;
      overflow: hidden;
    }

    .hero-shirt::after {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at top, rgba(255,0,0,0.18), transparent 60%);
      opacity: 0.7;
      mix-blend-mode: screen;
      pointer-events: none;
    }

    .hero-shirt-label {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--muted);
      margin-bottom: 0.5rem;
    }

    .hero-shirt-name {
      font-size: 0.9rem;
      font-weight: 600;
      margin-bottom: 0.75rem;
    }

    .hero-shirt-tag {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--accent);
    }

    /* SECTION WRAPPER */

    section {
      padding: 2.5rem 0;
    }

    .section-header {
      margin-bottom: 1.5rem;
    }

    .section-kicker {
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--accent);
      margin-bottom: 0.25rem;
    }

    .section-title {
      font-size: 1.4rem;
      font-weight: 700;
      margin-bottom: 0.25rem;
    }

    .section-sub {
      font-size: 0.95rem;
      color: var(--muted);
    }

    /* EVIL WAYS GRID */

    .grid-4 {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 1.5rem;
    }

    .product-card {
      background: linear-gradient(145deg, #151515, #050505);
      border-radius: 1rem;
      padding: 1rem;
      border: 1px solid rgba(255,255,255,0.06);
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
      position: relative;
      overflow: hidden;
    }

    .product-tag {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--muted);
    }

    .product-name {
      font-size: 0.95rem;
      font-weight: 600;
    }

    .product-meta {
      font-size: 0.8rem;
      color: var(--muted);
    }

    /* BRAND STATEMENT */

    .brand-block {
      background: radial-gradient(circle at top, #111111, #000000 70%);
      border-radius: 1.25rem;
      border: 1px solid rgba(255,255,255,0.08);
      padding: 2rem 1.75rem;
      text-align: center;
      margin-top: 1rem;
    }

    .brand-block p {
      font-size: 0.95rem;
      max-width: 32rem;
      margin: 0 auto;
      color: var(--bone);
    }

    /* BEST SELLERS */

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.5rem;
    }

    .product-footer {
      margin-top: 0.75rem;
    }

    .btn-view {
      display: inline-block;
      padding: 0.55rem 1.2rem;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.18);
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--bone);
      background: transparent;
      cursor: pointer;
      transition: background 0.2s ease, border-color 0.2s ease;
    }

    .btn-view:hover {
      background: rgba(255,255,255,0.06);
      border-color: var(--accent);
    }

    /* EMAIL SIGNUP */

    .cta {
      margin-top: 1.5rem;
      background: radial-gradient(circle at top, #151515, #000000 70%);
      border-radius: 1.25rem;
      border: 1px solid rgba(255,255,255,0.08);
      padding: 2rem 1.75rem;
      position: relative;
      overflow: hidden;
    }

    .cta::before {
      content: "";
      position: absolute;
      inset: -40%;
      background: radial-gradient(circle at center, rgba(255,0,0,0.12), transparent 60%);
      opacity: 0.7;
      mix-blend-mode: screen;
      pointer-events: none;
    }

    .cta-inner {
      position: relative;
      z-index: 1;
    }

    .cta-title {
      font-size: 1.2rem;
      font-weight: 700;
      margin-bottom: 0.25rem;
    }

    .cta-sub {
      font-size: 0.9rem;
      color: var(--muted);
      margin-bottom: 1.25rem;
    }

    .cta-form {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }

    .cta-input {
      flex: 1 1 220px;
      min-width: 0;
      padding: 0.75rem 0.9rem;
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.2);
      background: rgba(0,0,0,0.7);
      color: var(--bone);
      font-size: 0.9rem;
    }

    .cta-input::placeholder {
      color: rgba(255,255,255,0.4);
    }

    .cta-button {
      padding: 0.75rem 1.6rem;
      border-radius: 999px;
      border: none;
      background: linear-gradient(135deg, var(--blood), var(--accent));
      color: #ffffff;
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      cursor: pointer;
      box-shadow: 0 0 16px rgba(255,0,0,0.5);
    }

    .cta-button:hover {
      box-shadow: 0 0 22px rgba(255,0,0,0.7);
    }

    /* FOOTER */

    footer {
      padding: 1.75rem 0 2.5rem;
      font-size: 0.8rem;
      color: var(--muted);
      text-align: center;
    }

    /* RESPONSIVE */

    @media (max-width: 960px) {
      .hero-inner {
        grid-template-columns: minmax(0, 1fr);
      }
      .hero-art {
        order: -1;
      }
      .grid-4 {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
      .grid-3 {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
      .nav-links {
        display: none;
      }
    }

    @media (max-width: 640px) {
      .hero-title {
        font-size: 2.1rem;
      }
      .hero-logo-text {
        font-size: 1.8rem;
      }
      .grid-4,
      .grid-3 {
        grid-template-columns: minmax(0, 1fr);
      }
    }
  </style>
</head>
<body>
  <div class="page">
    <!-- HEADER -->
    <header>
      <div class="container nav">
        <div class="nav-left">
          <div class="logo-text">
            <span class="logo-main">DEATH&nbsp;SQUAD</span>
            <span class="logo-sub">APPAREL</span>
          </div>
        </div>
        <nav class="nav-links">
          <a href="#new-drops">New Drops</a>
          <a href="#evil-ways">Evil Ways</a>
          <a href="#best-sellers">Best Sellers</a>
          <a href="#limited-bloodline">Limited Bloodline</a>
        </nav>
        <div class="nav-right">
          <div class="cart-icon">🛒</div>
        </div>
      </div>
    </header>

    <!-- HERO -->
    <main>
      <section class="hero">
        <div class="container hero-inner">
          <div>
            <div class="hero-logo">
              <div class="hero-logo-text">DEATH&nbsp;SQUAD</div>
              <div class="hero-logo-sub">APPAREL</div>
            </div>
            <h1 class="hero-title">Wear Your Darkness.</h1>
            <p class="hero-sub">
              Premium streetwear forged in shadow. Limited drops only. Built for the ones who walk the edge.
            </p>
            <div class="hero-buttons">
              <button class="btn btn-primary">Shop New Drops</button>
              <button class="btn btn-ghost">Evil Ways Collection</button>
            </div>
            <div class="hero-note">
             
            </div>
          </div>

          <div class="hero-art">
            <div class="hero-art-inner">
              <div class="hero-shirt">
                
                <a href="Copilot_20260311_191056.png"><img src="Copilot_20260311_191056.png"></a>
                
              </div>
              <div class="hero-shirt">
                <a href="Copilot_20260311_195924.png"><img src="Copilot_20260311_195924.png"></a>
              </div>
              <div class="hero-shirt">
                <a href="Copilot_20260311_200544.png"><img src="Copilot_20260311_200544.png"></a>
              </div>
              <div class="hero-shirt">
                <a href="Copilot_20260311_201213.png"><img src="Copilot_20260311_201213.png"></a>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- EVIL WAYS SECTION -->
      <section id="evil-ways">
        <div class="container">
          <div class="section-header">
            
            <h2 class="section-title">Evil Ways: The Signature Line</h2>
            <p class="section-sub">
              Icons of the macabre. Built for the wicked. Each piece feels like a symbol, not just a shirt.
            </p>
          </div>

          <div class="grid-4">
            <article class="product-card">
              <div class="product-name">Crimson Harvester</div>
              <a href="Copilot_20260311_165835.png"><img src="Copilot_20260311_165835.png"></a>
            </article>
            <article class="product-card">
              <div class="product-name">Infernal Relic</div>
              <a href="Copilot_20260311_171244.png"><img src="Copilot_20260311_171244.png"></a>
            </article>
            <article class="product-card">
              <div class="product-name">Silent Witness</div>
              <a href="Copilot_20260311_173212.png"><img src="Copilot_20260311_173212.png"></a>
            </article>
            <article class="product-card">
              <div class="product-name">Venom Oath</div>
              <a href="Copilot_20260311_173806.png"><img src="Copilot_20260311_173806.png"></a>
            </article>
          </div>
      

     
        <div class="container">
          <div class="section-header">
            
            <h2 class="section-title">Marked by the Squad</h2>
            <p class="section-sub">
              The pieces that never stay in stock for long. Once they’re gone, they’re gone.
            </p>
          </div>

          <div class="grid-3">
            <article class="product-card">
              <div class="product-name">Limited Run!</div>
              <a href="Copilot_20260311_192711.png"><img src="Copilot_20260311_192711.png"></a>
              <div class="product-footer">
              </div>
            </article>
            <article class="product-card">
              
              <div class="product-name">Limited Run!</div>
              <a href="Copilot_20260311_194426.png"><img src="Copilot_20260311_194426.png"></a>
              <div class="product-footer">
                
              </div>
            </article>
            <article class="product-card">
              
              <div class="product-name">Limited Run!</div>
              <a href="Copilot_20260311_195122.png"><img src="Copilot_20260311_195122.png"></a>
              <div class="product-footer">
                
              </div>
            </article>
          </div>
        </div>
      

      <!-- LIMITED BLOODLINE + EMAIL -->
      <section id="limited-bloodline">
        <div class="container">
          <div class="section-header">
           
            <h2 class="section-title">Numbered Releases Only</h2>
            <p class="section-sub">
              Short-run drops for collectors of the dark. Each piece is tagged, tracked, and never reprinted.
            </p>
          </div>

          <div class="cta">
            <div class="cta-inner">
              <h3 class="cta-title">Join the Death Squad</h3>
              <p class="cta-sub">
                Get early access to drops & exclusive releases. No spam. Just darkness.
              </p>
              <form class="cta-form">
                <input
                  type="email"
                  class="cta-input"
                  placeholder="Enter your email"
                  required
                />
                <button type="submit" class="cta-button">Join Now</button>
              </form>
            </div>
          </div>
        </div>
      </section>
    

    <!-- FOOTER -->
    <footer>
      <div class="container">
        © <span id="year"></span> Death Squad Apparel. All rights reserved.
      </div>
    </footer>
  </div>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
<article class="product-card">
<img src="Copilot_20260311_202618.png">
</article>
