<template>
  <div class="max-w-3xl mx-auto space-y-2">
    <div v-for="(faq, i) in faqs" :key="i" class="rounded-xl overflow-hidden shadow-sm">
      <button
        class="w-full flex text-sm justify-between items-center px-6 py-4 hover:bg-infin-secbg cursor-pointer font-semibold"
        @click="toggle(i)"
      >
        {{ faq.q }}
        <svg
          class="w-5 h-5 transition-transform"
          :class="{ 'rotate-180': open === i }"
          viewBox="0 0 24 24"
        >
          <path d="M19 9l-7 7-7-7" stroke="currentColor" fill="none" />
        </svg>
      </button>

      <div v-show="open === i" class="px-6 py-4 bg-infin-pribg text-sm text-infin-teritiary">
        {{ faq.a }}
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const open = ref<number | null>(null)

const toggle = (i: number): void => {
  open.value = open.value === i ? null : i
}

const faqs = [
  {
    q: 'What types of medical devices does Infinity Medicals offer?',
    a: 'Infinity Medicals specializes in energy-based medical technologies for dermatology and ophthalmology. Our product portfolio includes advanced laser systems, RF microneedling devices, plasma technology platforms, and innovative hair regrowth therapies',
  },
  {
    q: 'Do you provide training for your devices?',
    a: 'Yes, comprehensive training is included with all our devices. Our expert technical team provides installation support, hands-on training sessions, and ongoing educational resources to ensure practitioners can safely and effectively utilize our equipment.',
  },
  {
    q: 'What is your warranty and support policy?',
    a: 'All Infinity Medicals devices come with manufacturer warranties and comprehensive technical support. We offer installation assistance, maintenance services, and responsive customer support. Specific warranty terms vary by product and can be discussed during consultation.',
  },
  {
    q: 'How can I request a product demonstration?',
    a: 'You can request a demonstration by clicking the "Book a Demo" button on our website. Select your preferred date, provide your contact information, and our team will reach out to schedule a personalized demonstration of our devices at your convenience.',
  },
  {
    q: 'What countries do you serve?',
    a: 'We currently have offices in Kuwait (headquarters), Oman, and Egypt, with UAE operations coming soon. We serve medical professionals throughout the Middle East region and are expanding our global presence.',
  },
  {
    q: 'Are your devices ISO certified?',
    a: 'Yes, all Infinity Medicals devices meet rigorous international quality and safety standards, including ISO certifications. We comply with global medical device regulations to ensure the highest standards of safety and efficacy.',
  },
  {
    q: 'How do I get pricing information?',
    a: 'For pricing information, please submit a quote request through our website. Our sales team will provide you with detailed information about product pricing, financing options, and any current promotions based on your specific needs and location.',
  },
  {
    q: 'What is your refund policy?',
    a: 'We offer fair, transparent refund protections with every purchase. Specific refund terms and conditions are provided during the sales process and vary based on product and regional regulations. Your investment is protected with clear policies.',
  },
  {
    q: 'Do you offer financing options?',
    a: 'Yes, we work with various financing partners to help make our advanced medical technology accessible. Financing options and terms vary by region and can be discussed with our sales team during consultation.',
  },
  {
    q: 'How long does delivery and installation take?',
    a: 'Delivery and installation timelines vary based on your location and product selection. Generally, after order confirmation, delivery takes 2-6 weeks depending on region. Our technical team will schedule installation and training at your convenience.',
  },
]
</script>
