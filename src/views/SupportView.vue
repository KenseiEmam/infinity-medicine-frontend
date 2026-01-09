<template>
  <div class="relative">
    <!-- CTA -->
    <section v-reveal="'up'" class="relative container overflow-hidden py-16 border-b">
      <div
        class="pointer-events-none absolute inset-0 -z-10 bg-gradient-to-br frominfin/10 via-infin-secbg to-/20"
      ></div>
      <div class="mx-auto relative max-w-4xl text-center space-y-6">
        <h2 class="text-3xl font-bold tracking-tight text-infin md:text-4xl">
          Frequently Asked Questions
        </h2>
        <p class="text-base text-infin-secondary leading-relaxed">
          Find answers to common questions about our products and services
        </p>
      </div>
    </section>
    <section v-reveal="'down'" class="relative container overflow-hidden py-16 border-b">
      <FaqList />
    </section>
  </div>
</template>

<script setup lang="ts">
import FaqList from '@/components/FaqList.vue'
const vReveal = {
  // eslint-disable-next-line @typescript-eslint/no-explicit-any
  mounted(el: HTMLElement, binding: any) {
    const direction = binding.value || 'up'
    el.classList.add('reveal', `reveal-${direction}`)

    const observer = new IntersectionObserver(
      ([entry]) => {
        if (entry && entry.isIntersecting) {
          el.classList.add('reveal-visible')
          observer.unobserve(el)
        }
      },
      { threshold: 0.15 },
    )

    observer.observe(el)
  },
}
</script>
