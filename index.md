---
layout: null
permalink: /
---

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Santhose Kumar S — Staff / Lead Software Engineer, Technical Lead and Engineering Manager." />
  <meta name="theme-color" content="#0b1020" id="theme-color" />
  <title>Santhose Kumar S | Engineering Portfolio</title>

  <style>
    :root {
      --canvas: #0b1020;
      --canvas-soft: #101a33;
      --surface: rgba(18, 29, 55, 0.76);
      --surface-solid: #14203d;
      --surface-hover: #17284b;
      --text: #f3f7ff;
      --muted: #aebbd3;
      --line: rgba(187, 209, 249, 0.16);
      --primary: #73d8ff;
      --secondary: #ad9cff;
      --accent: #8ee7b4;
      --button-text: #07111e;
      --header: rgba(11, 16, 32, 0.84);
      --shadow: 0 22px 70px rgba(0, 0, 0, 0.30);
      --card-shadow: 0 12px 38px rgba(0, 0, 0, 0.11);
    }

    [data-theme="light"] {
      --canvas: #f5f8ff;
      --canvas-soft: #eef4ff;
      --surface: rgba(255, 255, 255, 0.82);
      --surface-solid: #ffffff;
      --surface-hover: #f7faff;
      --text: #10203c;
      --muted: #5e6d86;
      --line: rgba(43, 65, 105, 0.14);
      --primary: #087bbd;
      --secondary: #6653d6;
      --accent: #16885d;
      --button-text: #ffffff;
      --header: rgba(245, 248, 255, 0.86);
      --shadow: 0 20px 58px rgba(31, 53, 92, 0.12);
      --card-shadow: 0 12px 34px rgba(39, 62, 102, 0.08);
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      min-width: 320px;
      color: var(--text);
      background:
        radial-gradient(circle at 8% -6%, color-mix(in srgb, var(--primary) 18%, transparent), transparent 31rem),
        radial-gradient(circle at 93% 0%, color-mix(in srgb, var(--secondary) 16%, transparent), transparent 29rem),
        radial-gradient(circle at 50% 100%, color-mix(in srgb, var(--accent) 9%, transparent), transparent 30rem),
        var(--canvas);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.62;
      transition: background 260ms ease, color 260ms ease;
      overflow-x: hidden;
    }

    a { color: inherit; text-decoration: none; }
    button { font: inherit; }
    .container { width: min(calc(100% - 32px), 1160px); margin: 0 auto; }

    /* Header */
    .site-header {
      position: sticky;
      top: 0;
      z-index: 60;
      border-bottom: 1px solid transparent;
      transition: background 220ms ease, border-color 220ms ease, box-shadow 220ms ease;
    }
    .site-header.is-scrolled {
      background: var(--header);
      border-color: var(--line);
      box-shadow: 0 10px 34px rgba(0,0,0,0.12);
      backdrop-filter: blur(18px);
    }
    .nav {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }
    .wordmark {
      display: inline-flex;
      align-items: center;
      gap: 11px;
      font-size: 1rem;
      font-weight: 820;
      letter-spacing: -0.025em;
      white-space: nowrap;
    }
    .mark {
      display: grid;
      place-items: center;
      width: 34px;
      height: 34px;
      border-radius: 11px;
      color: #07111e;
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      box-shadow: 0 8px 22px color-mix(in srgb, var(--primary) 26%, transparent);
      font-size: 0.84rem;
      font-weight: 900;
    }
    .wordmark b { color: var(--primary); }

    .desktop-links {
      display: flex;
      align-items: center;
      gap: 22px;
      color: var(--muted);
      font-size: 0.93rem;
      font-weight: 700;
    }
    .desktop-links a {
      position: relative;
      padding: 8px 0;
      transition: color 180ms ease;
    }
    .desktop-links a::after {
      content: "";
      position: absolute;
      left: 0;
      right: 0;
      bottom: 2px;
      height: 2px;
      border-radius: 999px;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 180ms ease;
    }
    .desktop-links a:hover, .desktop-links a:focus-visible { color: var(--text); }
    .desktop-links a:hover::after, .desktop-links a:focus-visible::after { transform: scaleX(1); }

    .theme-toggle, .menu-button {
      display: inline-grid;
      place-items: center;
      width: 42px;
      height: 42px;
      border: 1px solid var(--line);
      border-radius: 12px;
      color: var(--text);
      background: var(--surface);
      cursor: pointer;
      transition: transform 180ms ease, border-color 180ms ease, background 180ms ease;
    }
    .theme-toggle:hover, .menu-button:hover {
      transform: translateY(-2px);
      border-color: color-mix(in srgb, var(--primary) 46%, var(--line));
      background: var(--surface-hover);
    }
    .theme-toggle { margin-left: 2px; }
    .menu-button { display: none; }

    .mobile-menu {
      display: none;
      grid-template-columns: 1fr auto;
      gap: 8px;
      padding: 0 16px 16px;
    }
    .mobile-menu.open { display: grid; }
    .mobile-menu a {
      grid-column: 1 / -1;
      padding: 13px 14px;
      border: 1px solid var(--line);
      border-radius: 12px;
      color: var(--muted);
      background: var(--surface-solid);
      font-weight: 700;
    }
    .mobile-menu a:hover { color: var(--text); border-color: color-mix(in srgb, var(--primary) 46%, var(--line)); }

    /* Hero */
    .hero {
      min-height: 700px;
      display: grid;
      place-items: center;
      padding: 84px 0 66px;
    }
    .hero-content {
      width: 100%;
      max-width: 980px;
      text-align: center;
      animation: hero-in 760ms cubic-bezier(.2,.8,.2,1) both;
    }
    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 13px;
      border: 1px solid color-mix(in srgb, var(--primary) 31%, var(--line));
      border-radius: 999px;
      color: var(--primary);
      background: color-mix(in srgb, var(--primary) 8%, transparent);
      font-size: 0.78rem;
      font-weight: 850;
      letter-spacing: 0.075em;
      text-transform: uppercase;
    }
    .eyebrow::before {
      content: "";
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 0 5px color-mix(in srgb, var(--accent) 13%, transparent);
    }
    h1 {
      margin: 20px auto 18px;
      max-width: 930px;
      font-size: clamp(3rem, 7vw, 6.4rem);
      line-height: 0.98;
      letter-spacing: -0.068em;
    }
    .gradient {
      background: linear-gradient(110deg, var(--primary), color-mix(in srgb, var(--text) 90%, var(--primary)), var(--secondary));
      background-size: 180% 100%;
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      animation: shimmer 8s linear infinite;
    }
    .hero-copy {
      max-width: 770px;
      margin: 0 auto;
      color: var(--muted);
      font-size: clamp(1.06rem, 2.1vw, 1.27rem);
    }
    .hero-copy strong { color: var(--text); }

    .typing-row {
      min-height: 34px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      margin-top: 19px;
      padding: 7px 13px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: var(--surface);
      color: var(--text);
      font-size: 0.94rem;
      font-weight: 720;
    }
    .typing-prefix { color: var(--muted); }
    .typing-text { color: var(--primary); }
    .typing-cursor { color: var(--primary); animation: blink 850ms step-end infinite; }

    .actions {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 30px;
    }
    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 47px;
      padding: 0 18px;
      border: 1px solid transparent;
      border-radius: 12px;
      font-size: 0.95rem;
      font-weight: 790;
      transition: transform 180ms ease, box-shadow 180ms ease, background 180ms ease, border-color 180ms ease;
    }
    .button:hover { transform: translateY(-2px); box-shadow: 0 12px 26px rgba(0,0,0,0.19); }
    .button-primary { color: var(--button-text); background: linear-gradient(110deg, var(--primary), var(--secondary)); }
    [data-theme="dark"] .button-primary { color: #07111e; }
    .button-secondary { color: var(--text); border-color: var(--line); background: var(--surface); }
    .button-secondary:hover { border-color: color-mix(in srgb, var(--primary) 46%, var(--line)); background: var(--surface-hover); }

    .slider {
      position: relative;
      max-width: 800px;
      min-height: 122px;
      margin: 50px auto 0;
      overflow: hidden;
      border: 1px solid var(--line);
      border-radius: 18px;
      background: var(--surface);
      box-shadow: var(--card-shadow);
    }
    .slides { display: flex; width: 300%; transition: transform 600ms cubic-bezier(.2,.8,.2,1); }
    .slide {
      width: 33.333%;
      padding: 22px 24px;
      display: grid;
      grid-template-columns: auto 1fr;
      align-items: center;
      gap: 16px;
      text-align: left;
    }
    .slide-icon {
      display: grid;
      place-items: center;
      width: 42px;
      height: 42px;
      border-radius: 14px;
      background: linear-gradient(135deg, color-mix(in srgb, var(--primary) 20%, transparent), color-mix(in srgb, var(--secondary) 18%, transparent));
      font-size: 1.2rem;
    }
    .slide h3 { margin: 0 0 2px; font-size: 1rem; }
    .slide p { margin: 0; color: var(--muted); font-size: 0.93rem; }
    .slider-dots { display: flex; justify-content: center; gap: 7px; padding: 0 0 14px; }
    .dot { width: 7px; height: 7px; border-radius: 50%; background: var(--line); transition: transform 180ms ease, background 180ms ease; }
    .dot.active { background: var(--primary); transform: scale(1.35); }

    /* Content */
    section { padding: 82px 0; }
    .section-head { max-width: 780px; margin-bottom: 30px; }
    .section-kicker { margin-bottom: 8px; color: var(--primary); font-size: 0.79rem; font-weight: 850; letter-spacing: 0.08em; text-transform: uppercase; }
    h2 { margin: 0 0 10px; font-size: clamp(2.05rem, 4.3vw, 3.3rem); line-height: 1.06; letter-spacing: -0.052em; }
    .section-head p { margin: 0; color: var(--muted); font-size: 1.04rem; }
    .grid { display: grid; gap: 18px; }
    .grid-2 { grid-template-columns: repeat(2, minmax(0, 1fr)); }
    .grid-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }
    .card {
      padding: 23px;
      border: 1px solid var(--line);
      border-radius: 20px;
      background: var(--surface);
      box-shadow: var(--card-shadow);
      transition: transform 200ms ease, border-color 200ms ease, background 200ms ease;
    }
    .card:hover { transform: translateY(-5px); border-color: color-mix(in srgb, var(--primary) 38%, var(--line)); background: var(--surface-hover); }
    .card-icon { display: grid; place-items: center; width: 42px; height: 42px; margin-bottom: 14px; border-radius: 14px; background: linear-gradient(135deg, color-mix(in srgb, var(--primary) 20%, transparent), color-mix(in srgb, var(--secondary) 18%, transparent)); font-size: 1.12rem; }
    .card h3 { margin: 0 0 8px; font-size: 1.07rem; letter-spacing: -0.015em; }
    .card p { margin: 0; color: var(--muted); font-size: 0.96rem; }
    .tag { display: inline-flex; margin: 0 7px 8px 0; padding: 7px 10px; border: 1px solid var(--line); border-radius: 999px; color: var(--text); background: color-mix(in srgb, var(--surface-solid) 80%, transparent); font-size: 0.87rem; font-weight: 650; transition: transform 160ms ease, border-color 160ms ease; }
    .tag:hover { transform: translateY(-2px); border-color: color-mix(in srgb, var(--secondary) 46%, var(--line)); }

    /* Experience */
    .experience-list { display: grid; gap: 18px; }
    .role { position: relative; overflow: hidden; padding: 26px 26px 26px 30px; border: 1px solid var(--line); border-radius: 20px; background: var(--surface); transition: transform 200ms ease, border-color 200ms ease; }
    .role::before { content: ""; position: absolute; top: 0; bottom: 0; left: 0; width: 4px; background: linear-gradient(to bottom, var(--primary), var(--secondary), var(--accent)); }
    .role:hover { transform: translateY(-4px); border-color: color-mix(in srgb, var(--primary) 38%, var(--line)); }
    .role-header { display: flex; align-items: flex-start; justify-content: space-between; gap: 20px; margin-bottom: 14px; }
    .role h3 { margin: 0; font-size: 1.18rem; letter-spacing: -0.02em; }
    .company { margin-top: 2px; color: var(--primary); font-weight: 780; }
    .period { color: var(--muted); font-size: 0.90rem; white-space: nowrap; }
    .role ul { margin: 0; padding-left: 19px; color: var(--muted); }
    .role li + li { margin-top: 7px; }
    .role strong { color: var(--text); }

    .contact {
      padding: 54px 28px;
      text-align: center;
      border: 1px solid var(--line);
      border-radius: 30px;
      background: radial-gradient(circle at 50% 0%, color-mix(in srgb, var(--primary) 15%, transparent), transparent 26rem), var(--surface);
    }
    .contact p { max-width: 690px; margin: 0 auto; color: var(--muted); }
    .contact-links { display: flex; justify-content: center; flex-wrap: wrap; gap: 10px; margin-top: 18px; color: var(--muted); font-size: 0.94rem; }
    .contact-links a { padding: 4px 8px; border-radius: 8px; }
    .contact-links a:hover { color: var(--text); background: var(--surface-hover); }

    footer { padding: 34px 0 46px; text-align: center; color: var(--muted); font-size: 0.90rem; }
    .reveal { opacity: 0; transform: translateY(18px); transition: opacity 520ms ease, transform 520ms ease; }
    .reveal.visible { opacity: 1; transform: translateY(0); }

    @keyframes hero-in { from { opacity: 0; transform: translateY(22px); } to { opacity: 1; transform: translateY(0); } }
    @keyframes shimmer { 0% { background-position: 0% 50%; } 100% { background-position: 180% 50%; } }
    @keyframes blink { 50% { opacity: 0; } }

    @media (max-width: 900px) {
      .desktop-links { display: none; }
      .menu-button { display: inline-grid; }
      .theme-toggle { margin-left: auto; }
      .grid-2, .grid-3 { grid-template-columns: 1fr; }
      .hero { min-height: auto; padding-top: 76px; }
    }
    @media (max-width: 620px) {
      .container { width: min(calc(100% - 24px), 1160px); }
      .nav { min-height: 68px; }
      h1 { font-size: clamp(2.75rem, 13vw, 4.5rem); }
      .hero-copy { font-size: 1.02rem; }
      .actions { display: grid; }
      .button { width: 100%; }
      .slider { margin-top: 36px; }
      .slide { padding: 19px; }
      .role-header { display: block; }
      .period { display: block; margin-top: 7px; white-space: normal; }
      .role, .card { padding: 20px; }
      .role { padding-left: 24px; }
      section { padding: 62px 0; }
      .contact { padding: 40px 20px; }
    }
    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
      *, *::before, *::after { animation-duration: 0.01ms !important; animation-iteration-count: 1 !important; transition-duration: 0.01ms !important; }
    }
  </style>
