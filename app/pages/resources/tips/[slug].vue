<script setup lang="ts">
const route = useRoute();
const slug = route.params.slug as string;

// Mock tips data - in a real app, this would come from a CMS or API
const tips: Record<
    string,
    {
        title: string;
        category: string;
        date: string;
        readTime: string;
        image: string;
        content: string;
    }
> = {
    "the-power-of-pause": {
        title: "The Power of Pause",
        category: "Delivery",
        date: "March 20, 2026",
        readTime: "3 min read",
        image: "/carousel/img2.webp",
        content: `
            <p>Silence is not empty space—it's a tool. In my thirty years of working with speakers, I've seen that those who master the art of the pause speak with more authority, impact, and connection.</p>
            
            <p>Most speakers fear silence. They rush to fill every moment, worried that a gap will make them look unprepared or lose their audience's attention. But the opposite is true.</p>
            
            <h2>The Pause as Emphasis</h2>
            
            <p>A strategic pause acts like a highlighter for your words. When you pause before and after a key point, you signal to your audience: <em>This matters.</em></p>
            
            <p>Think of it this way: if everything is equally important, nothing is. The pause creates contrast, and contrast creates emphasis.</p>
            
            <h2>The Pause as Processing Time</h2>
            
            <p>Your audience needs time to absorb what you're saying. When you move too quickly from point to point, you don't allow them to fully process your message.</p>
            
            <p>A pause gives them space to think, to feel, to connect with what you've just said. It's not empty time—it's processing time.</p>
            
            <h2>The Pause as Confidence</h2>
            
            <p>There's something powerful about a speaker who is comfortable with silence. It signals confidence. It shows that you're not rushing, that you trust your message, that you're in command of the room.</p>
            
            <p>Speakers who rush often communicate anxiety. Speakers who pause communicate presence.</p>
            
            <h2>How to Use the Pause Effectively</h2>
            
            <p>Here are three specific ways to incorporate pauses into your speaking:</p>
            
            <ul>
                <li><strong>Before key points:</strong> Pause briefly before you deliver your most important message. This creates anticipation and signals that something important is coming.</li>
                <li><strong>After key points:</strong> Pause after delivering important information. Give your audience time to absorb and reflect.</li>
                <li><strong>Between sections:</strong> Use longer pauses to signal transitions. This helps your audience follow your structure and stay engaged.</li>
            </ul>
            
            <h2>How Long Should You Pause?</h2>
            
            <p>Most speakers don't pause nearly long enough. A comfortable pause for your audience will feel uncomfortably long to you.</p>
            
            <p>As a rule of thumb: count to three in your head before and after key points. It will feel like an eternity to you, but to your audience, it will feel just right.</p>
            
            <h2>The Courage of Silence</h2>
            
            <p>Using silence requires courage. It means being comfortable with not speaking, with being present, with letting your message breathe.</p>
            
            <p>But this courage is rewarded. Speakers who master the pause speak with more impact, more authority, and more connection.</p>
            
            <p>Silence is not empty space. It's one of the most powerful tools in your speaking toolkit.</p>
        `,
    },
    "starting-strong-openings-that-captivate": {
        title: "Starting Strong: Openings That Captivate",
        category: "Structure",
        date: "March 15, 2026",
        readTime: "4 min read",
        image: "/carousel/img4.webp",
        content: `
            <p>The first 30 seconds of any presentation determine whether your audience leans in or tunes out. In my work with leaders, I've seen that those who master their openings have dramatically more impact.</p>
            
            <p>Most speakers waste their openings. They start with "Hello, my name is..." or "Today I'm going to talk about..." or some other generic introduction that fails to engage.</p>
            
            <h2>The Problem With Traditional Openings</h2>
            
            <p>Traditional openings are safe, but they're not effective. They don't capture attention. They don't create connection. They don't signal that something important is about to happen.</p>
            
            <p>Your audience is making rapid decisions about whether to invest their attention in you. A generic opening tells them they can safely tune out.</p>
            
            <h2>What Great Openings Do</h2>
            
            <p>A great opening does three things: it captures attention, creates connection, and establishes relevance.</p>
            
            <p>It makes your audience think: <em>This is for me. This matters. I need to pay attention.</em></p>
            
            <h2>Opening Strategies That Work</h2>
            
            <p>Here are four opening strategies that consistently captivate audiences:</p>
            
            <ul>
                <li><strong>Start with a story:</strong> Human beings are wired for story. A brief, relevant story immediately engages emotions and creates connection.</li>
                <li><strong>Ask a provocative question:</strong> A good question makes your audience think. It engages their intellect and creates curiosity about what's coming next.</li>
                <li><strong>Share a surprising statistic:</strong> A counterintuitive fact can jolt your audience to attention and establish the importance of your topic.</li>
                <li><strong>State a bold claim:</strong> A clear, compelling statement about what you believe or what you've discovered can immediately establish your authority and relevance.</li>
            </ul>
            
            <h2>The Opening Must Connect to Your Message</h2>
            
            <p>Whatever opening strategy you choose, it must connect directly to your core message. A captivating opening that doesn't lead anywhere is a trick, not a tool.</p>
            
            <p>Your opening should be the first step on a clear journey, not a disconnected attention-grabber.</p>
            
            <h2>Practice Your Opening</h2>
            
            <p>Your opening deserves special attention. Practice it until you can deliver it without thinking. It should be so polished that it feels effortless.</p>
            
            <p>When you start with confidence and clarity, you set the tone for everything that follows.</p>
            
            <h2>The First 30 Seconds Matter Most</h2>
            
            <p>You never get a second chance to make a first impression. Your opening is your opportunity to capture attention, create connection, and establish why your audience should care.</p>
            
            <p>Invest in your opening. It's the most important 30 seconds of your presentation.</p>
        `,
    },
    "eye-contact-that-builds-connection": {
        title: "Eye Contact That Builds Connection",
        category: "Presence",
        date: "March 10, 2026",
        readTime: "3 min read",
        image: "/carousel/img6.webp",
        content: `
            <p>Beyond technique—true eye contact is about relationship. In my work with leaders, I've seen that those who understand this distinction speak with significantly more impact.</p>
            
            <p>Most speakers treat eye contact as a technique: look at people for three seconds, then move to the next person. This is better than no eye contact, but it misses the point.</p>
            
            <h2>Eye Contact as Relationship</h2>
            
            <p>True eye contact is not about scanning the room—it's about connecting with individuals. When you look at someone, you're not just meeting their gaze. You're entering into a brief relationship with them.</p>
            
            <p>This subtle shift in mindset transforms everything about how you engage your audience.</p>
            
            <h2>The Problem With Scanning</h2>
            
            <p>When speakers scan the room, their eyes are constantly moving. They're not really seeing anyone—they're looking through people.</p>
            
            <p>Audiences can sense this. They can tell when a speaker is performing for the room rather than connecting with individuals.</p>
            
            <h2>How to Make Real Eye Contact</h2>
            
            <p>Here's how to shift from scanning to connecting:</p>
            
            <ul>
                <li><strong>Choose one person:</strong> Select one person in the audience and actually look at them—not at them, but at them. Notice their eyes, their expression, their response.</li>
                <li><strong>Complete a thought:</strong> Hold that connection while you complete one full thought or sentence. Don't rush away.</li>
                <li><strong>Move intentionally:</strong> When you move to another person, make it intentional. Choose someone in a different part of the room.</li>
                <li><strong>Repeat:</strong> Continue this pattern, connecting with individuals throughout your presentation.</li>
            </ul>
            
            <h2>Eye Contact in Large Rooms</h2>
            
            <p>In large rooms, you can't make eye contact with everyone. But you can still create the experience of connection by focusing on specific sections of the room.</p>
            
            <p>Divide the room into quadrants and make sure you connect with people in each section. Everyone will feel included.</p>
            
            <h2>Eye Contact With Virtual Audiences</h2>
            
            <p>With virtual presentations, eye contact means looking at the camera, not at the people on your screen. This takes practice because it feels counterintuitive.</p>
            
            <p>When you look at the camera, you create the experience of eye contact for everyone watching. When you look at people on your screen, you're looking down, which breaks connection.</p>
            
            <h2>The Courage of Connection</h2>
            
            <p>Real eye contact requires vulnerability. When you truly look at someone, you're making yourself visible to them. You're allowing them to see you.</p>
            
            <p>This vulnerability is what creates genuine connection. It's what transforms a presentation into a relationship.</p>
            
            <p>Eye contact is not a technique. It's a relationship. Master it, and your speaking will never be the same.</p>
        `,
    },
    "using-your-voice-as-an-instrument": {
        title: "Using Your Voice as an Instrument",
        category: "Voice",
        date: "March 5, 2026",
        readTime: "5 min read",
        image: "/carousel/img8.webp",
        content: `
            <p>Your voice carries more than words—it carries emotion, conviction, and presence. In my thirty years of coaching speakers, I've seen that those who learn to use their voice as an instrument speak with dramatically more impact.</p>
            
            <p>Most speakers use their voice unconsciously. They speak in their habitual patterns, unaware of how their voice affects their message and their audience.</p>
            
            <h2>The Voice as Communication Tool</h2>
            
            <p>Your voice is not just a delivery system for your words. It's a communication tool in its own right. The tone, pace, volume, and quality of your voice all convey meaning.</p>
            
            <p>In fact, research suggests that how you say something matters more than what you say. Your voice can reinforce or contradict your words.</p>
            
            <h2>The Elements of Vocal Variety</h2>
            
            <p>Here are the key elements of vocal variety and how to use them effectively:</p>
            
            <ul>
                <li><strong>Pace:</strong> The speed at which you speak. Varying your pace creates interest. Slow down for emphasis, speed up for excitement or energy.</li>
                <li><strong>Volume:</strong> How loudly or softly you speak. Volume changes create drama and emphasis. A sudden drop in volume can be as powerful as a raise.</li>
                <li><strong>Pitch:</strong> The highness or lowness of your voice. Natural pitch variation conveys emotion and engagement. A monotone voice signals disengagement.</li>
                <li><strong>Tone:</strong> The emotional quality of your voice. Warmth, authority, concern, excitement—these are all conveyed through tone.</li>
                <li><strong>Pause:</strong> The use of silence. Strategic pauses create emphasis, allow processing time, and signal confidence.</li>
            </ul>
            
            <h2>Matching Voice to Message</h2>
            
            <p>The key to effective vocal variety is matching your voice to your message. Different parts of your presentation call for different vocal approaches.</p>
            
            <p>Stories might call for more warmth and emotion. Data might call for more precision and clarity. Calls to action might call for more energy and conviction.</p>
            
            <h2>The Trap of Performance</h2>
            
            <p>Be careful not to treat vocal variety as performance. When you're trying to sound a certain way, you come across as inauthentic.</p>
            
            <p>The goal is not to add artificial variety to your voice. The goal is to release the natural variety that's already there when you're speaking about something you care about.</p>
            
            <h2>Developing Vocal Awareness</h2>
            
            <p>Developing vocal awareness begins with listening. Record yourself speaking and listen back. Notice patterns. Identify areas where more variety would enhance your message.</p>
            
            <p>Then practice intentionally. Experiment with pace, volume, and tone. Find what feels natural and authentic for you.</p>
            
            <h2>Your Voice, Your Message</h2>
            
            <p>Your voice is uniquely yours. It carries your identity, your personality, your truth. When you learn to use it fully as an instrument, you amplify your message and your impact.</p>
            
            <p>Don't just speak with your words. Speak with your voice.</p>
        `,
    },
    "handling-questions-with-grace": {
        title: "Handling Questions With Grace",
        category: "Engagement",
        date: "February 28, 2026",
        readTime: "4 min read",
        image: "/carousel/img1.webp",
        content: `
            <p>Q&A is where authenticity shines. In my work with leaders, I've seen that those who handle questions with grace and confidence build significantly more trust and credibility.</p>
            
            <p>Many speakers fear Q&A. They worry about difficult questions, about being caught off guard, about losing control of the room. But Q&A is not a threat—it's an opportunity.</p>
            
            <h2>Q&A as Connection</h2>
            
            <p>Q&A is where you connect most directly with your audience. It's where you respond to their specific concerns, where you demonstrate your expertise, where you show your authentic self.</p>
            
            <p>Handled well, Q&A can be the most powerful part of your presentation.</p>
            
            <h2>The Mindset of Q&A</h2>
            
            <p>The most important aspect of handling questions is mindset. Approach Q&A with curiosity rather than defensiveness.</p>
            
            <p>When someone asks a question, they're giving you a gift. They're telling you what matters to them, what they're curious about, what they need to understand.</p>
            
            <h2>How to Receive Questions</h2>
            
            <p>Here's how to receive questions effectively:</p>
            
            <ul>
                <li><strong>Listen fully:</strong> Let the person complete their question without interrupting. Show that you're genuinely listening.</li>
                <li><strong>Acknowledge:</strong> Before responding, acknowledge the question. "That's a great question" or "Thank you for asking that."</li>
                <li><strong>Clarify if needed:</strong> If you're not sure what they're asking, politely clarify. "Let me make sure I understand your question..."</li>
                <li><strong>Take your time:</strong> It's okay to pause before responding. A thoughtful pause shows you're taking their question seriously.</li>
            </ul>
            
            <h2>How to Respond to Questions</h2>
            
            <p>When responding to questions:</p>
            
            <ul>
                <li><strong>Be honest:</strong> If you don't know the answer, say so. "That's a great question, and I don't have the answer right now. Let me look into that and get back to you."</li>
                <li><strong>Stay on message:</strong> Connect your response to your core message when possible. This reinforces your key points.</li>
                <li><strong>Keep it concise:</strong> Most questions don't require long answers. Be direct and concise.</li>
                <li><strong>Bridge when needed:</strong> If a question takes you off track, acknowledge it and bridge back to your main topic.</li>
            </ul>
            
            <h2>Handling Difficult Questions</h2>
            
            <p>Difficult questions are opportunities to demonstrate grace under pressure. Stay calm, stay respectful, and stay honest.</p>
            
            <p>If someone is being aggressive or argumentative, don't engage in a debate. Acknowledge their perspective, share your view respectfully, and move on.</p>
            
            <h2>The Power of Authenticity</h2>
            
            <p>The most effective Q&A responses are authentic ones. When you speak honestly and respectfully, you build trust and credibility.</p>
            
            <p>Don't try to have all the answers. Try to be authentic, respectful, and helpful. That's what audiences remember.</p>
            
            <p>Q&A is not a test. It's a conversation. Approach it that way, and you'll handle questions with grace.</p>
        `,
    },
    "body-language-that-communicates-truth": {
        title: "Body Language That Communicates Truth",
        category: "Presence",
        date: "February 22, 2026",
        readTime: "4 min read",
        image: "/carousel/img3.webp",
        content: `
            <p>Your body speaks before you do. In my work with leaders, I've seen that those who align their physical presence with their message speak with significantly more impact.</p>
            
            <p>Most speakers are unaware of their body language. They focus on their words, their slides, their content—missing the powerful communication happening through their physical presence.</p>
            
            <h2>The Primacy of Nonverbal Communication</h2>
            
            <p>Research consistently shows that nonverbal communication carries more weight than verbal communication. Your posture, gestures, facial expressions, and movement all convey meaning.</p>
            
            <p>When your body language contradicts your words, audiences believe your body. When they align, your message is amplified.</p>
            
            <h2>The Elements of Powerful Presence</h2>
            
            <p>Here are the key elements of body language that communicate presence and authority:</p>
            
            <ul>
                <li><strong>Posture:</strong> Stand tall with your shoulders back and your weight evenly distributed. This communicates confidence and openness.</li>
                <li><strong>Eye contact:</strong> Connect with individuals in your audience, not just scan the room. Real eye contact builds relationship.</li>
                <li><strong>Gestures:</strong> Use natural gestures that support your message. Avoid rehearsed or artificial movements.</li>
                <li><strong>Facial expressions:</strong> Let your face reflect the emotion of your message. Authentic expressions create connection.</li>
                <li><strong>Movement:</strong> Move with purpose. Use the space intentionally to emphasize points or transitions.</li>
            </ul>
            
            <h2>The Trap of Performance</h2>
            
            <p>Be careful not to treat body language as performance. When you're trying to look confident or authoritative, you often come across as inauthentic.</p>
            
            <p>The goal is not to adopt a set of "power poses" or rehearsed gestures. The goal is to release your natural, authentic presence.</p>
            
            <h2>Aligning Body and Message</h2>
            
            <p>The key to effective body language is alignment with your message. Your physical presence should support and reinforce what you're saying.</p>
            
            <p>When you speak about something important, your body should show that importance. When you share something emotional, your face should reflect that emotion.</p>
            
            <h2>Body Language in Virtual Settings</h2>
            
            <p>In virtual presentations, body language still matters. Frame yourself so your upper body is visible. Maintain eye contact by looking at the camera. Use gestures within the frame.</p>
            
            <p>Even on screen, your physical presence communicates.</p>
            
            <h2>Developing Body Awareness</h2>
            
            <p>Developing body awareness begins with observation. Record yourself speaking and watch with the sound off. Notice what your body is communicating.</p>
            
            <p>Then practice intentionally. Experiment with different postures, gestures, and movements. Find what feels authentic and effective for you.</p>
            
            <h2>Your Body, Your Voice</h2>
            
            <p>Your body is not separate from your voice—it's part of it. When you align your physical presence with your message, you communicate with your whole self.</p>
            
            <p>That's when speaking becomes most powerful.</p>
        `,
    },
    "nervousness-as-fuel-not-barrier": {
        title: "Nervousness as Fuel, Not Barrier",
        category: "Mindset",
        date: "February 15, 2026",
        readTime: "5 min read",
        image: "/carousel/img5.webp",
        content: `
            <p>Nervousness is not your enemy—it's energy. In my thirty years of working with speakers, I've seen that those who learn to channel their nervousness speak with more power and authenticity.</p>
            
            <p>Most speakers view nervousness as a problem to be solved. They try to eliminate it, suppress it, or hide it. But nervousness is not a flaw—it's a sign that something matters.</p>
            
            <h2>The Truth About Nervousness</h2>
            
            <p>Every speaker experiences nervousness. The most experienced, confident speakers you admire still feel it before they take the stage.</p>
            
            <p>The difference is not whether they feel nervousness—it's how they relate to it.</p>
            
            <h2>Nervousness as Energy</h2>
            
            <p>At its core, nervousness is just energy—physiological arousal preparing you for something important. Your heart beats faster, your breathing changes, your senses heighten.</p>
            
            <p>This energy is not the problem. The problem is when we interpret this energy as a threat rather than a resource.</p>
            
            <h2>The Fear of Fear</h2>
            
            <p>What makes nervousness difficult is not the physical sensations—it's our interpretation of them. When we feel nervous and think "something is wrong with me," we create a second layer of anxiety.</p>
            
            <p>This fear of fear is what spirals into full-blown anxiety.</p>
            
            <h2>Reframing Nervousness</h2>
            
            <p>The key to working with nervousness is reframing it. Instead of "I'm nervous," try "I'm energized" or "I'm excited" or "I'm ready."</p>
            
            <p>These statements describe the same physical experience, but they frame it as a resource rather than a problem.</p>
            
            <h2>Practical Strategies for Working With Nervousness</h2>
            
            <p>Here are practical strategies for channeling nervousness into powerful speaking:</p>
            
            <ul>
                <li><strong>Acknowledge it:</strong> Don't fight your nervousness. Acknowledge it: "I'm feeling some energy right now, and that's okay."</li>
                <li><strong>Breathe:</strong> Deep, slow breathing activates your parasympathetic nervous system, calming the fight-or-flight response.</li>
                <li><strong>Move:</strong> Physical movement helps discharge excess energy. Walk, stretch, or gesture before you speak.</li>
                <li><strong>Focus outward:</strong> Shift your focus from yourself to your audience and your message. Nervousness is self-focused; service is other-focused.</li>
                <li><strong>Start slow:</strong> Begin your presentation slowly and deliberately. This signals to your nervous system that you're in control.</li>
            </ul>
            
            <h2>The Courage of Vulnerability</h2>
            
            <p>There's courage in acknowledging nervousness. When you're honest about feeling nervous, you create connection with your audience.</p>
            
            <p>"I'm excited to be here, and I'll admit I'm feeling a bit nervous because this topic matters so much to me." This kind of honesty builds trust.</p>
            
            <h2>Nervousness as Preparation</h2>
            
            <p>Nervousness is your body's way of preparing you for something important. It's heightening your senses, sharpening your focus, mobilizing your resources.</p>
            
            <p>Thank your nervousness for this preparation. Then use the energy it provides.</p>
            
            <h2>From Nervousness to Presence</h2>
            
            <p>When you stop fighting your nervousness and start working with it, something shifts. The energy that was working against you now works for you.</p>
            
            <p>Nervousness becomes presence. Anxiety becomes aliveness. Fear becomes fuel.</p>
            
            <p>That's when speaking becomes most powerful.</p>
        `,
    },
    "ending-with-impact": {
        title: "Ending With Impact",
        category: "Structure",
        date: "February 8, 2026",
        readTime: "4 min read",
        image: "/carousel/img7.webp",
        content: `
            <p>How you leave the room matters as much as how you enter it. In my work with leaders, I've seen that those who master their endings create lasting impact and inspire action.</p>
            
            <p>Most speakers give their endings little thought. They rush through their conclusion, trail off awkwardly, or end with a weak "thank you." But your ending is your final impression—make it count.</p>
            
            <h2>The Power of the Final Impression</h2>
            
            <p>Psychological research shows that people remember endings more than beginnings or middles. This is called the "recency effect."</p>
            
            <p>Your ending is what your audience carries with them. It's what they remember. It's what they act on.</p>
            
            <h2>What Great Endings Do</h2>
            
            <p>A great ending does three things: it reinforces your core message, creates emotional resonance, and inspires action.</p>
            
            <p>It leaves your audience with clarity about what they heard, feeling about what matters, and motivation to do something about it.</p>
            
            <h2>Ending Strategies That Work</h2>
            
            <p>Here are four ending strategies that consistently create impact:</p>
            
            <ul>
                <li><strong>Circle back to your opening:</strong> Return to the story, question, or statement you began with. This creates a satisfying sense of completion.</li>
                <li><strong>Summarize with power:</strong> Distill your message into a clear, memorable statement. Make it something your audience can easily remember and repeat.</li>
                <li><strong>End with a story:</strong> A brief, powerful story that encapsulates your message can create emotional resonance that stays with your audience.</li>
                <li><strong>Call to action:</strong> Be clear about what you want your audience to do. Specific, actionable calls to action are more effective than vague requests.</li>
            </ul>
            
            <h2>The Ending Must Be Earned</h2>
            
            <p>Your ending should feel earned, not tacked on. It should flow naturally from everything you've said, bringing your presentation to a satisfying conclusion.</p>
            
            <p>A powerful ending that doesn't connect to your message feels manipulative. An ending that emerges organically from your message feels authentic.</p>
            
            <h2>Avoid Weak Endings</h2>
            
            <p>Here are common weak endings to avoid:</p>
            
            <ul>
                <li><strong>"That's all I have."</strong> This signals that you've run out of things to say, not that you've completed your message.</li>
                <li><strong>"Are there any questions?"</strong> While Q&A is valuable, it shouldn't be your ending. End after Q&A with a final statement.</li>
                <li><strong>Trailing off:</strong> Don't let your voice fade away at the end. End with clarity and conviction.</li>
                <li><strong>"Thank you" as your final words:</strong> Gratitude is important, but "thank you" alone is not an ending. End with your message, then thank your audience.</li>
            </ul>
            
            <h2>Practice Your Ending</h2>
            
            <p>Your ending deserves special attention. Practice it until you can deliver it with confidence and clarity. It should be the most polished part of your presentation.</p>
            
            <p>When you end strong, you leave your audience with a clear sense of your message and its importance.</p>
            
            <h2>The Last Word Matters</h2>
            
            <p>You never get a second chance to make a final impression. Your ending is your opportunity to reinforce your message, create emotional impact, and inspire action.</p>
            
            <p>Invest in your ending. It's the most important final moment of your presentation.</p>
        `,
    },
};

