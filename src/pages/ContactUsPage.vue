<template>
  <section class="page-section">
    <div class="section-heading">
      <p class="eyebrow">Contact us</p>
      <h2>Let’s talk about your next growth move.</h2>
    </div>

    <div class="contact-grid">
      <div class="info-card">
        <h3>Reach us</h3>
        <ul>
          <li>Email: hello@growmoreresearch.com</li>
          <li>Phone: +1 (415) 555-0147</li>
          <li>Address: Floor No.1, Shop No.35 and 36, Grace Plaza, Gopalwadi Road, Daund, Daund, Pune, Maharashtra, 413801</li>
        </ul>
      </div>

      <form class="contact-form" @submit.prevent>
        <div class="field-row">
          <label>
            <span>Name</span>
            <input type="text" placeholder="Your name" />
          </label>
          <label>
            <span>Email</span>
            <input type="email" placeholder="Your email" />
          </label>
        </div>

        <label>
          <span>Subject</span>
          <input type="text" placeholder="How can we help?" />
        </label>

        <label>
          <span>Message</span>
          <textarea rows="5" placeholder="Tell us about your project"></textarea>
        </label>

        <button type="submit">Send Message</button>
      </form>
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

.contact-grid {
  display: grid;
  grid-template-columns: 0.9fr 1.1fr;
  gap: 1rem;
}

.info-card,
.contact-form {
  background: rgba(17, 29, 39, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 18px;
  padding: 1.5rem;
}

.info-card h3 {
  margin-top: 0;
  color: #f8fbff;
}

.info-card ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: grid;
  gap: 0.8rem;
  color: #d5e4f4;
  line-height: 1.7;
}

.contact-form {
  display: grid;
  gap: 1rem;
}

.field-row {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1rem;
}

label {
  display: grid;
  gap: 0.5rem;
  color: #edf7ff;
  font-weight: 600;
}

input,
textarea {
  width: 100%;
  border: 1px solid rgba(255, 255, 255, 0.12);
  background: rgba(9, 16, 23, 0.9);
  color: #edf7ff;
  border-radius: 12px;
  padding: 0.9rem 1rem;
  font: inherit;
  box-sizing: border-box;
}

input::placeholder,
textarea::placeholder {
  color: rgba(226, 238, 248, 0.65);
}

button {
  border: none;
  border-radius: 999px;
  padding: 0.9rem 1.3rem;
  font-size: 1rem;
  font-weight: 700;
  background: linear-gradient(135deg, #2dd4bf, #3b82f6);
  color: #04141d;
  cursor: pointer;
}

@media (max-width: 760px) {
  .contact-grid,
  .field-row {
    grid-template-columns: 1fr;
  }

  .page-section {
    padding-top: 3rem;
  }
}

@media (max-width: 520px) {
  .info-card,
  .contact-form {
    padding: 1.1rem;
  }

  button {
    width: 100%;
  }
}
</style>
