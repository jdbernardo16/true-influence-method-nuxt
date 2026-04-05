<script setup lang="ts">
useHead({
    title: "Articles & Insights — True Influence Method™️",
    meta: [
        {
            name: "description",
            content:
                "Explore articles and insights on leadership, communication, and authentic influence from Joanna Horton McPherson.",
        },
    ],
});

const articles = [
    {
        slug: "leadership-begins-with-knowing-what-you-stand-for",
        title: "Leadership Begins With Knowing What You Stand For",
        excerpt:
            "The most powerful leaders don't just have a vision—they have a clear understanding of their values and the courage to live by them.",
        category: "Leadership",
        date: "March 15, 2026",
        readTime: "5 min read",
        image: "/carousel/img1.webp",
    },
    {
        slug: "the-art-of-authentic-communication",
        title: "The Art of Authentic Communication",
        excerpt:
            "Authenticity isn't a skill you learn—it's a truth you uncover. Here's how to find your voice and speak with genuine authority.",
        category: "Communication",
        date: "March 8, 2026",
        readTime: "7 min read",
        image: "/carousel/img2.webp",
    },
    {
        slug: "why-your-story-matters-more-than-your-script",
        title: "Why Your Story Matters More Than Your Script",
        excerpt:
            "The most compelling messages come not from perfect scripts, but from lived experience and honest reflection.",
        category: "Storytelling",
        date: "March 1, 2026",
        readTime: "6 min read",
        image: "/carousel/img3.webp",
    },
    {
        slug: "finding-courage-in-the-room",
        title: "Finding Courage in the Room",
        excerpt:
            "Speaking up in high-stakes environments requires more than preparation—it requires the bravery to be seen and heard.",
        category: "Leadership",
        date: "February 22, 2026",
        readTime: "4 min read",
        image: "/carousel/img4.webp",
    },
    {
        slug: "the-defining-moment-every-leader-has",
        title: "The Defining Moment Every Leader Has",
        excerpt:
            "Behind every great leader is a moment that shaped them. Naming this moment is the first step to owning your message.",
        category: "Leadership",
        date: "February 15, 2026",
        readTime: "8 min read",
        image: "/carousel/img5.webp",
    },
    {
        slug: "from-impact-to-influence",
        title: "From Impact to Influence",
        excerpt:
            "You've built something real. Now it's time to speak about it in a way that creates lasting change and builds trust.",
        category: "Communication",
        date: "February 8, 2026",
        readTime: "5 min read",
        image: "/carousel/img6.webp",
    },
    {
        slug: "the-myth-of-the-perfect-speaker",
        title: "The Myth of the Perfect Speaker",
        excerpt:
            "Perfection isn't the goal of great speaking. Connection is. Here's why vulnerability is your greatest strength.",
        category: "Speaking",
        date: "February 1, 2026",
        readTime: "6 min read",
        image: "/carousel/img7.webp",
    },
    {
        slug: "leading-with-emotional-intelligence",
        title: "Leading With Emotional Intelligence",
        excerpt:
            "The most influential leaders understand that logic alone doesn't move people—emotion does. Here's how to harness both.",
        category: "Leadership",
        date: "January 25, 2026",
        readTime: "7 min read",
        image: "/carousel/img8.webp",
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
                    src="/carousel/img1.webp"
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
                        Articles & Insights
                    </span>
                </div>

                <h1
                    class="font-serif text-4xl md:text-5xl lg:text-6xl text-[#faf8f5] mb-8 leading-tight"
                >
                    Leadership Begins With Knowing What You Stand For.
                </h1>

                <p
                    class="text-[#faf8f5]/80 text-lg md:text-xl max-w-2xl mx-auto leading-relaxed"
                >
                    Joanna writes about the intersection of leadership,
                    communication, and authentic influence. Her articles explore
                    the questions that matter most to founders, CEOs, and
                    mission-driven leaders.
                </p>
            </div>
        </section>

        <!-- Articles Grid Section -->
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
                        v-for="article in articles"
                        :key="article.slug"
                        :to="`/resources/articles/${article.slug}`"
                        class="group bg-[#1a1a4e]/50 backdrop-blur-sm rounded-xl border border-[#faf8f5]/10 hover:border-[#d4952a]/30 transition-all duration-300 overflow-hidden"
                    >
                        <div class="relative aspect-[16/10] overflow-hidden">
                            <img
                                :src="article.image"
                                :alt="article.title"
                                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />
                            <div class="absolute top-4 left-4">
                                <span
                                    class="inline-block px-3 py-1 bg-[#d4952a] text-[#1a1a4e] text-xs font-semibold rounded-full"
                                >
                                    {{ article.category }}
                                </span>
                            </div>
                        </div>

                        <div class="p-6">
                            <div
                                class="flex items-center gap-3 mb-3 text-sm text-[#faf8f5]/60"
                            >
                                <span>{{ article.date }}</span>
                                <span
                                    class="w-1 h-1 rounded-full bg-[#d4952a]"
                                />
                                <span>{{ article.readTime }}</span>
                            </div>

                            <h3
                                class="font-serif text-xl text-[#faf8f5] mb-3 leading-tight group-hover:text-[#d4952a] transition-colors"
                            >
                                {{ article.title }}
                            </h3>

                            <p
                                class="text-[#faf8f5]/70 text-sm leading-relaxed line-clamp-3"
                            >
                                {{ article.excerpt }}
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
