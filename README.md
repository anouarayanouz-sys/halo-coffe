<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Halo Coffee</title>
  <style>
    :root{
      --bg:#0f0f10;
      --panel:#161616;
      --muted:#bdbdbd;
      --accent:#d4a373;
      --card:#1c1c1c;
      --glass: rgba(255,255,255,0.02);
      --radius:12px;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background:var(--bg);
      color:#fff;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }
    header{
      padding:28px 20px;
      text-align:center;
      background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
      border-bottom:1px solid rgba(255,255,255,0.03);
    }
    header h1{
      margin:0;
      font-size:2rem;
      letter-spacing:1px;
      color:var(--accent);
    }
    header p{margin:6px 0 0;color:var(--muted)}
    nav{
      display:flex;
      justify-content:center;
      gap:18px;
      padding:14px 10px;
      background:var(--panel);
      position:sticky;
      top:0;
      z-index:20;
    }
    nav a{
      color:var(--muted);
      text-decoration:none;
      font-weight:600;
    }
    nav a:hover{color:var(--accent)}
    main{
      max-width:980px;
      margin:36px auto;
      padding:0 18px 60px;
    }
    .section-title{
      display:flex;
      align-items:center;
      gap:12px;
      margin-bottom:14px;
    }
    .section-title h2{
      margin:0;
      color:var(--accent);
      font-size:1.2rem;
    }
    .card-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:14px;
    }
    .card{
      background:var(--card);
      border-radius:var(--radius);
      padding:14px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.5);
      transition:transform .18s ease, box-shadow .18s ease;
    }
    .card:hover{ transform:translateY(-6px); box-shadow:0 10px 25px rgba(0,0,0,0.6) }
    .card h3{margin:6px 0;color:#fff;font-size:1rem}
    .card p{margin:0;color:var(--muted);font-size:.92rem}
    section{margin-bottom:28px}
    #about p{color:var(--muted)}
    footer{
      text-align:center;
      padding:18px;
      color:rgba(255,255,255,0.5);
      border-top:1px solid rgba(255,255,255,0.03);
      background:var(--panel);
    }
    a.cta{
      display:inline-block;
      margin-top:10px;
      padding:8px 14px;
      border-radius:10px;
      background:linear-gradient(90deg,var(--accent), #c8925e);
      color:#111;
      text-decoration:none;
      font-weight:700;
    }
    @media (max-width:520px){
      header h1{font-size:1.4rem}
    }
  </style>
</head>
<body>
  <header>
    <h1>Halo Coffee ☕</h1>
    <p>Modern flavors — Moroccan heart</p>
  </header>

  <nav>
    <a href="#menu">Menu</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>

  <main>
    <section id="menu">
      <div class="section-title">
        <h2>Our Menu</h2>
      </div>

      <h3 style="color:var(--accent);margin-top:6px">Tea</h3>
      <div class="card-grid" style="margin-bottom:16px">
        <div class="card"><h3>Mint Tea</h3><p>Traditional Moroccan mint with fresh leaves and sugar.</p></div>
        <div class="card"><h3>Black Tea</h3><p>Rich and full-bodied — served hot or iced.</p></div>
        <div class="card"><h3>Green Tea</h3><p>Light and refreshing.</p></div>
      </div>

      <h3 style="color:var(--accent)">Coffee</h3>
      <div class="card-grid" style="margin-bottom:16px">
        <div class="card"><h3>Espresso</h3><p>Intense and aromatic.</p></div>
        <div class="card"><h3>Cappuccino</h3><p>Velvety foam with a bold brew.</p></div>
        <div class="card"><h3>Latte</h3><p>Smooth, creamy, balanced.</p></div>
      </div>

      <h3 style="color:var(--accent)">Cakes</h3>
      <div class="card-grid" style="margin-bottom:16px">
        <div class="card"><h3>Chocolate Cake</h3><p>Moist and decadent.</p></div>
        <div class="card"><h3>Cheesecake</h3><p>Creamy classic.</p></div>
        <div class="card"><h3>Lemon Tart</h3><p>Bright and zesty.</p></div>
      </div>

      <h3 style="color:var(--accent)">Moroccan Breakfasts</h3>
      <div class="card-grid">
        <div class="card"><h3>Msemen</h3><p>Flaky pancake served with honey.</p></div>
        <div class="card"><h3>Baghrir</h3><p>Spongy thousand-hole pancakes.</p></div>
        <div class="card"><h3>Amlou & Bread</h3><p>Almond-argan spread with fresh bread.</p></div>
      </div>
    </section>

    <section id="about">
      <div class="section-title"><h2>About Us</h2></div>
      <p>Halo Coffee brings a modern cafe experience with Moroccan warmth. Quality beans, freshly prepared breakfasts and homemade pastries.</p>
      <a class="cta" href="#contact">Contact & Orders</a>
    </section>

    <section id="contact">
      <div class="section-title"><h2>Contact</h2></div>
      <p style="color:var(--muted);margin-bottom:8px">Email: <a href="mailto:contact@halocoffee.com" style="color:var(--accent)">contact@halocoffee.com</a></p>
      <p style="color:var(--muted)">Address: Avenue Hassan II, Al Hoceima, Morocco</p>
    </section>
  </main>

  <footer>© <span id="year"></span> Halo Coffee</footer>

  <script>
    // small helpers: current year + smooth scroll behavior
    document.getElementById('year').textContent = new Date().getFullYear();
    // smooth scroll for local anchors
    if ('scrollBehavior' in document.documentElement.style) {
      document.querySelectorAll('a[href^="#"]').forEach(a=>{
        a.addEventListener('click', e=>{
          e.preventDefault();
          const id = a.getAttribute('href').slice(1);
          const el = document.getElementById(id);
          if(el) el.scrollIntoView({behavior:'smooth', block:'start'});
        });
      });
    }
  </script>
</body>
</html>
