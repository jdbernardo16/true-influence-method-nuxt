<script setup lang="ts">
useHead({
    title: "Media Features — True Influence Method™️",
    meta: [
        {
            name: "description",
            content:
                "Joanna has been featured across media, podcasts, and stages as one of the leading voices on authentic leadership communication.",
        },
    ],
});

const mediaFeatures = [
    {
        slug: "forbes-council-authentic-leadership",
        title: "The Power of Authentic Leadership Communication",
        source: "Forbes Business Council",
        type: "Article",
        date: "March 15, 2026",
        excerpt:
            "Why the most influential leaders are not the most polished—they're the most honest.",
        image: "/carousel/img1.webp",
        url: "#",
    },
    {
        slug: "tedx-talk-true-influence",
        title: "True Influence: Finding Your Voice",
        source: "TEDx",
        type: "Talk",
        date: "February 28, 2026",
        excerpt:
            "A TEDx talk on how authentic communication transforms leadership and creates lasting influence.",
        image: "/carousel/img3.webp",
        url: "#",
    },
    {
        slug: "leadership-podcast-episode",
        title: "From Impact to Influence: A Conversation",
        source: "The Leadership Podcast",
        type: "Podcast",
        date: "February 15, 2026",
        excerpt:
            "Joanna shares insights on the journey from building impact to speaking with influence.",
        image: "/carousel/img5.webp",
        url: "#",
    },
    {
        slug: "harvard-business-review",
        title: "The Defining Moment Every Leader Has",
        source: "Harvard Business Review",
        type: "Article",
        date: "January 30, 2026",
        excerpt:
            "How identifying your defining moment transforms your leadership communication.",
        image: "/carousel/img7.webp",
        url: "#",
    },
    {
        slug: "entrepreneur-magazine",
        title: "Why Your Story Matters More Than Your Script",
        source: "Entrepreneur Magazine",
        type: "Article",
        date: "January 15, 2026",
        excerpt:
            "The most compelling messages come from lived experience, not perfect scripts.",
        image: "/carousel/img2.webp",
        url: "#",
    },
    {
        slug: "cnbc-interview",
        title: "Speaking Truth to Power",
        source: "CNBC",
        type: "Interview",
        date: "December 20, 2025",
        excerpt:
            "An interview on authentic communication in high-stakes business environments.",
        image: "/carousel/img4.webp",
        url: "#",
    },
    {
        slug: "master-class-podcast",
        title: "The Art of Authentic Communication",
        source: "Master Class Podcast",
        type: "Podcast",
        date: "December 5, 2025",
        excerpt:
            "Deep dive into the principles and practices of authentic leadership communication.",
        image: "/carousel/img6.webp",
        url: "#",
    },
    {
        slug: "fast-company-feature",
        title: "Leaders Who Speak Their Truth",
        source: "Fast Company",
        type: "Feature",
        date: "November 18, 2025",
        excerpt:
            "A profile of leaders who have transformed their communication through authenticity.",
        image: "/carousel/img8.webp",
        url: "#",
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
                    src="/carousel/img3.webp"
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
                        Media Features
                    </span>
                </div>

                <h1
                    class="font-serif text-4xl md:text-5xl lg:text-6xl text-[#faf8f5] mb-8 leading-tight"
                >
                    Joanna in the World.
                </h1>

                <p
                    class="text-[#faf8f5]/80 text-lg md:text-xl max-w-2xl mx-auto leading-relaxed"
                >
                    Joanna has been featured across media, podcasts, and stages
                    as one of the leading voices on authentic leadership
                    communication. Explore selected features below.
                </p>
            </div>
        </section>

        <!-- Media Features Grid Section -->
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
                        v-for="feature in mediaFeatures"
                        :key="feature.slug"
                        :to="`/resources/media/${feature.slug}`"
                        class="group bg-[#1a1a4e]/50 backdrop-blur-sm rounded-xl border border-[#faf8f5]/10 hover:border-[#d4952a]/30 transition-all duration-300 overflow-hidden"
                    >
                        <div class="relative aspect-[16/10] overflow-hidden">
                            <img
                                :src="feature.image"
                                :alt="feature.title"
                                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />
                            <div
                                class="absolute top-4 left-4 flex items-center gap-2"
                            >
                                <span
                                    class="inline-block px-3 py-1 bg-[#d4952a] text-[#1a1a4e] text-xs font-semibold rounded-full"
                                >
                                    {{ feature.type }}
                                </span>
                            </div>
                        </div>

                        <div class="p-6">
                            <div
                                class="flex items-center gap-3 mb-3 text-sm text-[#faf8f5]/60"
                            >
                                <span>{{ feature.source }}</span>
                                <span
                                    class="w-1 h-1 rounded-full bg-[#d4952a]"
                                />
                                <span>{{ feature.date }}</span>
                            </div>

                            <h3
                                class="font-serif text-xl text-[#faf8f5] mb-3 leading-tight group-hover:text-[#d4952a] transition-colors"
                            >
                                {{ feature.title }}
                            </h3>

                            <p
                                class="text-[#faf8f5]/70 text-sm leading-relaxed line-clamp-3"
                            >
                                {{ feature.excerpt }}
                            </p>

                            <div
                                class="mt-4 flex items-center gap-2 text-[#d4952a] text-sm font-medium group-hover:gap-3 transition-all"
                            >
                                View Feature
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
