<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>John Sullivan | AI & Agentic Systems</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="John Sullivan - AI/ML engineer and agentic systems architect portfolio" />
  <style>
    :root {
      --bg: #05070c;
      --bg-alt: #0c101a;
      --accent: #39d98a;
      --accent-soft: rgba(57, 217, 138, 0.12);
      --text: #f5f7ff;
      --muted: #a5b0d0;
      --border: #20263a;
      --card-radius: 14px;
      --shadow-soft: 0 18px 45px rgba(0,0,0,0.45);
      --font-sans: system-ui,-apple-system,BlinkMacSystemFont,"SF Pro Text","Segoe UI",sans-serif;
      --font-mono: "SF Mono","JetBrains Mono",Menlo,Consolas,monospace;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: var(--font-sans);
      background: radial-gradient(circle at top left,#10152b,#05070c 52%);
      color: var(--text);
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }

    a {
      color: var(--accent);
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }

    .page {
      max-width: 1100px;
      margin: 0 auto;
      padding: 32px 18px 80px;
    }

    header {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 24px;
      margin-bottom: 40px;
    }

    .avatar {
      width: 120px;
      height: 120px;
      border-radius: 32px;
      overflow: hidden;
      border: 2px solid var(--border);
      box-shadow: var(--shadow-soft);
      flex-shrink: 0;
    }
    .avatar img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .hero-main {
      flex: 1 1 260px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 3px 9px;
      border-radius: 99px;
      border: 1px solid var(--border);
      background: rgba(8,13,30,0.9);
      font-size: 12px;
      color: var(--muted);
      margin-bottom: 10px;
    }
    .eyebrow span.dot {
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: var(--accent);
      box-shadow: 0 0 14px rgba(57,217,138,0.8);
    }

    h1 {
      font-size: clamp(30px, 4.2vw, 40px);
      letter-spacing: -0.03em;
      margin-bottom: 10px;
    }

    .hero-subtitle {
      color: var(--muted);
      max-width: 540px;
      font-size: 14px;
    }

    .hero-meta {
      margin-top: 14px;
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      font-size: 13px;
      color: var(--muted);
    }

    .hero-meta span {
      padding: 4px 10px;
      border-radius: 999px;
      background: rgba(13,18,38,0.95);
      border: 1px solid var(--border);
    }

    nav {
      margin: 24px 0 32px;
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    nav a {
      font-size: 13px;
      padding: 8px 14px;
      border-radius: 999px;
      border: 1px solid var(--border);
      background: rgba(12,17,34,0.92);
    }

    nav a.primary-cta {
      background: linear-gradient(135deg,#39d98a,#52e3c2);
      border: none;
      color: #020308;
      font-weight: 500;
      box-shadow: 0 10px 25px rgba(0,0,0,0.6);
    }
    nav a.primary-cta:hover {
      text-decoration: none;
      transform: translateY(-1px);
    }

    main {
      display: grid;
      grid-template-columns: minmax(0, 3.2fr) minmax(0, 1.6fr);
      gap: 22px;
    }

    @media (max-width: 850px) {
      main {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    section {
      margin-bottom: 26px;
    }

    .section-card {
      background: radial-gradient(circle at top left,#121931,#050812 55%);
      border-radius: var(--card-radius);
      border: 1px solid var(--border);
      box-shadow: var(--shadow-soft);
      padding: 18px 16px 16px;
      position: relative;
      overflow: hidden;
    }

    .section-card::before {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at top right, rgba(57,217,138,0.12), transparent 55%);
      opacity: 0.9;
      pointer-events: none;
      mix-blend-mode: screen;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      margin-bottom: 10px;
      position: relative;
      z-index: 1;
    }

    .section-title {
      font-size: 16px;
      letter-spacing: 0.09em;
      text-transform: uppercase;
      color: var(--muted);
    }

    .section-kicker {
      font-size: 11px;
      color: var(--muted);
    }

    .pill {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 4px 8px;
      border-radius: 999px;
      background: rgba(3, 163, 97, 0.12);
      color: #8af0c9;
      font-size: 11px;
      border: 1px solid rgba(57,217,138,0.35);
    }

    .pill span.dot {
      width: 6px;
      height: 6px;
      border-radius: 99px;
      background: #39d98a;
    }

    .body-text {
      font-size: 14px;
      color: var(--muted);
      position: relative;
      z-index: 1;
    }

    .stack {
      margin-top: 10px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      position: relative;
      z-index: 1;
    }

    .item {
      padding: 10px 10px 9px;
      border-radius: 11px;
      background: rgba(13, 18, 40, 0.95);
      border: 1px solid rgba(32,38,58,0.95);
      display: grid;
      grid-template-columns: minmax(0, 3fr) minmax(0, 2fr);
      gap: 9px;
    }

    @media (max-width: 650px) {
      .item {
        grid-template-columns: minmax(0,1fr);
      }
    }

    .item-main h3 {
      font-size: 14px;
      margin-bottom: 3px;
    }

    .item-main p {
      font-size: 13px;
      color: var(--muted);
    }

    .item-meta {
      font-size: 11px;
      color: var(--muted);
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      justify-content: flex-end;
      align-content: flex-start;
    }

    .tag {
      padding: 2px 7px 3px;
      border-radius: 999px;
      border: 1px solid #283248;
      background: rgba(9, 14, 32, 0.9);
    }

    .chip-row {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 7px;
    }

    .chip {
      border-radius: 999px;
      border: 1px solid #202742;
      padding: 3px 8px 4px;
      font-size: 11px;
      color: var(--muted);
      background: rgba(6, 10, 27, 0.9);
    }

    .apps-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 10px;
      margin-top: 10px;
      position: relative;
      z-index: 1;
    }

    .app-card {
      padding: 10px 10px 9px;
      border-radius: 11px;
      border: 1px solid #252e49;
      background: rgba(10, 14, 30, 0.95);
      display: flex;
      flex-direction: column;
      gap: 6px;
    }

    .app-title-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 4px;
    }

    .app-title-row h3 {
      font-size: 13px;
    }

    .app-status {
      font-size: 11px;
      color: #8af0c9;
      display: inline-flex;
      align-items: center;
      gap: 5px;
    }

    .app-status span {
      width: 6px;
      height: 6px;
      border-radius: 99px;
      background: #39d98a;
    }

    .app-summary {
      font-size: 12px;
      color: var(--muted);
    }

    .app-links {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      font-size: 11px;
      margin-top: 4px;
    }

    .app-links a {
      padding: 4px 8px;
      border-radius: 999px;
      border: 1px solid #283248;
      background: rgba(7, 12, 26, 0.9);
    }

    .thought-post {
      padding: 9px 10px 9px;
      border-radius: 11px;
      border: 1px solid #252e49;
      background: rgba(10, 14, 30, 0.95);
      font-size: 13px;
    }

    .thought-post h3 {
      font-size: 13px;
      margin-bottom: 4px;
    }

    .thought-meta {
      font-size: 11px;
      color: var(--muted);
      margin-bottom: 5px;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 8px;
      position: relative;
      z-index: 1;
    }

    label {
      font-size: 12px;
      color: var(--muted);
    }

    input, textarea {
      background: rgba(7, 11, 26, 0.98);
      border-radius: 9px;
      border: 1px solid #202742;
      padding: 7px 9px;
      color: var(--text);
      font: inherit;
      font-size: 13px;
      resize: vertical;
      min-height: 34px;
    }

    textarea {
      min-height: 80px;
    }

    button {
      margin-top: 4px;
      border-radius: 999px;
      border: none;
      padding: 7px 14px;
      font-size: 13px;
      font-weight: 500;
      background: linear-gradient(135deg,#39d98a,#52e3c2);
      color: #020308;
      cursor: pointer;
      align-self: flex-start;
    }

    button:hover {
      filter: brightness(1.05);
      transform: translateY(-0.5px);
    }

    footer {
      margin-top: 40px;
      text-align: center;
      font-size: 11px;
      color: var(--muted);
    }

    footer a {
      color: var(--muted);
      text-decoration: underline;
      text-decoration-style: dotted;
    }
  </style>

  <!-- EmailJS (optional) – uncomment and configure if you use EmailJS -->
  <!--
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
  <script type="text/javascript">
    (function() {
      emailjs.init({ publicKey: "YOUR_PUBLIC_KEY" });
    })();
    window.addEventListener("DOMContentLoaded", function () {
      const form = document.getElementById("contact-form");
      form.addEventListener("submit", function (e) {
        e.preventDefault();
        emailjs.sendForm("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", this)
          .then(() => {
            alert("Thanks, your message is on its way.");
            form.reset();
          }, (error) => {
            alert("Something went wrong – please try again.");
            console.log(error);
          });
      });
    });
  </script>
  -->
</head>
<body>
  <div class="page">
    <header id="top">
      <div class="avatar">
        <!-- Replace with your actual file name -->
        <img src="headshot.jpg" alt="John Sullivan headshot" />
      </div>
      <div class="hero-main">
        <div class="eyebrow">
          <span class="dot"></span>
          <span>Agentic AI & Applied ML</span>
        </div>
        <h1>John Sullivan</h1>
        <p class="hero-subtitle">
          AI/ML engineer and **agentic** systems architect helping mission-driven organizations ship production-grade AI products that bridge infrastructure, data, and real-world decision-making.
        </p>
        <div class="hero-meta">
          <span>Bethesda, MD · Open to AI & data roles</span>
          <span>Top Secret cleared</span>
          <span>10+ years building with Databricks</span>
        </div>
      </div>
    </header>

    <nav>
      <a href="#about">About</a>
      <a href="#apps">Agentic Apps</a>
      <a href="#use-cases">AI Use Cases</a>
      <a href="#posts">Thought Leadership</a>
      <a href="#contact" class="primary-cta">Contact</a>
      <a href="https://www.linkedin.com/in/jvsullivan" target="_blank" rel="noopener">LinkedIn</a>
      <a href="mailto:jvsullivan@gmail.com">Email</a>
    </nav>

    <main>
      <!-- Left column: About + Apps + Thought Leadership -->
      <div>
        <!-- About / Resume -->
        <section id="about" class="section-card">
          <div class="section-header">
            <div>
              <div class="section-title">Profile</div>
              <div class="section-kicker">AI/ML, data platforms, and agentic systems</div>
            </div>
            <div class="pill">
              <span class="dot"></span>
              <span>Hands-on builder & strategist</span>
            </div>
          </div>
          <div class="body-text">
            <p>
              I design and deliver AI platforms and agentic applications that make advanced analytics feel like a native capability, not a bolt-on experiment.
              My work spans end-to-end architecture, data engineering, model integration, and operational deployment in security and mission-driven environments.
            </p>
            <p style="margin-top: 6px;">
              Recent focus areas include: multi-agent workflows, retrieval-augmented generation on sensitive data, and operational guardrails that let teams safely ship AI faster.
            </p>

            <div class="stack" style="margin-top: 12px;">
              <div class="item">
                <div class="item-main">
                  <h3>Experience snapshot</h3>
                  <p>
                    10+ years helping enterprises and government organizations modernize analytics with Databricks, cloud-native data platforms, and applied machine learning.
                    Trusted partner for cross-functional teams spanning engineering, product, and operations.
                  </p>
                  <div class="chip-row">
                    <span class="chip">Databricks</span>
                    <span class="chip">Azure & AWS</span>
                    <span class="chip">LLM & RAG</span>
                    <span class="chip">Streaming data</span>
                    <span class="chip">Security & compliance</span>
                  </div>
                </div>
                <div class="item-meta">
                  <span class="tag">Top Secret clearance</span>
                  <span class="tag">No sponsorship required</span>
                  <span class="tag">US-based (DMV)</span>
                </div>
              </div>

              <div class="item">
                <div class="item-main">
                  <h3>Core skill set</h3>
                  <p>
                    Agentic AI design, modern data engineering, ML workflow orchestration, LLM integration, security-aware architecture, and executive-facing storytelling that connects technical decisions to mission outcomes.
                  </p>
                  <div class="chip-row">
                    <span class="chip">Python</span>
                    <span class="chip">Spark & Databricks</span>
                    <span class="chip">Vector search</span>
                    <span class="chip">MLflow & MLOps</span>
                    <span class="chip">Prompt & system design</span>
                  </div>
                </div>
                <div class="item-meta">
                  <span class="tag">Strategy → Architecture → Delivery</span>
                </div>
              </div>
            </div>
          </div>
        </section>

        <!-- Agentic Apps Portfolio -->
        <section id="apps" class="section-card">
          <div class="section-header">
            <div>
              <div class="section-title">Agentic app portfolio</div>
              <div class="section-kicker">Hands-on builds with summary views & live demos</div>
            </div>
            <div class="pill">
              <span class="dot"></span>
              <span>Multi-agent systems in the wild</span>
            </div>
          </div>

          <div class="body-text">
            <p>
              These projects explore how agentic patterns can be safely wired into real workflows: each app has a clear objective, bounded autonomy, and a human-centric review loop.
            </p>
          </div>

          <div class="apps-grid">
            <!-- App 1 -->
            <article class="app-card">
              <div class="app-title-row">
                <h3>Homeland Intelligence Assistant</h3>
                <div class="app-status">
                  <span></span>
                  <span>Prototype</span>
                </div>
              </div>
              <p class="app-summary">
                Multi-agent copilot that helps analysts triage open-source and internal feeds, summarize events, and assemble investigative briefs with clear provenance and confidence scoring.
              </p>
              <div class="chip-row">
                <span class="chip">Agent orchestration</span>
                <span class="chip">RAG on secure data</span>
                <span class="chip">Source attribution</span>
              </div>
              <div class="app-links">
                <!-- Replace with your real URLs or app hosts -->
                <a href="https://example.com/homeland-intel-demo" target="_blank" rel="noopener">Live demo</a>
                <a href="https://example.com/homeland-intel-notes" target="_blank" rel="noopener">Design notes</a>
                <a href="#use-cases-homeland">Use case overview</a>
              </div>
            </article>

            <!-- App 2 -->
            <article class="app-card">
              <div class="app-title-row">
                <h3>Unified Casework Agent Hub</h3>
                <div class="app-status">
                  <span></span>
                  <span>In progress</span>
                </div>
              </div>
              <p class="app-summary">
                A unified “agent dock” for caseworkers that routes tasks to specialized agents for intake summarization, document extraction, and next-step planning while maintaining strict policy guardrails.
              </p>
              <div class="chip-row">
                <span class="chip">Workflow routing</span>
                <span class="chip">Document AI</span>
                <span class="chip">Copilot UX</span>
              </div>
              <div class="app-links">
                <a href="https://example.com/case-agent-hub-demo" target="_blank" rel="noopener">Live demo</a>
                <a href="https://example.com/case-agent-architecture" target="_blank" rel="noopener">Architecture</a>
                <a href="#use-cases-casework">Use case overview</a>
              </div>
            </article>

            <!-- App 3 -->
            <article class="app-card">
              <div class="app-title-row">
                <h3>Databricks Ops Auto-Runbook</h3>
                <div class="app-status">
                  <span></span>
                  <span>Deployed</span>
                </div>
              </div>
              <p class="app-summary">
                Agent that watches platform telemetry, interprets alerts, and drafts remediation steps or runbook PRs, closing the loop between monitoring data and concrete engineering actions.
              </p>
              <div class="chip-row">
                <span class="chip">LLM + observability</span>
                <span class="chip">Ops automation</span>
                <span class="chip">Guardrailed actions</span>
              </div>
              <div class="app-links">
                <a href="https://example.com/dbx-runbook-demo" target="_blank" rel="noopener">Live demo</a>
                <a href="https://example.com/dbx-runbook-github" target="_blank" rel="noopener">Code / repo</a>
                <a href="#use-cases-ops">Use case overview</a>
              </div>
            </article>

            <!-- App 4 -->
            <article class="app-card">
              <div class="app-title-row">
                <h3>Mission Briefing Narrative Builder</h3>
                <div class="app-status">
                  <span></span>
                  <span>Prototype</span>
                </div>
              </div>
              <p class="app-summary">
                Narrative-generation agent that converts complex data outputs into executive-ready mission briefings, with inline caveats, scenario comparisons, and links back to the underlying analyses.
              </p>
              <div class="chip-row">
                <span class="chip">Narrative analytics</span>
                <span class="chip">Exec-ready views</span>
                <span class="chip">Traceable insights</span>
              </div>
              <div class="app-links">
                <a href="https://example.com/mission-brief-demo" target="_blank" rel="noopener">Live demo</a>
                <a href="https://example.com/mission-brief-system-design" target="_blank" rel="noopener">System design</a>
                <a href="#use-cases-briefings">Use case overview</a>
              </div>
            </article>
          </div>
        </section>

        <!-- Thought leadership -->
        <section id="posts" class="section-card">
          <div class="section-header">
            <div>
              <div class="section-title">Thought leadership</div>
              <div class="section-kicker">Writing at the intersection of AI, mission, and infrastructure</div>
            </div>
            <div class="pill">
              <span class="dot"></span>
              <span>Drafts ready for LinkedIn</span>
            </div>
          </div>

          <div class="stack">
            <article class="thought-post">
              <h3>Agentic AI is a workflow problem, not a model problem</h3>
              <div class="thought-meta">Post draft · ~3–5 min read</div>
              <p>
                Everyone wants “agents,” but most teams still treat them like smarter chatbots. The real unlock comes when you treat agents as opinionated workflow participants, not text-generating oracles.
                When an agent owns a specific objective, a bounded action space, and a clear contract with the rest of the system, it stops being a toy and starts being infrastructure.
              </p>
              <p style="margin-top: 6px;">
                The pattern I see work best in the field is simple: one agent that understands intent, a small group of specialists that act on behalf of real roles in the organization,
                and a thin control plane that logs, constrains, and explains every decision. It’s less glamorous than the “autonomous AI” pitch, but it’s what actually ships.
              </p>
            </article>

            <article class="thought-post">
              <h3>From dashboards to decisions: why we built agents on top of analytics</h3>
              <div class="thought-meta">Post draft · ~3–5 min read</div>
              <p>
                For a decade, organizations have been told that “data-driven” means building more dashboards. The result is familiar:
                plenty of charts, but the same meetings, the same gut-driven calls, and the same operational bottlenecks.
              </p>
              <p style="margin-top: 6px;">
                Agentic systems offer a different pattern: instead of asking people to pull insights from dashboards,
                we push decisions toward them with context, options, and trade-offs already mapped out.
                In practice, that means connecting LLMs to the data platform, encoding playbooks as code, and designing UX so the right person can say “yes/no/adjust” in a few seconds—not a few hours.
              </p>
            </article>

            <article class="thought-post">
              <h3>Guardrails are a feature, not a tax</h3>
              <div class="thought-meta">Post draft · ~2–3 min read</div>
              <p>
                In regulated or sensitive domains, the fastest way to stall an AI program is to treat governance as a separate track that “we’ll handle later.”
                The teams that move quickly are the ones that build controls into the first prototype.
              </p>
              <p style="margin-top: 6px;">
                Logging every action, enforcing explicit allow-lists, and exposing model confidence to the user are not nice-to-haves;
                they are the reason security, legal, and mission owners feel comfortable saying “turn it on.”
                When guardrails ship with version one, the conversation shifts from “should we?” to “where else could we safely apply this?”.
              </p>
            </article>

            <article class="thought-post">
              <h3>What “production” means for AI agents</h3>
              <div class="thought-meta">Post draft · ~2–3 min read</div>
              <p>
                In classic software, “production” is a deployment stage.
                For AI agents, production is a relationship: between the agent, the data it sees, the humans it collaborates with, and the controls that keep it inside the lines.
              </p>
              <p style="margin-top: 6px;">
                I look for three signals before I call an agent production-ready:
                it has a clear owner, it has telemetry that explains what it’s doing in business language, and the people it serves would miss it if it disappeared.
                Anything less is still a lab experiment with a nice UI.
              </p>
            </article>
          </div>
        </section>
      </div>

      <!-- Right column: Use cases + Contact -->
      <div>
        <!-- AI Use Cases -->
        <section id="use-cases" class="section-card">
          <div class="section-header">
            <div>
              <div class="section-title">Agentic AI use cases</div>
              <div class="section-kicker">Where these apps fit in the real world</div>
            </div>
            <div class="pill">
              <span class="dot"></span>
              <span>From ideas to deployable patterns</span>
            </div>
          </div>

          <div class="stack">
            <div class="item" id="use-cases-homeland">
              <div class="item-main">
                <h3>Homeland Intelligence Assistant</h3>
                <p>
                  Agents coordinate to monitor open-source feeds, internal reports, and sensor data, then surface anomalies, context, and draft briefs for analyst review,
                  keeping humans firmly in the loop for judgment calls.
                </p>
              </div>
              <div class="item-meta">
                <span class="tag">Mission: intelligence triage</span>
                <span class="tag">Outcome: faster, better briefs</span>
              </div>
            </div>

            <div class="item" id="use-cases-casework">
              <div class="item-main">
                <h3>Unified Casework Agent Hub</h3>
                <p>
                  Caseworkers get a single workspace where specialized agents summarize new intakes, extract structured fields from documents, and propose next actions that align with policy and eligibility rules.
                </p>
              </div>
              <div class="item-meta">
                <span class="tag">Mission: service delivery</span>
                <span class="tag">Outcome: less swivel-chair work</span>
              </div>
            </div>

            <div class="item" id="use-cases-ops">
              <div class="item-main">
                <h3>Databricks Ops Auto-Runbook</h3>
                <p>
                  An observability-aware agent interprets platform alerts, clusters related incidents, and drafts remediation steps or PRs.
                  Engineers retain approval authority, but time-to-understanding drops dramatically.
                </p>
              </div>
              <div class="item-meta">
                <span class="tag">Mission: platform reliability</span>
                <span class="tag">Outcome: fewer 2am pages</span>
              </div>
            </div>

            <div class="item" id="use-cases-briefings">
              <div class="item-main">
                <h3>Mission Briefing Narrative Builder</h3>
                <p>
                  Instead of manually stitching together slides, leaders receive a narrative that connects metrics, risks, and recommendations—backed by links to the exact queries, notebooks, and models used.
                </p>
              </div>
              <div class="item-meta">
                <span class="tag">Mission: decision support</span>
                <span class="tag">Outcome: fewer meetings, clearer calls</span>
              </div>
            </div>
          </div>
        </section>

        <!-- Contact -->
        <section id="contact" class="section-card">
          <div class="section-header">
            <div>
              <div class="section-title">Contact</div>
              <div class="section-kicker">Let’s talk about agentic AI, data platforms, or your next build</div>
            </div>
          </div>

          <div class="body-text" style="margin-bottom: 8px;">
            <p>
              The fastest way to reach me is email or LinkedIn.
              For convenience, you can also drop a note here and it will route directly to my inbox.
            </p>
          </div>

          <!-- Option A: Simple mailto fallback -->
          <p class="body-text" style="font-size: 12px; margin-bottom: 8px;">
            Prefer your own mail client?
            <a href="mailto:jvsullivan@gmail.com">Send me an email</a> or connect on
            <a href="https://www.linkedin.com/in/jvsullivan" target="_blank" rel="noopener">LinkedIn</a>.
          </p>

          <!-- Option B: EmailJS/Web3Forms-powered form -->
          <!-- If using Web3Forms instead of EmailJS, replace the form tag as per docs:
               action="https://api.web3forms.com/submit"
               method="POST"
               and include your access_key field. [web:12] -->
          <form id="contact-form">
            <label for="name">Name</label>
            <input id="name" name="name" type="text" required />

            <label for="email">Email</label>
            <input id="email" name="email" type="email" required />

            <label for="message">Message</label>
            <textarea id="message" name="message" required></textarea>

            <button type="submit">Send message</button>
          </form>

          <p class="body-text" style="font-size: 11px; margin-top: 8px;">
            Note: This form requires configuration with a no-backend email service (EmailJS or Web3Forms) to deliver messages to <strong>jvsullivan@gmail.com</strong>.
          </p>
        </section>
      </div>
    </main>

    <footer>
      <p>
        &copy; <span id="year"></span> John Sullivan ·
        <a href="https://www.linkedin.com/in/jvsullivan" target="_blank" rel="noopener">LinkedIn</a> ·
        <a href="mailto:jvsullivan@gmail.com">Email</a>
      </p>
    </footer>
  </div>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
