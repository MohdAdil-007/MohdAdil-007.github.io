<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mohammed Adil | Portfolio</title>
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Lucide Icons CDN -->
  <script src="https://unpkg.com/lucide@latest"></script>

  <!-- Custom configuration for Tailwind to match the Sikura Theme -->
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
          },
          colors: {
            brand: {
              orange: '#F35B30', 
              orangeHover: '#d94c26',
              dark: '#121212',   
              darker: '#0a0a0a',
              cardLight: '#F3F7FA', 
              pillLight: '#E2F1FD', 
            }
          }
        }
      }
    }
  </script>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
    
    body {
      font-family: 'Inter', sans-serif;
    }
    
    /* Custom Scrollbar */
    ::-webkit-scrollbar { width: 8px; }
    ::-webkit-scrollbar-track { background: #121212; }
    ::-webkit-scrollbar-thumb { background: #333; border-radius: 4px; }
    ::-webkit-scrollbar-thumb:hover { background: #F35B30; }

    /* Page Transition Animation */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .animate-fadeIn {
      animation: fadeIn 0.4s ease-out forwards;
    }
  </style>
</head>
<body class="bg-brand-dark text-white min-h-screen flex flex-col selection:bg-brand-orange selection:text-white">

  <!-- Navbar (Dark) -->
  <nav id="navbar" class="fixed w-full z-50 transition-all duration-300 bg-brand-dark py-4 border-b border-gray-800">
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center">
      
      <!-- Sikura-style Logo -->
      <a onclick="navigateTo('home')" class="flex items-center gap-2 group cursor-pointer">
        <div class="flex items-center gap-0.5">
          <div class="w-4 h-4 rounded-full bg-white transition-transform group-hover:scale-110"></div>
          <div class="w-4 h-4 rounded-sm bg-white transition-transform group-hover:scale-110"></div>
        </div>
        <span class="text-xl font-bold tracking-[0.2em] text-white">ADIL</span>
      </a>

      <!-- Desktop Nav -->
      <div class="hidden md:flex space-x-8 items-center text-xs font-semibold tracking-widest text-gray-300">
        <button onclick="navigateTo('home')" class="nav-link text-white transition-colors uppercase tracking-widest" data-target="home">HOME</button>
        <button onclick="navigateTo('skills')" class="nav-link hover:text-white transition-colors uppercase tracking-widest" data-target="skills">SKILLS</button>
        <button onclick="navigateTo('experience')" class="nav-link hover:text-white transition-colors uppercase tracking-widest" data-target="experience">EXPERIENCE</button>
        <button onclick="navigateTo('education')" class="nav-link hover:text-white transition-colors uppercase tracking-widest" data-target="education">EDUCATION</button>
        <button onclick="navigateTo('projects')" class="nav-link hover:text-white transition-colors uppercase tracking-widest" data-target="projects">PROJECTS</button>
      </div>

      <!-- CTA Button -->
      <div class="hidden md:block">
        <a href="mailto:adilvpalain@gmail.com" class="bg-brand-orange hover:bg-brand-orangeHover text-white text-xs font-bold tracking-wider px-6 py-3 rounded transition-colors">
          CONTACT
        </a>
      </div>

      <!-- Mobile Menu Toggle -->
      <button id="menu-toggle" class="md:hidden text-gray-300 hover:text-white transition-colors">
        <i data-lucide="menu" id="menu-icon" class="w-6 h-6"></i>
      </button>
    </div>

    <!-- Mobile Nav (Hidden by default) -->
    <div id="mobile-menu" class="hidden absolute top-full left-0 w-full bg-brand-dark border-b border-gray-800 flex flex-col text-sm font-semibold tracking-widest text-gray-300 shadow-xl">
      <button onclick="navigateTo('home')" class="mobile-nav-link px-6 py-4 border-b border-gray-800 text-white bg-gray-900 text-left" data-target="home">HOME</button>
      <button onclick="navigateTo('skills')" class="mobile-nav-link px-6 py-4 border-b border-gray-800 hover:text-white hover:bg-gray-900 text-left" data-target="skills">SKILLS</button>
      <button onclick="navigateTo('experience')" class="mobile-nav-link px-6 py-4 border-b border-gray-800 hover:text-white hover:bg-gray-900 text-left" data-target="experience">EXPERIENCE</button>
      <button onclick="navigateTo('education')" class="mobile-nav-link px-6 py-4 border-b border-gray-800 hover:text-white hover:bg-gray-900 text-left" data-target="education">EDUCATION</button>
      <button onclick="navigateTo('projects')" class="mobile-nav-link px-6 py-4 border-b border-gray-800 hover:text-white hover:bg-gray-900 text-left" data-target="projects">PROJECTS</button>
      <a href="mailto:adilvpalain@gmail.com" class="px-6 py-4 text-brand-orange hover:bg-gray-900 text-left block">CONTACT</a>
    </div>
  </nav>

  <!-- Main Content Area -->
  <main class="flex-grow pt-20 flex flex-col">
    
    <!-- HOME PAGE -->
    <section id="home" class="page-section flex-grow relative flex flex-col items-center justify-center min-h-[80vh] text-center px-6 bg-gradient-to-b from-brand-dark to-[#1a1c23] animate-fadeIn">
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] bg-brand-orange/5 rounded-full blur-[100px] pointer-events-none"></div>

      <div class="relative z-10 max-w-4xl mx-auto mt-8 flex flex-col items-center">
        
        <div class="inline-flex items-center gap-2 px-5 py-2 rounded-full border border-gray-700/60 bg-gray-800/30 text-gray-300 text-sm font-medium mb-8 backdrop-blur-sm">
          <i data-lucide="terminal" class="w-4 h-4 text-brand-orange"></i> AI Developer & Linux Enthusiast
        </div>
        
        <h1 class="text-4xl md:text-6xl lg:text-7xl font-extrabold tracking-tight text-white mb-6 leading-tight">
          Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand-orange to-red-400">Mohammed Adil</span>
        </h1>
        
        <p class="text-base md:text-lg text-gray-400 max-w-2xl mx-auto mb-10 leading-relaxed">
          A Computer Science engineering student passionate about AI-powered solutions, robust software engineering, and Linux system administration. Proven ability to lead teams, deliver under pressure, and develop scalable applications.
        </p>
        
        <div class="flex items-center justify-center gap-4 flex-col sm:flex-row w-full">
          <button onclick="navigateTo('projects')" class="w-full sm:w-auto bg-brand-orange hover:bg-brand-orangeHover text-white text-sm font-semibold px-8 py-3.5 rounded-lg transition-all shadow-lg flex items-center justify-center gap-2">
            View My Work <i data-lucide="chevron-right" class="w-4 h-4"></i>
          </button>
          <a href="https://drive.google.com/file/d/1QQuLBuR14LzBrt0GILUmoQpb0C7vsA5M/view?usp=drive_link" target="_blank" rel="noopener noreferrer" class="w-full sm:w-auto border border-gray-700 hover:border-gray-500 hover:bg-gray-800 text-white text-sm font-semibold px-8 py-3.5 rounded-lg transition-all flex items-center justify-center gap-2">
            <i data-lucide="download" class="w-4 h-4 text-gray-400"></i> Resume
          </a>
        </div>

      </div>
    </section>

    <!-- SKILLS PAGE -->
    <section id="skills" class="page-section hidden flex-grow bg-white text-gray-900 py-16 px-6">
      <div class="max-w-6xl mx-auto flex flex-col items-center">
        
        <div class="bg-brand-pillLight text-[#0A2540] text-xs font-semibold px-4 py-1.5 rounded-lg mb-8 tracking-wide uppercase">
          Technical Stack
        </div>

        <h2 class="text-3xl md:text-4xl font-bold tracking-tight mb-4 text-center">
          <span class="text-gray-900">CORE</span> <span class="text-gray-400">SKILLS</span>
        </h2>
        <p class="text-gray-500 max-w-xl text-center mb-12 text-base">
          A comprehensive overview of my technical capabilities across systems administration, software development, and artificial intelligence.
        </p>

        <div class="grid md:grid-cols-2 gap-6 w-full max-w-4xl">
          
          <div class="bg-[#111111] text-white p-8 rounded-xl flex flex-col h-[280px] group relative overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-t from-black/80 to-transparent z-10 pointer-events-none"></div>
            <div class="absolute bottom-0 right-0 opacity-10 transform translate-x-1/4 translate-y-1/4 group-hover:scale-110 transition-transform duration-700">
              <i data-lucide="terminal" class="w-48 h-48"></i>
            </div>

            <div class="relative z-20">
              <h3 class="text-xl md:text-2xl font-semibold mb-3 tracking-tight">Linux & Systems</h3>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed mb-6">
                Proficient in managing complex Red Hat Enterprise Linux servers, DBMS, and engineering secure routing protocols.
              </p>
            </div>
            <div class="relative z-20 mt-auto flex flex-wrap gap-2">
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">RHEL</span>
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">Bash</span>
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">DBMS</span>
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">Git</span>
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">SQL</span>
            </div>
          </div>

          <div class="bg-[#111111] text-white p-8 rounded-xl flex flex-col h-[280px] group relative overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-t from-black/80 to-transparent z-10 pointer-events-none"></div>
            <div class="absolute bottom-0 right-0 opacity-10 transform translate-x-1/4 translate-y-1/4 group-hover:scale-110 transition-transform duration-700">
              <i data-lucide="cpu" class="w-48 h-48"></i>
            </div>

            <div class="relative z-20">
              <h3 class="text-xl md:text-2xl font-semibold mb-3 tracking-tight">AI & Development</h3>
              <p class="text-gray-400 text-sm md:text-base leading-relaxed mb-6">
                Developing intelligent biometric tools. Coupling computer vision with deep learning inference for real-time analytics.
              </p>
            </div>
            <div class="relative z-20 mt-auto flex flex-wrap gap-2">
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">Python</span>
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">TensorFlow</span>
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">OpenCV</span>
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">Java</span>
              <span class="px-2.5 py-1 bg-gray-800 border border-gray-700 rounded text-xs font-medium">Tailwind</span>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- EXPERIENCE PAGE -->
    <section id="experience" class="page-section hidden flex-grow bg-white text-gray-900 py-16 px-6">
      <div class="max-w-6xl mx-auto flex flex-col items-center">
        
        <div class="mb-12 text-center">
          <h2 class="text-3xl md:text-4xl font-bold tracking-tight mb-4">
            <span class="text-gray-900">PROFESSIONAL</span> <a href="https://drive.google.com/file/d/1xuIvuPNqmPaA2eGZQfP18mJDeQqVImZX/view?usp=drive_link" target="_blank" rel="noopener noreferrer" class="text-gray-500 hover:text-brand-orange transition-colors">EXPERIENCE</a>
          </h2>
          <p class="text-gray-500 text-base">
            My organizational leadership roles and professional work history.
          </p>
        </div>

        <div class="grid md:grid-cols-2 gap-6 w-full max-w-5xl">
          
          <div class="bg-brand-cardLight rounded-xl p-6 relative shadow-sm border border-gray-100 flex flex-col">
            <div class="bg-brand-orange text-white w-10 h-10 flex items-center justify-center rounded-lg mb-6 shadow-sm">
              <i data-lucide="briefcase" class="w-5 h-5"></i>
            </div>
            <h3 class="text-lg md:text-xl font-bold text-gray-900 mb-1 leading-tight">
              Senior Manager (Outgoing Social Sector)
            </h3>
            <p class="text-sm font-semibold text-gray-700 mb-1">AIESEC</p>
            <p class="text-xs font-semibold tracking-wider text-brand-orange mb-4 uppercase">Feb 2024 - Jan 2025</p>
            <p class="text-gray-600 text-sm leading-relaxed mt-auto">
              Undertook a leadership role in the volunteering department. Managed a team to meet target deadlines and gained hands-on experience collaborating with multiple departments to achieve overarching organizational targets.
            </p>
          </div>

          <div class="bg-brand-cardLight rounded-xl p-6 relative shadow-sm border border-gray-100 flex flex-col">
            <div class="bg-brand-orange text-white w-10 h-10 flex items-center justify-center rounded-lg mb-6 shadow-sm">
              <i data-lucide="briefcase" class="w-5 h-5"></i>
            </div>
            <h3 class="text-lg md:text-xl font-bold text-gray-900 mb-1 leading-tight">
              Junior Manager (Outgoing Social Sector)
            </h3>
            <p class="text-sm font-semibold text-gray-700 mb-1">AIESEC</p>
            <p class="text-xs font-semibold tracking-wider text-brand-orange mb-4 uppercase">Aug 2023 - Jan 2024</p>
            <p class="text-gray-600 text-sm leading-relaxed mt-auto">
              Developed vital professional skills including cold calling, sales, and working under pressure. Conducted multiple successful marketing campaigns within universities to drive social sector initiatives.
            </p>
          </div>

        </div>
      </div>
    </section>

    <!-- EDUCATION PAGE -->
    <section id="education" class="page-section hidden flex-grow bg-white text-gray-900 py-16 px-6">
      <div class="max-w-6xl mx-auto flex flex-col items-center">
        
        <div class="mb-12 text-center">
          <h2 class="text-3xl md:text-4xl font-bold tracking-tight mb-4">
            <span class="text-gray-900">EDUCATION &</span> <a href="https://drive.google.com/drive/folders/15yJTFOJsje-R-Uq5DM2ZHbYaH4mpT91p?usp=sharing" target="_blank" rel="noopener noreferrer" class="text-gray-500 hover:text-brand-orange transition-colors">CERTIFICATIONS</a>
          </h2>
          <p class="text-gray-500 text-base">
            My academic background, technical training, and key achievements.
          </p>
        </div>

        <div class="grid md:grid-cols-2 gap-10 w-full max-w-5xl">
          
          <!-- Education Column -->
          <div class="space-y-6">
            <h3 class="text-xl font-bold text-gray-900 border-b border-gray-200 pb-2 mb-4">Academic Background</h3>
            
            <div class="bg-brand-cardLight rounded-xl p-6 relative shadow-sm border border-gray-100">
              <h4 class="text-lg font-bold text-gray-900 mb-1 leading-tight">B.Tech Computer Science</h4>
              <p class="text-sm font-semibold text-gray-700 mb-1">Lovely Professional University | Punjab, India</p>
              <p class="text-xs font-semibold tracking-wider text-brand-orange mb-3 uppercase">Since Aug 2023</p>
              <p class="text-gray-600 text-sm">CGPA: 6.6</p>
            </div>

            <div class="bg-brand-cardLight rounded-xl p-6 relative shadow-sm border border-gray-100">
              <h4 class="text-lg font-bold text-gray-900 mb-1 leading-tight">Intermediate & Matriculation</h4>
              <p class="text-sm font-semibold text-gray-700 mb-1">New Indian Model School | Al Ain, UAE</p>
              <p class="text-xs font-semibold tracking-wider text-brand-orange mb-3 uppercase">Apr 2020 - Mar 2023</p>
              <p class="text-gray-600 text-sm">Intermediate: 76% | Matriculation: 99%</p>
            </div>
          </div>

          <!-- Certifications Column -->
          <div class="space-y-6">
            <h3 class="text-xl font-bold text-gray-900 border-b border-gray-200 pb-2 mb-4">Certifications & Awards</h3>
            
            <div class="bg-brand-cardLight rounded-xl p-6 relative shadow-sm border border-gray-100">
              <ul class="space-y-5">
                <li class="flex items-start gap-3">
                  <i data-lucide="award" class="w-5 h-5 text-brand-orange shrink-0 mt-0.5"></i>
                  <div>
                    <strong class="text-gray-900 block text-sm">WebKa Hackathon Top 10 Finalist</strong>
                    <span class="text-gray-500 text-xs block mb-1">Jun 2025 - Jul 2025</span>
                    <span class="text-gray-600 text-sm leading-relaxed block">Showcased collaborative skills and ability to perform under high pressure.</span>
                  </div>
                </li>
                <li class="flex items-start gap-3">
                  <i data-lucide="award" class="w-5 h-5 text-brand-orange shrink-0 mt-0.5"></i>
                  <div>
                    <strong class="text-gray-900 block text-sm">RHCSA Summer Training</strong>
                    <span class="text-gray-500 text-xs block mb-1">Jul 2024 - Aug 2024</span>
                    <span class="text-gray-600 text-sm leading-relaxed block">Mastering Linux System Administration I & II.</span>
                  </div>
                </li>
                <li class="flex items-start gap-3">
                  <i data-lucide="award" class="w-5 h-5 text-brand-orange shrink-0 mt-0.5"></i>
                  <div>
                    <strong class="text-gray-900 block text-sm">FreeCodeCamp Certification</strong>
                    <span class="text-gray-500 text-xs block mb-1">Sep 2023</span>
                    <span class="text-gray-600 text-sm leading-relaxed block">Responsive Web Development (HTML, CSS, JavaScript).</span>
                  </div>
                </li>
              </ul>
            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- PROJECTS PAGE -->
    <section id="projects" class="page-section hidden flex-grow bg-brand-dark py-16 px-6 border-t border-gray-800">
      <div class="max-w-4xl mx-auto">
        <h2 class="text-3xl md:text-4xl font-bold tracking-tight text-white mb-10 text-center">FEATURED PROJECTS</h2>
        
        <div class="space-y-4">
          
          <div class="border border-gray-800 rounded-lg p-5 flex flex-col md:flex-row justify-between items-start md:items-center bg-[#0d0d0d] hover:border-gray-600 transition-colors">
            <div class="max-w-2xl">
              <div class="flex items-center gap-3 mb-1">
                <h3 class="text-xl font-semibold text-white">Hairstyle Recommending AI</h3>
              </div>
              <p class="text-brand-orange text-xs mb-2">Nov 2025 - Dec 2025</p>
              <p class="text-gray-400 text-sm mb-3 md:mb-0 leading-relaxed">
                Developed an AI-powered hairstyle recommendation system utilizing computer vision, facial mesh technology, and Python Streamlit. Designed algorithms to accurately classify face shapes and integrate predictive personalized suggestions.
              </p>
              <a href="https://github.com/MohdAdil-007" target="_blank" class="inline-flex items-center gap-1.5 text-xs font-semibold tracking-wider text-brand-orange hover:text-brand-orangeHover transition-colors mt-3 uppercase">
                <i data-lucide="github" class="w-4 h-4"></i> GitHub Repository
              </a>
            </div>
            <div class="flex flex-wrap gap-2 md:justify-end mt-4 md:mt-0 min-w-fit">
              <span class="px-2 py-1 bg-gray-900 text-gray-300 text-xs rounded border border-gray-700">Python</span>
              <span class="px-2 py-1 bg-gray-900 text-gray-300 text-xs rounded border border-gray-700">OpenCV</span>
              <span class="px-2 py-1 bg-gray-900 text-gray-300 text-xs rounded border border-gray-700">Streamlit</span>
            </div>
          </div>

          <div class="border border-gray-800 rounded-lg p-5 flex flex-col md:flex-row justify-between items-start md:items-center bg-[#0d0d0d] hover:border-gray-600 transition-colors">
            <div class="max-w-2xl">
              <div class="flex items-center gap-3 mb-1">
                <h3 class="text-xl font-semibold text-white">Age and Gender Prediction</h3>
              </div>
              <p class="text-brand-orange text-xs mb-2">Oct 2024 - Nov 2024</p>
              <p class="text-gray-400 text-sm mb-3 md:mb-0 leading-relaxed">
                Created an intelligent biometric classification tool, optimizing Python application logic for seamless real-time image processing. Coupled OpenCV face detection with deep learning inference tailored for immediate user feedback.
              </p>
              <a href="https://github.com/MohdAdil-007" target="_blank" class="inline-flex items-center gap-1.5 text-xs font-semibold tracking-wider text-brand-orange hover:text-brand-orangeHover transition-colors mt-3 uppercase">
                <i data-lucide="github" class="w-4 h-4"></i> GitHub Repository
              </a>
            </div>
            <div class="flex flex-wrap gap-2 md:justify-end mt-4 md:mt-0 min-w-fit">
              <span class="px-2 py-1 bg-gray-900 text-gray-300 text-xs rounded border border-gray-700">TensorFlow</span>
              <span class="px-2 py-1 bg-gray-900 text-gray-300 text-xs rounded border border-gray-700">OpenCV</span>
            </div>
          </div>

          <div class="border border-gray-800 rounded-lg p-5 flex flex-col md:flex-row justify-between items-start md:items-center bg-[#0d0d0d] hover:border-gray-600 transition-colors">
            <div class="max-w-2xl">
              <div class="flex items-center gap-3 mb-1">
                <h3 class="text-xl font-semibold text-white">Halo Route - Smart Tourist Safety</h3>
              </div>
              <p class="text-brand-orange text-xs mb-2">Apr 2025 - May 2025</p>
              <p class="text-gray-400 text-sm mb-3 md:mb-0 leading-relaxed">
                Architected a real-time safety monitoring platform designed to protect travelers. Engineered a Guardian Logic system using Leaflet.js and JavaScript, implementing live geo-fencing that detects breaches and triggers automated alerts.
              </p>
              <a href="https://github.com/MohdAdil-007" target="_blank" class="inline-flex items-center gap-1.5 text-xs font-semibold tracking-wider text-brand-orange hover:text-brand-orangeHover transition-colors mt-3 uppercase">
                <i data-lucide="github" class="w-4 h-4"></i> GitHub Repository
              </a>
            </div>
            <div class="flex flex-wrap gap-2 md:justify-end mt-4 md:mt-0 min-w-fit">
              <span class="px-2 py-1 bg-gray-900 text-gray-300 text-xs rounded border border-gray-700">JavaScript</span>
              <span class="px-2 py-1 bg-gray-900 text-gray-300 text-xs rounded border border-gray-700">Leaflet.js</span>
              <span class="px-2 py-1 bg-gray-900 text-gray-300 text-xs rounded border border-gray-700">API</span>
            </div>
          </div>
        </div>
      </div>
    </section>

  </main>

  <!-- Persistent Global Footer -->
  <footer class="bg-white text-gray-900 pt-12 pb-8 px-6 border-t border-gray-200 mt-auto">
    <div class="max-w-7xl mx-auto">
      
      <div class="flex flex-col md:flex-row justify-between items-start md:items-center gap-8 mb-8">
        
        <div>
          <a onclick="navigateTo('home')" class="flex items-center gap-2 mb-4 cursor-pointer w-fit">
            <div class="flex items-center gap-0.5">
              <div class="w-4 h-4 rounded-full bg-black"></div>
              <div class="w-4 h-4 rounded-sm bg-black"></div>
            </div>
            <span class="text-xl font-bold tracking-[0.2em] text-black">ADIL</span>
          </a>
          <p class="text-sm text-gray-600 mb-2">adilvpalain@gmail.com | +91-7902202985</p>
          <p class="text-sm text-gray-500">Based in Punjab, India & Al Ain, UAE</p>
        </div>

        <div class="flex gap-4">
          <a href="mailto:adilvpalain@gmail.com" class="p-3 bg-brand-orange hover:bg-brand-orangeHover text-white rounded-lg transition-colors shadow-sm">
            <i data-lucide="mail" class="w-5 h-5"></i>
          </a>
          <a href="https://github.com/MohdAdil-007" target="_blank" class="p-3 bg-gray-100 hover:bg-gray-200 text-gray-900 rounded-lg transition-colors shadow-sm">
            <i data-lucide="github" class="w-5 h-5"></i>
          </a>
          <a href="https://www.linkedin.com/in/mohammed-adil-vp" target="_blank" class="p-3 bg-gray-100 hover:bg-gray-200 text-blue-600 rounded-lg transition-colors shadow-sm">
            <i data-lucide="linkedin" class="w-5 h-5"></i>
          </a>
        </div>
        
      </div>

      <div class="border-t border-gray-200 pt-6 flex flex-col md:flex-row justify-between items-center gap-4 text-xs text-gray-500">
        <div>
          &copy; <span id="year"></span> Mohammed Adil. Built with HTML & Tailwind CSS.
        </div>
      </div>

    </div>
  </footer>

  <!-- Application Logic -->
  <script>
    document.getElementById('year').textContent = new Date().getFullYear();

    const menuToggle = document.getElementById('menu-toggle');
    const mobileMenu = document.getElementById('mobile-menu');
    const menuIcon = document.getElementById('menu-icon');

    // Toggle Mobile Menu
    menuToggle.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
      if (mobileMenu.classList.contains('hidden')) {
        menuIcon.setAttribute('data-lucide', 'menu');
      } else {
        menuIcon.setAttribute('data-lucide', 'x');
      }
      lucide.createIcons();
    });

    // Multi-Page Navigation Logic
    window.navigateTo = function(targetId) {
      // Hide all sections
      const sections = document.querySelectorAll('.page-section');
      sections.forEach(sec => sec.classList.add('hidden'));
      
      // Show targeted section and re-trigger animation
      const targetSection = document.getElementById(targetId);
      if (targetSection) {
        targetSection.classList.remove('hidden');
        targetSection.classList.remove('animate-fadeIn');
        void targetSection.offsetWidth; // trigger reflow
        targetSection.classList.add('animate-fadeIn');
      }

      // Update Desktop Nav Active States
      const desktopLinks = document.querySelectorAll('.nav-link');
      desktopLinks.forEach(link => {
        if (link.dataset.target === targetId) {
          link.classList.add('text-white');
          link.classList.remove('text-gray-300');
        } else {
          link.classList.remove('text-white');
          link.classList.add('text-gray-300');
        }
      });

      // Update Mobile Nav Active States
      const mobileLinks = document.querySelectorAll('.mobile-nav-link');
      mobileLinks.forEach(link => {
        if (link.dataset.target === targetId) {
          link.classList.add('text-white', 'bg-gray-900');
          link.classList.remove('text-gray-300');
        } else {
          link.classList.remove('text-white', 'bg-gray-900');
          link.classList.add('text-gray-300');
        }
      });

      // Close mobile menu
      mobileMenu.classList.add('hidden');
      menuIcon.setAttribute('data-lucide', 'menu');
      lucide.createIcons();

      // Scroll to top
      window.scrollTo({ top: 0, behavior: 'smooth' });
    };

    // Initialize Lucide Icons
    document.addEventListener('DOMContentLoaded', () => {
      lucide.createIcons();
    });
  </script>
</body>
</html>
