<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Zakaria Zakia | Portfolio</title>
  <meta name="description" content="Zakaria Zakia — AI Engineer, Cybersecurity Researcher, Systems Builder" />
  <style>
    :root {
      --bg: #07111f;
      --bg-2: #0d1b2a;
      --panel: rgba(18, 31, 47, 0.82);
      --panel-strong: rgba(15, 24, 38, 0.95);
      --text: #e5eefb;
      --muted: #9fb2c9;
      --primary: #6ee7f9;
      --secondary: #7c9cff;
      --accent: #7ef7c7;
      --border: rgba(255,255,255,0.08);
      --shadow: rgba(0, 0, 0, 0.35);
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      background:
        radial-gradient(circle at top left, rgba(110, 231, 249, 0.15), transparent 25%),
        radial-gradient(circle at right, rgba(124, 156, 255, 0.12), transparent 30%),
        linear-gradient(180deg, var(--bg) 0%, #030a12 100%);
      color: var(--text);
    }

    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }

    .container {
      width: min(1100px, calc(100% - 32px));
      margin: 0 auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(12px);
      background: rgba(7, 17, 31, 0.75);
      border-bottom: 1px solid var(--border);
    }

    nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 18px 0;
    }

    .brand {
      font-weight: 800;
      font-size: 1.1rem;
      letter-spacing: 0.04em;
    }

    .nav-links {
      display: flex;
      gap: 22px;
      color: var(--muted);
      font-size: 0.96rem;
    }

    .nav-links a:hover { color: var(--text); }

    .btn {
      display: inline-block;
      padding: 12px 18px;
      border-radius: 12px;
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      color: #051018;
      font-weight: 800;
      border: none;
      transition: 0.25s ease;
      box-shadow: 0 10px 25px rgba(110, 231, 249, 0.2);
    }

    .btn:hover {
      transform: translateY(-1px);
      box-shadow: 0 16px 30px rgba(110, 231, 249, 0.26);
    }

    .hero {
      padding: 72px 0 40px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.3fr 0.9fr;
      gap: 40px;
      align-items: center;
    }

    .eyebrow {
      color: var(--primary);
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      font-size: 0.75rem;
      margin-bottom: 16px;
    }

    h1 {
      font-size: clamp(2.8rem, 5vw, 5rem);
      line-height: 1.04;
      margin: 0 0 18px;
      letter-spacing: -0.05em;
    }

    .gradient-text {
      background: linear-gradient(135deg, var(--primary), var(--secondary), var(--accent));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .lead {
      font-size: 1.08rem;
      line-height: 1.8;
      color: var(--muted);
      max-width: 650px;
      margin-bottom: 28px;
    }

    .hero-actions {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      margin-bottom: 30px;
    }

    .btn-secondary {
      border: 1px solid var(--border);
      background: rgba(255,255,255,0.02);
      color: var(--text);
      box-shadow: none;
    }

    .socials {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      color: var(--muted);
      font-size: 0.95rem;
    }

    .socials a {
      padding: 8px 12px;
      border: 1px solid var(--border);
      border-radius: 999px;
      background: rgba(255,255,255,0.02);
    }

    .profile-card {
      background: linear-gradient(180deg, rgba(18, 29, 44, 0.95), rgba(10, 19, 30, 0.95));
      border: 1px solid var(--border);
      border-radius: 28px;
      padding: 24px;
      box-shadow: 0 25px 60px var(--shadow);
    }

    .avatar-shell {
      width: min(320px, 100%);
      aspect-ratio: 1;
      margin: 0 auto 18px;
      border-radius: 50%;
      padding: 12px;
      background: linear-gradient(135deg, var(--primary), var(--secondary), var(--accent));
      box-shadow: 0 18px 38px rgba(110, 231, 249, 0.18);
    }

    .avatar {
      width: 100%;
      height: 100%;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: radial-gradient(circle at 30% 30%, rgba(255,255,255,0.15), transparent 20%),
                  linear-gradient(135deg, #0f172a, #0b101b);
      border: 2px solid rgba(255,255,255,0.08);
      color: var(--text);
      font-size: clamp(1.8rem, 2.5vw, 2.8rem);
      font-weight: 800;
      letter-spacing: 0.08em;
    }

    .mini-info {
      text-align: center;
      margin-top: 10px;
    }

    .mini-info h3 {
      margin: 0;
      font-size: clamp(1.5rem, 2.2vw, 2.2rem);
    }

    .mini-info p {
      margin: 8px 0 0;
      color: var(--muted);
      line-height: 1.7;
    }

    section {
      padding: 34px 0;
    }

    .section-head {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 16px;
      margin-bottom: 26px;
    }

    .section-head h2 {
      margin: 0;
      font-size: clamp(1.7rem, 3vw, 2.6rem);
      letter-spacing: -0.04em;
    }

    .section-head span {
      color: var(--muted);
      font-size: 0.97rem;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 18px;
    }

    .card {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 18px 18px 16px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.1);
    }

    .card h3 {
      margin: 0 0 8px;
      font-size: 1.1rem;
    }

    .card p {
      margin: 0;
      color: var(--muted);
      line-height: 1.7;
    }

    .chip-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 14px;
    }

    .chip {
      background: rgba(110, 231, 249, 0.08);
      border: 1px solid rgba(110, 231, 249, 0.18);
      color: var(--primary);
      border-radius: 999px;
      padding: 7px 12px;
      font-size: 0.82rem;
      font-weight: 700;
    }

    .stack-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 18px;
    }

    .stack-box {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 18px;
    }

    .stack-box h3 {
      margin: 0 0 12px;
      font-size: 1.04rem;
    }

    .stack-box ul {
      margin: 0;
      padding-left: 18px;
      color: var(--muted);
      line-height: 2;
    }

    .projects {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 22px;
    }

    .project {
      background: var(--panel-strong);
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 20px;
      transition: transform 0.2s ease;
    }

    .project:hover { transform: translateY(-2px); }

    .project-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
      margin-bottom: 10px;
    }

    .project h3 {
      margin: 0;
      font-size: 1.18rem;
    }

    .project-tag {
      color: var(--primary);
      background: rgba(110, 231, 249, 0.08);
      border: 1px solid rgba(110, 231, 249, 0.18);
      padding: 6px 8px;
      border-radius: 10px;
      font-size: 0.72rem;
      font-weight: 700;
    }

    .project p {
      color: var(--muted);
      line-height: 1.7;
      margin: 12px 0 18px;
    }

    .project-links {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .project-links a {
      font-size: 0.9rem;
      color: var(--text);
      border: 1px solid var(--border);
      border-radius: 999px;
      padding: 8px 12px;
      background: rgba(255,255,255,0.02);
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 16px;
      margin-top: 8px;
    }

    .stat {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 18px;
    }

    .stat strong {
      display: block;
      font-size: clamp(1.8rem, 3vw, 2.5rem);
      margin-bottom: 6px;
      letter-spacing: -0.04em;
    }

    .stat span {
      color: var(--muted);
    }

    footer {
      padding: 28px 0 60px;
      color: var(--muted);
      text-align: center;
      border-top: 1px solid var(--border);
      margin-top: 32px;
    }

    @media (max-width: 840px) {
      .hero-grid,
      .cards,
      .stack-grid,
      .projects,
      .stats {
        grid-template-columns: 1fr;
      }

      .nav-links {
        display: none;
      }

      .section-head {
        display: block;
      }
      .section-head span {
        display: block;
        margin-top: 8px;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav>
        <div class="brand">Zakaria Zakia</div>
        <div class="nav-links">
          <a href="#about">About</a>
          <a href="#projects">Projects</a>
          <a href="#stack">Stack</a>
          <a href="#contact">Contact</a>
        </div>
        <a class="btn" href="#contact">Hire Me</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero" id="about">
      <div class="hero-grid">
        <div>
          <div class="eyebrow">AI Engineer • Cybersecurity • Systems</div>
          <h1>
            Building <span class="gradient-text">secure</span>, intelligent, and scalable systems.
          </h1>
          <p class="lead">
            I’m Zakaria Zakia, a software engineer and security-focused developer passionate about AI,
            cybersecurity, distributed systems, and low-level engineering. I enjoy turning complex
            ideas into practical systems and security tools that solve real-world problems.
          </p>

          <div class="hero-actions">
            <a class="btn" href="#projects">View Projects</a>
            <a class="btn btn-secondary" href="https://github.com/zakariazakia15-jpg" target="_blank" rel="noreferrer">GitHub</a>
          </div>

          <div class="socials">
            <a href="https://github.com/zakariazakia15-jpg" target="_blank" rel="noreferrer">GitHub</a>
            <a href="https://github.com/zakariazakia15-jpg/-Portfolio-" target="_blank" rel="noreferrer">Portfolio</a>
            <a href="mailto:zakariazakia15@gmail.com">Email</a>
          </div>
        </div>

        <div class="profile-card">
          <div class="avatar-shell">
            <div class="avatar">ZZ</div>
          </div>
          <div class="mini-info">
            <h3>Zakaria Zakia</h3>
            <p>
              AI Engineer • Cybersecurity Researcher • Systems Builder
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="stats">
      <div class="stats">
        <div class="stat">
          <strong>8+</strong>
          <span>Projects</span>
        </div>
        <div class="stat">
          <strong>3</strong>
          <span>Core Domains</span>
        </div>
        <div class="stat">
          <strong>∞</strong>
          <span>Ideas</span>
        </div>
        <div class="stat">
          <strong>24/7</strong>
          <span>Learning</span>
        </div>
      </div>
    </section>

    <section id="projects">
      <div class="section-head">
        <h2>Featured Projects</h2>
        <span>Research-driven engineering and security-focused builds</span>
      </div>

      <div class="projects">
        <article class="project">
          <div class="project-header">
            <h3>EagleEye</h3>
            <span class="project-tag">Public</span>
          </div>
          <p>
            Advanced supply chain security scanner for GitHub and npm ecosystems, designed to
            detect and analyze vulnerable patterns across dependency chains.
          </p>
          <div class="project-links">
            <a href="https://github.com/zakariazakia15-jpg/EagleEye" target="_blank" rel="noreferrer">Repo</a>
          </div>
        </article>

        <article class="project">
          <div class="project-header">
            <h3>GhostShield</h3>
            <span class="project-tag">AI + Security</span>
          </div>
          <p>
            AI-powered Linux kernel firewall that detects and blocks zero-day threats in real time
            using intelligent monitoring and adaptive behavior.
          </p>
          <div class="project-links">
            <a href="https://github.com/zakariazakia15-jpg/GhostShield-" target="_blank" rel="noreferrer">Repo</a>
          </div>
        </article>

        <article class="project">
          <div class="project-header">
            <h3>LexiCode-Audit</h3>
            <span class="project-tag">Compliance</span>
          </div>
          <p>
            AI-driven security auditing tool that maps vulnerabilities to privacy and compliance
            standards such as GDPR and CCPA.
          </p>
          <div class="project-links">
            <a href="https://github.com/zakariazakia15-jpg/LexiCode-Audit" target="_blank" rel="noreferrer">Repo</a>
          </div>
        </article>

        <article class="project">
          <div class="project-header">
            <h3>NexusDB</h3>
            <span class="project-tag">Systems</span>
          </div>
          <p>
            Distributed SQL engine project focused on ACID, Raft, and LSM-based design with
            scalable persistence and concurrency.
          </p>
          <div class="project-links">
            <a href="https://github.com/zakariazakia15-jpg/NexusDB" target="_blank" rel="noreferrer">Repo</a>
          </div>
        </article>

        <article class="project">
          <div class="project-header">
            <h3>NovaOS</h3>
            <span class="project-tag">Operating System</span>
          </div>
          <p>
            A complete operating system project built from the ground up, focused on system
            architecture and kernel-level experimentation.
          </p>
          <div class="project-links">
            <a href="https://github.com/zakariazakia15-jpg/NovaOS" target="_blank" rel="noreferrer">Repo</a>
          </div>
        </article>

        <article class="project">
          <div class="project-header">
            <h3>OpenClaw</h3>
            <span class="project-tag">AI Agent</span>
          </div>
          <p>
            Autonomous AI web agent and vulnerability hunter built for intelligent security
            exploration and automated discovery workflows.
          </p>
          <div class="project-links">
            <a href="https://github.com/zakariazakia15-jpg/OpenClaw" target="_blank" rel="noreferrer">Repo</a>
          </div>
        </article>
      </div>
    </section>

    <section id="stack">
      <div class="section-head">
        <h2>Tech Stack</h2>
        <span>Tools, languages, and foundations I build with</span>
      </div>

      <div class="stack-grid">
        <div class="stack-box">
          <h3>Languages</h3>
          <ul>
            <li>Python</li>
            <li>JavaScript</li>
            <li>TypeScript</li>
            <li>Rust</li>
            <li>C / C++</li>
            <li>Bash</li>
          </ul>
        </div>

        <div class="stack-box">
          <h3>AI / Security</h3>
          <ul>
            <li>LLMs</li>
            <li>Threat Modeling</li>
            <li>Vulnerability Analysis</li>
            <li>Security Automation</li>
            <li>Compliance Mapping</li>
            <li>Monitoring Tools</li>
          </ul>
        </div>

        <div class="stack-box">
          <h3>Systems</h3>
          <ul>
            <li>Linux</li>
            <li>Distributed Systems</li>
            <li>Database Internals</li>
            <li>Kernel Exploration</li>
            <li>Architecture Design</li>
            <li>Scalable Engineering</li>
          </ul>
        </div>
      </div>
    </section>

    <section>
      <div class="section-head">
        <h2>What I Focus On</h2>
      </div>

      <div class="cards">
        <div class="card">
          <h3>Cybersecurity</h3>
          <p>
            Building security-first systems for detection, auditing, compliance, and resilient defense.
          </p>
          <div class="chip-row">
            <span class="chip">Threat Detection</span>
            <span class="chip">Scanning</span>
            <span class="chip">Audit Tools</span>
          </div>
        </div>

        <div class="card">
          <h3>AI & Automation</h3>
          <p>
            Exploring how intelligent systems can increase productivity, automate discovery,
            and support decision-making.
          </p>
          <div class="chip-row">
            <span class="chip">LLMs</span>
            <span class="chip">Automation</span>
            <span class="chip">Agents</span>
          </div>
        </div>

        <div class="card">
          <h3>Distributed Systems</h3>
          <p>
            Designing systems that are scalable, reliable, and resilient under concurrency and load.
          </p>
          <div class="chip-row">
            <span class="chip">ACID</span>
            <span class="chip">Raft</span>
            <span class="chip">Storage</span>
          </div>
        </div>

        <div class="card">
          <h3>Low-Level Engineering</h3>
          <p>
            Investigating system internals, performance, architecture, and the foundations that
            power modern software.
          </p>
          <div class="chip-row">
            <span class="chip">Kernel</span>
            <span class="chip">OS</span>
            <span class="chip">Architecture</span>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer id="contact">
    <div class="container">
      <p>© 2026 Zakaria Zakia — Building secure, intelligent, and scalable systems.</p>
    </div>
  </footer>
</body>
</html>
