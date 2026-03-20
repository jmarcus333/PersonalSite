<script setup lang="ts">
import heroImg from "../assets/hero.png";
import { ref, onMounted, onUnmounted } from "vue";

const scrolled = ref(false);

const handleScroll = () => {
  scrolled.value = window.scrollY > 40;
};

onMounted(() => window.addEventListener("scroll", handleScroll));
onUnmounted(() => window.removeEventListener("scroll", handleScroll));
</script>

<template>
  <!-- Navigation -->
  <nav :class="['site-nav', { scrolled }]">
    <div class="nav-inner">
      <a href="#hero" class="nav-logo">JBM</a>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#expertise">Expertise</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#connect" class="nav-cta">Connect</a></li>
      </ul>
    </div>
  </nav>

  <!-- Hero -->
  <section id="hero" class="hero-section">
    <div class="hero-inner">
      <div class="hero-text">
        <p class="eyebrow">Principal Solution Engineer · Salesforce</p>
        <h1>Jeremy B. Marcus</h1>
        <p class="hero-sub">
          Bridging technical complexity and business value in commerce.
          Specializing in Salesforce Commerce Cloud, headless architecture, and
          unified B2B/B2C experiences.
        </p>
        <div class="hero-actions">
          <a href="#connect" class="btn-primary">Get in touch</a>
          <a href="#experience" class="btn-outline">View background</a>
        </div>
      </div>
      <div class="hero-photo-wrap">
        <div class="hero-photo-ring"></div>
        <img :src="heroImg" alt="Jeremy B. Marcus" class="hero-photo" />
      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="section">
    <div class="container">
      <span class="section-label">About</span>
      <h2>Making complex systems feel simple</h2>
      <div class="about-body">
        <p>
          I'm a Principal Solution Engineer at Salesforce with deep roots in the
          e-commerce and SaaS ecosystems. My career spans Salesforce, Demandware
          (now Salesforce Commerce Cloud), and Vendasta—where I've focused on
          building and scaling modern commerce solutions that connect complex
          backend architectures to seamless consumer experiences.
        </p>
        <p>
          I thrive in the space between technical teams and business
          stakeholders, translating hard engineering problems into clear value
          for customers. Whether it's architecting a headless checkout flow or
          enabling a partner channel at scale, I care about getting the details
          right.
        </p>
      </div>
    </div>
  </section>

  <!-- Expertise -->
  <section id="expertise" class="section section-alt">
    <div class="container">
      <span class="section-label">Expertise</span>
      <h2>What I work on</h2>
      <div class="cards-grid">
        <div class="card">
          <div class="card-icon">
            <svg
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1.8"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path d="M6 2 3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z" />
              <line x1="3" y1="6" x2="21" y2="6" />
              <path d="M16 10a4 4 0 0 1-8 0" />
            </svg>
          </div>
          <h3>Salesforce Commerce Cloud</h3>
          <p>
            Deep expertise in SFCC (formerly Demandware)—checkout APIs,
            extensibility, platform architecture, and enterprise deployment
            patterns.
          </p>
        </div>
        <div class="card">
          <div class="card-icon">
            <svg
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1.8"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <polyline points="22 12 18 12 15 21 9 3 6 12 2 12" />
            </svg>
          </div>
          <h3>Headless & Composable Commerce</h3>
          <p>
            Designing modern, API-first storefronts using Lightning Web Runtime
            (LWR) and public APIs—flexibility without sacrificing performance.
          </p>
        </div>
        <div class="card">
          <div class="card-icon">
            <svg
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1.8"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2" />
              <circle cx="9" cy="7" r="4" />
              <path d="M23 21v-2a4 4 0 0 0-3-3.87" />
              <path d="M16 3.13a4 4 0 0 1 0 7.75" />
            </svg>
          </div>
          <h3>Solution Engineering</h3>
          <p>
            Bridging technical complexity with business value—crafting unified
            B2B and B2C solutions that solve real problems and move deals
            forward.
          </p>
        </div>
        <div class="card">
          <div class="card-icon">
            <svg
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="1.8"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <rect x="2" y="3" width="6" height="6" rx="1" />
              <rect x="16" y="3" width="6" height="6" rx="1" />
              <rect x="9" y="15" width="6" height="6" rx="1" />
              <path d="M5 9v4h14V9" />
              <line x1="12" y1="13" x2="12" y2="15" />
            </svg>
          </div>
          <h3>Systems Integration</h3>
          <p>
            Connecting commerce platforms with ERP, OMS, CRM, and marketing
            systems to build seamless, end-to-end customer experiences.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Experience -->
  <section id="experience" class="section">
    <div class="container">
      <span class="section-label">Experience</span>
      <h2>Professional background</h2>
      <div class="timeline">
        <div class="timeline-item">
          <div class="timeline-marker"></div>
          <div class="timeline-body">
            <div class="timeline-meta">
              <span class="timeline-company">Salesforce</span>
            </div>
            <div class="timeline-role">
              Principal Solution Engineer — Commerce Cloud
            </div>
            <p>
              Leading pre-sales engineering for enterprise commerce customers.
              Architecting complex B2B and B2C solutions on SFCC, driving
              technical strategy, and partnering with sales to demonstrate
              platform value at scale.
            </p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-marker"></div>
          <div class="timeline-body">
            <div class="timeline-meta">
              <span class="timeline-company">Demandware</span>
              <span class="timeline-tag">Acquired by Salesforce</span>
            </div>
            <div class="timeline-role">Solution Engineer</div>
            <p>
              Focused on enterprise e-commerce platform delivery before and
              through the Salesforce acquisition. Built deep expertise in the
              Demandware platform that became the foundation of SFCC.
            </p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-marker"></div>
          <div class="timeline-body">
            <div class="timeline-meta">
              <span class="timeline-company">Vendasta</span>
            </div>
            <div class="timeline-role">Technical Program Manager</div>
            <p>
              Scaled SaaS solutions for channel partners, working with resellers
              and SMBs to deliver digital marketing and commerce tooling through
              a multi-tenant platform.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Connect -->
  <section id="connect" class="section section-alt">
    <div class="container connect-container">
      <span class="section-label">Let's talk</span>
      <h2>Interested in working together?</h2>
      <p class="connect-sub">
        Whether you're exploring commerce architecture, evaluating Salesforce,
        or just want to talk shop—I'd love to connect.
      </p>
      <div class="connect-cards">
        <a
          href="https://www.linkedin.com/in/jeremybmarcus/"
          target="_blank"
          rel="noopener"
          class="connect-card"
        >
          <span class="connect-icon linkedin-icon">
            <svg viewBox="0 0 24 24" fill="currentColor">
              <path
                d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"
              />
            </svg>
          </span>
          <div class="connect-card-text">
            <strong>LinkedIn</strong>
            <span>jeremybmarcus</span>
          </div>
        </a>
        <a
          href="https://github.com/jmarcus333"
          target="_blank"
          rel="noopener"
          class="connect-card"
        >
          <span class="connect-icon github-icon">
            <svg viewBox="0 0 24 24" fill="currentColor">
              <path
                d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"
              />
            </svg>
          </span>
          <div class="connect-card-text">
            <strong>GitHub</strong>
            <span>jeremymarcus</span>
          </div>
        </a>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="site-footer">
    <div class="container footer-inner">
      <span>© 2025 Jeremy B. Marcus</span>
      <span class="footer-role">Principal Solution Engineer · Salesforce</span>
    </div>
  </footer>
