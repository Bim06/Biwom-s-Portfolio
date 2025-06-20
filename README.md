<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Andeshi Biwom | Content & Communications Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700;800&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Neutrals (Slate, Zinc, Stone) with a Purple Accent -->
    <!-- Application Structure Plan: A top-to-bottom single-page application designed as an interactive narrative. The flow starts with a high-impact Hero and a quantitative Achievements Dashboard to immediately show value. This is followed by an interactive Skills section, a clickable Career Timeline to detail experience without overwhelming the user, and a tabbed Portfolio section to cleanly showcase different writing styles. This structure guides the user from high-level impact to detailed proof, making it more engaging and scannable than a traditional linear resume. The primary goal is to surface key data points and skills interactively to hold a recruiter's attention. -->
    <!-- Visualization & Content Choices: 
        - Achievements (e.g., 120% KPI increase, 55% ROI increase): Goal=Impress. Method=Animated Bar Chart (Chart.js). Interaction=Loads on scroll. Justification=Visually represents growth and impact more effectively than text.
        - Quantifiable Metrics (e.g., 1M installs, 60k followers): Goal=Inform. Method=Dynamic number counters. Interaction=Count-up animation on scroll. Justification=Draws attention to key figures and makes them memorable.
        - Career History: Goal=Organize. Method=Vertical Timeline. Interaction=Clicking a role expands details. Justification=Condenses a large amount of text into a manageable, user-controlled format.
        - Writing Samples: Goal=Compare Styles. Method=Tabbed content view. Interaction=Clicking tabs switches content. Justification=Allows easy comparison of different writing tones (CSR, How-To, Narrative) in a compact space.
        - Skills: Goal=Organize. Method=Grouped tags/buttons. Interaction=None (visual grouping). Justification=Simple, clean visual organization of expertise areas.
        - AI-Enhanced Descriptions: Goal=Enhance context/engagement. Method=LLM-generated text. Interaction=Click button to generate/display. Justification=Provides dynamic, enriched descriptions for portfolio pieces, showcasing depth.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc; /* slate-50 */
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -30px;
            top: 4px;
            width: 16px;
            height: 16px;
            border-radius: 50%;
            background-color: #a78bfa; /* violet-400 */
            border: 3px solid #f1f5f9; /* slate-100 */
        }
         .timeline-line {
            position: absolute;
            left: -23px;
            top: 4px;
            bottom: 4px;
            width: 2px;
            background-color: #e2e8f0; /* slate-200 */
        }
    </style>
