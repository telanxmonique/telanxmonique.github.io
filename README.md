<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telan, Monique - Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;900&display=swap" rel="stylesheet">
    <style>
        html {
            scroll-behavior: smooth;
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: #111827; /* Tailwind: bg-gray-900 */
            color: #E5E7EB; /* Tailwind: text-gray-200 */
        }
        .hero-section {
            background-color: #1F2937; /* Tailwind: bg-gray-800 */
        }
        .content-section {
            padding-top: 3rem; /* py-12 */
            padding-bottom: 3rem; /* py-12 */
        }
        @media (min-width: 640px) { /* sm breakpoint */
            .content-section {
                padding-top: 4rem; /* sm:py-16 */
                padding-bottom: 4rem; /* sm:py-16 */
            }
        }
        @media (min-width: 768px) { /* md breakpoint */
            .content-section {
                padding-top: 5rem; /* md:py-20 */
                padding-bottom: 5rem; /* md:py-20 */
            }
        }
        .contact-bar { /* This class seems unused if contact section uses .content-section */
            background-color: #374151; /* Tailwind: bg-gray-700 */
        }
        .logo-accent {
            color: #10B981; /* Tailwind: text-green-500 */
        }
        .cta-button {
            background-color: #10B981; /* Tailwind: bg-green-500 */
            transition: background-color 0.3s ease;
        }
        .cta-button:hover {
            background-color: #059669; /* Tailwind: hover:bg-green-600 */
        }
        .nav-link.active { /* Applied by JavaScript for scrollspy */
            color: #10B981; /* Tailwind: text-green-500 */
            font-weight: 600; /* Tailwind: font-semibold */
        }
        /* .nav-link:hover is handled by Tailwind: hover:text-green-400 directly on elements */

        .blinking-cursor::after {
            content: '|';
            animation: blink 1s step-start infinite;
        }
        @keyframes blink {
            50% {
                opacity: 0;
            }
        }
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #1F2937; /* bg-gray-800 */
        }
        ::-webkit-scrollbar-thumb {
            background: #10B981; /* bg-green-500 */
            border-radius: 4px; /* rounded */
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #059669; /* bg-green-600 */
        }
        .hero-image-container {
            position: relative;
        }
        .scroll-indicator {
            position: absolute;
            bottom: 2rem;
            right: 1rem;
            width: 24px;
            height: 40px;
            border: 2px solid #9CA3AF; /* border-gray-400 */
            border-radius: 12px; /* rounded-xl */
            display: flex; 
            justify-content: center;
            padding-top: 6px;
        }
         @media (min-width: 768px) { /* md breakpoint */
            .scroll-indicator {
                right: 2rem;
            }
        }
        .scroll-indicator-dot {
            width: 6px;
            height: 6px;
            background-color: #9CA3AF; /* bg-gray-400 */
            border-radius: 50%; /* rounded-full */
            animation: scroll-dot-animation 1.5s infinite ease-in-out;
        }
        @keyframes scroll-dot-animation {
            0% { opacity: 1; transform: translateY(0); }
            50% { opacity: 0.5; transform: translateY(8px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        .skill-item { /* For Tools & Languages section */
            background-color: #374151; /* bg-gray-700 */
            color: #D1D5DB; /* text-gray-300 */
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            border: 1px solid #4B5563; /* border-gray-600 */
            transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
        }
        .skill-item:hover {
            border-color: #10B981; /* border-green-500 */
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1), 0 0 0 4px rgba(16, 185, 129, 0.2);
        }
        /* Styling for project items - uses Tailwind directly in HTML */
    </style>
</head>
<body class="antialiased">

    <header class="py-4 md:py-6 sticky top-0 z-50 bg-gray-900/80 backdrop-blur-md shadow-lg">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 flex flex-wrap justify-between items-center">
            <a href="#home" class="text-2xl sm:text-3xl font-bold text-white whitespace-nowrap">My Portfolio<span class="logo-accent">.</span></a>
            
            <button id="mobile-menu-button" class="md:hidden p-2 rounded-md text-gray-300 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-green-500" aria-controls="mobile-menu" aria-expanded="false">
                <span class="sr-only">Open main menu</span>
                <svg class="block h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                </svg>
                <svg class="hidden h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                </svg>
            </button>

            <nav id="mobile-menu" class="hidden w-full md:flex md:w-auto md:items-center mt-2 md:mt-0">
                <ul class="flex flex-col md:flex-row md:space-x-4 lg:space-x-6 items-start md:items-center text-sm sm:text-base">
                    <li><a href="#home" class="nav-link block py-2 px-3 md:p-1 lg:p-2 text-gray-300 hover:text-green-400 transition-colors duration-300">Home</a></li>
                    <li><a href="#resume" class="nav-link block py-2 px-3 md:p-1 lg:p-2 text-gray-300 hover:text-green-400 transition-colors duration-300">Resume</a></li>
                    <li><a href="#skills" class="nav-link block py-2 px-3 md:p-1 lg:p-2 text-gray-300 hover:text-green-400 transition-colors duration-300">Skills</a></li>
                    <li><a href="#projects" class="nav-link block py-2 px-3 md:p-1 lg:p-2 text-gray-300 hover:text-green-400 transition-colors duration-300">Projects</a></li>
                    <li><a href="#tools" class="nav-link block py-2 px-3 md:p-1 lg:p-2 text-gray-300 hover:text-green-400 transition-colors duration-300">Tools & Languages</a></li>
                    <li><a href="#contact" class="nav-link block py-2 px-3 md:p-1 lg:p-2 text-gray-300 hover:text-green-400 transition-colors duration-300">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section id="home" class="hero-section relative min-h-screen flex items-center overflow-hidden py-10 sm:py-12 md:py-16">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid md:grid-cols-2 gap-8 items-center">
                    <div class="text-center md:text-left">
                        <p class="text-lg sm:text-xl md:text-2xl text-gray-400 mb-2 sm:mb-3">Hi There!</p>
                        <h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-extrabold text-white mb-3 sm:mb-4 leading-tight">
                            I'm Monique Telan<span id="cursor" class="blinking-cursor logo-accent"></span>
                        </h1>
                        <p class="text-lg sm:text-xl md:text-2xl text-gray-300 mb-6 sm:mb-8">
                            Software Developer | DevOps Enthusiast
                        </p>
                        <a href="#contact" class="cta-button text-white font-semibold py-3 px-6 sm:px-8 rounded-lg text-base sm:text-lg inline-block shadow-md hover:shadow-lg transform hover:scale-105">
                            Send me a message
                        </a>
                    </div>
                    <div class="hero-image-container block relative w-full mt-8 md:mt-0 h-64 sm:h-80 md:h-auto md:aspect-[4/5] min-h-[250px] sm:min-h-[300px] md:min-h-[400px] lg:min-h-[500px]">
                        <img src="Profile.jpg.jpg" alt="Developer Portrait" class="absolute inset-0 w-full h-full object-cover rounded-lg shadow-2xl opacity-70"
                             onerror="this.onerror=null;this.src='https://placehold.co/800x1000/2D3748/E2E8F0?text=Image+Error&font=inter';">
                        <div class="scroll-indicator flex"> <div class="scroll-indicator-dot"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="resume" class="content-section bg-gray-800">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-center mb-6 sm:mb-8 md:mb-12 text-white">My Resume</h2>
                <div class="text-center mb-8 sm:mb-10 md:mb-12">
                    <a href="CV-TELAN.pdf" download="CV-TELAN.pdf" class="cta-button text-white font-semibold py-3 px-6 sm:px-8 rounded-lg text-base sm:text-lg inline-block shadow-md hover:shadow-lg transform hover:scale-105 transition-all duration-300">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 inline-block mr-2 -mt-1" viewBox="0 0 20 20" fill="currentColor">
                            <path fill-rule="evenodd" d="M3 17a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm3.293-7.707a1 1 0 011.414 0L9 10.586V3a1 1 0 112 0v7.586l1.293-1.293a1 1 0 111.414 1.414l-3 3a1 1 0 01-1.414 0l-3-3a1 1 0 010-1.414z" clip-rule="evenodd" />
                        </svg>
                        Download CV-TELAN  (PDF)
                    </a>
                </div>
            </div>
        </section>

        <section id="skills" class="content-section bg-gray-700">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-center mb-6 sm:mb-8 md:mb-12 text-white">Skills</h2>
                <p class="text-center text-gray-400 mb-8 sm:mb-10 md:mb-12 max-w-2xl mx-auto text-sm sm:text-base md:text-lg">
                    In addition to the specific tools and languages I’m familiar with, I offer the following key competencies and methodologies.
                </p>
                <div class="grid md:grid-cols-2 gap-8 lg:gap-12 max-w-4xl mx-auto">
                    <div class="bg-gray-800 p-6 rounded-lg shadow-lg">
                        <h3 class="text-xl font-semibold text-green-400 text-center mb-4">Soft Skills</h3>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Effective Communication (Written & Verbal)</li>
                            <li>Problem-Solving & Analytical Thinking</li>
                            <li>Teamwork & Collaboration</li>
                            <li>Adaptability & Quick Learning</li>
                            <li>Attention to Detail</li>
                        </ul>
                    </div>
                    <div class="bg-gray-800 p-6 rounded-lg shadow-lg">
                        <h3 class="text-xl font-semibold text-green-400 text-center mb-4">Methodologies & Practices</h3>
                        <ul class="list-disc list-inside text-gray-300 space-y-2">
                            <li>Agile Development Principles</li>
                            <li>Scrum Framework</li>
                            <li>DevOps Culture & Collaboration</li>
                            <li>Version Control (Git) Workflows</li>
                            <li>Object-Oriented Design</li>
                            <li>Technical Documentation</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section id="projects" class="content-section bg-gray-800">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-center mb-6 sm:mb-8 md:mb-12 text-white">Projects</h2>
                <p class="text-center text-gray-400 mb-8 sm:mb-10 md:mb-12 max-w-2xl mx-auto text-sm sm:text-base md:text-lg">
Below are some of the projects I have worked on this year.                </p>
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <div class="project-item bg-gray-700 p-5 rounded-lg shadow-xl cursor-pointer transition-transform hover:scale-105"
                         data-project-name="Virtual Wallet Pictures"
                         data-project-description="A simple virtual wallet application that helps users deposit, withdraw, and transfer money from any device at their convenience."
                         data-images='[
                             "images/Proj1-sample1.png", 
                             "images/Proj1-sample2.png", 
                             "images/Proj1-sample3.png",
                             "images/Proj1-sample4.png",
                             "images/Proj1-sample5.png",
                             "images/Proj1-sample6.png",
                             "images/Proj1-sample7.png"]'>
                        <img src="images/Proj1-sample.png" alt="Virtual Wallet Thumbnail" class="w-full h-48 object-cover rounded-md mb-4">
                        <h3 class="text-xl font-semibold text-green-400 mb-2">Virtual Wallet Application</h3>
                        <p class="text-gray-300 text-sm">A simple virtual wallet application. Click to view 6 sample images.</p>
                    </div>

                    <div class="project-item bg-gray-700 p-5 rounded-lg shadow-xl cursor-pointer transition-transform hover:scale-105"
                         data-project-name="Ordering System Pictures"
                         data-project-description="A simple and user-friendly ordering system application that allows customers to browse products, place orders, and receive a digital receipt upon completion."
                         data-images='[
                             "images/Proj2-sample4.png", 
                             "images/Proj2-sample2.png",
                             "images/Proj2-sample3.png",
                             "images/Proj2-sample5.png",
                             "images/Proj2-sample6.png"
                         ]'>
                        <img src="images/Proj2-sample1.png" alt="Ordering System Thumbnail" class="w-full h-48 object-cover rounded-md mb-4">
                        <h3 class="text-xl font-semibold text-green-400 mb-2">Ordering System Application</h3>
                        <p class="text-gray-300 text-sm">A simple ordering system where users can browse food items, add them to cart, view  their orders and generate receipts.</p>
                    </div>

                    </div>
            </div>
        </section>

        <section id="tools" class="content-section bg-gray-700">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-center mb-6 sm:mb-8 md:mb-12 text-white">Tools & Languages</h2>
                <p class="text-center text-gray-400 mb-6 sm:mb-8 md:mb-10 max-w-2xl mx-auto text-sm sm:text-base md:text-lg">The following are the tools and programming languages I am proficient in.</p>
                <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-3 sm:gap-4 md:gap-6 text-center max-w-4xl mx-auto">
                    <div class="skill-item p-3 sm:p-4 md:p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="java.png" alt="Java Icon" class="w-12 h-12 sm:w-16 sm:h-16 md:w-20 md:h-20 mb-2 object-contain" onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=J&font=inter';">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold mt-1 sm:mt-2">Java</h3>
                    </div>
                    <div class="skill-item p-3 sm:p-4 md:p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="python.png" alt="Python Icon" class="w-12 h-12 sm:w-16 sm:h-16 md:w-20 md:h-20 mb-2 object-contain" onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=P&font=inter';">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold mt-1 sm:mt-2">Python</h3>
                    </div>
                    <div class="skill-item p-3 sm:p-4 md:p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="html.png" alt="HTML Icon" class="w-12 h-12 sm:w-16 sm:h-16 md:w-20 md:h-20 mb-2 object-contain" onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=H&font=inter';">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold mt-1 sm:mt-2">HTML</h3>
                    </div>
                    <div class="skill-item p-3 sm:p-4 md:p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="css.png.webp" alt="CSS Icon" class="w-12 h-12 sm:w-16 sm:h-16 md:w-20 md:h-20 mb-2 object-contain" onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=C&font=inter';">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold mt-1 sm:mt-2">CSS</h3>
                    </div>
                    <div class="skill-item p-3 sm:p-4 md:p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="linux.png" alt="Linux Icon" class="w-12 h-12 sm:w-16 sm:h-16 md:w-20 md:h-20 mb-2 object-contain" onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=L&font=inter';">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold mt-1 sm:mt-2">Linux</h3>
                    </div>
                    <div class="skill-item p-3 sm:p-4 md:p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="bash.png" alt="Bash Icon" class="w-12 h-12 sm:w-16 sm:h-16 md:w-20 md:h-20 mb-2 object-contain" onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=B&font=inter';">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold mt-1 sm:mt-2">Bash</h3>
                    </div>
                    <div class="skill-item p-3 sm:p-4 md:p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="git.jpg" alt="GIT Icon" class="w-12 h-12 sm:w-16 sm:h-16 md:w-20 md:h-20 mb-2 object-contain" onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=G&font=inter';">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold mt-1 sm:mt-2">GIT</h3>
                    </div>
                    <div class="skill-item p-3 sm:p-4 md:p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="mysql.jpg" alt="MySQL Icon" class="w-12 h-12 sm:w-16 sm:h-16 md:w-20 md:h-20 mb-2 object-contain" onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=S&font=inter';">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold mt-1 sm:mt-2">MySQL</h3>
                    </div>
                </div>
            </div>
        </section>

        <section id="contact" class="content-section bg-gray-800 py-10 sm:py-12 md:py-16">
            <div class="container mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-2xl sm:text-3xl md:text-4xl font-bold text-center mb-3 sm:mb-4 text-white">Contact Details</h2>
                <hr class="border-gray-600 w-1/2 sm:w-1/3 md:w-1/4 mx-auto mb-6 sm:mb-8 md:mb-12">
                <p class="text-base sm:text-lg text-center text-gray-300 mb-6 sm:mb-8 md:mb-12">
                    Feel free to reach out through any of the methods below.
                </p>
                <div class="grid md:grid-cols-3 gap-4 sm:gap-6 md:gap-8 text-center md:text-left">
                    <div class="contact-item bg-gray-700 p-4 sm:p-6 rounded-lg shadow-lg hover:bg-gray-600/80 transition-colors">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold text-green-400 uppercase tracking-wider mb-1 sm:mb-2">Email</h3>
                        <a href="mailto:nickotelan3@gmail.com" class="text-base sm:text-lg md:text-xl text-gray-200 hover:text-white transition-colors break-all">nickotelan3@gmail.com</a>
                    </div>
                    <div class="contact-item bg-gray-700 p-4 sm:p-6 rounded-lg shadow-lg hover:bg-gray-600/80 transition-colors">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold text-green-400 uppercase tracking-wider mb-1 sm:mb-2">Phone</h3>
                        <a href="tel:+639123924549" class="text-base sm:text-lg md:text-xl text-gray-200 hover:text-white transition-colors">+639123924549</a>
                    </div>
                    <div class="contact-item bg-gray-700 p-4 sm:p-6 rounded-lg shadow-lg hover:bg-gray-600/80 transition-colors">
                        <h3 class="text-sm sm:text-base md:text-lg font-semibold text-green-400 uppercase tracking-wider mb-1 sm:mb-2">Location</h3>
                        <p class="text-base sm:text-lg md:text-xl text-gray-200">Pembo, Taguig City</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="text-center py-6 sm:py-8 bg-gray-900">
        <p class="text-xs sm:text-sm md:text-base text-gray-500">&copy; <span id="currentYear"></span> Telan, Monique. All rights reserved.</p>
    </footer>

    <div id="image-lightbox" class="fixed inset-0 bg-black bg-opacity-80 flex items-center justify-center p-4 hidden z-[100]">
        <div class="bg-gray-800 p-4 sm:p-6 rounded-lg shadow-2xl w-full max-w-3xl max-h-[90vh] relative flex flex-col">
            <button id="lightbox-close" class="absolute top-3 right-3 text-gray-300 hover:text-white text-3xl leading-none font-bold z-10">&times;</button>
            
            <div class="flex-grow flex items-center justify-center overflow-hidden">
                <img id="lightbox-image" src="" alt="Lightbox Image" class="max-w-full max-h-[calc(90vh-150px)] sm:max-h-[calc(90vh-180px)] object-contain">
            </div>
            
            <div id="lightbox-caption" class="text-center text-gray-300 mt-3 text-sm break-words"></div>
            
            <div class="flex justify-between items-center mt-4">
                <button id="lightbox-prev" class="bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded transition-colors disabled:opacity-50 disabled:cursor-not-allowed">
                    Prev
                </button>
                <div id="lightbox-counter" class="text-gray-400 text-sm"></div>
                <button id="lightbox-next" class="bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded transition-colors disabled:opacity-50 disabled:cursor-not-allowed">
                    Next
                </button>
            </div>
        </div>
    </div>


    <script>
        document.addEventListener('DOMContentLoaded', function () {
            // --- Footer Current Year ---
            const currentYearEl = document.getElementById('currentYear');
            if (currentYearEl) {
                currentYearEl.textContent = new Date().getFullYear();
            }

            // --- Mobile Menu Toggle ---
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            const openIcon = mobileMenuButton ? mobileMenuButton.querySelector('svg:nth-child(1)') : null;
            const closeIcon = mobileMenuButton ? mobileMenuButton.querySelector('svg:nth-child(2)') : null;

            if (mobileMenuButton && mobileMenu && openIcon && closeIcon) {
                mobileMenuButton.addEventListener('click', () => {
                    console.log('Mobile menu button clicked.'); // For debugging
                    const isExpanded = mobileMenuButton.getAttribute('aria-expanded') === 'true' || false;
                    mobileMenuButton.setAttribute('aria-expanded', String(!isExpanded));
                    mobileMenu.classList.toggle('hidden');
                    openIcon.classList.toggle('hidden');
                    closeIcon.classList.toggle('hidden');
                });

                const mobileNavLinks = mobileMenu.querySelectorAll('ul li a');
                mobileNavLinks.forEach(link => {
                    link.addEventListener('click', () => {
                        if (!mobileMenu.classList.contains('hidden')) {
                            console.log('Mobile nav link clicked, closing menu.'); // For debugging
                            mobileMenuButton.setAttribute('aria-expanded', 'false');
                            mobileMenu.classList.add('hidden');
                            openIcon.classList.remove('hidden');
                            closeIcon.classList.add('hidden');
                        }
                    });
                });
            } else {
                console.error('Mobile menu button, mobile menu, or icons not found. Check IDs and structure if mobile menu is not working.');
            }
            
            // --- Scrollspy for Navigation Links ---
            const sections = document.querySelectorAll('section[id]');
            const allNavLinksForScrollSpy = document.querySelectorAll('header nav a[href^="#"]');

            if (sections.length > 0 && allNavLinksForScrollSpy.length > 0) {
                window.addEventListener('scroll', () => {
                    let currentSectionId = '';
                    sections.forEach(section => {
                        const sectionTop = section.offsetTop;
                        if (pageYOffset >= (sectionTop - 90)) { // 90 is an offset for the sticky header height
                            currentSectionId = section.getAttribute('id');
                        }
                    });

                    allNavLinksForScrollSpy.forEach(link => {
                        link.classList.remove('active'); // Custom class defined in <style>
                        const linkHref = link.getAttribute('href');
                        if (linkHref && linkHref.substring(1) === currentSectionId) {
                            link.classList.add('active');
                        }
                    });
                    
                    const homeLink = document.querySelector('header nav a[href="#home"]');
                    if (homeLink) {
                        if (!currentSectionId && pageYOffset < (sections[0] ? sections[0].offsetTop - 90 : 200) ) {
                            allNavLinksForScrollSpy.forEach(l => l.classList.remove('active'));
                            homeLink.classList.add('active');
                        } else if (!currentSectionId && sections.length === 0) { // Fallback if no sections
                             allNavLinksForScrollSpy.forEach(l => l.classList.remove('active'));
                            homeLink.classList.add('active');
                        }
                    }
                });
                // Trigger scroll event once on load to set initial active state
                window.dispatchEvent(new Event('scroll'));
            }


            // --- Lightbox Functionality ---
            const lightbox = document.getElementById('image-lightbox');
            const lightboxImage = document.getElementById('lightbox-image');
            const lightboxClose = document.getElementById('lightbox-close');
            const lightboxPrev = document.getElementById('lightbox-prev');
            const lightboxNext = document.getElementById('lightbox-next');
            const lightboxCaption = document.getElementById('lightbox-caption');
            const lightboxCounter = document.getElementById('lightbox-counter');
            const projectItems = document.querySelectorAll('.project-item');

            let currentProjectImages = [];
            let currentImageIndex = 0;
            let currentProjectNameForLightbox = ''; // To store project name for caption updates

            function openLightbox(images, index, projectName) {
                if (!lightbox) { console.error("Lightbox element not found."); return; }
                currentProjectImages = images;
                currentImageIndex = index;
                currentProjectNameForLightbox = projectName;
                updateLightboxDisplay();
                lightbox.classList.remove('hidden');
                document.body.style.overflow = 'hidden'; 
            }

            function closeLightbox() {
                if (!lightbox) return;
                lightbox.classList.add('hidden');
                currentProjectImages = [];
                document.body.style.overflow = 'auto';
            }

            function updateLightboxDisplay() {
                if (!lightboxImage || !currentProjectImages || currentProjectImages.length === 0) return;

                lightboxImage.src = currentProjectImages[currentImageIndex];
                
                if (lightboxCaption) {
                    lightboxCaption.textContent = `${currentProjectNameForLightbox}`; 
                }
                if (lightboxCounter) {
                    lightboxCounter.textContent = `${currentImageIndex + 1} / ${currentProjectImages.length}`;
                }

                if (lightboxPrev) lightboxPrev.disabled = currentImageIndex === 0;
                if (lightboxNext) lightboxNext.disabled = currentImageIndex === currentProjectImages.length - 1;
            }

            function showPrevImage() {
                if (currentImageIndex > 0) {
                    currentImageIndex--;
                    updateLightboxDisplay();
                }
            }

            function showNextImage() {
                if (currentImageIndex < currentProjectImages.length - 1) {
                    currentImageIndex++;
                    updateLightboxDisplay();
                }
            }

            if (projectItems.length > 0 && lightbox) {
                projectItems.forEach(item => {
                    item.addEventListener('click', () => {
                        const imagesString = item.dataset.images;
                        const projectName = item.dataset.projectName || 'Project Details';
                        
                        if (imagesString) {
                            try {
                                const images = JSON.parse(imagesString);
                                if (images && images.length > 0) {
                                    openLightbox(images, 0, projectName);
                                } else {
                                    console.warn('Project item has no images or invalid image data:', item.dataset.projectName);
                                }
                            } catch (e) {
                                console.error('Error parsing images JSON for project:', item.dataset.projectName, e, imagesString);
                            }
                        } else {
                            console.warn('Project item is missing data-images attribute:', item.dataset.projectName);
                        }
                    });
                });

                if (lightboxClose) lightboxClose.addEventListener('click', closeLightbox);
                if (lightboxPrev) lightboxPrev.addEventListener('click', showPrevImage);
                if (lightboxNext) lightboxNext.addEventListener('click', showNextImage);

                document.addEventListener('keydown', (event) => {
                    if (!lightbox.classList.contains('hidden')) {
                        if (event.key === 'Escape') closeLightbox();
                        if (event.key === 'ArrowLeft') showPrevImage();
                        if (event.key === 'ArrowRight') showNextImage();
                    }
                });

                lightbox.addEventListener('click', (event) => {
                    if (event.target === lightbox) closeLightbox();
                });
            } else {
                if (projectItems.length === 0) console.log("No '.project-item' elements found for lightbox.");
                if (!lightbox) console.log("Lightbox HTML structure with ID 'image-lightbox' not found.");
            }
        });
    </script>

</body>
</html>
