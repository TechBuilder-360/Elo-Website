<template>
  <section id="features" class="w-full py-20 md:py-32 bg-secondary/30">
    <div class="container mx-auto px-4 md:px-6">
      <div class="flex flex-col items-center justify-center space-y-4 text-center mb-16">
        <h2 class="text-3xl md:text-5xl font-bold tracking-tighter text-foreground">
          Everything you need to scale
        </h2>
        <p class="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
          Our platform provides a complete suite of tools to manage your finances, streamline operations, and drive growth.
        </p>
      </div>
      
      <div class="grid w-full grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
        <!-- Feature 1 -->
        <div class="group flex flex-col items-start space-y-4 rounded-xl border border-border bg-card p-6 shadow-sm transition-all hover:shadow-md hover:border-primary/50 relative overflow-hidden">
          <div class="absolute -right-4 -top-4 w-24 h-24 bg-primary/10 rounded-full blur-2xl group-hover:bg-primary/20 transition-all"></div>
          <div class="p-2 bg-primary/10 rounded-lg text-primary">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6"><path d="M21 12V7H5a2 2 0 0 1 0-4h14v4"></path><path d="M3 5v14a2 2 0 0 0 2 2h16v-5"></path><path d="M18 12a2 2 0 0 0 0 4h4v-4Z"></path></svg>
          </div>
          <h3 class="text-xl font-semibold text-card-foreground">Global Wallet</h3>
          <p class="text-muted-foreground leading-relaxed">
            Manage fiat and crypto assets in one unified platform. Send, receive, and swap instantly across borders.
          </p>
        </div>
        
        <!-- Feature 2 -->
        <div class="group flex flex-col items-start space-y-4 rounded-xl border border-border bg-card p-6 shadow-sm transition-all hover:shadow-md hover:border-primary/50 relative overflow-hidden">
          <div class="absolute -right-4 -top-4 w-24 h-24 bg-primary/10 rounded-full blur-2xl group-hover:bg-primary/20 transition-all"></div>
          <div class="p-2 bg-primary/10 rounded-lg text-primary">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6"><rect width="18" height="18" x="3" y="4" rx="2" ry="2"></rect><line x1="16" x2="16" y1="2" y2="6"></line><line x1="8" x2="8" y1="2" y2="6"></line><line x1="3" x2="21" y1="10" y2="10"></line><path d="M8 14h.01"></path><path d="M12 14h.01"></path><path d="M16 14h.01"></path><path d="M8 18h.01"></path><path d="M12 18h.01"></path><path d="M16 18h.01"></path></svg>
          </div>
          <h3 class="text-xl font-semibold text-card-foreground">Automated Compliance</h3>
          <p class="text-muted-foreground leading-relaxed">
            Stay compliant effortlessly with automated KYC/KYB checks, transaction monitoring, and integrated reporting.
          </p>
        </div>
        
        <!-- Feature 3 -->
        <div class="group flex flex-col items-start space-y-4 rounded-xl border border-border bg-card p-6 shadow-sm transition-all hover:shadow-md hover:border-primary/50 relative overflow-hidden">
          <div class="absolute -right-4 -top-4 w-24 h-24 bg-primary/10 rounded-full blur-2xl group-hover:bg-primary/20 transition-all"></div>
          <div class="p-2 bg-primary/10 rounded-lg text-primary">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6"><path d="M3 3v18h18"></path><path d="m19 9-5 5-4-4-3 3"></path></svg>
          </div>
          <h3 class="text-xl font-semibold text-card-foreground">Real-time Analytics</h3>
          <p class="text-muted-foreground leading-relaxed">
            Make data-driven decisions with real-time insights, custom dashboards, and comprehensive financial reports.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
