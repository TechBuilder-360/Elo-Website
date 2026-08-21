<template>
  <section id="features" class="w-full py-24 md:py-32 relative overflow-hidden">
    <!-- Subtle background gradient -->
    <div class="absolute inset-0 bg-gradient-to-b from-background via-secondary/20 to-background pointer-events-none"></div>

    <div class="container mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
      <!-- Header -->
      <div class="text-center max-w-3xl mx-auto mb-16">
        <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full border border-primary/30 bg-primary/10 text-primary text-xs font-semibold tracking-wide mb-5">
          Everything You Need
        </div>
        <h2 class="text-4xl md:text-5xl font-extrabold tracking-tight text-foreground mb-4">
          Built for modern businesses
        </h2>
        <p class="text-lg text-muted-foreground leading-relaxed">
          ELO provides every financial tool a growing business needs — in a single, beautifully designed platform.
        </p>
      </div>

      <!-- Feature Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div v-for="(feature, i) in features" :key="i"
          class="group relative flex flex-col p-6 rounded-2xl border border-border bg-card hover:border-primary/40 hover:shadow-lg hover:shadow-primary/5 transition-all duration-300 overflow-hidden">
          <!-- Background glow on hover -->
          <div class="absolute -right-6 -top-6 w-32 h-32 bg-primary/10 rounded-full blur-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>

          <!-- Icon -->
          <div class="mb-5 w-11 h-11 rounded-xl bg-primary/10 flex items-center justify-center text-primary shrink-0 group-hover:bg-primary/20 transition-colors">
            <component :is="feature.icon" class="w-5 h-5" />
          </div>

          <!-- Content -->
          <h3 class="text-base font-semibold text-foreground mb-2">{{ feature.title }}</h3>
          <p class="text-sm text-muted-foreground leading-relaxed">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import {
  Wallet, ShieldCheck, BarChart3, Globe, Building2, Zap, FileText, Users, Lock
} from 'lucide-vue-next'

const features = [
  {
    icon: Wallet,
    title: 'Multi-Currency Wallet',
    description: 'Manage fiat and crypto assets in a single unified wallet. Send, receive, and swap across borders in real-time with competitive rates.',
  },
  {
    icon: ShieldCheck,
    title: 'Automated Compliance (KYB)',
    description: 'Stay fully compliant without the paperwork. Our automated KYB/KYC process verifies your business identity and documents in minutes.',
  },
  {
    icon: BarChart3,
    title: 'Real-Time Analytics',
    description: 'Track business performance, customer growth, and revenue trends with beautiful, interactive dashboards updated in real-time.',
  },
  {
    icon: Globe,
    title: 'Global Payments',
    description: 'Accept and send payments across 100+ countries. Support for local payment methods, international wire transfers, and crypto payouts.',
  },
  {
    icon: Building2,
    title: 'Multi-Business Management',
    description: 'Manage multiple business entities under a single account. Switch between businesses, track finances, and control access with ease.',
  },
  {
    icon: Zap,
    title: 'Instant Settlements',
    description: 'Say goodbye to 3-5 day bank delays. ELO settles your transactions instantly, so your cash flow stays healthy and predictable.',
  },
  {
    icon: FileText,
    title: 'Document Management',
    description: 'Upload, store, and manage compliance documents securely. Track document status, expiry dates, and approval workflows all in one place.',
  },
  {
    icon: Users,
    title: 'Team Access Control',
    description: 'Invite team members and assign custom roles. Control who can view, approve, or initiate financial transactions.',
  },
  {
    icon: Lock,
    title: 'Enterprise-Grade Security',
    description: 'Protected by end-to-end encryption, two-factor authentication, and advanced fraud monitoring to keep your business safe.',
  },
]
</script>
