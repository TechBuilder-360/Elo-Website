<template>
  <div class="min-h-screen bg-background text-foreground">
    <Navbar />
    <main>
      <Hero />
      <Stats />
      <Features />
      <HowItWorks />
      <CTA />
    </main>
    <Footer />
  </div>
</template>

<script setup>
useHead({
  title: 'ELO — Business Finance & Advertising, Simplified',
  meta: [
    { name: 'description', content: 'ELO is your all-in-one financial operating system. Manage multi-currency wallets, automate compliance, track analytics, and scale globally.' },
    { property: 'og:title', content: 'ELO — Business Finance & Advertising, Simplified' },
    { property: 'og:description', content: 'Manage multi-currency wallets, automate compliance, and scale globally with ELO.' },
    { property: 'og:type', content: 'website' },
    { name: 'robots', content: 'index, follow' },
  ],
})
</script>
