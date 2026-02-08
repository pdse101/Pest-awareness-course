root {
        --pds-blue: #0ea5e9; /* Sky 500 */
        --pds-dark: #0f172a; /* Slate 900 */
    }

    body { 
        font-family: 'Plus Jakarta Sans', sans-serif; 
        overscroll-behavior: none;
    }

    .slide { 
        display: none; 
        height: calc(100vh - 140px);
        overflow-y: auto;
        -webkit-overflow-scrolling: touch;
    }

    .slide.active { 
        display: flex; 
        animation: fadeIn 0.3s ease-out; 
    }

    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(10px); }
        to { opacity: 1; transform: translateY(0); }
    }

    /* Thumb-friendly navigation */
    .nav-button {
        -webkit-tap-highlight-color: transparent;
        touch-action: manipulation;
    }

    .logo-text { line-height: 0.9; }
</style>
</head> <body class="bg-slate-50 text-slate-900 flex flex-col fixed inset-0">
Copy to clipboard
<!-- TOP LOGO BAR -->
<header class="bg-white border-b border-slate-200 px-5 py-3 flex justify-between items-center z-50">
    <div class="flex items-center gap-3">
        <div class="text-sky-600">
            <svg class="w-8 h-8" viewBox="0 0 100 100" fill="currentColor">
                <circle cx="50" cy="15" r="4"/><circle cx="50" cy="85" r="4"/><circle cx="15" cy="50" r="4"/><circle cx="85" cy="50" r="4"/>
                <circle cx="25" cy="25" r="4"/><circle cx="75" cy="25" r="4"/><circle cx="25" cy="75" r="4"/><circle cx="75" cy="75" r="4"/>
                <circle cx="50" cy="30" r="3"/><circle cx="50" cy="70" r="3"/><circle cx="30" cy="50" r="3"/><circle cx="70" cy="50" r="3"/>
            </svg>
        </div>
        <div class="h-8 w-px bg-slate-200"></div>
        <div class="logo-text uppercase font-extrabold text-sky-600">
            <div class="text-[13px] tracking-tighter">PDS</div>
            <div class="text-[8px] tracking-tight">Environmental</div>
        </div>
    </div>
    <div class="text-[10px] font-bold text-slate-400 bg-slate-100 px-2 py-1 rounded">
        SLIDE <span id="current-num">1</span>/8
    </div>
</header>

<!-- PROGRESS BAR -->
<div class="w-full h-1 bg-slate-100">
    <div id="progress" class="h-full bg-sky-500 transition-all duration-500" style="width: 12.5%"></div>
</div>

