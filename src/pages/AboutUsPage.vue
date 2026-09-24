<template>
  <section class="page-section">
    <div class="section-heading">
      <p class="eyebrow">About us</p>
      <h2>Research built around your growth goals.</h2>
    </div>

    <div class="content-grid">
      <div class="text-panel">
        <p>
          At <strong>Go More Research Private Limited</strong>, we believe true digital transformation is built on rigorous analysis and reliable execution. We combine research-backed technical strategy with modern software development to help organizations optimize their infrastructure, automate complex workflows, and unlock sustainable growth.
        </p>
        <p>
          As an enterprise technology partner, we bridge the gap between technical vision and operational reality. From consulting on system modernization to building custom, secure software platforms, our focus remains on engineering resilient solutions that scale alongside our clients' ambitions.
        </p>
      </div>

      <div class="value-panel">
        <h3>Our Core Principles</h3>
        <ul>
          <li>Research Before Execution</li>
          <li>Scalability by Design</li>
          <li>Client-Centric Transparency</li>
        </ul>
      </div>
    </div>

    <div class="info-layout">
      <div class="detail-panel">
        <h3>What We Do</h3>
        <ul>
          <li><strong>IT Consulting &amp; Strategic Advisory:</strong> We assess operational bottlenecks, audit technical performance, and design strategic roadmaps. Our team provides unbiased advisory on software procurement, systems architecture, and business technology modernization.</li>
          <li><strong>Custom Software &amp; Web Application Development:</strong> We design, code, and deploy secure, full-stack software applications tailored to specific business workflows. Every application is built with modern frameworks to ensure performance, reliability, and security.</li>
          <li><strong>Systems Integration &amp; API Architecture:</strong> We connect disparate third-party tools, databases, and enterprise platforms into unified digital ecosystems, removing data silos and enabling automated business processes.</li>
          <li><strong>Cloud Infrastructure &amp; IT Support Services:</strong> We provide end-to-end technical support, maintenance, security patching, and disaster recovery planning to guarantee high availability and uninterrupted operational continuity.</li>
        </ul>
      </div>

      <div class="detail-panel">
        <h3>Our Mission &amp; Vision</h3>
        <ul>
          <li><strong>Our Mission:</strong> To equip forward-thinking enterprises with intelligent, secure, and data-informed digital platforms that streamline operations and drive compounding value.</li>
          <li><strong>Our Vision:</strong> To become a benchmark IT consultancy recognized globally for delivering high-impact technical architecture, precision engineering, and sustainable digital scalability.</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.page-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 4rem 1.5rem 2rem;
}

.section-heading {
  margin-bottom: 2rem;
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

.content-grid,
.info-layout {
  display: grid;
  grid-template-columns: 1.3fr 0.7fr;
  gap: 1.5rem;
}

.info-layout {
  margin-top: 1.5rem;
  grid-template-columns: 1fr 1fr;
}

.text-panel,
.value-panel,
.detail-panel {
  background: rgba(17, 29, 39, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 20px;
  padding: 1.7rem;
}

.text-panel p {
  margin: 0 0 1rem;
  color: #d5e4f4;
  line-height: 1.8;
  font-size: 1.04rem;
}

.value-panel h3,
.detail-panel h3 {
  margin-top: 0;
  margin-bottom: 1rem;
  color: #f8fbff;
  font-size: 1.3rem;
}

.value-panel ul,
.detail-panel ul {
  margin: 0;
  padding-left: 1.2rem;
  color: #d5e4f4;
  line-height: 1.9;
}

.detail-panel li,
.value-panel li {
  margin-bottom: 0.8rem;
}

.detail-panel strong {
  color: #f8fbff;
}

@media (max-width: 760px) {
  .content-grid,
  .info-layout {
    grid-template-columns: 1fr;
  }

  .page-section {
    padding-top: 3rem;
  }
}
</style>
