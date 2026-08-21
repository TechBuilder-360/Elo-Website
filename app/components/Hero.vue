<template>
  <section class="relative min-h-screen flex items-center overflow-hidden pt-16">
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <img src="/hero_bg.png" alt="" class="w-full h-full object-cover opacity-60" />
      <div class="absolute inset-0 bg-gradient-to-b from-background/10 via-background/60 to-background"></div>
    </div>

    <!-- Floating Orbs -->
    <div class="absolute top-1/4 -right-24 w-96 h-96 bg-primary/20 rounded-full blur-3xl opacity-50 animate-pulse-slow"></div>
    <div class="absolute bottom-1/4 -left-24 w-80 h-80 bg-primary/10 rounded-full blur-3xl opacity-40"></div>

    <div class="container mx-auto px-4 sm:px-6 lg:px-8 relative z-10 py-24">
      <div class="max-w-4xl mx-auto text-center">
        <!-- Badge -->
        <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full border border-primary/30 bg-primary/10 text-primary text-xs font-semibold tracking-wide mb-8 backdrop-blur-sm">
          <span class="w-1.5 h-1.5 rounded-full bg-primary animate-pulse"></span>
          Trusted by 2,000+ businesses globally
        </div>

        <!-- Headline -->
        <h1 class="text-5xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight text-foreground leading-[1.08] mb-6">
          Business Finance,
          <br/>
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary via-primary/80 to-primary/60">
            Finally Simplified
          </span>
        </h1>

        <!-- Subheadline -->
        <p class="text-lg sm:text-xl text-muted-foreground leading-relaxed max-w-2xl mx-auto mb-10">
          ELO Business is your all-in-one financial operating system. Manage multi-currency wallets, automate compliance, track analytics, and scale globally — all from one powerful dashboard.
        </p>

        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center mb-16">
          <a href="https://elo-business-web.netlify.app/signup" target="_blank"
            class="group inline-flex items-center gap-2.5 px-7 py-3.5 rounded-xl bg-primary text-primary-foreground font-semibold text-base hover:bg-primary/90 transition-all shadow-xl shadow-primary/30 hover:shadow-primary/40 hover:-translate-y-1">
            Start for Free
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round" class="group-hover:translate-x-0.5 transition-transform"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
          </a>
          <a href="/#how-it-works"
            class="inline-flex items-center gap-2.5 px-7 py-3.5 rounded-xl border border-border bg-background/50 backdrop-blur text-foreground font-semibold text-base hover:bg-accent transition-all hover:-translate-y-1">
            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><polygon points="10 8 16 12 10 16 10 8"/></svg>
            See How It Works
          </a>
        </div>

        <!-- Social Proof -->
        <div class="flex flex-col sm:flex-row items-center justify-center gap-6 text-sm text-muted-foreground">
          <div class="flex items-center gap-2">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="currentColor" class="text-primary"><path d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/></svg>
            <span>Bank-grade security</span>
          </div>
          <div class="hidden sm:block w-px h-4 bg-border"></div>
          <div class="flex items-center gap-2">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="text-primary"><path d="M3 12a9 9 0 1 0 9-9 9.75 9.75 0 0 0-6.74 2.74L3 8"/><path d="M3 3v5h5"/><path d="M12 7v5l4 2"/></svg>
            <span>Real-time transactions</span>
          </div>
          <div class="hidden sm:block w-px h-4 bg-border"></div>
          <div class="flex items-center gap-2">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="text-primary"><path d="M12 22V12"/><path d="m2 7 10 5 10-5"/><path d="M2 17l10 5 10-5"/><path d="m2 12 10 5 10-5"/></svg>
            <span>Fiat &amp; Crypto support</span>
          </div>
        </div>
      </div>

      <!-- Dashboard Preview -->
      <div class="mt-20 relative max-w-5xl mx-auto">
        <div class="absolute inset-x-0 -top-8 h-px bg-gradient-to-r from-transparent via-primary/50 to-transparent"></div>
        <!-- Glow behind image -->
        <div class="absolute inset-0 bg-primary/5 rounded-2xl blur-3xl scale-95 -z-10"></div>
        <div class="rounded-2xl overflow-hidden border border-border/60 shadow-2xl shadow-black/40 bg-card/30 backdrop-blur p-1.5">
          <img
            src="/dashboard_preview.png"
            alt="ELO Business Dashboard Preview"
            class="w-full rounded-xl object-cover"
          />
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
  50% { opacity: 0.7; transform: scale(1.05); }
}
.animate-pulse-slow {
  animation: pulse-slow 4s ease-in-out infinite;
}
</style>
