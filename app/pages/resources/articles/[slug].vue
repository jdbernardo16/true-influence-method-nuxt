<script setup lang="ts">
const route = useRoute();
const slug = route.params.slug as string;

// Mock articles data - in a real app, this would come from a CMS or API
const articles: Record<
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
    "leadership-begins-with-knowing-what-you-stand-for": {
        title: "Leadership Begins With Knowing What You Stand For",
        category: "Leadership",
        date: "March 15, 2026",
        readTime: "5 min read",
        image: "/carousel/img1.webp",
        content: `
            <p>The most powerful leaders I've worked with share a common trait: they don't just have a vision—they have a clear understanding of their values and the courage to live by them.</p>
            
            <p>This might sound simple. But in practice, it's anything but.</p>
            
            <h2>The Gap Between Vision and Values</h2>
            
            <p>Most leaders can articulate what they want to achieve. They can describe their goals, their metrics, their desired outcomes. But when you ask them what they stand for—what principles they will not compromise, what lines they will not cross—many struggle.</p>
            
            <p>This gap between vision and values is where leadership either deepens or fractures.</p>
            
            <p>When a leader knows what they stand for, decisions become clearer. Communication becomes more authentic. Trust builds faster because people sense consistency—not just in what you say, but in who you are.</p>
            
            <h2>The Cost of Uncertainty</h2>
            
            <p>When a leader is uncertain about their values, the cost is high. Teams sense the hesitation. Messages land with less impact because they lack conviction. Opportunities for meaningful influence are lost because the leader hasn't done the internal work to ground their message in something real.</p>
            
            <p>I've seen this pattern repeatedly in my work with executives. The ones who struggle most with influence are not those who lack technical skill or experience. They are the ones who haven't taken the time to name and claim their values.</p>
            
            <h2>Finding Your Foundation</h2>
            
            <p>So how do you discover what you stand for? It begins with honest reflection.</p>
            
            <p>What experiences shaped you? What moments defined your sense of right and wrong? What principles have guided your most important decisions? What would you refuse to do, even if it cost you something significant?</p>
            
            <p>These questions are not abstract. They are the foundation of authentic leadership.</p>
            
            <h2>Living Your Values</h2>
            
            <p>Knowing what you stand for is only the beginning. The real work is living it—especially when it's difficult.</p>
            
            <p>True influence comes not from perfect performance, but from consistent authenticity. When your actions align with your values, people notice. They trust you not because you're flawless, but because you're real.</p>
            
            <p>Leadership, at its core, is about influence. And influence begins with clarity about what you stand for.</p>
        `,
    },
    "the-art-of-authentic-communication": {
        title: "The Art of Authentic Communication",
        category: "Communication",
        date: "March 8, 2026",
        readTime: "7 min read",
        image: "/carousel/img2.webp",
        content: `
            <p>Authenticity isn't a skill you learn—it's a truth you uncover. This is the fundamental insight that transforms how leaders approach communication.</p>
            
            <p>Most communication training focuses on technique: how to structure a message, how to use body language, how to project confidence. These are valuable tools. But they are not the source of authentic influence.</p>
            
            <h2>The Performance Trap</h2>
            
            <p>Many leaders fall into what I call the performance trap. They believe that better communication means better performance—more polished delivery, more sophisticated language, more perfect presence.</p>
            
            <p>This approach often backfires. Audiences can sense when someone is performing rather than speaking. The message may be technically sound, but it lacks emotional resonance because it lacks truth.</p>
            
            <h2>Authenticity as Discovery</h2>
            
            <p>Authentic communication begins not with learning new techniques, but with discovering what is already true about you.</p>
            
            <p>What is your actual voice—not the one you think you should have? What stories feel most alive when you tell them? What makes you lean in with genuine engagement?</p>
            
            <p>These questions point toward your authentic communication style. It's not something you construct; it's something you uncover.</p>
            
            <h2>The Courage to Be Real</h2>
            
            <p>Authentic communication requires courage. It means showing up as yourself—not as a version of yourself you think others want to see.</p>
            
            <p>This is especially challenging for leaders who have spent years cultivating a professional persona. The risk of vulnerability feels too high. The fear of judgment too real.</p>
            
            <p>But here's what I've learned from three decades of working with leaders: the most influential communicators are not the most polished. They are the most honest.</p>
            
            <h2>Finding Your Voice</h2>
            
            <p>Your authentic voice is already within you. It's the voice you use when you're speaking about something that truly matters to you. It's the voice that emerges when you're not trying to impress anyone.</p>
            
            <p>The work of authentic communication is creating the conditions for that voice to emerge consistently—even in high-stakes situations.</p>
            
            <p>This is not about abandoning professionalism. It's about bringing your full, authentic self to your professional communication.</p>
            
            <h2>The Impact of Authenticity</h2>
            
            <p>When leaders communicate authentically, something shifts in the room. People lean in. Trust builds more quickly. Messages land with greater impact because they carry the weight of genuine conviction.</p>
            
            <p>Authentic communication is not just more effective—it's more sustainable. Performing is exhausting. Being yourself is energizing.</p>
            
            <p>The art of authentic communication is the art of discovering and expressing your truth. It's not easy work, but it's the most important work a leader can do.</p>
        `,
    },
    "why-your-story-matters-more-than-your-script": {
        title: "Why Your Story Matters More Than Your Script",
        category: "Storytelling",
        date: "March 1, 2026",
        readTime: "6 min read",
        image: "/carousel/img3.webp",
        content: `
            <p>The most compelling messages come not from perfect scripts, but from lived experience and honest reflection. This is a truth I've witnessed repeatedly in my work with leaders.</p>
            
            <p>Many leaders approach communication with a script-first mindset. They craft carefully worded messages, rehearse their delivery, and focus on getting every detail right. This approach has value—but it has limits.</p>
            
            <h2>The Problem with Perfect Scripts</h2>
            
            <p>A perfect script can be technically impressive. It can be well-structured, articulate, and persuasive. But if it doesn't connect with something real in the speaker's experience, it will lack emotional impact.</p>
            
            <p>Audiences can sense the difference between a memorized script and a message that comes from lived experience. The former may be polished, but the latter is powerful.</p>
            
            <h2>Your Story as Authority</h2>
            
            <p>When you speak from your own experience, you speak with a different kind of authority. You're not just conveying information—you're sharing truth that you've lived through.</p>
            
            <p>This kind of authority cannot be manufactured. It comes from having actually experienced what you're talking about. It comes from the scars, the lessons, the moments of insight that shaped your understanding.</p>
            
            <h2>The Defining Moment</h2>
            
            <p>Every leader has defining moments—experiences that shaped their leadership, their values, their vision. These moments are not just personal history; they are the foundation of authentic communication.</p>
            
            <p>When you can identify and articulate your defining moments, you tap into a source of communication power that no script can replicate.</p>
            
            <h2>From Script to Story</h2>
            
            <p>Moving from script-based communication to story-based communication requires a shift in mindset. Instead of asking "What should I say?", you ask "What is my story?"</p>
            
            <p>This is not about abandoning structure or preparation. It's about grounding your message in something real and personal.</p>
            
            <p>The most effective messages combine the clarity of good structure with the power of authentic story.</p>
            
            <h2>The Courage of Vulnerability</h2>
            
            <p>Sharing your story requires vulnerability. It means revealing parts of yourself—the struggles, the failures, the moments of doubt—that you might prefer to keep hidden.</p>
            
            <p>But vulnerability is not weakness. In communication, vulnerability is connection. When leaders are willing to be real about their experiences, they create space for others to do the same.</p>
            
            <h2>The Impact of Story</h2>
            
            <p>Stories move people in ways that facts alone cannot. They engage emotions, create meaning, and build connection.</p>
            
            <p>When you share your story authentically, you're not just communicating information—you're inviting others into your experience. This is the essence of influence.</p>
            
            <p>Your story matters more than your script because it carries the weight of truth. And truth is the most powerful communication tool you have.</p>
        `,
    },
    "finding-courage-in-the-room": {
        title: "Finding Courage in the Room",
        category: "Leadership",
        date: "February 22, 2026",
        readTime: "4 min read",
        image: "/carousel/img4.webp",
        content: `
            <p>Speaking up in high-stakes environments requires more than preparation—it requires the bravery to be seen and heard.</p>
            
            <p>I've worked with countless leaders who are brilliant, prepared, and knowledgeable. Yet when they step into important meetings, boardrooms, or presentations, something holds them back.</p>
            
            <h2>The Fear of Being Seen</h2>
            
            <p>At its core, the hesitation to speak up is often a fear of being seen—really seen. When you speak with conviction, you make yourself visible. You expose your thinking, your perspective, your judgment.</p>
            
            <p>This visibility feels risky. What if you're wrong? What if you're judged? What if your contribution isn't valued?</p>
            
            <p>These fears are normal. They're human. But they don't have to control you.</p>
            
            <h2>Courage as Practice</h2>
            
            <p>Courage is not the absence of fear. Courage is acting despite fear. And like any skill, courage can be practiced and developed.</p>
            
            <p>Every time you speak up—especially when it's uncomfortable—you're building your courage muscle. You're proving to yourself that you can handle the visibility, the risk, the potential for judgment.</p>
            
            <h2>The Cost of Silence</h2>
            
            <p>When leaders hold back, the cost is high. Important perspectives go unshared. Critical questions go unasked. The collective intelligence of the room is diminished.</p>
            
            <p>But perhaps the greatest cost is personal. When you consistently hold back your voice, you diminish your own influence. You reinforce the belief that your perspective doesn't matter.</p>
            
            <h2>Finding Your Courage</h2>
            
            <p>So how do you find the courage to speak up? It begins with recognizing that your voice matters—not because you're the most knowledgeable person in the room, but because you're in the room.</p>
            
            <p>Your perspective is unique. Your experience is valuable. Your voice deserves to be heard.</p>
            
            <p>Start small. Speak up in low-stakes situations. Ask questions. Share observations. Build your confidence gradually.</p>
            
            <h2>The Ripple Effect</h2>
            
            <p>When you find your courage, something interesting happens. Others are encouraged to find theirs too. Your bravery creates permission for others to speak up.</p>
            
            <p>This is how culture shifts—through individual acts of courage that ripple outward.</p>
            
            <h2>Leading With Voice</h2>
            
            <p>Leadership is not just about what you know—it's about how you use your voice in service of the collective good.</p>
            
            <p>Finding courage in the room is not just about personal growth. It's about leadership impact. When you speak up with authenticity and conviction, you create value for everyone in the room.</p>
            
            <p>Your voice is your leadership. Finding the courage to use it is one of the most important investments you can make.</p>
        `,
    },
    "the-defining-moment-every-leader-has": {
        title: "The Defining Moment Every Leader Has",
        category: "Leadership",
        date: "February 15, 2026",
        readTime: "8 min read",
        image: "/carousel/img5.webp",
        content: `
            <p>Behind every great leader is a moment that shaped them. Naming this moment is the first step to owning your message.</p>
            
            <p>In my three decades of working with leaders, I've discovered something consistent: every influential leader has a defining moment—a specific experience that fundamentally shaped their leadership, their values, and their vision.</p>
            
            <h2>What Is a Defining Moment?</h2>
            
            <p>A defining moment is not just an important experience. It's a moment of transformation—a time when something shifted in your understanding of yourself, your work, or your purpose.</p>
            
            <p>It might be a moment of failure that taught you resilience. A moment of success that revealed your values. A moment of connection that showed you what matters most.</p>
            
            <p>What makes it defining is not just that it happened, but that it changed you.</p>
            
            <h2>The Power of Naming</h2>
            
            <p>Here's what I've observed: many leaders have defining moments, but few have named them. They carry the impact of these experiences without ever articulating what happened and why it mattered.</p>
            
            <p>This is a missed opportunity. When you name your defining moment, you unlock its power. You transform it from an unconscious influence into a conscious resource.</p>
            
            <h2>Your Defining Moment as Foundation</h2>
            
            <p>Your defining moment is the foundation of your leadership story. It's the source of your authentic voice. It's the wellspring of your conviction.</p>
            
            <p>When you can articulate your defining moment clearly, you gain clarity about who you are as a leader and what you stand for. This clarity translates into more powerful communication.</p>
            
            <h2>Finding Your Defining Moment</h2>
            
            <p>How do you identify your defining moment? It requires reflection and honesty.</p>
            
            <p>Think about the experiences that shaped you. What moments stand out as turning points? What experiences do you find yourself returning to again and again in your thinking?</p>
            
            <p>Pay attention to the stories you tell about yourself. The stories that feel most alive, most meaningful, often point toward your defining moments.</p>
            
            <h2>The Interview Process</h2>
            
            <p>In my work with leaders, I use an interview-based process to help them uncover their defining moments. Through thoughtful questions and deep listening, we surface the experiences that have shaped their leadership.</p>
            
            <p>This process is not always easy. It requires vulnerability. It requires facing parts of your story that might be uncomfortable. But the clarity that emerges is worth it.</p>
            
            <h2>From Defining Moment to Message</h2>
            
            <p>Once you've identified your defining moment, the next step is connecting it to your message. How does this experience inform what you want to communicate? What does it reveal about your values, your vision, your purpose?</p>
            
            <p>Your defining moment is not just personal history—it's the foundation of your leadership message.</p>
            
            <h2>The Impact of Sharing</h2>
            
            <p>When leaders share their defining moments authentically, something powerful happens. The message becomes more than information—it becomes connection.</p>
            
            <p>Audiences respond to vulnerability. They connect with honesty. They are moved by truth.</p>
            
            <p>Your defining moment is your unique contribution to the conversation. No one else has your story. No one else can tell it the way you can.</p>
            
            <h2>Owning Your Story</h2>
            
            <p>Naming and claiming your defining moment is an act of ownership. It's saying: This is who I am. This is what shaped me. This is why I lead the way I do.</p>
            
            <p>This ownership is the foundation of authentic influence. When you own your story, you speak with a different kind of authority.</p>
            
            <p>Your defining moment is waiting to be named. When you find it and claim it, you unlock a powerful source of leadership communication.</p>
        `,
    },
    "from-impact-to-influence": {
        title: "From Impact to Influence",
        category: "Communication",
        date: "February 8, 2026",
        readTime: "5 min read",
        image: "/carousel/img6.webp",
        content: `
            <p>You've built something real. Now it's time to speak about it in a way that creates lasting change and builds trust.</p>
            
            <p>Many of the leaders I work with have achieved significant impact. They've built companies, led teams, created value. They've done the work.</p>
            
            <p>But they struggle with influence—the ability to articulate their impact in a way that moves rooms, earns trust, and creates a legacy.</p>
            
            <h2>The Gap Between Impact and Influence</h2>
            
            <p>Impact is what you've done. Influence is how you communicate what you've done.</p>
            
            <p>Many leaders are excellent at impact but struggle with influence. They've built something meaningful, but they can't articulate it in a way that resonates with others.</p>
            
            <p>This gap is costly. It limits their reach. It diminishes their legacy. It prevents them from having the impact they could have.</p>
            
            <h2>Why Influence Matters</h2>
            
            <p>Influence is how impact scales. When you can articulate your work compellingly, you inspire others. You attract resources. You build movements.</p>
            
            <p>Influence is also how impact lasts. The leaders whose work endures are not just those who did great things—they're those who could tell the story of what they did in a way that others could carry forward.</p>
            
            <h2>The Communication Challenge</h2>
            
            <p>So why do so many capable leaders struggle with influence? Often, it's because they approach communication as a technical skill rather than a truth-telling exercise.</p>
            
            <p>They focus on what to say rather than discovering what is true to say. They craft messages rather than uncovering their authentic voice.</p>
            
            <h2>From Craft to Discover</h2>
            
            <p>The shift from impact to influence begins with a shift in approach. Instead of asking "How should I communicate my work?", ask "What is the truth of my work?"</p>
            
            <p>This is not about abandoning structure or preparation. It's about grounding your communication in something real and authentic.</p>
            
            <h2>Your Story as Influence</h2>
            
            <p>Your story is your most powerful influence tool. Not the polished version you think people want to hear—the real version of what you've experienced, learned, and believe.</p>
            
            <p>When you share your story authentically, you create connection. Connection builds trust. Trust enables influence.</p>
            
            <h2>The Clarity Factor</h2>
            
            <p>Clarity is essential for influence. If you can't articulate what you do clearly, others can't understand it, value it, or help you scale it.</p>
            
            <p>But clarity doesn't mean simplification. It means distillation—finding the essence of your work and expressing it in language that resonates.</p>
            
            <h2>From Doing to Being</h2>
            
            <p>Impact is often about doing—influence is about being. The most influential leaders are those who can articulate not just what they've done, but who they've become through the doing.</p>
            
            <p>This shift from doing to being is where influence deepens. It's where communication moves from transactional to transformational.</p>
            
            <h2>The Legacy Question</h2>
            
            <p>Here's a question I often ask leaders: What do you want people to remember about your work?</p>
            
            <p>The answer to this question points toward your influence legacy. It's not just about what you built—it's about how you communicated what you built.</p>
            
            <h2>Your Voice, Your Legacy</h2>
            
            <p>You've done the work. You've built something real. Now it's time to speak about it in a way that creates the influence your work deserves.</p>
            
            <p>Your voice is your legacy. Finding it, owning it, and using it is the bridge from impact to influence.</p>
        `,
    },
    "the-myth-of-the-perfect-speaker": {
        title: "The Myth of the Perfect Speaker",
        category: "Speaking",
        date: "February 1, 2026",
        readTime: "6 min read",
        image: "/carousel/img7.webp",
        content: `
            <p>Perfection isn't the goal of great speaking. Connection is. Here's why vulnerability is your greatest strength.</p>
            
            <p>In my work with leaders, I encounter a common belief: to be a great speaker, you need to be perfect. Flawless delivery. Polished presence. No mistakes, no hesitation, no vulnerability.</p>
            
            <p>This belief is not only wrong—it's counterproductive.</p>
            
            <h2>The Perfection Trap</h2>
            
            <p>The pursuit of perfection in speaking is a trap. It creates anxiety. It stifles authenticity. It prevents genuine connection.</p>
            
            <p>When you're focused on being perfect, you're focused on yourself—your performance, your image, your perceived competence. This self-focus is the enemy of connection.</p>
            
            <h2>What Audiences Actually Want</h2>
            
            <p>Here's what I've learned from three decades of working with speakers and audiences: audiences don't want perfection. They want authenticity.</p>
            
            <p>They want to connect with a real human being, not a polished performance. They want to feel something, not just hear something. They want to be engaged, not impressed.</p>
            
            <h2>The Power of Vulnerability</h2>
            
            <p>Vulnerability is not weakness in speaking—it's strength. When you allow yourself to be seen, flaws and all, you create space for genuine connection.</p>
            
            <p>Vulnerability doesn't mean oversharing or being unprofessional. It means being real—acknowledging when you don't have all the answers, sharing your struggles, letting your humanity show.</p>
            
            <h2>Connection Over Perfection</h2>
            
            <p>The goal of speaking is not to demonstrate perfection. The goal is to create connection.</p>
            
            <p>Connection happens when you meet your audience where they are—when you speak to their experience, their concerns, their hopes. Connection happens through shared humanity, not superior performance.</p>
            
            <h2>The Authenticity Advantage</h2>
            
            <p>Authentic speakers have an advantage that perfect speakers can never match: they're believable.</p>
            
            <p>When you speak authentically, people trust you. When you try to be perfect, people sense the performance and their guard goes up.</p>
            
            <h2>Mistakes as Connection</h2>
            
            <p>Even mistakes can be opportunities for connection. When you stumble and recover with grace, you show that you're human. When you acknowledge a mistake honestly, you build trust.</p>
            
            <p>The most memorable speaking moments often come not from flawless delivery, but from authentic response to the unexpected.</p>
            
            <h2>Preparation Without Performance</h2>
            
            <p>This doesn't mean you shouldn't prepare. Preparation is important. But preparation should serve authenticity, not replace it.</p>
            
            <p>Prepare so thoroughly that you can be present. Know your material so well that you can focus on connection rather than recall.</p>
            
            <h2>The Courage to Be Real</h2>
            
            <p>Letting go of perfection requires courage. It means risking judgment. It means accepting that you won't always look or sound your best.</p>
            
            <p>But this courage is rewarded with deeper connection, greater influence, and more meaningful impact.</p>
            
            <h2>Your Voice, Not a Performance</h2>
            
            <p>Your voice is not a performance to be perfected. It's an expression of who you are.</p>
            
            <p>When you speak from your authentic voice—flaws, hesitations, and all—you create something that no perfect performance can match: genuine human connection.</p>
            
            <p>That's the goal of speaking. That's what moves rooms. That's what creates influence.</p>
        `,
    },
    "leading-with-emotional-intelligence": {
        title: "Leading With Emotional Intelligence",
        category: "Leadership",
        date: "January 25, 2026",
        readTime: "7 min read",
        image: "/carousel/img8.webp",
        content: `
            <p>The most influential leaders understand that logic alone doesn't move people—emotion does. Here's how to harness both.</p>
            
            <p>In the world of leadership, there's often an emphasis on rationality. Data-driven decisions. Logical arguments. Objective analysis.</p>
            
            <p>These are important. But they're not enough.</p>
            
            <h2>The Emotional Dimension of Leadership</h2>
            
            <p>Leadership is fundamentally an emotional endeavor. People are not purely rational beings—they are emotional beings who use rationality.</p>
            
            <p>The most influential leaders understand this. They know that to move people, you must engage both their minds and their hearts.</p>
            
            <h2>Logic and Emotion: Not Opposites</h2>
            
            <p>Logic and emotion are often presented as opposites—head versus heart, reason versus feeling. But this framing is misleading.</p>
            
            <p>The most powerful communication combines logic and emotion. It provides rational substance and emotional resonance. It engages the intellect and touches the heart.</p>
            
            <h2>The Role of Emotional Intelligence</h2>
            
            <p>Emotional intelligence is the ability to recognize, understand, and manage emotions—your own and others'. It's not a soft skill; it's a leadership essential.</p>
            
            <p>Leaders with high emotional intelligence can read a room, sense unspoken concerns, and respond in ways that build trust and connection.</p>
            
            <h2>Self-Awareness as Foundation</h2>
            
            <p>The foundation of emotional intelligence is self-awareness—understanding your own emotional landscape.</p>
            
            <p>What triggers you? What motivates you? How do your emotions affect your communication and decision-making?</p>
            
            <p>Without self-awareness, you cannot effectively manage your emotions or respond to others' emotions.</p>
            
            <h2>Empathy in Action</h2>
            
            <p>Empathy is the ability to understand and share the feelings of others. It's not just a nice-to-have quality—it's essential for influence.</p>
            
            <p>When leaders demonstrate empathy, they create psychological safety. They build trust. They make it safe for others to engage authentically.</p>
            
            <h2>Emotional Regulation</h2>
            
            <p>Emotional regulation is the ability to manage your emotions effectively—not suppress them, but channel them constructively.</p>
            
            <p>This doesn't mean never feeling or expressing emotion. It means expressing emotion appropriately and in ways that serve your leadership goals.</p>
            
            <h2>Communication That Moves</h2>
            
            <p>Emotionally intelligent leaders communicate in ways that move people. They use stories, not just statistics. They speak to hopes and fears, not just facts and figures.</p>
            
            <p>They understand that people may forget what you said, but they will never forget how you made them feel.</p>
            
            <h2>The Trust Factor</h2>
            
            <p>Trust is built through emotional connection, not just rational assessment. When leaders demonstrate emotional intelligence, they build trust more quickly and deeply.</p>
            
            <p>People trust leaders who understand them, who care about them, who can read and respond to their emotional needs.</p>
            
            <h2>Developing Emotional Intelligence</h2>
            
            <p>The good news is that emotional intelligence can be developed. It begins with awareness and practice.</p>
            
            <p>Pay attention to emotions—yours and others'. Reflect on your emotional responses. Practice empathy. Seek feedback on how you come across emotionally.</p>
            
            <h2>The Integrated Leader</h2>
            
            <p>The most effective leaders integrate logic and emotion. They are rational and emotional. They engage minds and hearts.</p>
            
            <p>This integration is not a contradiction—it's a complement. Logic provides substance; emotion provides connection. Both are necessary for true influence.</p>
            
            <h2>Leading With Heart and Head</h2>
            
            <p>Leadership with emotional intelligence is not about being soft—it's about being fully human.</p>
            
            <p>When you lead with both heart and head, you create the conditions for genuine influence. You move people not just to understand, but to care, to commit, to act.</p>
            
            <p>That's the power of emotional intelligence in leadership.</p>
        `,
    },
};

