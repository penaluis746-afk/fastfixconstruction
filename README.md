Got you—sounds like you want a simple HTML viewer: paste HTML on one side, see the result on the other.

Here’s a minimal self-contained HTML viewer you can save as viewer.html and open in your browser:

`html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Simple HTML Viewer</title>
  <style>
    body { margin: 0; font-family: sans-serif; display: flex; height: 100vh; }
    textarea { width: 50%; padding: 10px; border: none; border-right: 1px solid #ccc; font-family: monospace; }
    iframe { width: 50%; border: none; }
    header { position: fixed; top: 0; left: 0; right: 0; padding: 8px 12px; background: #222; color: #fff; font-size: 14px; }
    .wrap { display: flex; width: 100%; height: 100%; padding-top: 32px; box-sizing: border-box; }
  </style>
</head>
<body>
  <header>Simple HTML Viewer – type HTML on the left, see it on the right</header>
  <div class="wrap">
    <textarea id="source">
<!DOCTYPE html>
<html>
  <head>
    <title>Test</title>
  </head>
  <body>
    <h1>Hello, Luis 👋</h1>
    <p>This is your live HTML viewer.</p>
  </body>
</html>
    </textarea>
    <iframe id="preview"></iframe>
  </div>

  <script>
    const src = document.getElementById('source');
    const frame = document.getElementById('preview');

    function update() {
      const doc = frame.contentDocument || frame.contentWindow.document;
      doc.open();
      doc.write(src.value);
      doc.close();
    }

    src.addEventListener('input', update);
    window.addEventListener('load', update);
  </script>
</body>
</html>
`

If you tell me where you want to use this (phone, desktop app, website builder), I can tailor it.<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>FastFix Construction</title>

  <style>
    body {
      margin: 0;
      font-family: system-ui, sans-serif;
      background: #f3f4f6;
      color: #111827;
    }

    /* NAVBAR */
    header {
      background: #111827;
      color: white;
      padding: 18px 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 10;
    }
    header h1 {
      margin: 0;
      font-size: 22px;
      letter-spacing: 0.5px;
    }
    nav a {
      color: white;
      margin-left: 20px;
      text-decoration: none;
      font-size: 15px;
      font-weight: 500;
    }
    nav a:hover {
      color: #38bdf8;
    }

    /* HERO */
    .hero {
      background: url('https://images.unsplash.com/photo-1581091012184-5c8af7a4c7e6?auto=format&fit=crop&w=1400&q=80')
        center/cover no-repeat;
      height: 70vh;
      display: flex;
      align-items: center;
      padding: 0 40px;
      color: white;
      position: relative;
    }
    .hero::after {
      content: "";
      position: absolute;
      inset: 0;
      background: rgba(0,0,0,0.55);
    }
    .hero-content {
      position: relative;
      max-width: 600px;
    }
    .hero h2 {
      font-size: 42px;
      margin: 0 0 10px;
    }
    .hero p {
      font-size: 18px;
      margin-bottom: 20px;
    }
    .btn {
      background: #38bdf8;
      color: #0f172a;
      padding: 12px 22px;
      border-radius: 6px;
      text-decoration: none;
      font-weight: 600;
      font-size: 16px;
    }
    .btn:hover {
      background: #0ea5e9;
    }

    /* SECTIONS */
    section {
      padding: 60px 40px;
      max-width: 1100px;
      margin: auto;
    }
    h3 {
      font-size: 28px;
      margin-bottom: 20px;
      color: #0f172a;
    }

    /* SERVICES */
    .services {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 20px;
    }
    .service-card {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
      border-left: 5px solid #38bdf8;
    }
    .service-card h4 {
      margin: 0 0 10px;
      font-size: 20px;
    }
    .service-card p {
      margin: 0;
      color: #4b5563;
    }

    /* ABOUT */
    .about {
      background: white;
      border-radius: 12px;
      padding: 30px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    }

    /* CONTACT */
    .contact-box {
      background: #111827;
      color: white;
      padding: 30px;
      border-radius: 12px;
    }
    .contact-box p {
      margin: 8px 0;
      font-size: 16px;
    }

    /* FOOTER */
    footer {
      background: #0f172a;
      color: #9ca3af;
      text-align: center;
      padding: 20px;
      margin-top: 40px;
      font-size: 14px;
    }

    @media (max-width: 700px) {
      .hero h2 { font-size: 32px; }
      header { flex-direction: column; gap: 10px; }
    }
  </style>
</head>

<body>

  <!-- NAVBAR -->
  <header>
    <h1>FastFix Construction</h1>
    <nav>
      <a href="#services">Services</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-content">
      <h2>Fast, Reliable, Professional Construction</h2>
      <p>From drywall to full renovations — FastFix delivers clean workmanship, honest pricing, and fast turnaround.</p>
      <a class="btn" href="#contact">Get a Free Quote</a>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services">
    <h3>Our Services</h3>
    <div class="services">
      <div class="service-card">
        <h4>Drywall Installation</h4>
        <p>Perfect cuts, clean seams, and durable results for any room or project.</p>
      </div>
      <div class="service-card">
        <h4>Drywall Repair</h4>
        <p>Holes, cracks, water damage — we restore walls to flawless condition.</p>
      </div>
      <div class="service-card">
        <h4>Taping & Finishing</h4>
        <p>Level 4–5 finishes with smooth, professional results every time.</p>
      </div>
      <div class="service-card">
        <h4>Painting & Texture</h4>
        <p>Clean coats, custom textures, and modern finishes for any style.</p>
      </div>
      <div class="service-card">
        <h4>Framing & Remodeling</h4>
        <p>Basements, additions, and structural improvements done right.</p>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="about">
      <h3>About FastFix Construction</h3>
      <p>
        FastFix Construction is built on one promise: **quality work with zero stress**.
        We show up on time, protect your home, deliver clean craftsmanship, and finish fast.
      </p>
      <p>
        Whether it’s a small repair or a full renovation, we treat every project with pride and professionalism.
      </p>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <h3>Contact Us</h3>
    <div class="contact-box">
      <p><strong>📞 Phone:</strong> (708) 438-1640</p>
      <p><strong>📧 Email:</strong> penaluis746@gmail.com</p>
      <p><strong>📍 Service Area:</strong> Chicagoland & surrounding suburbs</p>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    © 2026 FastFix Construction — Built with pride and precision.
  </footer>

</body>
</html>
