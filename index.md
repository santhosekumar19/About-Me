---
layout: null
permalink: /
---

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Santhose Kumar S — Staff / Lead Software Engineer, Technical Lead and Engineering Manager." />
  <meta name="theme-color" content="#0a1020" />
  <title>Santhose Kumar S | Engineering Portfolio</title>
  <style>
    :root {
      --canvas:#0a1020; --surface:rgba(18,28,54,.74); --surface-solid:#121d38;
      --line:rgba(177,201,240,.16); --text:#f4f8ff; --muted:#aebbd3;
      --primary:#74d8ff; --secondary:#a99afc; --success:#8ee7b4;
      --radius:20px; --radius-lg:30px; --max:1140px;
    }
    *{box-sizing:border-box} html{scroll-behavior:smooth}
    body{margin:0;color:var(--text);font-family:Inter,ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;line-height:1.65;overflow-x:hidden;background:radial-gradient(circle at 12% -8%,rgba(116,216,255,.18),transparent 30rem),radial-gradient(circle at 95% 4%,rgba(169,154,252,.16),transparent 29rem),radial-gradient(circle at 48% 98%,rgba(142,231,180,.09),transparent 29rem),var(--canvas)}
    a{color:inherit;text-decoration:none}.container{width:min(calc(100% - 32px),var(--max));margin:auto}

    /* Header and navigation — shares the same palette as the hero */
    .site-header{position:sticky;top:0;z-index:50;border-bottom:1px solid transparent;transition:background .22s ease,border-color .22s ease,box-shadow .22s ease}
    .site-header.is-scrolled{background:rgba(10,16,32,.86);border-color:var(--line);box-shadow:0 10px 34px rgba(0,0,0,.18);backdrop-filter:blur(18px)}
    .nav{min-height:76px;display:flex;align-items:center;justify-content:space-between;gap:24px}
    .wordmark{display:inline-flex;align-items:center;gap:11px;font-size:1.02rem;font-weight:820;letter-spacing:-.02em}.wordmark-mark{width:32px;height:32px;display:grid;place-items:center;border-radius:10px;color:#061121;background:linear-gradient(135deg,var(--primary),var(--secondary));box-shadow:0 8px 24px rgba(116,216,255,.24);font-size:.86rem}.wordmark b{color:var(--primary)}
    .desktop-links{display:flex;align-items:center;gap:24px;color:var(--muted);font-size:.94rem;font-weight:650}.desktop-links a{position:relative;padding:8px 0;transition:color .18s ease}.desktop-links a:after{content:"";position:absolute;right:0;bottom:2px;left:0;height:2px;border-radius:99px;transform:scaleX(0);transform-origin:left;background:linear-gradient(90deg,var(--primary),var(--secondary));transition:transform .18s ease}.desktop-links a:hover,.desktop-links a:focus-visible{color:var(--text)}.desktop-links a:hover:after,.desktop-links a:focus-visible:after{transform:scaleX(1)}
    .nav-cta{padding:9px 14px!important;border:1px solid rgba(116,216,255,.30);border-radius:10px;color:var(--text)!important;background:rgba(116,216,255,.08)}.nav-cta:after{display:none}.nav-cta:hover{border-color:rgba(116,216,255,.68);background:rgba(116,216,255,.15)}
    .menu-button{display:none;width:44px;height:44px;border:1px solid var(--line);border-radius:12px;color:var(--text);background:rgba(255,255,255,.035);cursor:pointer;font-size:1.15rem}.mobile-menu{display:none;padding:0 16px 16px}.mobile-menu.open{display:grid;gap:6px}.mobile-menu a{padding:13px 14px;border:1px solid var(--line);border-radius:12px;color:var(--muted);background:rgba(18,28,54,.9);font-weight:680}.mobile-menu a:hover{color:var(--text);border-color:rgba(116,216,255,.45)}

    /* Hero */
    .hero{min-height:680px;display:grid;place-items:center;padding:80px 0 70px}.hero-inner{width:100%;max-width:930px;text-align:center;animation:hero-enter .76s cubic-bezier(.2,.8,.2,1) both}.eyebrow{display:inline-flex;align-items:center;gap:8px;padding:8px 13px;border:1px solid rgba(116,216,255,.30);border-radius:999px;color:var(--primary);background:rgba(116,216,255,.075);font-size:.78rem;font-weight:800;letter-spacing:.07em;text-transform:uppercase}.eyebrow:before{content:"";width:7px;height:7px;border-radius:50%;background:var(--success);box-shadow:0 0 0 5px rgba(142,231,180,.10)}
    h1{margin:21px auto 18px;max-width:900px;font-size:clamp(2.9rem,7vw,6.4rem);line-height:.98;letter-spacing:-.065em}.gradient-text{background:linear-gradient(110deg,var(--primary),#d9efff 45%,var(--secondary));background-size:180% 100%;-webkit-background-clip:text;background-clip:text;color:transparent;animation:shimmer 7s linear infinite}.hero-subtitle{max-width:740px;margin:auto;color:var(--muted);font-size:clamp(1.05rem,2.2vw,1.25rem)}.hero-subtitle strong{color:var(--text)}
    .actions{display:flex;justify-content:center;flex-wrap:wrap;gap:12px;margin-top:30px}.button{display:inline-flex;align-items:center;justify-content:center;min-height:47px;padding:0 18px;border:1px solid transparent;border-radius:12px;font-size:.95rem;font-weight:790;transition:transform .18s ease,box-shadow .18s ease,background .18s ease,border-color .18s ease}.button:hover{transform:translateY(-2px);box-shadow:0 12px 26px rgba(0,0,0,.22)}.button-primary{color:#061121;background:linear-gradient(110deg,var(--primary),var(--secondary))}.button-secondary{color:var(--text);border-color:var(--line);background:rgba(255,255,255,.035)}.button-secondary:hover{border-color:rgba(116,216,255,.45);background:rgba(116,216,255,.09)}
    .hero-strip{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;max-width:740px;margin:52px auto 0;text-align:left}.hero-metric{padding:15px 17px;border:1px solid var(--line);border-radius:16px;background:rgba(18,28,54,.50);backdrop-filter:blur(10px);transition:transform .18s ease,border-color .18s ease}.hero-metric:hover{transform:translateY(-4px);border-color:rgba(116,216,255,.35)}.hero-metric b{display:block;font-size:1.03rem}.hero-metric span{display:block;margin-top:2px;color:var(--muted);font-size:.86rem}

    /* Sections */
    section{padding:82px 0}.section-head{max-width:760px;margin-bottom:30px}.section-kicker{margin-bottom:8px;color:var(--primary);font-size:.80rem;font-weight:800;letter-spacing:.08em;text-transform:uppercase}h2{margin:0 0 10px;font-size:clamp(2rem,4.2vw,3.25rem);line-height:1.06;letter-spacing:-.05em}.section-head p{margin:0;color:var(--muted);font-size:1.04rem}.grid{display:grid;gap:18px}.grid-2{grid-template-columns:repeat(2,minmax(0,1fr))}.grid-3{grid-template-columns:repeat(3,minmax(0,1fr))}
    .card{padding:23px;border:1px solid var(--line);border-radius:var(--radius);background:var(--surface);box-shadow:0 12px 36px rgba(0,0,0,.08);transition:transform .2s ease,border-color .2s ease,background .2s ease}.card:hover{transform:translateY(-5px);border-color:rgba(116,216,255,.36);background:rgba(22,35,66,.86)}.card-icon{display:grid;place-items:center;width:42px;height:42px;margin-bottom:15px;border-radius:14px;background:linear-gradient(135deg,rgba(116,216,255,.20),rgba(169,154,252,.18));font-size:1.1rem}.card h3{margin:0 0 8px;font-size:1.07rem;letter-spacing:-.015em}.card p{margin:0;color:var(--muted);font-size:.96rem}
    .skill-card h3{margin-bottom:14px}.tag{display:inline-flex;margin:0 7px 8px 0;padding:7px 10px;border:1px solid var(--line);border-radius:999px;color:#d8e7ff;background:rgba(255,255,255,.035);font-size:.87rem;font-weight:620;transition:transform .16s ease,border-color .16s ease}.tag:hover{transform:translateY(-2px);border-color:rgba(169,154,252,.45)}

    /* Experience */
    .experience-list{display:grid;gap:18px}.role{position:relative;overflow:hidden;padding:26px 26px 26px 30px;border:1px solid var(--line);border-radius:var(--radius);background:var(--surface);transition:transform .2s ease,border-color .2s ease}.role:before{content:"";position:absolute;inset:0 auto 0 0;width:4px;background:linear-gradient(to bottom,var(--primary),var(--secondary),var(--success))}.role:hover{transform:translateY(-4px);border-color:rgba(116,216,255,.36)}.role-header{display:flex;align-items:flex-start;justify-content:space-between;gap:20px;margin-bottom:14px}.role h3{margin:0;font-size:1.18rem;letter-spacing:-.02em}.company{margin-top:2px;color:var(--primary);font-weight:780}.period{color:var(--muted);font-size:.90rem;white-space:nowrap}.role ul{margin:0;padding-left:19px;color:var(--muted)}.role li+li{margin-top:7px}.role strong{color:var(--text)}
    .contact{text-align:center;padding:52px 26px;border:1px solid var(--line);border-radius:var(--radius-lg);background:radial-gradient(circle at 50% 0%,rgba(116,216,255,.16),transparent 27rem),var(--surface)}.contact p{max-width:660px;margin:0 auto;color:var(--muted)}footer{padding:34px 0 46px;text-align:center;color:var(--muted);font-size:.90rem}
    .reveal{opacity:0;transform:translateY(18px);transition:opacity .52s ease,transform .52s ease}.reveal.visible{opacity:1;transform:translateY(0)}
    @keyframes hero-enter{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}@keyframes shimmer{0%{background-position:0% 50%}100%{background-position:180% 50%}}
    @media(max-width:840px){.desktop-links{display:none}.menu-button{display:inline-grid;place-items:center}.grid-2,.grid-3{grid-template-columns:1fr}.hero{min-height:auto;padding:76px 0 64px}.hero-strip{grid-template-columns:1fr;max-width:510px}.role-header{display:block}.period{display:block;margin-top:8px;white-space:normal}}
    @media(max-width:560px){.container{width:min(calc(100% - 24px),var(--max))}.nav{min-height:68px}h1{font-size:clamp(2.65rem,14vw,4.35rem)}.hero-subtitle{font-size:1.02rem}.actions{display:grid}.button{width:100%}.role,.card{padding:20px}.role{padding-left:24px}section{padding:62px 0}.contact{padding:40px 20px}}
    @media(prefers-reduced-motion:reduce){html{scroll-behavior:auto}*,*:before,*:after{animation-duration:.01ms!important;animation-iteration-count:1!important;transition-duration:.01ms!important}}
  </style>
</head>
<body>
  <header class="site-header" id="site-header">
    <div class="container nav">
      <a class="wordmark" href="#top" aria-label="Santhose Kumar S home"><span class="wordmark-mark">SK</span><span>Santhose <b>Kumar S</b></span></a>
      <nav class="desktop-links" aria-label="Primary navigation"><a href="#about">About</a><a href="#expertise">Expertise</a><a href="#experience">Experience</a><a class="nav-cta" href="#contact">Let’s Connect</a></nav>
      <button class="menu-button" id="menu-button" aria-label="Open navigation menu" aria-expanded="false" aria-controls="mobile-menu">☰</button>
    </div>
    <nav class="mobile-menu" id="mobile-menu" aria-label="Mobile navigation"><a href="#about">About</a><a href="#expertise">Expertise</a><a href="#experience">Experience</a><a href="#contact">Let’s Connect</a></nav>
  </header>

  <main id="top" class="container">
    <section class="hero"><div class="hero-inner">
      <span class="eyebrow">12+ years in product & platform engineering</span>
      <h1>Turning complex systems into <span class="gradient-text">secure, scalable products.</span></h1>
      <p class="hero-subtitle">I am <strong>Santhose Kumar S</strong> — a Staff / Lead Software Engineer, Technical Lead, and Engineering Manager building API-led banking and SaaS platforms, enabling teams, and creating reliable customer journeys.</p>
      <div class="actions"><a class="button button-primary" href="mailto:santhosekumar@ymail.com">Email Me</a><a class="button button-secondary" href="https://www.linkedin.com/in/santhose-kumar-s-578515118/" target="_blank" rel="noreferrer">LinkedIn</a><a class="button button-secondary" href="https://github.com/santhosekumar19/" target="_blank" rel="noreferrer">GitHub</a></div>
      <div class="hero-strip"><div class="hero-metric"><b>Retail Banking</b><span>API-led modernization</span></div><div class="hero-metric"><b>Distributed Services</b><span>Kafka, Redis & resilient integration</span></div><div class="hero-metric"><b>Engineering Leadership</b><span>Mentoring, standards & delivery</span></div></div>
    </div></section>

    <section id="about" class="reveal"><div class="section-head"><div class="section-kicker">About</div><h2>Product thinking. Platform depth. Team momentum.</h2><p>I help organizations evolve legacy applications into reliable, API-led services that are easier to build, operate, and scale. My work connects hands-on engineering, technical direction, delivery leadership, and measurable product impact.</p></div>
      <div class="grid grid-3"><article class="card"><div class="card-icon">⚡</div><h3>Product delivery</h3><p>Customer journeys, responsive applications, dashboards, reusable UI, and practical business outcomes.</p></article><article class="card"><div class="card-icon">🔐</div><h3>Platform modernization</h3><p>Secure APIs, BFFs, core-system integration, distributed services, event-driven workflows, and resilience.</p></article><article class="card"><div class="card-icon">🤝</div><h3>Team leadership</h3><p>Mentoring, technical direction, documentation, delivery planning, quality standards, and cross-functional execution.</p></article></div>
    </section>

    <section id="expertise" class="reveal"><div class="section-head"><div class="section-kicker">Core Expertise</div><h2>Technology with purpose.</h2><p>Focused on the stack and practices that make product platforms secure, observable, and easier to evolve.</p></div>
      <div class="grid grid-2"><article class="card skill-card"><h3>Product & full-stack engineering</h3><span class="tag">React</span><span class="tag">Next.js</span><span class="tag">TypeScript</span><span class="tag">Node.js</span><span class="tag">Java</span><span class="tag">Spring Boot</span><span class="tag">REST</span><span class="tag">GraphQL</span><span class="tag">SSR / ISR</span></article><article class="card skill-card"><h3>Integration & distributed services</h3><span class="tag">API Gateway</span><span class="tag">BFF</span><span class="tag">Microservices</span><span class="tag">Apache Kafka</span><span class="tag">Redis</span><span class="tag">3scale</span><span class="tag">Event-driven workflows</span><span class="tag">Finacle integration</span></article><article class="card skill-card"><h3>Cloud, reliability & delivery</h3><span class="tag">AWS</span><span class="tag">OpenShift</span><span class="tag">Kubernetes</span><span class="tag">Docker</span><span class="tag">Jenkins</span><span class="tag">GitHub Actions</span><span class="tag">AppDynamics</span><span class="tag">Elasticsearch / Kibana</span></article><article class="card skill-card"><h3>Leadership & engineering practices</h3><span class="tag">Technical leadership</span><span class="tag">Mentoring</span><span class="tag">Agile delivery</span><span class="tag">API documentation</span><span class="tag">Code reviews</span><span class="tag">Release governance</span><span class="tag">AI-assisted development</span><span class="tag">MCP automation</span></article></div>
    </section>

    <section id="experience" class="reveal"><div class="section-head"><div class="section-kicker">Experience</div><h2>Selected work and impact.</h2><p>Building products that connect customer experience, business workflows, and production reliability.</p></div>
      <div class="experience-list">
        <article class="role"><div class="role-header"><div><h3>Lead Software Engineer</h3><div class="company">Emirates NBD · Retail Banking Platform Modernization</div></div><div class="period">Nov 2025 – Present</div></div><ul><li>Modernizing core-banking integrations into secure, reusable <strong>API-led services</strong> using Node.js, Java/Spring Boot, Rust, Redis, Kafka, OpenShift, and 3scale.</li><li>Reduced a critical request path from <strong>~10 ms to ~2 ms</strong> through streamlined routing, caching, and integration flows.</li><li>Established API contracts and documentation to reduce handoff friction and create clearer delivery ownership across teams.</li><li>Improved production resilience with Kafka consumer-lag monitoring, DLQ workflows, AppDynamics APM, and Elasticsearch/Kibana observability.</li><li>Introduced AI-assisted development and MCP-based automation for Java-to-Node migration analysis and engineering productivity.</li></ul></article>
        <article class="role"><div class="role-header"><div><h3>Staff Software Engineer</h3><div class="company">Okta · Product Experience</div></div><div class="period">Mar 2024 – Oct 2025</div></div><ul><li>Built multilingual, mobile-first documentation and dashboard experiences with React, Next.js, Node.js, GraphQL, Redis, and AWS.</li><li>Improved discoverability and page performance through SSR and ISR, delivering faster and SEO-friendly content experiences.</li><li>Streamlined i18n onboarding and translation workflows for localized product publishing.</li></ul></article>
        <article class="role"><div class="role-header"><div><h3>Software Consultant</h3><div class="company">Randstad · Carbon Credit Exchange Platform</div></div><div class="period">Jun 2022 – May 2023</div></div><ul><li>Replaced manual carbon-credit reporting with automated, role-based dashboards using React, Node.js, GraphQL, MongoDB, and AWS.</li><li>Built exchange APIs and workflow services for trade, validation, and analytics flows.</li><li>Automated secure releases with Docker and GitHub Actions; implemented JWT/RBAC and audit-ready data traceability.</li></ul></article>
        <article class="role"><div class="role-header"><div><h3>Advanced Software Engineer</h3><div class="company">Honeywell · Building Management & Sustainability</div></div><div class="period">Jun 2020 – Mar 2022</div></div><ul><li>Modernized enterprise building-management dashboards with React, TypeScript, and Redux.</li><li>Built reusable design-system components and microfrontend-ready foundations for B2B monitoring and sustainability workflows.</li><li>Improved responsiveness and reliability through better client-side state, rendering, and API-integration patterns.</li></ul></article>
        <article class="role"><div class="role-header"><div><h3>Earlier Experience</h3><div class="company">Altimetrik · IBM / J.P. Morgan Chase · MFX Infotech</div></div><div class="period">2016 – 2020</div></div><ul><li>Built real-time decision analytics platforms using React, Node.js, GraphQL, Docker, and AWS.</li><li>Modernized internal financial tools using React, Angular, RxJS, Redux, and Cloud Foundry.</li><li>Delivered multi-brand B2B, B2C, and B2B2C insurance portals using AngularJS, REST APIs, and PostgreSQL.</li></ul></article>
      </div>
    </section>

    <section id="contact" class="reveal"><div class="contact"><div class="section-kicker">Contact</div><h2>Let’s build something meaningful.</h2><p>Open to Staff Engineer, Lead Software Engineer, Technical Lead, Engineering Manager, and platform engineering opportunities.</p><div class="actions"><a class="button button-primary" href="mailto:santhosekumar@ymail.com">Start a conversation</a><a class="button button-secondary" href="https://www.linkedin.com/in/santhose-kumar-s-578515118/" target="_blank" rel="noreferrer">View LinkedIn</a></div></div></section>
    <footer>© <span id="year"></span> Santhose Kumar S · Built with ownership, curiosity, and engineering discipline.</footer>
  </main>

  <script>
    const header=document.getElementById('site-header');
    const menuButton=document.getElementById('menu-button');
    const mobileMenu=document.getElementById('mobile-menu');
    const setHeaderState=()=>header.classList.toggle('is-scrolled',window.scrollY>12);
    setHeaderState();window.addEventListener('scroll',setHeaderState,{passive:true});
    menuButton.addEventListener('click',()=>{const open=mobileMenu.classList.toggle('open');menuButton.setAttribute('aria-expanded',String(open));menuButton.textContent=open?'✕':'☰';});
    mobileMenu.querySelectorAll('a').forEach(link=>link.addEventListener('click',()=>{mobileMenu.classList.remove('open');menuButton.setAttribute('aria-expanded','false');menuButton.textContent='☰';}));
    document.getElementById('year').textContent=new Date().getFullYear();
    const observer=new IntersectionObserver(entries=>entries.forEach(entry=>{if(entry.isIntersecting){entry.target.classList.add('visible');observer.unobserve(entry.target)}}),{threshold:.12});
    document.querySelectorAll('.reveal').forEach(item=>observer.observe(item));
  </script>
</body>
</html>
