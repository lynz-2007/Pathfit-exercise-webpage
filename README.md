<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PATHFIT | Exercise Program</title>
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&family=Oswald:wght@400;500;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Oswald', 'sans-serif'],
                    },
                    colors: {
                        background: '#0f172a',
                        foreground: '#f8fafc',
                        primary: '#22c55e',
                        secondary: '#0ea5e9',
                        accent: '#0ea5e9',
                        card: '#1e293b',
                        border: '#334155',
                    }
                }
            }
        }
    </script>

    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <style>
        body {
            background-color: #0f172a;
            color: #f8fafc;
            overflow-x: hidden;
        }
        
        /* Animation Classes matching Framer Motion feel */
        .fade-up {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.8s ease-out, transform 0.8s ease-out;
        }
        
        .fade-up.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .delay-100 { transition-delay: 0.1s; }
        .delay-200 { transition-delay: 0.2s; }
        .delay-300 { transition-delay: 0.3s; }
        .delay-400 { transition-delay: 0.4s; }

        html { scroll-behavior: smooth; }
    </style>
</head>
<body class="min-h-screen bg-background text-foreground font-sans selection:bg-primary selection:text-primary-foreground">

    <!-- NAVBAR -->
    <nav class="fixed top-0 w-full z-50 bg-background/80 backdrop-blur-md border-b border-white/10">
        <div class="container mx-auto px-4 md:px-6 h-16 flex items-center justify-between">
            <div class="flex items-center gap-2 font-display font-bold text-xl tracking-wider">
                <i data-lucide="dumbbell" class="text-primary h-6 w-6"></i>
                <span>PATHFIT<span class="text-primary">.</span></span>
            </div>
            <div class="hidden md:flex gap-8 text-sm font-bold uppercase tracking-widest text-muted-foreground">
                <a href="#types" class="hover:text-primary transition-colors">Types</a>
                <a href="#phases" class="hover:text-primary transition-colors">Phases</a>
                <a href="#fitt" class="hover:text-primary transition-colors">F.I.T.T.</a>
                <a href="#benefits" class="hover:text-primary transition-colors">Benefits</a>
            </div>
            <a href="#types" class="hidden md:inline-flex items-center justify-center rounded-md text-sm font-medium transition-colors focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 bg-primary text-primary-foreground shadow hover:bg-primary/90 h-9 px-4 py-2 uppercase tracking-wider font-display">
                Start Learning
            </a>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section class="relative h-screen w-full overflow-hidden flex items-center justify-center">
        <!-- Background Image -->
        <div class="absolute inset-0 z-0">
            <img src="https://images.unsplash.com/photo-1534438327276-14e5300c3a48?q=80&w=2070&auto=format&fit=crop" alt="Gym Background" class="w-full h-full object-cover">
            <div class="absolute inset-0 bg-gradient-to-b from-background/80 via-background/40 to-background/90"></div>
            <div class="absolute inset-0 bg-black/50"></div>
        </div>

        <div class="container relative z-10 px-4 md:px-6 text-center">
            <div class="fade-up max-w-5xl mx-auto space-y-6">
                <span class="inline-block py-1 px-3 rounded-full bg-primary/20 border border-primary/30 text-primary text-sm font-bold tracking-widest uppercase backdrop-blur-md">
                    Unit 3: Exercise Program
                </span>
                <h1 class="text-6xl md:text-8xl lg:text-9xl font-display font-bold uppercase tracking-tight text-white drop-shadow-2xl leading-none">
                    Unlock Your <br/><span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-accent">Potential</span>
                </h1>
                <p class="text-lg md:text-2xl text-gray-200 max-w-2xl mx-auto font-light leading-relaxed">
                    Master the biomechanics of movement. Understand the science of fitness. Build a stronger, healthier you.
                </p>
                <div class="pt-8 flex flex-col md:flex-row gap-4 justify-center">
                    <a href="#types" class="inline-flex items-center justify-center whitespace-nowrap rounded-md text-sm font-medium transition-colors focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 bg-primary text-primary-foreground hover:bg-primary/90 shadow-[0_0_20px_rgba(34,197,94,0.4)] h-14 px-8 text-lg font-display uppercase tracking-wider hover:scale-105 transform duration-200">
                        Start Learning
                    </a>
                    <a href="#phases" class="inline-flex items-center justify-center whitespace-nowrap rounded-md text-sm font-medium transition-colors focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 border border-white/30 bg-transparent text-white hover:bg-white/10 backdrop-blur-md h-14 px-8 text-lg font-display uppercase tracking-wider hover:scale-105 transform duration-200">
                        View Exercises
                    </a>
                </div>
            </div>
        </div>
        
        <!-- Scroll Indicator -->
        <div class="absolute bottom-10 left-1/2 -translate-x-1/2 text-white/50 animate-bounce">
            <i data-lucide="arrow-down" class="h-6 w-6"></i>
        </div>
    </section>

    <!-- INTRO SECTION -->
    <section class="py-24 container mx-auto px-4 md:px-6 relative">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-16 items-center">
            <div class="fade-up space-y-8">
                <div>
                    <h2 class="text-4xl md:text-5xl font-display font-bold uppercase tracking-wide text-primary mb-2">What is Exercise?</h2>
                    <div class="h-1 w-20 bg-accent"></div>
                </div>
                <p class="text-slate-400 text-xl leading-relaxed font-light">
                    Exercise is any bodily activity that enhances or maintains physical fitness and overall health and wellness. 
                    It is performed for various reasons: to aid growth, improve strength, prevent aging, develop muscles and the 
                    cardiovascular system.
                </p>
                <div class="grid grid-cols-2 gap-4 pt-4">
                    <div class="p-6 bg-card rounded-xl border border-border/50 hover:border-primary/50 transition-colors">
                        <i data-lucide="heart" class="h-10 w-10 text-accent mb-4"></i>
                        <h4 class="font-bold text-lg mb-2 uppercase tracking-wide">Physical Health</h4>
                        <p class="text-sm text-slate-400">Reduces risk of chronic diseases and improves longevity.</p>
                    </div>
                    <div class="p-6 bg-card rounded-xl border border-border/50 hover:border-primary/50 transition-colors">
                        <i data-lucide="brain" class="h-10 w-10 text-primary mb-4"></i>
                        <h4 class="font-bold text-lg mb-2 uppercase tracking-wide">Mental Wellness</h4>
                        <p class="text-sm text-slate-400">Reduces tension, acts as anti-depressant, and relieves stress.</p>
                    </div>
                </div>
            </div>
            
            <div class="relative fade-up delay-200">
                <div class="absolute -inset-4 bg-gradient-to-r from-primary/20 to-accent/20 rounded-2xl blur-3xl opacity-40"></div>
                <div class="relative bg-card/80 backdrop-blur-sm border border-border p-10 rounded-2xl shadow-2xl">
                    <h3 class="font-display text-3xl mb-8 uppercase tracking-wide flex items-center gap-3">
                        <i data-lucide="activity" class="text-primary"></i> Key Functions
                    </h3>
                    <ul class="grid grid-cols-1 gap-4">
                        <li class="flex items-center gap-4 text-lg p-3 rounded-lg hover:bg-white/5 transition-colors"><div class="h-2 w-2 rounded-full bg-accent shrink-0"></div> Release pent-up emotions</li>
                        <li class="flex items-center gap-4 text-lg p-3 rounded-lg hover:bg-white/5 transition-colors"><div class="h-2 w-2 rounded-full bg-accent shrink-0"></div> Build Strength & Coordination</li>
                        <li class="flex items-center gap-4 text-lg p-3 rounded-lg hover:bg-white/5 transition-colors"><div class="h-2 w-2 rounded-full bg-accent shrink-0"></div> Increase Flexibility</li>
                        <li class="flex items-center gap-4 text-lg p-3 rounded-lg hover:bg-white/5 transition-colors"><div class="h-2 w-2 rounded-full bg-accent shrink-0"></div> Reduce Weight</li>
                        <li class="flex items-center gap-4 text-lg p-3 rounded-lg hover:bg-white/5 transition-colors"><div class="h-2 w-2 rounded-full bg-accent shrink-0"></div> Warm up muscles before vigor</li>
                        <li class="flex items-center gap-4 text-lg p-3 rounded-lg hover:bg-white/5 transition-colors"><div class="h-2 w-2 rounded-full bg-accent shrink-0"></div> Discharge excess energy</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- TYPES OF EXERCISE -->
    <section id="types" class="py-24 bg-secondary/10 relative overflow-hidden">
        <div class="container mx-auto px-4 md:px-6 relative z-10">
            <div class="text-center mb-20 fade-up">
                <h2 class="text-5xl md:text-7xl font-display font-bold uppercase tracking-tighter mb-6">Types of <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-accent">Exercise</span></h2>
                <p class="text-slate-400 text-xl max-w-3xl mx-auto">Physical exercises are generally grouped into three types, depending on the overall effect they have on the human body.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Aerobic Card -->
                <div class="fade-up delay-100 group relative overflow-hidden rounded-2xl bg-card border border-border h-[600px] flex flex-col shadow-2xl hover:-translate-y-2 transition-transform duration-300">
                    <div class="absolute inset-0 z-0">
                        <img src="https://images.unsplash.com/photo-1552674605-469555942c77?q=80&w=2000&auto=format&fit=crop" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0">
                        <div class="absolute inset-0 bg-gradient-to-t from-black via-black/70 to-transparent opacity-90 group-hover:opacity-80 transition-opacity"></div>
                    </div>
                    <div class="relative z-10 mt-auto p-10 space-y-6">
                        <div class="p-3 bg-accent w-fit rounded-lg shadow-[0_0_15px_rgba(14,165,233,0.5)]">
                            <i data-lucide="activity" class="h-8 w-8 text-white"></i>
                        </div>
                        <div>
                            <h3 class="text-4xl font-display font-bold uppercase text-white mb-2">Aerobic</h3>
                            <div class="h-1 w-12 bg-accent mb-4"></div>
                            <p class="text-gray-300 text-base leading-relaxed mb-6">
                                Uses large muscle groups and causes the body to use more oxygen. The goal is to increase cardiovascular endurance.
                            </p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-3 py-1 bg-white/10 text-white text-xs font-bold uppercase tracking-wider rounded-full backdrop-blur-sm border border-white/10">Running</span>
                                <span class="px-3 py-1 bg-white/10 text-white text-xs font-bold uppercase tracking-wider rounded-full backdrop-blur-sm border border-white/10">Cycling</span>
                                <span class="px-3 py-1 bg-white/10 text-white text-xs font-bold uppercase tracking-wider rounded-full backdrop-blur-sm border border-white/10">Swimming</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Anaerobic Card -->
                <div class="fade-up delay-200 group relative overflow-hidden rounded-2xl bg-card border border-border h-[600px] flex flex-col shadow-2xl hover:-translate-y-2 transition-transform duration-300">
                    <div class="absolute inset-0 z-0">
                        <img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?q=80&w=2000&auto=format&fit=crop" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0">
                        <div class="absolute inset-0 bg-gradient-to-t from-black via-black/70 to-transparent opacity-90 group-hover:opacity-80 transition-opacity"></div>
                    </div>
                    <div class="relative z-10 mt-auto p-10 space-y-6">
                        <div class="p-3 bg-primary w-fit rounded-lg shadow-[0_0_15px_rgba(34,197,94,0.5)]">
                            <i data-lucide="zap" class="h-8 w-8 text-black"></i>
                        </div>
                        <div>
                            <h3 class="text-4xl font-display font-bold uppercase text-white mb-2">Anaerobic</h3>
                            <div class="h-1 w-12 bg-primary mb-4"></div>
                            <p class="text-gray-300 text-base leading-relaxed mb-6">
                                Strength and resistance training to firm, strengthen, and increase muscle mass. Improves bone density.
                            </p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-3 py-1 bg-white/10 text-white text-xs font-bold uppercase tracking-wider rounded-full backdrop-blur-sm border border-white/10">Weights</span>
                                <span class="px-3 py-1 bg-white/10 text-white text-xs font-bold uppercase tracking-wider rounded-full backdrop-blur-sm border border-white/10">Push-ups</span>
                                <span class="px-3 py-1 bg-white/10 text-white text-xs font-bold uppercase tracking-wider rounded-full backdrop-blur-sm border border-white/10">Squats</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Flexibility Card -->
                <div class="fade-up delay-300 group relative overflow-hidden rounded-2xl bg-card border border-border h-[600px] flex flex-col shadow-2xl hover:-translate-y-2 transition-transform duration-300">
                    <div class="absolute inset-0 z-0">
                        <img src="https://images.unsplash.com/photo-1544367563-12123d896889?q=80&w=2000&auto=format&fit=crop" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110 grayscale group-hover:grayscale-0">
                        <div class="absolute inset-0 bg-gradient-to-t from-black via-black/70 to-transparent opacity-90 group-hover:opacity-80 transition-opacity"></div>
                    </div>
                    <div class="relative z-10 mt-auto p-10 space-y-6">
                        <div class="p-3 bg-purple-500 w-fit rounded-lg shadow-[0_0_15px_rgba(168,85,247,0.5)]">
                            <i data-lucide="layers" class="h-8 w-8 text-white"></i>
                        </div>
                        <div>
                            <h3 class="text-4xl font-display font-bold uppercase text-white mb-2">Flexibility</h3>
                            <div class="h-1 w-12 bg-purple-500 mb-4"></div>
                            <p class="text-gray-300 text-base leading-relaxed mb-6">
                                Stretches and lengthens muscles to improve joint flexibility and keep muscles limber. Reduces injury risk.
                            </p>
                            <div class="flex flex-wrap gap-2">
                                <span class="px-3 py-1 bg-white/10 text-white text-xs font-bold uppercase tracking-wider rounded-full backdrop-blur-sm border border-white/10">Yoga</span>
                                <span class="px-3 py-1 bg-white/10 text-white text-xs font-bold uppercase tracking-wider rounded-full backdrop-blur-sm border border-white/10">Stretching</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- PHASES OF FITNESS -->
    <section id="phases" class="py-32 container mx-auto px-4 md:px-6">
        <div class="text-center max-w-4xl mx-auto mb-20 fade-up">
            <span class="text-primary font-bold tracking-widest uppercase mb-4 block">The Process</span>
            <h2 class="text-5xl md:text-7xl font-display font-bold uppercase tracking-tight mb-8">Phases of <span class="text-white">Fitness</span></h2>
            <p class="text-slate-400 text-xl">A complete exercise program consists of three essential phases to ensure safety and effectiveness.</p>
        </div>
        
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 relative">
            <!-- Phase 1 -->
            <div class="fade-up delay-100 relative z-10 bg-card border border-border rounded-2xl p-8 hover:border-primary transition-all duration-300 group">
                <div class="w-16 h-16 bg-background border-2 border-border rounded-full flex items-center justify-center text-2xl font-display font-bold mb-6 group-hover:border-primary group-hover:text-primary transition-colors mx-auto lg:mx-0 shadow-lg">01</div>
                <h3 class="text-3xl font-display font-bold uppercase mb-4 text-center lg:text-left">Warm-Up</h3>
                <div class="h-1 w-12 bg-primary mb-6 mx-auto lg:mx-0"></div>
                <p class="text-slate-400 mb-6 leading-relaxed text-center lg:text-left">Elevates body temperature to prepare muscles. Increases blood flow and oxygen. Prevents cramps.</p>
                <div class="bg-secondary/10 p-4 rounded-lg">
                    <div class="flex items-center gap-3 mb-2 font-bold text-sm uppercase text-white"><i data-lucide="flame" class="text-orange-500 h-4 w-4"></i> <span>Activity: 5-10 Mins</span></div>
                    <p class="text-xs text-slate-400 pl-8">Walking, jogging, stationary bicycling.</p>
                </div>
            </div>

            <!-- Phase 2 -->
            <div class="fade-up delay-200 relative z-10 bg-gradient-to-b from-primary/10 to-card border border-primary/30 rounded-2xl p-8 shadow-[0_0_30px_rgba(34,197,94,0.1)] transform lg:-translate-y-8">
                <div class="w-16 h-16 bg-primary border-2 border-primary rounded-full flex items-center justify-center text-2xl font-display font-bold mb-6 text-primary-foreground mx-auto lg:mx-0 shadow-lg shadow-primary/20">02</div>
                <h3 class="text-3xl font-display font-bold uppercase mb-4 text-center lg:text-left text-white">Exercise Proper</h3>
                <div class="h-1 w-12 bg-primary mb-6 mx-auto lg:mx-0"></div>
                <p class="text-gray-300 mb-6 leading-relaxed text-center lg:text-left">The main workout phase designed to meet training objectives using calisthenics or weight training.</p>
                <div class="bg-primary/20 p-4 rounded-lg border border-primary/20">
                    <div class="flex items-center gap-3 mb-2 font-bold text-sm uppercase text-primary"><i data-lucide="dumbbell" class="h-4 w-4"></i> <span>Main Goals</span></div>
                    <p class="text-xs text-gray-300 pl-8">Develop major muscles: Push up, Squats, Lunges.</p>
                </div>
            </div>

            <!-- Phase 3 -->
            <div class="fade-up delay-300 relative z-10 bg-card border border-border rounded-2xl p-8 hover:border-accent transition-all duration-300 group">
                <div class="w-16 h-16 bg-background border-2 border-border rounded-full flex items-center justify-center text-2xl font-display font-bold mb-6 group-hover:border-accent group-hover:text-accent transition-colors mx-auto lg:mx-0 shadow-lg">03</div>
                <h3 class="text-3xl font-display font-bold uppercase mb-4 text-center lg:text-left">Cool Down</h3>
                <div class="h-1 w-12 bg-accent mb-6 mx-auto lg:mx-0"></div>
                <p class="text-slate-400 mb-6 leading-relaxed text-center lg:text-left">Gradually tapers off stress. Keeps blood circulating to prevent dizziness and pooling.</p>
                <div class="bg-accent/10 p-4 rounded-lg">
                    <div class="flex items-center gap-3 mb-2 font-bold text-sm uppercase text-white"><i data-lucide="clock" class="text-accent h-4 w-4"></i> <span>Recovery Phase</span></div>
                    <p class="text-xs text-slate-400 pl-8">Returns body to pre-exercise level.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- FITT FORMULA -->
    <section id="fitt" class="py-32 bg-primary relative overflow-hidden">
        <div class="container mx-auto px-4 md:px-6 relative z-10">
            <div class="flex flex-col md:flex-row items-start md:items-end justify-between mb-20 gap-8 fade-up">
                <div>
                    <h2 class="text-6xl md:text-8xl font-display font-bold uppercase tracking-tight text-primary-foreground leading-none">The F.I.T.T. <br/>Formula</h2>
                    <p class="text-primary-foreground/80 text-xl max-w-md mt-6 font-medium">Important factors in determining how much physical activity is enough for you.</p>
                </div>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- F -->
                <div class="fade-up delay-100 bg-black/20 backdrop-blur-md border border-white/10 p-8 rounded-2xl hover:bg-black/30 transition-all hover:-translate-y-2 duration-300">
                    <div class="flex justify-between items-start mb-6">
                        <span class="text-7xl font-display font-bold opacity-30 text-white">F</span>
                        <div class="p-3 bg-white/10 rounded-full"><i data-lucide="repeat" class="h-6 w-6 text-white"></i></div>
                    </div>
                    <h3 class="text-2xl font-bold uppercase mb-3 text-white">Frequency</h3>
                    <div class="h-0.5 w-10 bg-white/50 mb-4"></div>
                    <p class="text-white/80 leading-relaxed text-sm">How often one does the physical activity. (e.g., Daily, 3x/week)</p>
                </div>
                <!-- I -->
                <div class="fade-up delay-200 bg-black/20 backdrop-blur-md border border-white/10 p-8 rounded-2xl hover:bg-black/30 transition-all hover:-translate-y-2 duration-300">
                    <div class="flex justify-between items-start mb-6">
                        <span class="text-7xl font-display font-bold opacity-30 text-white">I</span>
                        <div class="p-3 bg-white/10 rounded-full"><i data-lucide="zap" class="h-6 w-6 text-white"></i></div>
                    </div>
                    <h3 class="text-2xl font-bold uppercase mb-3 text-white">Intensity</h3>
                    <div class="h-0.5 w-10 bg-white/50 mb-4"></div>
                    <p class="text-white/80 leading-relaxed text-sm">How hard one performs. Determined by type and fitness goals.</p>
                </div>
                <!-- T -->
                <div class="fade-up delay-300 bg-black/20 backdrop-blur-md border border-white/10 p-8 rounded-2xl hover:bg-black/30 transition-all hover:-translate-y-2 duration-300">
                    <div class="flex justify-between items-start mb-6">
                        <span class="text-7xl font-display font-bold opacity-30 text-white">T</span>
                        <div class="p-3 bg-white/10 rounded-full"><i data-lucide="clock" class="h-6 w-6 text-white"></i></div>
                    </div>
                    <h3 class="text-2xl font-bold uppercase mb-3 text-white">Time</h3>
                    <div class="h-0.5 w-10 bg-white/50 mb-4"></div>
                    <p class="text-white/80 leading-relaxed text-sm">How long one does the activity. (e.g., 15-30 minutes).</p>
                </div>
                <!-- T -->
                <div class="fade-up delay-400 bg-black/20 backdrop-blur-md border border-white/10 p-8 rounded-2xl hover:bg-black/30 transition-all hover:-translate-y-2 duration-300">
                    <div class="flex justify-between items-start mb-6">
                        <span class="text-7xl font-display font-bold opacity-30 text-white">T</span>
                        <div class="p-3 bg-white/10 rounded-full"><i data-lucide="activity" class="h-6 w-6 text-white"></i></div>
                    </div>
                    <h3 class="text-2xl font-bold uppercase mb-3 text-white">Type</h3>
                    <div class="h-0.5 w-10 bg-white/50 mb-4"></div>
                    <p class="text-white/80 leading-relaxed text-sm">The specific activity chosen to build a specific part of fitness.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- BENEFITS & PRINCIPLES -->
    <section id="benefits" class="py-32 container mx-auto px-4 md:px-6">
        <div class="grid grid-cols-1 xl:grid-cols-2 gap-20">
            <!-- Principles -->
            <div class="fade-up">
                <div class="flex items-center gap-4 mb-8">
                    <div class="p-3 bg-primary/10 rounded-xl"><i data-lucide="shield-check" class="text-primary h-8 w-8"></i></div>
                    <h2 class="text-4xl font-display font-bold uppercase tracking-wide">Principles of Training</h2>
                </div>
                <div class="space-y-4">
                    <details class="group bg-card/30 border border-border rounded-xl">
                        <summary class="flex justify-between items-center font-display uppercase tracking-wide text-xl py-6 px-6 cursor-pointer hover:text-primary transition-colors list-none">
                            Specificity
                            <span class="transition group-open:rotate-180"><i data-lucide="chevron-down" class="h-5 w-5"></i></span>
                        </summary>
                        <div class="text-slate-400 leading-relaxed text-base px-6 pb-6">Benefits associated with the training stimulus can only be achieved when it duplicates the movements and energy systems involved in the exercise.</div>
                    </details>
                    <details class="group bg-card/30 border border-border rounded-xl">
                        <summary class="flex justify-between items-center font-display uppercase tracking-wide text-xl py-6 px-6 cursor-pointer hover:text-primary transition-colors list-none">
                            Overload
                            <span class="transition group-open:rotate-180"><i data-lucide="chevron-down" class="h-5 w-5"></i></span>
                        </summary>
                        <div class="text-slate-400 leading-relaxed text-base px-6 pb-6">A body system must be exercised at a level beyond which it is presently accustomed. The body adapts to this overload.</div>
                    </details>
                    <details class="group bg-card/30 border border-border rounded-xl">
                        <summary class="flex justify-between items-center font-display uppercase tracking-wide text-xl py-6 px-6 cursor-pointer hover:text-primary transition-colors list-none">
                            Progression
                            <span class="transition group-open:rotate-180"><i data-lucide="chevron-down" class="h-5 w-5"></i></span>
                        </summary>
                        <div class="text-slate-400 leading-relaxed text-base px-6 pb-6">The amount and intensity of your exercise should be increased gradually. Rejects the 'no pain, no gain' theory.</div>
                    </details>
                    <details class="group bg-card/30 border border-border rounded-xl">
                        <summary class="flex justify-between items-center font-display uppercase tracking-wide text-xl py-6 px-6 cursor-pointer hover:text-primary transition-colors list-none">
                            Reversibility
                            <span class="transition group-open:rotate-180"><i data-lucide="chevron-down" class="h-5 w-5"></i></span>
                        </summary>
                        <div class="text-slate-400 leading-relaxed text-base px-6 pb-6">If an individual stops exercising, the body returns to its initial level of fitness. "If you don't use it, you will lose it."</div>
                    </details>
                </div>
            </div>

            <!-- Benefits -->
            <div class="fade-up delay-100">
                <div class="flex items-center gap-4 mb-8">
                    <div class="p-3 bg-accent/10 rounded-xl"><i data-lucide="bar-chart-3" class="text-accent h-8 w-8"></i></div>
                    <h2 class="text-4xl font-display font-bold uppercase tracking-wide">Benefits of Exercise</h2>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="bg-card/50 border border-border/60 p-6 rounded-xl hover:bg-card transition-colors">
                        <h3 class="text-primary uppercase tracking-wide text-xl flex items-center gap-2 mb-4"><i data-lucide="activity" class="h-5 w-5"></i> Physiological</h3>
                        <ul class="space-y-4">
                            <li class="flex gap-3 text-sm text-slate-400"><span class="h-1.5 w-1.5 rounded-full bg-primary mt-2 shrink-0"></span> Improved heart function</li>
                            <li class="flex gap-3 text-sm text-slate-400"><span class="h-1.5 w-1.5 rounded-full bg-primary mt-2 shrink-0"></span> Increased muscle tone</li>
                            <li class="flex gap-3 text-sm text-slate-400"><span class="h-1.5 w-1.5 rounded-full bg-primary mt-2 shrink-0"></span> Better weight control</li>
                            <li class="flex gap-3 text-sm text-slate-400"><span class="h-1.5 w-1.5 rounded-full bg-primary mt-2 shrink-0"></span> Better sleep</li>
                        </ul>
                    </div>

                    <div class="bg-card/50 border border-border/60 p-6 rounded-xl hover:bg-card transition-colors">
                        <h3 class="text-accent uppercase tracking-wide text-xl flex items-center gap-2 mb-4"><i data-lucide="brain" class="h-5 w-5"></i> Psychological</h3>
                        <ul class="space-y-4">
                            <li class="flex gap-3 text-sm text-slate-400"><span class="h-1.5 w-1.5 rounded-full bg-accent mt-2 shrink-0"></span> Elevated mood</li>
                            <li class="flex gap-3 text-sm text-slate-400"><span class="h-1.5 w-1.5 rounded-full bg-accent mt-2 shrink-0"></span> Relieved stress</li>
                            <li class="flex gap-3 text-sm text-slate-400"><span class="h-1.5 w-1.5 rounded-full bg-accent mt-2 shrink-0"></span> Improved self-esteem</li>
                            <li class="flex gap-3 text-sm text-slate-400"><span class="h-1.5 w-1.5 rounded-full bg-accent mt-2 shrink-0"></span> Better relaxation</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="py-12 bg-black border-t border-border text-center">
        <div class="container mx-auto px-4">
            <h3 class="text-2xl font-display font-bold tracking-wider mb-2">PATHFIT<span class="text-primary">.</span></h3>
            <p class="text-slate-500 text-sm">Empowering students with the knowledge of physical fitness.</p>
            <p class="text-slate-700 text-xs mt-8">&copy; 2025 PATHFIT Unit 3. All rights reserved.</p>
        </div>
    </footer>

    <!-- Init Icons & Animations -->
    <script>
        lucide.createIcons();

        // Simple Intersection Observer for Fade Up
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));
    </script>
</body>
</html># Pathfit-exercise-webpage
