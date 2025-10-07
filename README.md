<meta name='viewport' content='width=device-width, initial-scale=1'/><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abishek - Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        body {
            box-sizing: border-box;
        }
        
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.1);
        }
        
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(45deg, #667eea, #764ba2);
            border-radius: 4px;
        }
        
        /* Smooth scroll */
        html {
            scroll-behavior: smooth;
        }
        
        /* Glassmorphism effect */
        .glass {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .dark .glass {
            background: rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Gradient backgrounds */
        .gradient-bg {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        /* Animations */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        @keyframes fadeInUp {
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
                      
