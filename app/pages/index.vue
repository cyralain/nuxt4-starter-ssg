<script setup lang="ts">
useHead({
  title: 'Hello World — Nuxt 4 SSG',
  meta: [{ name: 'description', content: 'Page statique générée avec Nuxt 4' }],
})

const generatedAt = new Date().toISOString()
</script>

<template>
  <main class="page">
    <h1>Hello World 👋</h1>
    <p>Nuxt 4 · rendu statique (SSG)</p>
    <p class="meta">Généré le {{ generatedAt }}</p>
  </main>
</template>

<style scoped>
.page {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  font-family: system-ui, -apple-system, sans-serif;
  text-align: center;
}
h1 { font-size: 3rem; margin: 0; }
p { margin: 0; color: #444; }
.meta { font-size: 0.85rem; color: #888; }
</style>