</head>
<body class="text-slate-700">

    <nav class="sticky top-0 bg-slate-50/80 backdrop-blur-lg z-20 border-b border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <div class="flex-shrink-0">
                    <a href="#home" class="text-2xl font-bold text-slate-800">Andeshi Biwom</a>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-4">
                        <a href="#achievements" class="text-slate-600 hover:bg-slate-200 hover:text-slate-800 px-3 py-2 rounded-md text-sm font-medium">Achievements</a>
                        <a href="#skills" class="text-slate-600 hover:bg-slate-200 hover:text-slate-800 px-3 py-2 rounded-md text-sm font-medium">Skills</a>
                        <a href="#experience" class="text-slate-600 hover:bg-slate-200 hover:text-slate-800 px-3 py-2 rounded-md text-sm font-medium">Experience</a>
                        <a href="#portfolio" class="text-slate-600 hover:bg-slate-200 hover:text-slate-800 px-3 py-2 rounded-md text-sm font-medium">Portfolio</a>
                        <a href="#contact" class="text-slate-600 hover:bg-slate-200 hover:text-slate-800 px-3 py-2 rounded-md text-sm font-medium">Contact</a>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <main>
        <section id="home" class="py-24 sm:py-32 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-slate-900 tracking-tight">
                    Content Writer & Marketing Communications Strategist
                </h1>
                <p class="mt-6 max-w-3xl mx-auto text-lg sm:text-xl text-slate-600">
                    With over 5 years of experience, I craft compelling narratives and execute data-driven campaigns that build brands, engage communities, and drive growth across different sectors.
                </p>
                <div class="mt-10">
                    <a href="#portfolio" class="bg-violet-600 text-white hover:bg-violet-700 font-bold py-3 px-8 rounded-full text-lg transition duration-300">
                        View My Work
                    </a>
                </div>
            </div>
        </section>

        <section id="achievements" class="py-20 sm:py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center">
                    <h2 class="text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">Proven Impact & Results</h2>
                    <p class="mt-4 text-lg text-slate-600">I focus on delivering measurable outcomes. This section provides a snapshot of the key results and growth I've driven in my roles, from boosting user acquisition to significantly increasing engagement and ROI.</p>
                </div>
                <div class="mt-16 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 text-center">
                    <div class="bg-white p-6 rounded-xl shadow-md">
                        <div id="counter1" class="text-4xl font-extrabold text-violet-600" data-target="1000000">0</div>
                        <p class="mt-2 text-base font-medium text-slate-500">App Installs Generated</p>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-md">
                        <div id="counter2" class="text-4xl font-extrabold text-violet-600" data-target="60000">0</div>
                        <p class="mt-2 text-base font-medium text-slate-500">Active Community Followers</p>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-md">
                        <div id="counter3" class="text-4xl font-extrabold text-violet-600" data-target="350">0</div>
                        <p class="mt-2 text-base font-medium text-slate-500">Million (₦) in New Business</p>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-md">
                        <div id="counter4" class="text-4xl font-extrabold text-violet-600" data-target="45000">0</div>
                        <p class="mt-2 text-base font-medium text-slate-500">Organic Instagram Followers</p>
                    </div>
                </div>
                <div class="mt-16 bg-white p-6 sm:p-8 rounded-xl shadow-md">
                     <h3 class="text-xl font-bold text-center text-slate-800">Key Performance Indicator Growth</h3>
                     <p class="text-center text-slate-500 mt-2 mb-6">Visual comparison of engagement and ROI increases achieved through strategic initiatives.</p>
                    <div class="chart-container">
                        <canvas id="achievementsChart"></canvas>
                    </div>
                </div>
            </div>
        </section>

        <section id="skills" class="py-20 sm:py-24 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center">
                    <h2 class="text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">Core Competencies</h2>
                    <p class="mt-4 text-lg text-slate-600">My skill set spans across content, strategy, and community management, enabling me to build and execute comprehensive communication plans. Here are the key areas of my expertise.</p>
                </div>
                <div class="mt-16 space-y-12">
                    <div>
                        <h3 class="text-xl font-semibold text-slate-800 mb-4">Content Creation & Management</h3>
                        <div class="flex flex-wrap gap-3">
                            <span class="skill-tag">Copywriting</span><span class="skill-tag">Article Writing</span><span class="skill-tag">Newsletter Curation</span><span class="skill-tag">Social Media Content</span><span class="skill-tag">Press Releases</span><span class="skill-tag">Scripting</span>
                        </div>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold text-slate-800 mb-4">Marketing & Communications Strategy</h3>
                        <div class="flex flex-wrap gap-3">
                            <span class="skill-tag">Campaign Planning</span><span class="skill-tag">Brand Management</span><span class="skill-tag">Public Relations</span><span class="skill-tag">Influencer Marketing</span><span class="skill-tag">Google & Social Ads</span>
                        </div>
                    </div>
                    <div>
                        <h3 class="text-xl font-semibold text-slate-800 mb-4">Community & Engagement</h3>
                        <div class="flex flex-wrap gap-3">
                             <span class="skill-tag">Community Building</span><span class="skill-tag">Customer Engagement</span><span class="skill-tag">User Persona Crafting</span><span class="skill-tag">Feedback Analysis</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="experience" class="py-20 sm:py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center">
                    <h2 class="text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">Career Journey</h2>
                    <p class="mt-4 text-lg text-slate-600">This interactive timeline outlines my professional path and key responsibilities in each role. Click on any position to see the details of my contributions and the skills I applied.</p>
                </div>
                <div class="mt-16 max-w-3xl mx-auto">
                    <div id="timeline-container" class="relative">
                        <div class="timeline-line"></div>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="portfolio" class="py-20 sm:py-24 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center">
                    <h2 class="text-3xl font-bold tracking-tight text-slate-900 sm:text-4xl">My Writing Portfolio</h2>
                     <p class="mt-4 text-lg text-slate-600">Here is a selection of my work, demonstrating my ability to adapt my writing style for different goals and audiences, from corporate social responsibility pieces to user-focused promotional content and personal narratives. Click a tab to explore each sample.</p>
                </div>
                <div class="mt-16 max-w-4xl mx-auto">
                    <div class="border-b border-slate-200">
                        <nav id="portfolio-tabs" class="-mb-px flex space-x-6" aria-label="Tabs">
                        </nav>
                    </div>
                    <div id="portfolio-content" class="mt-8">
                    </div>
                </div>
            </div>
        </section>
        
        <footer id="contact" class="bg-slate-800 text-white">
            <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8 text-center">
                <h2 class="text-3xl font-bold">Let's Connect</h2>
                <p class="mt-4 text-lg text-slate-300">I'm currently available for new opportunities. If you're looking for a passionate and results-driven content professional, I'd love to hear from you.</p>
                <div class="mt-8 flex justify-center items-center space-x-6">
                     <a href="mailto:biwomandeshi@gmail.com" class="text-violet-300 hover:text-white text-lg">biwomandeshi@gmail.com</a>
                     <span class="text-slate-500">|</span>
                     <span class="text-lg">+234 813 764 8403</span>
                </div>
            </div>
        </footer>

    </main>

    <script>
        const experienceData = [
            {
                role: "Content Writer",
                company: "Rova (FCMB UK)",
                dates: "08/2022 - Ongoing",
                details: [
                    "Create communication and marketing strategies for new products, launches, and events.",
                    "Plan and manage the design, content, and production of all marketing materials.",
                    "Develop strategies to build customer loyalty, brand awareness, and satisfaction.",
                    "Manage and grow all social media accounts including Facebook, Instagram, and TikTok.",
                    "Place and optimize ads on Google and across social media platforms.",
                ]
            },
            {
                role: "Community & Communications Manager",
                company: "Assets MFB (Monie Tree)",
                dates: "04/2022 - 08/2022",
                details: [
                    "Set, planned, and implemented social media and communication campaigns.",
                    "Provided engaging text, image, and video content for all social media accounts.",
                    "Created press releases for product and feature launches.",
                    "Built relationships with customers, industry professionals, and journalists.",
                    "Managed all influencer marketing relationships for the brand.",
                ]
            },
            {
                role: "Community/Social Media Manager",
                company: "PalmPay Limited",
                dates: "2019 - 2022",
                details: [
                    "Increased engagement KPIs in a 500K member Facebook group by 120% in 3 months.",
                    "Conducted user interviews to craft personas, boosting social ad ROI by 55%.",
                    "Generated over 1 million app installs via promotions and social media campaigns.",
                    "Grew organic Instagram followers to 45k through engaging content.",
                    "Wrote and prepared publishable articles and newsletters for the brand.",
                ]
            },
            {
                role: "TV Presenter/Content Manager",
                company: "Greywold Empire",
                dates: "2018 - 2019",
                details: [
                    "Ideated and scripted shows, and served as the main presenter.",
                    "Curated engaging topics for shows, including popular vox pop segments.",
                    "Created a wide range of content for various shows at the station.",
                    "Held the position of Director of Programs and News.",
                ]
            }
        ];

        const portfolioData = [
            {
                title: "CSR & Community",
                id: "csr",
                objective: "This piece highlights PalmPay's corporate social responsibility initiative during the COVID-19 pandemic, showcasing a key partnership to build brand trust and a positive public image.",
                excerpt: `The year 2020 was a tough one, the world was shut down because of the effect and spread of the Covid-19 pandemic... To fight and lessen the effect of the Coronavirus pandemic, the world had to come together to show solidarity and support to the vulnerable communities... PalmPay partnered with the Lagos Food Bank Initiative, an NGO based in Lagos Nigeria to support their Covid-19 Emergency Food Intervention programme. On 21st November, 2020, we visited Papa Ashafa, Orile-Agege community and staff members of PalmPay collaborated with the volunteers at Lagos food bank to distribute relief materials, food items and thousands of nose masks to women and children.`,
                ai_enhanced_description: null // To store AI generated content
            },
            {
                title: "Promotional 'How-To'",
                id: "promo",
                objective: "This article is a promotional piece for PalmPay, detailing how users can leverage the app's features and promotions to save money. The goal was to drive feature adoption and user engagement.",
                excerpt: `Isn't it ironic how even these days when so much is done digitally, the places we put our money for safekeeping overwhelm us with charges and excessive fees? PalmPay, a new pan-African fintech startup that boasts TECNO Mobile as an investor, is looking to change all that. Currently, PalmPay has a Super Easter promotion live where you can pay less and get more on your airtime purchases using discount coupons. We thought this would be a great time to introduce you to PalmPay and walk you through how you too can claim and save!`,
                ai_enhanced_description: null // To store AI generated content
            },
            {
                title: "Narrative & Lifestyle",
                id: "narrative",
                objective: "A personal, storytelling piece reflecting on Easter experiences. It showcases a narrative writing style while subtly integrating product benefits to demonstrate lifestyle relevance.",
                excerpt: `Easter season has come and gone but the memories I created during the 4-day-weekend were amazing. This Easter I initially planned to do a lot of things with my family... My nephews and nieces expected me to buy them gift items too as their 'big uncle' but to save cost I got them airtime and data using my PalmPay app instead of my bank app since I get rewarded cashback for every airtime purchase I did and I used the cashback to discount the next airtime I bought. For the ones I sent cash, the fund transfer was free instead of the regular N10 charge by banks.`,
                ai_enhanced_description: null // To store AI generated content
            }
        ];

        document.addEventListener('DOMContentLoaded', function() {
            
            function styleElements() {
                 document.querySelectorAll('.skill-tag').forEach(tag => {
                    tag.classList.add('bg-violet-100', 'text-violet-800', 'px-3', 'py-1', 'rounded-full', 'font-medium', 'text-sm');
                });
            }

            function setupCounters() {
                const counters = [
                    { id: 'counter1', target: 1000000 },
                    { id: 'counter2', target: 60000 },
                    { id: 'counter3', target: 350 },
                    { id: 'counter4', target: 45000 }
                ];

                const observer = new IntersectionObserver((entries) => {
                    entries.forEach(entry => {
                        if (entry.isIntersecting) {
                            const counterElement = entry.target;
                            const target = parseInt(counterElement.dataset.target);
                            animateCounter(counterElement, target);
                            observer.unobserve(counterElement);
                        }
                    });
                }, { threshold: 0.5 });

                counters.forEach(counter => {
                    const el = document.getElementById(counter.id);
                    if (el) observer.observe(el);
                });
            }

            function animateCounter(element, target) {
                let current = 0;
                const duration = 2000;
                const stepTime = Math.abs(Math.floor(duration / target));
                const timer = setInterval(() => {
                    current += Math.ceil(target / (duration / 16));
                    if (current >= target) {
                        current = target;
                        clearInterval(timer);
                    }
                    element.innerText = current.toLocaleString();
                }, 16);
            }

            function setupAchievementsChart() {
                const ctx = document.getElementById('achievementsChart')?.getContext('2d');
                if (!ctx) return;
                
                const observer = new IntersectionObserver((entries) => {
                    if (entries[0].isIntersecting) {
                        new Chart(ctx, {
                            type: 'bar',
                            data: {
                                labels: ['Facebook Group Engagement', 'Social Ad ROI', 'Pilot Campaign Lift'],
                                datasets: [{
                                    label: '% Increase',
                                    data: [120, 55, 100],
                                    backgroundColor: [
                                        'rgba(139, 92, 246, 0.6)',
                                        'rgba(99, 102, 241, 0.6)',
                                        'rgba(167, 139, 250, 0.6)',
                                    ],
                                    borderColor: [
                                        'rgba(139, 92, 246, 1)',
                                        'rgba(99, 102, 241, 1)',
                                        'rgba(167, 139, 250, 1)',
                                    ],
                                    borderWidth: 1
                                }]
                            },
                            options: {
                                responsive: true,
                                maintainAspectRatio: false,
                                scales: {
                                    y: {
                                        beginAtZero: true,
                                        ticks: {
                                            callback: function(value) {
                                                return value + '%'
                                            }
                                        }
                                    }
                                },
                                plugins: {
                                    legend: {
                                        display: false
                                    },
                                    tooltip: {
                                        callbacks: {
                                            label: function(context) {
                                                return `${context.dataset.label}: ${context.parsed.y}%`;
                                            }
                                        }
                                    }
                                }
                            }
                        });
                        observer.unobserve(ctx.canvas);
                    }
                }, { threshold: 0.5 });
                observer.observe(ctx.canvas);
            }

            function setupTimeline() {
                const container = document.getElementById('timeline-container');
                if (!container) return;

                experienceData.forEach((item, index) => {
                    const div = document.createElement('div');
                    div.className = 'relative pl-8 mb-8 timeline-item';
                    div.innerHTML = `
                        <div class="cursor-pointer">
                            <h4 class="text-lg font-bold text-slate-800">${item.role}</h4>
                            <p class="text-violet-600 font-semibold">${item.company}</p>
                            <p class="text-sm text-slate-500">${item.dates}</p>
                        </div>
                        <div class="timeline-details hidden mt-4 pl-4 border-l-2 border-slate-200">
                            <ul class="list-disc list-inside space-y-2 text-slate-600">
                                ${item.details.map(d => `<li>${d}</li>`).join('')}
                            </ul>
                        </div>
                    `;
                    container.appendChild(div);
                });
                
                container.addEventListener('click', (e) => {
                    const header = e.target.closest('.cursor-pointer');
                    if (header) {
                        const details = header.nextElementSibling;
                        const wasOpen = !details.classList.contains('hidden');

                        container.querySelectorAll('.timeline-details').forEach(d => d.classList.add('hidden'));
                        
                        if (!wasOpen) {
                            details.classList.remove('hidden');
                        }
                    }
                });
            }

            async function generateAIEnhancedDescription(item, contentBlockId) {
                const contentBlock = document.getElementById(contentBlockId);
                if (!contentBlock) return;

                const originalExcerpt = item.excerpt;
                const loadingText = 'Generating enhanced description...';
                contentBlock.innerHTML = `
                    <h3 class="text-xl font-bold text-slate-800">${item.title}</h3>
                    <p class="mt-2 text-slate-500 italic">${item.objective}</p>
                    <blockquote class="mt-6 border-l-4 border-violet-200 pl-4 text-slate-600">
                        <p class="text-lg animate-pulse">${loadingText}</p>
                    </blockquote>
                    <button class="mt-4 bg-gray-200 text-gray-700 py-2 px-4 rounded-full text-sm hover:bg-gray-300 transition duration-300" onclick="restoreOriginalDescription('${item.id}', '${contentBlockId}')">Restore Original</button>
                    <p class="mt-2 text-sm text-slate-400">Powered by Gemini API</p>
                `;

                if (item.ai_enhanced_description) {
                    contentBlock.innerHTML = `
                        <h3 class="text-xl font-bold text-slate-800">${item.title}</h3>
                        <p class="mt-2 text-slate-500 italic">${item.objective}</p>
                        <blockquote class="mt-6 border-l-4 border-violet-200 pl-4 text-slate-600">
                            "${item.ai_enhanced_description}"
                        </blockquote>
                        <button class="mt-4 bg-gray-200 text-gray-700 py-2 px-4 rounded-full text-sm hover:bg-gray-300 transition duration-300" onclick="restoreOriginalDescription('${item.id}', '${contentBlockId}')">Restore Original</button>
                        <p class="mt-2 text-sm text-slate-400">Powered by Gemini API</p>
                    `;
                    return;
                }

                try {
                    const prompt = `Expand on the following content writing excerpt, highlighting its purpose, target audience, and potential impact on a marketing campaign. Make it sound professional and engaging for a portfolio: '${originalExcerpt}'`;
                    let chatHistory = [];
                    chatHistory.push({ role: "user", parts: [{ text: prompt }] });
                    const payload = { contents: chatHistory };
                    const apiKey = ""; 
                    const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${apiKey}`;
                    const response = await fetch(apiUrl, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify(payload)
                    });
                    const result = await response.json();

                    if (result.candidates && result.candidates.length > 0 &&
                        result.candidates[0].content && result.candidates[0].content.parts &&
                        result.candidates[0].content.parts.length > 0) {
                        const text = result.candidates[0].content.parts[0].text;
                        item.ai_enhanced_description = text; // Store the generated content
                        contentBlock.innerHTML = `
                            <h3 class="text-xl font-bold text-slate-800">${item.title}</h3>
                            <p class="mt-2 text-slate-500 italic">${item.objective}</p>
                            <blockquote class="mt-6 border-l-4 border-violet-200 pl-4 text-slate-600">
                                "${item.ai_enhanced_description}"
                            </blockquote>
                            <button class="mt-4 bg-gray-200 text-gray-700 py-2 px-4 rounded-full text-sm hover:bg-gray-300 transition duration-300" onclick="restoreOriginalDescription('${item.id}', '${contentBlockId}')">Restore Original</button>
                            <p class="mt-2 text-sm text-slate-400">✨ AI-Enhanced Description via Gemini API ✨</p>
                        `;
                    } else {
                        console.error("Gemini API response structure unexpected:", result);
                        contentBlock.innerHTML = `
                            <h3 class="text-xl font-bold text-slate-800">${item.title}</h3>
                            <p class="mt-2 text-slate-500 italic">${item.objective}</p>
                            <blockquote class="mt-6 border-l-4 border-violet-200 pl-4 text-slate-600">
                                "${originalExcerpt}"
                            </blockquote>
                            <p class="mt-2 text-red-500 text-sm">Error generating enhanced description. Please try again.</p>
                            <button class="mt-4 bg-violet-600 text-white py-2 px-4 rounded-full text-sm hover:bg-violet-700 transition duration-300" onclick="generateAIEnhancedDescription(portfolioData.find(p => p.id === '${item.id}'), '${contentBlockId}')">Retry ✨ AI-Enhanced Description ✨</button>
                        `;
                    }
                } catch (error) {
                    console.error("Error calling Gemini API:", error);
                    contentBlock.innerHTML = `
                        <h3 class="text-xl font-bold text-slate-800">${item.title}</h3>
                        <p class="mt-2 text-slate-500 italic">${item.objective}</p>
                        <blockquote class="mt-6 border-l-4 border-violet-200 pl-4 text-slate-600">
                            "${originalExcerpt}"
                        </blockquote>
                        <p class="mt-2 text-red-500 text-sm">Network error or API issue. Please try again.</p>
                        <button class="mt-4 bg-violet-600 text-white py-2 px-4 rounded-full text-sm hover:bg-violet-700 transition duration-300" onclick="generateAIEnhancedDescription(portfolioData.find(p => p.id === '${item.id}'), '${contentBlockId}')">Retry ✨ AI-Enhanced Description ✨</button>
                    `;
                }
            }

            window.restoreOriginalDescription = function(itemId, contentBlockId) {
                const item = portfolioData.find(p => p.id === itemId);
                const contentBlock = document.getElementById(contentBlockId);
                 if (item && contentBlock) {
                     contentBlock.innerHTML = `
                        <h3 class="text-xl font-bold text-slate-800">${item.title}</h3>
                        <p class="mt-2 text-slate-500 italic">${item.objective}</p>
                        <blockquote class="mt-6 border-l-4 border-violet-200 pl-4 text-slate-600">
                            "${item.excerpt}"
                        </blockquote>
                        <button class="mt-4 bg-violet-600 text-white py-2 px-4 rounded-full text-sm hover:bg-violet-700 transition duration-300" onclick="generateAIEnhancedDescription(portfolioData.find(p => p.id === '${item.id}'), '${contentBlockId}')">✨ AI-Enhanced Description ✨</button>
                    `;
                }
            };


            function setupPortfolio() {
                const tabsContainer = document.getElementById('portfolio-tabs');
                const contentContainer = document.getElementById('portfolio-content');
                if (!tabsContainer || !contentContainer) return;

                portfolioData.forEach((item, index) => {
                    const tab = document.createElement('a');
                    tab.href = `#`;
                    tab.dataset.tab = item.id;
                    tab.className = `whitespace-nowrap py-4 px-1 border-b-2 font-medium text-sm transition-colors duration-300 ${index === 0 ? 'border-violet-500 text-violet-600' : 'border-transparent text-slate-500 hover:border-slate-300 hover:text-slate-700'}`;
                    tab.textContent = item.title;
                    tabsContainer.appendChild(tab);
                });

                function updateContent(tabId) {
                    const item = portfolioData.find(p => p.id === tabId);
                    if (item) {
                        contentContainer.innerHTML = `
                            <h3 class="text-xl font-bold text-slate-800">${item.title}</h3>
                            <p class="mt-2 text-slate-500 italic">${item.objective}</p>
                            <blockquote class="mt-6 border-l-4 border-violet-200 pl-4 text-slate-600" id="excerpt-${item.id}">
                                "${item.excerpt}"
                            </blockquote>
                            <button class="mt-4 bg-violet-600 text-white py-2 px-4 rounded-full text-sm hover:bg-violet-700 transition duration-300" onclick="generateAIEnhancedDescription(portfolioData.find(p => p.id === '${item.id}'), 'excerpt-${item.id}')">✨ AI-Enhanced Description ✨</button>
                        `;
                    }
                }

                tabsContainer.addEventListener('click', (e) => {
                    e.preventDefault();
                    if (e.target.tagName === 'A') {
                        const tabId = e.target.dataset.tab;
                        tabsContainer.querySelectorAll('a').forEach(tab => {
                            if (tab.dataset.tab === tabId) {
                                tab.classList.remove('border-transparent', 'text-slate-500', 'hover:border-slate-300', 'hover:text-slate-700');
                                tab.classList.add('border-violet-500', 'text-violet-600');
                            } else {
                                tab.classList.remove('border-violet-500', 'text-violet-600');
                                tab.classList.add('border-transparent', 'text-slate-500', 'hover:border-slate-300', 'hover:text-slate-700');
                            }
                        });
                        updateContent(tabId);
                    }
                });
                
                updateContent(portfolioData[0].id);
            }

            styleElements();
            setupCounters();
            setupAchievementsChart();
            setupTimeline();
            setupPortfolio();
        });
    </script>
</body>
</html>
