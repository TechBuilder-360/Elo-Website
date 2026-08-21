<template>
  <div class="min-h-screen bg-background font-sans text-foreground antialiased selection:bg-primary selection:text-primary-foreground">
    <NuxtPage />
  </div>
</template>

<script setup>
import '~/assets/css/main.css'

useHead({
  htmlAttrs: {
    lang: 'en',
    class: 'dark' // Default to dark mode based on theme or script in Navbar
  }
})
</script>