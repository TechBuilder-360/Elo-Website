<template>
  <section class="relative min-h-screen flex items-center overflow-hidden pt-16">
    <!-- Background -->
    <div class="absolute inset-0 z-0">
      <img src="/hero_bg.png" alt="" class="w-full h-full object-cover opacity-50" />
      <div class="absolute inset-0 bg-gradient-to-b from-background/20 via-background/70 to-background"></div>
      <div class="absolute inset-0 bg-gradient-to-r from-background via-background/40 to-transparent"></div>
    </div>

    <!-- Floating Orbs -->
    <div class="absolute top-1/3 right-1/4 w-72 h-72 bg-primary/15 rounded-full blur-3xl opacity-60 animate-pulse-slow"></div>
    <div class="absolute bottom-1/4 left-1/3 w-56 h-56 bg-primary/10 rounded-full blur-3xl opacity-40"></div>

    <div class="container mx-auto px-4 sm:px-6 lg:px-8 relative z-10 py-20">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16 items-center">

        <!-- Left: Copy -->
        <div class="max-w-xl">
          <!-- Badge -->
          <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full border border-primary/30 bg-primary/10 text-primary text-xs font-semibold tracking-wide mb-8">
            <span class="w-1.5 h-1.5 rounded-full bg-primary animate-pulse"></span>
            Trusted by 2,000+ businesses globally
          </div>

          <!-- Headline -->
          <h1 class="text-5xl sm:text-6xl font-extrabold tracking-tight text-foreground leading-[1.08] mb-6">
            Business Finance,
            <br/>
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary via-primary/80 to-primary/50">
              Finally Simplified
            </span>
          </h1>

          <!-- Subheadline -->
          <p class="text-lg text-muted-foreground leading-relaxed mb-10">
            ELO Business is your all-in-one financial operating system. Manage multi-currency wallets, automate compliance, and scale your business globally — from a single, powerful dashboard.
          </p>

          <!-- CTAs -->
          <div class="flex flex-col sm:flex-row gap-4 mb-12">
            <a href="https://elo-business-web.netlify.app/signup" target="_blank"
              class="group inline-flex items-center justify-center gap-2.5 px-7 py-3.5 rounded-xl bg-primary text-primary-foreground font-semibold text-base hover:bg-primary/90 transition-all shadow-xl shadow-primary/30 hover:shadow-primary/40 hover:-translate-y-1">
              Start for Free
              <svg xmlns="http://www.w3.org/2000/svg" width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" class="group-hover:translate-x-0.5 transition-transform"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
            </a>
            <a href="/#how-it-works"
              class="inline-flex items-center justify-center gap-2.5 px-7 py-3.5 rounded-xl border border-border/60 bg-card/50 backdrop-blur text-foreground font-semibold text-base hover:bg-accent transition-all hover:-translate-y-1">
              <svg xmlns="http://www.w3.org/2000/svg" width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><polygon points="10 8 16 12 10 16 10 8"/></svg>
              How It Works
            </a>
          </div>

          <!-- Trust Indicators -->
          <div class="flex flex-wrap gap-6 text-sm text-muted-foreground">
            <div class="flex items-center gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="text-primary"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>
              <span>Bank-grade security</span>
            </div>
            <div class="flex items-center gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="text-primary"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
              <span>Real-time settlements</span>
            </div>
            <div class="flex items-center gap-2">
              <svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="text-primary"><path d="M3 12a9 9 0 1 0 18 0 9 9 0 0 0-18 0"/><path d="M3.6 9h16.8"/><path d="M3.6 15h16.8"/><path d="M11.5 3a17 17 0 0 0 0 18"/><path d="M12.5 3a17 17 0 0 1 0 18"/></svg>
              <span>40+ countries</span>
            </div>
          </div>
        </div>

        <!-- Right: Marketing Image -->
        <div class="relative hidden lg:flex items-center justify-center">
          <div class="absolute inset-0 bg-primary/5 rounded-3xl blur-3xl scale-90"></div>
          <div class="relative rounded-2xl overflow-hidden border border-border/40 shadow-2xl shadow-black/30">
            <img
              src="/hero_marketing.png"
              alt="ELO Business — Empowering global businesses"
              class="w-full h-full object-cover"
              style="max-height: 600px;"
            />
            <!-- Overlay Stats Cards -->
            <div class="absolute bottom-5 left-5 right-5 flex gap-3">
              <div class="flex-1 bg-background/80 backdrop-blur border border-border/60 rounded-xl p-3 text-center">
                <p class="text-xl font-extrabold text-primary">$120M+</p>
                <p class="text-xs text-muted-foreground">Processed</p>
              </div>
              <div class="flex-1 bg-background/80 backdrop-blur border border-border/60 rounded-xl p-3 text-center">
                <p class="text-xl font-extrabold text-primary">2,000+</p>
                <p class="text-xs text-muted-foreground">Businesses</p>
              </div>
              <div class="flex-1 bg-background/80 backdrop-blur border border-border/60 rounded-xl p-3 text-center">
                <p class="text-xl font-extrabold text-primary">99.9%</p>
                <p class="text-xs text-muted-foreground">Uptime</p>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style>
@keyframes pulse-slow {
  0%, 100% { opacity: 0.5; transform: scale(1); }
  50% { opacity: 0.8; transform: scale(1.08); }
}
.animate-pulse-slow { animation: pulse-slow 5s ease-in-out infinite; }
</style>