// Get the current article or redirect to 404
const article = articles[slug];

// Handle 404
if (!article) {
    throw createError({
        statusCode: 404,
        statusMessage: "Article not found",
    });
}

// Set page meta
useHead({
    title: `${article.title} — True Influence Method™️`,
    meta: [
        {
            name: "description",
            content: article.content.replace(/<[^>]*>/g, "").substring(0, 160),
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
                    :src="article.image"
                    alt="Article cover"
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
                        to="/resources/articles"
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
                        Back to Articles
                    </NuxtLink>
                    <span class="text-[#faf8f5]/30">|</span>
                    <span
                        class="text-[#d4952a] text-sm font-medium tracking-[0.2em] uppercase"
                    >
                        {{ article.category }}
                    </span>
                </div>

                <h1
                    class="font-serif text-3xl md:text-4xl lg:text-5xl text-[#faf8f5] mb-6 leading-tight"
                >
                    {{ article.title }}
                </h1>

                <div
                    class="flex items-center justify-center gap-4 text-sm text-[#faf8f5]/60"
                >
                    <span>{{ article.date }}</span>
                    <span class="w-1 h-1 rounded-full bg-[#d4952a]" />
                    <span>{{ article.readTime }}</span>
                </div>
            </div>
        </section>

        <!-- Article Content Section -->
        <section class="py-16 md:py-24 relative">
            <div
                class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e] via-[#232360] to-[#1a1a4e]"
            />

            <div class="max-w-3xl mx-auto px-6 relative z-10">
                <article>
                    <div v-html="article.content" class="article-content" />
                </article>
            </div>
        </section>

        <!-- Related Articles Section -->
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
                        More Articles & Insights
                    </h2>
                    <p class="text-[#faf8f5]/60 max-w-2xl mx-auto">
                        Explore more perspectives on leadership, communication,
                        and authentic influence.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <NuxtLink
                        v-for="(relatedArticle, relatedSlug) in articles"
                        v-show="relatedSlug !== slug"
                        :key="relatedSlug"
                        :to="`/resources/articles/${relatedSlug}`"
                        class="group bg-[#1a1a4e]/50 backdrop-blur-sm rounded-xl border border-[#faf8f5]/10 hover:border-[#d4952a]/30 transition-all duration-300 overflow-hidden"
                    >
                        <div class="relative aspect-[16/10] overflow-hidden">
                            <img
                                :src="relatedArticle.image"
                                :alt="relatedArticle.title"
                                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />
                            <div class="absolute top-4 left-4">
                                <span
                                    class="inline-block px-3 py-1 bg-[#d4952a] text-[#1a1a4e] text-xs font-semibold rounded-full"
                                >
                                    {{ relatedArticle.category }}
                                </span>
                            </div>
                        </div>

                        <div class="p-6">
                            <h3
                                class="font-serif text-lg text-[#faf8f5] mb-3 leading-tight group-hover:text-[#d4952a] transition-colors"
                            >
                                {{ relatedArticle.title }}
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
