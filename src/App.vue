<script setup lang="ts">
import { computed, ref } from 'vue'
import Navbar from './components/Navbar.vue'
import HomePage from './pages/HomePage.vue'
import AboutUsPage from './pages/AboutUsPage.vue'
import FinancialsPage from './pages/FinancialsPage.vue'
import CompanyProfilePage from './pages/CompanyProfilePage.vue'
import ContactUsPage from './pages/ContactUsPage.vue'

const navItems = [
  { key: 'home', label: 'Home' },
  { key: 'about', label: 'About Us' },
  { key: 'financials', label: 'Financials' },
  { key: 'company', label: 'Company Profile' },
  { key: 'contact', label: 'Contact Us' },
]

const activePage = ref('home')

const currentPage = computed(() => {
  switch (activePage.value) {
    case 'about':
      return AboutUsPage
    case 'financials':
      return FinancialsPage
    case 'company':
      return CompanyProfilePage
    case 'contact':
      return ContactUsPage
    case 'home':
    default:
      return HomePage
  }
})

function handleNavigate(page: string) {
  activePage.value = page
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
  <div class="page-shell">
    <Navbar :items="navItems" :active-page="activePage" @navigate="handleNavigate" />

    <main class="main-content">
      <component :is="currentPage" />
    </main>
  </div>
</template>

<style>
:root {
  color-scheme: dark;
  font-family: Inter, 'Segoe UI', sans-serif;
  background: #061018;
  color: #edf7ff;
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  min-height: 100vh;
  background:
    radial-gradient(circle at top, rgba(35, 128, 205, 0.24), transparent 30%),
    linear-gradient(180deg, #061018 0%, #0d1b2a 100%);
  overflow-x: hidden;
}

button,
input,
textarea {
  font: inherit;
}

img {
  max-width: 100%;
}

#app {
  min-height: 100vh;
}

.page-shell {
  min-height: 100vh;
}

.main-content {
  width: 100%;
}
</style>
