<template>
  <section class="w-full py-24 bg-secondary/20">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
        <div v-for="(stat, i) in stats" :key="i" class="space-y-1">
          <p class="text-4xl font-extrabold text-primary">{{ stat.value }}</p>
          <p class="text-sm text-muted-foreground font-medium">{{ stat.label }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const stats = [
  { value: '2,000+', label: 'Businesses Onboarded' },
  { value: '$120M+', label: 'Transactions Processed' },
  { value: '40+', label: 'Countries Supported' },
  { value: '99.9%', label: 'Uptime Guarantee' },
]
</script>
