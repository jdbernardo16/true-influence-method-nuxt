<script setup lang="ts">
const route = useRoute();
const slug = route.params.slug as string;

// Mock media data - in a real app, this would come from a CMS or API
const mediaFeatures: Record<
    string,
    {
        title: string;
        source: string;
        type: string;
        date: string;
        image: string;
        url: string;
        content: string;
    }
> = {
    "forbes-council-authentic-leadership": {
        title: "The Power of Authentic Leadership Communication",
        source: "Forbes Business Council",
        type: "Article",
        date: "March 15, 2026",
        image: "/carousel/img1.webp",
        url: "#",
        content: `
            <p>In this Forbes Business Council article, Joanna explores why the most influential leaders are not the most polished—they're the most honest.</p>
            
            <p>The piece examines how authentic communication transforms leadership and creates lasting impact in organizations.</p>
            
            <h2>The Authenticity Advantage</h2>
            
            <p>Joanna argues that authenticity is not a soft skill—it's a strategic advantage. Leaders who communicate authentically build trust faster, inspire greater loyalty, and create more sustainable influence.</p>
            
            <p>The article draws on Joanna's 30 years of experience working with executives and founders across industries.</p>
            
            <h2>Key Takeaways</h2>
            
            <ul>
                <li>Authenticity builds trust more quickly than polish</li>
                <li>Vulnerability in leadership is strength, not weakness</li>
                <li>Your story is your most powerful communication tool</li>
                <li>The defining moment every leader has shapes their communication</li>
            </ul>
            
            <p>Read the full article on Forbes to discover how authentic communication can transform your leadership.</p>
        `,
    },
    "tedx-talk-true-influence": {
        title: "True Influence: Finding Your Voice",
        source: "TEDx",
        type: "Talk",
        date: "February 28, 2026",
        image: "/carousel/img3.webp",
        url: "#",
        content: `
            <p>In this powerful TEDx talk, Joanna shares insights on how authentic communication transforms leadership and creates lasting influence.</p>
            
            <p>The talk explores the journey from impact to influence—how leaders who have built something real can learn to speak about it in a way that moves rooms and creates legacy.</p>
            
            <h2>The Core Message</h2>
            
            <p>Joanna's central thesis is that your voice is your leadership. The ability to articulate your work, your values, and your vision is not optional for leaders—it's essential.</p>
            
            <p>She shares stories from her work with executives and founders, illustrating how finding your authentic voice transforms not just communication, but leadership itself.</p>
            
            <h2>Key Themes</h2>
            
            <ul>
                <li>The defining moment every leader has</li>
                <li>Why your story matters more than your script</li>
                <li>The courage of authentic communication</li>
                <li>From doing to being in leadership</li>
            </ul>
            
            <p>Watch the full TEDx talk to discover how finding your voice can transform your leadership.</p>
        `,
    },
    "leadership-podcast-episode": {
        title: "From Impact to Influence: A Conversation",
        source: "The Leadership Podcast",
        type: "Podcast",
        date: "February 15, 2026",
        image: "/carousel/img5.webp",
        url: "#",
        content: `
            <p>In this episode of The Leadership Podcast, Joanna joins host Sarah Mitchell for a deep conversation about the journey from building impact to speaking with influence.</p>
            
            <p>The conversation explores why so many capable leaders struggle to articulate their work compellingly—and how to bridge that gap.</p>
            
            <h2>Episode Highlights</h2>
            
            <p>Joanna shares insights from her 30 years of experience working with leaders, including:</p>
            
            <ul>
                <li>Why most communication training focuses on the wrong thing</li>
                <li>The interview-based process that uncovers authentic voice</li>
                <li>How to identify your defining moment as a leader</li>
                <li>The courage required for authentic communication</li>
            </ul>
            
            <h2>Key Takeaways</h2>
            
            <p>Listeners will learn practical approaches to finding their voice and speaking with greater influence, including:</p>
            
            <ul>
                <li>The difference between impact and influence</li>
                <li>Why your story matters more than your script</li>
                <li>How to prepare for high-stakes communication</li>
                <li>The role of vulnerability in leadership</li>
            </ul>
            
            <p>Listen to the full episode to discover how to transform your communication and your leadership.</p>
        `,
    },
    "harvard-business-review": {
        title: "The Defining Moment Every Leader Has",
        source: "Harvard Business Review",
        type: "Article",
        date: "January 30, 2026",
        image: "/carousel/img7.webp",
        url: "#",
        content: `
            <p>In this Harvard Business Review article, Joanna explores the concept of the defining moment—how identifying this experience transforms leadership communication.</p>
            
            <p>The piece draws on Joanna's work with executives and founders, illustrating how naming your defining moment unlocks a powerful source of communication authority.</p>
            
            <h2>The Defining Moment Concept</h2>
            
            <p>A defining moment is not just an important experience—it's a moment of transformation that fundamentally shaped your leadership, your values, and your vision.</p>
            
            <p>Joanna argues that every influential leader has such a moment, but few have named it. This unclaimed moment is a missed opportunity.</p>
            
            <h2>The Power of Naming</h2>
            
            <p>When you name your defining moment, you unlock its power. You transform it from an unconscious influence into a conscious resource.</p>
            
            <p>Your defining moment becomes the foundation of your leadership story—the source of your authentic voice and the wellspring of your conviction.</p>
            
            <h2>Practical Application</h2>
            
            <p>The article includes practical guidance for identifying your defining moment, including questions to ask yourself and approaches to reflection.</p>
            
            <ul>
                <li>What experiences shaped you as a leader?</li>
                <li>What moments stand out as turning points?</li>
                <li>What stories do you find yourself returning to?</li>
            </ul>
            
            <p>Read the full article on HBR to discover how identifying your defining moment can transform your leadership communication.</p>
        `,
    },
    "entrepreneur-magazine": {
        title: "Why Your Story Matters More Than Your Script",
        source: "Entrepreneur Magazine",
        type: "Article",
        date: "January 15, 2026",
        image: "/carousel/img2.webp",
        url: "#",
        content: `
            <p>In this Entrepreneur Magazine article, Joanna argues that the most compelling messages come from lived experience, not perfect scripts.</p>
            
            <p>The piece examines why so many leaders struggle with influence despite having built significant impact—and how shifting from script-based to story-based communication transforms results.</p>
            
            <h2>The Script Problem</h2>
            
            <p>Many leaders approach communication with a script-first mindset. They craft carefully worded messages, rehearse their delivery, and focus on getting every detail right.</p>
            
            <p>This approach has value, but it has limits. A perfect script can be technically impressive but lack emotional impact if it doesn't connect with something real in the speaker's experience.</p>
            
            <h2>Your Story as Authority</h2>
            
            <p>When you speak from your own experience, you speak with a different kind of authority. You're not just conveying information—you're sharing truth that you've lived through.</p>
            
            <p>This kind of authority cannot be manufactured. It comes from having actually experienced what you're talking about.</p>
            
            <h2>From Script to Story</h2>
            
            <p>Moving from script-based communication to story-based communication requires a shift in mindset. Instead of asking "What should I say?", ask "What is my story?"</p>
            
            <p>This is not about abandoning structure or preparation. It's about grounding your message in something real and personal.</p>
            
            <p>Read the full article on Entrepreneur to discover how shifting from script to story can transform your communication.</p>
        `,
    },
    "cnbc-interview": {
        title: "Speaking Truth to Power",
        source: "CNBC",
        type: "Interview",
        date: "December 20, 2025",
        image: "/carousel/img4.webp",
        url: "#",
        content: `
            <p>In this CNBC interview, Joanna discusses authentic communication in high-stakes business environments.</p>
            
            <p>The conversation explores how leaders can speak with truth and conviction even when the pressure is high and the stakes are significant.</p>
            
            <h2>Interview Highlights</h2>
            
            <p>Joanna shares insights on:</p>
            
            <ul>
                <li>Why authenticity matters more than polish in high-stakes situations</li>
                <li>How to prepare for boardroom presentations</li>
                <li>The role of vulnerability in executive communication</li>
                <li>Building trust through honest communication</li>
            </ul>
            
            <h2>Key Insights</h2>
            
            <p>The interview reveals that the most effective leaders in high-stakes environments are not the ones who perform perfectly—they're the ones who speak authentically.</p>
            
            <p>Joanna argues that authenticity is not a risk in high-stakes communication—it's an advantage. When you speak truthfully, you build trust more quickly and communicate with greater authority.</p>
            
            <p>Watch the full interview on CNBC to discover how authentic communication can transform your high-stakes speaking.</p>
        `,
    },
    "master-class-podcast": {
        title: "The Art of Authentic Communication",
        source: "Master Class Podcast",
        type: "Podcast",
        date: "December 5, 2025",
        image: "/carousel/img6.webp",
        url: "#",
        content: `
            <p>In this episode of the Master Class Podcast, Joanna takes a deep dive into the principles and practices of authentic leadership communication.</p>
            
            <p>The episode explores the True Influence Method™️—Joanna's signature process for helping leaders find their voice and speak with greater impact.</p>
            
            <h2>Episode Overview</h2>
            
            <p>Joanna shares the foundational principles of authentic communication, drawing on her 30 years of experience working with leaders across industries.</p>
            
            <p>The conversation covers:</p>
            
            <ul>
                <li>The difference between performance and authentic communication</li>
                <li>Why most communication training gets it wrong</li>
                <li>The interview-based process that uncovers authentic voice</li>
                <li>How to develop your signature message</li>
            </ul>
            
            <h2>Practical Takeaways</h2>
            
            <p>Listeners will learn practical approaches to authentic communication, including:</p>
            
            <ul>
                <li>How to identify your defining moment</li>
                <li>Why your story matters more than your script</li>
                <li>The courage required for authentic communication</li>
                <li>How to prepare for high-stakes speaking</li>
            </ul>
            
            <p>Listen to the full episode to discover how to transform your communication through authenticity.</p>
        `,
    },
    "fast-company-feature": {
        title: "Leaders Who Speak Their Truth",
        source: "Fast Company",
        type: "Feature",
        date: "November 18, 2025",
        image: "/carousel/img8.webp",
        url: "#",
        content: `
            <p>In this Fast Company feature, Joanna profiles leaders who have transformed their communication through authenticity.</p>
            
            <p>The piece tells the stories of executives and founders who worked with Joanna to find their voice and speak with greater impact.</p>
            
            <h2>The Leaders Profiled</h2>
            
            <p>The feature includes stories from:</p>
            
            <ul>
                <li>A CEO who discovered her defining moment and transformed her boardroom presence</li>
                <li>A founder who learned to speak from his story instead of his script</li>
                <li>An executive who found the courage to be vulnerable in high-stakes communication</li>
                <li>A leader who developed her signature message and stepped into thought leadership</li>
            </ul>
            
            <h2>The Transformation</h2>
            
            <p>Each story illustrates the same pattern: leaders who were already successful in their work but struggled to communicate it compellingly.</p>
            
            <p>Through Joanna's process, they discovered their authentic voice and learned to speak with greater authority, connection, and impact.</p>
            
            <h2>Key Insights</h2>
            
            <p>The feature reveals that authentic communication is not just about speaking better—it's about leading better.</p>
            
            <p>When leaders find their voice, they don't just communicate more effectively. They lead with greater clarity, courage, and influence.</p>
            
            <p>Read the full feature on Fast Company to discover how authentic communication can transform your leadership.</p>
        `,
    },
};

