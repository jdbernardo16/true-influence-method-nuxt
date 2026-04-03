<template>
  <div class="overflow-x-hidden">
    <section
      class="py-24 md:py-32 bg-[#1a1a4e] text-[#faf8f5] text-center relative overflow-hidden"
    >
      <!-- Background decoration -->
      <div class="absolute top-0 left-1/2 transform -translate-x-1/2 w-full h-full max-w-4xl opacity-5 pointer-events-none">
        <div class="w-full h-full border border-[#d4952a] rounded-full scale-150" />
      </div>

      <div class="max-w-4xl mx-auto px-6 relative z-10">
        <span class="block text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase mb-6">
          Apply / Work With Joanna
        </span>

        <h1 class="font-serif text-4xl md:text-6xl mb-8 text-[#faf8f5]">
          Let's Find Out If This Is the Right Fit.
        </h1>

        <p class="text-[#faf8f5]/80 text-xl font-light mb-12 max-w-3xl mx-auto">
          Joanna works with a limited number of private clients at any one time, and every corporate and group engagement is carefully considered. The inquiry form is the first step — not a commitment, just a conversation.
        </p>

        <p class="text-[#faf8f5]/80 text-xl font-light mb-12 max-w-3xl mx-auto">
          Fill it out honestly. Tell us where you are, where you want to go, and what feels most alive in your work right now. Joanna's team will review your submission and be in touch within 2 business days.
        </p>

        <!-- Contact Form -->
        <form @submit="handleSubmit" class="max-w-xl mx-auto space-y-6 text-left">
          <div>
            <label
              for="name"
              class="block text-sm font-medium text-[#faf8f5]/80 mb-2"
            >
              Name
            </label>
            <input
              id="name"
              v-model="formData.name"
              type="text"
              required
              placeholder="Your name"
              class="w-full px-4 py-3 bg-[#faf8f5]/5 border border-[#faf8f5]/10 rounded-lg text-[#faf8f5] placeholder-[#faf8f5]/40 focus:outline-none focus:border-[#d4952a] focus:ring-1 focus:ring-[#d4952a] transition-all"
            />
          </div>

          <div>
            <label
              for="email"
              class="block text-sm font-medium text-[#faf8f5]/80 mb-2"
            >
              Email
            </label>
            <input
              id="email"
              v-model="formData.email"
              type="email"
              required
              placeholder="your@email.com"
              class="w-full px-4 py-3 bg-[#faf8f5]/5 border border-[#faf8f5]/10 rounded-lg text-[#faf8f5] placeholder-[#faf8f5]/40 focus:outline-none focus:border-[#d4952a] focus:ring-1 focus:ring-[#d4952a] transition-all"
            />
          </div>

          <div>
            <label
              for="message"
              class="block text-sm font-medium text-[#faf8f5]/80 mb-2"
            >
              Message
            </label>
            <textarea
              id="message"
              v-model="formData.message"
              required
              rows="6"
              placeholder="Tell us about yourself, your work, and what you're hoping to achieve..."
              class="w-full px-4 py-3 bg-[#faf8f5]/5 border border-[#faf8f5]/10 rounded-lg text-[#faf8f5] placeholder-[#faf8f5]/40 focus:outline-none focus:border-[#d4952a] focus:ring-1 focus:ring-[#d4952a] transition-all resize-none"
            />
          </div>

          <button
            type="submit"
            :disabled="isSubmitting"
            class="w-full py-4 px-6 bg-[#d4952a] hover:bg-[#e8a838] text-[#1a1a4e] font-semibold rounded-lg transition-all disabled:opacity-50 disabled:cursor-not-allowed hover:shadow-lg hover:shadow-[#d4952a]/20"
          >
            {{ isSubmitting ? 'Submitting...' : 'Submit Your Application →' }}
          </button>
        </form>

        <!-- Additional Links -->
        <div class="mt-12 flex flex-col md:flex-row items-center gap-6 justify-center">
          <a
            href="mailto:joanna@trueinfluencemethod.com"
            class="text-xl md:text-2xl font-serif italic text-[#d4952a] hover:text-[#e8a838] transition-colors border-b border-transparent hover:border-[#e8a838] pb-1"
          >
            joanna@trueinfluencemethod.com
          </a>

          <a
            href="https://calendly.com/joanna-trueinfluencemethod/private-training"
            target="_blank"
            rel="noopener noreferrer"
            class="px-6 py-3 border-2 border-[#d4952a] text-[#d4952a] hover:bg-[#d4952a]/10 font-semibold rounded-lg transition-all"
          >
            Book a Consultation →
          </a>
        </div>
      </div>
    </section>

    <!-- Success Modal -->
    <Transition name="fade">
      <div
        v-if="isSubmitted"
        class="fixed inset-0 z-50 flex items-center justify-center bg-black/60 backdrop-blur-sm p-4"
        @click="isSubmitted = false"
      >
        <div
          class="bg-[#1a1a4e] border border-[#d4952a]/30 rounded-2xl p-8 max-w-md w-full shadow-2xl relative"
          @click.stop
        >
          <button
            @click="isSubmitted = false"
            class="absolute top-4 right-4 text-[#faf8f5]/60 hover:text-[#d4952a] transition-colors"
            aria-label="Close modal"
          >
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <line x1="18" x2="6" y1="6" y2="18"></line>
              <line x1="6" x2="18" y1="6" y2="18"></line>
            </svg>
          </button>

          <div class="flex flex-col items-center text-center">
            <div class="w-16 h-16 bg-[#d4952a]/20 rounded-full flex items-center justify-center mb-6">
              <svg class="w-8 h-8 text-[#d4952a]" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"></path>
                <polyline points="22 4 12 14.01 9 11.01"></polyline>
              </svg>
            </div>

            <h3 class="font-serif text-2xl text-[#faf8f5] mb-3">
              Application Submitted!
            </h3>

            <p class="text-[#faf8f5]/70 mb-6">
              Thank you for reaching out. Your application has been received, and we'll get back to you within 2 business days.
            </p>

            <button
              @click="isSubmitted = false"
              class="px-8 py-3 bg-[#d4952a] hover:bg-[#e8a838] text-[#1a1a4e] font-semibold rounded-lg transition-all hover:shadow-lg hover:shadow-[#d4952a]/20"
            >
              Close
            </button>
          </div>
        </div>
      </div>
    </Transition>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const GOOGLE_FORM_ACTION = 'https://docs.google.com/forms/d/e/1FAIpQLSd6G2lES4cHi3EUXXpFkuABsOu4FlVDM7QKMhoZEFeVcjrV6g/formResponse'

