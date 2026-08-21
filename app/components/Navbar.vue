<template>
  <nav class="fixed top-0 inset-x-0 z-50 transition-all duration-300"
    :class="scrolled ? 'bg-background/90 backdrop-blur-xl border-b border-border/60 shadow-sm shadow-black/10' : 'bg-transparent'">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
      <!-- Logo -->
      <NuxtLink to="/" class="flex items-center gap-2.5 group">
        <div class="w-8 h-8 rounded-lg bg-primary flex items-center justify-center overflow-hidden shadow-lg shadow-primary/30">
          <img src="/favicon_io/favicon_io/apple-touch-icon.png" alt="ELO" class="w-full h-full object-cover" />
        </div>
        <span class="text-lg font-bold tracking-tight text-foreground group-hover:text-primary transition-colors">ELO Business</span>
      </NuxtLink>

      <!-- Desktop Nav -->
      <div class="hidden md:flex items-center gap-1">
        <a href="/#features" class="nav-link">Features</a>
        <a href="/#how-it-works" class="nav-link">How It Works</a>
        <NuxtLink to="/about" class="nav-link">About</NuxtLink>
      </div>

      <!-- Desktop CTA -->
      <div class="hidden md:flex items-center gap-3">
        <a href="https://eloweb.netlify.app/" target="_blank"
          class="text-sm font-medium text-foreground/80 hover:text-foreground transition-colors px-3 py-2 rounded-md hover:bg-accent">
          Sign In
        </a>
        <a href="https://eloweb.netlify.app/signup" target="_blank"
          class="inline-flex items-center gap-2 px-4 py-2 rounded-lg bg-primary text-primary-foreground text-sm font-semibold hover:bg-primary/90 transition-all shadow-md shadow-primary/25 hover:shadow-lg hover:shadow-primary/30 hover:-translate-y-0.5">
          Get Started Free
          <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
        </a>
      </div>

      <!-- Mobile Hamburger -->
      <button @click="mobileOpen = !mobileOpen" class="md:hidden p-2 rounded-lg text-foreground/70 hover:text-foreground hover:bg-accent">
        <svg v-if="!mobileOpen" xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="4" x2="20" y1="6" y2="6"/><line x1="4" x2="20" y1="12" y2="12"/><line x1="4" x2="20" y1="18" y2="18"/></svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M18 6 6 18"/><path d="m6 6 12 12"/></svg>
      </button>
    </div>

    <!-- Mobile Menu -->
    <div v-if="mobileOpen" class="md:hidden bg-background/95 backdrop-blur-xl border-b border-border">
      <div class="container mx-auto px-4 py-4 flex flex-col gap-1">
        <a href="/#features" class="mobile-nav-link" @click="mobileOpen = false">Features</a>
        <a href="/#how-it-works" class="mobile-nav-link" @click="mobileOpen = false">How It Works</a>
        <NuxtLink to="/about" class="mobile-nav-link" @click="mobileOpen = false">About</NuxtLink>
        <div class="flex flex-col gap-2 pt-3 mt-2 border-t border-border">
          <a href="https://eloweb.netlify.app/" target="_blank" class="w-full text-center py-2.5 rounded-lg border border-border text-sm font-medium hover:bg-accent transition-colors">Sign In</a>
          <a href="https://eloweb.netlify.app/signup" target="_blank" class="w-full text-center py-2.5 rounded-lg bg-primary text-primary-foreground text-sm font-semibold hover:bg-primary/90 transition-colors">Get Started Free</a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const scrolled = ref(false)
const mobileOpen = ref(false)

const handleScroll = () => {
  scrolled.value = window.scrollY > 20
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll, { passive: true })
})
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.nav-link {
  @apply text-sm font-medium text-foreground/70 hover:text-foreground px-3 py-2 rounded-md hover:bg-accent/60 transition-all;
}
.mobile-nav-link {
  @apply text-sm font-medium text-foreground/80 hover:text-foreground px-3 py-2.5 rounded-lg hover:bg-accent transition-colors;
}
</style>
