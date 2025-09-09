<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ateng Sani - Portal Digital Futuristik</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Inter:wght@300;400;500;600&display=swap');
        
        .font-futuristic { font-family: 'Orbitron', monospace; }
        .font-modern { font-family: 'Inter', sans-serif; }
        
        .glow {
            box-shadow: 0 0 20px rgba(59, 130, 246, 0.5);
        }
        
        .glow-green {
            box-shadow: 0 0 20px rgba(34, 197, 94, 0.5);
        }
        
        .glow-purple {
            box-shadow: 0 0 20px rgba(168, 85, 247, 0.5);
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        .pulse-slow {
            animation: pulse 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
        
        .gradient-text {
            background: linear-gradient(45deg, #3b82f6, #8b5cf6, #06d6a0);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .hologram {
            background: linear-gradient(45deg, rgba(59, 130, 246, 0.1), rgba(139, 92, 246, 0.1));
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .cyber-grid {
            background-image: 
                linear-gradient(rgba(59, 130, 246, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(59, 130, 246, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
        }
        
        .neon-border {
            border: 2px solid transparent;
            background: linear-gradient(45deg, #3b82f6, #8b5cf6) border-box;
            -webkit-mask: linear-gradient(#fff 0 0) padding-box, linear-gradient(#fff 0 0);
            -webkit-mask-composite: exclude;
        }
    </style>
</head>
<body class="bg-gray-900 text-white font-modern overflow-x-hidden">
    <!-- Animated Background -->
    <div class="fixed inset-0 cyber-grid opacity-20"></div>
    <div class="fixed inset-0 bg-gradient-to-br from-blue-900/20 via-purple-900/20 to-green-900/20"></div>
    
    <!-- Navigation -->
    <nav class="relative z-50 p-6">
        <div class="max-w-7xl mx-auto flex justify-between items-center">
            <div class="font-futuristic text-2xl font-bold gradient-text">
                ATENG SANI
            </div>
            <div class="hidden md:flex space-x-8">
                <button class="nav-btn hover:text-blue-400 transition-colors duration-300" onclick="scrollToSection('hero')">Home</button>
                <button class="nav-btn hover:text-blue-400 transition-colors duration-300" onclick="scrollToSection('about')">About</button>
                <button class="nav-btn hover:text-blue-400 transition-colors duration-300" onclick="scrollToSection('projects')">Projects</button>
                <button class="nav-btn hover:text-blue-400 transition-colors duration-300" onclick="scrollToSection('contact')">Contact</button>
            </div>
            <button class="md:hidden text-2xl" onclick="toggleMobileMenu()">☰</button>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobileMenu" class="hidden md:hidden mt-4 hologram rounded-lg p-4">
            <button class="block w-full text-left py-2 hover:text-blue-400" onclick="scrollToSection('hero')">Home</button>
            <button class="block w-full text-left py-2 hover:text-blue-400" onclick="scrollToSection('about')">About</button>
            <button class="block w-full text-left py-2 hover:text-blue-400" onclick="scrollToSection('projects')">Projects</button>
            <button class="block w-full text-left py-2 hover:text-blue-400" onclick="scrollToSection('contact')">Contact</button>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="hero" class="relative min-h-screen flex items-center justify-center px-6">
        <div class="text-center max-w-4xl mx-auto">
            <div class="floating">
                <h1 class="font-futuristic text-6xl md:text-8xl font-black mb-6 gradient-text">
                    DIGITAL FUTURE
                </h1>
            </div>
            <p class="text-xl md:text-2xl mb-8 text-gray-300 font-light">
                Menjelajahi teknologi masa depan dengan kreativitas dan inovasi
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <button class="hologram px-8 py-4 rounded-full font-semibold hover:glow transition-all duration-300 transform hover:scale-105" onclick="scrollToSection('projects')">
                    Jelajahi Proyek
                </button>
                <button class="bg-gradient-to-r from-blue-600 to-purple-600 px-8 py-4 rounded-full font-semibold hover:glow-purple transition-all duration-300 transform hover:scale-105" onclick="scrollToSection('about')">
                    Tentang Saya
                </button>
            </div>
        </div>
        
        <!-- Floating Elements -->
        <div class="absolute top-20 left-10 w-20 h-20 bg-blue-500/20 rounded-full blur-xl floating"></div>
        <div class="absolute bottom-20 right-10 w-32 h-32 bg-purple-500/20 rounded-full blur-xl floating" style="animation-delay: -2s;"></div>
        <div class="absolute top-1/2 left-20 w-16 h-16 bg-green-500/20 rounded-full blur-xl floating" style="animation-delay: -4s;"></div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-6">
        <div class="max-w-6xl mx-auto">
            <h2 class="font-futuristic text-4xl md:text-6xl font-bold text-center mb-16 gradient-text">
                TENTANG SAYA
            </h2>
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="hologram p-8 rounded-2xl">
                    <h3 class="font-futuristic text-2xl font-bold mb-4 text-blue-400">Digital Creator</h3>
                    <p class="text-gray-300 leading-relaxed mb-6">
                        Saya adalah seorang kreator digital yang berfokus pada pengembangan teknologi futuristik dan solusi inovatif. Dengan pengalaman dalam berbagai bidang teknologi, saya menciptakan konten yang menginspirasi dan mendidik.
                    </p>
                    <div class="flex flex-wrap gap-3">
                        <span class="px-4 py-2 bg-blue-600/30 rounded-full text-sm">Web Development</span>
                        <span class="px-4 py-2 bg-purple-600/30 rounded-full text-sm">UI/UX Design</span>
                        <span class="px-4 py-2 bg-green-600/30 rounded-full text-sm">Innovation</span>
                    </div>
                </div>
                <div class="relative">
                    <div class="w-80 h-80 mx-auto bg-gradient-to-br from-blue-600 to-purple-600 rounded-full flex items-center justify-center text-8xl pulse-slow">
                        🚀
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 px-6">
        <div class="max-w-6xl mx-auto">
            <h2 class="font-futuristic text-4xl md:text-6xl font-bold text-center mb-16 gradient-text">
                PROYEK FUTURISTIK
            </h2>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="project-card hologram p-6 rounded-2xl cursor-pointer transform transition-all duration-300 hover:scale-105 hover:glow" onclick="openProject('ai')">
                    <div class="text-4xl mb-4">🤖</div>
                    <h3 class="font-futuristic text-xl font-bold mb-3 text-blue-400">AI Assistant</h3>
                    <p class="text-gray-300 text-sm">Asisten AI cerdas untuk membantu produktivitas sehari-hari</p>
                </div>
                <div class="project-card hologram p-6 rounded-2xl cursor-pointer transform transition-all duration-300 hover:scale-105 hover:glow-green" onclick="openProject('vr')">
                    <div class="text-4xl mb-4">🥽</div>
                    <h3 class="font-futuristic text-xl font-bold mb-3 text-green-400">VR Experience</h3>
                    <p class="text-gray-300 text-sm">Pengalaman virtual reality yang imersif dan interaktif</p>
                </div>
                <div class="project-card hologram p-6 rounded-2xl cursor-pointer transform transition-all duration-300 hover:scale-105 hover:glow-purple" onclick="openProject('blockchain')">
                    <div class="text-4xl mb-4">⛓️</div>
                    <h3 class="font-futuristic text-xl font-bold mb-3 text-purple-400">Blockchain App</h3>
                    <p class="text-gray-300 text-sm">Aplikasi blockchain untuk keamanan data masa depan</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Interactive Stats -->
    <section class="py-20 px-6">
        <div class="max-w-4xl mx-auto">
            <div class="grid md:grid-cols-3 gap-8 text-center">
                <div class="hologram p-8 rounded-2xl">
                    <div class="font-futuristic text-4xl font-bold gradient-text counter" data-target="50">0</div>
                    <p class="text-gray-300 mt-2">Proyek Selesai</p>
                </div>
                <div class="hologram p-8 rounded-2xl">
                    <div class="font-futuristic text-4xl font-bold gradient-text counter" data-target="1000">0</div>
                    <p class="text-gray-300 mt-2">Jam Coding</p>
                </div>
                <div class="hologram p-8 rounded-2xl">
                    <div class="font-futuristic text-4xl font-bold gradient-text counter" data-target="25">0</div>
                    <p class="text-gray-300 mt-2">Teknologi Dikuasai</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20 px-6">
        <div class="max-w-4xl mx-auto text-center">
            <h2 class="font-futuristic text-4xl md:text-6xl font-bold mb-8 gradient-text">
                HUBUNGI SAYA
            </h2>
            <p class="text-xl text-gray-300 mb-12">
                Mari berkolaborasi untuk menciptakan masa depan digital yang luar biasa
            </p>
            <div class="flex flex-col sm:flex-row gap-6 justify-center">
                <button class="hologram px-8 py-4 rounded-full font-semibold hover:glow transition-all duration-300 transform hover:scale-105" onclick="openContact('email')">
                    📧 Email
                </button>
                <button class="hologram px-8 py-4 rounded-full font-semibold hover:glow-green transition-all duration-300 transform hover:scale-105" onclick="openContact('whatsapp')">
                    💬 WhatsApp
                </button>
                <button class="hologram px-8 py-4 rounded-full font-semibold hover:glow-purple transition-all duration-300 transform hover:scale-105" onclick="openContact('linkedin')">
                    💼 LinkedIn
                </button>
            </div>
        </div>
    </section>

    <!-- Modal -->
    <div id="modal" class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden flex items-center justify-center p-6">
        <div class="hologram max-w-md w-full p-8 rounded-2xl relative">
            <button class="absolute top-4 right-4 text-2xl hover:text-red-400 transition-colors" onclick="closeModal()">×</button>
            <div id="modalContent"></div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="py-12 px-6 border-t border-gray-800">
        <div class="max-w-6xl mx-auto text-center">
            <div class="font-futuristic text-2xl font-bold gradient-text mb-4">ATENG SANI</div>
            <p class="text-gray-400">© 2024 Digital Future Portal. Semua hak dilindungi.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        function scrollToSection(sectionId) {
            document.getElementById(sectionId).scrollIntoView({
                behavior: 'smooth'
            });
            // Close mobile menu if open
            document.getElementById('mobileMenu').classList.add('hidden');
        }

        // Mobile menu toggle
        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        // Counter animation
        function animateCounters() {
            const counters = document.querySelectorAll('.counter');
            counters.forEach(counter => {
                const target = parseInt(counter.getAttribute('data-target'));
                const increment = target / 100;
                let current = 0;
                
                const updateCounter = () => {
                    if (current < target) {
                        current += increment;
                        counter.textContent = Math.ceil(current);
                        requestAnimationFrame(updateCounter);
                    } else {
                        counter.textContent = target;
                    }
                };
                updateCounter();
            });
        }

        // Project modal
        function openProject(type) {
            const modal = document.getElementById('modal');
            const content = document.getElementById('modalContent');
            
            const projects = {
                ai: {
                    title: '🤖 AI Assistant',
                    description: 'Asisten AI yang dapat membantu Anda dalam berbagai tugas sehari-hari dengan teknologi machine learning terdepan.',
                    features: ['Natural Language Processing', 'Voice Recognition', 'Smart Automation']
                },
                vr: {
                    title: '🥽 VR Experience',
                    description: 'Pengalaman virtual reality yang memungkinkan Anda menjelajahi dunia digital dengan cara yang belum pernah ada sebelumnya.',
                    features: ['Immersive 3D Environment', 'Hand Tracking', 'Spatial Audio']
                },
                blockchain: {
                    title: '⛓️ Blockchain App',
                    description: 'Aplikasi blockchain yang menyediakan keamanan data tingkat enterprise dengan teknologi terdesentralisasi.',
                    features: ['Smart Contracts', 'Decentralized Storage', 'Crypto Integration']
                }
            };
            
            const project = projects[type];
            content.innerHTML = `
                <h3 class="font-futuristic text-2xl font-bold mb-4 gradient-text">${project.title}</h3>
                <p class="text-gray-300 mb-6">${project.description}</p>
                <h4 class="font-semibold mb-3 text-blue-400">Fitur Utama:</h4>
                <ul class="space-y-2 mb-6">
                    ${project.features.map(feature => `<li class="text-gray-300">• ${feature}</li>`).join('')}
                </ul>
                <button class="w-full bg-gradient-to-r from-blue-600 to-purple-600 py-3 rounded-full font-semibold hover:glow-purple transition-all duration-300">
                    Pelajari Lebih Lanjut
                </button>
            `;
            modal.classList.remove('hidden');
        }

        // Contact modal
        function openContact(type) {
            const modal = document.getElementById('modal');
            const content = document.getElementById('modalContent');
            
            const contacts = {
                email: {
                    title: '📧 Email',
                    description: 'Kirim email untuk diskusi proyek atau kolaborasi',
                    action: 'hello@atengsani.com'
                },
                whatsapp: {
                    title: '💬 WhatsApp',
                    description: 'Chat langsung untuk konsultasi cepat',
                    action: '+62 812-3456-7890'
                },
                linkedin: {
                    title: '💼 LinkedIn',
                    description: 'Terhubung untuk networking profesional',
                    action: 'linkedin.com/in/atengsani'
                }
            };
            
            const contact = contacts[type];
            content.innerHTML = `
                <h3 class="font-futuristic text-2xl font-bold mb-4 gradient-text">${contact.title}</h3>
                <p class="text-gray-300 mb-6">${contact.description}</p>
                <div class="bg-gray-800 p-4 rounded-lg mb-6">
                    <code class="text-blue-400">${contact.action}</code>
                </div>
                <button class="w-full bg-gradient-to-r from-green-600 to-blue-600 py-3 rounded-full font-semibold hover:glow-green transition-all duration-300">
                    Hubungi Sekarang
                </button>
            `;
            modal.classList.remove('hidden');
        }

        // Close modal
        function closeModal() {
            document.getElementById('modal').classList.add('hidden');
        }

        // Initialize animations on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting && entry.target.querySelector('.counter')) {
                    animateCounters();
                }
            });
        });

        // Observe stats section
        document.addEventListener('DOMContentLoaded', () => {
            const statsSection = document.querySelector('.counter').closest('section');
            observer.observe(statsSection);
        });

        // Close modal when clicking outside
        document.getElementById('modal').addEventListener('click', (e) => {
            if (e.target.id === 'modal') {
                closeModal();
            }
        });
    </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'97c37e4627528de9',t:'MTc1NzM4NzQzNC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
