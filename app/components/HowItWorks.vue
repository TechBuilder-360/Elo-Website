<template>
  <section id="how-it-works" class="w-full py-24 md:py-32 bg-secondary/20">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center max-w-3xl mx-auto mb-16">
        <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full border border-primary/30 bg-primary/10 text-primary text-xs font-semibold tracking-wide mb-5">
          Simple Onboarding
        </div>
        <h2 class="text-4xl md:text-5xl font-extrabold tracking-tight text-foreground mb-4">
          Up and running in minutes
        </h2>
        <p class="text-lg text-muted-foreground">
          Getting started with ELO Business is fast, simple, and completely free.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 md:gap-12 relative">
        <!-- Connecting Line (desktop only) -->
        <div class="hidden md:block absolute top-10 left-1/6 right-1/6 h-px bg-gradient-to-r from-transparent via-border to-transparent"></div>

        <div v-for="(step, i) in steps" :key="i" class="flex flex-col items-center text-center relative">
          <!-- Step Number -->
          <div class="w-20 h-20 rounded-2xl bg-primary/10 border border-primary/20 flex items-center justify-center mb-5 relative z-10 shadow-lg shadow-primary/5">
            <component :is="step.icon" class="w-8 h-8 text-primary" />
            <span class="absolute -top-2 -right-2 w-6 h-6 rounded-full bg-primary text-primary-foreground text-xs font-bold flex items-center justify-center shadow">{{ i + 1 }}</span>
          </div>
          <h3 class="text-lg font-bold text-foreground mb-2">{{ step.title }}</h3>
          <p class="text-sm text-muted-foreground leading-relaxed max-w-xs">{{ step.description }}</p>
        </div>
      </div>

      <div class="text-center mt-14">
        <a href="https://eloweb.netlify.app/signup" target="_blank"
          class="inline-flex items-center gap-2.5 px-8 py-3.5 rounded-xl bg-primary text-primary-foreground font-semibold text-base hover:bg-primary/90 transition-all shadow-xl shadow-primary/25 hover:-translate-y-0.5">
          Create Free Account
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M5 12h14"/><path d="m12 5 7 7-7 7"/></svg>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { UserPlus, Building2, Rocket } from 'lucide-vue-next'

const steps = [
  {
    icon: UserPlus,
    title: 'Create Your Account',
    description: 'Sign up in under 2 minutes. No credit card required. Start with your email and a secure password.',
  },
  {
    icon: Building2,
    title: 'Register Your Business',
    description: 'Add your business details and upload compliance documents. Our automated KYB process handles the rest.',
  },
  {
    icon: Rocket,
    title: 'Start Transacting',
    description: 'Fund your wallet, send payments globally, track analytics, and grow your business — all from one dashboard.',
  },
]
</script>
