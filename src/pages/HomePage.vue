<template>
  <section class="page-section hero-section">
    <div class="content-block">
      <p class="eyebrow">Growth-focused market intelligence</p>
      <h1>Helping businesses make smarter investment decisions.</h1>
      <p class="lead">
        We deliver strategic research, market insights, and financial analysis that empower leaders to act with clarity and confidence.
      </p>
      <div class="cta-row">
        <button type="button">Get Started</button>
        <button type="button" class="secondary">Learn More</button>
      </div>
      <ul class="stats-list">
        <li><strong>12+</strong><span>Years of research</span></li>
        <li><strong>350+</strong><span>Client engagements</span></li>
        <li><strong>96%</strong><span>Client retention</span></li>
      </ul>
    </div>

    <div class="hero-panel">
      <div class="panel-card">
        <span class="pill">Market Overview</span>
        <h3>Revenue growth accelerated by 24%</h3>
        <div class="chart-bars" aria-label="Chart illustration">
          <span style="height: 35%"></span>
          <span style="height: 48%"></span>
          <span style="height: 56%"></span>
          <span style="height: 72%"></span>
          <span style="height: 90%"></span>
          <span style="height: 100%"></span>
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
}

.hero-section {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  align-items: center;
  gap: 2.5rem;
}

.eyebrow {
  margin: 0 0 1rem;
  color: #7dd3b3;
  font-size: 0.8rem;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  font-weight: 700;
}

h1 {
  margin: 0;
  font-size: clamp(2.5rem, 5vw, 4.5rem);
  line-height: 1.04;
  color: #f8fbff;
}

.lead {
  margin: 1.25rem 0 0;
  max-width: 40rem;
  font-size: 1.08rem;
  line-height: 1.7;
  color: #c2d4e5;
}

.cta-row {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  margin-top: 2rem;
}

button {
  border: none;
  border-radius: 999px;
  padding: 0.9rem 1.5rem;
  font-size: 0.98rem;
  font-weight: 700;
  background: linear-gradient(135deg, #2dd4bf, #3b82f6);
  color: #07131d;
  cursor: pointer;
}

button.secondary {
  background: transparent;
  color: #edf7ff;
  border: 1px solid rgba(255, 255, 255, 0.15);
}

.stats-list {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  margin: 2.5rem 0 0;
  padding: 0;
}

.stats-list li {
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
  min-width: 120px;
}

.stats-list strong {
  font-size: 1.7rem;
  color: #f8fbff;
}

.stats-list span {
  color: #b8cfe0;
  font-size: 0.9rem;
}

.hero-panel {
  display: flex;
  justify-content: center;
}

.panel-card {
  width: min(100%, 430px);
  background: linear-gradient(180deg, rgba(18, 35, 48, 0.9), rgba(11, 20, 29, 0.96));
  border: 1px solid rgba(255, 255, 255, 0.07);
  border-radius: 24px;
  padding: 1.5rem;
  box-shadow: 0 24px 55px rgba(0, 0, 0, 0.25);
}

.pill {
  display: inline-flex;
  padding: 0.38rem 0.7rem;
  border-radius: 999px;
  background: rgba(61, 196, 152, 0.14);
  color: #9ae6c8;
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
}

.panel-card h3 {
  margin: 1rem 0 1.5rem;
  color: #f8fbff;
  font-size: 1.7rem;
}

.chart-bars {
  height: 210px;
  display: flex;
  align-items: end;
  gap: 0.8rem;
  padding: 1rem 0 0.5rem;
}

.chart-bars span {
  flex: 1;
  display: block;
  border-radius: 12px 12px 0 0;
  background: linear-gradient(180deg, #34d399, #3b82f6);
  box-shadow: 0 12px 25px rgba(59, 130, 246, 0.3);
}

@media (max-width: 900px) {
  .hero-section {
    grid-template-columns: 1fr;
  }

  .page-section {
    padding-top: 3rem;
  }
}

@media (max-width: 540px) {
  .cta-row {
    flex-direction: column;
  }

  .cta-row button {
    width: 100%;
  }

  .stats-list {
    gap: 1rem 1.5rem;
  }

  .stats-list li {
    min-width: 110px;
  }

  .panel-card {
    padding: 1.2rem;
  }
}
</style>
