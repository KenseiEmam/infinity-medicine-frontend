<template>
  <div class="relative">
    <!-- HERO -->
    <main v-reveal="'down'" class="py-12 container md:py-20">
      <div class="max-w-4xl mx-auto">
        <div class="text-center space-y-4 mb-12">
          <div class="flex justify-center">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="lucide lucide-calendar-check h-12 w-12 text-primary"
            >
              <path d="M8 2v4"></path>
              <path d="M16 2v4"></path>
              <rect width="18" height="18" x="3" y="4" rx="2"></rect>
              <path d="M3 10h18"></path>
              <path d="m9 16 2 2 4-4"></path>
            </svg>
          </div>
          <h1 class="text-4xl font-bold tracking-tight md:text-5xl">Book a Demo</h1>
          <p class="text-lg text-infin-secondary max-w-2xl mx-auto leading-relaxed">
            Select your preferred date and we'll contact you to schedule a personalized
            demonstration of our medical devices.
          </p>
        </div>
        <div
          data-slot="card"
          class="bg-card text-infin flex flex-col gap-6 rounded-xl border py-6 shadow-sm max-w-2xl mx-auto"
        >
          <div
            data-slot="card-header"
            class="@container/card-header grid auto-rows-min grid-rows-[auto_auto] items-start gap-2 px-6 has-data-[slot=card-action]:grid-cols-[1fr_auto] [.border-b]:pb-6"
          >
            <div data-slot="card-title" class="leading-none font-semibold">Select a Date</div>
            <div data-slot="card-description" class="text-infin-secondary text-sm">
              Choose one day for your demo appointment. Our team will reach out to confirm the exact
              time.
            </div>
          </div>
          <div data-slot="card-content" class="px-6 space-y-6">
            <div class="flex justify-center">
              <div class="w-auto">
                <VueDatePicker
                  class="mx-auto"
                  inline
                  :time-config="{ enableTimePicker: false }"
                  auto-apply
                  v-model="date"
                ></VueDatePicker>
              </div>
            </div>
            <div v-if="interest" class="bg-infin/5 border border-infin/20 rounded-lg p-4">
              <p class="text-sm">
                <span class="font-semibold">Demo Product:</span>
                {{ interest }}
              </p>
            </div>
            <button
              @click="routeQuote"
              class="btn-lg w-full disabled:opacity-40 disabled:cursor-default disabled:hover:bg-infin/40 disabled:bg-infin/40"
              :disabled="!date"
            >
              Continue to Contact Information
            </button>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { useRoute } from 'vue-router'
import { VueDatePicker } from '@vuepic/vue-datepicker'
import '@vuepic/vue-datepicker/dist/main.css'
import router from '@/router'
const date = ref<Date | null>(null)
const route = useRoute()
const interest = ref(route.query.interest || '')
function routeQuote() {
  let link = '/quote?demo=' + date.value
  if (interest.value) link += '&interest=' + interest.value
  console.log(link)
  router.push(link)
}
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
