<template>
  <div class="group bg-white p-0 rounded-xl shadow-lg hover:shadow-2xl transition-all duration-300 border border-[#faf8f5] hover:border-[#d4952a]/30 relative overflow-hidden">
    <div class="absolute top-0 right-0 w-32 h-32 bg-[#d4952a]/5 rounded-full blur-2xl group-hover:bg-[#d4952a]/10 transition-all" />

    <div class="relative h-48 overflow-hidden">
      <img
        :src="image"
        :alt="title"
        class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
      />
      <div class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent" />
      
      <div class="absolute bottom-4 left-4 right-4">
        <span class="text-xs font-semibold tracking-wider uppercase text-[#faf8f5] bg-[#d4952a] px-3 py-1 rounded-full">
          {{ badge }}
        </span>
      </div>
    </div>

    <div class="p-6">
      <h3 class="font-serif text-2xl text-[#1a1a4e] mb-3 group-hover:text-[#d4952a] transition-colors">
        {{ title }}
      </h3>

      <p class="text-[#1a1a4e]/70 text-sm leading-relaxed mb-6">
        {{ description }}
      </p>

      <p class="text-[#d4952a] font-semibold text-lg mb-6">
        {{ price }}
      </p>

      <ul class="space-y-3 mb-8">
        <li
          v-for="feature in features"
          :key="feature"
          class="flex items-center gap-2 text-[#1a1a4e]/70 text-sm"
        >
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-[#d4952a] flex-shrink-0">
            <polyline points="20 6 9 17 4 12"></polyline>
          </svg>
          {{ feature }}
        </li>
      </ul>

      <NuxtLink
        to="/apply"
        class="inline-flex items-center gap-2 w-full justify-center px-6 py-3 bg-[#1a1a4e] hover:bg-[#d4952a] text-[#faf8f5] font-semibold rounded-lg transition-all duration-300"
      >
        {{ cta }}
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="group-hover:translate-x-1 transition-transform">
          <line x1="5" y1="12" x2="19" y2="12"></line>
          <polyline points="12 5 19 12 12 19"></polyline>
        </svg>
      </NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  icon: 'user' | 'users' | 'building'
  title: string
  description: string
  price: string
  cta: string
  badge: string
  features: string[]
}>()

const image = computed(() => {
   switch (props.icon) {
     case 'user':
       return '/carousel/img6.webp'
     case 'users':
       return '/carousel/img7.webp'
     case 'building':
       return '/carousel/img8.webp'
     default:
       return '/carousel/img1.webp'
   }
})
</script>
