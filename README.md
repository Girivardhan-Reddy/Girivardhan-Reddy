<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Girivardhan-Reddy · Premium Profile</title>
  <!-- Font & minimal reset -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      background: #0a0a12;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
      display: flex;
      justify-content: center;
      padding: 2rem 1rem;
      color: #eef2f6;
      line-height: 1.5;
    }
    .readme-container {
      max-width: 1100px;
      width: 100%;
      background: radial-gradient(circle at 20% 30%, #12121f, #07070e);
      border-radius: 3rem;
      padding: 2.5rem 2.5rem 2rem;
      box-shadow: 0 30px 80px rgba(0,0,0,0.8), 0 0 0 1px rgba(120, 80, 255, 0.08);
      position: relative;
      overflow: hidden;
    }
    /* Glow orbs */
    .readme-container::before {
      content: '';
      position: absolute;
      width: 600px;
      height: 600px;
      background: radial-gradient(circle at 30% 40%, rgba(90, 40, 255, 0.08), transparent 70%);
      top: -200px;
      left: -200px;
      z-index: 0;
      pointer-events: none;
    }
    .readme-container::after {
      content: '';
      position: absolute;
      width: 500px;
      height: 500px;
      background: radial-gradient(circle at 80% 70%, rgba(0, 200, 255, 0.05), transparent 70%);
      bottom: -150px;
      right: -150px;
      z-index: 0;
      pointer-events: none;
    }
    /* all content above background */
    .content {
      position: relative;
      z-index: 2;
    }
    /* hero banner */
    .hero {
      background: linear-gradient(145deg, #14142a, #1a1a30);
      border-radius: 2.5rem;
      padding: 3.5rem 2.5rem;
      margin-bottom: 3.5rem;
      position: relative;
      overflow: hidden;
      box-shadow: 0 20px 40px -12px rgba(0,0,0,0.7), inset 0 0 0 1px rgba(180, 140, 255, 0.15);
      backdrop-filter: blur(4px);
    }
    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at 70% 20%, #3a2a7a, transparent 60%);
      opacity: 0.25;
    }
    .hero-glow {
      position: absolute;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(70, 130, 255, 0.15), transparent 70%);
      top: -100px;
      right: -100px;
      border-radius: 50%;
    }
    .hero-content {
      position: relative;
      z-index: 2;
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
    }
    .hero-badge {
      background: rgba(120, 80, 255, 0.15);
      backdrop-filter: blur(8px);
      padding: 0.3rem 1.2rem;
      border-radius: 40px;
      display: inline-flex;
      align-items: center;
      width: fit-content;
      border: 1px solid rgba(180, 140, 255, 0.15);
      font-size: 0.85rem;
      font-weight: 500;
      letter-spacing: 0.3px;
      color: #b7adff;
      margin-bottom: 0.5rem;
    }
    .hero h1 {
      font-size: 4.2rem;
      font-weight: 800;
      letter-spacing: -0.03em;
      background: linear-gradient(135deg, #eef2ff, #b7adff, #7aa2ff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      line-height: 1.1;
    }
    .hero .title-line {
      font-size: 1.7rem;
      font-weight: 400;
      color: #c8d0f0;
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 0.4rem;
    }
    .typing-wrapper {
      display: inline-block;
      background: linear-gradient(135deg, #5f4bdb, #3b82f6);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      font-weight: 600;
    }
    .hero-desc {
      font-size: 1.1rem;
      max-width: 700px;
      color: #bcc3e0;
      margin-top: 0.75rem;
      border-left: 3px solid #6a5acd;
      padding-left: 1.2rem;
      font-weight: 300;
    }
    .badge-group {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem 1rem;
      margin-top: 0.75rem;
    }
    .badge-group span {
      background: rgba(255,255,255,0.03);
      backdrop-filter: blur(6px);
      padding: 0.3rem 1rem;
      border-radius: 30px;
      font-size: 0.8rem;
      border: 1px solid rgba(255,255,255,0.04);
      color: #bcc6e6;
      letter-spacing: 0.2px;
    }
    /* section style */
    .section-title {
      font-size: 2rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      margin-bottom: 1.8rem;
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }
    .section-title span {
      background: linear-gradient(135deg, #a78bfa, #60a5fa);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    .section-title .accent-line {
      width: 60px;
      height: 3px;
      background: linear-gradient(90deg, #7c6af0, transparent);
      border-radius: 4px;
    }
    .card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1.8rem;
      margin: 2rem 0 2.5rem;
    }
    .card {
      background: rgba(20, 20, 40, 0.6);
      backdrop-filter: blur(12px);
      border-radius: 2rem;
      padding: 1.8rem 1.5rem;
      border: 1px solid rgba(180, 150, 255, 0.06);
      box-shadow: 0 12px 30px -10px rgba(0,0,0,0.4);
      transition: 0.25s ease;
    }
    .card:hover {
      transform: translateY(-4px);
      border-color: rgba(130, 100, 255, 0.2);
      box-shadow: 0 20px 40px -10px rgba(70, 40, 200, 0.15);
    }
    .card-icon {
      font-size: 2rem;
      margin-bottom: 0.5rem;
      display: block;
    }
    .card h4 {
      font-size: 1.25rem;
      font-weight: 600;
      color: #e0e6ff;
      margin-bottom: 0.3rem;
    }
    .card p {
      color: #aab2d6;
      font-weight: 300;
      font-size: 0.95rem;
    }
    .skill-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem 1.2rem;
      background: rgba(10,10,25,0.3);
      backdrop-filter: blur(4px);
      padding: 1.8rem 2rem;
      border-radius: 3rem;
      border: 1px solid rgba(255,255,255,0.02);
      margin: 1.5rem 0 2.5rem;
    }
    .skill-item {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 1rem;
      background: rgba(255,255,255,0.02);
      padding: 0.4rem 1.2rem 0.4rem 0.8rem;
      border-radius: 40px;
      border: 1px solid rgba(255,255,255,0.02);
      backdrop-filter: blur(2px);
    }
    .skill-item img {
      width: 32px;
      height: 32px;
      filter: drop-shadow(0 0 4px rgba(100, 80, 255, 0.2));
    }
    .stat-row {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem 4rem;
      background: rgba(10,10,28,0.3);
      backdrop-filter: blur(4px);
      padding: 2rem 2.5rem;
      border-radius: 3rem;
      border: 1px solid rgba(255,255,255,0.02);
      margin: 2rem 0 2.5rem;
      justify-content: center;
    }
    .stat-item {
      text-align: center;
    }
    .stat-number {
      font-size: 2.5rem;
      font-weight: 700;
      background: linear-gradient(135deg, #c4b5fd, #93bbfc);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    .stat-label {
      font-weight: 300;
      color: #aab2d6;
      letter-spacing: 0.3px;
    }
    .social-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem;
      margin: 2.5rem 0 2rem;
    }
    .social-btn {
      background: rgba(255,255,255,0.02);
      border: 1px solid rgba(255,255,255,0.04);
      padding: 0.7rem 1.8rem;
      border-radius: 60px;
      color: #d0d8f0;
      text-decoration: none;
      font-weight: 500;
      backdrop-filter: blur(8px);
      transition: 0.2s;
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 0.95rem;
    }
    .social-btn:hover {
      background: rgba(120, 80, 255, 0.1);
      border-color: rgba(180, 140, 255, 0.2);
      transform: scale(1.02);
    }
    .footer {
      margin-top: 3.5rem;
      padding-top: 2rem;
      border-top: 1px solid rgba(255,255,255,0.02);
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 1rem;
      font-size: 0.9rem;
      color: #6b7394;
    }
    /* divider */
    .divider-svg {
      width: 100%;
      height: 28px;
      margin: 1rem 0 2rem;
      opacity: 0.15;
      filter: drop-shadow(0 0 6px #4a3a8a);
    }
    /* particles placeholder (animated via css) */
    .particle-bg {
      position: absolute;
      inset: 0;
      overflow: hidden;
      pointer-events: none;
      z-index: 1;
    }
    .particle {
      position: absolute;
      width: 6px;
      height: 6px;
      background: rgba(140, 120, 255, 0.15);
      border-radius: 50%;
      animation: floatParticle 18s infinite alternate ease-in-out;
    }
    @keyframes floatParticle {
      0% { transform: translate(0, 0) scale(1); opacity: 0.1; }
      100% { transform: translate(40px, -60px) scale(1.8); opacity: 0.5; }
    }
    /* responsive */
    @media (max-width: 650px) {
      .hero h1 { font-size: 2.8rem; }
      .readme-container { padding: 1.5rem; }
      .hero { padding: 2rem 1.5rem; }
      .stat-row { gap: 1.5rem; }
    }
  </style>
</head>
<body>
<div class="readme-container">
  <!-- animated particles (static positions, css animation) -->
  <div class="particle-bg">
    <div class="particle" style="top:10%;left:5%;animation-delay:0s;"></div>
    <div class="particle" style="top:25%;left:85%;animation-delay:2s;width:10px;height:10px;"></div>
    <div class="particle" style="top:55%;left:15%;animation-delay:4s;"></div>
    <div class="particle" style="top:70%;left:70%;animation-delay:1s;width:8px;height:8px;"></div>
    <div class="particle" style="top:90%;left:40%;animation-delay:3s;"></div>
    <div class="particle" style="top:40%;left:40%;animation-delay:5s;width:12px;height:12px;background:rgba(80,160,255,0.08);"></div>
  </div>

  <div class="content">

    <!-- HERO BANNER -->
    <div class="hero">
      <div class="hero-glow"></div>
      <div class="hero-content">
        <div class="hero-badge">✦  B.Tech · 2026  ✦</div>
        <h1>Vennapusa Girivardhan Reddy</h1>
        <div class="title-line">
          <span>AI & ML Enthusiast</span>
          <span style="color:#6b7bb0;">|</span>
          <span class="typing-wrapper">Java Full Stack Developer</span>
          <span style="color:#6b7bb0;">|</span>
          <span>IoT & Web Innovator</span>
        </div>
        <div class="hero-desc">
          Passionate about building intelligent applications, predictive systems, web platforms, 
          and innovative solutions using AI, machine learning, IoT, and modern technologies.
        </div>
        <div class="badge-group">
          <span>📍 India</span>
          <span>🎓 B.Tech (Batch 2026)</span>
          <span>⚡ AI · IoT · Full‑Stack</span>
        </div>
      </div>
    </div>

    <!-- DIVIDER SVG (futuristic) -->
    <svg class="divider-svg" viewBox="0 0 1200 30" preserveAspectRatio="none">
      <path d="M0,15 Q150,0 300,15 T600,15 T900,15 T1200,15 L1200,30 L0,30 Z" fill="url(#gradDiv)" opacity="0.5"/>
      <defs>
        <linearGradient id="gradDiv" x1="0%" y1="0%" x2="100%" y2="0%">
          <stop offset="0%" stop-color="#6a5acd" stop-opacity="0" />
          <stop offset="25%" stop-color="#8b7af0" stop-opacity="0.6" />
          <stop offset="50%" stop-color="#4f8cf7" stop-opacity="0.9" />
          <stop offset="75%" stop-color="#8b7af0" stop-opacity="0.6" />
          <stop offset="100%" stop-color="#6a5acd" stop-opacity="0" />
        </linearGradient>
      </defs>
    </svg>

    <!-- ABOUT ME + modern cards -->
    <div style="display:flex; flex-wrap:wrap; gap:2rem; margin-bottom:0.5rem;">
      <div style="flex:1; min-width:240px;">
        <div class="section-title"><span>About Me</span><div class="accent-line"></div></div>
        <p style="font-weight:300; color:#bcc3e0; max-width:500px; font-size:1.05rem;">
          I'm a passionate developer and innovator, merging AI, IoT, and full‑stack development 
          to craft systems that make a difference. Currently pursuing B.Tech, I love turning 
          complex ideas into elegant, intelligent solutions.
        </p>
      </div>
      <div style="flex:1; min-width:200px; background:rgba(255,255,255,0.01); border-radius:2rem; padding:0.8rem 1.8rem; backdrop-filter:blur(4px); border:1px solid rgba(255,255,255,0.02);">
        <div style="display:flex; gap:1.8rem; flex-wrap:wrap;">
          <div><span style="color:#8b9bd0;">📍</span> India</div>
          <div><span style="color:#8b9bd0;">🎓</span> B.Tech 2026</div>
          <div><span style="color:#8b9bd0;">🧠</span> AI/ML · Java · IoT</div>
        </div>
      </div>
    </div>

    <!-- WHAT I CAN DO -->
    <div class="section-title" style="margin-top:2.8rem;"><span>What I Can Do</span><div class="accent-line"></div></div>
    <div class="card-grid">
      <div class="card"><span class="card-icon">🧠</span><h4>AI & ML Apps</h4><p>Intelligent systems, predictive models & NLP</p></div>
      <div class="card"><span class="card-icon">☕</span><h4>Java Full‑Stack</h4><p>Spring Boot, microservices, robust backends</p></div>
      <div class="card"><span class="card-icon">🌐</span><h4>Responsive Websites</h4><p>Modern, fast, accessible frontends</p></div>
      <div class="card"><span class="card-icon">📡</span><h4>IoT Systems</h4><p>Connected devices, real‑time data pipelines</p></div>
      <div class="card"><span class="card-icon">🎬</span><h4>Movie Production Platforms</h4><p>End‑to‑end media & workflow tools</p></div>
      <div class="card"><span class="card-icon">⚙️</span><h4>Automation Tools</h4><p>Streamline workflows, CI/CD, bots</p></div>
      <div class="card"><span class="card-icon">📊</span><h4>Predictive Systems</h4><p>Forecasting, analytics, decision intelligence</p></div>
    </div>

    <!-- SKILLS animated icons -->
    <div class="section-title" style="margin-top:1.5rem;"><span>Skills & Tools</span><div class="accent-line"></div></div>
    <div class="skill-grid">
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=java" alt="Java" /> Java</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=spring" alt="Spring" /> Spring</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=python" alt="Python" /> Python</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=tensorflow" alt="TF" /> TensorFlow</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=react" alt="React" /> React</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=nodejs" alt="Node" /> Node</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=aws" alt="AWS" /> AWS</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=docker" alt="Docker" /> Docker</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=git" alt="Git" /> Git</span>
      <span class="skill-item"><img src="https://skillicons.dev/icons?i=postgres" alt="Postgres" /> PostgreSQL</span>
    </div>

    <!-- STATISTICS SECTION -->
    <div class="section-title"><span>Highlights</span><div class="accent-line"></div></div>
    <div class="stat-row">
      <div class="stat-item"><div class="stat-number">10+</div><div class="stat-label">Projects Built</div></div>
      <div class="stat-item"><div class="stat-number">6</div><div class="stat-label">AI/ML Models</div></div>
      <div class="stat-item"><div class="stat-number">4</div><div class="stat-label">IoT Prototypes</div></div>
      <div class="stat-item"><div class="stat-number">8</div><div class="stat-label">Web Platforms</div></div>
    </div>

    <!-- SOCIAL LINKS -->
    <div class="section-title" style="margin-top:1.5rem;"><span>Connect</span><div class="accent-line"></div></div>
    <div class="social-links">
      <a href="#" class="social-btn">🐙 GitHub</a>
      <a href="#" class="social-btn">🔗 LinkedIn</a>
      <a href="#" class="social-btn">🐦 Twitter</a>
      <a href="#" class="social-btn">📧 Email</a>
      <a href="#" class="social-btn">📄 Portfolio</a>
    </div>

    <!-- FOOTER with animation -->
    <div class="footer">
      <span>✦ Vennapusa Girivardhan Reddy · 2026</span>
      <span style="display:flex; gap:0.5rem; align-items:center;">
        <span style="display:inline-block; width:8px; height:8px; border-radius:50%; background: #6a5acd; box-shadow: 0 0 12px #6a5acd;"></span>
        AI · IoT · Full‑Stack
      </span>
      <span>✨ built with ❤️</span>
    </div>

    <!-- TYPING EFFECT (via CSS + inline span) + capsule render subtle -->
    <div style="height:2px; background:linear-gradient(90deg, transparent, #4f46e5, transparent); width:60%; margin:1rem auto 0; opacity:0.15;"></div>
  </div>
</div>
</body>
</html>
