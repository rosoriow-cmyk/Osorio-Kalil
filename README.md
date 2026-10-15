<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Osorio Kalil Energy Advisors | Independent Owner's Engineering</title>

  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fontsource/inter@5.0.0/index.min.css">

  <style>
    :root {
      --navy-deep: #07101f;
      --navy: #0a1628;
      --navy-mid: #0f1f3d;
      --navy-light: #162a52;
      --gold: #c9a84c;
      --gold-light: #e8c96a;
      --gold-dim: rgba(201, 168, 76, 0.2);
      --white: #ffffff;
      --muted: #8a9bb5;
      --border: rgba(201, 168, 76, 0.25);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: var(--navy-deep);
      color: var(--white);
      overflow-x: hidden;
      line-height: 1.6;
    }

    .gold {
      color: var(--gold);
    }

    /* Header */
    .site-header {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      background: rgba(7, 16, 31, 0.88);
      backdrop-filter: blur(20px);
      border-bottom: 1px solid var(--border);
      padding: 18px 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: all 0.3s ease;
    }

    .logo-area {
      display: flex;
      flex-direction: column;
    }

    .logo-text {
      font-size: 18px;
      font-weight: 800;
      letter-spacing: 1px;
      color: var(--white);
    }

    .logo-tagline {
      font-size: 11px;
      color: var(--muted);
      letter-spacing: 2px;
      text-transform: uppercase;
      margin-top: 2px;
    }

    .header-cta {
      background: var(--gold);
      color: var(--navy-deep);
      padding: 12px 24px;
      border-radius: 6px;
      font-size: 13px;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1px;
      cursor: pointer;
      border: none;
      transition: all 0.3s ease;
      font-family: inherit;
    }

    .header-cta:hover {
      background: var(--gold-light);
      transform: translateY(-2px);
    }

    /* Hero */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      padding: 120px 60px 80px;
      position: relative;
      overflow: hidden;
    }

    .hero-bg {
      position: absolute;
      inset: 0;
      background:
        radial-gradient(circle at 20% 20%, rgba(201, 168, 76, 0.12), transparent 35%),
        radial-gradient(circle at 80% 70%, rgba(22, 42, 82, 0.7), transparent 40%),
        #07101f;
      opacity: 1;
    }

    .hero-bg::after {
      content: '';
      position: absolute;
      inset: 0;
      background: linear-gradient(135deg, rgba(7, 16, 31, 0.9), rgba(10, 22, 40, 0.72));
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 820px;
    }

    .hero-label {
      font-size: 13px;
      color: var(--gold);
      letter-spacing: 3px;
      text-transform: uppercase;
      font-weight: 600;
      margin-bottom: 20px;
      display: inline-flex;
      align-items: center;
      gap: 12px;
    }

    .hero-label::before {
      content: '';
      width: 40px;
      height: 2px;
      background: var(--gold);
    }

    .hero-title {
      font-size: clamp(40px, 6vw, 72px);
      font-weight: 800;
      line-height: 1.05;
      margin-bottom: 24px;
      letter-spacing: -2px;
    }

    .hero-subtitle {
      font-size: clamp(18px, 2vw, 22px);
      color: var(--muted);
      margin-bottom: 32px;
      line-height: 1.5;
      max-width: 640px;
    }

    .motto {
      font-size: 14px;
      color: var(--gold-light);
      letter-spacing: 2px;
      text-transform: uppercase;
      font-weight: 600;
      margin-bottom: 40px;
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .motto::before {
      content: '';
      width: 30px;
      height: 2px;
      background: var(--gold);
    }

    .hero-cta-group {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .cta-button {
      display: inline-block;
      background: var(--gold);
      color: var(--navy-deep);
      padding: 18px 40px;
      border-radius: 8px;
      font-size: 16px;
      font-weight: 700;
      text-decoration: none;
      text-transform: uppercase;
      letter-spacing: 1px;
      cursor: pointer;
      border: none;
      transition: all 0.3s ease;
      font-family: inherit;
    }

    .cta-button:hover {
      background: var(--gold-light);
      transform: translateY(-2px);
      box-shadow: 0 12px 32px rgba(201, 168, 76, 0.3);
    }

    .cta-button.outline {
      background: transparent;
      color: var(--gold);
      border: 2px solid var(--gold);
    }

    .cta-button.outline:hover {
      background: var(--gold);
      color: var(--navy-deep);
    }

    /* Sections */
    .section {
      padding: 100px 60px;
      position: relative;
    }

    .section-label {
      font-size: 12px;
      color: var(--gold);
      letter-spacing: 3px;
      text-transform: uppercase;
      font-weight: 600;
      margin-bottom: 16px;
    }

    .section-title {
      font-size: clamp(32px, 4vw, 48px);
      font-weight: 800;
      line-height: 1.1;
      margin-bottom: 20px;
      letter-spacing: -1px;
    }

    .section-subtitle {
      font-size: 18px;
      color: var(--muted);
      max-width: 720px;
      margin-bottom: 60px;
    }

    /* Challenge */
    .role-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 30px;
    }

    .role-card {
      background: linear-gradient(135deg, var(--navy-mid), var(--navy));
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 40px;
      position: relative;
      overflow: hidden;
      transition: all 0.4s ease;
    }

    .role-card:hover {
      border-color: var(--gold);
      transform: translateY(-4px);
    }

    .role-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: var(--gold);
    }

    .role-icon {
      width: 56px;
      height: 56px;
      background: var(--gold-dim);
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 24px;
      color: var(--gold);
    }

    .role-card h3 {
      font-size: 22px;
      font-weight: 700;
      margin-bottom: 8px;
    }

    .role-for {
      font-size: 13px;
      color: var(--gold);
      letter-spacing: 1px;
      text-transform: uppercase;
      font-weight: 600;
      margin-bottom: 16px;
    }

    .role-card p {
      font-size: 16px;
      color: var(--muted);
      line-height: 1.6;
    }

    /* Services */
    .services-section {
      background: var(--navy);
    }

    .services-grid-web {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 24px;
    }

    .svc-card {
      background: var(--navy-mid);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 36px;
      transition: all 0.4s ease;
      position: relative;
      overflow: hidden;
    }

    .svc-card:hover {
      border-color: var(--gold);
      transform: translateY(-6px);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
    }

    .svc-number {
      position: absolute;
      top: 20px;
      right: 24px;
      font-size: 48px;
      font-weight: 800;
      color: var(--gold-dim);
      line-height: 1;
    }

    .svc-card h3 {
      font-size: 20px;
      font-weight: 700;
      margin-bottom: 6px;
      color: var(--white);
      max-width: 80%;
    }

    .svc-sub {
      font-size: 13px;
      color: var(--gold);
      letter-spacing: 1px;
      text-transform: uppercase;
      font-weight: 600;
      margin-bottom: 16px;
    }

    .svc-card p {
      font-size: 15px;
      color: var(--muted);
      line-height: 1.6;
    }

    .svc-tag {
      display: inline-block;
      margin-top: 16px;
      padding: 6px 14px;
      background: var(--gold-dim);
      color: var(--gold-light);
      border-radius: 4px;
      font-size: 12px;
      font-weight: 600;
      letter-spacing: 1px;
      text-transform: uppercase;
    }

    /* Differentiators */
    .diff-grid-web {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 30px;
    }

    .diff-card-web {
      text-align: center;
      padding: 40px 30px;
      background: var(--navy-mid);
      border: 1px solid var(--border);
      border-radius: 16px;
      transition: all 0.4s ease;
    }

    .diff-card-web:hover {
      border-color: var(--gold);
      transform: translateY(-4px);
    }

    .diff-icon-web {
      width: 72px;
      height: 72px;
      margin: 0 auto 24px;
      background: var(--gold-dim);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--gold);
    }

    .diff-card-web h3 {
      font-size: 20px;
      font-weight: 700;
      margin-bottom: 12px;
      color: var(--gold-light);
    }

    .diff-card-web p {
      font-size: 15px;
      color: var(--muted);
      line-height: 1.6;
    }

    /* Process */
    .process-section {
      background: var(--navy);
    }

    .process-steps {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
      position: relative;
    }

    .process-steps::before {
      content: '';
      position: absolute;
      top: 40px;
      left: 15%;
      right: 15%;
      height: 2px;
      background: linear-gradient(90deg, transparent, var(--gold), transparent);
      z-index: 0;
    }

    .step-card {
      text-align: center;
      position: relative;
      z-index: 1;
      padding: 20px;
    }

    .step-num {
      width: 80px;
      height: 80px;
      background: var(--navy-mid);
      border: 2px solid var(--gold);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 20px;
      font-size: 28px;
      font-weight: 800;
      color: var(--gold);
    }

    .step-card h3 {
      font-size: 18px;
      font-weight: 700;
      color: var(--gold-light);
      margin-bottom: 8px;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .step-card p {
      font-size: 14px;
      color: var(--muted);
      line-height: 1.5;
    }

    /* Final CTA */
    .final-cta {
      text-align: center;
      padding: 120px 60px;
      position: relative;
      background: linear-gradient(135deg, var(--navy-deep), var(--navy-mid));
    }

    .final-cta::before {
      content: '';
      position: absolute;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 100px;
      height: 3px;
      background: var(--gold);
    }

    .final-cta .section-title {
      max-width: 720px;
      margin: 0 auto 20px;
    }

    .final-cta p {
      font-size: 18px;
      color: var(--muted);
      max-width: 640px;
      margin: 0 auto 40px;
    }

    .final-cta-actions {
      display: flex;
      gap: 16px;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 60px;
    }

    .contact-info {
      display: flex;
      gap: 30px;
      justify-content: center;
      flex-wrap: wrap;
      padding-top: 40px;
      border-top: 1px solid var(--border);
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 10px;
      color: var(--muted);
      font-size: 14px;
    }

    .contact-item svg {
      color: var(--gold);
      flex-shrink: 0;
    }

    /* Footer */
    .site-footer {
      padding: 30px 60px;
      background: var(--navy-deep);
      border-top: 1px solid var(--border);
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 16px;
    }

    .footer-text {
      font-size: 13px;
      color: var(--muted);
    }

    .footer-motto {
      font-size: 12px;
      color: var(--gold);
      letter-spacing: 2px;
      text-transform: uppercase;
      font-weight: 600;
    }

    /* Animations */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .animate-in {
      animation: fadeInUp 0.8s ease forwards;
    }

    .delay-1 {
      animation-delay: 0.1s;
      opacity: 0;
    }

    .delay-2 {
      animation-delay: 0.2s;
      opacity: 0;
    }

    .delay-3 {
      animation-delay: 0.3s;
      opacity: 0;
    }

    .delay-4 {
      animation-delay: 0.4s;
      opacity: 0;
    }

    .reveal {
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.8s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Responsive */
    @media (max-width: 900px) {
      .site-header {
        padding: 14px 20px;
        gap: 16px;
      }

      .logo-text {
        font-size: 15px;
      }

      .logo-tagline {
        font-size: 10px;
      }

      .header-cta {
        padding: 10px 14px;
        font-size: 11px;
      }

      .hero {
        padding: 110px 24px 70px;
      }

      .section {
        padding: 70px 24px;
      }

      .role-grid,
      .services-grid-web,
      .diff-grid-web,
      .process-steps {
        grid-template-columns: 1fr;
      }

      .process-steps::before {
        display: none;
      }

      .final-cta {
        padding: 80px 24px;
      }

      .site-footer {
        padding: 24px;
        flex-direction: column;
        text-align: center;
      }

      .hero-cta-group,
      .final-cta-actions {
        flex-direction: column;
        align-items: flex-start;
      }

      .final-cta-actions {
        align-items: center;
      }

      .cta-button {
        width: 100%;
        max-width: 360px;
        text-align: center;
      }
    }
  </style>
</head>

<body>

  <!-- Header -->
  <header class="site-header">
    <div class="logo-area">
      <div class="logo-text">OSORIO <span class="gold">&amp;</span> KALIL</div>
      <div class="logo-tagline">Energy Advisors</div>
    </div>

    <button class="header-cta" onclick="scrollToSection('final-cta')">
      Request Technical Validation
    </button>
  </header>

  <!-- Hero -->
  <section class="hero">
    <div class="hero-bg"></div>

    <div class="hero-content">
      <div class="hero-label animate-in">
        Independent Owner's Engineering
      </div>

      <h1 class="hero-title animate-in delay-1">
        Protecting CAPEX.<br>
        <span class="gold">Mitigating Risk.</span>
      </h1>

      <p class="hero-subtitle animate-in delay-2">
        For energy producers anywhere. We validate, audit, and secure your assets before the concrete is poured.
      </p>

      <div class="motto animate-in delay-3">
        No tokens. Creative solutions.
      </div>

      <div class="hero-cta-group animate-in delay-4">
        <button class="cta-button" onclick="scrollToSection('services')">
          Explore Our Services
        </button>

        <button class="cta-button outline" onclick="scrollToSection('process')">
          See Our Process
        </button>
      </div>
    </div>
  </section>

  <!-- Challenge -->
  <section class="section" id="problem">
    <div class="section-label reveal">The Challenge</div>

    <h2 class="section-title reveal">
      Two Stakeholders.<br>
      <span class="gold">One Solution.</span>
    </h2>

    <p class="section-subtitle reveal">
      Role-based messaging for the decision-makers who control your asset's future.
    </p>

    <div class="role-grid">
      <div class="role-card reveal">
        <div class="role-icon">
          <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2"/>
            <circle cx="12" cy="7" r="4"/>
          </svg>
        </div>

        <div class="role-for">For Executives</div>

        <h3>Mitigate Operational Risk</h3>

        <p>
          You need a senior independent voice to validate critical technical decisions before they impact the bottom line.
          We protect your investment.
        </p>
      </div>

      <div class="role-card reveal">
        <div class="role-icon">
          <svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M14.7 6.3a1 1 0 000 1.4l1.6 1.6a1 1 0 001.4 0l3.77-3.77a6 6 0 01-7.94 7.94l-6.91 6.91a2.12 2.12 0 01-3-3l6.91-6.91a6 6 0 017.94-7.94l-3.76 3.76z"/>
          </svg>
        </div>

        <div class="role-for">For Technical Managers</div>

        <h3>Technical Load Relief</h3>

        <p>
          We are your second pair of eyes. We review engineering deliverables and EPC interfaces independently,
          ensuring contractor quality without burning out your team.
        </p>
      </div>
    </div>
  </section>

  <!-- Services -->
  <section class="section services-section" id="services">
    <div class="section-label reveal">Packaged Services</div>

    <h2 class="section-title reveal">
      Express Services<br>
      <span class="gold">for Owners.</span>
    </h2>

    <p class="section-subtitle reveal">
      High-value technical packages. Clear scope. Fixed deliverables. Immediate impact.
    </p>

    <div class="services-grid-web">
      <div class="svc-card reveal">
        <div class="svc-number">01</div>

        <h3>Executive Technical Validation</h3>
        <div class="svc-sub">2nd Opinion</div>

        <p>
          Independent review of high-impact decisions. Aligns technical reality with business goals.
          Protects long-term value.
        </p>

        <div class="svc-tag">Decision Support</div>
      </div>

      <div class="svc-card reveal">
        <div class="svc-number">02</div>

        <h3>Independent Contractor Oversight</h3>
        <div class="svc-sub">FEED / EPC Review</div>

        <p>
          Audits deliverables. Prevents change orders. Ensures compliance with owner standards.
          Protects your CAPEX.
        </p>

        <div class="svc-tag">Contractor Control</div>
      </div>

      <div class="svc-card reveal">
        <div class="svc-number">03</div>

        <h3>Asset Acquisition Integrity</h3>
        <div class="svc-sub">Due Diligence RAG</div>

        <p>
          Red-Amber-Green assessment of technical risks for M&amp;A. Know the risk before you buy.
          Protect the investment.
        </p>

        <div class="svc-tag">M&amp;A Protection</div>
      </div>

      <div class="svc-card reveal">
        <div class="svc-number">04</div>

        <h3>Unbiased Process Safety Assurance</h3>
        <div class="svc-sub">HAZOP / HAZID</div>

        <p>
          Safety reviews independent of the EPC firm. Schedule does not compromise safety.
          Long-term operational integrity.
        </p>

        <div class="svc-tag">Safety First</div>
      </div>
    </div>
  </section>

  <!-- Differentiators -->
  <section class="section" id="differentiators">
    <div class="section-label reveal">Why Trust Us</div>

    <h2 class="section-title reveal">
      Why a Boutique Firm?<br>
      <span class="gold">Senior. Focused. Unbiased.</span>
    </h2>

    <p class="section-subtitle reveal">
      Producers need to know why they should trust an external boutique firm over internal teams or massive EPCs.
    </p>

    <div class="diff-grid-web">
      <div class="diff-card-web reveal">
        <div class="diff-icon-web">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/>
          </svg>
        </div>

        <h3>Owner's Mindset</h3>

        <p>
          We treat your CAPEX as our own. Your interests drive every decision we make.
        </p>
      </div>

      <div class="diff-card-web reveal">
        <div class="diff-icon-web">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <circle cx="12" cy="12" r="10"/>
            <polyline points="12 6 12 12 16 14"/>
          </svg>
        </div>

        <h3>40+ Years Senior Credibility</h3>

        <p>
          Decades of global experience. Unbiased technical excellence. Zero conflicts of interest.
        </p>
      </div>

      <div class="diff-card-web reveal">
        <div class="diff-icon-web">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M9 11l3 3L22 4"/>
            <path d="M21 12v7a2 2 0 01-2 2H5a2 2 0 01-2-2V5a2 2 0 012-2h11"/>
          </svg>
        </div>

        <h3>Execution Focus</h3>

        <p>
          Moving beyond theoretical advice. Concrete, actionable reports. Deliverables that move projects forward.
        </p>
      </div>
    </div>
  </section>

  <!-- Process -->
  <section class="section process-section" id="process">
    <div class="section-label reveal">Our Process</div>

    <h2 class="section-title reveal">
      From Contact<br>
      <span class="gold">to Delivery.</span>
    </h2>

    <p class="section-subtitle reveal">
      A clear, three-phase roadmap designed to convert expert profile into tangible results.
    </p>

    <div class="process-steps">
      <div class="step-card reveal">
        <div class="step-num">1</div>

        <h3>Focus &amp; Target</h3>

        <p>
          Identify needs. Prioritize opportunities. Plan the engagement.
        </p>
      </div>

      <div class="step-card reveal">
        <div class="step-num">2</div>

        <h3>Engage &amp; Qualify</h3>

        <p>
          Connect. Understand pain points. Align on objectives.
        </p>
      </div>

      <div class="step-card reveal">
        <div class="step-num">3</div>

        <h3>Win &amp; Deliver</h3>

        <p>
          Propose pilot. Partner. Execute with excellence.
        </p>
      </div>
    </div>
  </section>

  <!-- Final CTA -->
  <section class="final-cta" id="final-cta">
    <div class="section-label reveal">Take Action</div>

    <h2 class="section-title reveal">
      Ready to Secure<br>
      <span class="gold">Your Asset?</span>
    </h2>

    <p class="reveal">
      Let's discuss your project gray areas, pain points, technical load, budget, or urgency.
      Start with a small paid pilot.
    </p>

    <div class="final-cta-actions reveal">
      <button class="cta-button" onclick="window.location.href='mailto:info@osoriokalil.com?subject=Technical Validation Request'">
        Request a Technical Validation
      </button>
    </div>

    <div class="contact-info reveal">
      <div class="contact-item">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/>
          <polyline points="22,6 12,13 2,6"/>
        </svg>
        info@osoriokalil.com
      </div>

      <div class="contact-item">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6z"/>
          <rect x="2" y="9" width="4" height="12"/>
          <circle cx="4" cy="4" r="2"/>
        </svg>
        LinkedIn: Osorio Kalil Energy Advisory Group
      </div>

      <div class="contact-item">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/>
          <circle cx="12" cy="10" r="3"/>
        </svg>
        Americas, Middle East and Far East Regions
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="site-footer">
    <div class="footer-text">
      © 2026 Osorio Kalil Energy Advisors. All rights reserved.
    </div>

    <div class="footer-motto">
      No tokens. Creative solutions.
    </div>
  </footer>

  <script>
    function scrollToSection(id) {
      const element = document.getElementById(id);

      if (element) {
        element.scrollIntoView({
          behavior: 'smooth',
          block: 'start'
        });
      }
    }

    function initRevealAnimations() {
      const reveals = document.querySelectorAll('.reveal');

      const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
          }
        });
      }, {
        threshold: 0.1
      });

      reveals.forEach((item) => observer.observe(item));
    }

    document.addEventListener('DOMContentLoaded', () => {
      initRevealAnimations();
    });
  </script>

</body>
</html>
