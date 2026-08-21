<template>
  <div class="min-h-screen bg-background text-foreground">
    <Navbar />

    <main class="pt-16">
      <!-- Hero Section -->
      <section class="relative py-24 md:py-32 overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-b from-primary/10 via-background to-background pointer-events-none"></div>
        <div class="absolute top-1/4 right-0 w-96 h-96 bg-primary/10 rounded-full blur-3xl opacity-40"></div>

        <div class="container mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
          <div class="max-w-3xl">
            <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full border border-primary/30 bg-primary/10 text-primary text-xs font-semibold tracking-wide mb-8">
              Our Story
            </div>
            <h1 class="text-5xl md:text-6xl font-extrabold tracking-tight text-foreground mb-6 leading-tight">
              We're building the financial OS for
              <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-primary/60"> tomorrow's businesses</span>
            </h1>
            <p class="text-xl text-muted-foreground leading-relaxed">
              ELO Business was founded on a single belief: that every business — regardless of size or location — deserves access to world-class financial infrastructure. We're changing that, one transaction at a time.
            </p>
          </div>
        </div>
      </section>

      <!-- Mission Section -->
      <section class="py-16 md:py-24 bg-secondary/20">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-20 items-center">
            <div>
              <h2 class="text-3xl md:text-4xl font-extrabold tracking-tight text-foreground mb-6">
                Our Mission
              </h2>
              <p class="text-base text-muted-foreground leading-relaxed mb-4">
                Global financial infrastructure has historically been complex, expensive, and inaccessible to most businesses. Banks move slowly, compliance is a nightmare, and international payments are riddled with hidden fees.
              </p>
              <p class="text-base text-muted-foreground leading-relaxed mb-4">
                ELO Business exists to fix this. We've built a platform that combines business wallets, automated compliance, real-time analytics, and global payment rails into one beautifully designed product that any business can use from day one.
              </p>
              <p class="text-base text-muted-foreground leading-relaxed">
                We believe that financial access is a competitive advantage — and we're determined to make it available to everyone.
              </p>
            </div>
            <div class="rounded-2xl overflow-hidden border border-border shadow-xl shadow-black/10">
              <img src="/team_photo.png" alt="The ELO Business Team" class="w-full h-full object-cover" />
            </div>
          </div>
        </div>
      </section>

      <!-- Values Section -->
      <section class="py-16 md:py-24">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="text-center max-w-2xl mx-auto mb-14">
            <h2 class="text-3xl md:text-4xl font-extrabold tracking-tight text-foreground mb-4">Our Core Values</h2>
            <p class="text-lg text-muted-foreground">These principles guide every decision we make at ELO.</p>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
            <div v-for="(value, i) in values" :key="i"
              class="p-6 rounded-2xl border border-border bg-card hover:border-primary/40 hover:shadow-lg hover:shadow-primary/5 transition-all duration-300">
              <div class="w-10 h-10 rounded-xl bg-primary/10 flex items-center justify-center mb-4 text-primary">
                <component :is="value.icon" class="w-5 h-5" />
              </div>
              <h3 class="text-base font-bold text-foreground mb-2">{{ value.title }}</h3>
              <p class="text-sm text-muted-foreground leading-relaxed">{{ value.description }}</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Stats Section -->
      <Stats />

      <!-- Team Section -->
      <section class="py-16 md:py-24 bg-secondary/20">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="text-center max-w-2xl mx-auto mb-14">
            <h2 class="text-3xl md:text-4xl font-extrabold tracking-tight text-foreground mb-4">Meet the Team</h2>
            <p class="text-lg text-muted-foreground">
              We're a team of fintech veterans, engineers, and compliance specialists passionate about democratizing business finance.
            </p>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <div v-for="(member, i) in team" :key="i"
              class="flex flex-col items-center text-center p-8 rounded-2xl border border-border bg-card hover:border-primary/40 hover:shadow-lg hover:shadow-primary/5 transition-all">
              <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-primary/30 to-primary/10 flex items-center justify-center mb-4 text-2xl font-extrabold text-primary">
                {{ member.initials }}
              </div>
              <h3 class="text-base font-bold text-foreground">{{ member.name }}</h3>
              <p class="text-sm text-primary font-medium mt-0.5">{{ member.role }}</p>
              <p class="text-sm text-muted-foreground leading-relaxed mt-3">{{ member.bio }}</p>
            </div>
          </div>
        </div>
      </section>

      <!-- CTA -->
      <CTA />
    </main>

    <Footer />
  </div>
</template>

<script setup>
import { ShieldCheck, Zap, Globe, Heart } from 'lucide-vue-next'

useHead({
  title: 'About Us — ELO Business',
  meta: [
    { name: 'description', content: 'Learn about ELO Business, our mission to democratize global financial infrastructure, our core values, and the team behind the platform.' },
    { name: 'robots', content: 'index, follow' },
  ],
})

const values = [
  {
    icon: ShieldCheck,
    title: 'Trust & Security',
    description: 'We hold your financial data and assets to the highest standard of protection and transparency.',
  },
  {
    icon: Zap,
    title: 'Speed & Simplicity',
    description: 'Complex financial operations should feel effortless. We obsess over making things fast and intuitive.',
  },
  {
    icon: Globe,
    title: 'Global Accessibility',
    description: 'We believe great financial tools should be available to businesses anywhere in the world.',
  },
  {
    icon: Heart,
    title: 'Customer-First',
    description: 'Every product decision starts and ends with what creates genuine value for our customers.',
  },
]

const team = [
  {
    initials: 'AJ',
    name: 'Adebayo Johnson',
    role: 'Co-Founder & CEO',
    bio: '15+ years in fintech and banking. Former VP at Flutterwave. Passionate about building inclusive financial tools for African businesses.',
  },
  {
    initials: 'EA',
    name: 'Emeka Asante',
    role: 'Co-Founder & CTO',
    bio: 'Full-stack engineer and systems architect. Previously built payment infrastructure at Paystack serving millions of users.',
  },
  {
    initials: 'NK',
    name: 'Nkem Okafor',
    role: 'Head of Compliance',
    bio: 'Compliance and AML specialist with deep expertise in KYB processes, financial regulation, and cross-border payment law.',
  },
  {
    initials: 'ZA',
    name: 'Zainab Aliyu',
    role: 'Head of Product',
    bio: 'Product designer turned PM. Specializes in complex financial UX — making hard workflows feel simple and intuitive.',
  },
  {
    initials: 'CO',
    name: 'Chukwudi Onwudiwe',
    role: 'Head of Partnerships',
    bio: 'Builds the bridges. Manages strategic relationships with banks, regulators, and payment rails across 40+ countries.',
  },
  {
    initials: 'FA',
    name: 'Funmi Adeola',
    role: 'Head of Customer Success',
    bio: 'Ensures every business on ELO thrives. Leads onboarding, support, and growth programs for our merchant community.',
  },
]
</script>