</template>

<style scoped>
/* ── Navigation ──────────────────────────────────────────── */
.site-nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  padding: 0 24px;
  transition:
    background 0.25s,
    box-shadow 0.25s,
    backdrop-filter 0.25s;
}

.site-nav.scrolled {
  background: var(--nav-bg);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  box-shadow: 0 1px 0 var(--border);
}

.nav-inner {
  max-width: 960px;
  margin: 0 auto;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-logo {
  font-size: 18px;
  font-weight: 700;
  letter-spacing: -0.04em;
  color: var(--text-h);
  text-decoration: none;
}

.nav-links {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  align-items: center;
  gap: 4px;
}

.nav-links a {
  font-size: 14px;
  font-weight: 500;
  color: var(--text);
  padding: 6px 14px;
  border-radius: 8px;
  transition:
    color 0.2s,
    background 0.2s;
  text-decoration: none;
}

.nav-links a:hover {
  color: var(--text-h);
  background: var(--accent-light);
}

.nav-links .nav-cta {
  color: var(--accent);
  background: var(--accent-light);
  font-weight: 600;
}

.nav-links .nav-cta:hover {
  background: var(--accent-mid);
}

/* ── Hero ────────────────────────────────────────────────── */
.hero-section {
  padding: 140px 24px 96px;
  min-height: 100svh;
  display: flex;
  align-items: center;
}

.hero-inner {
  max-width: 960px;
  margin: 0 auto;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 64px;
}

.hero-text {
  flex: 1;
  min-width: 0;
}

.eyebrow {
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 20px;
}

.hero-text h1 {
  font-size: clamp(2.4rem, 6vw, 4rem);
  font-weight: 700;
  margin-bottom: 24px;
  line-height: 1.05;
}

.hero-sub {
  font-size: 18px;
  line-height: 1.7;
  color: var(--text);
  max-width: 520px;
  margin-bottom: 40px;
}

.hero-actions {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

.btn-primary {
  display: inline-flex;
  align-items: center;
  padding: 12px 24px;
  background: var(--accent);
  color: #ffffff;
  font-size: 15px;
  font-weight: 600;
  border-radius: 10px;
  transition:
    opacity 0.2s,
    transform 0.2s,
    box-shadow 0.2s;
  box-shadow: 0 2px 8px rgba(79, 70, 229, 0.35);
}

.btn-primary:hover {
  opacity: 0.92;
  transform: translateY(-1px);
  box-shadow: 0 6px 20px rgba(79, 70, 229, 0.4);
}

.btn-outline {
  display: inline-flex;
  align-items: center;
  padding: 12px 24px;
  border: 1.5px solid var(--border);
  color: var(--text-h);
  font-size: 15px;
  font-weight: 500;
  border-radius: 10px;
  transition:
    border-color 0.2s,
    box-shadow 0.2s,
    transform 0.2s;
}

.btn-outline:hover {
  border-color: var(--accent-border);
  box-shadow: var(--shadow);
  transform: translateY(-1px);
}

.hero-photo-wrap {
  position: relative;
  flex-shrink: 0;
}

.hero-photo-ring {
  position: absolute;
  inset: -8px;
  border-radius: 50%;
  background: conic-gradient(
    from 180deg,
    var(--accent) 0%,
    var(--accent-light) 40%,
    var(--accent) 100%
  );
  opacity: 0.25;
  filter: blur(1px);
}

.hero-photo {
  width: 220px;
  height: 220px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid var(--bg);
  box-shadow: var(--shadow-lg);
  position: relative;
  z-index: 1;
  display: block;
}

/* ── Shared section styles ───────────────────────────────── */
.section {
  padding: 96px 24px;
}

.section-alt {
  background: var(--bg-alt);
}

.container {
  max-width: 960px;
  margin: 0 auto;
}

.section-label {
  display: inline-block;
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--accent);
  background: var(--accent-light);
  padding: 4px 12px;
  border-radius: 99px;
  margin-bottom: 16px;
}

.section h2 {
  font-size: clamp(1.6rem, 3.5vw, 2.25rem);
  margin-bottom: 24px;
}

/* ── About ───────────────────────────────────────────────── */
.about-body {
  display: flex;
  flex-direction: column;
  gap: 16px;
  max-width: 680px;
}

.about-body p {
  font-size: 17px;
  line-height: 1.75;
  color: var(--text);
}

/* ── Cards ───────────────────────────────────────────────── */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  margin-top: 8px;
}

