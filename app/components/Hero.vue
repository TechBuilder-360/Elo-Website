<template>
  <section class="relative w-full py-20 md:py-32 overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0 z-0 bg-[radial-gradient(ellipse_at_top,_var(--tw-gradient-stops))] from-primary/20 via-background to-background"></div>
    
    <div class="container relative z-10 mx-auto px-4 md:px-6 flex flex-col items-center text-center space-y-8">
      <div class="inline-flex items-center rounded-full border border-primary/20 bg-primary/10 px-3 py-1 text-sm font-medium text-primary">
        🚀 Introducing Elo Business Web
      </div>
      
      <h1 class="text-4xl md:text-6xl lg:text-7xl font-bold tracking-tighter text-foreground max-w-4xl">
        The Future of <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-accent-foreground">Business Finance</span> is Here
      </h1>
      
      <p class="max-w-[42rem] leading-normal text-muted-foreground sm:text-xl sm:leading-8">
        Streamline your financial operations, manage assets securely, and scale your business with Elo's powerful, intelligent platform designed for modern enterprises.
      </p>
      
      <div class="flex flex-col sm:flex-row gap-4 mt-8">
        <button class="inline-flex items-center justify-center rounded-md text-sm font-medium bg-primary text-primary-foreground hover:bg-primary/90 h-12 px-8 shadow-lg shadow-primary/25 transition-transform hover:scale-105">
          Start for free
        </button>
        <button class="inline-flex items-center justify-center rounded-md text-sm font-medium border border-input bg-background hover:bg-accent hover:text-accent-foreground h-12 px-8 transition-transform hover:scale-105">
          Book a demo
        </button>
      </div>
      
      <!-- Mockup Image / Graphic -->
      <div class="mt-16 w-full max-w-5xl rounded-xl border border-border bg-card/50 backdrop-blur shadow-2xl p-2 sm:p-4">
        <div class="aspect-[16/9] rounded-lg bg-muted overflow-hidden flex items-center justify-center relative">
          <!-- Glassmorphism overlay to look premium -->
          <div class="absolute inset-0 bg-gradient-to-br from-primary/10 to-transparent"></div>
          <p class="text-muted-foreground font-medium flex items-center gap-2">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6"><rect width="18" height="18" x="3" y="3" rx="2" ry="2"></rect><circle cx="9" cy="9" r="2"></circle><path d="m21 15-3.086-3.086a2 2 0 0 0-2.828 0L6 21"></path></svg>
            Interactive Dashboard Preview
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
