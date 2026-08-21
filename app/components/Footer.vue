<template>
  <footer class="w-full border-t border-border bg-background">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8 py-14">
      <div class="grid grid-cols-2 md:grid-cols-5 gap-10">
        <!-- Brand Column -->
        <div class="col-span-2 space-y-5">
          <div class="flex items-center gap-2.5">
            <div class="w-8 h-8 rounded-lg bg-primary flex items-center justify-center overflow-hidden shadow-md shadow-primary/20">
              <img src="/favicon_io/favicon_io/apple-touch-icon.png" alt="ELO" class="w-full h-full object-cover" />
            </div>
            <span class="text-lg font-bold tracking-tight text-foreground">ELO Business</span>
          </div>
          <p class="text-sm text-muted-foreground leading-relaxed max-w-xs">
            The next-generation financial infrastructure for ambitious businesses. Built for the modern global economy.
          </p>
          <div class="flex items-center gap-3">
            <a href="#" aria-label="Twitter/X" class="w-8 h-8 rounded-lg bg-muted flex items-center justify-center text-muted-foreground hover:text-foreground hover:bg-accent transition-colors">
              <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
            </a>
            <a href="#" aria-label="LinkedIn" class="w-8 h-8 rounded-lg bg-muted flex items-center justify-center text-muted-foreground hover:text-foreground hover:bg-accent transition-colors">
              <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
            </a>
            <a href="#" aria-label="Instagram" class="w-8 h-8 rounded-lg bg-muted flex items-center justify-center text-muted-foreground hover:text-foreground hover:bg-accent transition-colors">
              <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect width="20" height="20" x="2" y="2" rx="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/></svg>
            </a>
          </div>
        </div>

        <!-- Links -->
        <div v-for="(col, i) in columns" :key="i" class="space-y-4">
          <h4 class="text-sm font-semibold text-foreground">{{ col.title }}</h4>
          <ul class="space-y-2.5">
            <li v-for="(link, j) in col.links" :key="j">
              <component :is="link.external ? 'a' : 'NuxtLink'"
                :href="link.href" :to="link.href"
                :target="link.external ? '_blank' : undefined"
                class="text-sm text-muted-foreground hover:text-foreground transition-colors">
                {{ link.label }}
              </component>
            </li>
          </ul>
        </div>
      </div>

      <!-- Bottom -->
      <div class="mt-12 pt-6 border-t border-border flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-muted-foreground">
        <p>© {{ new Date().getFullYear() }} ELO Business. All rights reserved.</p>
        <div class="flex items-center gap-4">
          <span class="flex items-center gap-1.5">
            <span class="w-1.5 h-1.5 rounded-full bg-green-500 animate-pulse"></span>
            All systems operational
          </span>
          <NuxtLink to="/policy" class="hover:text-foreground transition-colors">Privacy Policy</NuxtLink>
          <NuxtLink to="/policy" class="hover:text-foreground transition-colors">Terms of Service</NuxtLink>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
const columns = [
  {
    title: 'Product',
    links: [
      { label: 'Features', href: '/#features' },
      { label: 'Pricing', href: '/#pricing' },
      { label: 'How It Works', href: '/#how-it-works' },
      { label: 'Sign In', href: 'https://eloweb.netlify.app/', external: true },
    ],
  },
  {
    title: 'Company',
    links: [
      { label: 'About Us', href: '/about' },
      { label: 'Blog', href: '#' },
      { label: 'Careers', href: '#' },
      { label: 'Contact', href: '#' },
    ],
  },
  {
    title: 'Legal',
    links: [
      { label: 'Privacy Policy', href: '/policy' },
      { label: 'Terms of Service', href: '/policy' },
      { label: 'Cookie Policy', href: '/policy' },
      { label: 'Compliance', href: '/policy' },
    ],
  },
]
</script>