.card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 28px;
  transition:
    box-shadow 0.25s,
    transform 0.25s,
    border-color 0.25s;
}

.card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-3px);
  border-color: var(--accent-border);
}

.card-icon {
  width: 44px;
  height: 44px;
  border-radius: 12px;
  background: var(--accent-light);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 16px;
}

.card-icon svg {
  width: 22px;
  height: 22px;
}

.card h3 {
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 10px;
  color: var(--text-h);
}

.card p {
  font-size: 15px;
  line-height: 1.65;
  color: var(--text);
}

/* ── Timeline ────────────────────────────────────────────── */
.timeline {
  margin-top: 8px;
  display: flex;
  flex-direction: column;
  position: relative;
  padding-left: 28px;
}

.timeline::before {
  content: "";
  position: absolute;
  left: 6px;
  top: 8px;
  bottom: 8px;
  width: 1.5px;
  background: var(--border);
}

.timeline-item {
  position: relative;
  padding-bottom: 44px;
}

.timeline-item:last-child {
  padding-bottom: 0;
}

.timeline-marker {
  position: absolute;
  left: -25px;
  top: 6px;
  width: 13px;
  height: 13px;
  border-radius: 50%;
  background: var(--accent);
  border: 2.5px solid var(--bg);
  box-shadow: 0 0 0 2px var(--accent-border);
}

