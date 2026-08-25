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
              Our Vision &amp; Mission
            </div>
            <h1 class="text-5xl md:text-6xl font-extrabold tracking-tight text-foreground mb-6 leading-tight">
              Revolutionising advertising through
              <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-primary/60"> market-led excellence</span>
            </h1>
            <p class="text-xl text-muted-foreground leading-relaxed">
              ELO aims to revolutionise the advertising industry through effective advertising (market-led) of products that meet standardisation, ranging from money spent to services rendered and an accurate return on investment for every client and a brand lift.
            </p>
          </div>
        </div>
      </section>

      <!-- Core Execution Pillars Section -->
      <section class="py-16 md:py-24 bg-secondary/20 border-y border-border">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-20 items-center">
            <div>
              <h2 class="text-3xl md:text-4xl font-extrabold tracking-tight text-foreground mb-6">
                How We Deliver Value
              </h2>
              <p class="text-base text-muted-foreground leading-relaxed mb-8">
                To fulfill our commitment to standardisation, financial clarity, and measurable brand growth, ELO executes through four foundational pillars:
              </p>

              <div class="space-y-4">
                <div v-for="(pillar, i) in executionPillars" :key="i"
                  class="flex items-start gap-4 p-4 rounded-xl border border-border/80 bg-card/60 backdrop-blur-sm hover:border-primary/40 transition-all">
                  <div class="w-10 h-10 rounded-lg bg-primary/10 text-primary flex items-center justify-center shrink-0 mt-0.5">
                    <component :is="pillar.icon" class="w-5 h-5" />
                  </div>
                  <div>
                    <h3 class="text-base font-bold text-foreground">{{ pillar.title }}</h3>
                    <p class="text-sm text-muted-foreground mt-1 leading-relaxed">{{ pillar.description }}</p>
                  </div>
                </div>
              </div>
            </div>

            <div class="rounded-2xl overflow-hidden border border-border shadow-xl shadow-black/10">
              <img src="/team_photo.png" alt="The ELO Team" class="w-full h-full object-cover" />
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
              We're a team of industry leaders, engineers, and specialists passionate about market-led growth and business infrastructure.
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
import { ShieldCheck, Zap, Globe, Heart, TrendingUp, Megaphone, Image, CheckCircle2 } from 'lucide-vue-next'

useHead({
  title: 'About Us — ELO',
  meta: [
    { name: 'description', content: 'ELO aims to revolutionise the advertising industry through effective market-led advertising, standardisation, and accurate ROI.' },
    { name: 'robots', content: 'index, follow' },
  ],
})

const executionPillars = [
  {
    icon: TrendingUp,
    title: 'Increased Sales',
    description: 'Drive direct revenue expansion through targeted campaigns and optimized ad conversions.',
  },
  {
    icon: Megaphone,
    title: 'Boost Brand Awareness',
    description: 'Maximize audience reach and brand recall across key target demographics.',
  },
  {
    icon: Image,
    title: 'Improve Images via Ads',
    description: 'Enhance brand perception with standardized, premium ad creative and messaging.',
  },
  {
    icon: CheckCircle2,
    title: 'Build Loyalty via Verification',
    description: 'Ensure customers are thoroughly satisfied with verified services and products, fostering long-term brand trust.',
  },
]

const values = [
  {
    icon: ShieldCheck,
    title: 'Trust & Security',
    description: 'We hold your financial data and campaigns to the highest standard of protection and transparency.',
  },
  {
    icon: Zap,
    title: 'Speed & Simplicity',
    description: 'Complex marketing and financial workflows are streamlined to feel completely intuitive.',
  },
  {
    icon: Globe,
    title: 'Global Reach',
    description: 'Empowering brands to connect with customers across borders seamlessly.',
  },
  {
    icon: Heart,
    title: 'Customer-First ROI',
    description: 'Every campaign and tool is designed to deliver verified value and tangible return on investment.',
  },
]

const team = [
  {
    initials: 'AJ',
    name: 'Adebayo Johnson',
    role: 'Co-Founder & CEO',
    bio: '15+ years in advertising and fintech. Passionate about building market-led tools for growing businesses.',
  },
  {
    initials: 'EA',
    name: 'Emeka Asante',
    role: 'Co-Founder & CTO',
    bio: 'Full-stack engineer and systems architect. Built high-scale platforms serving millions of users.',
  },
  {
    initials: 'NK',
    name: 'Nkem Okafor',
    role: 'Head of Compliance & Verification',
    bio: 'Specialist in business verification, merchant trust, and standardized service quality assurance.',
  },
  {
    initials: 'ZA',
    name: 'Zainab Aliyu',
    role: 'Head of Product',
    bio: 'Product manager focused on ROI tracking, user experience, and ad platform optimization.',
  },
  {
    initials: 'CO',
    name: 'Chukwudi Onwudiwe',
    role: 'Head of Growth',
    bio: 'Drives brand lift and market penetration strategies for client portfolios.',
  },
  {
    initials: 'FA',
    name: 'Funmi Adeola',
    role: 'Head of Customer Success',
    bio: 'Ensures client satisfaction across all campaign touchpoints and verification processes.',
  },
]
</script>
