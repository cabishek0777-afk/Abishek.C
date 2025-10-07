<meta name='viewport' content='width=device-width, initial-scale=1'/><meta name='viewport' content='width=device-width, initial-scale=1'/>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abishek - Creative Developer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            box-sizing: border-box;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .glass-effect {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .floating-animation {
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .slide-in {
            animation: slideIn 0.8s ease-out;
        }
        
        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 1rem;
        }
        
        .project-card {
            transition: all 0.3s ease;
            transform-style: preserve-3d;
        }
        
        .project-card:hover {
            transform: rotateY(5deg) rotateX(5deg);
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
        }
        
        .dark-mode {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
        }
    </style>
</head>
<body class="dark-mode text-white overflow-x-hidden">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full z-50 glass-effect">
        <div class="max-w-7xl mx-auto px-6 py-4">
            <div class="flex justify-between items-center">
                <div class="text-2xl font-bold gradient-text">Abishek</div>
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="hover:text-purple-400 transition duration-300">Home</a>
                    <a href="#about" class="hover:text-purple-400 transition duration-300">About</a>
                    <a href="#skills" class="hover:text-purple-400 transition duration-300">Skills</a>
                    <a href="#projects" class="hover:text-purple-400 transition duration-300">Projects</a>
                    <a href="#contact" class="hover:text-purple-400 transition duration-300">Contact</a>
                </div>
                <button id="mobile-menu-btn" class="md:hidden">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
            <div id="mobile-menu" class="md:hidden hidden mt-4 space-y-2">
                <a href="#home" class="block py-2 hover:text-purple-400">Home</a>
                <a href="#about" class="block py-2 hover:text-purple-400">About</a>
                <a href="#skills" class="block py-2 hover:text-purple-400">Skills</a>
                <a href="#projects" class="block py-2 hover:text-purple-400">Projects</a>
                <a href="#contact" class="block py-2 hover:text-purple-400">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="min-h-screen flex items-center justify-center relative overflow-hidden pt-20">
        <div class="absolute inset-0 opacity-20">
            <div class="absolute top-20 left-10 w-72 h-72 bg-purple-500 rounded-full mix-blend-multiply filter blur-xl floating-animation"></div>
            <div class="absolute top-40 right-10 w-72 h-72 bg-blue-500 rounded-full mix-blend-multiply filter blur-xl floating-animation" style="animation-delay: 2s;"></div>
            <div class="absolute bottom-20 left-1/2 w-72 h-72 bg-pink-500 rounded-full mix-blend-multiply filter blur-xl floating-animation" style="animation-delay: 4s;"></div>
        </div>
        
        <div class="text-center z-10 px-6 slide-in">
            <div class="mb-8">
                <div class="w-40 h-40 mx-auto rounded-full bg-gradient-to-r from-purple-400 via-pink-500 to-red-500 p-1">
                    <div class="w-full h-full rounded-full bg-gray-900 flex items-center justify-center text-6xl">
                        👨‍💻
                    </div>
                </div>
            </div>
            <h1 class="text-6xl md:text-8xl font-bold mb-6">
                <span class="gradient-text">Abishek</span>
            </h1>
            <p class="text-xl md:text-2xl mb-4 text-gray-300">Creative Developer & Digital Artist</p>
            <p class="text-lg mb-8 max-w-2xl mx-auto text-gray-400 leading-relaxed">
                Crafting beautiful digital experiences with code, creativity, and a passion for innovation. 
                Let's build something amazing together.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#projects" class="bg-gradient-to-r from-purple-500 to-pink-500 px-8 py-4 rounded-full font-semibold hover:from-purple-600 hover:to-pink-600 transition duration-300 transform hover:scale-105">
                    View My Work
                </a>
                <a href="#contact" class="border-2 border-purple-500 px-8 py-4 rounded-full font-semibold hover:bg-purple-500 transition duration-300 transform hover:scale-105">
                    Get In Touch
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-6">
        <div class="max-w-6xl mx-auto">
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <h2 class="text-4xl md:text-5xl font-bold gradient-text">About Me</h2>
                    <p class="text-gray-300 text-lg leading-relaxed">
                        I'm a passionate developer who loves creating digital experiences that make a difference. 
                        With expertise in modern web technologies and a keen eye for design, I transform ideas into reality.
                    </p>
                    <p class="text-gray-400 leading-relaxed">
                        When I'm not coding, you'll find me exploring new technologies, contributing to open-source projects, 
                        or sharing knowledge with the developer community. I believe in continuous learning and pushing the 
                        boundaries of what's possible with code.
                    </p>
                    <div class="flex flex-wrap gap-3">
                        <span class="bg-purple-900/50 text-purple-300 px-4 py-2 rounded-full text-sm">🚀 Innovation</span>
                        <span class="bg-blue-900/50 text-blue-300 px-4 py-2 rounded-full text-sm">💡 Problem Solver</span>
                        <span class="bg-pink-900/50 text-pink-300 px-4 py-2 rounded-full text-sm">🎨 Creative</span>
                        <span class="bg-green-900/50 text-green-300 px-4 py-2 rounded-full text-sm">🌱 Lifelong Learner</span>
                    </div>
                </div>
                <div class="relative">
                    <div class="w-80 h-80 mx-auto relative">
                        <div class="absolute inset-0 bg-gradient-to-r from-purple-500 to-pink-500 rounded-3xl transform rotate-6"></div>
                        <div class="absolute inset-0 glass-effect rounded-3xl flex items-center justify-center text-8xl transform -rotate-3">
                            🎯
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20 px-6">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-bold gradient-text mb-4">Skills & Technologies</h2>
                <p class="text-gray-400 max-w-2xl mx-auto">
                    Here are the technologies and tools I work with to bring ideas to life
                </p>
            </div>
            
            <div class="tech-grid mb-12">
                <div class="glass-effect p-6 rounded-2xl text-center hover:bg-white/20 transition duration-300">
                    <div class="text-4xl mb-3">⚛️</div>
                    <h3 class="font-semibold text-purple-300">React</h3>
                </div>
                <div class="glass-effect p-6 rounded-2xl text-center hover:bg-white/20 transition duration-300">
                    <div class="text-4xl mb-3">📱</div>
                    <h3 class="font-semibold text-blue-300">React Native</h3>
                </div>
                <div class="glass-effect p-6 rounded-2xl text-center hover:bg-white/20 transition duration-300">
                    <div class="text-4xl mb-3">🟨</div>
                    <h3 class="font-semibold text-yellow-300">JavaScript</h3>
                </div>
                <div class="glass-effect p-6 rounded-2xl text-center hover:bg-white/20 transition duration-300">
                    <div class="text-4xl mb-3">🔷</div>
                    <h3 class="font-semibold text-blue-400">TypeScript</h3>
                </div>
                <div class="glass-effect p-6 rounded-2xl text-center hover:bg-white/20 transition duration-300">
                    <div class="text-4xl mb-3">🟢</div>
                    <h3 class="font-semibold text-green-300">Node.js</h3>
                </div>
                <div class="glass-effect p-6 rounded-2xl text-center hover:bg-white/20 transition duration-300">
                    <div class="text-4xl mb-3">🐍</div>
                    <h3 class="font-semibold text-green-400">Python</h3>
                </div>
                <div class="glass-effect p-6 rounded-2xl text-center hover:bg-white/20 transition duration-300">
                    <div class="text-4xl mb-3">🎨</div>
                    <h3 class="font-semibold text-pink-300">CSS/Tailwind</h3>
                </div>
                <div class="glass-effect p-6 rounded-2xl text-center hover:bg-white/20 transition duration-300">
                    <div class="text-4xl mb-3">🗄️</div>
                    <h3 class="font-semibold text-orange-300">MongoDB</h3>
                </div>
            </div>

            <div class="grid md:grid-cols-3 gap-8">
                <div class="glass-effect p-8 rounded-2xl">
                    <h3 class="text-2xl font-bold text-purple-300 mb-4">Frontend</h3>
                    <ul class="space-y-2 text-gray-300">
                        <li>• Modern React & Next.js</li>
                        <li>• Responsive Design</li>
                        <li>• State Management</li>
                        <li>• Performance Optimization</li>
                    </ul>
                </div>
                <div class="glass-effect p-8 rounded-2xl">
                    <h3 class="text-2xl font-bold text-blue-300 mb-4">Backend</h3>
                    <ul class="space-y-2 text-gray-300">
                        <li>• RESTful APIs</li>
                        <li>• Database Design</li>
                        <li>• Authentication</li>
                        <li>• Cloud Services</li>
                    </ul>
                </div>
                <div class="glass-effect p-8 rounded-2xl">
                    <h3 class="text-2xl font-bold text-pink-300 mb-4">Tools</h3>
                    <ul class="space-y-2 text-gray-300">
                        <li>• Git & GitHub</li>
                        <li>• Docker</li>
                        <li>• CI/CD Pipelines</li>
                        <li>• Testing Frameworks</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 px-6">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-bold gradient-text mb-4">Featured Projects</h2>
                <p class="text-gray-400 max-w-2xl mx-auto">
                    A showcase of my recent work and creative solutions
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="project-card glass-effect rounded-2xl overflow-hidden">
                    <div class="h-48 bg-gradient-to-br from-purple-500 to-pink-500 flex items-center justify-center text-6xl">
                        🚀
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">AI-Powered Dashboard</h3>
                        <p class="text-gray-400 mb-4">
                            A modern analytics dashboard with AI insights and real-time data visualization.
                        </p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-purple-900/50 text-purple-300 px-2 py-1 rounded text-xs">React</span>
                            <span class="bg-blue-900/50 text-blue-300 px-2 py-1 rounded text-xs">TypeScript</span>
                            <span class="bg-green-900/50 text-green-300 px-2 py-1 rounded text-xs">Node.js</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-purple-400 hover:text-purple-300 font-semibold">Live Demo</a>
                            <a href="#" class="text-gray-400 hover:text-gray-300 font-semibold">GitHub</a>
                        </div>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="project-card glass-effect rounded-2xl overflow-hidden">
                    <div class="h-48 bg-gradient-to-br from-blue-500 to-cyan-500 flex items-center justify-center text-6xl">
                        📱
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">Mobile Fitness App</h3>
                        <p class="text-gray-400 mb-4">
                            Cross-platform fitness tracking app with social features and workout plans.
                        </p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-blue-900/50 text-blue-300 px-2 py-1 rounded text-xs">React Native</span>
                            <span class="bg-purple-900/50 text-purple-300 px-2 py-1 rounded text-xs">Firebase</span>
                            <span class="bg-pink-900/50 text-pink-300 px-2 py-1 rounded text-xs">Redux</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-blue-400 hover:text-blue-300 font-semibold">Live Demo</a>
                            <a href="#" class="text-gray-400 hover:text-gray-300 font-semibold">GitHub</a>
                        </div>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="project-card glass-effect rounded-2xl overflow-hidden">
                    <div class="h-48 bg-gradient-to-br from-green-500 to-teal-500 flex items-center justify-center text-6xl">
                        🌐
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold text-white mb-2">E-Commerce Platform</h3>
                        <p class="text-gray-400 mb-4">
                            Full-stack e-commerce solution with payment integration and admin panel.
                        </p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-green-900/50 text-green-300 px-2 py-1 rounded text-xs">Next.js</span>
                            <span class="bg-yellow-900/50 text-yellow-300 px-2 py-1 rounded text-xs">Stripe</span>
                            <span class="bg-orange-900/50 text-orange-300 px-2 py-1 rounded text-xs">MongoDB</span>
                        </div>
                        <div class="flex space-x-4">
                            <a href="#" class="text-green-400 hover:text-green-300 font-semibold">Live Demo</a>
                            <a href="#" class="text-gray-400 hover:text-gray-300 font-semibold">GitHub</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-6">
        <div class="max-w-4xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-bold gradient-text mb-4">Let's Connect</h2>
                <p class="text-gray-400 max-w-2xl mx-auto">
                    Ready to start your next project? Let's discuss how we can work together.
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 gap-12">
                <div class="space-y-8">
                    <div class="glass-effect p-6 rounded-2xl">
                        <div class="flex items-center space-x-4">
                            <div class="w-12 h-12 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full flex items-center justify-center text-xl">
                                📧
                            </div>
                            <div>
                                <h3 class="font-semibold text-white">Email</h3>
                                <p class="text-gray-400">cabishek0777@gmail.com</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="glass-effect p-6 rounded-2xl">
                        <div class="flex items-center space-x-4">
                            <div class="w-12 h-12 bg-gradient-to-r from-blue-500 to-cyan-500 rounded-full flex items-center justify-center text-xl">
                                📱
                            </div>
                            <div>
                                <h3 class="font-semibold text-white">Phone</h3>
                                <p class="text-gray-400">+1 (780) 681-9765</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="glass-effect p-6 rounded-2xl">
                        <div class="flex items-center space-x-4">
                            <div class="w-12 h-12 bg-gradient-to-r from-green-500 to-teal-500 rounded-full flex items-center justify-center text-xl">
                                📍
                            </div>
                            <div>
                                <h3 class="font-semibold text-white">Location</h3>
                                <p class="text-gray-400">Salem</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="flex space-x-4">
                        <a href="#" class="w-12 h-12 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full flex items-center justify-cen        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .float-animation {
            animation: float 6s ease-in-out infinite;
        }
        
        .fade-in-up {
            animation: fadeInUp 0.8s ease-out forwards;
        }
        
        /* Hover effects */
        .hover-scale {
            transition: transform 0.3s ease;
        }
        
        .hover-scale:hover {
            transform: scale(1.05);
        }
        
        /* Progress bars */
        .progress-bar {
            height: 8px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 4px;
            overflow: hidden;
        }
        
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #667eea, #764ba2);
            border-radius: 4px;
            transition: width 2s ease-in-out;
        }
        
        /* Floating hire me button */
        .floating-btn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 1000;
            animation: float 3s ease-in-out infinite;
        }
        
        /* Dark mode styles */
        .dark {
            background: #0f0f23;
            color: white;
        }
        
        .light {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #333;
        }
        
        /* Theme colors */
        .theme-blue { --theme-color: #667eea; }
        .theme-purple { --theme-color: #764ba2; }
        .theme-green { --theme-color: #11998e; }
        
        /* Mobile responsiveness */
        @media (max-width: 768px) {
            .floating-btn {
                bottom: 20px;
                right: 20px;
            }
        }
    </style>
</head>
<body class="light transition-all duration-500">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full z-50 glass">
        <div class="container mx-auto px-6 py-4">
            <div class="flex justify-between items-center">
                <div class="text-2xl font-bold gradient-text">Abishek</div>
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="hover:text-purple-600 transition-colors">Home</a>
                    <a href="#about" class="hover:text-purple-600 transition-colors">About</a>
                    <a href="#projects" class="hover:text-purple-600 transition-colors">Projects</a>
                    <a href="#skills" class="hover:text-purple-600 transition-colors">Skills</a>
                    <a href="#resume" class="hover:text-purple-600 transition-colors">Resume</a>
                    <a href="#contact" class="hover:text-purple-600 transition-colors">Contact</a>
                </div>
                <div class="flex items-center space-x-4">
                    <!-- Theme Toggle -->
                    <button id="themeToggle" class="p-2 rounded-full glass hover-scale">
                        <i class="fas fa-moon"></i>
                    </button>
                    <!-- Color Theme Selector -->
                    <div class="flex space-x-2">
                        <button class="w-4 h-4 rounded-full bg-blue-500 theme-btn" data-theme="blue"></button>
                        <button class="w-4 h-4 rounded-full bg-purple-500 theme-btn" data-theme="purple"></button>
                        <button class="w-4 h-4 rounded-full bg-green-500 theme-btn" data-theme="green"></button>
                    </div>
                    <!-- Mobile menu button -->
                    <button id="mobileMenu" class="md:hidden p-2">
                        <i class="fas fa-bars"></i>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="min-h-screen flex items-center justify-center relative overflow-hidden">
        <div class="container mx-auto px-6 text-center">
            <div class="fade-in-up">
                <div class="w-32 h-32 mx-auto mb-8 rounded-full glass p-1 float-animation">
                    <div class="w-full h-full rounded-full gradient-bg flex items-center justify-center text-white text-4xl font-bold">
                        A
                    </div>
                </div>
                <h1 class="text-5xl md:text-7xl font-bold mb-6">
                    Hi, I'm <span class="gradient-text">Abishek</span>
                </h1>
                <p class="text-xl md:text-2xl mb-8 opacity-80">
                    Passionate about technology and creativity
                </p>
                <p class="text-lg mb-12 max-w-2xl mx-auto opacity-70">
                    Full-stack developer and designer crafting beautiful digital experiences with modern technologies
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <a href="#projects" class="px-8 py-4 gradient-bg text-white rounded-full hover-scale font-semibold">
                        View My Work
                    </a>
                    <a href="#contact" class="px-8 py-4 glass rounded-full hover-scale font-semibold">
                        Get In Touch
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-16 gradient-text">About Me</h2>
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="fade-in-up">
                    <div class="w-80 h-80 mx-auto rounded-2xl glass p-4">
                        <div class="w-full h-full rounded-xl gradient-bg flex items-center justify-center text-white text-6xl">
                            <i class="fas fa-user"></i>
                        </div>
                    </div>
                </div>
                <div class="fade-in-up">
                    <h3 class="text-2xl font-bold mb-6">Creative Developer & Designer</h3>
                    <p class="text-lg mb-6 opacity-80">
                        I'm a passionate full-stack developer with 3+ years of experience creating digital solutions that combine beautiful design with powerful functionality. I love turning complex problems into simple, elegant designs.
                    </p>
                    <div class="mb-6">
                        <h4 class="text-xl font-semibold mb-4">Education</h4>
                        <div class="glass p-4 rounded-lg">
                            <p class="font-semibold">Bachelor of Computer Science</p>
                            <p class="opacity-70">University of Technology • 2020-2024</p>
                        </div>
                    </div>
                    <div class="flex flex-wrap gap-3">
                        <span class="px-4 py-2 glass rounded-full text-sm">React</span>
                        <span class="px-4 py-2 glass rounded-full text-sm">Node.js</span>
                        <span class="px-4 py-2 glass rounded-full text-sm">Python</span>
                        <span class="px-4 py-2 glass rounded-full text-sm">UI/UX Design</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-16 gradient-text">Featured Projects</h2>
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1 -->
                <div class="glass rounded-2xl p-6 hover-scale fade-in-up">
                    <div class="w-full h-48 gradient-bg rounded-xl mb-6 flex items-center justify-center text-white text-4xl">
                        <i class="fas fa-shopping-cart"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">E-Commerce Platform</h3>
                    <p class="opacity-70 mb-4">Full-stack e-commerce solution with React, Node.js, and MongoDB. Features include user authentication, payment integration, and admin dashboard.</p>
                    <div class="flex gap-3 mb-4">
                        <span class="px-3 py-1 bg-blue-500 text-white rounded-full text-xs">React</span>
                        <span class="px-3 py-1 bg-green-500 text-white rounded-full text-xs">Node.js</span>
                        <span class="px-3 py-1 bg-purple-500 text-white rounded-full text-xs">MongoDB</span>
                    </div>
                    <div class="flex gap-4">
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fab fa-github mr-2"></i>Code
                        </a>
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fas fa-external-link-alt mr-2"></i>Live Demo
                        </a>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="glass rounded-2xl p-6 hover-scale fade-in-up">
                    <div class="w-full h-48 gradient-bg rounded-xl mb-6 flex items-center justify-center text-white text-4xl">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">Task Management App</h3>
                    <p class="opacity-70 mb-4">Mobile-first task management application with drag-and-drop functionality, real-time updates, and team collaboration features.</p>
                    <div class="flex gap-3 mb-4">
                        <span class="px-3 py-1 bg-blue-500 text-white rounded-full text-xs">React Native</span>
                        <span class="px-3 py-1 bg-yellow-500 text-white rounded-full text-xs">Firebase</span>
                        <span class="px-3 py-1 bg-red-500 text-white rounded-full text-xs">Redux</span>
                    </div>
                    <div class="flex gap-4">
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fab fa-github mr-2"></i>Code
                        </a>
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fas fa-external-link-alt mr-2"></i>Live Demo
                        </a>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="glass rounded-2xl p-6 hover-scale fade-in-up">
                    <div class="w-full h-48 gradient-bg rounded-xl mb-6 flex items-center justify-center text-white text-4xl">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">Analytics Dashboard</h3>
                    <p class="opacity-70 mb-4">Interactive data visualization dashboard with real-time charts, filtering capabilities, and export functionality using D3.js and Python.</p>
                    <div class="flex gap-3 mb-4">
                        <span class="px-3 py-1 bg-orange-500 text-white rounded-full text-xs">D3.js</span>
                        <span class="px-3 py-1 bg-blue-500 text-white rounded-full text-xs">Python</span>
                        <span class="px-3 py-1 bg-green-500 text-white rounded-full text-xs">Flask</span>
                    </div>
                    <div class="flex gap-4">
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fab fa-github mr-2"></i>Code
                        </a>
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fas fa-external-link-alt mr-2"></i>Live Demo
                        </a>
                    </div>
                </div>

                <!-- Project 4 -->
                <div class="glass rounded-2xl p-6 hover-scale fade-in-up">
                    <div class="w-full h-48 gradient-bg rounded-xl mb-6 flex items-center justify-center text-white text-4xl">
                        <i class="fas fa-brain"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">AI Chat Assistant</h3>
                    <p class="opacity-70 mb-4">Intelligent chatbot with natural language processing capabilities, built with Python and integrated with modern web technologies.</p>
                    <div class="flex gap-3 mb-4">
                        <span class="px-3 py-1 bg-purple-500 text-white rounded-full text-xs">Python</span>
                        <span class="px-3 py-1 bg-blue-500 text-white rounded-full text-xs">TensorFlow</span>
                        <span class="px-3 py-1 bg-green-500 text-white rounded-full text-xs">FastAPI</span>
                    </div>
                    <div class="flex gap-4">
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fab fa-github mr-2"></i>Code
                        </a>
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fas fa-external-link-alt mr-2"></i>Live Demo
                        </a>
                    </div>
                </div>

                <!-- Project 5 -->
                <div class="glass rounded-2xl p-6 hover-scale fade-in-up">
                    <div class="w-full h-48 gradient-bg rounded-xl mb-6 flex items-center justify-center text-white text-4xl">
                        <i class="fas fa-palette"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">Design System</h3>
                    <p class="opacity-70 mb-4">Comprehensive design system and component library with documentation, built for scalable web applications and consistent user experiences.</p>
                    <div class="flex gap-3 mb-4">
                        <span class="px-3 py-1 bg-pink-500 text-white rounded-full text-xs">Figma</span>
                        <span class="px-3 py-1 bg-blue-500 text-white rounded-full text-xs">Storybook</span>
                        <span class="px-3 py-1 bg-green-500 text-white rounded-full text-xs">CSS</span>
                    </div>
                    <div class="flex gap-4">
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fab fa-github mr-2"></i>Code
                        </a>
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fas fa-external-link-alt mr-2"></i>Live Demo
                        </a>
                    </div>
                </div>

                <!-- Project 6 -->
                <div class="glass rounded-2xl p-6 hover-scale fade-in-up">
                    <div class="w-full h-48 gradient-bg rounded-xl mb-6 flex items-center justify-center text-white text-4xl">
                        <i class="fas fa-gamepad"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3">Interactive Game</h3>
                    <p class="opacity-70 mb-4">Browser-based puzzle game with smooth animations, progressive difficulty levels, and local storage for game progress tracking.</p>
                    <div class="flex gap-3 mb-4">
                        <span class="px-3 py-1 bg-yellow-500 text-white rounded-full text-xs">JavaScript</span>
                        <span class="px-3 py-1 bg-red-500 text-white rounded-full text-xs">Canvas</span>
                        <span class="px-3 py-1 bg-blue-500 text-white rounded-full text-xs">CSS3</span>
                    </div>
                    <div class="flex gap-4">
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fab fa-github mr-2"></i>Code
                        </a>
                        <a href="#" target="_blank" rel="noopener noreferrer" class="text-purple-600 hover:text-purple-800">
                            <i class="fas fa-external-link-alt mr-2"></i>Live Demo
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center mb-16 gradient-text">Skills & Technologies</h2>
            <div class="grid md:grid-cols-2 gap-12">
                <div class="fade-in-up">
                    <h3 class="text-2xl font-bold mb-8">Technical Skills</h3>
                    <div class="space-y-6">
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-semibold">JavaScript / TypeScript</span>
                                <span class="text-sm opacity-70">90%</span>
                            </div>
                            <div class="progress-bar">
                                <div class="progress-fill" style="width: 90%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                      
