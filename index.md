---
layout: null
permalink: /
---

<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Santhose Kumar S — Staff / Lead Software Engineer, Technical Lead and Engineering Manager." />
  <title>Santhose Kumar S | Staff / Lead Software Engineer</title>

  <style>
    :root {
      --bg: #0b1020;
      --bg-soft: #111a31;
      --surface: rgba(18, 27, 51, 0.74);
      --surface-strong: #15213f;
      --text: #eff5ff;
      --muted: #a8b6ce;
      --line: rgba(190, 209, 242, 0.15);
      --primary: #7dd3fc;
      --secondary: #c4b5fd;
      --accent: #86efac;
      --shadow: 0 18px 60px rgba(0, 0, 0, 0.28);
      --radius-lg: 28px;
      --radius-md: 18px;
      --max: 1120px;
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background:
        radial-gradient(circle at 0% 0%, rgba(125, 211, 252, 0.15), transparent 28rem),
        radial-gradient(circle at 100% 4%, rgba(196, 181, 253, 0.13), transparent 28rem),
        var(--bg);
      color: var(--text);
      line-height: 1.65;
    }

    a { color: inherit; text-decoration: none; }

    .page { width: min(100% - 32px, var(--max)); margin: 0 auto; }

    .nav {
      position: sticky;
      top: 0;
      z-index: 20;
      backdrop-filter: blur(18px);
      background: rgba(11, 16, 32, 0.78);
      border-bottom: 1px solid var(--line);
    }

    .nav-inner {
      width: min(100% - 32px, var(--max));
      min-height: 68px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }

    .brand { font-weight: 800; letter-spacing: 0.2px; }
    .brand span { color: var(--primary); }

    .nav-links {
      display: flex;
      gap: 20px;
      color: var(--muted);
      font-size: 0.94rem;
    }

    .nav-links a:hover { color: var(--text); }

    .hero {
      min-height: 700px;
      padding: 96px 0 72px;
      display: grid;
      grid-template-columns: 1.35fr 0.65fr;
      gap: 56px;
      align-items: center;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 12px;
      border: 1px solid rgba(125, 211, 252, 0.32);
      background: rgba(125, 211, 252, 0.08);
      border-radius: 999px;
      color: var(--primary);
      font-size: 0.82rem;
      font-weight: 750;
      letter-spacing: 0.04em;
      text-transform: uppercase;
    }

    h1, h2, h3, p { margin-top: 0; }

    h1 {
      margin: 18px 0 20px;
      max-width: 800px;
      font-size: clamp(2.7rem, 6vw, 5.4rem);
      line-height: 1.03;
      letter-spacing: -0.06em;
    }

    h1 .gradient {
      background: linear-gradient(100deg, var(--primary), var(--secondary), var(--accent));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .hero-copy {
      max-width: 710px;
      color: var(--muted);
      font-size: clamp(1.05rem, 2vw, 1.24rem);
    }

    .hero-copy strong { color: var(--text); }

    .actions {
      margin-top: 30px;
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
      padding: 13px 17px;
      border-radius: 12px;
      font-weight: 800;
      border: 1px solid transparent;
      transition: transform 180ms ease, box-shadow 180ms ease, background 180ms ease;
    }

    .button:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 28px rgba(0, 0, 0, 0.23);
    }

    .button-primary {
      color: #06101e;
      background: linear-gradient(110deg, var(--primary), var(--secondary));
    }

    .button-ghost {
      border-color: var(--line);
      background: rgba(255, 255, 255, 0.03);
      color: var(--text);
    }

    .profile-card {
      position: relative;
      overflow: hidden;
      border: 1px solid var(--line);
      border-radius: var(--radius-lg);
      padding: 28px;
      background:
        linear-gradient(145deg, rgba(125, 211, 252, 0.12), rgba(196, 181, 253, 0.09)),
        var(--surface);
      box-shadow: var(--shadow);
    }

    .profile-card::after {
      content: "";
      position: absolute;
      inset: auto -45px -65px auto;
      width: 190px;
      height: 190px;
      border-radius: 50%;
      background: rgba(134, 239, 172, 0.13);
      filter: blur(2px);
    }

    .avatar {
      display: block;
      width: min(100%, 270px);
      aspect-ratio: 1;
      margin: 0 auto 22px;
      object-fit: cover;
      border-radius: 24px;
      border: 1px solid rgba(255, 255, 255, 0.18);
      box-shadow: 0 16px 38px rgba(0, 0, 0, 0.24);
    }

    .profile-card h3 { margin-bottom: 4px; font-size: 1.28rem; }
    .profile-card p { margin-bottom: 18px; color: var(--muted); }

    .meta-list { display: grid; gap: 10px; font-size: 0.95rem; color: var(--muted); }
    .meta-list b { color: var(--text); }

    section { padding: 82px 0; }
    .section-title { max-width: 760px; margin-bottom: 30px; }
    .section-title h2 { font-size: clamp(2rem, 4vw, 3.2rem); letter-spacing: -0.04em; margin-bottom: 10px; }
    .section-title p { color: var(--muted); margin-bottom: 0; }

    .grid { display: grid; gap: 18px; }
    .grid-2 { grid-template-columns: repeat(2, minmax(0, 1fr)); }
    .grid-3 { grid-template-columns: repeat(3, minmax(0, 1fr)); }

    .card {
      border: 1px solid var(--line);
      border-radius: var(--radius-md);
      padding: 22px;
      background: var(--surface);
    }

    .card h3 { margin-bottom: 10px; font-size: 1.08rem; }
    .card p { margin-bottom: 0; color: var(--muted); }

    .skill {
      display: inline-flex;
      padding: 8px 10px;
      border-radius: 999px;
      border: 1px solid var(--line);
      background: rgba(255, 255, 255, 0.035);
      color: #dce9ff;
      font-size: 0.9rem;
      margin: 0 8px 8px 0;
    }

    .timeline { display: grid; gap: 18px; }

    .role {
      position: relative;
      border: 1px solid var(--line);
      border-radius: var(--radius-md);
      background: var(--surface);
      padding: 24px;
      overflow: hidden;
    }

    .role::before {
      content: "";
      position: absolute;
      left: 0;
      top: 0;
      bottom: 0;
      width: 4px;
      background: linear-gradient(var(--primary), var(--secondary));
    }

    .role-top {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 16px;
      margin-bottom: 14px;
    }

    .role h3 { margin: 0; font-size: 1.2rem; }
    .role .company { color: var(--primary); font-weight: 750; }
    .role .period { flex: 0 0 auto; color: var(--muted); font-size: 0.9rem; text-align: right; }
    .role ul { margin: 0; padding-left: 20px; color: var(--muted); }
    .role li + li { margin-top: 7px; }

    .highlight {
      color: var(--text);
      font-weight: 750;
    }

    .contact {
      border: 1px solid var(--line);
      border-radius: var(--radius-lg);
      padding: 42px;
      text-align: center;
      background:
        radial-gradient(circle at 50% 0%, rgba(125, 211, 252, 0.16), transparent 24rem),
        var(--surface);
    }

    .contact h2 { margin-bottom: 12px; font-size: clamp(2rem, 4vw, 3.1rem); letter-spacing: -0.04em; }
    .contact p { color: var(--muted); max-width: 650px; margin: 0 auto 24px; }

    footer {
      padding: 34px 0 48px;
      text-align: center;
      color: var(--muted);
      font-size: 0.92rem;
    }

    @media (max-width: 820px) {
      .hero { grid-template-columns: 1fr; padding-top: 70px; }
      .profile-card { max-width: 440px; }
      .grid-2, .grid-3 { grid-template-columns: 1fr; }
      .nav-links { display: none; }
    }

    @media (max-width: 560px) {
      .page, .nav-inner { width: min(100% - 24px, var(--max)); }
      section { padding: 60px 0; }
      .hero { gap: 34px; }
      .profile-card, .card, .role, .contact { padding: 20px; }
      .role-top { display: block; }
      .role .period { margin-top: 7px; text-align: left; }
      .actions { display: grid; }
      .button { width: 100%; }
    }
  </style>
