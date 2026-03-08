# Shopinsted-
This Is Grocery Site.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Shopinsted — Fresh groceries delivered to your door</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  /* ─── RESET & BASE ─── */
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --green:   #1a6641;
    --green-l: #2a8a57;
    --green-xl:#e8f5ee;
    --amber:   #f59e0b;
    --amber-l: #fef3c7;
    --red:     #dc2626;
    --ink:     #111827;
    --muted:   #6b7280;
    --border:  #e5e7eb;
    --bg:      #f9fafb;
    --white:   #ffffff;
    --card-shadow: 0 2px 12px rgba(0,0,0,.08);
    --card-shadow-hover: 0 8px 30px rgba(0,0,0,.14);
    --radius:  16px;
    --font-head: 'Playfair Display', Georgia, serif;
    --font-body: 'DM Sans', sans-serif;
  }
  html { scroll-behavior: smooth; }
  body {
    font-family: var(--font-body);
    background: var(--bg);
    color: var(--ink);
    min-height: 100vh;
    overscroll-behavior: none;
  }

  /* ─── HEADER ─── */
  header {
    background: var(--green);
    color: var(--white);
    padding: 0 20px;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 16px rgba(0,0,0,.2);
  }
  .header-inner {
    max-width: 1100px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 64px;
    gap: 12px;
  }
  .brand { display: flex; align-items: center; gap: 10px; text-decoration: none; }
  .brand-logo {
    width: 40px; height: 40px;
    background: var(--amber);
    border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    font-size: 20px; flex-shrink: 0;
  }
  .brand-text {}
  .brand-name {
    font-family: var(--font-head);
    font-size: 1.35rem;
    color: var(--white);
    line-height: 1.1;
    letter-spacing: -.3px;
  }
  .brand-tag {
    font-size: .7rem;
    color: rgba(255,255,255,.7);
    font-weight: 400;
    display: block;
  }
  .header-actions { display: flex; align-items: center; gap: 10px; }
  .cart-btn {
    background: rgba(255,255,255,.15);
    border: 1.5px solid rgba(255,255,255,.3);
    color: var(--white);
    border-radius: 12px;
    padding: 8px 16px;
    font-family: var(--font-body);
    font-size: .85rem;
    font-weight: 600;
    cursor: pointer;
    display: flex; align-items: center; gap: 6px;
    transition: background .2s;
  }
  .cart-btn:hover { background: rgba(255,255,255,.25); }
  .cart-badge {
    background: var(--amber);
    color: var(--ink);
    border-radius: 999px;
    min-width: 20px;
    height: 20px;
    font-size: .72rem;
    font-weight: 700;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0 5px;
    transition: transform .2s;
  }
  .cart-badge.bump { animation: bump .25s ease; }
  @keyframes bump { 0%,100%{transform:scale(1)} 50%{transform:scale(1.5)} }

  /* ─── HERO STRIP ─── */
  .hero {
    background: linear-gradient(135deg, var(--green-xl) 0%, #d1fae5 100%);
    padding: 28px 20px 24px;
    border-bottom: 1px solid #c6e8d4;
  }
  .hero-inner {
    max-width: 1100px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
  }
  .hero-text h1 {
    font-family: var(--font-head);
    font-size: clamp(1.5rem, 4vw, 2.4rem);
    color: var(--green);
    line-height: 1.2;
  }
  .hero-text p { color: var(--muted); font-size: .92rem; margin-top: 4px; }
  .hero-meta {
    display: flex;
    gap: 14px;
    flex-wrap: wrap;
    margin-top: 14px;
  }
  .hero-pill {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    background: var(--white);
    border: 1px solid #c6e8d4;
    border-radius: 999px;
    padding: 5px 12px;
    font-size: .78rem;
    font-weight: 500;
    color: var(--green);
  }

  /* ─── SEARCH ─── */
  .search-wrap {
    max-width: 1100px;
    margin: 22px auto 0;
    padding: 0 20px;
  }
  .search-box {
    display: flex;
    align-items: center;
    background: var(--white);
    border: 1.5px solid var(--border);
    border-radius: 12px;
    padding: 0 14px;
    gap: 8px;
    box-shadow: var(--card-shadow);
    transition: border-color .2s;
  }
  .search-box:focus-within { border-color: var(--green-l); }
  .search-box span { color: var(--muted); font-size: 1.1rem; flex-shrink: 0; }
  .search-box input {
    flex: 1;
    border: none;
    outline: none;
    font-family: var(--font-body);
    font-size: .9rem;
    padding: 12px 0;
    background: transparent;
    color: var(--ink);
  }
  .search-box input::placeholder { color: #9ca3af; }

  /* ─── CATEGORIES ─── */
  .cats-wrap {
    max-width: 1100px;
    margin: 18px auto 0;
    padding: 0 20px;
    display: flex;
    gap: 8px;
    overflow-x: auto;
    scrollbar-width: none;
    -webkit-overflow-scrolling: touch;
  }
  .cats-wrap::-webkit-scrollbar { display: none; }
  .cat-btn {
    flex-shrink: 0;
    background: var(--white);
    border: 1.5px solid var(--border);
    border-radius: 999px;
    padding: 7px 16px;
    font-family: var(--font-body);
    font-size: .82rem;
    font-weight: 500;
    color: var(--muted);
    cursor: pointer;
    transition: all .18s;
    white-space: nowrap;
  }
  .cat-btn:hover, .cat-btn.active {
    background: var(--green);
    border-color: var(--green);
    color: var(--white);
  }

  /* ─── PRODUCTS GRID ─── */
  .products-section {
    max-width: 1100px;
    margin: 24px auto 120px;
    padding: 0 16px;
  }
  .section-title {
    font-family: var(--font-head);
    font-size: 1.3rem;
    color: var(--ink);
    margin-bottom: 16px;
    padding: 0 4px;
  }
  .products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(155px, 1fr));
    gap: 14px;
  }
  @media(min-width:640px) {
    .products-grid { grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 18px; }
  }
  .product-card {
    background: var(--white);
    border-radius: var(--radius);
    box-shadow: var(--card-shadow);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    transition: transform .22s, box-shadow .22s;
    cursor: default;
    border: 1px solid transparent;
  }
  .product-card:hover {
    transform: translateY(-4px);
    box-shadow: var(--card-shadow-hover);
    border-color: var(--green-xl);
  }
  .product-img-wrap {
    position: relative;
    aspect-ratio: 1 / 1;
    overflow: hidden;
    background: var(--green-xl);
  }
  .product-img-wrap img {
    width: 100%; height: 100%;
    object-fit: cover;
    transition: transform .35s;
  }
  .product-card:hover .product-img-wrap img { transform: scale(1.06); }
  .cat-tag {
    position: absolute;
    top: 8px; left: 8px;
    background: rgba(255,255,255,.88);
    backdrop-filter: blur(4px);
    border-radius: 6px;
    padding: 2px 7px;
    font-size: .65rem;
    font-weight: 600;
    color: var(--green);
    text-transform: uppercase;
    letter-spacing: .5px;
  }
  .product-body { padding: 12px; flex: 1; display: flex; flex-direction: column; gap: 4px; }
  .product-name {
    font-size: .88rem;
    font-weight: 600;
    color: var(--ink);
    line-height: 1.3;
  }
  .product-desc {
    font-size: .73rem;
    color: var(--muted);
    line-height: 1.4;
    flex: 1;
  }
  .product-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 10px;
    gap: 6px;
  }
  .product-price {
    font-family: var(--font-head);
    font-size: 1.05rem;
    color: var(--green);
    font-weight: 700;
  }
  .add-btn {
    background: var(--green);
    color: var(--white);
    border: none;
    border-radius: 8px;
    padding: 7px 12px;
    font-family: var(--font-body);
    font-size: .78rem;
    font-weight: 600;
    cursor: pointer;
    transition: background .18s, transform .14s;
    white-space: nowrap;
    display: flex; align-items: center; gap: 4px;
  }
  .add-btn:hover { background: var(--green-l); }
  .add-btn:active { transform: scale(.94); }
  .add-btn.added { background: var(--amber); color: var(--ink); }

  /* ─── EMPTY STATE ─── */
  .empty-state {
    text-align: center;
    padding: 60px 20px;
    color: var(--muted);
    grid-column: 1/-1;
  }
  .empty-state .emoji { font-size: 3rem; display: block; margin-bottom: 10px; }
  .empty-state p { font-size: .9rem; }

  /* ─── FLOATING BUTTONS ─── */
  .fab-group {
    position: fixed;
    bottom: 24px;
    right: 18px;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    gap: 12px;
    z-index: 90;
  }
  .fab {
    width: 52px; height: 52px;
    border-radius: 50%;
    border: none;
    cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.4rem;
    box-shadow: 0 4px 16px rgba(0,0,0,.2);
    transition: transform .2s, box-shadow .2s;
  }
  .fab:hover { transform: scale(1.1); box-shadow: 0 6px 24px rgba(0,0,0,.28); }
  .fab-wa { background: #25d366; color: var(--white); }
  .fab-cart {
    background: var(--green);
    color: var(--white);
    position: relative;
    width: 56px; height: 56px;
    font-size: 1.6rem;
  }
  .fab-cart-badge {
    position: absolute;
    top: -4px; right: -4px;
    background: var(--amber);
    color: var(--ink);
    border-radius: 999px;
    min-width: 20px;
    height: 20px;
    font-size: .7rem;
    font-weight: 700;
    display: flex; align-items: center; justify-content: center;
    padding: 0 4px;
    border: 2px solid var(--white);
  }

  /* ─── MODAL OVERLAY ─── */
  .overlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,.45);
    z-index: 200;
    backdrop-filter: blur(2px);
    align-items: flex-end;
    justify-content: center;
  }
  .overlay.open { display: flex; }
  @media(min-width: 640px) {
    .overlay { align-items: center; }
  }

  /* ─── CART MODAL ─── */
  .cart-modal {
    background: var(--white);
    border-radius: 20px 20px 0 0;
    width: 100%;
    max-width: 520px;
    max-height: 90vh;
    display: flex;
    flex-direction: column;
    animation: slideUp .3s ease;
    overflow: hidden;
  }
  @media(min-width:640px) {
    .cart-modal { border-radius: 20px; max-height: 85vh; }
  }
  @keyframes slideUp { from{transform:translateY(40px);opacity:0} to{transform:none;opacity:1} }
  .modal-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 18px 20px;
    border-bottom: 1px solid var(--border);
    flex-shrink: 0;
  }
  .modal-title {
    font-family: var(--font-head);
    font-size: 1.2rem;
    color: var(--ink);
  }
  .close-btn {
    background: var(--bg);
    border: none;
    width: 32px; height: 32px;
    border-radius: 50%;
    font-size: 1.1rem;
    cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    color: var(--muted);
    transition: background .18s;
  }
  .close-btn:hover { background: var(--border); }

  /* Cart Items */
  .cart-items { overflow-y: auto; flex: 1; padding: 12px 16px; }
  .cart-item {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 12px 0;
    border-bottom: 1px solid var(--border);
  }
  .cart-item:last-child { border-bottom: none; }
  .cart-item-img {
    width: 54px; height: 54px;
    border-radius: 10px;
    object-fit: cover;
    flex-shrink: 0;
    background: var(--green-xl);
  }
  .cart-item-info { flex: 1; min-width: 0; }
  .cart-item-name { font-size: .85rem; font-weight: 600; color: var(--ink); white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
  .cart-item-price { font-size: .78rem; color: var(--muted); margin-top: 2px; }
  .cart-item-subtotal { font-size: .82rem; font-weight: 600; color: var(--green); margin-top: 2px; }
  .qty-ctrl {
    display: flex; align-items: center; gap: 6px; flex-shrink: 0;
  }
  .qty-btn {
    width: 28px; height: 28px;
    border-radius: 8px;
    border: 1.5px solid var(--border);
    background: var(--white);
    font-size: 1rem;
    font-weight: 700;
    cursor: pointer;
    display: flex; align-items: center; justify-content: center;
    color: var(--green);
    transition: background .15s;
  }
  .qty-btn:hover { background: var(--green-xl); }
  .qty-val { font-size: .88rem; font-weight: 600; min-width: 20px; text-align: center; }
  .remove-btn {
    background: none; border: none; cursor: pointer;
    color: var(--red); font-size: 1rem; padding: 4px;
    flex-shrink: 0; opacity: .7;
  }
  .remove-btn:hover { opacity: 1; }

  /* Cart Empty */
  .cart-empty {
    text-align: center;
    padding: 50px 20px;
    color: var(--muted);
  }
  .cart-empty .emoji { font-size: 3rem; display: block; margin-bottom: 10px; }

  /* Cart Footer */
  .cart-footer {
    padding: 16px 20px;
    border-top: 1px solid var(--border);
    flex-shrink: 0;
  }
  .cart-total-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 14px;
  }
  .cart-total-label { font-size: .9rem; font-weight: 500; color: var(--muted); }
  .cart-total-val {
    font-family: var(--font-head);
    font-size: 1.3rem;
    color: var(--green);
  }
  .checkout-btn {
    width: 100%;
    background: var(--green);
    color: var(--white);
    border: none;
    border-radius: 12px;
    padding: 15px;
    font-family: var(--font-body);
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    transition: background .18s, transform .14s;
    letter-spacing: .3px;
  }
  .checkout-btn:hover { background: var(--green-l); }
  .checkout-btn:active { transform: scale(.98); }

  /* ─── CHECKOUT MODAL ─── */
  .checkout-modal {
    background: var(--white);
    border-radius: 20px 20px 0 0;
    width: 100%;
    max-width: 520px;
    max-height: 95vh;
    display: flex;
    flex-direction: column;
    animation: slideUp .3s ease;
    overflow: hidden;
  }
  @media(min-width:640px) { .checkout-modal { border-radius: 20px; max-height: 90vh; } }
  .checkout-body { overflow-y: auto; flex: 1; padding: 16px 20px 20px; }
  .form-group { margin-bottom: 14px; }
  .form-label {
    display: block;
    font-size: .8rem;
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 5px;
    text-transform: uppercase;
    letter-spacing: .5px;
  }
  .form-label span { color: var(--red); }
  .form-input, .form-textarea {
    width: 100%;
    border: 1.5px solid var(--border);
    border-radius: 10px;
    padding: 11px 13px;
    font-family: var(--font-body);
    font-size: .9rem;
    color: var(--ink);
    background: var(--white);
    outline: none;
    transition: border-color .2s;
    resize: none;
  }
  .form-input:focus, .form-textarea:focus { border-color: var(--green-l); }
  .order-summary-box {
    background: var(--green-xl);
    border-radius: 12px;
    padding: 14px;
    margin-bottom: 16px;
  }
  .order-summary-title {
    font-size: .78rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: .5px;
    color: var(--green);
    margin-bottom: 8px;
  }
  .order-summary-item {
    display: flex;
    justify-content: space-between;
    font-size: .82rem;
    color: var(--ink);
    padding: 3px 0;
  }
  .order-summary-total {
    border-top: 1px solid #b7ddc6;
    margin-top: 8px;
    padding-top: 8px;
    display: flex;
    justify-content: space-between;
    font-weight: 700;
    color: var(--green);
    font-size: .92rem;
  }
  .place-order-btn {
    width: 100%;
    background: var(--green);
    color: var(--white);
    border: none;
    border-radius: 12px;
    padding: 16px;
    font-family: var(--font-body);
    font-size: 1rem;
    font-weight: 700;
    cursor: pointer;
    transition: background .18s;
    letter-spacing: .3px;
    margin-top: 4px;
  }
  .place-order-btn:hover { background: var(--green-l); }
  .place-order-btn:disabled { background: #9ca3af; cursor: not-allowed; }

  /* ─── SUCCESS MODAL ─── */
  .success-modal {
    background: var(--white);
    border-radius: 20px 20px 0 0;
    width: 100%;
    max-width: 420px;
    padding: 40px 28px;
    text-align: center;
    animation: slideUp .3s ease;
  }
  @media(min-width:640px) { .success-modal { border-radius: 20px; } }
  .success-icon { font-size: 3.5rem; display: block; margin-bottom: 14px; }
  .success-title {
    font-family: var(--font-head);
    font-size: 1.5rem;
    color: var(--green);
    margin-bottom: 10px;
  }
  .success-msg { font-size: .9rem; color: var(--muted); line-height: 1.6; }
  .wa-order-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: #25d366;
    color: var(--white);
    text-decoration: none;
    border-radius: 12px;
    padding: 13px 24px;
    font-weight: 600;
    font-size: .92rem;
    margin-top: 20px;
    font-family: var(--font-body);
    transition: background .18s;
  }
  .wa-order-btn:hover { background: #1ebe5c; }
  .continue-btn {
    display: block;
    margin: 12px auto 0;
    background: none;
    border: 1.5px solid var(--border);
    border-radius: 12px;
    padding: 11px 24px;
    font-family: var(--font-body);
    font-size: .88rem;
    cursor: pointer;
    color: var(--muted);
    transition: border-color .18s;
  }
  .continue-btn:hover { border-color: var(--green); color: var(--green); }

  /* ─── TOAST ─── */
  .toast {
    position: fixed;
    bottom: 90px;
    left: 50%;
    transform: translateX(-50%) translateY(20px);
    background: var(--ink);
    color: var(--white);
    border-radius: 999px;
    padding: 10px 22px;
    font-size: .83rem;
    font-weight: 500;
    z-index: 500;
    opacity: 0;
    pointer-events: none;
    transition: opacity .25s, transform .25s;
    white-space: nowrap;
  }
  .toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

  /* ─── FOOTER ─── */
  footer {
    background: var(--ink);
    color: rgba(255,255,255,.6);
    text-align: center;
    padding: 20px;
    font-size: .78rem;
    position: fixed;
    bottom: 0; left: 0; right: 0;
    z-index: 1;
    display: none;
  }

  /* ─── UTILS ─── */
  .hidden { display: none !important; }
</style>
</head>
<body>

<!-- ════════════════════ HEADER ════════════════════ -->
<header>
  <div class="header-inner">
    <a class="brand" href="#">
      <div class="brand-logo">🛒</div>
      <div class="brand-text">
        <span class="brand-name">Shopinsted</span>
        <span class="brand-tag">Fresh groceries delivered to your door</span>
      </div>
    </a>
    <div class="header-actions">
      <button class="cart-btn" onclick="openCart()">
        🛒 Cart <span class="cart-badge" id="hdr-badge">0</span>
      </button>
    </div>
  </div>
</header>

<!-- ════════════════════ HERO ════════════════════ -->
<div class="hero">
  <div class="hero-inner">
    <div class="hero-text">
      <h1>Your neighbourhood<br>grocery store, online.</h1>
      <p>Place your order — we'll confirm on WhatsApp &amp; deliver fresh!</p>
      <div class="hero-meta">
        <span class="hero-pill">📍 Bagaha, West Champaran, Bihar</span>
        <span class="hero-pill">📞 <a href="tel:+917999999999" style="color:inherit;text-decoration:none;">WhatsApp us</a></span>
        <span class="hero-pill">✅ Order &amp; Pay on delivery</span>
      </div>
    </div>
  </div>
</div>

<!-- ════════════════════ SEARCH ════════════════════ -->
<div class="search-wrap">
  <div class="search-box">
    <span>🔍</span>
    <input type="search" id="search-input" placeholder="Search products…" oninput="renderProducts()" autocomplete="off">
  </div>
</div>

<!-- ════════════════════ CATEGORIES ════════════════════ -->
<div class="cats-wrap" id="cats-wrap"></div>

<!-- ════════════════════ PRODUCTS ════════════════════ -->
<section class="products-section">
  <div class="section-title" id="section-title">All Products</div>
  <div class="products-grid" id="products-grid"></div>
</section>

<!-- ════════════════════ FLOATING BUTTONS ════════════════════ 
