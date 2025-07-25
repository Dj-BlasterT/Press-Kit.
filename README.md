<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DJ [Votre Nom] - Press Kit</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0a1a3b;
            color: #e5e7eb;
            overflow-x: hidden;
        }
        /* Animation pour l'en-tête */
        .header-container {
            position: relative;
            overflow: hidden;
        }
        .header-line {
            position: absolute;
            background: linear-gradient(90deg, transparent, #00ddeb, transparent);
            height: 2px;
            width: 100%;
            animation: slideLine 3.5s infinite ease-in-out;
        }
        .header-line:nth-child(1) { top: 0; }
        .header-line:nth-child(2) { bottom: 0; animation-delay: 1.75s; }
        @keyframes slideLine {
            0% { transform: translateX(-100%); }
            50% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }
        /* Animation pour le logo */
        .logo {
            transition: transform 0.3s ease;
            animation: pulseLogo 2.5s infinite ease-in-out;
        }
        .logo:hover {
            transform: scale(1.15);
        }
        @keyframes pulseLogo {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.12); }
        }
        /* Animation pour les liens de navigation */
        nav a {
            position: relative;
            transition: color 0.3s ease;
        }
        nav a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: #00ddeb;
            transition: width 0.3s ease;
        }
        nav a:hover {
            color: #00ddeb;
        }
        nav a:hover::after {
            width: 100%;
        }
        /* Style des titres de section */
        .section-title {
            position: relative;
            display: inline-block;
            margin-bottom: 2rem;
        }
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 50%;
            transform: translateX(-50%);
            width: 50px;
            height: 3px;
            background-color: #00ddeb;
            transition: width 0.5s ease;
        }
        .section-title:hover::after {
            width: 100px;
        }
        /* Animation de fond pour la section Accueil */
        .hero-bg {
            position: relative;
            overflow: hidden;
        }
        .hero-bg::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(0, 221, 235, 0.2) 8%, transparent 8%);
            background-size: 20px 20px;
            animation: floatParticles 10s infinite linear;
            z-index: 0;
        }
        @keyframes floatParticles {
            0% { background-position: 0 0; }
            100% { background-position: 100px 100px; }
        }
        /* Animation fade-in pour les sections */
        .section {
            opacity: 0;
            transform: translateY(30px);
            animation: fadeIn 1.2s ease-out forwards;
        }
        @keyframes fadeIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .section:nth-child(2) { animation-delay: 0.3s; }
        .section:nth-child(3) { animation-delay: 0.6s; }
        .section:nth-child(4) { animation-delay: 0.9s; }
        .section:nth-child(5) { animation-delay: 1.2s; }
        /* Effet de survol pour les cartes */
        .card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 10px rgba(0, 221, 235, 0.3);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="fixed w-full top-0 z-50 bg-[#0a1a3b] bg-opacity-95 header-container">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <div class="flex items-center">
                <img src="logo.jpg" alt="DJ Logo" class="logo h-12 w-auto">
                 <h1 class="text-3xl font-bold tracking-tight ml-4">DJ BlasterT</h1>
            </div>
            <ul class="flex space-x-8 text-sm uppercase tracking-wide">
                <li><a href="#accueil" class="hover:text-cyan-400">Accueil</a></li>
                <li><a href="#presentation" class="hover:text-cyan-400">Présentation</a></li>
                <li><a href="#sets" class="hover:text-cyan-400">Sets Enregistrés</a></li>
                <li><a href="#dates" class="hover:text-cyan-400">Références</a></li>
                <li><a href="#offres" class="hover:text-cyan-400">Offres</a></li>
                <li><a href="#contact" class="hover:text-cyan-400">Contact</a></li>
            </ul>
        </div>
        <div class="header-line"></div>
        <div class="header-line"></div>
    </nav>

    <!-- Section Accueil -->
    <section id="accueil" class="h-screen flex items-center justify-center bg-cover bg-center hero-bg section" style="background-image: linear-gradient(rgba(10, 26, 59, 0.7), rgba(10, 26, 59, 0.7)), url('https://source.unsplash.com/random/1920x1080?dj');">
        <div class="text-center relative z-10">
            <h1 class="text-5xl md:text-6xl font-extrabold tracking-tight mb-4">BlasterT</h1>
            <p class="text-xl md:text-2xl mb-8 opacity-80">Pure Tech House Energy</p>
            <a href="#contact" class="bg-cyan-500 hover:bg-cyan-600 text-black py-3 px-8 rounded-full font-medium uppercase tracking-wide transition-all duration-300">Me contacter</a>
        </div>
    </section>

    <!-- Section Présentation -->
    <section id="presentation" class="py-20 container mx-auto px-6 section">
        <h2 class="text-4xl font-bold text-center section-title">Présentation</h2>
        <div class="flex flex-col md:flex-row items-center max-w-5xl mx-auto">
            <div class="md:w-1/2 mb-8 md:mb-0">
                <img src="https://source.unsplash.com/random/600x400?dj" alt="DJ Photo" class="rounded-lg shadow-xl w-full card">
            </div>
            <div class="md:w-1/2 md:pl-10">
                <p class="text-lg leading-relaxed opacity-90">BlasterT est un DJ tech house de 18 ans.
