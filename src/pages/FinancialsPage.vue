<script setup lang="ts">
function downloadFinancialReport() {
  window.print()
}
</script>

<template>
  <section class="page-section">
    <div class="section-heading">
      <p class="eyebrow">Financials</p>
      <h2>Performance that supports confident decision-making.</h2>
    </div>

    <div class="actions-row">
      <button type="button" class="download-btn" @click="downloadFinancialReport">
        Download Financial Reports
      </button>
    </div>

    <div class="print-header" aria-hidden="true">
      <img class="print-logo" src="/images/Gomore_logo.png" alt="Go More Research Private Limited logo" />
      <div>
        <p class="print-company-name">GO MORE RESEARCH PRIVATE LIMITED</p>
        <p class="print-company-subtitle">Financial Performance Report</p>
      </div>
    </div>

    <div class="stats-grid">
      <article class="stat-card">
        <span>Annual Revenue</span>
        <strong>$18.4M</strong>
        <small>+22.6% YoY</small>
      </article>
      <article class="stat-card">
        <span>Net Margin</span>
        <strong>18.7%</strong>
        <small>Stable outlook</small>
      </article>
      <article class="stat-card">
        <span>Operating Cash Flow</span>
        <strong>$5.1M</strong>
        <small>Healthy liquidity</small>
      </article>
      <article class="stat-card">
        <span>Projected Growth</span>
        <strong>31%</strong>
        <small>Next 12 months</small>
      </article>
    </div>

    <div class="table-wrap">
      <table>
        <thead>
          <tr>
            <th>Metric</th>
            <th>FY2024</th>
            <th>FY2025</th>
            <th>Trend</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Revenue</td>
            <td>$14.9M</td>
            <td>$18.4M</td>
            <td>Up 24%</td>
          </tr>
          <tr>
            <td>EBITDA</td>
            <td>$3.2M</td>
            <td>$4.1M</td>
            <td>Up 28%</td>
          </tr>
          <tr>
            <td>Cash Reserves</td>
            <td>$6.8M</td>
            <td>$8.2M</td>
            <td>Up 21%</td>
          </tr>
        </tbody>
      </table>
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

.stats-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 1rem;
}

.stat-card {
  background: rgba(17, 29, 39, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 18px;
  padding: 1.5rem;
}

.stat-card span,
.stat-card small {
  display: block;
  color: #b8cfe0;
}

.stat-card strong {
  display: block;
  margin: 0.8rem 0;
  color: #f8fbff;
  font-size: 2rem;
}

.table-wrap {
  margin-top: 2rem;
  background: rgba(17, 29, 39, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 18px;
  overflow: hidden;
}

table {
  width: 100%;
  border-collapse: collapse;
}

th,
td {
  padding: 1rem 1.2rem;
  text-align: left;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  color: #e8f4ff;
}

th {
  background: rgba(255, 255, 255, 0.03);
  color: #9fe9d8;
  font-weight: 700;
}

@media (max-width: 900px) {
  .stats-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 540px) {
  .stats-grid {
    grid-template-columns: 1fr;
  }

  .page-section {
    padding-top: 3rem;
  }

  .download-btn {
    width: 100%;
  }

  .table-wrap {
    overflow-x: auto;
  }

  table {
    min-width: 480px;
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
  .stat-card strong,
  .print-company-name,
  .print-company-subtitle,
  th,
  td {
    color: #0f172a !important;
  }

  .eyebrow {
    color: #0f766e !important;
  }

  .stat-card,
  .table-wrap {
    background: rgba(255, 255, 255, 0.92) !important;
    border-color: rgba(15, 23, 42, 0.12) !important;
    box-shadow: none !important;
  }

  .stat-card span,
  .stat-card small,
  th,
  td {
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
