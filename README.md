Here's a clean, modern-looking single-page website using only HTML + CSS (no JavaScript). It's a simple personal/portfolio-style landing page that looks good on both mobile and desktop.
HTML<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Ayyappa Naidu • Creative Developer</title>
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', system-ui, -apple-system, sans-serif;
      background: #0f0f11;
      color: #e0e0e5;
      line-height: 1.6;
      min-height: 100vh;
    }

    /* Header / Hero */
    header {
      height: 100vh;
      min-height: 680px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      background: linear-gradient(135deg, #0f0f11 0%, #1a1a24 100%);
      position: relative;
      overflow: hidden;
    }

    header::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: radial-gradient(circle at 20% 30%, rgba(99, 91, 255, 0.12) 0%, transparent 50%);
      pointer-events: none;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 900px;
      padding: 0 24px;
    }

    h1 {
      font-size: clamp(3.2rem, 8vw, 7.5rem);
      font-weight: 700;
      letter-spacing: -0.04em;
      margin-bottom: 1.2rem;
      background: linear-gradient(90deg, #a78bfa, #7c3aed, #c084fc);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .subtitle {
      font-size: clamp(1.25rem, 4vw, 1.8rem);
      color: #a0a0c0;
      margin-bottom: 2.5rem;
      font-weight: 300;
    }

    .cta-buttons {
      display: flex;
      gap: 1.5rem;
      justify-content: center;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-block;
      padding: 0.9rem 2.2rem;
      font-size: 1.1rem;
      font-weight: 500;
      text-decoration: none;
      border-radius: 50px;
      transition: all 0.3s ease;
    }

    .btn-primary {
      background: linear-gradient(90deg, #7c3aed, #a78bfa);
      color: white;
      box-shadow: 0 10px 30px rgba(124, 58, 237, 0.25);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 15px 40px rgba(124, 58, 237, 0.4);
    }

    .btn-outline {
      border: 1.5px solid #6b7280;
      color: #d1d5db;
    }

    .btn-outline:hover {
      background: rgba(255,255,255,0.08);
      border-color: #a0a0c0;
    }

    /* Sections */
    section {
      padding: 120px 24px;
      max-width: 1200px;
      margin: 0 auto;
    }

    h2 {
      font-size: 3.2rem;
      text-align: center;
      margin-bottom: 4rem;
      background: linear-gradient(90deg, #c4b5fd, #a78bfa);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 2rem;
    }

    .card {
      background: #17171f;
      border: 1px solid #2a2a38;
      border-radius: 16px;
      padding: 2.2rem;
      transition: all 0.35s ease;
    }

    .card:hover {
      transform: translateY(-12px);
      border-color: #7c3aed55;
      box-shadow: 0 20px 40px rgba(0,0,0,0.4);
    }

    .card h3 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
      color: #c4b5fd;
    }

    footer {
      text-align: center;
      padding: 4rem 1rem 6rem;
      color: #6b7280;
      font-size: 0.95rem;
      border-top: 1px solid #222233;
    }

    @media (max-width: 640px) {
      h1 { font-size: 3.8rem; }
      h2 { font-size: 2.4rem; }
      section { padding: 80px 20px; }
      .cta-buttons { flex-direction: column; gap: 1rem; }
    }
  </style>
</head>
<body>

  <header>
    <div class="hero-content">
      <h1>Alex Rivera</h1>
      <p class="subtitle">Creative Developer & Interface Designer</p>
      
      <div class="cta-buttons">
        <a href="#projects" class="btn btn-primary">View Projects</a>
        <a href="mailto:hello@alexrivera.dev" class="btn btn-outline">Get in Touch</a>
      </div>
    </div>
  </header>

  <section id="projects">
    <h2>Selected Work</h2>
    <div class="grid">
      <div class="card">
        <h3>Ethereal Dashboard</h3>
        <p>Modern analytics interface with glassmorphism, dark mode and real-time data visualization. Built with React & Tailwind.</p>
      </div>
      <div class="card">
        <h3>Neon Stories</h3>
        <p>Experimental storytelling platform with interactive 3D elements and scroll-based animations using Three.js.</p>
      </div>
      <div class="card">
        <h3>Flowstate App</h3>
        <p>Mobile-first productivity tool with calming UI, focus timers and ambient sound integration.</p>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2026 Alex Rivera — Made with curiosity and coffee</p>
  </footer>

</body>
</html>

