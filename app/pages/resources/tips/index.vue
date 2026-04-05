<script setup lang="ts">
useHead({
    title: "Speaking Tips — True Influence Method™️",
    meta: [
        {
            name: "description",
            content:
                "Practical speaking tips and insights from Joanna's 30+ years of experience to help you find your footing and own your message.",
        },
    ],
});

const tips = [
    {
        slug: "the-power-of-pause",
        title: "The Power of Pause",
        excerpt:
            "Silence is not empty space—it's a tool. Learn how strategic pauses can amplify your message and command attention.",
        category: "Delivery",
        date: "March 20, 2026",
        readTime: "3 min read",
        image: "/carousel/img2.webp",
    },
    {
        slug: "starting-strong-openings-that-captivate",
        title: "Starting Strong: Openings That Captivate",
        excerpt:
            "The first 30 seconds determine whether your audience leans in or tunes out. Here's how to make every opening count.",
        category: "Structure",
        date: "March 15, 2026",
        readTime: "4 min read",
        image: "/carousel/img4.webp",
    },
    {
        slug: "eye-contact-that-builds-connection",
        title: "Eye Contact That Builds Connection",
        excerpt:
            "Beyond technique—true eye contact is about relationship. Learn how to connect authentically with your audience.",
        category: "Presence",
        date: "March 10, 2026",
        readTime: "3 min read",
        image: "/carousel/img6.webp",
    },
    {
        slug: "using-your-voice-as-an-instrument",
        title: "Using Your Voice as an Instrument",
        excerpt:
            "Your voice carries more than words—it carries emotion, conviction, and presence. Here's how to use it fully.",
        category: "Voice",
        date: "March 5, 2026",
        readTime: "5 min read",
        image: "/carousel/img8.webp",
    },
    {
        slug: "handling-questions-with-grace",
        title: "Handling Questions With Grace",
        excerpt:
            "Q&A is where authenticity shines. Learn how to respond to questions with confidence, honesty, and connection.",
        category: "Engagement",
        date: "February 28, 2026",
        readTime: "4 min read",
        image: "/carousel/img1.webp",
    },
    {
        slug: "body-language-that-communicates-truth",
        title: "Body Language That Communicates Truth",
        excerpt:
            "Your body speaks before you do. Learn how to align your physical presence with your authentic message.",
        category: "Presence",
        date: "February 22, 2026",
        readTime: "4 min read",
        image: "/carousel/img3.webp",
    },
    {
        slug: "nervousness-as-fuel-not-barrier",
        title: "Nervousness as Fuel, Not Barrier",
        excerpt:
            "Nervousness is not your enemy—it's energy. Learn how to channel it into powerful, authentic presence.",
        category: "Mindset",
        date: "February 15, 2026",
        readTime: "5 min read",
        image: "/carousel/img5.webp",
    },
    {
        slug: "ending-with-impact",
        title: "Ending With Impact",
        excerpt:
            "How you leave the room matters as much as how you enter it. Learn to craft endings that resonate and inspire action.",
        category: "Structure",
        date: "February 8, 2026",
        readTime: "4 min read",
        image: "/carousel/img7.webp",
    },
];
</script>

