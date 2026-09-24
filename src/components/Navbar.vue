<script setup lang="ts">
interface NavItem {
  key: string
  label: string
}

const props = defineProps<{
  items: NavItem[]
  activePage: string
}>()

const emit = defineEmits<{
  (event: 'navigate', key: string): void
}>()
</script>

<template>
  <header class="topbar">
    <div class="brand-wrap">
      <img class="brand-logo" src="/images/Gomore_BG_logo.png" alt="Grow More Research background logo" />
      <div>
        <p class="brand-name">GO MORE RESEARCH PRIVATE LIMITED</p>
      </div>
    </div>

    <nav class="nav" aria-label="Main navigation">
      <button
        v-for="item in props.items"
        :key="item.key"
        type="button"
        class="nav-link"
        :class="{ active: props.activePage === item.key }"
        @click="emit('navigate', item.key)"
      >
        {{ item.label }}
      </button>
    </nav>
  </header>
</template>

<style scoped>
.topbar {
  position: sticky;
  top: 0;
  z-index: 30;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  padding: 1rem 5vw;
  background: rgba(8, 19, 33, 0.92);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
}

.brand-wrap {
  display: flex;
  align-items: center;
  gap: 0.9rem;
}

.brand-logo {
  width: 170px;
  height: auto;
  display: block;
  object-fit: contain;
  filter: drop-shadow(0 8px 18px rgba(40, 156, 250, 0.18));
}

.brand-name {
  margin: 0;
  color: #edf7ff;
  font-size: 1.05rem;
  font-weight: 700;
  letter-spacing: 0.02em;
}

.nav {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 0.5rem;
}

.nav-link {
  border: 1px solid transparent;
  background: transparent;
  color: #d9ebf8;
  font-size: 0.95rem;
  font-weight: 600;
  padding: 0.72rem 1rem;
  border-radius: 999px;
  cursor: pointer;
  transition: all 0.2s ease;
}

.nav-link:hover,
.nav-link.active {
  background: rgba(62, 207, 142, 0.12);
  border-color: rgba(62, 207, 142, 0.35);
  color: #ffffff;
}

@media (max-width: 720px) {
  .topbar {
    flex-direction: column;
    align-items: stretch;
    padding-top: 0.9rem;
    padding-bottom: 0.9rem;
  }

  .brand-wrap {
    width: 100%;
    justify-content: center;
    text-align: center;
    flex-wrap: wrap;
  }

  .brand-logo {
    width: 120px;
    max-width: 42vw;
  }

  .brand-name {
    font-size: 0.82rem;
    line-height: 1.4;
    letter-spacing: 0.02em;
  }

  .nav {
    width: 100%;
    justify-content: center;
    gap: 0.4rem;
  }

  .nav-link {
    flex: 1 1 calc(50% - 0.5rem);
    min-width: 0;
    padding: 0.6rem 0.7rem;
    font-size: 0.76rem;
    text-align: center;
    white-space: nowrap;
  }
}

@media (max-width: 420px) {
  .topbar {
    padding-left: 0.85rem;
    padding-right: 0.85rem;
  }

  .brand-name {
    font-size: 0.72rem;
  }

  .nav {
    gap: 0.35rem;
  }

  .nav-link {
    flex-basis: calc(50% - 0.35rem);
    padding: 0.55rem 0.45rem;
    font-size: 0.7rem;
  }
}

@media print {
  .topbar {
    display: none !important;
  }
}
</style>
