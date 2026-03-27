<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Ganesh Pawar — Frontend Developer</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=DM+Mono:wght@300;400;500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #0a0a0f;
      --surface: #111118;
      --border: #1e1e2e;
      --accent: #f4c842;
      --accent2: #e87c3e;
      --text: #e8e8f0;
      --muted: #6b6b80;
      --card: #14141e;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'DM Sans', sans-serif;
      min-height: 100vh;
      padding: 48px 24px;
      line-height: 1.6;
    }

    .wrapper {
      max-width: 760px;
      margin: 0 auto;
    }

    /* ── HEADER ── */
    .header {
      border-bottom: 1px solid var(--border);
      padding-bottom: 40px;
      margin-bottom: 48px;
      animation: fadeUp 0.6s ease both;
    }

    .greeting {
      font-family: 'DM Mono', monospace;
      font-size: 13px;
      color: var(--accent);
      letter-spacing: 0.15em;
      text-transform: uppercase;
      margin-bottom: 14px;
    }

    .name {
      font-family: 'Playfair Display', serif;
      font-size: clamp(40px, 8vw, 68px);
      font-weight: 900;
      line-height: 1.0;
      letter-spacing: -0.02em;
      color: var(--text);
    }

    .name span {
      color: var(--accent);
    }

    .tagline {
      font-family: 'DM Sans', sans-serif;
      font-size: 16px;
      color: var(--muted);
      margin-top: 14px;
      font-weight: 300;
      letter-spacing: 0.02em;
    }

    .tagline strong {
      color: var(--accent2);
      font-weight: 500;
    }

    /* ── SECTION LABEL ── */
    .section-label {
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      color: var(--muted);
      letter-spacing: 0.2em;
      text-transform: uppercase;
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .section-label::after {
      content: '';
      flex: 1;
      height: 1px;
      background: var(--border);
    }

    /* ── CONNECT ── */
    .connect-section {
      margin-bottom: 48px;
      animation: fadeUp 0.6s 0.1s ease both;
    }

    .social-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .social-link {
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 10px 18px;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 8px;
      text-decoration: none;
      color: var(--text);
      font-family: 'DM Mono', monospace;
      font-size: 13px;
      transition: border-color 0.2s, background 0.2s, transform 0.15s;
    }

    .social-link:hover {
      border-color: var(--accent);
      background: #1a1a24;
      transform: translateY(-2px);
    }

    .social-link svg {
      width: 18px;
      height: 18px;
      fill: var(--muted);
      transition: fill 0.2s;
      flex-shrink: 0;
    }

    .social-link:hover svg {
      fill: var(--accent);
    }

    /* ── SKILLS ── */
    .skills-section {
      margin-bottom: 48px;
      animation: fadeUp 0.6s 0.2s ease both;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(88px, 1fr));
      gap: 12px;
    }

    .skill-chip {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 8px;
      padding: 16px 10px;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 10px;
      transition: border-color 0.2s, background 0.2s, transform 0.15s;
      cursor: default;
    }

    .skill-chip:hover {
      border-color: var(--accent);
      background: #1a1a24;
      transform: translateY(-3px);
    }

    .skill-chip img {
      width: 32px;
      height: 32px;
      object-fit: contain;
    }

    .skill-chip span {
      font-family: 'DM Mono', monospace;
      font-size: 10px;
      color: var(--muted);
      text-align: center;
      letter-spacing: 0.05em;
    }

    .skill-chip:hover span {
      color: var(--accent);
    }

    /* ── FOOTER ── */
    .footer {
      border-top: 1px solid var(--border);
      padding-top: 28px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 12px;
      animation: fadeUp 0.6s 0.3s ease both;
    }

    .footer-text {
      font-family: 'DM Mono', monospace;
      font-size: 11px;
      color: var(--muted);
      letter-spacing: 0.08em;
    }

    .footer-dot {
      display: inline-block;
      width: 6px;
      height: 6px;
      background: var(--accent);
      border-radius: 50%;
      margin-right: 6px;
      animation: pulse 2s ease-in-out infinite;
    }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(18px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.4; transform: scale(0.7); }
    }
  </style>
