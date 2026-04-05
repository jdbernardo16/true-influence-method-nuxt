<script setup lang="ts">
const route = useRoute();
const slug = route.params.slug as string;

// Mock blog data - in a real app, this would come from a CMS or API
const blogPosts: Record<
    string,
    {
        title: string;
        type: string;
        date: string;
        readTime: string;
        image: string;
        content: string;
    }
> = {
    "conversation-with-ceo-on-authenticity": {
        title: "A Conversation on Authenticity in Leadership",
        type: "Blog Post",
        date: "March 18, 2026",
        readTime: "8 min read",
        image: "/carousel/img2.webp",
        content: `
            <p>Last week, I had the privilege of sitting down with Sarah Chen, CEO of a Fortune 500 company, to talk about authenticity in leadership. What struck me most about our conversation was her honesty about the journey.</p>
            
            <p>"For years," Sarah told me, "I thought being a leader meant having all the answers. I thought authenticity was a luxury I couldn't afford."</p>
            
            <h2>The Mask of Competence</h2>
            
            <p>Sarah's story is not unique. In my work with executives, I've seen countless leaders who wear a mask of competence—projecting certainty they don't feel, confidence they haven't earned, and answers they don't have.</p>
            
            <p>This mask serves a purpose. It protects them from vulnerability. It creates the appearance of strength. But it comes at a cost.</p>
            
            <h2>The Cost of Inauthenticity</h2>
            
            <p>When leaders wear masks, several things happen:</p>
            
            <ul>
                <li>Trust erodes because people sense the disconnect</li>
                <li>Connection suffers because vulnerability is absent</li>
                <li>Influence diminishes because the message lacks conviction</li>
                <li>Energy drains because maintaining the mask is exhausting</li>
            </ul>
            
            <p>Sarah experienced all of these. "I was successful by every metric," she said. "But I felt hollow. And I think my team felt it too."</p>
            
            <h2>The Turning Point</h2>
            
            <p>Sarah's turning point came during a board meeting where she was asked a question she didn't know the answer to. In the past, she would have faked it—deflected, obfuscated, or made something up.</p>
            
            <p>Instead, she said: "I don't know. But I'll find out and get back to you."</p>
            
            <p>The room went quiet. Then, something unexpected happened. People nodded. They appreciated the honesty.</p>
            
            <h2>The Power of Honest Not-Knowing</h2>
            
            <p>That moment changed everything for Sarah. She realized that admitting what she didn't know was not weakness—it was strength.</p>
            
            <p>Authenticity doesn't mean having all the answers. It means being honest about what you do know—and what you don't.</p>
            
            <h2>The Journey to Authentic Leadership</h2>
            
            <p>Since that moment, Sarah has been on a journey to authentic leadership. It hasn't been easy. It's required vulnerability, courage, and a willingness to be seen.</p>
            
            <p>But the results have been transformative. Trust has increased. Connection has deepened. Her influence has grown.</p>
            
            <h2>What Authenticity Looks Like</h2>
            
            <p>For Sarah, authenticity now looks like:</p>
            
            <ul>
                <li>Admitting when she doesn't have the answer</li>
                <li>Sharing her thought process, not just conclusions</li>
                <li>Being vulnerable about challenges and uncertainties</li>
                <li>Asking for help when she needs it</li>
            </ul>
            
            <p>"I'm not a perfect leader," Sarah said. "But I'm a real one. And that's better for everyone."</p>
            
            <h2>The Lesson</h2>
            
            <p>My conversation with Sarah reinforced a truth I've seen repeatedly in my work: authenticity is not a luxury for leaders—it's essential.</p>
            
            <p>The most influential leaders are not the ones who project perfection. They're the ones who have the courage to be real.</p>
            
            <p>Your team doesn't need you to be perfect. They need you to be authentic.</p>
        `,
    },
    "podcast-episode-emotional-intelligence": {
        title: "Emotional Intelligence in Leadership Communication",
        type: "Podcast",
        date: "March 10, 2026",
        readTime: "45 min listen",
        image: "/carousel/img4.webp",
        content: `
            <p>In this episode, I join host Michael Torres for a deep dive into emotional intelligence in leadership communication.</p>
            
            <p>We explore why EQ is not a soft skill—it's a leadership essential that determines whether your communication lands or falls flat.</p>
            
            <h2>Episode Overview</h2>
            
            <p>The conversation covers:</p>
            
            <ul>
                <li>Why logic alone doesn't move people</li>
                <li>The role of self-awareness in communication</li>
                <li>How empathy builds trust and influence</li>
                <li>Emotional regulation in high-stakes situations</li>
                <li>Practical approaches to developing EQ</li>
            </ul>
            
            <h2>Key Insights</h2>
            
            <p>One of the key insights we discuss is that emotional intelligence is not about being emotional—it's about understanding emotions.</p>
            
            <p>Leaders with high EQ can read a room, sense unspoken concerns, and respond in ways that build trust and connection.</p>
            
            <h2>Self-Awareness as Foundation</h2>
            
            <p>We explore how self-awareness is the foundation of emotional intelligence. Before you can understand others' emotions, you must understand your own.</p>
            
            <p>What triggers you? What motivates you? How do your emotions affect your communication and decision-making?</p>
            
            <h2>Empathy in Action</h2>
            <p>Empathy is not just a nice-to-have quality—it's essential for influence. When leaders demonstrate empathy, they create psychological safety and build trust.</p>
            
            <p>We discuss practical ways to demonstrate empathy in communication, including active listening, acknowledging others' perspectives, and validating feelings.</p>
            
            <h2>Emotional Regulation</h2>
            
            <p>Emotional regulation is the ability to manage your emotions effectively—not suppress them, but channel them constructively.</p>
            
            <p>We explore strategies for emotional regulation, including pausing before responding, reframing situations, and using breathing techniques.</p>
            
            <h2>Developing Your EQ</h2>
            
            <p>The good news is that emotional intelligence can be developed. We discuss practical approaches to building EQ, including:</p>
            
            <ul>
                <li>Paying attention to emotions—yours and others'</li>
                <li>Reflecting on your emotional responses</li>
                <li>Practicing empathy in daily interactions</li>
                <li>Seeking feedback on how you come across</li>
            </ul>
            
            <h2>Listen to the Full Episode</h2>
            
            <p>This conversation goes deep into the role of emotional intelligence in leadership communication. Whether you're naturally empathetic or struggle with EQ, you'll find valuable insights and practical strategies.</p>
            
            <p>Tune in to discover how emotional intelligence can transform your communication and your leadership.</p>
        `,
    },
    "blog-defining-moments": {
        title: "The Defining Moments That Shape Us",
        type: "Blog Post",
        date: "March 2, 2026",
        readTime: "6 min read",
        image: "/carousel/img6.webp",
        content: `
            <p>In my work with leaders, I've discovered something consistent: every influential leader has defining moments—experiences that fundamentally shaped their leadership, their values, and their vision.</p>
            
            <p>But here's what I've also observed: most leaders have never named these moments. They carry the impact without ever articulating what happened and why it mattered.</p>
            
            <h2>What Is a Defining Moment?</h2>
            
            <p>A defining moment is not just an important experience. It's a moment of transformation—a time when something shifted in your understanding of yourself, your work, or your purpose.</p>
            
            <p>It might be a moment of failure that taught you resilience. A moment of success that revealed your values. A moment of connection that showed you what matters most.</p>
            
            <h2>The Power of Naming</h2>
            
            <p>When you name your defining moment, you unlock its power. You transform it from an unconscious influence into a conscious resource.</p>
            
            <p>Your defining moment becomes the foundation of your leadership story—the source of your authentic voice and the wellspring of your conviction.</p>
            
            <h2>My Own Defining Moment</h2>
            
            <p>I'll share one of my own defining moments. Early in my career as a coach, I was working with a senior executive who was struggling with communication. He was brilliant, prepared, and knowledgeable—but when he spoke, people tuned out.</p>
            
            <p>For weeks, I tried everything. We worked on his structure, his delivery, his presence. Nothing worked.</p>
            
            <p>Then, in a session, he told me a story about his childhood—about growing up in poverty, about the moment he decided education would be his way out, about the first time he walked into a classroom as a teacher.</p>
            
            <p>As he spoke, something shifted. His voice changed. His presence changed. The room changed.</p>
            
            <p>That was my defining moment. I realized that the problem wasn't his communication skills—it was that he wasn't speaking from his truth.</p>
            
            <h2>The Insight That Changed Everything</h2>
            
            <p>In that moment, I understood that authentic communication is not about technique—it's about truth.</p>
            
            <p>The most powerful messages don't come from perfect scripts or polished delivery. They come from lived experience and honest reflection.</p>
            
            <p>This insight became the foundation of the True Influence Method™️.</p>
            
            <h2>Finding Your Defining Moment</h2>
            
            <p>How do you identify your defining moment? It requires reflection and honesty.</p>
            
            <p>Think about the experiences that shaped you. What moments stand out as turning points? What experiences do you find yourself returning to again and again in your thinking?</p>
            
            <p>Pay attention to the stories you tell about yourself. The stories that feel most alive, most meaningful, often point toward your defining moments.</p>
            
            <h2>Your Defining Moment as Foundation</h2>
            
            <p>Your defining moment is not just personal history—it's the foundation of your leadership message.</p>
            
            <p>When you can articulate your defining moment clearly, you gain clarity about who you are as a leader and what you stand for. This clarity translates into more powerful communication.</p>
            
            <h2>The Invitation</h2>
            
            <p>I invite you to spend some time reflecting on your defining moments. What experiences shaped your leadership? What moments transformed your understanding of yourself and your work?</p>
            
            <p>Name them. Claim them. Let them become the foundation of your authentic voice.</p>
            
            <p>Your defining moment is waiting to be named. When you find it and claim it, you unlock a powerful source of leadership communication.</p>
        `,
    },
    "podcast-episode-courage": {
        title: "The Courage to Speak Your Truth",
        type: "Podcast",
        date: "February 24, 2026",
        readTime: "52 min listen",
        image: "/carousel/img8.webp",
        content: `
            <p>In this episode, I join host Alex Rivera for a conversation about what it takes to speak authentically in high-stakes environments.</p>
            
            <p>We explore why courage is not the absence of fear—it's acting despite fear. And why speaking your truth is one of the bravest things a leader can do.</p>
            
            <h2>Episode Overview</h2>
            
            <p>The conversation covers:</p>
            
            <ul>
                <li>Why speaking truth requires courage</li>
                <li>The fear of being seen and judged</li>
                <li>Courage as practice, not trait</li>
                <li>The cost of silence in leadership</li>
                <li>How to find your courage</li>
            </ul>
            
            <h2>The Fear of Being Seen</h2>
            
            <p>At its core, the hesitation to speak truth is often a fear of being seen—really seen. When you speak with conviction, you make yourself visible. You expose your thinking, your perspective, your judgment.</p>
            
            <p>This visibility feels risky. What if you're wrong? What if you're judged? What if your contribution isn't valued?</p>
            
            <h2>Courage as Practice</h2>
            
            <p>We discuss how courage is not a trait you either have or don't have—it's a practice you develop.</p>
            
            <p>Every time you speak up—especially when it's uncomfortable—you're building your courage muscle. You're proving to yourself that you can handle the visibility, the risk, the potential for judgment.</p>
            
            <h2>The Cost of Silence</h2>
            
            <p>When leaders hold back, the cost is high. Important perspectives go unshared. Critical questions go unasked. The collective intelligence of the room is diminished.</p>
            
            <p>But perhaps the greatest cost is personal. When you consistently hold back your voice, you diminish your own influence.</p>
            
            <h2>Finding Your Courage</h2>
            
            <p>We explore practical approaches to finding courage, including:</p>
            
            <ul>
                <li>Recognizing that your voice matters</li>
                <li>Starting small in low-stakes situations</li>
                <li>Building confidence through practice</li>
                <li>Focusing on service rather than self</li>
            </ul>
            
            <h2>The Ripple Effect</h2>
            
            <p>When you find your courage, something interesting happens. Others are encouraged to find theirs too. Your bravery creates permission for others to speak up.</p>
            
            <p>This is how culture shifts—through individual acts of courage that ripple outward.</p>
            
            <h2>Listen to the Full Episode</h2>
            
            <p>This conversation goes deep into the courage required for authentic communication. Whether you struggle with speaking up or want to support others who do, you'll find valuable insights.</p>
            
            <p>Tune in to discover how to find the courage to speak your truth.</p>
        `,
    },
    "blog-vulnerability-strength": {
        title: "Vulnerability as Leadership Strength",
        type: "Blog Post",
        date: "February 16, 2026",
        readTime: "7 min read",
        image: "/carousel/img1.webp",
        content: `
            <p>In my work with leaders, I've observed a paradox: the most influential leaders are often the most vulnerable. Yet vulnerability is widely misunderstood as weakness.</p>
            
            <p>Let me be clear: vulnerability is not weakness. In leadership, vulnerability is strength.</p>
            
            <h2>The Myth of Invulnerability</h2>
            
            <p>There's a persistent myth that great leaders are invulnerable—that they project certainty, strength, and perfection at all times.</p>
            
            <p>This myth is not only false; it's damaging. When leaders try to be invulnerable, they create distance, erode trust, and diminish their influence.</p>
            
            <h2>What Vulnerability Actually Is</h2>
            
            <p>Vulnerability is not oversharing or being unprofessional. It's not complaining or weakness.</p>
            
            <p>Vulnerability is the courage to be seen—to show up as your authentic self, including your uncertainties, your questions, and your humanity.</p>
            
            <p>Vulnerability is admitting when you don't have the answer. It's sharing your thought process, not just conclusions. It's being honest about challenges and uncertainties.</p>
            
            <h2>Why Vulnerability Builds Trust</h2>
            
            <p>When leaders are vulnerable, something powerful happens. Trust builds more quickly and deeply.</p>
            
            <p>Why? Because vulnerability signals authenticity. When you show your humanity, people sense that you're real—not performing, not hiding, not pretending to be something you're not.</p>
            
            <p>People trust leaders who are real more than leaders who are perfect.</p>
            
            <h2>Vulnerability and Connection</h2>
            
            <p>Vulnerability creates connection. When you're honest about your experience—including the struggles and uncertainties—you create space for others to do the same.</p>
            
            <p>This creates psychological safety. When leaders are vulnerable, it signals that it's safe for others to be vulnerable too.</p>
            
            <h2>The Courage of Vulnerability</h2>
            
            <p>Vulnerability requires courage. It means risking judgment. It means accepting that you won't always look or sound your best.</p>
            
            <p>But this courage is rewarded with deeper connection, greater trust, and more meaningful influence.</p>
            
            <h2>Practical Vulnerability</h2>
            
            <p>What does vulnerability look like in practice? Here are some examples:</p>
            
            <ul>
                <li>Admitting when you don't know the answer</li>
                <li>Sharing your thought process and uncertainties</li>
                <li>Asking for help when you need it</li>
                <li>Acknowledging mistakes and what you learned</li>
                <li>Being honest about challenges you're facing</li>
            </ul>
            
            <h2>Vulnerability in High-Stakes Situations</h2>
            
            <p>Vulnerability is especially powerful in high-stakes situations. When everyone is projecting certainty and confidence, the leader who admits uncertainty stands out.</p>
            
            <p>This doesn't mean undermining confidence. It means being honest about what you know and what you don't. It means showing up with authenticity rather than performance.</p>
            
            <h2>The Invitation</h2>
            
            <p>I invite you to consider where you might be holding back your vulnerability. Where are you trying to project invulnerability instead of showing up authentically?</p>
            
            <p>Start small. Be honest about one uncertainty. Share one challenge. Ask for help once.</p>
            
            <p>Notice what happens. Notice how people respond. Notice how you feel.</p>
            
            <p>Vulnerability is not weakness. It's the foundation of authentic leadership and meaningful influence.</p>
        `,
    },
    "podcast-episode-storytelling": {
        title: "The Power of Story in Leadership",
        type: "Podcast",
        date: "February 8, 2026",
        readTime: "48 min listen",
        image: "/carousel/img3.webp",
        content: `
            <p>In this episode, I join host Lisa Park for a conversation about how leaders can use storytelling to create connection and inspire action.</p>
            
            <p>We explore why stories move people in ways that facts alone cannot—and how to craft stories that resonate with your audience.</p>
            
            <h2>Episode Overview</h2>
            
            <p>The conversation covers:</p>
            
            <ul>
                <li>Why humans are wired for story</li>
                <li>The difference between information and narrative</li>
                <li>How to identify your leadership stories</li>
                <li>Crafting stories that connect and inspire</li>
                <li>Using stories strategically in communication</li>
            </ul>
            
            <h2>The Science of Story</h2>
            
            <p>We discuss the neuroscience of storytelling—how stories engage different parts of the brain than facts and data, and how this creates emotional connection.</p>
            
            <p>When you tell a story, you're not just conveying information—you're creating an experience for your audience.</p>
            
            <h2>Your Story as Authority</h2>
            
            <p>When you speak from your own experience, you speak with a different kind of authority. You're not just conveying information—you're sharing truth that you've lived through.</p>
            
            <p>This kind of authority cannot be manufactured. It comes from having actually experienced what you're talking about.</p>
            
            <h2>Identifying Your Stories</h2>
            
            <p>We explore how to identify the stories that will resonate most with your audience. These are often:</p>
            
            <ul>
                <li>Your defining moments as a leader</li>
                <li>Challenges you've overcome</li>
                <li>Lessons you've learned the hard way</li>
                <li>Experiences that shaped your values</li>
            </ul>
            
            <h2>Crafting Stories That Connect</h2>
            
            <p>We discuss the elements of compelling stories, including:</p>
            
            <ul>
                <li>A clear beginning, middle, and end</li>
                <li>Emotional stakes and conflict</li>
                <li>Authentic details and specifics</li>
                <li>A clear lesson or insight</li>
                <li>Connection to your message</li>
            </ul>
            
            <h2>Using Stories Strategically</h2>
            
            <p>Stories are powerful, but they should be used strategically. We explore how to:</p>
            
            <ul>
                <li>Match stories to your message</li>
                <li>Use stories to illustrate key points</li>
                <li>Vary story length and complexity</li>
                <li>Connect stories to calls to action</li>
            </ul>
            
            <h2>Listen to the Full Episode</h2>
            
            <p>This conversation goes deep into the power of storytelling in leadership communication. Whether you're a natural storyteller or struggle with narrative, you'll find valuable insights.</p>
            
            <p>Tune in to discover how to use stories to create connection and inspire action.</p>
        `,
    },
    "blog-listening-communication": {
        title: "Listening as a Leadership Superpower",
        type: "Blog Post",
        date: "January 30, 2026",
        readTime: "5 min read",
        image: "/carousel/img5.webp",
        content: `
            <p>In my work with leaders, I've observed a pattern: the most influential leaders are often the best listeners.</p>
            
            <p>Yet listening is undervalued in leadership. We focus on speaking—on what to say, how to say it, how to project authority. But listening is equally important.</p>
            
            <h2>Why Listening Matters</h2>
            
            <p>Listening matters for several reasons:</p>
            
            <ul>
                <li>It builds trust by showing you value others' perspectives</li>
                <li>It provides information you can't get any other way</li>
                <li>It creates connection and psychological safety</li>
                <li>It helps you tailor your message to your audience</li>
            </ul>
            
            <p>When leaders don't listen, they miss critical information, erode trust, and diminish their influence.</p>
            
            <h2>What Real Listening Looks Like</h2>
            
            <p>Real listening is not just hearing words—it's seeking to understand. It's being fully present with the speaker, setting aside your own agenda, and genuinely trying to grasp their perspective.</p>
            
            <p>Real listening involves:</p>
            
            <ul>
                <li>Being present and focused</li>
                <li>Setting aside judgment and assumptions</li>
                <li>Asing clarifying questions</li>
                <li>Reflecting back what you hear</li>
                <li>Noticing nonverbal cues</li>
            </ul>
            
            <h2>The Trap of Waiting to Speak</h2>
            
            <p>One of the biggest barriers to listening is waiting to speak. When you're focused on what you want to say, you're not truly listening to what the other person is saying.</p>
            
            <p>This is especially common in high-stakes situations, where leaders feel pressure to contribute and demonstrate their expertise.</p>
            
            <h2>Listening and Influence</h2>
            
            <p>Here's the paradox: leaders who listen more often have more influence.</p>
            
            <p>Why? Because listening builds trust, provides valuable information, and helps you understand your audience. All of these make your communication more effective.</p>
            
            <h2>Practical Listening Skills</h2>
            
            <p>Here are practical ways to improve your listening:</p>
            
            <ul>
                <li>Practice being fully present in conversations</li>
                <li>Ask more questions, make fewer statements</li>
                <li>Reflect back what you hear before responding</li>
                <li>Notice your tendency to interrupt and pause instead</li>
                <li>Pay attention to nonverbal communication</li>
            </ul>
            
            <h2>Listening in High-Stakes Situations</h2>
            
            <p>Listening is especially important in high-stakes situations. When the pressure is on, the temptation to speak is strong—but the need to listen is even greater.</p>
            
            <p>In boardrooms, negotiations, and critical presentations, the leaders who listen first often have the most impact.</p>
            
            <h2>The Invitation</h2>
            
            <p>I invite you to consider your own listening habits. Where might you be focusing more on what you want to say than on truly understanding others?</p>
            
            <p>Practice listening in your next conversation. Notice what changes. Notice how people respond. Notice how you feel.</p>
            
            <p>Listening is not a soft skill—it's a leadership superpower that builds trust, provides insight, and amplifies your influence.</p>
        `,
    },
    "podcast-episode-legacy": {
        title: "Building a Legacy Through Your Voice",
        type: "Podcast",
        date: "January 22, 2026",
        readTime: "55 min listen",
        image: "/carousel/img7.webp",
        content: `
            <p>In this episode, I join host David Kim for a conversation about how your voice shapes your leadership legacy.</p>
            
            <p>We explore why the most enduring legacies are built not just on what leaders achieve, but on how they communicate what they achieve.</p>
            
            <h2>Episode Overview</h2>
            
            <p>The conversation covers:</p>
            
            <ul>
                <li>The relationship between voice and legacy</li>
                <li>Why impact doesn't automatically create influence</li>
                <li>The role of storytelling in legacy building</li>
                <li>How to articulate your work compellingly</li>
                <li>Creating messages that outlast your tenure</li>
            </ul>
            
            <h2>Voice and Legacy</h2>
            
            <p>Your voice is not just how you speak—it's how you articulate your values, your vision, and your impact. It's how you make your work understandable and meaningful to others.</p>
            
            <p>Leaders who find their voice create legacies that outlast their tenure. Their messages carry forward because they've been articulated clearly and compellingly.</p>
            
            <h2>The Gap Between Impact and Influence</h2>
            
            <p>We discuss the gap many leaders experience: they've built significant impact, but they struggle to articulate it in a way that creates lasting influence.</p>
            
            <p>This gap is costly. It limits reach, diminishes legacy, and prevents leaders from having the impact they could have.</p>
            
            <h2>Articulating Your Work</h2>
            
            <p>How do you articulate your work compellingly? We explore:</p>
            
            <ul>
                <li>Finding your core message</li>
                <li>Identifying your defining moments</li>
                <li>Crafting stories that illustrate your impact</li>
                <li>Developing language that is authentically yours</li>
            </ul>
            
            <h2>Messages That Outlast</h2>
            
            <p>What makes a message endure beyond a leader's tenure? We discuss the characteristics of lasting messages:</p>
            
            <ul>
                <li>They're grounded in truth and experience</li>
                <li>They're clear and memorable</li>
                <li>They connect emotionally, not just intellectually</li>
                <li>They're tied to values and purpose</li>
                <li>They're simple enough to be repeated</li>
            </ul>
            
            <h2>The Legacy Question</h2>
            
            <p>Here's a question I often ask leaders: What do you want people to remember about your work?</p>
            
            <p>The answer to this question points toward your influence legacy. It's not just about what you built—it's about how you communicated what you built.</p>
            
            <h2>Listen to the Full Episode</h2>
            
            <p>This conversation goes deep into the relationship between voice and legacy. Whether you're thinking about your legacy or just want to communicate more effectively, you'll find valuable insights.</p>
            
            <p>Tune in to discover how to build a legacy through your voice.</p>
        `,
    },
};

