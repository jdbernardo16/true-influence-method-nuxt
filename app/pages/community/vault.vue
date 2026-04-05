<script setup lang="ts">
useHead({
    title: "The Vault — True Influence Method™️",
    meta: [
        {
            name: "description",
            content:
                "Access The Vault — an exclusive digital library of frameworks, tools, and resources for True Influence Method™️ members.",
        },
    ],
});
</script>

<template>
    <div class="overflow-x-hidden">
        <!-- Hero Section -->
        <section
            class="relative py-20 md:py-32 flex items-center justify-center overflow-hidden"
        >
            <div
                class="absolute inset-0 bg-gradient-to-br from-[#1a1a4e] via-[#232360] to-[#1a1a4e]"
            />

            <!-- Decorative elements -->
            <div
                class="absolute top-20 left-10 w-72 h-72 bg-[#d4952a]/10 rounded-full blur-[100px]"
            />
            <div
                class="absolute bottom-20 right-10 w-96 h-96 bg-[#232360]/50 rounded-full blur-[120px]"
            />

            <!-- Floating particles -->
            <div class="absolute inset-0 overflow-hidden">
                <div
                    v-for="i in 15"
                    :key="i"
                    class="absolute w-2 h-2 bg-[#d4952a]/30 rounded-full animate-float"
                    :style="{
                        left: `${Math.random() * 100}%`,
                        top: `${Math.random() * 100}%`,
                        animationDelay: `${Math.random() * 5}s`,
                        animationDuration: `${6 + Math.random() * 4}s`,
                    }"
                />
            </div>

            <div class="relative z-10 max-w-6xl mx-auto px-6 text-center">
                <span
                    class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-8"
                >
                    <span
                        class="w-2 h-2 bg-[#d4952a] rounded-full animate-pulse"
                    />
                    Members' Resource
                </span>

                <h1
                    class="font-serif text-4xl md:text-6xl text-[#faf8f5] mb-8 leading-tight"
                >
                    The Vault
                </h1>

                <div class="max-w-3xl mx-auto">
                    <p
                        class="text-[#faf8f5]/80 text-lg md:text-xl leading-relaxed mb-6"
                    >
                        An exclusive digital library available to all private
                        clients and Speak & Rise members.
                    </p>
                    <p
                        class="text-[#faf8f5]/80 text-lg md:text-xl leading-relaxed"
                    >
                        The Vault grows with every cohort — a living library of
                        the True Influence Method™️ in practice.
                    </p>
                </div>
            </div>
        </section>

        <!-- What's Inside Section -->
        <section
            class="py-24 md:py-32 bg-[#faf8f5] text-[#1a1a4e] relative overflow-hidden"
        >
            <div
                class="absolute top-0 right-0 w-96 h-96 bg-[#d4952a]/5 rounded-full blur-[120px]"
            />

            <div class="max-w-6xl mx-auto px-6 relative z-10">
                <div class="text-center mb-16">
                    <span
                        class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-6"
                    >
                        Inside The Vault
                    </span>
                    <h2
                        class="font-serif text-3xl md:text-5xl text-[#1a1a4e] mb-6"
                    >
                        Everything You Need to Keep Your Voice Sharp
                    </h2>
                    <p class="text-[#1a1a4e]/70 text-lg max-w-2xl mx-auto">
                        A comprehensive collection of resources designed to
                        support your journey long after your program ends.
                    </p>
                </div>

                <!-- Resource Cards -->
                <div class="grid md:grid-cols-2 gap-8">
                    <!-- Card 1 -->
                    <div
                        class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300 border border-[#faf8f5]"
                    >
                        <div
                            class="w-14 h-14 bg-[#d4952a]/10 rounded-xl flex items-center justify-center mb-6"
                        >
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                width="28"
                                height="28"
                                viewBox="0 0 24 24"
                                fill="none"
                                stroke="#d4952a"
                                stroke-width="2"
                                stroke-linecap="round"
                                stroke-linejoin="round"
                            >
                                <path
                                    d="M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2z"
                                />
                                <path
                                    d="M22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z"
                                />
                            </svg>
                        </div>
                        <h3 class="font-serif text-xl text-[#1a1a4e] mb-3">
                            Training Recordings & Frameworks
                        </h3>
                        <p class="text-[#1a1a4e]/60 leading-relaxed">
                            Deep-dive sessions and comprehensive frameworks that
                            break down the True Influence Method™️ into
                            actionable steps.
                        </p>
                    </div>

                    <!-- Card 2 -->
                    <div
                        class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300 border border-[#faf8f5]"
                    >
                        <div
                            class="w-14 h-14 bg-[#d4952a]/10 rounded-xl flex items-center justify-center mb-6"
                        >
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                width="28"
                                height="28"
                                viewBox="0 0 24 24"
                                fill="none"
                                stroke="#d4952a"
                                stroke-width="2"
                                stroke-linecap="round"
                                stroke-linejoin="round"
                            >
                                <path d="M12 20h9" />
                                <path
                                    d="M16.5 3.5a2.121 2.121 0 0 1 3 3L7 19l-4 1 1-4L16.5 3.5z"
                                />
                            </svg>
                        </div>
                        <h3 class="font-serif text-xl text-[#1a1a4e] mb-3">
                            Message Clarity Tools
                        </h3>
                        <p class="text-[#1a1a4e]/60 leading-relaxed">
                            Practical exercises and templates to help you craft
                            and refine your core message with precision.
                        </p>
                    </div>

                    <!-- Card 3 -->
                    <div
                        class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300 border border-[#faf8f5]"
                    >
                        <div
                            class="w-14 h-14 bg-[#d4952a]/10 rounded-xl flex items-center justify-center mb-6"
                        >
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                width="28"
                                height="28"
                                viewBox="0 0 24 24"
                                fill="none"
                                stroke="#d4952a"
                                stroke-width="2"
                                stroke-linecap="round"
                                stroke-linejoin="round"
                            >
                                <path
                                    d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"
                                />
                                <circle cx="9" cy="7" r="4" />
                                <path d="M23 21v-2a4 4 0 0 0-3-3.87" />
                                <path d="M16 3.13a4 4 0 0 1 0 7.75" />
                            </svg>
                        </div>
                        <h3 class="font-serif text-xl text-[#1a1a4e] mb-3">
                            Story Development Guides
                        </h3>
                        <p class="text-[#1a1a4e]/60 leading-relaxed">
                            Step-by-step resources for uncovering and shaping
                            your defining story into a powerful narrative.
                        </p>
                    </div>

                    <!-- Card 4 -->
                    <div
                        class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300 border border-[#faf8f5]"
                    >
                        <div
                            class="w-14 h-14 bg-[#d4952a]/10 rounded-xl flex items-center justify-center mb-6"
                        >
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                width="28"
                                height="28"
                                viewBox="0 0 24 24"
                                fill="none"
                                stroke="#d4952a"
                                stroke-width="2"
                                stroke-linecap="round"
                                stroke-linejoin="round"
                            >
                                <path
                                    d="M12 1a3 3 0 0 0-3 3v8a3 3 0 0 0 6 0V4a3 3 0 0 0-3-3z"
                                />
                                <path d="M19 10v2a7 7 0 0 1-14 0v-2" />
                                <line x1="12" y1="19" x2="12" y2="23" />
                                <line x1="8" y1="23" x2="16" y2="23" />
                            </svg>
                        </div>
                        <h3 class="font-serif text-xl text-[#1a1a4e] mb-3">
                            Speaking Tips & Presence Practices
                        </h3>
                        <p class="text-[#1a1a4e]/60 leading-relaxed">
                            Daily practices and techniques to enhance your vocal
                            presence, body language, and stage confidence.
                        </p>
                    </div>
                </div>

                <!-- Bonus Resources -->
                <div
                    class="mt-16 bg-gradient-to-br from-[#1a1a4e] to-[#232360] rounded-2xl p-8 md:p-12 text-center"
                >
                    <div
                        class="w-16 h-16 bg-[#d4952a]/20 rounded-xl flex items-center justify-center mx-auto mb-6"
                    >
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            width="32"
                            height="32"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="#d4952a"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        >
                            <path
                                d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
                            />
                        </svg>
                    </div>
                    <h3 class="font-serif text-2xl text-[#faf8f5] mb-4">
                        Bonus Resources
                    </h3>
                    <p
                        class="text-[#faf8f5]/70 leading-relaxed max-w-2xl mx-auto"
                    >
                        Exclusive content including advanced frameworks, guest
                        expert sessions, and curated reading lists to accelerate
                        your growth as a speaker and leader.
                    </p>
                </div>
            </div>
        </section>

        <!-- CTA Section -->
        <section
            class="py-24 md:py-32 bg-[#1a1a4e] text-[#faf8f5] relative overflow-hidden"
        >
            <div
                class="absolute bottom-0 left-0 w-96 h-96 bg-[#d4952a]/10 rounded-full blur-[120px]"
            />

            <div class="max-w-4xl mx-auto px-6 relative z-10 text-center">
                <h2 class="font-serif text-3xl md:text-5xl text-[#faf8f5] mb-6">
                    Ready to Access The Vault?
                </h2>

                <p
                    class="text-[#faf8f5]/70 text-lg leading-relaxed mb-10 max-w-2xl mx-auto"
                >
                    Join Joanna's private training or Speak & Rise program to
                    unlock full access to The Vault and become part of our
                    growing community.
                </p>

                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <NuxtLink
                        to="/programs"
                        class="inline-flex items-center justify-center gap-3 bg-[#d4952a] text-white text-sm uppercase tracking-widest px-8 py-4 rounded-full font-medium hover:bg-[#b37a1f] transition-colors duration-300"
                    >
                        Explore Programs
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            width="16"
                            height="16"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                        >
                            <path d="M5 12h14" />
                            <path d="m12 5 7 7-7 7" />
                        </svg>
                    </NuxtLink>
                    <NuxtLink
                        to="/apply"
                        class="inline-flex items-center justify-center gap-3 border-2 border-[#d4952a] text-[#d4952a] text-sm uppercase tracking-widest px-8 py-4 rounded-full font-medium hover:bg-[#d4952a]/10 transition-colors duration-300"
                    >
                        Apply Now
                    </NuxtLink>
                </div>
            </div>
        </section>
    </div>
</template>

<style scoped>
@keyframes float {
    0%,
    100% {
        transform: translateY(0) translateX(0);
    }
    50% {
        transform: translateY(-20px) translateX(10px);
    }
}

.animate-float {
    animation: float 8s ease-in-out infinite;
}
</style>
