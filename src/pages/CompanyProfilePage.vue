<script setup lang="ts">
function downloadPdf() {
  window.print()
}
</script>

<template>
  <section class="page-section">
    <div class="section-heading">
      <p class="eyebrow">Company profile</p>
      <h2>Focused on strategic value and long-term trust.</h2>
    </div>

    <div class="actions-row">
      <button type="button" class="download-btn" @click="downloadPdf">
        Download Company Profile (PDF)
      </button>
    </div>

    <div class="print-header" aria-hidden="true">
      <img class="print-logo" src="/images/Gomore_logo.png" alt="Go More Research Private Limited logo" />
      <div>
        <p class="print-company-name">GO MORE RESEARCH PRIVATE LIMITED</p>
        <p class="print-company-subtitle">Corporate Profile &amp; Capabilities Statement</p>
      </div>
    </div>

    <div class="profile-grid">
      <div class="info-card wide-card">
        <h3>Corporate Profile &amp; Capabilities Statement</h3>
        <p>
          <strong>Go More Research Private Limited</strong> is an Indian information technology consulting and software engineering firm. We help modern businesses transition from rigid legacy processes to scalable, data-backed digital architectures. By uniting research-led technical discovery with full-stack software development, we engineer resilient software systems, integrate complex technical environments, and safeguard business continuity.
        </p>
      </div>
    </div>

    <div class="profile-grid two-column">
      <div class="info-card">
        <h3>Executive Summary</h3>
        <p>
          Go More Research Private Limited is an Indian information technology consulting and software engineering firm. We help modern businesses transition from rigid legacy processes to scalable, data-backed digital architectures. By uniting research-led technical discovery with full-stack software development, we engineer resilient software systems, integrate complex technical environments, and safeguard business continuity.
        </p>
      </div>

      <div class="info-card">
        <h3>Corporate Overview</h3>
        <div class="meta-list">
          <div><span>Legal Entity</span><strong>Go More Research Private Limited</strong></div>
          <div><span>Industry</span><strong>Information Technology &amp; Digital Services</strong></div>
          <div><span>Primary Classifications</span><strong>SAC 998313 (IT Consulting &amp; Support), SAC 998314 (IT Design &amp; Development)</strong></div>
          <div><span>Delivery Model</span><strong>End-to-End Delivery, Staff Augmentation, Dedicated Engineering Teams</strong></div>
          <div><span>Core Value</span><strong>Research-driven engineering with modular scalability</strong></div>
        </div>
      </div>
    </div>

    <div class="timeline">
      <div class="timeline-item">
        <span class="year">Core Capabilities</span>
        <div>
          <h4>What we do</h4>
          <p>
            <strong>IT Consulting &amp; Strategic Roadmaps:</strong> Comprehensive technical audits, technology stack advisory, infrastructure cost-optimization, and legacy system modernization frameworks.<br>
            <strong>Custom Software Engineering:</strong> Full-lifecycle development of enterprise web applications, mobile platforms, and customer portals using modern development stacks.<br>
            <strong>Systems Architecture &amp; Integration:</strong> Development of microservices, custom RESTful APIs, third-party ERP/CRM integrations, and database schemas designed to eliminate data silos.<br>
            <strong>Maintenance, Security &amp; Support:</strong> 24/7 technical monitoring, patch management, automated backup setups, database recovery planning, and system vulnerability assessments.
          </p>
        </div>
      </div>

      <div class="timeline-item">
        <span class="year">Engagement Lifecycle</span>
        <div>
          <h4>How we work</h4>
          <p>
            <strong>Phase 1: Discovery &amp; Research:</strong> In-depth technical due diligence, workflow mapping, and architecture planning before writing any code.<br>
            <strong>Phase 2: Prototyping &amp; Architecture:</strong> Developing responsive UI/UX wireframes, database schemas, and API documentation for transparent stakeholder sign-off.<br>
            <strong>Phase 3: Agile Development &amp; QA:</strong> Iterative development sprints paired with automated unit testing, code reviews, and end-to-end quality assurance.<br>
            <strong>Phase 4: Deployment &amp; Optimization:</strong> Cloud migration, CI/CD pipeline automation, production deployment, and continuous performance tuning.
          </p>
        </div>
      </div>

      <div class="timeline-item">
        <span class="year">Why Us</span>
        <div>
          <h4>Advantages</h4>
          <p>
            <strong>Proven Technical Standards:</strong> Modern, maintainable source code backed by clean documentation and clear intellectual property transfer.<br>
            <strong>Strict Business Continuity:</strong> Redundant cloud setups and disaster mitigation strategies built into every architectural deployment.<br>
            <strong>Agile Transparency:</strong> Direct milestone tracking, transparent sprint demos, and single points of contact for every client account.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.page-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 4rem 1.5rem 2rem;
  position: relative;
  overflow: hidden;
}

