<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sayora | Kosmetik, Aksesoris & Kesehatan</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root {
            --primary: #820000;
            --secondary: #FFEEDC;
            --accent: #FF8D8D;
        }
        
        body {
            font-family: 'Poppins', system-ui, -apple-system, sans-serif;
            background-color: var(--secondary);
            color: var(--primary);
            overflow-x: hidden;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animate-fade {
            animation: fadeIn 0.8s ease forwards;
        }
        
        .delay-100 { animation-delay: 100ms; }
        .delay-200 { animation-delay: 200ms; }
        .delay-300 { animation-delay: 300ms; }
        
        /* Card hover effect */
        .social-card {
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .social-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(130, 0, 0, 0.2);
        }
        
        /* Button pulse effect */
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .btn-pulse:hover {
            animation: pulse 1.5s infinite;
        }
        
        /* 3D Animation for cosmetics */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .float-animate {
            animation: float 6s ease-in-out infinite;
        }
        
        /* Mobile menu toggle */
        #mobile-menu {
            transition: all 0.3s ease;
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            .hero-image {
                height: 300px;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="bg-white shadow-md fixed w-full z-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16 items-center">
                <div class="flex-shrink-0 flex items-center">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/5362609c-ad3d-4731-86ac-50c693ccf2d6.png" alt="BioLink logo in maroon color with link chain icon" class="h-8">
                    <span class="ml-2 text-xl font-bold text-var(--primary)" style="color: var(--primary);">Sayora</span>
                </div>
                
                <!-- Desktop Navigation -->
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="text-gray-700 hover:text-var(--primary) px-3 py-2 rounded-md text-sm font-medium transition-colors" style="color: var(--primary);">Home</a>
                    <a href="#features" class="text-gray-700 hover:text-var(--primary) px-3 py-2 rounded-md text-sm font-medium transition-colors" style="color: var(--primary);">Features</a>
                    <a href="#links" class="text-gray-700 hover:text-var(--primary) px-3 py-2 rounded-md text-sm font-medium transition-colors" style="color: var(--primary);">Links</a>
                    <a href="#contact" class="text-gray-700 hover:text-var(--primary) px-3 py-2 rounded-md text-sm font-medium transition-colors" style="color: var(--primary);">Contact</a>
                </div>
                
                <!-- Mobile menu button -->
                <div class="md:hidden">
                    <button id="menu-toggle" class="text-gray-700 hover:text-var(--primary) focus:outline-none" style="color: var(--primary);">
                        <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        
        <!-- Mobile Navigation -->
        <div id="mobile-menu" class="hidden md:hidden bg-white shadow-lg">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <a href="#home" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-100" style="color: var(--primary);">Home</a>
                <a href="#features" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-100" style="color: var(--primary);">Features</a>
                <a href="#links" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-100" style="color: var(--primary);">Links</a>
                <a href="#contact" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:bg-gray-100" style="color: var(--primary);">Contact</a>
            </div>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <section id="home" class="pt-24 pb-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
        <div class="flex flex-col md:flex-row items-center justify-between">
            <div class="md:w-1/2 animate-fade">
                <h1 class="text-4xl md:text-5xl font-bold mb-6" style="color: var(--primary);">Sayora <span class="underline decoration-var(--accent)" style="text-decoration-color: var(--accent);">Beauty</span> Collection</h1>
                <p class="text-lg mb-8 text-gray-700">Temukan kosmetik premium, aksesoris cantik dan produk kesehatan terbaik kami di marketplace favorit Anda.</p>
                <div class="flex flex-col sm:flex-row gap-4">
                    <a href="#links" class="btn-pulse bg-var(--primary) text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:opacity-90 transition-opacity" style="background-color: var(--primary);">Explore Links</a>
                    <a href="#features" class="bg-transparent border-2 border-var(--primary) text-var(--primary) font-bold py-3 px-6 rounded-lg hover:bg-var(--primary) hover:text-white transition-colors" style="border-color: var(--primary); color: var(--primary);">Learn More</a>
                </div>
            </div>
            <div class="md:w-1/2 mt-12 md:mt-0 animate-fade delay-100">
                <div class="relative float-animate">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/[NEW_3D_COSMETICS_IMAGE_ID]" alt="3D rendering of premium cosmetics products with holographic effects" class="rounded-xl shadow-2xl w-full max-w-md mx-auto transition-transform duration-1000 hover:scale-105">
                </div>
            </div>
        </div>
    </section>
    
    <!-- Features Section -->
    <section id="features" class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto bg-white rounded-3xl shadow-lg mt-12 animate-fade">
        <div class="text-center mb-12">
            <h2 class="text-3xl font-bold mb-4" style="color: var(--primary);">Produk Unggulan</h2>
            <p class="text-gray-600 max-w-2xl mx-auto">Koleksi lengkap kosmetik, aksesoris dan produk kesehatan berkualitas premium</p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="social-card bg-white p-6 rounded-xl border border-gray-100 transition-all delay-100">
                <div class="w-12 h-12 mb-4 rounded-full flex items-center justify-center" style="background-color: var(--accent);">
                    <i class="fas fa-bolt text-white text-xl"></i>
                </div>
                <h3 class="text-xl font-semibold mb-3" style="color: var(--primary);">Kosmetik Premium</h3>
                <p class="text-gray-600">Produk kecantikan dengan bahan berkualitas tinggi yang aman untuk kulit.</p>
            </div>
            
            <div class="social-card bg-white p-6 rounded-xl border border-gray-100 transition-all delay-200">
                <div class="w-12 h-12 mb-4 rounded-full flex items-center justify-center" style="background-color: var(--accent);">
                    <i class="fas fa-chart-line text-white text-xl"></i>
                </div>
                <h3 class="text-xl font-semibold mb-3" style="color: var(--primary);">Aksesoris Eksklusif</h3>
                <p class="text-gray-600">Pelengkap gaya dengan desain unik dan kualitas premium.</p>
            </div>
            
            <div class="social-card bg-white p-6 rounded-xl border border-gray-100 transition-all delay-300">
                <div class="w-12 h-12 mb-4 rounded-full flex items-center justify-center" style="background-color: var(--accent);">
                    <i class="fas fa-palette text-white text-xl"></i>
                </div>
                <h3 class="text-xl font-semibold mb-3" style="color: var(--primary);">Kesehatan & Perawatan</h3>
                <p class="text-gray-600">Produk perawatan tubuh dan kesehatan dengan formula terbaik.</p>
            </div>
        </div>
    </section>
    
    <!-- Social Links Section -->
    <section id="links" class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto mt-8">
        <div class="text-center mb-12">
            <h2 class="text-3xl font-bold mb-4" style="color: var(--primary);">Connect With Me</h2>
            <p class="text-gray-600 max-w-2xl mx-auto">One link to all my social media and marketplace profiles</p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Social Media Cards -->
            <a href="#" class="social-card animate-fade delay-100">
                <div class="bg-white p-6 rounded-xl flex items-center border border-gray-100">
                    <div class="w-16 h-16 rounded-full flex items-center justify-center mr-4" style="background-color: #3b5998;">
                        <i class="fab fa-facebook-f text-white text-2xl"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold" style="color: var(--primary);">Facebook</h3>
                        <p class="text-gray-600 text-sm">Connect with me on Facebook</p>
                    </div>
                </div>
            </a>
            
            <a href="#" class="social-card animate-fade delay-150">
                <div class="bg-white p-6 rounded-xl flex items-center border border-gray-100">
                    <div class="w-16 h-16 rounded-full flex items-center justify-center mr-4" style="background: linear-gradient(45deg, #405de6, #5851db, #833ab4, #c13584, #e1306c, #fd1d1d);">
                        <i class="fab fa-instagram text-white text-2xl"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold" style="color: var(--primary);">Instagram</h3>
                        <p class="text-gray-600 text-sm">Follow me on Instagram</p>
                    </div>
                </div>
            </a>
            
            <a href="#" class="social-card animate-fade delay-200">
                <div class="bg-white p-6 rounded-xl flex items-center border border-gray-100">
                    <div class="w-16 h-16 rounded-full flex items-center justify-center mr-4" style="background-color: #25D366;">
                        <i class="fab fa-whatsapp text-white text-2xl"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold" style="color: var(--primary);">WhatsApp</h3>
                        <p class="text-gray-600 text-sm">Chat with me on WhatsApp</p>
                    </div>
                </div>
            </a>
            
            <a href="#" class="social-card animate-fade delay-250">
                <div class="bg-white p-6 rounded-xl flex items-center border border-gray-100">
                    <div class="w-16 h-16 rounded-full flex items-center justify-center mr-4" style="background-color: #FF0050;">
                        <i class="fab fa-tiktok text-white text-2xl"></i>
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold" style="color: var(--primary);">TikTok</h3>
                        <p class="text-gray-600 text-sm">Follow my TikTok</p>
                    </div>
                </div>
            </a>
            
            <!-- Marketplace Cards -->
            <a href="#" class="social-card animate-fade delay-300">
                <div class="bg-white p-6 rounded-xl flex items-center border border-gray-100">
                    <div class="w-16 h-16 rounded-full flex items-center justify-center mr-4" style="background-color: #EE4D2D;">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/b7365925-0342-4c5a-9cc4-f00b10b5600e.png" alt="Shopee logo icon" class="w-8 h-8">
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold" style="color: var(--primary);">Shopee</h3>
                        <p class="text-gray-600 text-sm">Check out my Shopee store</p>
                    </div>
                </div>
            </a>
            
            <a href="#" class="social-card animate-fade delay-350">
                <div class="bg-white p-6 rounded-xl flex items-center border border-gray-100">
                    <div class="w-16 h-16 rounded-full flex items-center justify-center mr-4" style="background-color: #41B549;">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a1c18663-47a6-4542-839f-35da9f8c63c7.png" alt="Tokopedia logo icon" class="w-8 h-8">
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold" style="color: var(--primary);">Tokopedia</h3>
                        <p class="text-gray-600 text-sm">Visit my Tokopedia shop</p>
                    </div>
                </div>
            </a>
            
            <a href="#" class="social-card animate-fade delay-400">
                <div class="bg-white p-6 rounded-xl flex items-center border border-gray-100">
                    <div class="w-16 h-16 rounded-full flex items-center justify-center mr-4" style="background-color: #0C5ECB;">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/4edc2041-31f0-4987-aa96-06ca69d9591c.png" alt="Lazada logo icon" class="w-8 h-8">
                    </div>
                    <div>
                        <h3 class="text-lg font-semibold" style="color: var(--primary);">Lazada</h3>
                        <p class="text-gray-600 text-sm">Browse my Lazada products</p>
                    </div>
                </div>
            </a>
        </div>
    </section>
    
    <!-- CTA Section -->
    <section class="py-16 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto mt-8 bg-cover bg-center rounded-3xl overflow-hidden animate-fade" style="background-color: var(--primary);">
        <div class="bg-black bg-opacity-50 p-12 rounded-2xl backdrop-blur-sm">
            <div class="text-center text-white">
                <h2 class="text-3xl font-bold mb-4">Siap Belanja Produk Kami?</h2>
                <p class="text-lg mb-8 max-w-2xl mx-auto">Temukan koleksi lengkap produk kecantikan dan kesehatan di marketplace favorit Anda.</p>
                <a href="#links" class="inline-block bg-white text-var(--primary) font-bold py-3 px-8 rounded-lg shadow-lg hover:bg-opacity-90 transition-all" style="color: var(--primary);">Lihat Produk Kami</a>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer id="contact" class="bg-white py-12 px-4 sm:px-6 lg:px-8 border-t border-gray-200 mt-12 animate-fade">
        <div class="max-w-7xl mx-auto">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div class="md:col-span-2">
                    <h3 class="text-xl font-bold mb-4" style="color: var(--primary);">Sayora</h3>
                    <p class="text-gray-600">Produk kosmetik, aksesoris dan kesehatan berkualitas premium untuk gaya hidup terkini.</p>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4" style="color: var(--primary);">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-600 hover:text-var(--primary) transition-colors" style="color: var(--primary);">Pricing</a></li>
                        <li><a href="#" class="text-gray-600 hover:text-var(--primary) transition-colors" style="color: var(--primary);">Features</a></li>
                        <li><a href="#" class="text-gray-600 hover:text-var(--primary) transition-colors" style="color: var(--primary);">Support</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-lg font-semibold mb-4" style="color: var(--primary);">Contact</h4>
                    <ul class="space-y-2">
                        <li class="flex items-center text-gray-600">
                            <i class="fas fa-envelope mr-2" style="color: var(--accent);"></i>
                            contact@biolink.com
                        </li>
                        <li class="flex items-center text-gray-600">
                            <i class="fas fa-phone-alt mr-2" style="color: var(--accent);"></i>
                            +1 (123) 456-7890
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-200 mt-8 pt-8 text-center text-gray-500 text-sm">
                <p>© 2023 Sayora. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <!-- Scroll reveal animation -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Mobile menu toggle
            const menuToggle = document.getElementById('menu-toggle');
            const mobileMenu = document.getElementById('mobile-menu');
            
            menuToggle.addEventListener('click', function() {
                mobileMenu.classList.toggle('hidden');
            });
            
            // Scroll reveal animation
            const animateElements = document.querySelectorAll('.animate-fade');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, { threshold: 0.1 });
            
            animateElements.forEach(element => {
                element.style.opacity = 0;
                observer.observe(element);
            });
            
            // Smooth scrolling for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                        
                        // Close mobile menu if open
                        mobileMenu.classList.add('hidden');
                    }
                });
            });
        });
    </script>
</body>
</html>