.timeline-body {
  padding: 24px;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: 14px;
  transition: box-shadow 0.2s;
}

.timeline-body:hover {
  box-shadow: var(--shadow);
}

.timeline-meta {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 6px;
}

.timeline-company {
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: var(--accent);
}

.timeline-tag {
  font-size: 11px;
  font-weight: 500;
  padding: 2px 8px;
  border-radius: 99px;
  background: var(--accent-light);
  color: var(--accent);
  border: 1px solid var(--accent-border);
}

.timeline-role {
  font-size: 17px;
  font-weight: 600;
  color: var(--text-h);
  margin-bottom: 10px;
}

.timeline-body p {
  font-size: 15px;
  line-height: 1.7;
  color: var(--text);
}

/* ── Connect ─────────────────────────────────────────────── */
.connect-container {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.connect-sub {
  font-size: 17px;
  line-height: 1.7;
  color: var(--text);
  max-width: 480px;
  margin-bottom: 40px;
}

.connect-cards {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
  justify-content: center;
}

.connect-card {
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 20px 28px;
  background: var(--bg-card);
  border: 1.5px solid var(--border);
  border-radius: 14px;
  min-width: 220px;
  transition:
    box-shadow 0.25s,
    transform 0.25s,
    border-color 0.25s;
  cursor: pointer;
}

.connect-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-3px);
  border-color: var(--accent-border);
}

.connect-icon {
  width: 44px;
  height: 44px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.connect-icon svg {
  width: 22px;
  height: 22px;
}

.linkedin-icon {
  background: #0a66c2;
  color: #fff;
}

.github-icon {
  background: #24292f;
  color: #fff;
}

@media (prefers-color-scheme: dark) {
  .github-icon {
    background: #30363d;
  }
}

.connect-card-text {
  display: flex;
  flex-direction: column;
  text-align: left;
}

.connect-card-text strong {
  font-size: 16px;
  font-weight: 600;
  color: var(--text-h);
  margin-bottom: 2px;
}

.connect-card-text span {
  font-size: 13px;
  color: var(--text-light);
}

/* ── Footer ──────────────────────────────────────────────── */
.site-footer {
  padding: 32px 24px;
  border-top: 1px solid var(--border);
  margin-top: auto;
}

.footer-inner {
  max-width: 960px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 14px;
  color: var(--text-light);
}

.footer-role {
  font-size: 13px;
}

/* ── Responsive ──────────────────────────────────────────── */
@media (max-width: 768px) {
  .hero-section {
    padding: 120px 24px 72px;
    min-height: auto;
  }

  .hero-inner {
    flex-direction: column-reverse;
    align-items: center;
    text-align: center;
    gap: 40px;
  }

  .hero-sub {
    max-width: 100%;
  }

  .hero-actions {
    justify-content: center;
  }

  .hero-photo {
    width: 160px;
    height: 160px;
  }

  .section {
    padding: 64px 20px;
  }

  .cards-grid {
    grid-template-columns: 1fr;
  }

  .nav-links li:not(:last-child) {
    display: none;
  }

  .footer-inner {
    flex-direction: column;
    gap: 8px;
    text-align: center;
  }

  .timeline {
    padding-left: 20px;
  }

  .timeline-marker {
    left: -17px;
  }
}
</style>