.page-section::before {
  content: "";
  position: absolute;
  inset: 8% 5%;
  background-image: url('/images/Gomore_logo.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: 62%;
  opacity: 0;
  pointer-events: none;
  z-index: 0;
}

.page-section > * {
  position: relative;
  z-index: 1;
}

.section-heading {
  margin-bottom: 2rem;
}

.actions-row {
  display: flex;
  justify-content: flex-start;
  margin: 0 0 1.5rem;
}

.print-header {
  display: none;
  align-items: center;
  gap: 1rem;
  padding: 0 0 1.2rem;
  border-bottom: 1px solid rgba(17, 29, 39, 0.15);
  margin-bottom: 1.5rem;
}

.print-logo {
  width: 120px;
  height: auto;
  display: block;
}

.print-company-name {
  margin: 0;
  color: #091b2a;
  font-size: 1.1rem;
  font-weight: 800;
  letter-spacing: 0.04em;
}

.print-company-subtitle {
  margin: 0.2rem 0 0;
  color: #2f3d4d;
  font-size: 0.9rem;
}

.download-btn {
  border: none;
  border-radius: 999px;
  padding: 0.9rem 1.4rem;
  font-size: 0.98rem;
  font-weight: 700;
  background: linear-gradient(135deg, #2dd4bf, #3b82f6);
  color: #04141d;
  cursor: pointer;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  box-shadow: 0 12px 30px rgba(59, 130, 246, 0.22);
}

.download-btn:hover {
  transform: translateY(-1px);
}

.eyebrow {
  margin: 0 0 0.7rem;
  color: #7dd3b3;
  font-size: 0.8rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  font-weight: 700;
}

h2 {
  margin: 0;
  font-size: clamp(2rem, 4vw, 3rem);
  color: #f8fbff;
}

.profile-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1rem;
}

.profile-grid.two-column {
  margin-top: 1rem;
}

.wide-card {
  grid-column: 1 / -1;
}

.info-card {
  background: rgba(17, 29, 39, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 18px;
  padding: 1.5rem;
}

.info-card h3 {
  color: #f8fbff;
  margin-top: 0;
}

.info-card p {
  margin: 0;
  line-height: 1.8;
  color: #d5e4f4;
}

.meta-list {
  display: grid;
  gap: 0.8rem;
}

.meta-list div {
  display: grid;
  gap: 0.25rem;
}

.meta-list span {
  color: #7dd3b3;
  font-size: 0.85rem;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  font-weight: 700;
}

.meta-list strong {
  color: #d5e4f4;
  line-height: 1.6;
  font-weight: 600;
}

.timeline {
  margin-top: 2rem;
  display: grid;
  gap: 1rem;
}

.timeline-item {
  display: grid;
  grid-template-columns: 180px 1fr;
  gap: 1rem;
  align-items: start;
  background: rgba(17, 29, 39, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 18px;
  padding: 1.2rem 1.5rem;
}

.year {
  display: inline-block;
  font-size: 1.1rem;
  font-weight: 800;
  color: #7dd3b3;
  line-height: 1.5;
}

.timeline-item h4 {
  margin: 0 0 0.4rem;
  color: #f8fbff;
}

.timeline-item p {
  margin: 0;
  color: #d5e4f4;
  line-height: 1.8;
}

.timeline-item strong {
  color: #f8fbff;
}

@media (max-width: 700px) {
  .profile-grid {
    grid-template-columns: 1fr;
  }

  .timeline-item {
    grid-template-columns: 1fr;
  }

  .page-section {
    padding-top: 3rem;
  }

  .download-btn {
    width: 100%;
    justify-content: center;
  }
}

@media print {
  @page {
    size: A4 portrait;
    margin: 12mm;
  }

  .download-btn {
    display: none;
  }

  .page-section {
    max-width: 100%;
    padding: 0;
    color: #0f172a;
    background: transparent;
  }

  .page-section::before {
    opacity: 0.08;
  }

  .print-header {
    display: flex;
  }

  .section-heading {
    margin-top: 0;
    margin-bottom: 1.2rem;
  }

  h2,
  .info-card h3,
  .timeline-item h4,
  .timeline-item strong,
  .meta-list strong,
  .print-company-name,
  .print-company-subtitle {
    color: #0f172a !important;
  }

  .eyebrow {
    color: #0f766e !important;
  }

  .info-card,
  .timeline-item {
    background: rgba(255, 255, 255, 0.92) !important;
    border-color: rgba(15, 23, 42, 0.12) !important;
    box-shadow: none !important;
  }

  .meta-list span,
  .year {
    color: #0f766e !important;
  }

  .info-card p,
  .timeline-item p,
  .value-panel,
  .detail-panel {
    color: #1f2937 !important;
  }

  body {
    background: #ffffff !important;
    color: #111827 !important;
    -webkit-print-color-adjust: exact;
    print-color-adjust: exact;
  }
}
</style>
