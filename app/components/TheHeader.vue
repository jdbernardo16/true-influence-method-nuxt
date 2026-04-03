<template>
  <nav
    class="fixed top-0 left-0 right-0 z-50 transition-all duration-500"
    :class="[
      scrolled ? 'bg-[#1a1a4e]/95 backdrop-blur-sm py-4 shadow-lg' : 'bg-transparent py-6'
    ]"
  >
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center">
      <!-- Logo -->
      <a
        href="/"
        class="relative z-50 block w-12 opacity-90 hover:opacity-100 transition-opacity"
      >
        <img
          src="/fulllogo_transparent_nobuffer.png"
          alt="Joanna Horton McPherson"
          class="w-full h-auto"
        />
      </a>

      <!-- Desktop Nav -->
      <div class="hidden lg:flex items-center space-x-8">
        <button
          @click.stop="toggleDropdown('programs')"
          class="text-[#faf8f5] hover:text-[#d4952a] text-sm uppercase tracking-widest transition-colors duration-300 font-medium flex items-center gap-2"
          aria-label="Programs menu"
        >
          Programs
          <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="m6 9 6 6 6-6"/>
          </svg>
        </button>

        <button
          @click.stop="toggleDropdown('about')"
          class="text-[#faf8f5] hover:text-[#d4952a] text-sm uppercase tracking-widest transition-colors duration-300 font-medium flex items-center gap-2"
          aria-label="About menu"
        >
          About
          <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="m6 9 6 6 6-6"/>
          </svg>
        </button>

        <NuxtLink
          to="/success-stories"
          class="text-[#faf8f5] hover:text-[#d4952a] text-sm uppercase tracking-widest transition-colors duration-300 font-medium"
        >
          Success Stories
        </NuxtLink>

        <button
          @click.stop="toggleDropdown('community')"
          class="text-[#faf8f5] hover:text-[#d4952a] text-sm uppercase tracking-widest transition-colors duration-300 font-medium flex items-center gap-2"
          aria-label="Community menu"
        >
          Community
          <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="m6 9 6 6 6-6"/>
          </svg>
        </button>

        <button
          @click.stop="toggleDropdown('resources')"
          class="text-[#faf8f5] hover:text-[#d4952a] text-sm uppercase tracking-widest transition-colors duration-300 font-medium flex items-center gap-2"
          aria-label="Resources menu"
        >
          Resources
          <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="m6 9 6 6 6-6"/>
          </svg>
        </button>

        <NuxtLink
          to="/faq"
          class="text-[#faf8f5] hover:text-[#d4952a] text-sm uppercase tracking-widest transition-colors duration-300 font-medium"
        >
          FAQ
        </NuxtLink>

        <NuxtLink
          to="/apply"
          class="bg-[#d4952a] text-white text-sm uppercase tracking-widest px-6 py-2.5 rounded-full font-medium hover:bg-[#b37a1f] transition-colors duration-300"
        >
          Apply
        </NuxtLink>
      </div>

      <!-- Mobile Menu Button -->
      <button
        class="lg:hidden text-[#faf8f5] z-50"
        @click="mobileMenuOpen = !mobileMenuOpen"
        aria-label="Toggle menu"
      >
        <svg v-if="!mobileMenuOpen" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <line x1="4" x2="20" y1="12" y2="12"></line>
          <line x1="4" x2="20" y1="6" y2="6"></line>
          <line x1="4" x2="20" y1="18" y2="18"></line>
        </svg>
        <svg v-else xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <line x1="18" x2="6" y1="6" y2="18"></line>
          <line x1="6" x2="18" y1="6" y2="18"></line>
        </svg>
      </button>
    </div>
  </nav>

  <!-- Mobile Menu Overlay -->
  <Transition name="fade">
    <div
      v-if="mobileMenuOpen"
      class="fixed inset-0 z-40 bg-[#1a1a4e] flex flex-col items-center justify-center"
    >
      <div class="flex flex-col space-y-6 text-center">
        <div class="flex flex-col space-y-3">
          <button
            @click="toggleMobileDropdown('programs')"
            class="text-[#faf8f5] text-xl font-serif hover:text-[#d4952a] transition-colors flex items-center gap-2 justify-center"
          >
            Programs
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="m6 9 6 6 6-6"/>
            </svg>
          </button>
          <div v-if="mobileDropdowns.programs" class="flex flex-col space-y-2 pl-4">
            <NuxtLink v-for="link in programsLinks" :key="link.href" :to="link.href" @click="mobileMenuOpen = false" class="text-[#faf8f5]/80 text-lg hover:text-[#d4952a] transition-colors">
              {{ link.name }}
            </NuxtLink>
          </div>
        </div>

        <div class="flex flex-col space-y-3">
          <button
            @click="toggleMobileDropdown('about')"
            class="text-[#faf8f5] text-xl font-serif hover:text-[#d4952a] transition-colors flex items-center gap-2 justify-center"
          >
            About
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="m6 9 6 6 6-6"/>
            </svg>
          </button>
          <div v-if="mobileDropdowns.about" class="flex flex-col space-y-2 pl-4">
            <NuxtLink v-for="link in aboutLinks" :key="link.href" :to="link.href" @click="mobileMenuOpen = false" class="text-[#faf8f5]/80 text-lg hover:text-[#d4952a] transition-colors">
              {{ link.name }}
            </NuxtLink>
          </div>
        </div>

        <NuxtLink to="/success-stories" @click="mobileMenuOpen = false" class="text-[#faf8f5] text-xl font-serif hover:text-[#d4952a] transition-colors">
          Success Stories
        </NuxtLink>

        <div class="flex flex-col space-y-3">
          <button
            @click="toggleMobileDropdown('community')"
            class="text-[#faf8f5] text-xl font-serif hover:text-[#d4952a] transition-colors flex items-center gap-2 justify-center"
          >
            Community
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="m6 9 6 6 6-6"/>
            </svg>
          </button>
          <div v-if="mobileDropdowns.community" class="flex flex-col space-y-2 pl-4">
            <NuxtLink v-for="link in communityLinks" :key="link.href" :to="link.href" @click="mobileMenuOpen = false" class="text-[#faf8f5]/80 text-lg hover:text-[#d4952a] transition-colors">
              {{ link.name }}
            </NuxtLink>
          </div>
        </div>

        <div class="flex flex-col space-y-3">
          <button
            @click="toggleMobileDropdown('resources')"
            class="text-[#faf8f5] text-xl font-serif hover:text-[#d4952a] transition-colors flex items-center gap-2 justify-center"
          >
            Resources
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="m6 9 6 6 6-6"/>
            </svg>
          </button>
          <div v-if="mobileDropdowns.resources" class="flex flex-col space-y-2 pl-4">
            <NuxtLink v-for="link in resourcesLinks" :key="link.href" :to="link.href" @click="mobileMenuOpen = false" class="text-[#faf8f5]/80 text-lg hover:text-[#d4952a] transition-colors">
              {{ link.name }}
            </NuxtLink>
          </div>
        </div>

        <NuxtLink to="/faq" @click="mobileMenuOpen = false" class="text-[#faf8f5] text-xl font-serif hover:text-[#d4952a] transition-colors">
          FAQ
        </NuxtLink>

        <NuxtLink to="/apply" @click="mobileMenuOpen = false" class="bg-[#d4952a] text-white text-xl uppercase tracking-widest px-8 py-3 rounded-full font-medium hover:bg-[#b37a1f] transition-colors">
          Apply
        </NuxtLink>
      </div>
    </div>
  </Transition>

  <!-- Dropdown Menus -->
  <Transition name="dropdown">
    <div
      v-if="activeDropdown"
      @click.stop
      class="fixed top-[72px] left-0 right-0 z-40 bg-[#1a1a4e]/95 backdrop-blur-sm border-t border-[#faf8f5]/10 shadow-xl"
    >
      <div class="max-w-7xl mx-auto px-6 py-8">
        <div class="grid grid-cols-4 gap-8">
          <div v-if="activeDropdown === 'programs'" class="space-y-4">
            <h3 class="text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase mb-4">Programs</h3>
            <nav class="space-y-3">
              <NuxtLink v-for="link in programsLinks" :key="link.href" :to="link.href" @click="activeDropdown = null" class="block text-[#faf8f5] hover:text-[#d4952a] transition-colors">
                {{ link.name }}
              </NuxtLink>
            </nav>
          </div>

          <div v-if="activeDropdown === 'about'" class="space-y-4">
            <h3 class="text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase mb-4">About</h3>
            <nav class="space-y-3">
              <NuxtLink v-for="link in aboutLinks" :key="link.href" :to="link.href" @click="activeDropdown = null" class="block text-[#faf8f5] hover:text-[#d4952a] transition-colors">
                {{ link.name }}
              </NuxtLink>
            </nav>
          </div>

          <div v-if="activeDropdown === 'community'" class="space-y-4">
            <h3 class="text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase mb-4">Community</h3>
            <nav class="space-y-3">
              <NuxtLink v-for="link in communityLinks" :key="link.href" :to="link.href" @click="activeDropdown = null" class="block text-[#faf8f5] hover:text-[#d4952a] transition-colors">
                {{ link.name }}
              </NuxtLink>
            </nav>
          </div>

          <div v-if="activeDropdown === 'resources'" class="space-y-4">
            <h3 class="text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase mb-4">Resources</h3>
            <nav class="space-y-3">
              <NuxtLink v-for="link in resourcesLinks" :key="link.href" :to="link.href" @click="activeDropdown = null" class="block text-[#faf8f5] hover:text-[#d4952a] transition-colors">
                {{ link.name }}
              </NuxtLink>
            </nav>
          </div>

          <div v-if="activeDropdown === 'programs'" class="col-span-3 pl-8 border-l border-[#faf8f5]/10">
            <p class="text-[#faf8f5]/60 text-sm leading-relaxed">
              Transform your speaking skills with our comprehensive programs designed for every stage of your journey.
            </p>
          </div>

          <div v-if="activeDropdown === 'about'" class="col-span-3 pl-8 border-l border-[#faf8f5]/10">
            <p class="text-[#faf8f5]/60 text-sm leading-relaxed">
              Discover the True Influence Method and learn about Joanna's journey from speaker to leadership coach.
            </p>
          </div>

          <div v-if="activeDropdown === 'community'" class="col-span-3 pl-8 border-l border-[#faf8f5]/10">
            <p class="text-[#faf8f5]/60 text-sm leading-relaxed">
              Join our community of speakers and leaders, access exclusive content, and attend transformational events.
            </p>
          </div>

          <div v-if="activeDropdown === 'resources'" class="col-span-3 pl-8 border-l border-[#faf8f5]/10">
            <p class="text-[#faf8f5]/60 text-sm leading-relaxed">
              Access articles, speaking tips, media features, and podcasts to accelerate your growth.
            </p>
          </div>
        </div>
      </div>
    </div>
  </Transition>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const scrolled = ref(false)
