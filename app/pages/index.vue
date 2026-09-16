<script setup lang="ts">
useHead({
  title: 'Hello World — Nuxt 4 SSG',
  meta: [{ name: 'description', content: 'Page statique générée avec Nuxt 4' }],
})

// Figé au moment du build : preuve que la page est bien pré-rendue.
const generatedAt = new Date().toISOString()
</script>

<template>
  <main class="page">
    <h1>Hello World 👋</h1>
    <p>Nuxt 4 · rendu statique (SSG)</p>
    <p class="meta">Généré au build le {{ generatedAt }}</p>
  </main>
</template>

<style>
:root {
  --bg: #ffffff;
  --fg: #111827;
  --muted: #6b7280;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg: #0b0d10;
    --fg: #f3f4f6;
    --muted: #9ca3af;
  }
}

html, body, #__nuxt {
  margin: 0;
  background: var(--bg);
  color: var(--fg);
}
</style>

<style scoped>
.page {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0 16px;
  font-family: system-ui, -apple-system, "Segoe UI", sans-serif;
  text-align: center;
}

h1 {
  font-size: clamp(2rem, 8vw, 3rem);
  margin: 0;
}

p {
  margin: 0;
}

.meta {
  font-size: 0.85rem;
  color: var(--muted);
}
</style>
