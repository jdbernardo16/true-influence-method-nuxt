<template>
    <section
        class="relative h-screen w-full flex flex-col items-center justify-center overflow-hidden"
    >
        <video
            autoplay
            muted
            loop
            playsinline
            class="absolute inset-0 w-full h-full object-cover"
            poster="/carousel/img1.webp"
            @error="handleVideoError"
        >
            <source src="/videos/video.mp4" type="video/mp4" />
        </video>

        <div
            class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e]/70 via-[#1a1a4e]/80 to-[#1a1a4e]/90"
        />
        <div
            class="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-[#232360]/50 to-[#1a1a4e]/90"
        />

        <div class="absolute inset-0 overflow-hidden">
            <div
                v-for="i in 20"
                :key="i"
                class="absolute w-1 h-1 bg-[#d4952a]/20 rounded-full animate-float"
                :style="{
                    left: `${Math.random() * 100}%`,
                    top: `${Math.random() * 100}%`,
                    animationDelay: `${Math.random() * 5}s`,
                    animationDuration: `${8 + Math.random() * 4}s`,
                }"
            />
        </div>

        <div
            class="relative z-10 flex flex-col items-center text-center px-4 max-w-4xl mx-auto"
        >
            <div class="mb-12">
                <div class="relative">
                    <div
                        class="absolute inset-0 bg-[#d4952a] blur-[60px] opacity-10 rounded-full animate-pulse"
                    />
                    <img
                        src="/icononly_transparent_nobuffer.png"
                        alt="Logo Mark"
                        class="w-32 h-32 md:w-40 md:h-40 object-contain relative z-10 animate-float-slow"
                    />
                </div>
            </div>

            <h1
                class="text-[#d4952a] text-2xl md:text-4xl font-medium tracking-[0.2em] uppercase mb-4 relative"
            >
                <span
                    class="absolute -left-8 top-1/2 -translate-y-1/2 w-6 h-px bg-[#d4952a]/40 hidden md:block"
                />
                True Influence Method™️ — Joanna Horton McPherson
                <span
                    class="absolute -right-8 top-1/2 -translate-y-1/2 w-6 h-px bg-[#d4952a]/40 hidden md:block"
                />
            </h1>

            <p
                class="text-[#faf8f5] font-serif italic text-xl md:text-3xl mb-8 font-light relative inline-block"
            >
                <span
                    class="absolute -top-3 -left-4 text-[#d4952a]/20 text-5xl font-serif"
                >
                    "
                </span>
                Your Voice Is Your Leadership.
                <span
                    class="absolute -bottom-3 -right-4 text-[#d4952a]/20 text-5xl font-serif"
                >
                    "
                </span>
            </p>

            <p
                class="text-[#faf8f5]/80 text-lg md:text-xl max-w-2xl mb-12 leading-relaxed"
            >
                You've built something real. Now it's time to speak about it in
                a way that moves rooms, earns trust, and creates a legacy that
                outlasts the work itself.
            </p>

            <div class="flex flex-col sm:flex-row gap-4">
                <NuxtLink
                    to="/apply"
                    class="group px-8 py-4 bg-[#d4952a] hover:bg-[#e8a838] text-[#1a1a4e] font-semibold rounded-lg transition-all hover:shadow-lg hover:shadow-[#d4952a]/20 text-center relative overflow-hidden"
                >
                    <span class="relative z-10 flex items-center gap-2">
                        Apply to Work With Joanna
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
                            class="group-hover:translate-x-1 transition-transform"
                        >
                            <line x1="5" y1="12" x2="19" y2="12"></line>
                            <polyline points="12 5 19 12 12 19"></polyline>
                        </svg>
                    </span>
                </NuxtLink>
                <NuxtLink
                    to="/programs"
                    class="px-8 py-4 border-2 border-[#d4952a] text-[#d4952a] hover:bg-[#d4952a]/10 font-semibold rounded-lg transition-all text-center"
                >
                    Explore Programs →
                </NuxtLink>
            </div>
        </div>

        <div class="absolute bottom-12 left-1/2 transform -translate-x-1/2">
            <div class="animate-bounce">
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
                    class="text-[#d4952a] opacity-60"
                >
                    <path d="M7 13l5 5 5-5M7 6l5 5 5-5"></path>
                </svg>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
const handleVideoError = () => {
    console.log("Video failed to load, using gradient fallback");
};

useHead({
    title: "True Influence Method™️ — Your Voice Is Your Leadership",
    meta: [
        {
            name: "description",
            content:
                "Discover the True Influence Method™️ by Joanna Horton McPherson. Transform your leadership through authentic communication and powerful storytelling.",
        },
    ],
});
</script>

<style scoped>
@keyframes float {
    0%,
    100% {
        transform: translateY(0) translateX(0);
        opacity: 0.2;
    }
    50% {
        transform: translateY(-20px) translateX(10px);
        opacity: 0.6;
    }
}

@keyframes float-slow {
    0%,
    100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-8px);
    }
}

.animate-float {
    animation: float 8s ease-in-out infinite;
}

.animate-float-slow {
    animation: float-slow 4s ease-in-out infinite;
}
</style>