<!-- CONTENT AREA -->
<main class="flex-grow relative overflow-hidden">
    
    <!-- Slide 1: Welcome -->
    <section class="slide active flex-col p-6 items-center text-center justify-center">
        <div class="w-20 h-20 bg-sky-100 rounded-full flex items-center justify-center mb-6">
            <i class="fa-solid fa-house-shield text-3xl text-sky-600"></i>
        </div>
        <h1 class="text-3xl font-extrabold text-slate-900 mb-4 leading-tight">Protect Your Home <br><span class="text-sky-600">Like a Pro</span></h1>
        <p class="text-slate-600 mb-8 px-4">Interactive guidance from PDS Environmental Services to help you identify and block pests.</p>
        <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200 w-full max-w-sm">
            <div class="flex items-center gap-3 text-left">
                <div class="w-10 h-10 bg-sky-600 rounded-lg flex items-center justify-center text-white">
                    <i class="fa-solid fa-play"></i>
                </div>
                <div>
                    <p class="text-xs font-bold text-slate-400 uppercase">Interactive Course</p>
                    <p class="font-bold text-slate-800">Start Home Awareness</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Slide 2: Risks -->
    <section class="slide flex-col p-6">
        <h2 class="text-2xl font-bold mb-4">Why it matters?</h2>
        <div class="space-y-4">
            <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-sm">
                <i class="fa-solid fa-virus text-red-500 text-2xl mb-2"></i>
                <h3 class="font-bold text-lg">Health Safety</h3>
                <p class="text-sm text-slate-600">Pests carry Salmonela and allergens. Protecting your home protects your family's health.</p>
            </div>
            <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-sm">
                <i class="fa-solid fa-fire-flame-curved text-orange-500 text-2xl mb-2"></i>
                <h3 class="font-bold text-lg">Fire Risk</h3>
                <p class="text-sm text-slate-600">Rodents chew electrical cables. Up to 25% of unexplained fires are pest-related.</p>
            </div>
        </div>
    </section>

    <!-- Slide 3: Rodents -->
    <section class="slide flex-col p-6">
        <h2 class="text-2xl font-bold mb-4">Rodent Proofing</h2>
        <div class="bg-slate-900 text-white p-6 rounded-2xl mb-4">
            <p class="text-sky-400 font-bold text-xs uppercase mb-1">The Pencil Test</p>
            <p class="text-lg leading-tight mb-4 italic">"If a pencil fits in a gap, a mouse can too."</p>
            <div class="h-px bg-white/20 mb-4"></div>
            <ul class="text-sm space-y-3">
                <li class="flex gap-2"><i class="fa-solid fa-circle-check text-sky-400 mt-1"></i> Seal gaps around pipes with Wire Wool.</li>
                <li class="flex gap-2"><i class="fa-solid fa-circle-check text-sky-400 mt-1"></i> Fit Brush Strips to external doors.</li>
            </ul>
        </div>
        <div class="bg-orange-50 border border-orange-100 p-4 rounded-xl flex items-center gap-3">
            <i class="fa-solid fa-lightbulb text-orange-500"></i>
            <p class="text-xs text-orange-800">Check your air-bricks! Use fine metal mesh covers to stop entry.</p>
        </div>
    </section>

    <!-- Slide 4: Insects -->
    <section class="slide flex-col p-6">
        <h2 class="text-2xl font-bold mb-4">Insects & Kitchens</h2>
        <p class="text-sm text-slate-600 mb-6">Insects like ants and cockroaches look for two things: <span class="font-bold">crumbs and moisture</span>.</p>
        <div class="grid grid-cols-1 gap-3">
            <div class="bg-white p-4 rounded-xl border border-slate-200 flex gap-4 items-start">
                <i class="fa-solid fa-sink text-sky-600 text-xl"></i>
                <div>
                    <h4 class="font-bold text-sm">Seal the Sink</h4>
                    <p class="text-xs text-slate-500">Apply silicone around pipe entries and backsplashes.</p>
                </div>
            </div>
            <div class="bg-white p-4 rounded-xl border border-slate-200 flex gap-4 items-start">
                <i class="fa-solid fa-box-open text-sky-600 text-xl"></i>
                <div>
                    <h4 class="font-bold text-sm">Airtight Storage</h4>
                    <p class="text-xs text-slate-500">Move sugars and cereals to plastic or glass containers.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Slide 5: Moths -->
    <section class="slide flex-col p-6">
        <h2 class="text-2xl font-bold mb-4">Protecting Fabrics</h2>
        <div class="bg-sky-600 text-white p-6 rounded-2xl mb-4 relative overflow-hidden">
            <i class="fa-solid fa-shirt absolute -right-4 -bottom-4 text-8xl opacity-10"></i>
            <h3 class="font-bold mb-2">The Wardrobe Rule</h3>
            <p class="text-sm opacity-90 mb-4">Moths love sweat and skin cells on natural fibers (wool/silk).</p>
            <div class="bg-white/20 p-3 rounded-lg text-xs">
                <strong>Tip:</strong> Never store worn clothes. Clean everything before long-term storage.
            </div>
        </div>
    </section>

    <!-- Slide 6: Checklist -->
    <section class="slide flex-col p-6">
        <h2 class="text-2xl font-bold mb-4">Exterior Checklist</h2>
        <div class="space-y-3">
            <div class="flex items-center gap-3 p-3 bg-white rounded-xl border border-slate-100">
                <input type="checkbox" class="w-5 h-5 rounded accent-sky-600">
                <label class="text-sm font-medium">Bins stored away from windows</label>
            </div>
            <div class="flex items-center gap-3 p-3 bg-white rounded-xl border border-slate-100">
                <input type="checkbox" class="w-5 h-5 rounded accent-sky-600">
                <label class="text-sm font-medium">Gutters cleared of debris</label>
            </div>
            <div class="flex items-center gap-3 p-3 bg-white rounded-xl border border-slate-100">
                <input type="checkbox" class="w-5 h-5 rounded accent-sky-600">
                <label class="text-sm font-medium">No branches touching the roof</label>
            </div>
            <div class="flex items-center gap-3 p-3 bg-white rounded-xl border border-slate-100">
                <input type="checkbox" class="w-5 h-5 rounded accent-sky-600">
                <label class="text-sm font-medium">Leaky external taps fixed</label>
            </div>
        </div>
    </section>

    <!-- Slide 7: Habits -->
    <section class="slide flex-col p-6">
        <h2 class="text-2xl font-bold mb-4">Daily Habits</h2>
        <div class="grid grid-cols-2 gap-3">
            <div class="bg-white p-4 rounded-xl text-center border border-slate-200">
                <i class="fa-solid fa-paw text-sky-600 mb-2"></i>
                <p class="text-[10px] font-bold uppercase">Pet food up at night</p>
            </div>
            <div class="bg-white p-4 rounded-xl text-center border border-slate-200">
                <i class="fa-solid fa-broom text-sky-600 mb-2"></i>
                <p class="text-[10px] font-bold uppercase">Wipe under fridge</p>
            </div>
            <div class="bg-white p-4 rounded-xl text-center border border-slate-200">
                <i class="fa-solid fa-box text-sky-600 mb-2"></i>
                <p class="text-[10px] font-bold uppercase">Ditch cardboard boxes</p>
            </div>
            <div class="bg-white p-4 rounded-xl text-center border border-slate-200">
                <i class="fa-solid fa-droplet text-sky-600 mb-2"></i>
                <p class="text-[10px] font-bold uppercase">Dry the kitchen sink</p>
            </div>
        </div>
    </section>

    <!-- Slide 8: Finish -->
    <section class="slide flex-col p-6 items-center text-center justify-center">
        <div class="w-20 h-20 bg-emerald-100 rounded-full flex items-center justify-center mb-6">
            <i class="fa-solid fa-circle-check text-3xl text-emerald-600"></i>
        </div>
        <h2 class="text-3xl font-extrabold mb-2">You're Protected!</h2>
        <p class="text-slate-500 mb-8 px-6 text-sm">Proofing is your first line of defense. For expert help, contact PDS Environmental Services.</p>
        
        <button onclick="window.location.reload()" class="w-full max-w-xs bg-slate-900 text-white py-4 rounded-2xl font-bold active:scale-95 transition-all">
            Restart Course
        </button>
        <p class="mt-8 text-[10px] text-slate-400 max-w-xs uppercase font-bold tracking-widest">PDS Environmental Services &copy; 2024</p>
    </section>

