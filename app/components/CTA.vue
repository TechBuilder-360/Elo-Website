<template>
  <section class="w-full py-24 md:py-32 overflow-hidden">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="relative rounded-3xl bg-gradient-to-br from-primary/20 via-card to-card border border-primary/20 overflow-hidden p-10 md:p-16">
        <!-- Background decorative elements -->
        <div class="absolute -top-24 -right-24 w-72 h-72 bg-primary/20 rounded-full blur-3xl"></div>
        <div class="absolute -bottom-16 -left-16 w-56 h-56 bg-primary/10 rounded-full blur-3xl"></div>

        <div class="relative z-10 text-center max-w-3xl mx-auto">
          <h2 class="text-4xl md:text-5xl font-extrabold tracking-tight text-foreground mb-4">
            Ready to grow your business?
          </h2>
          <p class="text-lg text-muted-foreground leading-relaxed mb-10">
            Join over 2,000 businesses already using ELO to manage their finances, stay compliant, and scale globally. Get started in minutes — completely free.
          </p>
          <div class="flex flex-col sm:flex-row gap-4 justify-center">
            <a href="https://elo-business-web.netlify.app/signup" target="_blank"
              class="inline-flex items-center justify-center gap-2.5 px-8 py-4 rounded-xl bg-primary text-primary-foreground font-bold text-base hover:bg-primary/90 transition-all shadow-xl shadow-primary/30 hover:-translate-y-1">
              Start for Free — No Credit Card
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
            </a>
            <NuxtLink to="/about"
              class="inline-flex items-center justify-center gap-2.5 px-8 py-4 rounded-xl border border-border bg-background/50 backdrop-blur text-foreground font-semibold text-base hover:bg-accent transition-all hover:-translate-y-1">
              Learn About Us
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
