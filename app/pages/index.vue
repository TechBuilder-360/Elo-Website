<template>
  <div class="flex flex-col min-h-screen">
    <Navbar />
    <main class="flex-1">
      <Hero />
      <Features />
    </main>
    <Footer />
  </div>
</template>

<script setup>
// SEO Best Practices
useHead({
  title: 'Elo - The Future of Business Finance',
  meta: [
    { name: 'description', content: 'Streamline your financial operations, manage assets securely, and scale your business with Elo.' }
  ]
})
</script>