</main>

<!-- BOTTOM NAVIGATION (Fixed for mobile) -->
<footer class="bg-white border-t border-slate-200 p-4 pb-8 flex justify-between items-center z-50">
    <button id="prev-btn" onclick="moveSlide(-1)" class="nav-button w-1/3 py-3 flex items-center justify-center gap-2 font-bold text-slate-400 disabled:opacity-20">
        <i class="fa-solid fa-arrow-left"></i> <span>BACK</span>
    </button>
    
    <div class="flex gap-1.5 justify-center items-center w-1/3">
        <div class="dot w-1.5 h-1.5 rounded-full bg-slate-200"></div>
        <div class="dot w-1.5 h-1.5 rounded-full bg-slate-200"></div>
        <div class="dot w-1.5 h-1.5 rounded-full bg-slate-200"></div>
    </div>

    <button id="next-btn" onclick="moveSlide(1)" class="nav-button w-1/3 py-4 bg-sky-600 text-white rounded-2xl flex items-center justify-center gap-2 font-bold shadow-lg shadow-sky-200 active:scale-95 transition-all">
        <span>NEXT</span> <i class="fa-solid fa-arrow-right"></i>
    </button>
</footer>

<script>
    let currentIdx = 0;
    const slides = document.querySelectorAll('.slide');
    const dots = document.querySelectorAll('.dot');
    const progress = document.getElementById('progress');
    const currentNum = document.getElementById('current-num');
    const nextBtn = document.getElementById('next-btn');
    const prevBtn = document.getElementById('prev-btn');

    function update() {
        slides.forEach((s, i) => s.classList.toggle('active', i === currentIdx));
        
        // Progress
        const p = ((currentIdx + 1) / slides.length) * 100;
        progress.style.width = p + '%';
        currentNum.innerText = currentIdx + 1;

        // Nav buttons
        prevBtn.disabled = currentIdx === 0;
        if(currentIdx === slides.length - 1) {
            nextBtn.style.visibility = 'hidden';
        } else {
            nextBtn.style.visibility = 'visible';
        }

        // Dots (show relative position)
        dots.forEach((dot, i) => {
            dot.classList.toggle('bg-sky-500', i === Math.floor((currentIdx / slides.length) * 3));
            dot.classList.toggle('w-4', i === Math.floor((currentIdx / slides.length) * 3));
        });
    }

    function moveSlide(n) {
        currentIdx += n;
        update();
    }

    // Swipe Support
    let touchstartX = 0;
    let touchendX = 0;
    const main = document.querySelector('main');

    main.addEventListener('touchstart', e => {
        touchstartX = e.changedTouches[0].screenX;
    });

    main.addEventListener('touchend', e => {
        touchendX = e.changedTouches[0].screenX;
        handleGesture();
    });

    function handleGesture() {
        if (touchendX < touchstartX - 50) moveSlide(1);
        if (touchendX > touchstartX + 50) moveSlide(-1);
    }

    update();
</script>
</body> </html>

