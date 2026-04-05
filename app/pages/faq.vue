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
                    Frequently Asked Questions
                </span>

                <h1
                    class="font-serif text-4xl md:text-6xl text-[#faf8f5] mb-8 leading-tight"
                >
                    Your Questions, Answered.
                </h1>

                <div class="max-w-3xl mx-auto">
                    <p
                        class="text-[#faf8f5]/80 text-lg md:text-xl leading-relaxed"
                    >
                        If you have a question that isn't answered here,
                        Joanna's team is always happy to help. Reach out via the
                        contact form or submit your application and we'll be in
                        touch.
                    </p>
                </div>
            </div>
        </section>

        <!-- FAQ Questions & Answers -->
        <section
            class="py-24 md:py-32 bg-[#faf8f5] text-[#1a1a4e] relative overflow-hidden"
        >
            <div
                class="absolute top-0 right-0 w-96 h-96 bg-[#d4952a]/5 rounded-full blur-[120px]"
            />

            <div class="max-w-4xl mx-auto px-6 relative z-10">
                <div class="space-y-6">
                    <!-- FAQ Item 1 -->
                    <div
                        class="bg-white rounded-2xl shadow-lg overflow-hidden border border-[#d4952a]/10"
                    >
                        <button
                            @click="toggleFaq(0)"
                            class="w-full px-8 py-6 flex items-center justify-between text-left hover:bg-[#faf8f5]/50 transition-colors"
                        >
                            <span
                                class="font-serif text-xl md:text-2xl text-[#1a1a4e] pr-4"
                            >
                                Who is the True Influence Method™️ designed for?
                            </span>
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
                                class="text-[#d4952a] flex-shrink-0 transition-transform duration-300"
                                :class="openFaqs[0] ? 'rotate-180' : ''"
                            >
                                <path d="m6 9 6 6 6-6" />
                            </svg>
                        </button>
                        <Transition name="faq">
                            <div v-if="openFaqs[0]" class="px-8 pb-6">
                                <p
                                    class="text-[#1a1a4e]/70 text-lg leading-relaxed"
                                >
                                    Joanna works primarily with founders, CEOs,
                                    executives, and mission-driven leaders who
                                    have built something meaningful and are
                                    ready to articulate it — to rooms, boards,
                                    media, and the world. Her Speak & Rise group
                                    program welcomes a broader range of emerging
                                    and established leaders. Her corporate
                                    programs serve leadership teams at every
                                    level.
                                </p>
                            </div>
                        </Transition>
                    </div>

                    <!-- FAQ Item 2 -->
                    <div
                        class="bg-white rounded-2xl shadow-lg overflow-hidden border border-[#d4952a]/10"
                    >
                        <button
                            @click="toggleFaq(1)"
                            class="w-full px-8 py-6 flex items-center justify-between text-left hover:bg-[#faf8f5]/50 transition-colors"
                        >
                            <span
                                class="font-serif text-xl md:text-2xl text-[#1a1a4e] pr-4"
                            >
                                What makes this different from traditional
                                speaking coaching?
                            </span>
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
                                class="text-[#d4952a] flex-shrink-0 transition-transform duration-300"
                                :class="openFaqs[1] ? 'rotate-180' : ''"
                            >
                                <path d="m6 9 6 6 6-6" />
                            </svg>
                        </button>
                        <Transition name="faq">
                            <div v-if="openFaqs[1]" class="px-8 pb-6">
                                <p
                                    class="text-[#1a1a4e]/70 text-lg leading-relaxed"
                                >
                                    Most coaching starts with the speech. Joanna
                                    starts with you. Through her signature
                                    interview-based process, she surfaces the
                                    truth behind your work — the defining
                                    moment, the real message, the lived
                                    experience that makes a leader worth
                                    following. What you get is not a polished
                                    performance. It is your actual voice.
                                </p>
                            </div>
                        </Transition>
                    </div>

                    <!-- FAQ Item 3 -->
                    <div
                        class="bg-white rounded-2xl shadow-lg overflow-hidden border border-[#d4952a]/10"
                    >
                        <button
                            @click="toggleFaq(2)"
                            class="w-full px-8 py-6 flex items-center justify-between text-left hover:bg-[#faf8f5]/50 transition-colors"
                        >
                            <span
                                class="font-serif text-xl md:text-2xl text-[#1a1a4e] pr-4"
                            >
                                I'm not sure which program is right for me. How
                                do I decide?
                            </span>
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
                                class="text-[#d4952a] flex-shrink-0 transition-transform duration-300"
                                :class="openFaqs[2] ? 'rotate-180' : ''"
                            >
                                <path d="m6 9 6 6 6-6" />
                            </svg>
                        </button>
                        <Transition name="faq">
                            <div v-if="openFaqs[2]" class="px-8 pb-6">
                                <p
                                    class="text-[#1a1a4e]/70 text-lg leading-relaxed"
                                >
                                    The best first step is completing Joanna's
                                    private client inquiry form. Once she and
                                    her team have a sense of your goals, your
                                    timeline, and where you are in your
                                    leadership journey, they will guide you to
                                    the right path. There is no pressure — just
                                    a conversation.
                                </p>
                            </div>
                        </Transition>
                    </div>

                    <!-- FAQ Item 4 -->
                    <div
                        class="bg-white rounded-2xl shadow-lg overflow-hidden border border-[#d4952a]/10"
                    >
                        <button
                            @click="toggleFaq(3)"
                            class="w-full px-8 py-6 flex items-center justify-between text-left hover:bg-[#faf8f5]/50 transition-colors"
                        >
                            <span
                                class="font-serif text-xl md:text-2xl text-[#1a1a4e] pr-4"
                            >
                                What does Private Training involve, and how long
                                does it take?
                            </span>
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
                                class="text-[#d4952a] flex-shrink-0 transition-transform duration-300"
                                :class="openFaqs[3] ? 'rotate-180' : ''"
                            >
                                <path d="m6 9 6 6 6-6" />
                            </svg>
                        </button>
                        <Transition name="faq">
                            <div v-if="openFaqs[3]" class="px-8 pb-6">
                                <p
                                    class="text-[#1a1a4e]/70 text-lg leading-relaxed"
                                >
                                    Private Training is a 90-day engagement with
                                    Joanna, structured around 4 to 14 sessions
                                    depending on the level you choose
                                    (Beginning, Intermediate, or Advanced).
                                    During that time, you also join Joanna's
                                    quarterly Mastermind & Retreat. Most clients
                                    describe it as the most transformative
                                    professional work they've ever done.
                                </p>
                            </div>
                        </Transition>
                    </div>

                    <!-- FAQ Item 5 -->
                    <div
                        class="bg-white rounded-2xl shadow-lg overflow-hidden border border-[#d4952a]/10"
                    >
                        <button
                            @click="toggleFaq(4)"
                            class="w-full px-8 py-6 flex items-center justify-between text-left hover:bg-[#faf8f5]/50 transition-colors"
                        >
                            <span
                                class="font-serif text-xl md:text-2xl text-[#1a1a4e] pr-4"
                            >
                                What is Speak & Rise and who is it for?
                            </span>
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
                                class="text-[#d4952a] flex-shrink-0 transition-transform duration-300"
                                :class="openFaqs[4] ? 'rotate-180' : ''"
                            >
                                <path d="m6 9 6 6 6-6" />
                            </svg>
                        </button>
                        <Transition name="faq">
                            <div v-if="openFaqs[4]" class="px-8 pb-6">
                                <p
                                    class="text-[#1a1a4e]/70 text-lg leading-relaxed"
                                >
                                    Speak & Rise is Joanna's group training
                                    program — the most accessible entry into the
                                    True Influence Method™️. It includes live
                                    sessions with Joanna, story development
                                    work, peer community, and access to The
                                    Vault. The 90-Day Mastermind & Retreat
                                    starts from $6,000. It is ideal for leaders
                                    who are ready to develop their voice and
                                    want to do so within a community.
                                </p>
                            </div>
                        </Transition>
                    </div>

                    <!-- FAQ Item 6 -->
                    <div
                        class="bg-white rounded-2xl shadow-lg overflow-hidden border border-[#d4952a]/10"
                    >
                        <button
                            @click="toggleFaq(5)"
                            class="w-full px-8 py-6 flex items-center justify-between text-left hover:bg-[#faf8f5]/50 transition-colors"
                        >
                            <span
                                class="font-serif text-xl md:text-2xl text-[#1a1a4e] pr-4"
                            >
                                Do you work with companies and organizations?
                            </span>
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
                                class="text-[#d4952a] flex-shrink-0 transition-transform duration-300"
                                :class="openFaqs[5] ? 'rotate-180' : ''"
                            >
                                <path d="m6 9 6 6 6-6" />
                            </svg>
                        </button>
                        <Transition name="faq">
                            <div v-if="openFaqs[5]" class="px-8 pb-6">
                                <p
                                    class="text-[#1a1a4e]/70 text-lg leading-relaxed"
                                >
                                    Yes. Joanna offers fully customized
                                    corporate programs including workshops,
                                    executive communication intensives, and the
                                    True Influence License — for organizations
                                    who want to embed the True Influence
                                    Method™️ in-house with their own
                                    facilitators. Pricing is custom based on
                                    scope and team size.
                                </p>
                            </div>
                        </Transition>
                    </div>

                    <!-- FAQ Item 7 -->
                    <div
                        class="bg-white rounded-2xl shadow-lg overflow-hidden border border-[#d4952a]/10"
                    >
                        <button
                            @click="toggleFaq(6)"
                            class="w-full px-8 py-6 flex items-center justify-between text-left hover:bg-[#faf8f5]/50 transition-colors"
                        >
                            <span
                                class="font-serif text-xl md:text-2xl text-[#1a1a4e] pr-4"
                            >
                                What results can I expect?
                            </span>
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
                                class="text-[#d4952a] flex-shrink-0 transition-transform duration-300"
                                :class="openFaqs[6] ? 'rotate-180' : ''"
                            >
                                <path d="m6 9 6 6 6-6" />
                            </svg>
                        </button>
                        <Transition name="faq">
                            <div v-if="openFaqs[6]" class="px-8 pb-6">
                                <p
                                    class="text-[#1a1a4e]/70 text-lg leading-relaxed"
                                >
                                    Every client journey is different, but
                                    common outcomes include: a clearly
                                    articulated leadership message, a signature
                                    talk or narrative, increased confidence
                                    speaking in high-stakes settings, stronger
                                    presence in rooms and on stages, and a
                                    deeper sense of ownership over their story
                                    and impact. Many clients describe a shift
                                    that extends far beyond communication — into
                                    how they lead, how they're seen, and what
                                    they believe is possible.
                                </p>
                            </div>
                        </Transition>
                    </div>

                    <!-- FAQ Item 8 -->
                    <div
                        class="bg-white rounded-2xl shadow-lg overflow-hidden border border-[#d4952a]/10"
                    >
                        <button
                            @click="toggleFaq(7)"
                            class="w-full px-8 py-6 flex items-center justify-between text-left hover:bg-[#faf8f5]/50 transition-colors"
                        >
                            <span
                                class="font-serif text-xl md:text-2xl text-[#1a1a4e] pr-4"
                            >
                                How do I get started?
                            </span>
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
                                class="text-[#d4952a] flex-shrink-0 transition-transform duration-300"
                                :class="openFaqs[7] ? 'rotate-180' : ''"
                            >
                                <path d="m6 9 6 6 6-6" />
                            </svg>
                        </button>
                        <Transition name="faq">
                            <div v-if="openFaqs[7]" class="px-8 pb-6">
                                <p
                                    class="text-[#1a1a4e]/70 text-lg leading-relaxed"
                                >
                                    Fill out the private client inquiry form.
                                    Joanna's team will review your submission
                                    and reach out to schedule a consultation.
                                    From there, you'll have everything you need
                                    to decide on the right path forward.
                                </p>
                            </div>
                        </Transition>
                    </div>
                </div>
            </div>
        </section>

        <!-- FAQ CTA -->
        <section
            class="py-24 md:py-32 bg-gradient-to-br from-[#1a1a4e] via-[#232360] to-[#1a1a4e] relative overflow-hidden"
        >
            <div class="absolute inset-0 overflow-hidden">
                <div
                    v-for="i in 10"
                    :key="`cta-${i}`"
                    class="absolute w-2 h-2 bg-[#d4952a]/20 rounded-full animate-float"
                    :style="{
                        left: `${Math.random() * 100}%`,
                        top: `${Math.random() * 100}%`,
                        animationDelay: `${Math.random() * 5}s`,
                        animationDuration: `${7 + Math.random() * 4}s`,
                    }"
                />
            </div>

            <div class="max-w-4xl mx-auto px-6 text-center relative z-10">
                <div class="mb-12">
                    <div class="relative inline-block">
                        <div
                            class="absolute inset-0 bg-[#d4952a] blur-[60px] opacity-20 rounded-full"
                        />
                        <img
                            src="/icononly_transparent_nobuffer.png"
                            alt="Logo"
                            class="w-32 h-32 object-contain relative z-10"
                        />
                    </div>
                </div>

                <h2 class="font-serif text-4xl md:text-6xl text-[#faf8f5] mb-6">
                    Still Have Questions?
                </h2>
                <p
                    class="text-[#faf8f5]/80 text-lg md:text-xl mb-12 max-w-2xl mx-auto"
                >
                    Joanna's team is happy to answer anything not covered here.
                    Reach out directly or submit your application and someone
                    will be in touch shortly.
                </p>

                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <NuxtLink
                        to="/apply"
                        class="group px-8 py-4 bg-[#d4952a] hover:bg-[#e8a838] text-[#1a1a4e] font-semibold rounded-lg transition-all hover:shadow-lg hover:shadow-[#d4952a]/20 relative overflow-hidden"
                    >
                        <span class="relative z-10 flex items-center gap-2">
                            Submit Your Application
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
                    <a
                        href="https://calendly.com/joanna-trueinfluencemethod/private-training"
                        target="_blank"
                        rel="noopener noreferrer"
                        class="group px-8 py-4 border-2 border-[#d4952a] text-[#d4952a] hover:bg-[#d4952a]/10 font-semibold rounded-lg transition-all flex items-center gap-2 justify-center"
                    >
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            width="18"
                            height="18"
                            viewBox="0 0 24 24"
                            fill="none"
                            stroke="currentColor"
                            stroke-width="2"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            class="group-hover:scale-110 transition-transform"
                        >
                            <rect
                                width="18"
                                height="18"
                                x="3"
                                y="4"
                                rx="2"
                                ry="2"
                            ></rect>
                            <line x1="16" x2="16" y1="2" y2="6"></line>
                            <line x1="8" x2="8" y1="2" y2="6"></line>
                            <line x1="3" x2="21" y1="10" y2="10"></line>
                        </svg>
                        Book a Consultation
                    </a>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const openFaqs = ref<boolean[]>(new Array(8).fill(false));

const toggleFaq = (index: number) => {
    openFaqs.value[index] = !openFaqs.value[index];
};

useHead({
    title: "FAQ | True Influence Method™️",
    meta: [
        {
            name: "description",
            content:
                "Find answers to frequently asked questions about the True Influence Method™️, programs, pricing, and how to get started with Joanna Horton McPherson.",
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

.faq-enter-active,
.faq-leave-active {
    transition: all 0.3s ease-out;
    max-height: 500px;
    overflow: hidden;
}

.faq-enter-from,
.faq-leave-to {
    max-height: 0;
    opacity: 0;
}
</style>