Inspiré par la scène UK, il livre des sets énergiques, groovy et techniquement précis.

Après plusieurs soirées privées réussies, il se lance sur les scènes publiques : clubs, bars, événements, avec une tech house calibrée pour faire lever les bras et faire vibrer les basses.            </div>
        </div>
    </section>

    <!-- Section Sets Enregistrés -->
    <section id="sets" class="py-20 bg-[#0a1a3b]/80 section">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center section-title">Sets Enregistrés</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <div class="bg-[#0a1a3b] p-6 rounded-lg shadow-lg card">
                  <h3 class="text-xl font-semibold mb-2">Tech House</h3>
                  <a href="https://www.youtube.com/watch?v=Bdc47GCgdzQ&list=RDBdc47GCgdzQ&start_radio=1" >
                    <img src="logo.jpg" alt="DJ Logo" >
                  </a>
                </div>
                <div class="bg-[#0a1a3b] p-6 rounded-lg shadow-lg card">
                    <h3 class="text-xl font-semibold mb-2">Tech House</h3>
                    <p class="mb-4 opacity-80"></p>
                    <iframe class="w-full h-48 rounded" src="https://www.youtube.com/embed/[ID_VIDEO_2]" frameborder="0" allowfullscreen></iframe>
                    <a href="https://www.youtube.com/watch?v=Bdc47GCgdzQ&list=RDBdc47GCgdzQ&start_radio=1" >YouTube</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Section Références -->
    <section id="dates" class="py-20 container mx-auto px-6 section">
        <h2 class="text-4xl font-bold text-center section-title">Références</h2>
        <ul class="max-w-2xl mx-auto text-lg leading-relaxed opacity-90 space-y-4">
            <li><strong>2025</strong> : Soirées privées</li>
            
        </ul>
    </section>

    <!-- Section Ce que je propose -->
    <section id="offres" class="py-20 bg-[#0a1a3b]/80 section">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center section-title">Ce que je propose</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <div class="bg-[#0a1a3b] p-6 rounded-lg shadow-lg text-center card">
                    <h3 class="text-xl font-semibold mb-4">Evénement</h3>
                    <p class="opacity-80">Des sets sur mesure pour tout événements.</p>
                </div>
                <div class="bg-[#0a1a3b] p-6 rounded-lg shadow-lg text-center card">
                    <h3 class="text-xl font-semibold mb-4">Clubs & Festivals</h3>
                    <p class="opacity-80">Des performances vibrantes pour clubs et grands festivals.</p>
                </div>
                <div class="bg-[#0a1a3b] p-6 rounded-lg shadow-lg text-center card">
                    <h3 class="text-xl font-semibold mb-4">Collaborations</h3>
                    <p class="opacity-80">Mixes exclusifs ou projets avec d'autres artistes.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Section Contact -->
    <section id="contact" class="py-20 bg-[#0a1a3b]/80 section">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-bold text-center section-title">Me contacter</h2>
            <div class="max-w-lg mx-auto text-center">
                <p class="text-lg mb-6 opacity-80">Pour toute demande de booking ou collaboration :</p>
                <p class="mb-2"><strong>Email :</strong> thomasbriffaut07@gmail.com</p>
                <p class="mb-4"><strong>Téléphone :</strong> +33 7 82 11 58 61</p>
                <div class="flex justify-center space-x-6">
                    <a href="https://www.instagram.com/dj_blaster_t/profilecard/?igsh=MWdtMXoxOTU2MTJsdQ==" class="hover:text-cyan-400 transition-all duration-300">Instagram</a>
                    <a href="https://www.youtube.com/channel/UCIhfu9YwSdmmyOadEA7o_Dg" class="hover:text-cyan-400 transition-all duration-300">YouTube</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-[#0a1a3b] py-6 text-center text-sm opacity-80">
        <p>© 2025 DJ [Votre Nom]. Tous droits réservés.</p>
    </footer>
</body>
</html>
