<script lang="ts">
	import { onMount } from 'svelte';

    // Data for sections
    const navLinks = ["Platform", "Courses", "For Teams", "Resources", "Pricing"];
    
    const logos = [
        { name: "Stripe", width: 100 },
        { name: "Shopify", width: 100 },
        { name: "Notion", width: 90 },
        { name: "Figma", width: 80 },
        { name: "Atlassian", width: 110 },
        { name: "Salesforce", width: 120 },
        { name: "HubSpot", width: 90 }
    ];

    const features = [
        {
            tag: "AI-POWERED PRACTICE",
            title: "Real-world scenarios that build actual skills",
            image: "phone",
            color: "bg-gray-100"
        },
        {
            tag: "EXPERT-LED COURSES",
            title: "Learn from industry leaders who've done it",
            image: "video",
            color: "bg-gray-100"
        },
        {
            tag: "AUTOMATED COHORTS",
            title: "Peer learning without the manual coordination",
            image: "search",
            color: "bg-gray-100"
        },
        {
            tag: "PERFORMANCE TRACKING",
            title: "Measure real skill gains, not just completion",
            image: "editor",
            color: "bg-gray-100"
        },
        {
            tag: "ADAPTIVE LEARNING",
            title: "AI adjusts difficulty to each learner's level",
            image: "admin",
            color: "bg-gray-100"
        },
        {
            tag: "OUTCOMES ANALYTICS",
            title: "Prove ROI with performance metrics that matter",
            image: "analytics",
            color: "bg-gray-100"
        }
    ];

    const testimonials = [
        {
            quote: "Uplimit transformed our AI upskilling from a checkbox exercise to measurable performance gains. Our engineers are actually applying what they learn.",
            name: "Sarah Chen",
            role: "VP of Engineering at TechCorp",
            avatar: "SC"
        },
        {
            quote: "Finally, a learning platform that focuses on practice and outcomes instead of just content consumption. Our completion rates went from 20% to 85%.",
            name: "Michael Rodriguez",
            role: "Head of L&D at DataFlow",
            avatar: "MR"
        },
         {
            quote: "The automated cohort management saved our team hundreds of hours. We can now run continuous learning programs without the operational overhead.",
            name: "Jennifer Park",
            role: "Director of People Operations at CloudScale",
            avatar: "JP"
        },
        {
            quote: "Uplimit's AI-powered practice scenarios are incredibly realistic. Our sales team improved their pitch conversion by 40% after completing the program.",
            name: "David Thompson",
            role: "VP of Sales Enablement at GrowthLabs",
            avatar: "DT"
        },
        {
            quote: "We've tried other platforms, but Uplimit is the only one that delivers measurable skill development. The performance analytics are game-changing.",
            name: "Lisa Martinez",
            role: "Chief Learning Officer at InnovateCo",
            avatar: "LM"
        },
        {
            quote: "The expert-led courses combined with AI practice create the perfect learning experience. Our team is more engaged than ever.",
            name: "James Wilson",
            role: "Head of Talent Development at FutureTech",
            avatar: "JW"
        }
    ];

    const partnershipServices = [
        "Dedicated success manager",
        "Custom course development",
        "Cohort design and scheduling",
        "Integration with your HRIS",
        "Performance analytics setup",
        "Train-the-trainer programs",
        "Ongoing content updates and support"
    ];

    const comparisons = [
        {
            tag: "ENGAGEMENT",
            left: "Low completion rates (10-20%) with passive video watching and reading",
            right: "High completion rates (80%+) through active practice and peer accountability"
        },
        {
            tag: "SKILL DEVELOPMENT",
            left: "Measure course completions and quiz scores, not actual performance",
            right: "Track real skill gains through AI-assessed practice scenarios and performance metrics"
        },
        {
            tag: "COHORT MANAGEMENT",
            left: "Manual scheduling, reminders, and coordination eating up L&D team time",
            right: "Automated cohort operations handle scheduling, matching, and progress tracking"
        },
        {
            tag: "CONTENT DELIVERY",
            left: "One-size-fits-all courses that don't adapt to individual needs",
            right: "AI-powered adaptive learning adjusts difficulty and focus based on performance"
        },
        {
            tag: "ROI MEASUREMENT",
            left: "Struggle to prove impact with vanity metrics like hours spent learning",
            right: "Demonstrate clear ROI with measurable performance improvements and skill assessments"
        }
    ];

    const faqs = [
        "What types of skills can teams learn on Uplimit?",
        "How does AI-powered practice work?",
        "What makes Uplimit different from traditional LMS platforms?",
        "How do you measure learning outcomes?",
        "Can we create custom courses for our team?",
        "How does automated cohort management work?",
        "What integrations does Uplimit support?",
        "What is Uplimit's pricing model?",
        "How do you ensure data security and privacy?"
    ];