<template>
    <div class="overflow-x-hidden">
        <!-- Hero Section -->
        <section
            class="relative min-h-[60vh] flex items-center justify-center py-20 md:py-32 overflow-hidden"
        >
            <div class="absolute inset-0">
                <img
                    src="/carousel/img2.webp"
                    alt="Background"
                    class="w-full h-full object-cover"
                />
                <div
                    class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e]/90 via-[#1a1a4e]/85 to-[#1a1a4e]/95"
                />
            </div>

            <div class="absolute inset-0">
                <div
                    class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-[#d4952a]/5 rounded-full blur-[120px]"
                />
            </div>

            <div class="max-w-4xl mx-auto px-6 relative z-10 text-center">
                <div class="mb-6">
                    <span
                        class="text-[#d4952a] text-sm md:text-base font-medium tracking-[0.2em] uppercase"
                    >
                        Speaking Tips
                    </span>
                </div>

                <h1
                    class="font-serif text-4xl md:text-5xl lg:text-6xl text-[#faf8f5] mb-8 leading-tight"
                >
                    The Stage Has Always Been a Place of Transformation.
                </h1>

                <p
                    class="text-[#faf8f5]/80 text-lg md:text-xl max-w-2xl mx-auto leading-relaxed"
                >
                    Whether you're speaking to a board, a ballroom, or a camera
                    — these practical insights from Joanna's 30+ years of
                    experience will help you find your footing and own your
                    message.
                </p>
            </div>
        </section>

        <!-- Tips Grid Section -->
        <section class="py-20 md:py-32 relative">
            <div
                class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e] via-[#232360] to-[#1a1a4e]"
            />
            <div
                class="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-[#d4952a]/5 to-transparent"
            />

            <div class="max-w-7xl mx-auto px-6 relative z-10">
                <div
                    class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8"
                >
                    <NuxtLink
                        v-for="tip in tips"
                        :key="tip.slug"
                        :to="`/resources/tips/${tip.slug}`"
                        class="group bg-[#1a1a4e]/50 backdrop-blur-sm rounded-xl border border-[#faf8f5]/10 hover:border-[#d4952a]/30 transition-all duration-300 overflow-hidden"
                    >
                        <div class="relative aspect-[16/10] overflow-hidden">
                            <img
                                :src="tip.image"
                                :alt="tip.title"
                                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />
                            <div class="absolute top-4 left-4">
                                <span
                                    class="inline-block px-3 py-1 bg-[#d4952a] text-[#1a1a4e] text-xs font-semibold rounded-full"
                                >
                                    {{ tip.category }}
                                </span>
                            </div>
                        </div>

                        <div class="p-6">
                            <div
                                class="flex items-center gap-3 mb-3 text-sm text-[#faf8f5]/60"
                            >
                                <span>{{ tip.date }}</span>
                                <span
                                    class="w-1 h-1 rounded-full bg-[#d4952a]"
                                />
                                <span>{{ tip.readTime }}</span>
                            </div>

                            <h3
                                class="font-serif text-xl text-[#faf8f5] mb-3 leading-tight group-hover:text-[#d4952a] transition-colors"
                            >
                                {{ tip.title }}
                            </h3>

                            <p
                                class="text-[#faf8f5]/70 text-sm leading-relaxed line-clamp-3"
                            >
                                {{ tip.excerpt }}
                            </p>

                            <div
                                class="mt-4 flex items-center gap-2 text-[#d4952a] text-sm font-medium group-hover:gap-3 transition-all"
                            >
                                Read More
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
                                    <line x1="5" y1="12" x2="19" y2="12"></line>
                                    <polyline
                                        points="12 5 19 12 12 19"
                                    ></polyline>
                                </svg>
                            </div>
                        </div>
                    </NuxtLink>
                </div>
            </div>
        </section>

        <!-- Newsletter CTA Section -->
        <section class="py-20 md:py-32 relative overflow-hidden">
            <div class="absolute inset-0">
                <img
                    src="/carousel/img7.webp"
                    alt="Background"
                    class="w-full h-full object-cover"
                />
                <div
                    class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e]/95 via-[#1a1a4e]/90 to-[#1a1a4e]/95"
                />
            </div>

            <div class="absolute inset-0">
                <div
                    class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[800px] h-[800px] bg-[#d4952a]/5 rounded-full blur-[150px]"
                />
            </div>

            <div class="max-w-4xl mx-auto px-6 relative z-10 text-center">
                <div class="mb-6">
                    <span
                        class="text-[#d4952a] text-sm md:text-base font-medium tracking-[0.2em] uppercase"
                    >
                        Stay Connected
                    </span>
                </div>

                <h2 class="font-serif text-4xl md:text-5xl text-[#faf8f5] mb-6">
                    Join 5,000+ Leaders Receiving Weekly Insights.
                </h2>

                <p
                    class="text-[#faf8f5]/80 text-lg md:text-xl mb-12 max-w-2xl mx-auto leading-relaxed"
                >
                    Authentic influence. Emotional clarity. Brave communication.
                    Every week, Joanna shares what she's learning, observing,
                    and practicing — delivered directly to your inbox.
                </p>

                <form class="max-w-md mx-auto flex flex-col sm:flex-row gap-4">
                    <input
                        type="email"
                        placeholder="Enter your email"
                        class="flex-1 px-6 py-4 bg-[#faf8f5]/10 border border-[#faf8f5]/20 rounded-lg text-[#faf8f5] placeholder:text-[#faf8f5]/40 focus:outline-none focus:border-[#d4952a] transition-colors"
                    />
                    <button
                        type="submit"
                        class="px-8 py-4 bg-[#d4952a] hover:bg-[#e8a838] text-[#1a1a4e] font-semibold rounded-lg transition-all hover:shadow-lg hover:shadow-[#d4952a]/20"
                    >
                        Subscribe
                    </button>
                </form>

                <p class="text-[#faf8f5]/50 text-sm mt-4">
                    No spam. Unsubscribe anytime. Your privacy is respected.
                </p>
            </div>
        </section>
    </div>
</template>