const mobileMenuOpen = ref(false)
const activeDropdown = ref<string | null>(null)
const mobileDropdowns = ref<{ [key: string]: boolean }>({})

const handleScroll = () => {
  scrolled.value = window.scrollY > 50
}

const handleEscape = (e: KeyboardEvent) => {
  if (e.key === 'Escape') {
    activeDropdown.value = null
    mobileMenuOpen.value = false
  }
}

const toggleDropdown = (dropdown: string) => {
  activeDropdown.value = activeDropdown.value === dropdown ? null : dropdown
}

const toggleMobileDropdown = (dropdown: string) => {
  mobileDropdowns.value[dropdown] = !mobileDropdowns.value[dropdown]
}

const closeDropdowns = (e: MouseEvent) => {
  const target = e.target as HTMLElement
  const nav = target.closest('nav')
  const dropdown = target.closest('.fixed.top-full')
  
  if (!nav && !dropdown) {
    activeDropdown.value = null
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  window.addEventListener('keydown', handleEscape)
  document.addEventListener('click', closeDropdowns as EventListener)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
  window.removeEventListener('keydown', handleEscape)
  document.removeEventListener('click', closeDropdowns as EventListener)
})

const programsLinks = [
  { name: 'Private Training', href: '/programs/private-training' },
  { name: 'Speak & Rise (Group)', href: '/programs/speak-rise' },
  { name: 'Corporate Programs', href: '/programs/corporate' },
  { name: 'True Influence License', href: '/programs/license' },
]

const aboutLinks = [
  { name: 'About Joanna', href: '/about' },
  { name: 'The Journey', href: '/journey' },
  { name: 'The Research', href: '/about/research' },
]

const communityLinks = [
  { name: 'The Vault', href: '/community/vault' },
  { name: 'Events & Workshops', href: '/community/events' },
]

const resourcesLinks = [
  { name: 'Articles & Insights', href: '/resources/articles' },
  { name: 'Speaking Tips', href: '/resources/tips' },
  { name: 'Media Features', href: '/resources/media' },
  { name: 'Blog & Podcast', href: '/resources/blog' },
]
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.dropdown-enter-active,
.dropdown-leave-active {
  transition: all 0.3s ease-out;
}

.dropdown-enter-from,
.dropdown-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
