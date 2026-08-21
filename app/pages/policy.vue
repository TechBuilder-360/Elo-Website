<template>
  <div class="min-h-screen bg-background text-foreground">
    <Navbar />

    <main class="pt-16">
      <!-- Header -->
      <section class="py-16 md:py-24 border-b border-border relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-b from-primary/5 to-transparent pointer-events-none"></div>
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
          <div class="max-w-3xl">
            <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full border border-primary/30 bg-primary/10 text-primary text-xs font-semibold tracking-wide mb-6">
              Legal & Privacy
            </div>
            <h1 class="text-4xl md:text-5xl font-extrabold tracking-tight text-foreground mb-4">Privacy Policy &amp; Terms</h1>
            <p class="text-muted-foreground text-base">
              Last updated: {{ lastUpdated }} &nbsp;·&nbsp; Effective: {{ lastUpdated }}
            </p>
          </div>
        </div>
      </section>

      <!-- Content -->
      <section class="py-12 md:py-20">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8">
          <div class="flex flex-col lg:flex-row gap-12">

            <!-- Sticky Table of Contents -->
            <aside class="lg:w-60 shrink-0">
              <nav class="sticky top-24 space-y-1">
                <p class="text-xs font-semibold text-muted-foreground uppercase tracking-widest mb-3 px-3">On this page</p>
                <a v-for="section in sections" :key="section.id"
                  :href="`#${section.id}`"
                  class="block px-3 py-2 rounded-lg text-sm text-muted-foreground hover:text-foreground hover:bg-accent transition-colors">
                  {{ section.title }}
                </a>
              </nav>
            </aside>

            <!-- Policy Content -->
            <div class="flex-1 max-w-3xl space-y-12 text-sm text-muted-foreground leading-relaxed">

              <div id="introduction">
                <h2 class="text-2xl font-bold text-foreground mb-4">1. Introduction</h2>
                <p class="mb-3">Welcome to ELO Business ("ELO", "we", "us", or "our"). We are committed to protecting your personal information and your right to privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you use our platform and services.</p>
                <p>By accessing or using ELO Business, you agree to this Privacy Policy and our Terms of Service. If you do not agree, please discontinue use of our services immediately.</p>
              </div>

              <div id="information-we-collect">
                <h2 class="text-2xl font-bold text-foreground mb-4">2. Information We Collect</h2>
                <p class="mb-3">We collect information that you provide directly to us, information we collect automatically, and information from third parties.</p>
                <h3 class="text-base font-semibold text-foreground mt-5 mb-2">2.1 Information You Provide</h3>
                <ul class="list-disc list-outside pl-5 space-y-1.5">
                  <li>Account information: name, email address, password, phone number</li>
                  <li>Business information: company name, registration number, industry, business address</li>
                  <li>Identity documents: government-issued ID, proof of address (for KYB/KYC compliance)</li>
                  <li>Financial information: bank account details, transaction history</li>
                  <li>Communications: messages sent to our support team</li>
                </ul>
                <h3 class="text-base font-semibold text-foreground mt-5 mb-2">2.2 Automatically Collected Information</h3>
                <ul class="list-disc list-outside pl-5 space-y-1.5">
                  <li>Log data: IP addresses, browser type, pages visited, time spent</li>
                  <li>Device information: device type, operating system, unique device identifiers</li>
                  <li>Usage data: features used, actions taken within the platform</li>
                  <li>Cookies and tracking technologies</li>
                </ul>
              </div>

              <div id="how-we-use">
                <h2 class="text-2xl font-bold text-foreground mb-4">3. How We Use Your Information</h2>
                <p class="mb-3">We use the information we collect to:</p>
                <ul class="list-disc list-outside pl-5 space-y-1.5">
                  <li>Provide, operate, and maintain our services</li>
                  <li>Process transactions and send related notices</li>
                  <li>Verify your identity and comply with KYB/KYC legal requirements</li>
                  <li>Detect and prevent fraudulent, illegal, or unauthorized activity</li>
                  <li>Communicate with you about products, services, and promotions</li>
                  <li>Analyze usage to improve our platform and user experience</li>
                  <li>Comply with applicable laws and regulations</li>
                </ul>
              </div>

              <div id="data-sharing">
                <h2 class="text-2xl font-bold text-foreground mb-4">4. Data Sharing & Disclosure</h2>
                <p class="mb-3">We do not sell your personal information. We may share your information with:</p>
                <ul class="list-disc list-outside pl-5 space-y-1.5">
                  <li><strong class="text-foreground">Service providers</strong> — trusted third parties who assist us in operating our platform (payment processors, cloud providers, analytics)</li>
                  <li><strong class="text-foreground">Regulatory authorities</strong> — government or financial regulators when required by law</li>
                  <li><strong class="text-foreground">Business transfers</strong> — in connection with a merger, acquisition, or sale of assets</li>
                  <li><strong class="text-foreground">With your consent</strong> — in any other circumstances where you give us explicit permission</li>
                </ul>
              </div>

              <div id="data-security">
                <h2 class="text-2xl font-bold text-foreground mb-4">5. Data Security</h2>
                <p class="mb-3">We implement industry-standard security measures including:</p>
                <ul class="list-disc list-outside pl-5 space-y-1.5">
                  <li>256-bit AES encryption for data at rest</li>
                  <li>TLS 1.3 encryption for all data in transit</li>
                  <li>Multi-factor authentication (MFA) for account access</li>
                  <li>Regular security audits and penetration testing</li>
                  <li>Role-based access controls for all internal systems</li>
                </ul>
                <p class="mt-3">Despite these measures, no method of transmission over the internet is 100% secure. We cannot guarantee absolute security but will notify you promptly in the event of a data breach affecting your information.</p>
              </div>

              <div id="your-rights">
                <h2 class="text-2xl font-bold text-foreground mb-4">6. Your Rights</h2>
                <p class="mb-3">Depending on your jurisdiction, you may have the following rights regarding your personal data:</p>
                <ul class="list-disc list-outside pl-5 space-y-1.5">
                  <li><strong class="text-foreground">Access</strong> — request a copy of the personal data we hold about you</li>
                  <li><strong class="text-foreground">Rectification</strong> — request correction of inaccurate or incomplete data</li>
                  <li><strong class="text-foreground">Erasure</strong> — request deletion of your personal data ("right to be forgotten")</li>
                  <li><strong class="text-foreground">Portability</strong> — receive your data in a structured, machine-readable format</li>
                  <li><strong class="text-foreground">Restriction</strong> — request that we restrict processing of your data</li>
                  <li><strong class="text-foreground">Objection</strong> — object to processing based on legitimate interests</li>
                </ul>
                <p class="mt-3">To exercise any of these rights, contact us at <a href="mailto:privacy@elobusiness.com" class="text-primary hover:underline">privacy@elobusiness.com</a>.</p>
              </div>

              <div id="cookies">
                <h2 class="text-2xl font-bold text-foreground mb-4">7. Cookies</h2>
                <p class="mb-3">We use cookies and similar tracking technologies to enhance your experience. These include:</p>
                <ul class="list-disc list-outside pl-5 space-y-1.5">
                  <li><strong class="text-foreground">Essential cookies</strong> — required for the platform to function</li>
                  <li><strong class="text-foreground">Analytics cookies</strong> — help us understand how you use our platform</li>
                  <li><strong class="text-foreground">Preference cookies</strong> — remember your settings and preferences</li>
                </ul>
                <p class="mt-3">You can control cookie settings through your browser at any time. Disabling certain cookies may affect platform functionality.</p>
              </div>

              <div id="terms-of-service">
                <h2 class="text-2xl font-bold text-foreground mb-4">8. Terms of Service</h2>
                <p class="mb-3">By using ELO Business, you agree to the following terms:</p>
                <ul class="list-disc list-outside pl-5 space-y-2">
                  <li>You must be at least 18 years of age to create an account</li>
                  <li>You are responsible for maintaining the confidentiality of your account credentials</li>
                  <li>You agree not to use the platform for any unlawful purpose, including money laundering, terrorism financing, or fraud</li>
                  <li>You grant ELO a limited license to use your business information solely to provide the services</li>
                  <li>ELO reserves the right to suspend or terminate accounts that violate these terms</li>
                  <li>We may update these terms at any time. Continued use after updates constitutes acceptance</li>
                </ul>
              </div>

              <div id="contact">
                <h2 class="text-2xl font-bold text-foreground mb-4">9. Contact Us</h2>
                <p class="mb-4">If you have any questions about this Privacy Policy or Terms of Service, please contact us:</p>
                <div class="p-6 rounded-2xl border border-border bg-card space-y-2">
                  <p><strong class="text-foreground">ELO Business Ltd.</strong></p>
                  <p>Email: <a href="mailto:privacy@elobusiness.com" class="text-primary hover:underline">privacy@elobusiness.com</a></p>
                  <p>Support: <a href="mailto:support@elobusiness.com" class="text-primary hover:underline">support@elobusiness.com</a></p>
                  <p class="text-xs text-muted-foreground/70 pt-2">We aim to respond to all inquiries within 2 business days.</p>
                </div>
              </div>

            </div>
          </div>
        </div>
      </section>
    </main>

    <Footer />
  </div>
</template>

<script setup>
useHead({
  title: 'Privacy Policy & Terms of Service — ELO Business',
  meta: [
    { name: 'description', content: 'Read the ELO Business Privacy Policy and Terms of Service. Understand how we collect, use, and protect your data.' },
    { name: 'robots', content: 'index, follow' },
  ],
})

const lastUpdated = 'August 2026'

const sections = [
  { id: 'introduction', title: '1. Introduction' },
  { id: 'information-we-collect', title: '2. Information We Collect' },
  { id: 'how-we-use', title: '3. How We Use Your Info' },
  { id: 'data-sharing', title: '4. Data Sharing' },
  { id: 'data-security', title: '5. Data Security' },
  { id: 'your-rights', title: '6. Your Rights' },
  { id: 'cookies', title: '7. Cookies' },
  { id: 'terms-of-service', title: '8. Terms of Service' },
  { id: 'contact', title: '9. Contact Us' },
]
</script>