</head>
<body>
  <div class="wrapper">

    <!-- HEADER -->
    <header class="header">
      <p class="greeting">// Hello, World!</p>
      <h1 class="name">Ganesh<br><span>Pawar</span></h1>
      <p class="tagline">Passionate <strong>Frontend Developer</strong> — crafting interfaces from Goa, India 🌊</p>
    </header>

    <!-- CONNECT -->
    <section class="connect-section">
      <div class="section-label">Connect</div>
      <div class="social-grid">

        <a class="social-link" href="https://www.linkedin.com/in/ganeshpawar243" target="_blank">
          <!-- LinkedIn -->
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M20.45 20.45h-3.554v-5.569c0-1.328-.024-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.352V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.284zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          LinkedIn
        </a>

        <a class="social-link" href="https://leetcode.com/u/pawarganesh243/" target="_blank">
          <!-- LeetCode -->
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M13.483 0a1.374 1.374 0 0 0-.961.438L7.116 6.226l-3.854 4.126a5.266 5.266 0 0 0-1.209 2.104 5.35 5.35 0 0 0-.125.513 5.527 5.527 0 0 0 .062 2.362 5.83 5.83 0 0 0 .349 1.017 5.938 5.938 0 0 0 1.271 1.818l4.277 4.193.039.038c2.248 2.165 5.852 2.133 8.063-.074l2.396-2.392c.54-.54.54-1.414.003-1.955a1.378 1.378 0 0 0-1.951-.003l-2.396 2.392a3.021 3.021 0 0 1-4.205.038l-.02-.019-4.276-4.193c-.652-.64-.972-1.469-.948-2.263a2.68 2.68 0 0 1 .066-.523 2.545 2.545 0 0 1 .619-1.164L9.13 8.114c1.058-1.134 3.204-1.27 4.43-.278l3.501 2.831c.593.48 1.461.387 1.94-.207a1.384 1.384 0 0 0-.207-1.943l-3.5-2.831c-.8-.647-1.766-1.045-2.774-1.202l2.015-2.158A1.384 1.384 0 0 0 13.483 0zm-2.866 12.815a1.38 1.38 0 0 0-1.38 1.382 1.38 1.38 0 0 0 1.38 1.382H20.79a1.38 1.38 0 0 0 1.38-1.382 1.38 1.38 0 0 0-1.38-1.382z"/></svg>
          LeetCode
        </a>

        <a class="social-link" href="https://www.instagram.com/ganeshpawar._/" target="_blank">
          <!-- Instagram -->
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 0 0 0-12.324zM12 16a4 4 0 1 1 0-8 4 4 0 0 1 0 8zm6.406-11.845a1.44 1.44 0 1 0 0 2.881 1.44 1.44 0 0 0 0-2.881z"/></svg>
          Instagram
        </a>

        <a class="social-link" href="https://discord.com/users/610053180583182342" target="_blank">
          <!-- Discord -->
          <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0 12.64 12.64 0 0 0-.617-1.25.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057c.002.022.015.043.032.054a19.9 19.9 0 0 0 5.993 3.03.078.078 0 0 0 .084-.028 14.09 14.09 0 0 0 1.226-1.994.076.076 0 0 0-.041-.106 13.107 13.107 0 0 1-1.872-.892.077.077 0 0 1-.008-.128 10.2 10.2 0 0 0 .372-.292.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127 12.299 12.299 0 0 1-1.873.892.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028 19.839 19.839 0 0 0 6.002-3.03.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03zM8.02 15.33c-1.183 0-2.157-1.085-2.157-2.419 0-1.333.956-2.419 2.157-2.419 1.21 0 2.176 1.096 2.157 2.42 0 1.333-.956 2.418-2.157 2.418zm7.975 0c-1.183 0-2.157-1.085-2.157-2.419 0-1.333.955-2.419 2.157-2.419 1.21 0 2.176 1.096 2.157 2.42 0 1.333-.946 2.418-2.157 2.418z"/></svg>
          Discord
        </a>

      </div>
    </section>

    <!-- SKILLS -->
    <section class="skills-section">
      <div class="section-label">Languages &amp; Tools</div>
      <div class="skills-grid">

        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="C"/>
          <span>C</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="C++"/>
          <span>C++</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="Java"/>
          <span>Java</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript"/>
          <span>JavaScript</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML5"/>
          <span>HTML5</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3"/>
          <span>CSS3</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="Node.js"/>
          <span>Node.js</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg" alt="Express" style="filter:invert(0.7)"/>
          <span>Express</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="MongoDB"/>
          <span>MongoDB</span>
        </div>
        <div class="skill-chip">
          <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="PostgreSQL"/>
          <span>PostgreSQL</span>
        </div>
        <div class="skill-chip">
          <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="Firebase"/>
          <span>Firebase</span>
        </div>

      </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
      <span class="footer-text"><span class="footer-dot"></span>Open to opportunities</span>
      <span class="footer-text">Goa, India 🌴 — 2025</span>
    </footer>

  </div>
</body>
</html>