</head>

<body>
  <nav class="nav">
    <div class="nav-inner">
      <a class="brand" href="#top">Santhose<span>.</span></a>
      <div class="nav-links">
        <a href="#about">About</a>
        <a href="#expertise">Expertise</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </nav>

  <main id="top" class="page">
    <section class="hero">
      <div>
        <span class="eyebrow">12+ years · Product & Platform Engineering</span>
        <h1>Building <span class="gradient">secure, scalable digital platforms</span> that make complex systems simpler.</h1>
        <p class="hero-copy">
          I am <strong>Santhose Kumar S</strong> — a Staff / Lead Software Engineer, Technical Lead, and Engineering Manager.
          I build API-led banking and SaaS platforms, guide engineering teams, and turn legacy complexity into reliable customer journeys.
        </p>

        <div class="actions">
          <a class="button button-primary" href="mailto:santhosekumar@ymail.com">✉️ Contact me</a>
          <a class="button button-ghost" href="https://www.linkedin.com/in/santhose-kumar-s-578515118/" target="_blank" rel="noreferrer">in LinkedIn</a>
          <a class="button button-ghost" href="https://github.com/santhosekumar19/" target="_blank" rel="noreferrer">⌘ GitHub</a>
        </div>
      </div>

      <aside class="profile-card">
        <!-- Upload santhosh_PP_White.jpg to the root of your repository -->
        <img class="avatar" src="santhosh_PP_White.jpg" alt="Santhose Kumar S" />
        <h3>Santhose Kumar S</h3>
        <p>Staff / Lead Software Engineer · Technical Lead · Engineering Manager</p>
        <div class="meta-list">
          <div>📍 <b>Based in:</b> Bengaluru, India</div>
          <div>🏦 <b>Focus:</b> Banking, SaaS & platform modernization</div>
          <div>🧭 <b>Strength:</b> Product delivery + engineering leadership</div>
        </div>
      </aside>
    </section>

    <section id="about">
      <div class="section-title">
        <h2>About</h2>
        <p>
          I work at the intersection of product engineering, platform modernization, and team leadership.
          My focus is helping organizations evolve tightly coupled applications into secure, observable, API-led services
          that are easier to build, operate, and grow.
        </p>
      </div>

      <div class="grid grid-3">
        <article class="card">
          <h3>⚡ Product delivery</h3>
          <p>Customer journeys, responsive applications, dashboards, reusable UI, and practical engineering outcomes.</p>
        </article>
        <article class="card">
          <h3>🔐 Platform modernization</h3>
          <p>Secure APIs, BFFs, core-system integration, distributed services, event-driven workflows, and resilient operations.</p>
        </article>
        <article class="card">
          <h3>🤝 Team leadership</h3>
          <p>Mentoring, technical direction, delivery planning, API standards, code quality, and cross-functional execution.</p>
        </article>
      </div>
    </section>

    <section id="expertise">
      <div class="section-title">
        <h2>Core expertise</h2>
        <p>Hands-on across product development, modern backend platforms, observability, and engineering enablement.</p>
      </div>

      <div class="grid grid-2">
        <article class="card">
          <h3>Product & full-stack engineering</h3>
          <div>
            <span class="skill">React</span><span class="skill">Next.js</span><span class="skill">TypeScript</span>
            <span class="skill">Node.js</span><span class="skill">Java</span><span class="skill">Spring Boot</span>
            <span class="skill">REST</span><span class="skill">GraphQL</span><span class="skill">SSR / ISR</span>
          </div>
        </article>

        <article class="card">
          <h3>Integration & distributed services</h3>
          <div>
            <span class="skill">API Gateway</span><span class="skill">BFF</span><span class="skill">Microservices</span>
            <span class="skill">Apache Kafka</span><span class="skill">Redis</span><span class="skill">3scale</span>
            <span class="skill">Event-driven workflows</span><span class="skill">Finacle integration</span>
          </div>
        </article>

        <article class="card">
          <h3>Cloud, reliability & delivery</h3>
          <div>
            <span class="skill">AWS</span><span class="skill">OpenShift</span><span class="skill">Kubernetes</span>
            <span class="skill">Docker</span><span class="skill">Jenkins</span><span class="skill">GitHub Actions</span>
            <span class="skill">AppDynamics</span><span class="skill">Elasticsearch / Kibana</span>
          </div>
        </article>

        <article class="card">
          <h3>Leadership & engineering practices</h3>
          <div>
            <span class="skill">Technical leadership</span><span class="skill">Mentoring</span>
            <span class="skill">Agile delivery</span><span class="skill">API documentation</span>
            <span class="skill">Code reviews</span><span class="skill">Release governance</span>
            <span class="skill">AI-assisted development</span><span class="skill">MCP automation</span>
          </div>
        </article>
      </div>
    </section>

    <section id="experience">
      <div class="section-title">
        <h2>Selected experience</h2>
        <p>Building platforms that connect customer experiences, business workflows, and operational reliability.</p>
      </div>

      <div class="timeline">
        <article class="role">
          <div class="role-top">
            <div>
              <h3>Lead Software Engineer</h3>
              <div class="company">Emirates NBD · Retail Banking Platform Modernization</div>
            </div>
            <div class="period">Nov 2025 – Present</div>
          </div>
          <ul>
            <li>Modernizing core-banking integrations into secure, reusable <span class="highlight">API-led services</span> using Node.js, Java/Spring Boot, Rust, Redis, Kafka, OpenShift, and 3scale.</li>
            <li>Reduced a critical request path from <span class="highlight">~10 ms to ~2 ms</span> through streamlined routing, caching, and integration flows.</li>
            <li>Established API contracts and documentation to reduce team dependencies and enable clearer delivery ownership.</li>
            <li>Improved production resilience with Kafka consumer-lag monitoring, DLQ workflows, AppDynamics APM, and Elasticsearch/Kibana observability.</li>
            <li>Introduced AI-assisted development and MCP-based automation for Java-to-Node migration analysis and engineering productivity.</li>
          </ul>
        </article>

        <article class="role">
          <div class="role-top">
            <div>
              <h3>Staff Software Engineer</h3>
              <div class="company">Okta · Product Experience</div>
            </div>
            <div class="period">Mar 2024 – Oct 2025</div>
          </div>
          <ul>
            <li>Built multilingual, mobile-first documentation and dashboard experiences with React, Next.js, Node.js, GraphQL, Redis, and AWS.</li>
            <li>Improved discoverability and page performance through SSR and ISR, delivering faster and SEO-friendly content experiences.</li>
            <li>Streamlined i18n onboarding and translation workflows for localized product publishing.</li>
          </ul>
        </article>

        <article class="role">
          <div class="role-top">
            <div>
              <h3>Software Consultant</h3>
              <div class="company">Randstad · Carbon Credit Exchange Platform</div>
            </div>
            <div class="period">Jun 2022 – May 2023</div>
          </div>
          <ul>
            <li>Replaced manual carbon-credit reporting with automated, role-based dashboards using React, Node.js, GraphQL, MongoDB, and AWS.</li>
            <li>Built exchange APIs and workflow services for trade, validation, and analytics flows.</li>
            <li>Automated secure releases with Docker and GitHub Actions; implemented JWT/RBAC and audit-ready data traceability.</li>
          </ul>
        </article>

        <article class="role">
          <div class="role-top">
            <div>
              <h3>Advanced Software Engineer</h3>
              <div class="company">Honeywell · Building Management & Sustainability</div>
            </div>
            <div class="period">Jun 2020 – Mar 2022</div>
          </div>
          <ul>
            <li>Modernized enterprise building-management dashboards with React, TypeScript, and Redux.</li>
            <li>Built reusable design-system components and microfrontend-ready foundations for B2B monitoring and sustainability workflows.</li>
            <li>Improved responsiveness and reliability through better client-side state, rendering, and API integration patterns.</li>
          </ul>
        </article>

        <article class="role">
          <div class="role-top">
            <div>
              <h3>Earlier experience</h3>
              <div class="company">Altimetrik · IBM / J.P. Morgan Chase · MFX Infotech</div>
            </div>
            <div class="period">2016 – 2020</div>
          </div>
          <ul>
            <li>Built real-time decision analytics platforms using React, Node.js, GraphQL, Docker, and AWS.</li>
            <li>Modernized internal financial tools using React, Angular, RxJS, Redux, and Cloud Foundry.</li>
            <li>Delivered multi-brand B2B, B2C, and B2B2C insurance portals using AngularJS, REST APIs, and PostgreSQL.</li>
          </ul>
        </article>
      </div>
    </section>

    <section>
      <div class="section-title">
        <h2>What I build</h2>
        <p>Examples of the problems I enjoy solving with teams.</p>
      </div>

      <div class="grid grid-3">
        <article class="card">
          <h3>🏦 Banking integration platforms</h3>
          <p>Secure API gateways, BFF services, core-system adapters, authorization, session management, and operational visibility.</p>
        </article>
        <article class="card">
          <h3>🔁 Event-driven workflows</h3>
          <p>Kafka processing, consumer-lag monitoring, DLQ handling, actionable alerts, and recovery-oriented operational design.</p>
        </article>
        <article class="card">
          <h3>🧩 Engineering enablement</h3>
          <p>Reusable API documentation, automated delivery, observability standards, mentoring, and AI-assisted developer workflows.</p>
        </article>
      </div>
    </section>

    <section id="contact">
      <div class="contact">
        <h2>Let’s build something meaningful.</h2>
        <p>Open to Staff Engineer, Lead Software Engineer, Technical Lead, Engineering Manager, and platform engineering opportunities.</p>
        <div class="actions" style="justify-content:center;">
          <a class="button button-primary" href="mailto:santhosekumar@ymail.com">✉️ Start a conversation</a>
          <a class="button button-ghost" href="https://www.linkedin.com/in/santhose-kumar-s-578515118/" target="_blank" rel="noreferrer">View LinkedIn</a>
        </div>
      </div>
    </section>

    <footer>
      © <span id="year"></span> Santhose Kumar S · Built with ownership, curiosity, and engineering discipline.
    </footer>
  </main>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
