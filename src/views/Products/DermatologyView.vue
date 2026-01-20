<template>
  <div class="relative">
    <!-- HERO -->
    <section
      v-reveal="'up'"
      class="relative overflow-hidden border-b border-infin-teritiary/30 dark:border-infin/30 bg-background py-16 md:py-24"
    >
      <div
        class="absolute inset-0 bg-gradient-to-b dark:bg-infin dark:bg-none from-infin/5 via-background to-background"
      ></div>
      <div
        class="absolute inset-y-0 left-1/2 hidden w-[60rem] -translate-x-1/2 rounded-full bg-infin/5 blur-3xl md:block"
      ></div>

      <div class="container relative">
        <div class="mx-auto max-w-4xl space-y-6 text-center">
          <span
            class="inline-flex items-center text-infin dark:text-white justify-center rounded-md border px-2 py-0.5 text-xs font-medium whitespace-nowrap shrink-0 border-transparent bg-secondary text-secondary-foreground mx-auto w-fit uppercase tracking-wider"
          >
            Dermatology Department
          </span>

          <h1 class="text-infin dark:text-white text-4xl font-bold tracking-tight md:text-5xl">
            Advanced Dermatology Systems for Clinical Excellence
          </h1>

          <p class="text-lg text-infin-secondary dark:text-gray-400 leading-relaxed">
            High-performance laser, RF, and regenerative technologies engineered for aesthetic,
            medical, and procedural dermatology with consistent, reproducible outcomes.
          </p>

          <div class="flex flex-col gap-3 sm:flex-row sm:justify-center">
            <a class="btn-lg" href="/quote">Request a Consultation</a>
            <a class="btn-lg-outline" href="/products">Explore All Devices</a>
          </div>

          <div class="flex flex-col items-center gap-2 text-sm text-infin-secondary">
            <span>
              Discover our aesthetic platforms, energy-based systems, and regenerative protocols.
            </span>
            <a
              href="#equipment"
              class="linktext text-xs text-infin dark:text-white hover:font-semibold"
            >
              Explore Dermatology Equipment
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- SPOTLIGHT -->
    <section
      v-reveal="'down'"
      class="relative dark:bg-infin-darkpribg bg-infin-pribg/20 py-16 md:py-24"
    >
      <div
        class="absolute inset-0 bg-gradient-to-br dark:bg-infin dark:bg-none from-infin/10 via-infin-pribg/30 to-background"
      ></div>

      <div class="container relative space-y-8">
        <div class="max-w-2xl space-y-4">
          <h2 class="text-3xl font-bold tracking-tight md:text-4xl text-infin dark:text-white">
            Spotlight Dermatology Devices
          </h2>
          <p class="text-lg text-infin-secondary dark:text-gray-400 leading-relaxed">
            Curated technologies supporting skin rejuvenation, pigmentation management, vascular
            treatments, and advanced aesthetic workflows.
          </p>
        </div>

        <div class="grid gap-6 md:grid-cols-2">
          <!-- Card 1 -->
          <div
            class="text-infin-secondary dark:text-gray-400 gap-6 rounded-xl border py-6 flex h-full flex-col border-infin-teritiary/30 dark:border-infin/30 bg-infin-secbg/85 dark:bg-infin-darksecbg/85 shadow-sm backdrop-blur transition-all duration-300 hover:-translate-y-1 hover:shadow-lg"
          >
          <div class="bg-infin-secbg  dark:bg-infin-darksecbg">
             <img class="h-24 md:h-36 2xl:h-44 mx-auto" src="https://res.cloudinary.com/dhm67jkou/image/upload/v1768536337/lavieen_f75dfd673e_33dd26455a.png" alt="">
          </div>

            <div class="grid auto-rows-min items-start gap-2 px-6">
              <div class="text-2xl font-semibold">Lavieen BB Laser</div>
            </div>

            <div class="px-6 flex flex-1 flex-col justify-between space-y-6">
              <p class="text-sm text-infin-secondary dark:text-gray-400 leading-relaxed">
                1927nm thulium laser platform delivering controlled skin resurfacing, tone
                correction, and collagen stimulation with minimal downtime.
              </p>
              <a class="btn-lg-outline" href="/products/lavieen"> View Device </a>
            </div>
          </div>

          <!-- Card 2 -->
          <div
            class="text-infin-secondary dark:text-gray-400 gap-6 rounded-xl border py-6 flex h-full flex-col border-infin-teritiary/30 dark:border-infin/30 bg-infin-secbg/85 dark:bg-infin-darksecbg/85 shadow-sm backdrop-blur transition-all duration-300 hover:-translate-y-1 hover:shadow-lg"
          >
           <div class="bg-infin-secbg  dark:bg-infin-darksecbg">
             <img class="h-24 md:h-36 2xl:h-44 mx-auto" src="https://res.cloudinary.com/dhm67jkou/image/upload/v1768536098/virtue_rf_346c031aa6_5f712a335e.png" alt="">
          </div>
            <div class="grid auto-rows-min items-start gap-2 px-6">
              <div class="text-2xl font-semibold">Virtue RF</div>
            </div>

            <div class="px-6 flex flex-1 flex-col justify-between space-y-6">
              <p class="text-sm text-infin-secondary dark:text-gray-400 leading-relaxed">
                RF microneedling system designed for dermal remodeling, scar revision, and skin
                tightening across all skin types.
              </p>
              <a class="btn-lg-outline" href="/products/virtue-rf"> View Device </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- FUTURE TRICHOLOGY PLACEHOLDER -->
    <section v-reveal="'right'" class="py-16 md:py-24">
      <div id="trichology" class="container text-center max-w-3xl mx-auto space-y-4">
        <h2 class="text-3xl font-bold tracking-tight md:text-4xl text-infin dark:text-white">
          Trichology Solutions
        </h2>
        <p class="text-lg text-infin-secondary dark:text-gray-400 leading-relaxed">
          Dedicated technologies and treatment protocols for hair restoration, scalp health, and
          regenerative trichology.
        </p>
        <div class="py-4">
          <a
                href="https://mega.nz/file/JAFjFChY#p2v91hBcT0clr82A-JOt1BKKJVMxuwjfvrWb7BcTUmQ"
                target="_blank"
                class="btn-lg"
                >View Documents</a
              >
        </div>
        <div class="grid gap-4 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
          <div
            v-for="eq in consumables"
            :key="eq.slug"
            class="text-infin-secondary dark:text-gray-400 gap-6 rounded-xl py-6 flex h-full flex-col overflow-hidden border border-infin-teritiary/30 dark:border-infin/30 bg-infin-secbg dark:bg-infin-darksecbg shadow-sm transition-shadow hover:shadow-md"
          >
            <div class="aspect-square bg-infin-secbg dark:bg-infin-darksecbg">
              <img :alt="eq.name" class="h-full w-full object-cover max-h-64" :src="eq.photo" />
            </div>
            <div class="flex flex-1 flex-col justify-between space-y-4 p-4">
              <div class="space-y-2">
                <h3 class="text-base font-semibold">{{ eq.name }}</h3>
                <p
                  class="text-xs text-infin-secondary dark:text-gray-400 line-clamp-4 leading-relaxed md:text-sm"
                >
                  {{ eq.description }}
                </p>
              </div>
              <RouterLink
                v-if="eq.department === 'dermatology'"
                :to="'products/' + eq.slug"
                class="w-full btn-lg-outline text-center block"
              >
                Learn More
              </RouterLink>
              <a class="btn-lg" :href="'/quote?interest=' + eq.slug">Request Quote</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ELEVATE -->
    <section v-reveal="'left'" class="py-16 container md:py-24">
      <div class="max-w-3xl mx-auto space-y-6 text-center">
        <h2 class="text-3xl font-bold tracking-tight md:text-4xl text-infin dark:text-white">
          Elevate Your Dermatology Practice
        </h2>
        <p class="text-lg text-infin-secondary dark:text-gray-400 leading-relaxed">
          Partner with Infinity Medicals for advanced dermatology platforms, clinical training, and
          long-term technical support tailored to your practice.
        </p>
        <a class="btn-lg" href="/demo">Book a Demo</a>
      </div>
    </section>

    <!-- Products -->
    <section
      v-reveal="'right'"
      class="relative dark:bg-infin-darkpribg bg-infin-pribg/20 py-16 md:py-24"
    >
      <div
        class="absolute inset-0 bg-gradient-to-b dark:bg-infin dark:bg-none from-background via-infin-pribg/20 to-background"
      ></div>
      <div id="equipment" class="container relative space-y-10">
        <div
          class="bg-infin-secbg dark:bg-infin-darksecbg text-infin-secondary dark:text-gray-400 flex flex-col gap-6 rounded-xl border py-6 shadow-sm scroll-mt-32"
          id="diagnostic-equipment"
        >
          <div
            class="@container/card-header gap-2 px-6 flex items-center justify-between [.border-b]:pb-6"
          >
            <div class="text-2xl font-semibold">Dermatology Equipment</div>
             <a
                href="https://mega.nz/file/REtiFByC#2AnySvsXUR2f_OkSbVcrHbgDJ6D0Ce1JadCHmNzioV4"
                target="_blank"
                class="btn-lg"
                >View Documents</a
              >
          </div>

          <div
            class="px-6 space-y-4 text-sm text-infin-secondary dark:text-gray-400 leading-relaxed"
          >
            <p>
              Advanced dermatology platforms including laser systems, RF technologies, and
              energy-based devices designed for aesthetic, medical, and procedural skin treatments.
            </p>

            <ProductScroller :products-list="equipment" />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
import ProductScroller from '@/components/ProductScroller.vue'
import { useProductStore } from '@/stores/productStore'
// import FaqList from '@/components/FaqList.vue'
import { computed, onMounted } from 'vue'
const productStore = useProductStore()

onMounted(async () => {
  productStore.fetchDermatology()
})
const equipment = computed(() => {
  return productStore.dermatology.filter((s) => s.type === 'equipment')
})
const consumables = computed(() => {
  return productStore.dermatology.filter((s) => s.type === 'consumable')
})

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
