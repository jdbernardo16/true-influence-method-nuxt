<template>
    <div class="overflow-x-hidden">
        <!-- Hero -->
        <section
            class="relative py-20 flex items-center justify-center overflow-hidden"
        >
            <div
                class="absolute inset-0 bg-gradient-to-br from-[#1a1a4e] via-[#232360] to-[#1a1a4e]"
            />

            <!-- Decorative elements -->
            <div
                class="absolute top-20 right-10 w-96 h-96 bg-[#d4952a]/10 rounded-full blur-[120px]"
            />
            <div
                class="absolute bottom-20 left-10 w-72 h-72 bg-[#232360]/50 rounded-full blur-[100px]"
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
                <!-- Journey Image - Suggestion: Abstract representation of a path or journey -->
                <div class="relative mb-12 inline-block">
                    <div
                        class="absolute inset-0 bg-[#d4952a] blur-[60px] opacity-20 rounded-full"
                    />
                    <img
                        src="https://picsum.photos/500/300?random=4"
                        alt="Journey visualization - Suggestion: Path winding through mountains or a road forward"
                        class="w-64 h-40 md:w-80 md:h-48 rounded-2xl object-cover relative z-10 shadow-2xl"
                    />
                </div>

                <span
                    class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-8"
                >
                    <span
                        class="w-2 h-2 bg-[#d4952a] rounded-full animate-pulse"
                    />
                    The Process
                </span>

                <h1
                    class="font-serif text-4xl md:text-6xl text-[#faf8f5] mb-8 leading-tight"
                >
                    A Process Rooted in Truth.
                    <br />
                    <span class="text-[#d4952a]">Built Around You.</span>
                </h1>

                <div class="max-w-3xl mx-auto">
                    <p
                        class="text-[#faf8f5]/80 text-lg md:text-xl leading-relaxed"
                    >
                        The True Influence Method™️ is not a framework you slot
                        yourself into. It's a living process — responsive, deep,
                        and entirely grounded in who you are. It moves through
                        five phases, each building on the last, until your
                        message and your delivery are one.
                    </p>
                </div>
            </div>
        </section>

        <!-- The 5 Phases -->
        <section
            class="py-24 md:py-32 bg-[#faf8f5] text-[#1a1a4e] relative overflow-hidden"
        >
            <div
                class="absolute top-0 left-0 w-96 h-96 bg-[#d4952a]/5 rounded-full blur-[120px]"
            />

            <div class="max-w-7xl mx-auto px-6 relative z-10">
                <div class="text-center mb-20">
                    <div
                        class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-8"
                    >
                        The 5-Phase Journey
                    </div>
                    <h2 class="font-serif text-4xl md:text-6xl text-[#1a1a4e]">
                        From Discovering Your Story
                        <br />
                        <span class="text-[#d4952a]">to Leading With It.</span>
                    </h2>
                </div>

                <!-- Phase 1 -->
                <div class="grid lg:grid-cols-2 gap-16 items-center mb-24">
                    <div class="relative order-2 lg:order-1">
                        <div
                            class="relative rounded-2xl overflow-hidden shadow-2xl"
                        >
                            <img
                                src="https://picsum.photos/600/500?random=5"
                                alt="Discover Phase - Suggestion: Light bulb moment, someone having an epiphany, or uncovering hidden treasure"
                                class="w-full h-[450px] object-cover"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/70 to-transparent"
                            />

                            <div class="absolute bottom-0 left-0 right-0 p-8">
                                <div
                                    class="bg-[#d4952a] text-[#1a1a4e] px-6 py-3 rounded-lg inline-block"
                                >
                                    <span class="font-bold text-2xl">01</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="order-1 lg:order-2">
                        <div
                            class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-6"
                        >
                            Phase One
                        </div>

                        <h3
                            class="font-serif text-3xl md:text-4xl text-[#1a1a4e] mb-4"
                        >
                            Discover
                        </h3>
                        <p class="text-[#d4952a] text-lg font-medium mb-6">
                            The Defining Moment
                        </p>

                        <p class="text-[#1a1a4e]/80 text-lg leading-relaxed">
                            Before any message can be crafted, the truth must be
                            found. In this phase, Joanna's interview-based
                            process uncovers the defining moment behind your
                            work — the experience that shaped your leadership,
                            your values, and your vision. Most leaders have
                            never named it. This is where it surfaces.
                        </p>
                    </div>
                </div>

                <!-- Phase 2 -->
                <div class="grid lg:grid-cols-2 gap-16 items-center mb-24">
                    <div>
                        <div
                            class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-6"
                        >
                            Phase Two
                        </div>

                        <h3
                            class="font-serif text-3xl md:text-4xl text-[#1a1a4e] mb-4"
                        >
                            Clarify
                        </h3>
                        <p class="text-[#d4952a] text-lg font-medium mb-6">
                            Your Core Message
                        </p>

                        <p class="text-[#1a1a4e]/80 text-lg leading-relaxed">
                            From your story, we build your message. Not a
                            tagline. Not an elevator pitch. A clear, resonant
                            expression of who you are, what you stand for, and
                            why it matters — articulated in language that is
                            authentically yours and unmistakably powerful.
                        </p>
                    </div>

                    <div class="relative">
                        <div
                            class="relative rounded-2xl overflow-hidden shadow-2xl"
                        >
                            <img
                                src="https://picsum.photos/600/500?random=6"
                                alt="Clarify Phase - Suggestion: Clear light beam, crystal prism, or someone gaining clarity and focus"
                                class="w-full h-[450px] object-cover"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/70 to-transparent"
                            />

                            <div class="absolute bottom-0 left-0 right-0 p-8">
                                <div
                                    class="bg-[#d4952a] text-[#1a1a4e] px-6 py-3 rounded-lg inline-block"
                                >
                                    <span class="font-bold text-2xl">02</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Phase 3 -->
                <div class="grid lg:grid-cols-2 gap-16 items-center mb-24">
                    <div class="relative order-2 lg:order-1">
                        <div
                            class="relative rounded-2xl overflow-hidden shadow-2xl"
                        >
                            <img
                                src="https://picsum.photos/600/500?random=7"
                                alt="Craft Phase - Suggestion: Artisan working, architect designing, or hands crafting something beautiful"
                                class="w-full h-[450px] object-cover"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/70 to-transparent"
                            />

                            <div class="absolute bottom-0 left-0 right-0 p-8">
                                <div
                                    class="bg-[#d4952a] text-[#1a1a4e] px-6 py-3 rounded-lg inline-block"
                                >
                                    <span class="font-bold text-2xl">03</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="order-1 lg:order-2">
                        <div
                            class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-6"
                        >
                            Phase Three
                        </div>

                        <h3
                            class="font-serif text-3xl md:text-4xl text-[#1a1a4e] mb-4"
                        >
                            Craft
                        </h3>
                        <p class="text-[#d4952a] text-lg font-medium mb-6">
                            Your Signature Talk or Narrative
                        </p>

                        <p class="text-[#1a1a4e]/80 text-lg leading-relaxed">
                            With your message clear, we build the structure.
                            Whether it's a keynote, a leadership narrative, or a
                            brand story, this phase gives shape to your message
                            — emotional arc, strategic structure, and the
                            stories that bring it to life.
                        </p>
                    </div>
                </div>

                <!-- Phase 4 -->
                <div class="grid lg:grid-cols-2 gap-16 items-center mb-24">
                    <div>
                        <div
                            class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-6"
                        >
                            Phase Four
                        </div>

                        <h3
                            class="font-serif text-3xl md:text-4xl text-[#1a1a4e] mb-4"
                        >
                            Deliver
                        </h3>
                        <p class="text-[#d4952a] text-lg font-medium mb-6">
                            Voice, Presence & Authority
                        </p>

                        <p class="text-[#1a1a4e]/80 text-lg leading-relaxed">
                            A message is only as powerful as its delivery. In
                            this phase, we train your body, your voice, and your
                            presence — so that when you speak, the message lands
                            not just intellectually but emotionally. This is
                            where authority becomes embodied.
                        </p>
                    </div>

                    <div class="relative">
                        <div
                            class="relative rounded-2xl overflow-hidden shadow-2xl"
                        >
                            <img
                                src="https://picsum.photos/600/500?random=8"
                                alt="Deliver Phase - Suggestion: Powerful speaker on stage, commanding presence, or microphone in spotlight"
                                class="w-full h-[450px] object-cover"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/70 to-transparent"
                            />

                            <div class="absolute bottom-0 left-0 right-0 p-8">
                                <div
                                    class="bg-[#d4952a] text-[#1a1a4e] px-6 py-3 rounded-lg inline-block"
                                >
                                    <span class="font-bold text-2xl">04</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Phase 5 -->
                <div class="grid lg:grid-cols-2 gap-16 items-center">
                    <div class="relative order-2 lg:order-1">
                        <div
                            class="relative rounded-2xl overflow-hidden shadow-2xl"
                        >
                            <img
                                src="https://picsum.photos/600/500?random=9"
                                alt="Lead Phase - Suggestion: Leader inspiring others, ripple effect, or someone making impact on many"
                                class="w-full h-[450px] object-cover"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/70 to-transparent"
                            />

                            <div class="absolute bottom-0 left-0 right-0 p-8">
                                <div
                                    class="bg-[#d4952a] text-[#1a1a4e] px-6 py-3 rounded-lg inline-block"
                                >
                                    <span class="font-bold text-2xl">05</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="order-1 lg:order-2">
                        <div
                            class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-6"
                        >
                            Phase Five
                        </div>

                        <h3
                            class="font-serif text-3xl md:text-4xl text-[#1a1a4e] mb-4"
                        >
                            Lead
                        </h3>
                        <p class="text-[#d4952a] text-lg font-medium mb-6">
                            Thought Leadership & Lasting Impact
                        </p>

                        <p class="text-[#1a1a4e]/80 text-lg leading-relaxed">
                            The final phase is about integration and
                            amplification. You step fully into your role as a
                            thought leader — speaking in rooms, on stages, in
                            media — with a message that is clear, consistent,
                            and creates lasting influence.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Process Callout -->
        <section
            class="py-24 md:py-32 bg-gradient-to-br from-[#1a1a4e] via-[#232360] to-[#1a1a4e] relative overflow-hidden"
        >
            <div class="absolute inset-0 overflow-hidden">
                <div
                    v-for="i in 20"
                    :key="`callout-${i}`"
                    class="absolute w-1 h-1 bg-[#d4952a]/20 rounded-full animate-float"
                    :style="{
                        left: `${Math.random() * 100}%`,
                        top: `${Math.random() * 100}%`,
                        animationDelay: `${Math.random() * 5}s`,
                        animationDuration: `${8 + Math.random() * 4}s`,
                    }"
                />
            </div>

            <div class="max-w-6xl mx-auto px-6 relative z-10">
                <div class="grid lg:grid-cols-2 gap-16 items-center">
                    <div>
                        <div
                            class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-8"
                        >
                            Not Coaching
                        </div>

                        <h2
                            class="font-serif text-4xl md:text-5xl text-[#faf8f5] mb-8 leading-tight"
                        >
                            This Is Not Coaching.
                            <br />
                            <span class="text-[#d4952a]">
                                It's Transformation.
                            </span>
                        </h2>

                        <p
                            class="text-[#faf8f5]/80 text-lg md:text-xl leading-relaxed mb-8"
                        >
                            Clients often arrive expecting a structured program
                            with deliverables and timelines. What they find is
                            something more powerful — a process that meets them
                            exactly where they are, surfaces what has always
                            been true, and gives them the tools to lead from it.
                        </p>
                    </div>

                    <div class="relative">
                        <!-- Testimonial Image - Suggestion: Warm, intimate shot of a client or group photo showing transformation -->
                        <div
                            class="relative rounded-2xl overflow-hidden shadow-2xl"
                        >
                            <img
                                src="https://picsum.photos/600/500?random=10"
                                alt="Client transformation - Suggestion: Photo showing authentic connection and breakthrough moment"
                                class="w-full h-[400px] object-cover"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />

                            <div class="absolute bottom-0 left-0 right-0 p-8">
                                <div
                                    class="bg-[#faf8f5] p-6 rounded-xl backdrop-blur-sm"
                                >
                                    <blockquote
                                        class="font-serif text-[#1a1a4e] text-lg italic"
                                    >
                                        "At first, I honestly wanted to quit. I
                                        was expecting a traditional approach.
                                        But Joanna focused on me — on where I
                                        come from, who I am. By the end, I
                                        didn't just have one story. I had
                                        several. And the confidence to deliver
                                        them in a way that captivates an
                                        audience, just like a scene in a movie."
                                    </blockquote>
                                    <p class="text-[#d4952a] font-medium mt-4">
                                        — Private Training Client, CEO
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Journey CTA -->
        <section
            class="py-24 md:py-32 bg-[#faf8f5] text-[#1a1a4e] relative overflow-hidden"
        >
            <div
                class="absolute bottom-0 right-0 w-96 h-96 bg-[#232360]/10 rounded-full blur-[120px]"
            />

            <div class="max-w-4xl mx-auto px-6 text-center relative z-10">
                <div class="mb-12">
                    <!-- Journey Complete Image - Suggestion: Sunrise, open door, or horizon representing new beginnings -->
                    <div class="relative inline-block">
                        <div
                            class="absolute inset-0 bg-[#d4952a] blur-[60px] opacity-20 rounded-full"
                        />
                        <img
                            src="https://picsum.photos/400/250?random=11"
                            alt="Begin your journey - Suggestion: Beautiful sunrise or open path forward"
                            class="w-64 h-40 rounded-2xl object-cover relative z-10 shadow-2xl"
                        />
                    </div>
                </div>

                <div
                    class="inline-flex items-center gap-2 bg-[#d4952a]/10 border border-[#d4952a]/30 text-[#d4952a] text-xs font-bold tracking-[0.2em] uppercase px-4 py-2 rounded-full mb-8"
                >
                    Begin Now
                </div>

                <h2 class="font-serif text-4xl md:text-6xl text-[#1a1a4e] mb-6">
                    Where Would You Like to Begin?
                </h2>
                <p
                    class="text-[#1a1a4e]/80 text-lg md:text-xl mb-12 max-w-2xl mx-auto"
                >
                    Every journey through the True Influence Method™️ starts
                    with a conversation. Let us know where you are and where you
                    want to go — and Joanna's team will guide you to the right
                    path.
                </p>

                <NuxtLink
                    to="/apply"
                    class="inline-flex items-center gap-3 px-10 py-5 bg-[#d4952a] hover:bg-[#e8a838] text-[#1a1a4e] font-semibold rounded-lg transition-all hover:shadow-xl hover:shadow-[#d4952a]/20 text-lg group"
                >
                    Start the Conversation
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="20"
                        height="20"
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
                </NuxtLink>
            </div>
        </section>
    </div>
</template>

<script setup lang="ts">
useHead({
    title: "The Journey | True Influence Method™️",
    meta: [
        {
            name: "description",
            content:
                "Discover the True Influence Method™️ journey through five transformative phases: Discover, Clarify, Craft, Deliver, and Lead. Find your authentic voice and create lasting impact.",
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

.animate-float {
    animation: float 8s ease-in-out infinite;
}
</style>