// Get the current media feature or redirect to 404
const feature = mediaFeatures[slug];

// Handle 404
if (!feature) {
    throw createError({
        statusCode: 404,
        statusMessage: "Media feature not found",
    });
}

// Set page meta
useHead({
    title: `${feature.title} — True Influence Method™️`,
    meta: [
        {
            name: "description",
            content: feature.content.replace(/<[^>]*>/g, "").substring(0, 160),
        },
    ],
});
</script>

<template>
    <div class="overflow-x-hidden">
        <!-- Hero Section -->
        <section
            class="relative min-h-[50vh] flex items-center justify-center py-20 md:py-32 overflow-hidden"
        >
            <div class="absolute inset-0">
                <img
                    :src="feature.image"
                    alt="Media feature cover"
                    class="w-full h-full object-cover"
                />
                <div
                    class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e]/95 via-[#1a1a4e]/90 to-[#1a1a4e]"
                />
            </div>

            <div class="absolute inset-0">
                <div
                    class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-[#d4952a]/5 rounded-full blur-[120px]"
                />
            </div>

            <div class="max-w-4xl mx-auto px-6 relative z-10 text-center">
                <div
                    class="mb-6 flex items-center justify-center gap-4 flex-wrap"
                >
                    <NuxtLink
                        to="/resources/media"
                        class="text-[#faf8f5]/60 hover:text-[#d4952a] transition-colors flex items-center gap-2 text-sm"
                    >
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
                            <line x1="19" y1="12" x2="5" y2="12"></line>
                            <polyline points="12 19 5 12 12 5"></polyline>
                        </svg>
                        Back to Media Features
                    </NuxtLink>
                    <span class="text-[#faf8f5]/30">|</span>
                    <span
                        class="text-[#d4952a] text-sm font-medium tracking-[0.2em] uppercase"
                    >
                        {{ feature.type }}
                    </span>
                    <span class="text-[#faf8f5]/30">|</span>
                    <span class="text-[#faf8f5]/80 text-sm">
                        {{ feature.source }}
                    </span>
                </div>

                <h1
                    class="font-serif text-3xl md:text-4xl lg:text-5xl text-[#faf8f5] mb-6 leading-tight"
                >
                    {{ feature.title }}
                </h1>

                <div
                    class="flex items-center justify-center gap-4 text-sm text-[#faf8f5]/60"
                >
                    <span>{{ feature.date }}</span>
                </div>
            </div>
        </section>

        <!-- Media Feature Content Section -->
        <section class="py-16 md:py-24 relative">
            <div
                class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e] via-[#232360] to-[#1a1a4e]"
            />

            <div class="max-w-3xl mx-auto px-6 relative z-10">
                <article>
                    <div v-html="feature.content" class="article-content" />
                </article>

                <div class="mt-12 text-center">
                    <a
                        :href="feature.url"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="inline-flex items-center gap-2 px-8 py-4 bg-[#d4952a] hover:bg-[#e8a838] text-[#1a1a4e] font-semibold rounded-lg transition-all hover:shadow-lg hover:shadow-[#d4952a]/20"
                    >
                        <span>View Original</span>
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
                            <path
                                d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"
                            ></path>
                            <polyline points="15 3 21 3 21 9"></polyline>
                            <line x1="10" y1="14" x2="21" y2="3"></line>
                        </svg>
                    </a>
                </div>
            </div>
        </section>

        <!-- Related Media Features Section -->
        <section class="py-20 md:py-32 relative">
            <div
                class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e] via-[#232360] to-[#1a1a4e]"
            />
            <div
                class="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-[#d4952a]/5 to-transparent"
            />

            <div class="max-w-7xl mx-auto px-6 relative z-10">
                <div class="text-center mb-12">
                    <h2
                        class="font-serif text-3xl md:text-4xl text-[#faf8f5] mb-4"
                    >
                        More Media Features
                    </h2>
                    <p class="text-[#faf8f5]/60 max-w-2xl mx-auto">
                        Explore more of Joanna's appearances across media,
                        podcasts, and stages.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <NuxtLink
                        v-for="(relatedFeature, relatedSlug) in mediaFeatures"
                        v-show="relatedSlug !== slug"
                        :key="relatedSlug"
                        :to="`/resources/media/${relatedSlug}`"
                        class="group bg-[#1a1a4e]/50 backdrop-blur-sm rounded-xl border border-[#faf8f5]/10 hover:border-[#d4952a]/30 transition-all duration-300 overflow-hidden"
                    >
                        <div class="relative aspect-[16/10] overflow-hidden">
                            <img
                                :src="relatedFeature.image"
                                :alt="relatedFeature.title"
                                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />
                            <div class="absolute top-4 left-4">
                                <span
                                    class="inline-block px-3 py-1 bg-[#d4952a] text-[#1a1a4e] text-xs font-semibold rounded-full"
                                >
                                    {{ relatedFeature.type }}
                                </span>
                            </div>
                        </div>

                        <div class="p-6">
                            <div
                                class="flex items-center gap-3 mb-3 text-sm text-[#faf8f5]/60"
                            >
                                <span>{{ relatedFeature.source }}</span>
                                <span
                                    class="w-1 h-1 rounded-full bg-[#d4952a]"
                                />
                                <span>{{ relatedFeature.date }}</span>
                            </div>

                            <h3
                                class="font-serif text-lg text-[#faf8f5] mb-3 leading-tight group-hover:text-[#d4952a] transition-colors"
                            >
                                {{ relatedFeature.title }}
                            </h3>

                            <div
                                class="flex items-center gap-2 text-[#d4952a] text-sm font-medium group-hover:gap-3 transition-all"
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

<style scoped>
.article-content :deep(p) {
    color: rgb(250 248 245 / 0.9);
    font-size: 1.125rem;
    line-height: 1.75;
    margin-bottom: 1.5rem;
}

.article-content :deep(h2) {
    font-family: "Playfair Display", serif;
    font-size: 1.5rem;
    line-height: 1.2;
    color: #faf8f5;
    margin-top: 3rem;
    margin-bottom: 1.5rem;
}

@media (min-width: 768px) {
    .article-content :deep(h2) {
        font-size: 1.875rem;
    }
}

.article-content :deep(h3) {
    font-family: "Playfair Display", serif;
    font-size: 1.25rem;
    line-height: 1.2;
    color: #faf8f5;
    margin-top: 2rem;
    margin-bottom: 1rem;
}

@media (min-width: 768px) {
    .article-content :deep(h3) {
        font-size: 1.5rem;
    }
}

.article-content :deep(ul),
.article-content :deep(ol) {
    list-style: disc;
    list-style-position: inside;
    color: rgb(250 248 245 / 0.9);
    font-size: 1.125rem;
    margin-bottom: 1.5rem;
}

.article-content :deep(ul) > li,
.article-content :deep(ol) > li {
    margin-top: 0.5rem;
}

.article-content :deep(li) {
    padding-left: 0.5rem;
}

.article-content :deep(blockquote) {
    border-left: 4px solid #d4952a;
    padding-left: 1.5rem;
    padding-top: 1rem;
    padding-bottom: 1rem;
    margin-top: 2rem;
    margin-bottom: 2rem;
    font-style: italic;
    color: rgb(250 248 245 / 0.8);
    font-size: 1.25rem;
}

.article-content :deep(a) {
    color: #d4952a;
    text-decoration: underline;
    text-underline-offset: 4px;
    transition: color 0.3s;
}

.article-content :deep(a:hover) {
    color: #e8a838;
}

.article-content :deep(strong) {
    color: #d4952a;
    font-weight: 600;
}
</style>