const formData = ref({
  name: '',
  email: '',
  message: '',
})
const isSubmitting = ref(false)
const isSubmitted = ref(false)

const handleSubmit = async (e: Event) => {
  e.preventDefault()
  isSubmitting.value = true

  const formDataObj = new FormData()
  formDataObj.append('entry.178362318', formData.value.name)
  formDataObj.append('entry.2077964853', formData.value.email)
  formDataObj.append('entry.1372900019', formData.value.message)

  try {
    await fetch(GOOGLE_FORM_ACTION, {
      method: 'POST',
      mode: 'no-cors',
      headers: {
        'Content-Type': 'application/x-www-form-urlencoded',
      },
      body: new URLSearchParams(formDataObj as any).toString(),
    })

    isSubmitting.value = false
    isSubmitted.value = true
    formData.value = { name: '', email: '', message: '' }
  } catch (error) {
    console.error('Error submitting form:', error)
    isSubmitting.value = false
    isSubmitted.value = true
    formData.value = { name: '', email: '', message: '' }
  }
}

useHead({
  title: 'Apply | True Influence Method™️',
  meta: [
    {
      name: 'description',
      content: 'Apply to work with Joanna Horton McPherson and the True Influence Method™️. Start your journey to authentic leadership communication.'
    }
  ]
})
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
</style>
