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
  title: 'ELO Business — Business Finance, Finally Simplified',
  meta: [
    { name: 'description', content: 'ELO Business is your all-in-one financial operating system. Manage multi-currency wallets, automate compliance, track analytics, and scale globally.' },
    { property: 'og:title', content: 'ELO Business — Business Finance, Finally Simplified' },
    { property: 'og:description', content: 'Manage multi-currency wallets, automate compliance, and scale globally with ELO Business.' },
    { property: 'og:type', content: 'website' },
    { name: 'robots', content: 'index, follow' },
  ],
})
</script>