// Get the current blog post or redirect to 404
const post = blogPosts[slug];

// Handle 404
if (!post) {
    throw createError({
        statusCode: 404,
        statusMessage: "Blog post not found",
    });
}

// Set page meta
useHead({
    title: `${post.title} — True Influence Method™️`,
    meta: [
        {
            name: "description",
            content: post.content.replace(/<[^>]*>/g, "").substring(0, 160),
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
                    :src="post.image"
                    alt="Blog post cover"
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
                        to="/resources/blog"
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
                        Back to Blog & Podcast
                    </NuxtLink>
                    <span class="text-[#faf8f5]/30">|</span>
                    <span
                        class="text-[#d4952a] text-sm font-medium tracking-[0.2em] uppercase"
                    >
                        {{ post.type }}
                    </span>
                </div>

                <h1
                    class="font-serif text-3xl md:text-4xl lg:text-5xl text-[#faf8f5] mb-6 leading-tight"
                >
                    {{ post.title }}
                </h1>

                <div
                    class="flex items-center justify-center gap-4 text-sm text-[#faf8f5]/60"
                >
                    <span>{{ post.date }}</span>
                    <span class="w-1 h-1 rounded-full bg-[#d4952a]" />
                    <span>{{ post.readTime }}</span>
                </div>
            </div>
        </section>

        <!-- Blog Post Content Section -->
        <section class="py-16 md:py-24 relative">
            <div
                class="absolute inset-0 bg-gradient-to-b from-[#1a1a4e] via-[#232360] to-[#1a1a4e]"
            />

            <div class="max-w-3xl mx-auto px-6 relative z-10">
                <article>
                    <div v-html="post.content" class="article-content" />
                </article>
            </div>
        </section>

        <!-- Related Blog Posts Section -->
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
                        More Blog & Podcast
                    </h2>
                    <p class="text-[#faf8f5]/60 max-w-2xl mx-auto">
                        Explore more conversations, stories, and insights on
                        authentic leadership.
                    </p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <NuxtLink
                        v-for="(relatedPost, relatedSlug) in blogPosts"
                        v-show="relatedSlug !== slug"
                        :key="relatedSlug"
                        :to="`/resources/blog/${relatedSlug}`"
                        class="group bg-[#1a1a4e]/50 backdrop-blur-sm rounded-xl border border-[#faf8f5]/10 hover:border-[#d4952a]/30 transition-all duration-300 overflow-hidden"
                    >
                        <div class="relative aspect-[16/10] overflow-hidden">
                            <img
                                :src="relatedPost.image"
                                :alt="relatedPost.title"
                                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
                            />
                            <div
                                class="absolute inset-0 bg-gradient-to-t from-[#1a1a4e]/80 to-transparent"
                            />
                            <div class="absolute top-4 left-4">
                                <span
                                    class="inline-block px-3 py-1 bg-[#d4952a] text-[#1a1a4e] text-xs font-semibold rounded-full"
                                >
                                    {{ relatedPost.type }}
                                </span>
                            </div>
                        </div>

                        <div class="p-6">
                            <div
                                class="flex items-center gap-3 mb-3 text-sm text-[#faf8f5]/60"
                            >
                                <span>{{ relatedPost.date }}</span>
                                <span
                                    class="w-1 h-1 rounded-full bg-[#d4952a]"
                                />
                                <span>{{ relatedPost.readTime }}</span>
                            </div>

                            <h3
                                class="font-serif text-lg text-[#faf8f5] mb-3 leading-tight group-hover:text-[#d4952a] transition-colors"
                            >
                                {{ relatedPost.title }}
                            </h3>

                            <div
                                class="flex items-center gap-2 text-[#d4952a] text-sm font-medium group-hover:gap-3 transition-all"
                            >
                                {{
                                    relatedPost.type === "Podcast"
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
