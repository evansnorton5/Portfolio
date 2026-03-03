
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio | Michel Johanice Whalace</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            line-height: 1.6;
            color: #2d2e32;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Navigation */
        nav {
            padding: 30px 0;
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
            animation: slideDown 0.8s ease;
        }

        @keyframes slideDown {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #2d2e32;
            text-decoration: none;
            transition: transform 0.3s;
        }

        .logo:hover {
            transform: scale(1.05);
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: #2d2e32;
            font-weight: 500;
            transition: all 0.3s;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #147efb;
            transition: width 0.3s;
        }

        .nav-links a:hover {
            color: #147efb;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            padding: 80px 0;
            background-color: rgba(255, 255, 255, 0.95);
            margin: 20px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            animation: fadeInUp 1s ease;
        }

        @keyframes fadeInUp {
            from {
                transform: translateY(50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .hero .container {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .hero-content {
            flex: 1;
        }

        .hero-content h1 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 20px;
            line-height: 1.2;
            animation: slideInLeft 1s ease;
        }

        @keyframes slideInLeft {
            from {
                transform: translateX(-50px);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        .hero-content p {
            font-size: 1.2rem;
            color: #555;
            margin-bottom: 30px;
            max-width: 500px;
            animation: slideInLeft 1s ease 0.2s both;
        }

        .hero-image {
            flex: 1;
            text-align: center;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }

        .hero-image img {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            box-shadow: 0 20px 30px rgba(0,0,0,0.15);
            border: 5px solid #fff;
            transition: transform 0.3s, box-shadow 0.3s;
            max-width: 100%;
        }

        .hero-image img:hover {
            transform: scale(1.05);
            box-shadow: 0 30px 40px rgba(0,0,0,0.2);
        }

        /* Skills Section */
        .skills {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            animation: fadeIn 1s ease;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        .section-title h2 {
            font-size: 2rem;
            font-weight: 700;
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .section-title p {
            color: #fff;
            font-weight: 500;
            margin-bottom: 10px;
            font-size: 1.2rem;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.4s;
            animation: scaleIn 0.8s ease;
            backdrop-filter: blur(10px);
        }

        @keyframes scaleIn {
            from {
                transform: scale(0.9);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        .skill-category:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .skill-category h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #147efb;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .skill-items {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .skill-item {
            display: flex;
            align-items: center;
            gap: 10px;
            animation: slideInRight 0.5s ease;
        }

        @keyframes slideInRight {
            from {
                transform: translateX(50px);
                opacity: 0;
            }
            to {
                transform: translateX(0);
                opacity: 1;
            }
        }

        .skill-name {
            width: 120px;
            font-weight: 500;
        }

        .skill-bar {
            flex: 1;
            height: 8px;
            background: #e9e9e9;
            border-radius: 4px;
            overflow: hidden;
        }

        .skill-level {
            height: 100%;
            background: linear-gradient(90deg, #147efb, #00c6fb);
            border-radius: 4px;
            width: 0%;
            transition: width 1s ease;
            animation: fillBar 1.5s ease;
        }

        @keyframes fillBar {
            from {
                width: 0%;
            }
        }

        .skill-percent {
            width: 45px;
            font-size: 0.9rem;
            color: #666;
        }

        .tech-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 20px;
        }

        .tech-tag {
            background: #f3f4f6;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            color: #555;
            transition: all 0.3s;
            cursor: default;
        }

        .tech-tag:hover {
            background: #147efb;
            color: #fff;
            transform: scale(1.1);
        }

        /* About Section */
        .about {
            padding: 80px 0;
            background-color: rgba(255, 255, 255, 0.95);
            margin: 20px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            animation: fadeInUp 1s ease;
        }

        .about-content {
            max-width: 700px;
            margin: 0 auto;
            text-align: center;
        }

        .about-content h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #2d2e32;
        }

        .about-content p {
            color: #555;
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        /* Contact Section */
        .contact {
            padding: 80px 0;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
            background: rgba(255, 255, 255, 0.95);
            padding: 15px 25px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            transition: all 0.3s;
            animation: bounceIn 0.8s ease;
            flex: 1;
            min-width: 250px;
            max-width: 300px;
            backdrop-filter: blur(10px);
        }

        @keyframes bounceIn {
            0% {
                transform: scale(0.3);
                opacity: 0;
            }
            50% {
                transform: scale(1.05);
                opacity: 0.8;
            }
            100% {
                transform: scale(1);
                opacity: 1;
            }
        }

        .contact-item:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
            background: #fff;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
            transition: transform 0.3s;
        }

        .contact-item:hover .contact-icon {
            transform: rotate(360deg);
        }

        .contact-text h4 {
            font-size: 1rem;
            color: #666;
            font-weight: 400;
        }

        .contact-text p {
            font-weight: 600;
            color: #2d2e32;
        }

        .contact-link {
            text-decoration: none;
            color: inherit;
            width: 100%;
        }

        /* WhatsApp specific style */
        .contact-item.whatsapp:hover {
            background: #25D366;
            color: white;
        }

        .contact-item.whatsapp:hover .contact-text h4,
        .contact-item.whatsapp:hover .contact-text p {
            color: white;
        }

        .contact-item.whatsapp:hover .contact-icon {
            background: white;
            color: #25D366;
        }

        /* Footer */
        footer {
            padding: 30px 0;
            background-color: rgba(0, 0, 0, 0.8);
            color: #fff;
            text-align: center;
            backdrop-filter: blur(10px);
            margin-top: 50px;
        }

        /* Images responsives */
        img {
            max-width: 100%;
            height: auto;
        }

        /* ===== MEDIA QUERIES POUR MOBILE ===== */
        /* Version téléphone portable (max-width: 600px) - Mode portrait */
        @media screen and (max-width: 600px) {
            body {
                font-size: 14px;
            }

            .container {
                padding: 0 15px;
            }

            /* Navigation */
            nav {
                padding: 15px 0;
            }

            .logo {
                font-size: 1.2rem;
            }

            .nav-links {
                display: none;
            }

            /* Hero Section */
            .hero {
                padding: 40px 0;
                margin: 10px;
            }

            .hero .container {
                flex-direction: column-reverse;
                text-align: center;
                gap: 30px;
            }

            .hero-content h1 {
                font-size: 2rem;
            }

            .hero-content p {
                font-size: 1rem;
                margin: 0 auto 20px;
            }

            .hero-image img {
                width: 200px;
                height: 200px;
            }

            /* Skills Section */
            .skills {
                padding: 40px 0;
            }

            .section-title h2 {
                font-size: 1.5rem;
            }

            .skills-grid {
                grid-template-columns: 1fr;
                gap: 20px;
            }

            .skill-category {
                padding: 20px;
            }

            .skill-category h3 {
                font-size: 1.3rem;
            }

            .skill-item {
                flex-wrap: wrap;
            }

            .skill-name {
                width: 100%;
                margin-bottom: 5px;
            }

            .skill-bar {
                width: 100%;
            }

            /* About Section */
            .about {
                padding: 40px 0;
                margin: 10px;
            }

            .about-content h3 {
                font-size: 1.5rem;
            }

            .about-content p {
                font-size: 1rem;
            }

            /* Contact Section */
            .contact {
                padding: 40px 0;
            }

            .contact-info {
                flex-direction: column;
                align-items: center;
                gap: 15px;
            }

            .contact-item {
                width: 100%;
                max-width: 100%;
                min-width: auto;
            }

            .contact-icon {
                width: 40px;
                height: 40px;
                font-size: 1.2rem;
            }

            .contact-text p {
                font-size: 0.9rem;
            }

            /* Footer */
            footer {
                padding: 20px 0;
                font-size: 0.9rem;
            }
        }

        /* Version téléphone en mode paysage (entre 601px et 768px) */
        @media screen and (min-width: 601px) and (max-width: 768px) {
            body {
                font-size: 15px;
            }

            .hero .container {
                flex-direction: row;
            }

            .hero-content h1 {
                font-size: 2.2rem;
            }

            .hero-image img {
                width: 250px;
                height: 250px;
            }

            .skills-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .contact-info {
                flex-wrap: wrap;
            }
        }

        /* Version tablette (769px à 1024px) */
        @media screen and (min-width: 769px) and (max-width: 1024px) {
            .container {
                max-width: 900px;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }
        }

        /* Icônes */
        .icon-email::after {
            content: "✉️";
        }
        .icon-github::after {
            content: "🐙";
        }
        .icon-linkedin::after {
            content: "🔗";
        }
        .icon-whatsapp::after {
            content: "📱";
        }
        .icon-phone::after {
            content: "📞";
        }
        .icon-code::after {
            content: "💻";
        }
        .icon-design::after {
            content: "🎨";
        }
        .icon-tools::after {
            content: "🛠️";
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="container">
            <a href="#" class="logo">Michel Johanice Whalace</a>
            <div class="nav-links">
                <a href="#skills">Compétences</a>
                <a href="#about">À propos</a>
                <a href="#contact">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Bonjour, je suis Michel Johanice Whalace</h1>
                <p>Développeur créatif passionné par la création d'expériences web élégantes et fonctionnelles.</p>
                <p>📍 Fianarantsoa, Madagascar</p>
            </div>
            <div class="hero-image">
                <img src="https://scontent-jnb2-1.xx.fbcdn.net/v/t39.30808-1/645678954_1511720434002629_4603668677788581470_n.jpg?stp=dst-jpg_s200x200_tt6&_nc_cat=107&ccb=1-7&_nc_sid=1d2534&_nc_ohc=h8EMHVXp3FkQ7kNvwE6AUcO&_nc_oc=Adm61SgkV8cPeJzvKheVvr6nqsjRZwLz7pHFwpCSu-VeZZk_3mTyZzyiDUrXD4adyNmEbJWp6Wh909dFjIndN2vO&_nc_zt=24&_nc_ht=scontent-jnb2-1.xx&_nc_gid=jVVtTzVbr-YtRsqhhFuKQw&_nc_ss=8&oh=00_AfzNjy8HW2Rtx1NmJH9ph6twVXw0zUFWcYKY10ysiFKfSQ&oe=69AC685F" alt="Photo de profil">
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <div class="section-title">
                <p>COMPÉTENCES</p>
                <h2>Mes expertises</h2>
            </div>
            <div class="skills-grid">
                <!-- Frontend -->
                <div class="skill-category">
                    <h3>
                        <span class="icon-code"></span>
                        Frontend
                    </h3>
                    <div class="skill-items">
                        <div class="skill-item">
                            <span class="skill-name">HTML/CSS</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 90%"></div>
                            </div>
                            <span class="skill-percent">90%</span>
                        </div>
                        <div class="skill-item">
                            <span class="skill-name">JavaScript</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 75%"></div>
                            </div>
                            <span class="skill-percent">75%</span>
                        </div>
                        <div class="skill-item">
                            <span class="skill-name">React</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 60%"></div>
                            </div>
                            <span class="skill-percent">60%</span>
                        </div>
                    </div>
                    <div class="tech-tags">
                        <span class="tech-tag">HTML</span>
                        <span class="tech-tag">CSS</span>
                        <span class="tech-tag">JavaScript</span>
                    </div>
                </div>

                <!-- Backend -->
                <div class="skill-category">
                    <h3>
                        <span class="icon-tools"></span>
                        Backend
                    </h3>
                    <div class="skill-items">
                        <div class="skill-item">
                            <span class="skill-name">Node.js</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 65%"></div>
                            </div>
                            <span class="skill-percent">65%</span>
                        </div>
                        <div class="skill-item">
                            <span class="skill-name">Python</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 70%"></div>
                            </div>
                            <span class="skill-percent">70%</span>
                        </div>
                        <div class="skill-item">
                            <span class="skill-name">PHP</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 50%"></div>
                            </div>
                            <span class="skill-percent">50%</span>
                        </div>
                    </div>
                    <div class="tech-tags">
                        <span class="tech-tag">Node.js</span>
                        <span class="tech-tag">Express</span>
                    </div>
                </div>

                <!-- Outils & Design -->
                <div class="skill-category">
                    <h3>
                        <span class="icon-design"></span>
                        Outils & Design
                    </h3>
                    <div class="skill-items">
                        <div class="skill-item">
                            <span class="skill-name">Git</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 80%"></div>
                            </div>
                            <span class="skill-percent">80%</span>
                        </div>
                        <div class="skill-item">
                            <span class="skill-name">Figma</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 65%"></div>
                            </div>
                            <span class="skill-percent">65%</span>
                        </div>
                        <div class="skill-item">
                            <span class="skill-name">UI/UX</span>
                            <div class="skill-bar">
                                <div class="skill-level" style="width: 70%"></div>
                            </div>
                            <span class="skill-percent">70%</span>
                        </div>
                    </div>
                    <div class="tech-tags">
                        <span class="tech-tag">Git</span>
                        <span class="tech-tag">GitHub</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <p>À PROPOS</p>
                <h2>Qui suis-je ?</h2>
            </div>
            <div class="about-content">
                <h3>Développeur passionné par le design et l'innovation</h3>
                <p>Je suis un développeur web créatif basé à Fianarantsoa, Madagascar. J'aime transformer des idées en solutions numériques uniques et fonctionnelles.</p>
                <p>Étudiant à l'EMIT Fianarantsoa, je suis constamment à la recherche de nouveaux défis pour améliorer mes compétences et créer des expériences web mémorables.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <p>CONTACT</p>
                <h2>Travaillons ensemble</h2>
            </div>
            <div class="contact-info">
                <!-- Email -->
                <a href="mailto:johanicewhalace@gmail.com" class="contact-link">
                    <div class="contact-item">
                        <div class="contact-icon icon-email"></div>
                        <div class="contact-text">
                            <h4>Email</h4>
                            <p>johanicewhalace@gmail.com</p>
                        </div>
                    </div>
                </a>

                <!-- Téléphone -->
                <a href="tel:+261385139111" class="contact-link">
                    <div class="contact-item">
                        <div class="contact-icon icon-phone"></div>
                        <div class="contact-text">
                            <h4>Téléphone</h4>
                            <p>+261 38 51 391 11</p>
                        </div>
                    </div>
                </a>

                <!-- WhatsApp -->
                <a href="https://wa.me/261385139111" target="_blank" class="contact-link">
                    <div class="contact-item whatsapp">
                        <div class="contact-icon icon-whatsapp"></div>
                        <div class="contact-text">
                            <h4>WhatsApp</h4>
                            <p>+261 38 51 391 11</p>
                        </div>
                    </div>
                </a>

                <!-- GitHub -->
                <a href="https://github.com/johanicewhalace-prog" target="_blank" class="contact-link">
                    <div class="contact-item">
                        <div class="contact-icon icon-github"></div>
                        <div class="contact-text">
                            <h4>GitHub</h4>
                            <p>@johanicewhalace-prog</p>
                        </div>
                    </div>
                </a>

                <!-- LinkedIn -->
                <a href="https://linkedin.com/in/johanicewhalace" target="_blank" class="contact-link">
                    <div class="contact-item">
                        <div class="contact-icon icon-linkedin"></div>
                        <div class="contact-text">
                            <h4>LinkedIn</h4>
                            <p>@johanicewhalace</p>
                        </div>
                    </div>
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>© 2026 Michel Johanice Whalace. Tous droits réservés.</p>
        </div>
    </footer>
</body>
</html>
