<script setup lang="ts">
useHead({
    title: "Blog & Podcast — True Influence Method™️",
    meta: [
        {
            name: "description",
            content:
                "Joanna's blog and podcast appearances go deep—exploring the stories, strategies, and honest reflections of leaders who have found their voice.",
        },
    ],
});

const blogPosts = [
    {
        slug: "conversation-with-ceo-on-authenticity",
        title: "A Conversation on Authenticity in Leadership",
        type: "Blog Post",
        date: "March 18, 2026",
        readTime: "8 min read",
        excerpt:
            "An honest conversation with a Fortune 500 CEO about the journey to authentic communication.",
        image: "/carousel/img2.webp",
    },
    {
        slug: "podcast-episode-emotional-intelligence",
        title: "Emotional Intelligence in Leadership Communication",
        type: "Podcast",
        date: "March 10, 2026",
        readTime: "45 min listen",
        excerpt:
            "A deep dive into how emotional intelligence transforms leadership communication.",
        image: "/carousel/img4.webp",
    },
    {
        slug: "blog-defining-moments",
        title: "The Defining Moments That Shape Us",
        type: "Blog Post",
        date: "March 2, 2026",
        readTime: "6 min read",
        excerpt:
            "Exploring how identifying your defining moment transforms your leadership journey.",
        image: "/carousel/img6.webp",
    },
    {
        slug: "podcast-episode-courage",
        title: "The Courage to Speak Your Truth",
        type: "Podcast",
        date: "February 24, 2026",
        readTime: "52 min listen",
        excerpt:
            "A conversation about what it takes to speak authentically in high-stakes environments.",
        image: "/carousel/img8.webp",
    },
    {
        slug: "blog-vulnerability-strength",
        title: "Vulnerability as Leadership Strength",
        type: "Blog Post",
        date: "February 16, 2026",
        readTime: "7 min read",
        excerpt:
            "Why vulnerability is not weakness—it's the foundation of authentic influence.",
        image: "/carousel/img1.webp",
    },
    {
        slug: "podcast-episode-storytelling",
        title: "The Power of Story in Leadership",
        type: "Podcast",
        date: "February 8, 2026",
        readTime: "48 min listen",
        excerpt:
            "How leaders can use storytelling to create connection and inspire action.",
        image: "/carousel/img3.webp",
    },
    {
        slug: "blog-listening-communication",
        title: "Listening as a Leadership Superpower",
        type: "Blog Post",
        date: "January 30, 2026",
        readTime: "5 min read",
        excerpt:
            "The most influential leaders are often the best listeners. Here's why.",
        image: "/carousel/img5.webp",
    },
    {
        slug: "podcast-episode-legacy",
        title: "Building a Legacy Through Your Voice",
        type: "Podcast",
        date: "January 22, 2026",
        readTime: "55 min listen",
        excerpt:
            "A conversation about how your voice shapes your leadership legacy.",
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
                    src="/carousel/img4.webp"
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
                        Blog & Podcast
                    </span>
                </div>

                <h1
                    class="font-serif text-4xl md:text-5xl lg:text-6xl text-[#faf8f5] mb-8 leading-tight"
                >
                    Conversations Worth Having.
                </h1>

                <p
                    class="text-[#faf8f5]/80 text-lg md:text-xl max-w-2xl mx-auto leading-relaxed"
                >
                    Joanna's blog and podcast appearances go deep—exploring the
                    stories, strategies, and honest reflections of leaders who
                    have done the work and found their voice.
                </p>
            </div>
        </section>

        <!-- Blog Posts Grid Section -->
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
                        v-for="post in blogPosts"
                        :key="post.slug"
                        :to="`/resources/blog/${post.slug}`"
                        class="group bg-[#1a1a4e]/50 backdrop-blur-sm rounded-xl border border-[#faf8f5]/10 hover:border-[#d4952a]/30 transition-all duration-300 overflow-hidden"
                    >
                        <div class="relative aspect-[16/10] overflow-hidden">
                            <img
                                :src="post.image"
                                :alt="post.title"
                                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />
                            <div class="absolute top-4 left-4">
                                <span
                                    class="inline-block px-3 py-1 bg-[#d4952a] text-[#1a1a4e] text-xs font-semibold rounded-full"
                                >
                                    {{ post.type }}
                                </span>
                            </div>
                        </div>

                        <div class="p-6">
                            <div
                                class="flex items-center gap-3 mb-3 text-sm text-[#faf8f5]/60"
                            >
                                <span>{{ post.date }}</span>
                                <span
                                    class="w-1 h-1 rounded-full bg-[#d4952a]"
                                />
                                <span>{{ post.readTime }}</span>
                            </div>

                            <h3
                                class="font-serif text-xl text-[#faf8f5] mb-3 leading-tight group-hover:text-[#d4952a] transition-colors"
                            >
                                {{ post.title }}
                            </h3>

                            <p
                                class="text-[#faf8f5]/70 text-sm leading-relaxed line-clamp-3"
                            >
                                {{ post.excerpt }}
                            </p>

                            <div
                                class="mt-4 flex items-center gap-2 text-[#d4952a] text-sm font-medium group-hover:gap-3 transition-all"
                            >
                                {{
                                    post.type === "Podcast"
                                        ? "Listen Now"
                                        : "Read More"
                                }}
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