// Get the current tip or redirect to 404
const tip = tips[slug];

// Handle 404
if (!tip) {
    throw createError({
        statusCode: 404,
        statusMessage: "Speaking tip not found",
    });
}

// Set page meta
useHead({
    title: `${tip.title} — True Influence Method™️`,
    meta: [
        {
            name: "description",
            content: tip.content.replace(/<[^>]*>/g, "").substring(0, 160),
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
                    :src="tip.image"
                    alt="Tip cover"
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
                        to="/resources/tips"
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
                        Back to Speaking Tips
                    </NuxtLink>
                    <span class="text-[#faf8f5]/30">|</span>
                    <span
                        class="text-[#d4952a] text-sm font-medium tracking-[0.2em] uppercase"
                    >
                        {{ tip.category }}
                    </span>
                </div>

                <h1
                    class="font-serif text-3xl md:text-4xl lg:text-5xl text-[#faf8f5] mb-6 leading-tight"
                >
                    {{ tip.title }}
                </h1>

                <div
                    class="flex items-center justify-center gap-4 text-sm text-[#faf8f5]/60"
                >
                    <span>{{ tip.date }}</span>
                    <span class="w-1 h-1 rounded-full bg-[#d4952a]" />
                    <span>{{ tip.readTime }}</span>
                </div>
            </div>
        </section>

        <!-- Tip Content Section -->
        <section class="py-16 md:py-24 relative">
            <div
                class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e] via-[#232360] to-[#1a1a4e]"
            />

            <div class="max-w-3xl mx-auto px-6 relative z-10">
                <article>
                    <div v-html="tip.content" class="article-content" />
                </article>
            </div>
        </section>

        <!-- Related Tips Section -->
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
                        More Speaking Tips
                    </h2>
                    <p class="text-[#faf8f5]/60 max-w-2xl mx-auto">
                        Explore more practical insights to enhance your speaking
                        and presence.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <NuxtLink
                        v-for="(relatedTip, relatedSlug) in tips"
                        v-show="relatedSlug !== slug"
                        :key="relatedSlug"
                        :to="`/resources/tips/${relatedSlug}`"
                        class="group bg-[#1a1a4e]/50 backdrop-blur-sm rounded-xl border border-[#faf8f5]/10 hover:border-[#d4952a]/30 transition-all duration-300 overflow-hidden"
                    >
                        <div class="relative aspect-[16/10] overflow-hidden">
                            <img
                                :src="relatedTip.image"
                                :alt="relatedTip.title"
                                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />
                            <div class="absolute top-4 left-4">
                                <span
                                    class="inline-block px-3 py-1 bg-[#d4952a] text-[#1a1a4e] text-xs font-semibold rounded-full"
                                >
                                    {{ relatedTip.category }}
                                </span>
                            </div>
                        </div>

                        <div class="p-6">
                            <h3
                                class="font-serif text-lg text-[#faf8f5] mb-3 leading-tight group-hover:text-[#d4952a] transition-colors"
                            >
                                {{ relatedTip.title }}
                            </h3>

                            <div
                                class="flex items-center gap-2 text-[#d4952a] text-sm font-medium group-hover:gap-3 transition-all"
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
