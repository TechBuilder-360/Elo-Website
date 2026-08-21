<template>
  <section id="pricing" class="w-full py-24 md:py-32">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center max-w-3xl mx-auto mb-16">
        <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full border border-primary/30 bg-primary/10 text-primary text-xs font-semibold tracking-wide mb-5">
          Transparent Pricing
        </div>
        <h2 class="text-4xl md:text-5xl font-extrabold tracking-tight text-foreground mb-4">
          Simple, honest pricing
        </h2>
        <p class="text-lg text-muted-foreground">
          No hidden fees. No surprises. Scale as your business grows.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-5xl mx-auto">
        <div v-for="(plan, i) in plans" :key="i"
          :class="[
            'relative rounded-2xl p-8 flex flex-col border transition-all duration-300',
            plan.featured
              ? 'bg-primary text-primary-foreground border-primary shadow-2xl shadow-primary/30 scale-[1.03]'
              : 'bg-card border-border hover:border-primary/40 hover:shadow-lg hover:shadow-primary/5'
          ]">

          <!-- Popular Badge -->
          <div v-if="plan.featured"
            class="absolute -top-3.5 left-1/2 -translate-x-1/2 px-4 py-1 rounded-full bg-foreground text-background text-xs font-bold tracking-wide shadow">
            MOST POPULAR
          </div>

          <div class="mb-6">
            <h3 class="text-lg font-bold mb-1" :class="plan.featured ? 'text-primary-foreground' : 'text-foreground'">{{ plan.name }}</h3>
            <p class="text-sm mb-4" :class="plan.featured ? 'text-primary-foreground/80' : 'text-muted-foreground'">{{ plan.description }}</p>
            <div class="flex items-baseline gap-1">
              <span class="text-4xl font-extrabold" :class="plan.featured ? 'text-primary-foreground' : 'text-foreground'">{{ plan.price }}</span>
              <span v-if="plan.period" class="text-sm" :class="plan.featured ? 'text-primary-foreground/70' : 'text-muted-foreground'">/{{ plan.period }}</span>
            </div>
          </div>

          <ul class="space-y-3 mb-8 flex-1">
            <li v-for="(item, j) in plan.features" :key="j" class="flex items-start gap-2.5 text-sm">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"
                :class="plan.featured ? 'text-primary-foreground shrink-0 mt-0.5' : 'text-primary shrink-0 mt-0.5'">
                <polyline points="20 6 9 17 4 12"/>
              </svg>
              <span :class="plan.featured ? 'text-primary-foreground/90' : 'text-muted-foreground'">{{ item }}</span>
            </li>
          </ul>

          <a :href="plan.href" target="_blank"
            :class="[
              'w-full text-center py-3 rounded-xl font-semibold text-sm transition-all',
              plan.featured
                ? 'bg-primary-foreground text-primary hover:opacity-90'
                : 'bg-primary text-primary-foreground hover:bg-primary/90 shadow-md shadow-primary/20'
            ]">
            {{ plan.cta }}
          </a>
        </div>
      </div>

      <p class="text-center text-sm text-muted-foreground mt-8">
        All plans include a 14-day free trial. No credit card required to start.
      </p>
    </div>
  </section>
</template>

<script setup>
const plans = [
  {
    name: 'Starter',
    description: 'Perfect for freelancers and early-stage startups.',
    price: 'Free',
    period: null,
    featured: false,
    cta: 'Get Started',
    href: 'https://eloweb.netlify.app/signup',
    features: [
      '1 business entity',
      'Fiat wallet (USD, EUR, GBP)',
      'Up to $5,000 monthly volume',
      'Basic KYB verification',
      'Transaction history & exports',
      'Email support',
    ],
  },
  {
    name: 'Growth',
    description: 'For growing teams who need more power.',
    price: '$49',
    period: 'month',
    featured: true,
    cta: 'Start Free Trial',
    href: 'https://eloweb.netlify.app/signup',
    features: [
      'Up to 5 business entities',
      'Fiat + Crypto wallets',
      'Up to $100,000 monthly volume',
      'Automated KYB + document storage',
      'Full analytics dashboard',
      'Instant settlements',
      'Priority email & chat support',
    ],
  },
  {
    name: 'Enterprise',
    description: 'Custom solutions for large-scale operations.',
    price: 'Custom',
    period: null,
    featured: false,
    cta: 'Contact Sales',
    href: 'mailto:hello@elobusiness.com',
    features: [
      'Unlimited business entities',
      'All currencies + crypto',
      'Unlimited monthly volume',
      'Custom KYB workflows',
      'Dedicated compliance manager',
      'API access & webhooks',
      '24/7 dedicated support',
    ],
  },
]
</script>
