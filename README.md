# Index1.html
<!DOCTYPE html>
<html lang="en" class="h-full">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AntiLala | Expose & Reform Toxic Workplaces</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#fff1f2',
                            100: '#ffe4e6',
                            500: '#f43f5e',
                            600: '#e11d48',
                            700: '#be123c',
                            900: '#881337',
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body { font-family: 'Inter', sans-serif; }
        .custom-scrollbar::-webkit-scrollbar { width: 6px; }
        .custom-scrollbar::-webkit-scrollbar-track { background: #f1f1f1; }
        .custom-scrollbar::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 3px; }
    </style>
</head>
<body class="bg-slate-900 text-slate-100 h-full flex flex-col selection:bg-brand-500 selection:text-white">

    <!-- Top Navigation Bar -->
    <header class="bg-slate-800 border-b border-slate-700 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <!-- Logo & Brand -->
            <div class="flex items-center space-x-3 cursor-pointer" onclick="switchTab('feed')">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-brand-600 to-amber-500 flex items-center justify-center shadow-lg shadow-brand-500/30">
                    <i class="fa-solid fa-triangle-exclamation text-white text-lg"></i>
                </div>
                <div>
                    <span class="text-xl font-bold tracking-tight text-white">Anti<span class="text-brand-500">Lala</span></span>
                    <span class="hidden sm:inline-block ml-2 text-xs px-2 py-0.5 rounded-full bg-slate-700 text-slate-300 font-medium border border-slate-600">Corporate Truth</span>
                </div>
            </div>

            <!-- Search Bar -->
            <div class="hidden md:flex flex-1 max-w-md mx-8">
                <div class="relative w-full">
                    <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none">
                        <i class="fa-solid fa-magnifying-glass text-slate-400"></i>
                    </div>
                    <input type="text" id="globalSearchInput" oninput="handleGlobalSearch(this.value)" placeholder="Search companies, red flags, or horror stories..." class="w-full pl-10 pr-4 py-2 bg-slate-900 border border-slate-700 rounded-lg text-sm text-slate-200 placeholder-slate-400 focus:outline-none focus:border-brand-500 focus:ring-1 focus:ring-brand-500 transition">
                </div>
            </div>

            <!-- Navigation Actions & Profile -->
            <div class="flex items-center space-x-2 sm:space-x-4">
                <button onclick="switchTab('feed')" id="navFeedBtn" class="flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition bg-slate-700 text-white">
                    <i class="fa-solid fa-newspaper"></i>
                    <span class="hidden sm:inline">Feed</span>
                </button>
                <button onclick="switchTab('directory')" id="navDirectoryBtn" class="flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition text-slate-300 hover:bg-slate-700 hover:text-white">
                    <i class="fa-solid fa-building-shield"></i>
                    <span class="hidden sm:inline">Directory</span>
                </button>
                <button onclick="openReportModal()" class="flex items-center space-x-2 px-4 py-2 bg-brand-600 hover:bg-brand-700 text-white rounded-lg text-sm font-semibold shadow-md shadow-brand-600/30 transition transform active:scale-95">
                    <i class="fa-solid fa-bullhorn"></i>
                    <span>Expose Company</span>
                </button>
                <div class="w-8 h-8 rounded-full bg-slate-700 border border-slate-600 flex items-center justify-center text-slate-300 font-bold text-xs" title="Anonymous Whistleblower">
                    🕵️‍♂️
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content Container -->
    <main class="flex-1 overflow-y-auto custom-scrollbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6">

            <!-- TAB 1: FEED VIEW -->
            <div id="tabFeed" class="space-y-6">
                <!-- Hero Banner / Notice -->
                <div class="bg-gradient-to-r from-slate-800 via-slate-800 to-slate-900 border border-slate-700/80 rounded-2xl p-6 sm:p-8 shadow-xl relative overflow-hidden">
                    <div class="absolute -right-10 -bottom-10 w-64 h-64 bg-brand-600/10 rounded-full blur-3xl pointer-events-none"></div>
                    <div class="max-w-2xl">
                        <span class="text-xs uppercase tracking-wider font-semibold text-brand-400 bg-brand-950/60 px-3 py-1 rounded-full border border-brand-800/50">Anonymous & Secure Whistleblowing</span>
                        <h1 class="text-2xl sm:text-3xl font-bold text-white mt-3">Exposing Feudal Workplaces & "Lala" Bosses</h1>
                        <p class="text-slate-400 mt-2 text-sm sm:text-base">Tired of "We are a family here" while working 70 hours without overtime? Expose autocratic management, delayed salaries, and micro-management safely and anonymously.</p>
                        <div class="mt-5 flex flex-wrap gap-3">
                            <button onclick="openReportModal()" class="px-4 py-2 bg-brand-600 hover:bg-brand-700 text-white font-medium rounded-lg text-sm transition shadow">
                                <i class="fa-solid fa-plus-circle mr-2"></i> Submit a Review
                            </button>
                            <button onclick="switchTab('directory')" class="px-4 py-2 bg-slate-700 hover:bg-slate-600 text-slate-200 font-medium rounded-lg text-sm transition">
                                <i class="fa-solid fa-chart-bar mr-2"></i> View Lala Directory
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Feed Filters & Quick Post Trigger -->
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
                    <!-- Left Sidebar: Trending Red Flags -->
                    <div class="space-y-6 hidden lg:block">
                        <div class="bg-slate-800 border border-slate-700 rounded-xl p-5 shadow-sm">
                            <h3 class="text-sm font-semibold text-slate-200 uppercase tracking-wider flex items-center">
                                <i class="fa-solid fa-fire text-brand-500 mr-2"></i> Trending Red Flags
                            </h3>
                            <div class="mt-4 flex flex-wrap gap-2" id="trendingTagsContainer">
                                <!-- Populated dynamically -->
                            </div>
                        </div>

                        <div class="bg-slate-800 border border-slate-700 rounded-xl p-5 shadow-sm">
                            <h3 class="text-sm font-semibold text-slate-200 uppercase tracking-wider flex items-center">
                                <i class="fa-solid fa-book-open text-amber-500 mr-2"></i> What is a "Lala" Company?
                            </h3>
                            <ul class="mt-3 space-y-2 text-xs text-slate-400 leading-relaxed">
                                <li class="flex items-start"><i class="fa-solid fa-circle-xmark text-brand-500 mt-0.5 mr-2"></i> Owner's family dictates policy over HR and logic.</li>
                                <li class="flex items-start"><i class="fa-solid fa-circle-xmark text-brand-500 mt-0.5 mr-2"></i> Salaries delayed regularly with emotional guilt-trips.</li>
                                <li class="flex items-start"><i class="fa-solid fa-circle-xmark text-brand-500 mt-0.5 mr-2"></i> Zero compliance, cash components, no appointment letters.</li>
                                <li class="flex items-start"><i class="fa-solid fa-circle-xmark text-brand-500 mt-0.5 mr-2"></i> Surveillance, attendance tracking down to the minute.</li>
                            </ul>
                        </div>
                    </div>

                    <!-- Center Main Feed Column -->
                    <div class="lg:col-span-2 space-y-4">
                        <!-- Create Quick Post Box -->
                        <div class="bg-slate-800 border border-slate-700 rounded-xl p-4 shadow-sm">
                            <div class="flex items-center space-x-3">
                                <div class="w-10 h-10 rounded-full bg-slate-700 flex items-center justify-center text-slate-300 font-bold">
                                    🕵️‍♂️
                                </div>
                                <button onclick="openReportModal()" class="flex-1 text-left px-4 py-3 bg-slate-900 border border-slate-700 rounded-xl text-slate-400 hover:bg-slate-950 transition text-sm">
                                    Share an anonymous horror story or report a company...
                                </button>
                            </div>
                            <div class="mt-3 pt-3 border-t border-slate-700 flex items-center justify-between text-xs text-slate-400 px-2">
                                <span class="flex items-center"><i class="fa-solid fa-user-secret text-brand-500 mr-1.5"></i> 100% Anonymous & Encrypted</span>
                                <button onclick="openReportModal()" class="text-brand-400 hover:underline font-medium">Post Review <i class="fa-solid fa-arrow-right ml-1"></i></button>
                            </div>
                        </div>

                        <!-- Filter Bar -->
                        <div class="flex items-center justify-between bg-slate-800/60 border border-slate-700/60 px-4 py-2.5 rounded-xl text-sm">
                            <span class="text-slate-400 font-medium">Sort Feed By:</span>
                            <div class="flex items-center space-x-2">
                                <button onclick="setFeedFilter('recent')" id="filterRecent" class="px-3 py-1.5 rounded-lg bg-brand-600 text-white font-medium text-xs transition">Most Recent</button>
                                <button onclick="setFeedFilter('highestLala')" id="filterHighest" class="px-3 py-1.5 rounded-lg bg-slate-700 text-slate-300 font-medium text-xs hover:bg-slate-600 transition">Highest Lala Score</button>
                            </div>
                        </div>

                        <!-- Posts Stream -->
                        <div id="postsFeedContainer" class="space-y-4">
                            <!-- Populated dynamically -->
                        </div>
                    </div>
                </div>
            </div>

            <!-- TAB 2: COMPANY DIRECTORY & LEADERBOARD -->
            <div id="tabDirectory" class="hidden space-y-6">
                <div class="flex flex-col md:flex-row md:items-center justify-between gap-4">
                    <div>
                        <h1 class="text-2xl font-bold text-white">Company Directory & Lala Index</h1>
                        <p class="text-slate-400 text-sm mt-1">Explore verified reports, toxicity scores, and red flags for companies.</p>
                    </div>
                    <div class="flex items-center space-x-3">
                        <div class="relative">
                            <input type="text" id="directorySearchInput" oninput="filterDirectory(this.value)" placeholder="Filter companies..." class="pl-9 pr-4 py-2 bg-slate-800 border border-slate-700 rounded-lg text-sm text-slate-200 focus:outline-none focus:border-brand-500">
                            <i class="fa-solid fa-search absolute left-3 top-3 text-slate-400 text-sm"></i>
                        </div>
                    </div>
                </div>

                <!-- Directory Grid / Table -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6" id="directoryGridContainer">
                    <!-- Populated dynamically -->
                </div>
            </div>

        </div>
    </main>

    <!-- Report a Company Modal -->
    <div id="reportModal" class="fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-sm hidden items-center justify-center p-4">
        <div class="bg-slate-800 border border-slate-700 rounded-2xl w-full max-w-2xl max-h-[90vh] overflow-y-auto shadow-2xl">
            <div class="p-6 border-b border-slate-700 flex items-center justify-between sticky top-0 bg-slate-800 z-10">
                <div class="flex items-center space-x-3">
                    <div class="w-10 h-10 rounded-xl bg-brand-600/20 text-brand-500 flex items-center justify-center">
                        <i class="fa-solid fa-triangle-exclamation text-lg"></i>
                    </div>
                    <div>
                        <h2 class="text-lg font-bold text-white">Expose a "Lala" Company</h2>
                        <p class="text-xs text-slate-400">Your identity remains completely secure and anonymous.</p>
                    </div>
                </div>
                <button onclick="closeReportModal()" class="w-8 h-8 rounded-full bg-slate-700 text-slate-300 hover:bg-slate-600 flex items-center justify-center transition">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <form id="reportForm" onsubmit="handleReportSubmit(event)" class="p-6 space-y-5">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1">Company Name *</label>
                        <input type="text" id="inputCompanyName" required placeholder="e.g. Sharma Textiles & Tech Solutions" class="w-full px-3 py-2.5 bg-slate-900 border border-slate-700 rounded-lg text-sm text-slate-200 placeholder-slate-500 focus:outline-none focus:border-brand-500">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1">Industry / Sector *</label>
                        <select id="inputIndustry" required class="w-full px-3 py-2.5 bg-slate-900 border border-slate-700 rounded-lg text-sm text-slate-200 focus:outline-none focus:border-brand-500">
                            <option value="IT Services & Agency">IT Services & Agency</option>
                            <option value="Family Manufacturing / Textile">Family Manufacturing / Textile</option>
                            <option value="E-Commerce & Retail">E-Commerce & Retail</option>
                            <option value="Real Estate & Construction">Real Estate & Construction</option>
                            <option value="Finance & Accounting">Finance & Accounting</option>
                            <option value="Startup / Consultancy">Startup / Consultancy</option>
                        </select>
                    </div>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1">Location / City *</label>
                        <input type="text" id="inputLocation" required placeholder="e.g. Noida, Sector 63 / Surat" class="w-full px-3 py-2.5 bg-slate-900 border border-slate-700 rounded-lg text-sm text-slate-200 placeholder-slate-500 focus:outline-none focus:border-brand-500">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1">Lala Index (Toxicity Score: 1 to 10) *</label>
                        <div class="flex items-center space-x-3 pt-1">
                            <input type="range" id="inputLalaScore" min="1" max="10" value="8" oninput="document.getElementById('scoreDisplay').innerText = this.value + '/10'" class="w-full accent-brand-500 bg-slate-900">
                            <span id="scoreDisplay" class="px-3 py-1 bg-brand-950 border border-brand-800 text-brand-400 font-bold rounded-lg text-sm">8/10</span>
                        </div>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-2">Select Applicable Red Flags *</label>
                    <div class="grid grid-cols-2 sm:grid-cols-3 gap-2" id="modalRedFlagsContainer">
                        <label class="flex items-center space-x-2 p-2.5 bg-slate-900 border border-slate-700 rounded-lg cursor-pointer hover:border-slate-600 text-xs text-slate-300">
                            <input type="checkbox" name="redFlags" value="#DelayedSalaries" class="accent-brand-500 rounded">
                            <span>#DelayedSalaries</span>
                        </label>
                        <label class="flex items-center space-x-2 p-2.5 bg-slate-900 border border-slate-700 rounded-lg cursor-pointer hover:border-slate-600 text-xs text-slate-300">
                            <input type="checkbox" name="redFlags" value="#MicromanagerBoss" class="accent-brand-500 rounded">
                            <span>#MicromanagerBoss</span>
                        </label>
                        <label class="flex items-center space-x-2 p-2.5 bg-slate-900 border border-slate-700 rounded-lg cursor-pointer hover:border-slate-600 text-xs text-slate-300">
                            <input type="checkbox" name="redFlags" value="#FamilyInterference" class="accent-brand-500 rounded">
                            <span>#FamilyInterference</span>
                        </label>
                        <label class="flex items-center space-x-2 p-2.5 bg-slate-900 border border-slate-700 rounded-lg cursor-pointer hover:border-slate-600 text-xs text-slate-300">
                            <input type="checkbox" name="redFlags" value="#NoOvertimePay" class="accent-brand-500 rounded">
                            <span>#NoOvertimePay</span>
                        </label>
                        <label class="flex items-center space-x-2 p-2.5 bg-slate-900 border border-slate-700 rounded-lg cursor-pointer hover:border-slate-600 text-xs text-slate-300">
                            <input type="checkbox" name="redFlags" value="#FakeFamilyCulture" class="accent-brand-500 rounded">
                            <span>#FakeFamilyCulture</span>
                        </label>
                        <label class="flex items-center space-x-2 p-2.5 bg-slate-900 border border-slate-700 rounded-lg cursor-pointer hover:border-slate-600 text-xs text-slate-300">
                            <input type="checkbox" name="redFlags" value="#ZeroCompliance" class="accent-brand-500 rounded">
                            <span>#ZeroCompliance</span>
                        </label>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-semibold uppercase tracking-wider text-slate-300 mb-1">Detailed Review / Horror Story *</label>
                    <textarea id="inputReviewText" required rows="4" placeholder="Explain what makes this company a Lala company. E.g., The owner sits at every desk, watches CCTV feeds, and deducts salary if you leave at 7 PM..." class="w-full px-3 py-2.5 bg-slate-900 border border-slate-700 rounded-lg text-sm text-slate-200 placeholder-slate-500 focus:outline-none focus:border-brand-500"></textarea>
                </div>

                <div class="flex items-center justify-end space-x-3 pt-2">
                    <button type="button" onclick="closeReportModal()" class="px-4 py-2 bg-slate-700 hover:bg-slate-600 text-slate-300 font-medium rounded-lg text-sm transition">Cancel</button>
                    <button type="submit" class="px-5 py-2 bg-brand-600 hover:bg-brand-700 text-white font-semibold rounded-lg text-sm shadow transition">Publish Anonymously</button>
                </div>
            </form>
        </div>
    </div>

    <!-- JavaScript Application Logic -->
    <script>
        // Mock Database / State
        let state = {
            activeTab: 'feed',
            feedFilter: 'recent',
            searchQuery: '',
            directoryFilter: '',
            posts: [
                {
                    id: 1,
                    companyName: "Apex Textile & Trading Co.",
                    industry: "Family Manufacturing / Textile",
                    location: "Surat, Gujarat",
                    lalaScore: 9,
                    author: "Anonymous Ex-Developer",
                    timeAgo: "2 hours ago",
                    redFlags: ["#FamilyInterference", "#DelayedSalaries", "#MicromanagerBoss"],
                    content: "The owner's son joined fresh out of college and started ordering senior engineers around. Salaries are routinely delayed by 15 days with lectures on 'dedication to the family business'. If you log out at 6:30 PM, the HR manager calls you asking if there's a family emergency.",
                    likes: 42,
                    commentsCount: 8,
                    comments: [
                        { author: "Ex-HR Lead", text: "Can confirm! I was asked to deduct salary for taking 15 minutes lunch break." },
                        { author: "Anonymous", text: "Worst place ever. They still owe me full and final settlement." }
                    ]
                },
                {
                    id: 2,
                    companyName: "Vishwa Web Solutions Pvt Ltd",
                    industry: "IT Services & Agency",
                    location: "Noida, Sector 62",
                    lalaScore: 8,
                    author: "Anonymous Tech Lead",
                    timeAgo: "Yesterday",
                    redFlags: ["#NoOvertimePay", "#FakeFamilyCulture", "#ZeroCompliance"],
                    content: "Classic Lala agency setup. They advertise 'Flexible startup culture' during interviews, but reality is 12-hour mandatory shifts on Saturdays. No PF contributions made for 8 months. Cash components given in envelopes.",
                    likes: 67,
                    commentsCount: 12,
                    comments: [
                        { author: "Fullstack Dev", text: "They literally fired someone for refusing Sunday deployment!" }
                    ]
                },
                {
                    id: 3,
                    companyName: "Gupta & Sons Real Estate",
                    industry: "Real Estate & Construction",
                    location: "Gurugram, Sector 44",
                    lalaScore: 10,
                    author: "Anonymous Sales Manager",
                    timeAgo: "3 days ago",
                    redFlags: ["#MicromanagerBoss", "#DelayedSalaries", "#FamilyInterference"],
                    content: "The boss listens to sales calls live on speakerphone and interrupts negotiations directly. Commission promises made verbally are never paid out during appraisal time. Total toxic autocracy.",
                    likes: 89,
                    commentsCount: 15,
                    comments: [
                        { author: "Ex-Sales Exec", text: "The turnover rate here is 100% every 4 months." }
                    ]
                }
            ],
            companies: [
                { name: "Apex Textile & Trading Co.", industry: "Family Manufacturing / Textile", location: "Surat, Gujarat", lalaScore: 9, reportsCount: 14, redFlags: ["#FamilyInterference", "#DelayedSalaries", "#MicromanagerBoss"] },
                { name: "Vishwa Web Solutions Pvt Ltd", industry: "IT Services & Agency", location: "Noida, Sector 62", lalaScore: 8, reportsCount: 22, redFlags: ["#NoOvertimePay", "#FakeFamilyCulture", "#ZeroCompliance"] },
                { name: "Gupta & Sons Real Estate", industry: "Real Estate & Construction", location: "Gurugram, Sector 44", lalaScore: 10, reportsCount: 19, redFlags: ["#MicromanagerBoss", "#DelayedSalaries", "#FamilyInterference"] },
                { name: "Shree Ram Logistics & Cargo", industry: "Logistics & Transport", location: "Mumbai, Bhiwandi", lalaScore: 8.5, reportsCount: 9, redFlags: ["#ZeroCompliance", "#NoOvertimePay"] },
                { name: "Modern Retail Chain India", industry: "E-Commerce & Retail", location: "Delhi, Karol Bagh", lalaScore: 7.5, reportsCount: 11, redFlags: ["#FakeFamilyCulture", "#MicromanagerBoss"] }
            ]
        };

        // Initialize App on Load
        window.onload = function() {
            renderFeed();
            renderDirectory();
            renderTrendingTags();
        };

        // Tab Switching
        function switchTab(tab) {
            state.activeTab = tab;
            const feedBtn = document.getElementById('navFeedBtn');
            const dirBtn = document.getElementById('navDirectoryBtn');
            const feedTab = document.getElementById('tabFeed');
            const dirTab = document.getElementById('tabDirectory');

            if (tab === 'feed') {
                feedBtn.className = "flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition bg-slate-700 text-white";
                dirBtn.className = "flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition text-slate-300 hover:bg-slate-700 hover:text-white";
                feedTab.classList.remove('hidden');
                dirTab.classList.add('hidden');
            } else {
                dirBtn.className = "flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition bg-slate-700 text-white";
                feedBtn.className = "flex items-center space-x-2 px-3 py-2 rounded-lg text-sm font-medium transition text-slate-300 hover:bg-slate-700 hover:text-white";
                dirTab.classList.remove('hidden');
                feedTab.classList.add('hidden');
            }
        }

        // Modal Controls
        function openReportModal() {
            document.getElementById('reportModal').classList.remove('hidden');
            document.getElementById('reportModal').classList.add('flex');
        }

        function closeReportModal() {
            document.getElementById('reportModal').classList.add('hidden');
            document.getElementById('reportModal').classList.remove('flex');
            document.getElementById('reportForm').reset();
            document.getElementById('scoreDisplay').innerText = "8/10";
        }

        // Handle Report Submission
        function handleReportSubmit(e) {
            e.preventDefault();
            const companyName = document.getElementById('inputCompanyName').value.trim();
            const industry = document.getElementById('inputIndustry').value;
            const location = document.getElementById('inputLocation').value.trim();
            const lalaScore = parseFloat(document.getElementById('inputLalaScore').value);
            const reviewText = document.getElementById('inputReviewText').value.trim();

            const checkboxes = document.querySelectorAll('input[name="redFlags"]:checked');
            const redFlags = Array.from(checkboxes).map(cb => cb.value);
            if (redFlags.length === 0) redFlags.push('#MicromanagerBoss');

            // Create new post object
            const newPost = {
                id: Date.now(),
                companyName,
                industry,
                location,
                lalaScore,
                author: "Anonymous Whistleblower",
                timeAgo: "Just now",
                redFlags,
                content: reviewText,
                likes: 1,
                commentsCount: 0,
                comments: []
            };

            state.posts.unshift(newPost);

            // Update or add to companies directory
            let existingCompany = state.companies.find(c => c.name.toLowerCase() === companyName.toLowerCase());
            if (existingCompany) {
                existingCompany.reportsCount += 1;
                existingCompany.lalaScore = ((existingCompany.lalaScore + lalaScore) / 2).toFixed(1);
            } else {
                state.companies.unshift({
                    name: companyName,
                    industry,
                    location,
                    lalaScore,
                    reportsCount: 1,
                    redFlags
                });
            }

            closeReportModal();
            renderFeed();
            renderDirectory();
            renderTrendingTags();
        }

        // Like Post
        function likePost(id) {
            const post = state.posts.find(p => p.id === id);
            if (post) {
                post.likes += 1;
                renderFeed();
            }
        }

        // Add Comment
        function addComment(id) {
            const commentText = prompt("Write an anonymous comment or confirmation:");
            if (commentText && commentText.trim() !== "") {
                const post = state.posts.find(p => p.id === id);
                if (post) {
                    post.comments.push({ author: "Anonymous Colleague", text: commentText.trim() });
                    post.commentsCount += 1;
                    renderFeed();
                }
            }
        }

        // Feed Filter
        function setFeedFilter(filter) {
            state.feedFilter = filter;
            const btnRecent = document.getElementById('filterRecent');
            const btnHighest = document.getElementById('filterHighest');
            if (filter === 'recent') {
                btnRecent.className = "px-3 py-1.5 rounded-lg bg-brand-600 text-white font-medium text-xs transition";
                btnHighest.className = "px-3 py-1.5 rounded-lg bg-slate-700 text-slate-300 font-medium text-xs hover:bg-slate-600 transition";
            } else {
                btnHighest.className = "px-3 py-1.5 rounded-lg bg-brand-600 text-white font-medium text-xs transition";
                btnRecent.className = "px-3 py-1.5 rounded-lg bg-slate-700 text-slate-300 font-medium text-xs hover:bg-slate-600 transition";
            }
            renderFeed();
        }

        // Global Search
        function handleGlobalSearch(query) {
            state.searchQuery = query.toLowerCase();
            renderFeed();
        }

        function filterDirectory(query) {
            state.directoryFilter = query.toLowerCase();
            renderDirectory();
        }

        // Render Feed Posts
        function renderFeed() {
            const container = document.getElementById('postsFeedContainer');
            let filteredPosts = [...state.posts];

            if (state.searchQuery) {
                filteredPosts = filteredPosts.filter(p => 
                    p.companyName.toLowerCase().includes(state.searchQuery) ||
                    p.content.toLowerCase().includes(state.searchQuery) ||
                    p.location.toLowerCase().includes(state.searchQuery) ||
                    p.redFlags.some(rf => rf.toLowerCase().includes(state.searchQuery))
                );
            }

            if (state.feedFilter === 'highestLala') {
                filteredPosts.sort((a, b) => b.lalaScore - a.lalaScore);
            }

            if (filteredPosts.length === 0) {
                container.innerHTML = `
                    <div class="bg-slate-800 border border-slate-700 rounded-xl p-8 text-center text-slate-400">
                        <i class="fa-solid fa-face-grimace text-3xl mb-2 text-slate-500"></i>
                        <p>No matching horror stories or reviews found.</p>
                    </div>
                `;
                return;
            }

            container.innerHTML = filteredPosts.map(post => `
                <div class="bg-slate-800 border border-slate-700 rounded-xl p-5 shadow-sm space-y-4">
                    <!-- Post Header -->
                    <div class="flex items-start justify-between">
                        <div class="flex items-center space-x-3">
                            <div class="w-10 h-10 rounded-full bg-slate-700 border border-slate-600 flex items-center justify-center text-slate-300 font-bold">
                                🕵️‍♂️
                            </div>
                            <div>
                                <h3 class="text-sm font-semibold text-white flex items-center">
                                    ${post.author}
                                    <span class="ml-2 text-xs px-2 py-0.5 rounded bg-brand-950 text-brand-400 border border-brand-800">Verified Insider</span>
                                </h3>
                                <p class="text-xs text-slate-400">${post.location} • <span class="text-slate-300">${post.timeAgo}</span></p>
                            </div>
                        </div>
                        <div class="flex items-center space-x-2 bg-slate-900 border border-slate-700 px-3 py-1 rounded-lg">
                            <span class="text-xs text-slate-400 font-medium">Lala Index:</span>
                            <span class="text-sm font-bold text-brand-400">${post.lalaScore}/10</span>
                        </div>
                    </div>

                    <!-- Company Tag & Red Flags -->
                    <div class="space-y-2">
                        <div class="flex items-center justify-between">
                            <h4 class="text-base font-bold text-white flex items-center">
                                <i class="fa-solid fa-building text-slate-400 mr-2"></i> ${post.companyName}
                            </h4>
                            <span class="text-xs text-slate-400 bg-slate-900 px-2.5 py-1 rounded border border-slate-700">${post.industry}</span>
                        </div>
                        <div class="flex flex-wrap gap-1.5 pt-1">
                            ${post.redFlags.map(rf => `<span class="text-xs bg-brand-950/80 text-brand-300 border border-brand-800/60 px-2 py-0.5 rounded-md font-medium">${rf}</span>`).join('')}
                        </div>
                    </div>

                    <!-- Post Body / Content -->
                    <p class="text-sm text-slate-200 leading-relaxed bg-slate-900/50 p-3.5 rounded-lg border border-slate-700/50">
                        ${post.content}
                    </p>

                    <!-- Engagement Bar -->
                    <div class="flex items-center justify-between pt-2 border-t border-slate-700/60 text-xs text-slate-400">
                        <button onclick="likePost(${post.id})" class="flex items-center space-x-1.5 hover:text-brand-400 transition py-1 px-2 rounded hover:bg-slate-700/50">
                            <i class="fa-solid fa-heart text-brand-500"></i>
                            <span>${post.likes} Helpful</span>
                        </button>
                        <button onclick="addComment(${post.id})" class="flex items-center space-x-1.5 hover:text-slate-200 transition py-1 px-2 rounded hover:bg-slate-700/50">
                            <i class="fa-solid fa-comment text-slate-400"></i>
                            <span>${post.commentsCount} Comments</span>
                        </button>
                        <button onclick="navigator.clipboard.writeText(window.location.href); alert('Link copied to clipboard!');" class="flex items-center space-x-1.5 hover:text-slate-200 transition py-1 px-2 rounded hover:bg-slate-700/50">
                            <i class="fa-solid fa-share"></i>
                            <span>Share</span>
                        </button>
                    </div>

                    <!-- Comments Section -->
                    ${post.comments && post.comments.length > 0 ? `
                        <div class="mt-3 pt-3 border-t border-slate-700/40 space-y-2">
                            ${post.comments.map(c => `
                                <div class="bg-slate-900/80 p-2.5 rounded-lg text-xs space-y-1">
                                    <span class="font-semibold text-slate-300">${c.author}:</span>
                                    <p class="text-slate-300">${c.text}</p>
                                </div>
                            `).join('')}
                        </div>
                    ` : ''}
                </div>
            `).join('');
        }

        // Render Directory
        function renderDirectory() {
            const container = document.getElementById('directoryGridContainer');
            let filteredCompanies = [...state.companies];

            if (state.directoryFilter) {
                filteredCompanies = filteredCompanies.filter(c => 
                    c.name.toLowerCase().includes(state.directoryFilter) ||
                    c.industry.toLowerCase().includes(state.directoryFilter) ||
                    c.location.toLowerCase().includes(state.directoryFilter)
                );
            }

            if (filteredCompanies.length === 0) {
                container.innerHTML = `
                    <div class="col-span-full bg-slate-800 border border-slate-700 rounded-xl p-8 text-center text-slate-400">
                        <i class="fa-solid fa-building-circle-exclamation text-3xl mb-2 text-slate-500"></i>
                        <p>No companies found in directory matching filter.</p>
                    </div>
                `;
                return;
            }

            container.innerHTML = filteredCompanies.map(company => `
                <div class="bg-slate-800 border border-slate-700 rounded-xl p-5 shadow-sm space-y-4 flex flex-col justify-between">
                    <div class="space-y-3">
                        <div class="flex items-start justify-between">
                            <div>
                                <h3 class="text-base font-bold text-white">${company.name}</h3>
                                <p class="text-xs text-slate-400">${company.location}</p>
                            </div>
                            <div class="px-2.5 py-1 bg-brand-950 border border-brand-800 rounded-lg text-right">
                                <span class="block text-[10px] text-brand-400 uppercase font-semibold">Lala Index</span>
                                <span class="text-sm font-bold text-white">${company.lalaScore}/10</span>
                            </div>
                        </div>

                        <div class="text-xs text-slate-400 bg-slate-900 px-3 py-1.5 rounded-lg border border-slate-700 flex items-center justify-between">
                            <span>Industry:</span>
                            <span class="text-slate-200 font-medium">${company.industry}</span>
                        </div>

                        <div>
                            <span class="text-[11px] font-semibold uppercase text-slate-400 block mb-1.5">Top Red Flags:</span>
                            <div class="flex flex-wrap gap-1">
                                ${company.redFlags.map(rf => `<span class="text-xs bg-slate-900 text-brand-300 border border-slate-700 px-2 py-0.5 rounded">${rf}</span>`).join('')}
                            </div>
                        </div>
                    </div>

                    <div class="pt-4 border-t border-slate-700 flex items-center justify-between text-xs text-slate-400">
                        <span><strong class="text-white">${company.reportsCount}</strong> Reports Filed</span>
                        <button onclick="openReportModal()" class="text-brand-400 hover:underline font-medium">Add Report <i class="fa-solid fa-arrow-right ml-1"></i></button>
                    </div>
                </div>
            `).join('');
        }

        // Render Trending Tags
        function renderTrendingTags() {
            const container = document.getElementById('trendingTagsContainer');
            const tags = ["#DelayedSalaries", "#MicromanagerBoss", "#FamilyInterference", "#NoOvertimePay", "#FakeFamilyCulture", "#ZeroCompliance", "#CCTVSurveillance"];
            container.innerHTML = tags.map(tag => `
                <button onclick="handleGlobalSearch('${tag}')" class="text-xs bg-slate-900 hover:bg-slate-700 text-slate-300 border border-slate-700 px-3 py-1.5 rounded-lg transition font-medium">
                    ${tag}
                </button>
            `).join('');
        }
    </script>
</body>
</html>