</head>

<body>
  <header class="site-header" id="site-header">
    <div class="container nav">
      <a class="wordmark" href="#top" aria-label="Santhose Kumar S home">
        <span class="mark">SK</span>
        <span>Santhose <b>Kumar S</b></span>
      </a>

      <nav class="desktop-links" aria-label="Primary navigation">
        <a href="#about">About</a>
        <a href="#expertise">Expertise</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
      </nav>

      <button class="theme-toggle" id="theme-toggle" type="button" aria-label="Toggle light or dark theme" title="Toggle theme">◐</button>
      <button class="menu-button" id="menu-button" type="button" aria-label="Open navigation menu" aria-expanded="false" aria-controls="mobile-menu">☰</button>
    </div>

    <nav class="mobile-menu" id="mobile-menu" aria-label="Mobile navigation">
      <a href="#about">About</a>
      <a href="#expertise">Expertise</a>
      <a href="#experience">Experience</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main id="top" class="container">
    <section class="hero">
      <div class="hero-content">
        <span class="eyebrow">12+ years · Engineering, product & platform delivery</span>
        <h1>Turning complex systems into <span class="gradient">secure, scalable digital products.</span></h1>
        <p class="hero-copy">
          I am <strong>Santhose Kumar S</strong> — a Staff / Lead Software Engineer, Technical Lead, and Engineering Manager, Engineering Leader.
          I build and modernize products across <strong>Banking, Insurance, Financial Services, SaaS, and enterprise platforms.</strong>
        </p>

        <div class="typing-row" aria-live="polite">
          <span class="typing-prefix">Focused on</span>
          <span class="typing-text" id="typing-text"></span><span class="typing-cursor">|</span>
        </div>

        <div class="actions">
          <a class="button button-primary" href="mailto:santhosekumar@ymail.com">Email Me</a>
          <a class="button button-secondary" href="tel:+919035361129">Call +91 90353 61129</a>
          <a class="button button-secondary" href="https://github.com/santhosekumar19/" target="_blank" rel="noreferrer">GitHub</a>
          <a class="button button-secondary" href="https://www.linkedin.com/in/santhose-kumar-s-578515118/" target="_blank" rel="noreferrer">LinkedIn</a>
        </div>

        <div class="slider" aria-label="Professional focus highlights">
          <div class="slides" id="slides">
            <article class="slide">
              <div class="slide-icon">🏦</div>
              <div><h3>Banking & Financial Services</h3><p>Secure integrations, API platforms, core-system modernization, and reliable customer journeys.</p></div>
            </article>
            <article class="slide">
              <div class="slide-icon">🚀</div>
              <div><h3>Product Development & Scaling</h3><p>Customer-facing experiences, reusable services, performance, and pragmatic engineering outcomes.</p></div>
            </article>
            <article class="slide">
              <div class="slide-icon">✦</div>
              <div><h3>Digital Transformation & AI Adoption</h3><p>AI-assisted development, MCP automation, modernization workflows, observability, and delivery enablement.</p></div>
            </article>
          </div>
          <div class="slider-dots" aria-hidden="true">
            <span class="dot active"></span><span class="dot"></span><span class="dot"></span>
          </div>
        </div>
      </div>
    </section>

    <section id="about" class="reveal">
      <div class="section-head">
        <div class="section-kicker">About</div>
        <h2>Product thinking. Platform depth. Team momentum.</h2>
        <p>
          I help organizations move from tightly coupled applications to reliable, API-led services that are easier to build, operate, and evolve.
          My work blends hands-on engineering, digital transformation, technical direction, delivery leadership, and measurable product impact.
        </p>
      </div>

      <div class="grid grid-3">
        <article class="card"><div class="card-icon">⚡</div><h3>Product Development</h3><p>Customer journeys, responsive applications, dashboards, reusable UI, and practical business outcomes.</p></article>
        <article class="card"><div class="card-icon">🔐</div><h3>Digital Transformation</h3><p>Secure APIs, BFFs, integration modernization, distributed services, event-driven workflows, and resilience.</p></article>
        <article class="card"><div class="card-icon">🤝</div><h3>AI Adoption & Leadership</h3><p>AI-assisted delivery, MCP automation, mentoring, engineering standards, and cross-functional execution.</p></article>
      </div>
    </section>

    <section id="expertise" class="reveal">
      <div class="section-head">
        <div class="section-kicker">Core Expertise</div>
        <h2>Technology with purpose.</h2>
        <p>Focused on the stack and practices that make products secure, observable, scalable, and easier to evolve.</p>
      </div>

      <div class="grid grid-2">
        <article class="card"><h3>Product & full-stack engineering</h3><span class="tag">React</span><span class="tag">Next.js</span><span class="tag">TypeScript</span><span class="tag">Node.js</span><span class="tag">Java</span><span class="tag">Spring Boot</span><span class="tag">REST</span><span class="tag">GraphQL</span><span class="tag">SSR / ISR</span></article>
        <article class="card"><h3>Banking, Insurance & Integration</h3><span class="tag">API Gateway</span><span class="tag">BFF</span><span class="tag">Microservices</span><span class="tag">Finacle integration</span><span class="tag">3scale</span><span class="tag">Secure API contracts</span><span class="tag">RBAC</span></article>
        <article class="card"><h3>Scaling & distributed services</h3><span class="tag">Apache Kafka</span><span class="tag">Redis</span><span class="tag">Rust</span><span class="tag">Event-driven workflows</span><span class="tag">Caching</span><span class="tag">DLQ handling</span><span class="tag">Performance optimization</span></article>
        <article class="card"><h3>Cloud, reliability & delivery</h3><span class="tag">AWS</span><span class="tag">OpenShift</span><span class="tag">Kubernetes</span><span class="tag">Docker</span><span class="tag">Jenkins</span><span class="tag">GitHub Actions</span><span class="tag">AppDynamics</span><span class="tag">Elasticsearch / Kibana</span></article>
        <article class="card"><h3>Leadership & quality</h3><span class="tag">Technical leadership</span><span class="tag">Mentoring</span><span class="tag">Agile delivery</span><span class="tag">API documentation</span><span class="tag">Code reviews</span><span class="tag">Release governance</span><span class="tag">Stakeholder management</span></article>
        <article class="card"><h3>AI adoption & automation</h3><span class="tag">AI-assisted development</span><span class="tag">MCP automation</span><span class="tag">Java-to-Node migration</span><span class="tag">Developer productivity</span><span class="tag">Code modernization</span></article>
      </div>
    </section>

    <section id="experience" class="reveal">
      <div class="section-head">
        <div class="section-kicker">Experience</div>
        <h2>Selected work and impact.</h2>
        <p>Building products that connect customer experience, business workflows, secure integration, and production reliability.</p>
      </div>

      <div class="experience-list">
        <article class="role">
          <div class="role-header"><div><h3>Lead Software Engineer</h3><div class="company">Emirates NBD · Retail Banking Platform Modernization</div></div><div class="period">Nov 2025 – Present</div></div>
          <ul>
            <li>Modernizing core-banking integrations into secure, reusable <strong>API-led services</strong> using Node.js, Java/Spring Boot, Rust, Redis, Kafka, OpenShift, and 3scale.</li>
            <li>Reduced a critical request path from <strong>~10 ms to ~2 ms</strong> through streamlined routing, caching, and integration flows.</li>
            <li>Established API contracts and documentation to reduce handoff friction and create clearer delivery ownership across teams.</li>
            <li>Improved production resilience with Kafka consumer-lag monitoring, DLQ workflows, AppDynamics APM, and Elasticsearch/Kibana observability.</li>
            <li>Introduced AI-assisted development and MCP-based automation for Java-to-Node migration analysis and engineering productivity.</li>
          </ul>
        </article>

        <article class="role">
          <div class="role-header"><div><h3>Staff Software Engineer</h3><div class="company">Okta · Product Experience</div></div><div class="period">Mar 2024 – Oct 2025</div></div>
          <ul>
            <li>Built multilingual, mobile-first documentation and dashboard experiences with React, Next.js, Node.js, GraphQL, Redis, and AWS.</li>
            <li>Improved discoverability and page performance through SSR and ISR, delivering faster and SEO-friendly content experiences.</li>
            <li>Streamlined i18n onboarding and translation workflows for localized product publishing.</li>
          </ul>
        </article>

        <article class="role">
          <div class="role-header"><div><h3>Software Consultant</h3><div class="company">Randstad · Carbon Credit Exchange Platform</div></div><div class="period">Jun 2022 – May 2023</div></div>
          <ul>
            <li>Replaced manual carbon-credit reporting with automated, role-based dashboards using React, Node.js, GraphQL, MongoDB, and AWS.</li>
            <li>Built exchange APIs and workflow services for trade, validation, and analytics flows.</li>
            <li>Automated secure releases with Docker and GitHub Actions; implemented JWT/RBAC and audit-ready data traceability.</li>
          </ul>
        </article>

        <article class="role">
          <div class="role-header"><div><h3>Advanced Software Engineer</h3><div class="company">Honeywell · Building Management & Sustainability</div></div><div class="period">Jun 2020 – Mar 2022</div></div>
          <ul>
            <li>Modernized enterprise building-management dashboards with React, TypeScript, and Redux.</li>
            <li>Built reusable design-system components and microfrontend-ready foundations for B2B monitoring and sustainability workflows.</li>
            <li>Improved responsiveness and reliability through better client-side state, rendering, and API-integration patterns.</li>
          </ul>
        </article>

        <article class="role">
          <div class="role-header"><div><h3>Earlier Experience</h3><div class="company">Altimetrik · IBM / J.P. Morgan Chase · MFX Infotech</div></div><div class="period">2016 – 2020</div></div>
          <ul>
            <li>Built real-time decision analytics platforms using React, Node.js, GraphQL, Docker, and AWS.</li>
            <li>Modernized internal financial tools using React, Angular, RxJS, Redux, and Cloud Foundry.</li>
            <li>Delivered multi-brand B2B, B2C, and B2B2C insurance portals using AngularJS, REST APIs, and PostgreSQL.</li>
          </ul>
        </article>
      </div>
    </section>

    <section id="contact" class="reveal">
      <div class="contact">
        <div class="section-kicker">Contact</div>
        <h2>Let’s build something meaningful.</h2>
        <p>Open to Staff Engineer, Lead Software Engineer, Technical Lead, Engineering Manager, and platform engineering opportunities.</p>
        <div class="actions">
          <a class="button button-primary" href="mailto:santhosekumar@ymail.com">Email santhosekumar@ymail.com</a>
          <a class="button button-secondary" href="tel:+919035361129">Call +91 90353 61129</a>
          <a class="button button-secondary" href="https://github.com/santhosekumar19/" target="_blank" rel="noreferrer">github.com/santhosekumar19</a>
        </div>
        <div class="contact-links">
          <a href="https://www.linkedin.com/in/santhose-kumar-s-578515118/" target="_blank" rel="noreferrer">LinkedIn</a>
          <span>•</span>
          <a href="https://github.com/santhosekumar19/" target="_blank" rel="noreferrer">GitHub</a>
          <span>•</span>
          <a href="mailto:santhosekumar@ymail.com">Email</a>
        </div>
      </div>
    </section>

    <footer>© <span id="year"></span> Santhose Kumar S · Built with ownership, curiosity, and engineering discipline.</footer>
  </main>

  <script>
    const root = document.documentElement;
    const themeToggle = document.getElementById("theme-toggle");
    const themeColor = document.getElementById("theme-color");

    function applyTheme(theme) {
      root.setAttribute("data-theme", theme);
      localStorage.setItem("sk-theme", theme);
      themeToggle.textContent = theme === "light" ? "☾" : "☀";
      themeToggle.setAttribute("aria-label", theme === "light" ? "Switch to dark theme" : "Switch to light theme");
      themeColor.setAttribute("content", theme === "light" ? "#f5f8ff" : "#0b1020");
    }

    const savedTheme = localStorage.getItem("sk-theme");
    const systemTheme = window.matchMedia("(prefers-color-scheme: light)").matches ? "light" : "dark";
    applyTheme(savedTheme || systemTheme);
    themeToggle.addEventListener("click", () => applyTheme(root.getAttribute("data-theme") === "light" ? "dark" : "light"));

    const header = document.getElementById("site-header");
    const menuButton = document.getElementById("menu-button");
    const mobileMenu = document.getElementById("mobile-menu");
    const setHeaderState = () => header.classList.toggle("is-scrolled", window.scrollY > 12);
    setHeaderState();
    window.addEventListener("scroll", setHeaderState, { passive: true });

    menuButton.addEventListener("click", () => {
      const open = mobileMenu.classList.toggle("open");
      menuButton.setAttribute("aria-expanded", String(open));
      menuButton.textContent = open ? "✕" : "☰";
    });
    mobileMenu.querySelectorAll("a").forEach((link) => link.addEventListener("click", () => {
      mobileMenu.classList.remove("open");
      menuButton.setAttribute("aria-expanded", "false");
      menuButton.textContent = "☰";
    }));

    const phrases = [
      "secure API-led platforms",
      "banking & financial services modernization",
      "insurance and SaaS product development",
      "scaling distributed, event-driven services",
      "digital transformation and AI adoption"
    ];
    const typing = document.getElementById("typing-text");
    let phraseIndex = 0, charIndex = 0, deleting = false;
    function typeLoop() {
      const phrase = phrases[phraseIndex];
      typing.textContent = deleting ? phrase.slice(0, charIndex--) : phrase.slice(0, charIndex++);
      let delay = deleting ? 35 : 55;
      if (!deleting && charIndex > phrase.length) { deleting = true; delay = 1500; }
      else if (deleting && charIndex < 0) { deleting = false; phraseIndex = (phraseIndex + 1) % phrases.length; charIndex = 0; delay = 420; }
      setTimeout(typeLoop, delay);
    }
    typeLoop();

    const slides = document.getElementById("slides");
    const dots = Array.from(document.querySelectorAll(".dot"));
    let slideIndex = 0;
    function showSlide(index) {
      slides.style.transform = `translateX(-${index * 33.333333}%)`;
      dots.forEach((dot, i) => dot.classList.toggle("active", i === index));
    }
    setInterval(() => { slideIndex = (slideIndex + 1) % 3; showSlide(slideIndex); }, 4300);

    document.getElementById("year").textContent = new Date().getFullYear();
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) { entry.target.classList.add("visible"); observer.unobserve(entry.target); }
      });
    }, { threshold: 0.12 });
    document.querySelectorAll(".reveal").forEach((item) => observer.observe(item));
  </script>
</body>
</html>