</script>

<div class="font-sans text-gray-900 bg-white selection:bg-primary-200 selection:text-black">
    <!-- Navbar -->
    <nav class="sticky top-0 z-50 bg-white/80 backdrop-blur-md border-b border-gray-100">
        <div class="max-w-[1400px] mx-auto px-6 h-16 flex items-center justify-between">
            <div class="flex items-center gap-2">
                <!-- Logo Mark -->
                <svg width="24" height="24" viewBox="0 0 66 65" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-black">
                    <path fill-rule="evenodd" clip-rule="evenodd" d="M44.0354 13.173H0.658203V0H65.4257V64.7675H52.2527V23.5853L11.9021 63.9358L2.58738 54.6211L44.0354 13.173Z" fill="currentColor"/>
                </svg>
                <span class="font-medium text-lg tracking-tight">Uplimit</span>
            </div>

            <div class="hidden md:flex items-center gap-8 text-sm font-medium text-gray-600">
                {#each navLinks as link}
                    <a href="#" class="hover:text-black transition-colors">{link}</a>
                {/each}
            </div>

            <button class="bg-black text-white px-5 py-2 rounded-full text-sm font-medium hover:bg-gray-800 transition-colors">
                Get started
            </button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="pt-20 pb-16 px-6 text-center overflow-hidden">
        <div class="max-w-4xl mx-auto mb-12">
            <h1 class="font-serif text-6xl md:text-7xl lg:text-[5rem] leading-[1.1] mb-6 font-normal tracking-tight">
                Workforce learning <br/> that drives performance
            </h1>
            <p class="text-lg md:text-xl text-gray-600 max-w-2xl mx-auto mb-8 leading-relaxed">
                AI-powered practice, expert-led courses, and automated cohorts that deliver measurable skill development—not just completions.
            </p>
            <button class="bg-black text-white px-8 py-3 rounded-full text-base font-medium hover:bg-gray-800 transition-colors">
                Get started
            </button>
        </div>

        <!-- Hero Image Collage Mockup -->
        <div class="relative max-w-[1400px] mx-auto h-[400px] md:h-[600px] mt-12 select-none pointer-events-none">
            <!-- We will build a CSS composition of screens -->
            <div class="relative w-full h-full flex justify-center items-end">
                
                <!-- Left Laptop -->
                <div class="absolute left-[-10%] bottom-0 w-[60%] md:w-[45%] z-10 transform -translate-x-10 translate-y-10">
                     <div class="bg-gray-900 rounded-t-xl p-1 shadow-2xl border border-gray-800 aspect-[16/10] overflow-hidden">
                        <!-- Screen Content -->
                        <div class="bg-gray-800 w-full h-full rounded-lg relative overflow-hidden">
                            <div class="absolute inset-0 bg-gradient-to-br from-blue-900 to-black opacity-80"></div>
                            <div class="p-4 text-white">
                                <div class="text-xs text-gray-400 mb-2">Space Tech</div>
                                <div class="h-2 w-20 bg-gray-600 rounded mb-4"></div>
                                <div class="grid grid-cols-2 gap-4">
                                    <div class="h-20 bg-gray-700/50 rounded"></div>
                                    <div class="h-20 bg-gray-700/50 rounded"></div>
                                </div>
                            </div>
                        </div>
                     </div>
                </div>

                <!-- Center Laptop (Main) -->
                <div class="absolute bottom-0 z-20 w-[70%] md:w-[50%] transform translate-y-5">
                    <div class="bg-black rounded-t-2xl p-2 shadow-2xl border border-gray-800 aspect-[16/10]">
                        <div class="bg-white w-full h-full rounded-xl overflow-hidden relative">
                            <!-- Mock UI -->
                            <div class="flex h-full">
                                <div class="w-1/3 bg-gray-50 p-4 border-r border-gray-100">
                                    <div class="h-8 w-8 bg-gray-200 rounded-full mb-4"></div>
                                    <div class="h-2 w-20 bg-gray-200 rounded mb-2"></div>
                                    <div class="h-2 w-16 bg-gray-200 rounded mb-6"></div>
                                    <div class="space-y-2">
                                        <div class="h-8 w-full bg-white border border-gray-200 rounded shadow-sm"></div>
                                        <div class="h-8 w-full bg-transparent rounded"></div>
                                    </div>
                                </div>
                                <div class="w-2/3 p-4">
                                    <div class="h-32 bg-gray-100 rounded-lg mb-4 flex items-center justify-center">
                                        <div class="w-12 h-12 bg-gray-300 rounded-full"></div>
                                    </div>
                                    <div class="h-4 w-3/4 bg-gray-100 rounded mb-2"></div>
                                    <div class="h-4 w-1/2 bg-gray-100 rounded"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Right Phone/Tablet -->
                <div class="absolute right-[-5%] bottom-10 w-[25%] md:w-[15%] z-30 transform translate-x-5">
                    <div class="bg-black rounded-[2rem] p-2 shadow-2xl border border-gray-800 aspect-[9/19]">
                        <div class="bg-white w-full h-full rounded-[1.5rem] overflow-hidden p-2 flex flex-col">
                             <div class="h-4 w-20 bg-gray-100 rounded mx-auto mb-4 mt-2"></div>
                             <div class="flex-1 bg-gray-50 rounded-xl p-2">
                                <div class="h-16 bg-primary-50 rounded-lg mb-2"></div>
                                <div class="h-16 bg-gray-100 rounded-lg mb-2"></div>
                             </div>
                        </div>
                    </div>
                </div>

                 <!-- Another Right Screen (Tablet?) -->
                <div class="absolute right-[10%] bottom-0 w-[40%] md:w-[30%] z-10 transform translate-x-10 translate-y-10">
                     <div class="bg-white rounded-t-xl p-1 shadow-2xl border border-gray-200 aspect-[4/3] overflow-hidden">
                        <div class="bg-gray-50 w-full h-full rounded-lg p-3">
                             <div class="flex gap-2 mb-3">
                                <div class="w-1/3 h-20 bg-white shadow-sm rounded-lg"></div>
                                <div class="w-1/3 h-20 bg-white shadow-sm rounded-lg"></div>
                                <div class="w-1/3 h-20 bg-white shadow-sm rounded-lg"></div>
                             </div>
                             <div class="h-32 bg-white shadow-sm rounded-lg"></div>
                        </div>
                     </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Logos Section -->
    <section class="py-16 border-b border-gray-100">
        <div class="max-w-[1400px] mx-auto px-6 text-center">
            <p class="text-sm text-gray-500 mb-10">Trusted by high-growth teams worldwide</p>
            <div class="flex flex-wrap justify-center items-center gap-12 md:gap-16 opacity-70 grayscale hover:grayscale-0 transition-all duration-500">
                {#each logos as logo}
                    <div class="h-8 flex items-center justify-center">
                        <!-- Placeholder for logo text/svg -->
                        <span class="font-bold text-xl font-serif italic">{logo.name}</span>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Meet Uplimit Grid -->
    <section class="py-24 px-6 bg-gray-50">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">How Uplimit works</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    Move beyond passive content consumption. Uplimit combines AI-powered practice, expert instruction, and peer learning to deliver the completion rates and performance outcomes L&D teams need.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                {#each features as feature}
                    <div class="group bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition-shadow duration-300 flex flex-col h-[500px]">
                        <div class="p-8 pb-0 flex-1">
                            <span class="inline-block bg-primary-100 text-primary-700 text-[10px] font-bold tracking-wider px-2 py-1 rounded mb-4 uppercase">
                                {feature.tag}
                            </span>
                            <h3 class="font-serif text-2xl leading-tight mb-4">
                                {feature.title}
                            </h3>
                        </div>
                        <div class="h-[300px] bg-gray-100 relative overflow-hidden mt-4 mx-4 rounded-t-xl group-hover:translate-y-[-5px] transition-transform duration-500">
                            <!-- Mockup Content based on type -->
                            {#if feature.image === 'phone'}
                                <div class="absolute bottom-[-20px] left-1/2 transform -translate-x-1/2 w-[180px] h-[350px] bg-black rounded-[2rem] border-4 border-black shadow-xl overflow-hidden">
                                     <div class="bg-white w-full h-full p-3 pt-8">
                                        <div class="h-2 w-12 bg-gray-200 rounded mx-auto mb-4"></div>
                                        <div class="space-y-2">
                                            <div class="h-16 bg-gray-50 rounded-lg"></div>
                                            <div class="h-16 bg-gray-50 rounded-lg"></div>
                                        </div>
                                     </div>
                                </div>
                            {:else if feature.image === 'video'}
                                <div class="absolute inset-0 p-4 flex items-end justify-center">
                                    <div class="w-full h-[90%] bg-gray-800 rounded-t-lg shadow-lg relative overflow-hidden">
                                        <div class="absolute inset-0 flex items-center justify-center text-white/20">
                                            <svg width="48" height="48" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 14.5v-9l6 4.5-6 4.5z"/></svg>
                                        </div>
                                        <div class="absolute bottom-4 left-4 flex gap-2">
                                            <div class="w-8 h-8 bg-gray-600 rounded-full"></div>
                                            <div class="w-8 h-8 bg-gray-600 rounded-full"></div>
                                        </div>
                                    </div>
                                </div>
                            {:else if feature.image === 'search'}
                                 <div class="absolute bottom-[-40px] right-[-20px] w-full h-full bg-white shadow-lg rounded-tl-2xl p-6 border border-gray-100">
                                     <div class="flex items-center gap-3 mb-4 border-b pb-4">
                                         <div class="w-8 h-8 bg-primary-200 rounded-full"></div>
                                         <div class="h-2 w-32 bg-gray-200 rounded"></div>
                                     </div>
                                     <div class="space-y-3">
                                         <div class="h-2 w-full bg-gray-100 rounded"></div>
                                         <div class="h-2 w-5/6 bg-gray-100 rounded"></div>
                                         <div class="h-2 w-4/6 bg-gray-100 rounded"></div>
                                     </div>
                                 </div>
                            {:else}
                                <div class="absolute inset-4 bg-white shadow-sm rounded-lg border border-gray-100 flex items-center justify-center">
                                    <div class="text-gray-300">UI Mockup</div>
                                </div>
                            {/if}
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Loved by L&D teams <br/> and learners alike</h2>
                <p class="text-lg text-gray-600 leading-relaxed mb-10">
                    High engagement meets measurable outcomes. <br/> Finally, a learning platform that delivers on both.
                </p>
            </div>

            <div class="columns-1 md:columns-2 lg:columns-3 gap-6 space-y-6">
                {#each testimonials as testimonial}
                    <div class="break-inside-avoid bg-gray-50 p-8 rounded-2xl">
                        <p class="text-lg leading-relaxed mb-6">"{testimonial.quote}"</p>
                        <div class="flex items-center gap-3">
                            <div class="w-10 h-10 bg-gray-300 rounded-full flex items-center justify-center text-sm font-bold text-gray-600">
                                {testimonial.avatar}
                            </div>
                            <div>
                                <div class="font-medium">{testimonial.name}</div>
                                <div class="text-sm text-gray-500">{testimonial.role}</div>
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Partnership Section -->
    <section class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Built for enterprise <br/> scale and success</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    From onboarding to ongoing support, we're with you every step <br/> of the way to ensure your learning programs succeed.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div class="bg-gray-50 p-12 rounded-3xl h-full">
                    <h3 class="font-serif text-2xl mb-8">Enterprise support included</h3>
                    <ul class="space-y-4">
                        {#each partnershipServices as service}
                            <li class="flex items-center gap-3">
                                <div class="w-5 h-5 rounded-full bg-black flex items-center justify-center shrink-0">
                                    <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>
                                </div>
                                <span class="text-gray-700">{service}</span>
                            </li>
                        {/each}
                    </ul>
                </div>
                <div class="h-full min-h-[500px] rounded-3xl overflow-hidden relative">
                    <!-- Placeholder image for people collaborating -->
                    <div class="absolute inset-0 bg-gray-200">
                        <div class="w-full h-full bg-[url('https://images.unsplash.com/photo-1522071820081-009f0129c71c?q=80&w=2070&auto=format&fit=crop')] bg-cover bg-center grayscale opacity-80 hover:grayscale-0 transition-all duration-700"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Case Studies Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
            <div class="flex justify-between items-end mb-12">
                <p class="text-lg text-gray-600 max-w-xl">Real teams, real results. See how Uplimit drives performance.</p>
                <div class="flex gap-2">
                    <button class="w-10 h-10 rounded-full border border-gray-200 flex items-center justify-center hover:bg-gray-50">
                        ←
                    </button>
                    <button class="w-10 h-10 rounded-full bg-black text-white flex items-center justify-center hover:bg-gray-800">
                        →
                    </button>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- Card 1 -->
                <div class="aspect-[4/5] relative rounded-2xl overflow-hidden group cursor-pointer">
                    <div class="absolute inset-0 bg-gray-900">
                        <!-- Mock Background Image -->
                        <div class="absolute inset-0 opacity-50 bg-gradient-to-t from-black via-transparent to-transparent"></div>
                        <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1549317661-bd32c8ce0db2?q=80&w=2070&auto=format&fit=crop')] bg-cover bg-center mix-blend-overlay opacity-40"></div>
                    </div>
                    <div class="absolute inset-0 p-8 flex flex-col justify-between text-white">
                        <div>
                            <h3 class="font-serif text-3xl leading-tight mb-4">TechCorp achieves 85% completion rate on AI upskilling</h3>
                            <div class="text-xs text-gray-300 uppercase tracking-wider">Employees: 2500 <br/> Industry: Technology</div>
                        </div>
                        <div class="font-bold text-xl">TechCorp</div>
                    </div>
                </div>

                <!-- Card 2 -->
                <div class="aspect-[4/5] relative rounded-2xl overflow-hidden group cursor-pointer">
                    <div class="absolute inset-0 bg-gray-900">
                         <div class="absolute inset-0 opacity-50 bg-gradient-to-t from-black via-transparent to-transparent"></div>
                         <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1542744173-8e7e53415bb0?q=80&w=2070&auto=format&fit=crop')] bg-cover bg-center mix-blend-overlay opacity-40"></div>
                    </div>
                    <div class="absolute inset-0 p-8 flex flex-col justify-between text-white">
                        <div>
                            <h3 class="font-serif text-3xl leading-tight mb-4">GrowthLabs improves sales performance by 40%</h3>
                            <div class="text-xs text-gray-300 uppercase tracking-wider">Employees: 850 <br/> Industry: SaaS</div>
                        </div>
                        <div class="font-bold text-xl">GrowthLabs</div>
                    </div>
                </div>

                <!-- Card 3 -->
                <div class="aspect-[4/5] relative rounded-2xl overflow-hidden group cursor-pointer">
                    <div class="absolute inset-0 bg-gray-900">
                         <div class="absolute inset-0 opacity-50 bg-gradient-to-t from-black via-transparent to-transparent"></div>
                         <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?q=80&w=2070&auto=format&fit=crop')] bg-cover bg-center mix-blend-overlay opacity-40"></div>
                    </div>
                    <div class="absolute inset-0 p-8 flex flex-col justify-between text-white">
                        <div>
                            <h3 class="font-serif text-3xl leading-tight mb-4">InnovateCo reduces onboarding time by 60%</h3>
                            <div class="text-xs text-gray-300 uppercase tracking-wider">Employees: 5000 <br/> Industry: Financial Services</div>
                        </div>
                        <div class="font-bold text-xl">InnovateCo</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Comparison Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">From low engagement <br/> to high performance</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    Traditional learning platforms focus on content delivery. <br/> Uplimit focuses on measurable outcomes.
                </p>
            </div>

            <div class="border-t border-gray-100">
                <div class="grid grid-cols-3 py-4 text-xs text-gray-400 uppercase tracking-wider border-b border-gray-100">
                    <div>Traditional platforms</div>
                    <div class="text-center">→</div>
                    <div>Uplimit</div>
                </div>
                {#each comparisons as item}
                    <div class="grid grid-cols-1 md:grid-cols-[1fr_auto_1fr] gap-8 py-12 border-b border-gray-100 items-center group hover:bg-gray-50 transition-colors px-4 -mx-4 rounded-xl">
                        <div class="text-gray-500 leading-relaxed md:pr-8">
                            {item.left}
                        </div>
                        <div class="flex justify-center">
                            <span class="bg-primary-100 text-primary-700 text-[10px] font-bold tracking-wider px-2 py-1 rounded uppercase whitespace-nowrap">
                                {item.tag}
                            </span>
                        </div>
                        <div class="text-black font-medium leading-relaxed md:pl-8">
                            {item.right}
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Integrations & Security Section -->
    <section class="py-24 px-6 bg-white">
        <div class="max-w-[1400px] mx-auto">
             <div class="text-center max-w-3xl mx-auto mb-20">
                <h2 class="font-serif text-5xl md:text-6xl mb-6">Enterprise-ready <br/> from day one</h2>
                <p class="text-lg text-gray-600 leading-relaxed">
                    Seamless integrations and enterprise-grade security built in.
                </p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
                <!-- Integrations -->
                <div>
                    <div class="text-center mb-8">
                        <span class="bg-primary-100 text-primary-700 text-[10px] font-bold tracking-wider px-2 py-1 rounded uppercase">
                            INTEGRATES WITH YOUR STACK
                        </span>
                    </div>
                    <div class="grid grid-cols-4 gap-6">
                        {#each ['Slack', 'Teams', 'Zoom', 'Workday', 'BambooHR', 'Greenhouse', 'Lever', 'Salesforce', 'HubSpot', 'Google Workspace', 'Okta', 'Azure AD'] as tool}
                            <div class="aspect-square bg-gray-50 rounded-xl flex flex-col items-center justify-center p-4 hover:bg-gray-100 transition-colors">
                                <div class="w-8 h-8 bg-gray-200 rounded-full mb-2"></div> <!-- Icon Placeholder -->
                                <span class="text-[10px] text-center text-gray-600 font-medium">{tool}</span>
                            </div>
                        {/each}
                    </div>
                </div>

                <!-- Security -->
                <div>
                    <div class="text-center mb-8">
                        <span class="bg-primary-100 text-primary-700 text-[10px] font-bold tracking-wider px-2 py-1 rounded uppercase">
                            ENTERPRISE SECURITY
                        </span>
                    </div>
                    <div class="grid grid-cols-4 gap-6">
                         {#each ['SOC 2 Type 2', 'GDPR compliant', 'SSO/SAML', 'Role-based access', 'Data encryption', 'Audit logs', 'Privacy controls', 'Compliance ready', 'Secure APIs', 'Regular audits', 'Data residency', 'Backup & recovery'] as item}
                            <div class="aspect-square bg-gray-50 rounded-xl flex flex-col items-center justify-center p-2 hover:bg-gray-100 transition-colors">
                                <div class="w-6 h-6 border-2 border-gray-300 rounded mb-2"></div> <!-- Icon Placeholder -->
                                <span class="text-[10px] text-center text-gray-600 font-medium leading-tight">{item}</span>
                            </div>
                        {/each}
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mission Section -->
    <section class="py-24 px-6">
        <div class="max-w-[1400px] mx-auto grid grid-cols-1 lg:grid-cols-2 min-h-[600px]">
            <div class="bg-white relative flex items-center justify-center p-12 overflow-hidden">
                <div class="flex gap-4 transform -rotate-6 scale-90">
                    <div class="w-64 h-80 bg-primary-600 flex items-center justify-center text-white font-bold text-4xl shadow-2xl">AI LEARNING</div>
                    <div class="w-64 h-80 bg-black flex items-center justify-center text-white font-bold text-4xl shadow-2xl z-10 -mt-12">PRACTICE</div>
                    <div class="w-64 h-80 bg-primary-400 flex items-center justify-center text-white font-bold text-4xl shadow-2xl">OUTCOMES</div>
                </div>
            </div>
            <div class="bg-primary-50 p-12 lg:p-24 flex flex-col justify-center">
                <p class="font-serif text-3xl md:text-4xl leading-tight mb-8">
                    Uplimit was founded by learning, product, and AI experts who saw firsthand how traditional platforms fail to deliver real skill development.
                </p>
                <p class="font-serif text-3xl md:text-4xl leading-tight">
                    We built Uplimit to solve the completion crisis and prove that learning programs can drive measurable performance gains when designed around practice, not passive consumption.
                </p>
            </div>
        </div>
    </section>

    <!-- Bottom CTA -->
    <section class="py-32 px-6 text-center bg-white">
        <div class="max-w-4xl mx-auto">
            <h2 class="font-serif text-6xl md:text-7xl mb-6">Ready to transform <br/> your learning programs?</h2>
            <p class="text-xl text-gray-600 mb-10">See how Uplimit can drive real performance outcomes for your team.</p>
            <button class="bg-black text-white px-8 py-3 rounded-full text-base font-medium hover:bg-gray-800 transition-colors">
                Get started
            </button>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto">
            <h2 class="font-serif text-5xl mb-16">FAQ</h2>
            <div class="space-y-4">
                {#each faqs as faq}
                    <div class="border-b border-gray-100 py-6 flex justify-between items-center cursor-pointer group hover:bg-gray-50 px-4 -mx-4 rounded-lg transition-colors">
                        <span class="text-lg font-medium">{faq}</span>
                        <div class="w-8 h-8 rounded-full bg-black text-white flex items-center justify-center group-hover:bg-gray-800 transition-colors">
                            <svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"><line x1="12" y1="5" x2="12" y2="19"></line><line x1="5" y1="12" x2="19" y2="12"></line></svg>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-24 px-6 bg-white border-t border-gray-100">
        <div class="max-w-[1400px] mx-auto grid grid-cols-1 md:grid-cols-4 gap-12">
            <div class="col-span-1 md:col-span-1">
                <div class="flex items-center gap-2 mb-8">
                     <svg width="24" height="24" viewBox="0 0 66 65" fill="none" xmlns="http://www.w3.org/2000/svg" class="text-black">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M44.0354 13.173H0.658203V0H65.4257V64.7675H52.2527V23.5853L11.9021 63.9358L2.58738 54.6211L44.0354 13.173Z" fill="currentColor"/>
                    </svg>
                    <span class="font-medium text-xl tracking-tight">Uplimit</span>
                </div>
                <div class="text-sm text-gray-500 mb-4">Stay updated on learning innovation</div>
                <div class="flex gap-2 border-b border-gray-200 pb-2 mb-8">
                    <input type="email" placeholder="Email address" class="w-full outline-none text-sm" />
                    <button class="text-gray-400 hover:text-black">→</button>
                </div>
                <div class="text-xs text-gray-400">© Uplimit 2025</div>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-3 gap-8 col-span-1 md:col-span-3">
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">Platform</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-black">Overview</a></li>
                        <li><a href="#" class="hover:text-black">AI-Powered Practice</a></li>
                        <li><a href="#" class="hover:text-black">Expert-Led Courses</a></li>
                        <li><a href="#" class="hover:text-black">Cohort Management</a></li>
                        <li><a href="#" class="hover:text-black">Analytics</a></li>
                        <li><a href="#" class="hover:text-black">Integrations</a></li>
                        <li><a href="#" class="hover:text-black">Security</a></li>
                        <li><a href="#" class="hover:text-black">Pricing</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">Resources</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-black">Case Studies</a></li>
                        <li><a href="#" class="hover:text-black">Blog</a></li>
                        <li><a href="#" class="hover:text-black">Learning Hub</a></li>
                        <li><a href="#" class="hover:text-black">Documentation</a></li>
                        <li><a href="#" class="hover:text-black">Help Center</a></li>
                        <li><a href="#" class="hover:text-black">API Reference</a></li>
                        <li><a href="#" class="hover:text-black">Webinars</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-xs font-bold text-gray-400 uppercase tracking-wider mb-6">Company</h4>
                    <ul class="space-y-3 text-sm text-gray-600">
                        <li><a href="#" class="hover:text-black">About</a></li>
                        <li><a href="#" class="hover:text-black">Careers</a></li>
                        <li><a href="#" class="hover:text-black">Team</a></li>
                        <li><a href="#" class="hover:text-black">Press</a></li>
                        <li><a href="#" class="hover:text-black">Contact</a></li>
                        <li><a href="#" class="hover:text-black">Privacy</a></li>
                        <li><a href="#" class="hover:text-black">Terms</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>

</div>

