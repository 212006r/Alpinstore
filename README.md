# Alpinstore
site sur les article descalade
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alpinisme & Escalade - Le Guide de la Montagne</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --glacier-blue: #4A90A4;
            --rock-gray: #5A5A5A;
            --snow-white: #F8F9FA;
            --sunset-orange: #E07A5F;
            --forest-green: #3D5A40;
            --dark-slate: #2C3E50;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: var(--snow-white);
        }

        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
        }

        /* Navigation */
        nav {
            background: linear-gradient(135deg, var(--dark-slate), var(--glacier-blue));
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 2rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        nav a:hover {
            color: var(--sunset-orange);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=1920') center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            margin-top: 0;
        }

        .hero-content h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            animation: fadeInUp 1s ease;
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.3s both;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: var(--sunset-orange);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: transform 0.3s, box-shadow 0.3s;
            animation: fadeInUp 1s ease 0.6s both;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
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

        /* Sections */
        section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--dark-slate);
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--sunset-orange);
            margin: 1rem auto;
            border-radius: 2px;
        }

        /* Articles Grid */
        .articles-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .article-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .article-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }

        .article-image {
            height: 200px;
            background: var(--glacier-blue);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .article-content {
            padding: 1.5rem;
        }

        .article-content h3 {
            color: var(--dark-slate);
            margin-bottom: 0.5rem;
            font-size: 1.3rem;
        }

        .article-content p {
            color: #666;
            margin-bottom: 1rem;
        }

        .read-more {
            color: var(--sunset-orange);
            text-decoration: none;
            font-weight: 600;
        }

        /* Guides Section */
        .guides {
            background: linear-gradient(135deg, #f5f7fa, #e4e8ec);
        }

        .guide-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .guide-item {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            border-left: 4px solid var(--glacier-blue);
        }

        .guide-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .guide-item h3 {
            color: var(--dark-slate);
            margin-bottom: 0.5rem;
        }

        /* Matériel Section */
        .materiel-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
        }

        .materiel-item {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .materiel-item:hover {
            transform: scale(1.05);
        }

        .materiel-item .icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        /* Sécurité Section */
        .securite {
            background: var(--dark-slate);
            color: white;
        }

        .securite .section-title {
            color: white;
        }

        .securite-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .securite-item {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 10px;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .securite-item h3 {
            color: var(--sunset-orange);
            margin-bottom: 1rem;
        }

        /* Galerie */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }

        .gallery-item {
            height: 250px;
            background: var(--rock-gray);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .gallery-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(transparent, rgba(0,0,0,0.7));
            opacity: 0;
            transition: opacity 0.3s;
        }

        .gallery-item:hover::before {
            opacity: 1;
        }

        /* Footer */
        footer {
            background: var(--dark-slate);
            color: white;
            text-align: center;
            padding: 3rem 2rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
            text-align: left;
        }

        .footer-section h4 {
            color: var(--sunset-orange);
            margin-bottom: 1rem;
        }

        .footer-section a {
            color: #aaa;
            text-decoration: none;
            display: block;
            margin-bottom: 0.5rem;
        }

        .footer-section a:hover {
            color: white;
        }

        .copyright {
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 2rem;
            color: #aaa;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            nav ul {
                gap: 1rem;
            }
            
            nav a {
                font-size: 0.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#accueil">Accueil</a></li>
            <li><a href="#articles">Articles</a></li>
            <li><a href="#guides">Guides</a></li>
            <li><a href="#materiel">Matériel</a></li>
            <li><a href="#securite">Sécurité</a></li>
            <li><a href="#galerie">Galerie</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="accueil">
        <div class="hero-content">
            <h1>Alpinisme & Escalade</h1>
            <p>Le guide complet de la montagne</p>
            <a href="#articles" class="btn">Explorer les articles</a>
        </div>
    </section>

    <!-- Articles Section -->
    <section id="articles">
        <h2 class="section-title">Nos Articles</h2>
        <div class="articles-grid">
            <article class="article-card">
                <img style="display: block;-webkit-user-select: none;margin: auto;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://media.istockphoto.com/id/481109476/fr/photo/magnifique-paysage-de-montagnes-de-lhimalaya-ou.jpg?s=612x612&amp;w=0&amp;k=20&amp;c=53HyqmPCyaN4wAx1b5ER63VMqvanWtSYBKg1VrYntOQ=">
                <div class="article-content">
                    <h3>Débuter en Alpinisme</h3>
                    <p>Guide complet pour les débutants : choisir sa première course, équipement de base et préparation physique.</p>
                    <a href="#" class="read-more">Lire la suite →</a>
                </div>
            </article>
            <article class="article-card">
                <img style="display: block;-webkit-user-select: none;margin: auto;cursor: zoom-in;background-color: hsl(0, 0%, 90%);transition: background-color 300ms;" src="https://contents.mediadecathlon.com/p2586586/k$902bb1ae3795eda0228fa3a96ab24864/1920x0/3762pt2501/5983xcr3986/default.jpg?format=auto" width="637" height="424">
                <div class="article-content">
                    <h3>Techniques d'Escalade</h3>
                    <p>Apprenez les mouvements essentiels : la posture, la respiration, et la gestion de la peur de la hauteur.</p>
                    <a href="#" class="read-more">Lire la suite →</a>
                </div>
            </article>
            <article class="article-card">
                <div class="article-image">🎒</div>
                <div class="article-content">
                    <h3>Randonnée en Haute Montagne</h3>
                    <p>Préparation, itinéraires et conseils pour des treks en toute sécurité dans les plus beaux massifs.</p>
                    <a href="#" class="read-more">Lire la suite →</a>
                </div>
            </article>
            <article class="article-card">
                <div class="article-image">❄️</div>
                <div class="article-content">
                    <h3>Cascade de Glace</h3>
                    <p>Tout sur cette discipline exigeante : technique de cramponnage, piolets et lecture des formations.</p>
                    <a href="#" class="read-more">Lire la suite →</a>
                </div>
            </article>
            <article class="article-card">
                <div class="article-image">⛺</div>
                <div class="article-content">
                    <h3>Bivouac en Montagne</h3>
                    <p>Choisir son site, installer sa tente et passer une nuit confortable à l'état sauvage.</p>
                    <a href="#" class="read-more">Lire la suite →</a>
                </div>
            </article>
            <article class="article-card">
                <div class="article-image">🗻</div>
                <div class="article-content">
                    <h3>Les 4000 des Alpes</h3>
                    <p>Présentation des 82 sommets de plus de 4000m dans les Alpes, classés par difficulté.</p>
                    <a href="#" class="read-more">Lire la suite →</a>
                </div>
            </article>
        </div>
    </section>

    <!-- Guides Section -->
    <section class="guides" id="guides">
        <h2 class="section-title">Guides Pratiques</h2>
        <div class="guide-list">
            <div class="guide-item">
                <div class="guide-icon">🧭</div>
                <h3>Orientation</h3>
                <p>Lecture de carte, utilisation de la boussole et GPS en montagne. Ne vous perdez plus jamais.</p>
            </div>
            <div class="guide-item">
                <div class="guide-icon">🌤️</div>
                <h3>Météo Montagne</h3>
                <p>Comprendre les signes météo et anticiper les changements brutaux de conditions.</p>
            </div>
            <div class="guide-item">
                <div class="guide-icon">🏥</div>
                <h3>Secourisme</h3>
                <p>Les gestes qui sauvent : premiers secours, alerte et évacuation en milieu hostile.</p>
            </div>
            <div class="guide-item">
                <div class="guide-icon">🥾</div>
                <h3>Technique de Marche</h3>
                <p>Économiser son énergie, gérer son souffle et préserver ses articulations.</p>
            </div>
        </div>
    </section>

    <!-- Matériel Section -->
    <section id="materiel">
        <h2 class="section-title">Matériel Essentiel</h2>
        <div class="materiel-grid">
            <div class="materiel-item">
                <div class="icon">🪢</div>
                <h4>Cordes</h4>
                <p>Semi-statiques et dynamiques</p>
            </div>
            <div class="materiel-item">
                <div class="icon">🪝</div>
                <h4>Mousquetons</h4>
                <p>À vis et à double</p>
            </div>
            <div class="materiel-item">
                <div class="icon">🪓</div>
                <h4>Piolets</h4>
                <p>Classiques et techniques</p>
            </div>
            <div class="materiel-item">
                <div class="icon">👢</div>
                <h4>Crampons</h4>
                <p>10 ou 12 pointes</p>
            </div>
            <div class="materiel-item">
                <div class="icon">⛑️</div>
                <h4>Casques</h4>
                <p>Légers et aérés</p>
            </div>
            <div class="materiel-item">
                <div class="icon">🎒</div>
                <h4>Sacs</h4>
                <p>30L à 60L</p>
            </div>
            <div class="materiel-item">
                <div class="icon">🧤</div>
                <h4>Gants</h4>
                <p>Chauds et précis</p>
            </div>
            <div class="materiel-item">
                <div class="icon">🕶️</div>
                <h4>Lunettes</h4>
                <p>Catégorie 4</p>
            </div>
        </div>
    </section>

    <!-- Sécurité Section -->
    <section class="securite" id="securite">
        <h2 class="section-title">Sécurité en Montagne</h2>
        <div class="securite-list">
            <div class="securite-item">
                <h3>⚠️ Risques Objectifs</h3>
                <p>Chutes de pierres, avalanches, crevasses et intempéries. Apprenez à les identifier et à les éviter.</p>
            </div>
            <div class="securite-item">
                <h3>📱 Communication</h3>
                <p>Numéros d'urgence, couverture réseau et appareils de localisation (DVA, téléphone satellite).</p>
            </div>
            <div class="securite-item">
                <h3>🤝 Cordée</h3>
                <p>Techniques de progression en cordee, encordement et assurage. La confiance entre partenaires.</p>
            </div>
            <div class="securite-item">
                <h3>⛈️ Orage</h3>
                <p>Se protéger de la foudre en montagne : positions de sécurité et comportements à adopter.</p>
            </div>
        </div>
    </section>

    <!-- Galerie Section -->
    <section id="galerie">
        <h2 class="section-title">Galerie</h2>
        <div class="gallery">
            <div class="gallery-item">🏔️ Mont Blanc</div>
            <div class="gallery-item">🧗 Grimpe</div>
            <div class="gallery-item">❄️ Glacier</div>
            <div class="gallery-item">⛺ Bivouac</div>
            <div class="gallery-item">🌄 Lever de soleil</div>
            <div class="gallery-item">🦅 Faune</div>
            <div class="gallery-item">🌸 Flore</div>
            <div class="gallery-item">🗻 Cime</div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h4>À propos</h4>
                <p>Site dédié à l'alpinisme et à l'escalade, créé par des passionnés pour partager notre amour de la montagne.</p>
            </div>
            <div class="footer-section">
                <h4>Liens rapides</h4>
                <a href="#articles">Articles</a>
                <a href="#guides">Guides</a>
                <a href="#materiel">Matériel</a>
                <a href="#securite">Sécurité</a>
            </div>
            <div class="footer-section">
                <h4>Contact</h4>
                <a href="mailto:contact@alpinisme-montagne.fr">contact@alpinisme-montagne.fr</a>
                <a href="#">Facebook</a>
                <a href="#">Instagram</a>
                <a href="#">YouTube</a>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2024 Alpinisme & Escalade. Tous droits réservés.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling pour les liens d'ancrage
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Animation au scroll
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Appliquer l'animation aux cartes
        document.querySelectorAll('.article-card, .guide-item, .materiel-item, .securite-item').forEach((el, index) => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = `opacity 0.6s ease ${index * 0.1}s, transform 0.6s ease ${index * 0.1}s`;
            observer.observe(el);
        });

        // Navigation sticky effect
        let lastScroll = 0;
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            const currentScroll = window.pageYOffset;
            
            if (currentScroll > 100) {
                nav.style.background = 'rgba(44, 62, 80, 0.95)';
            } else {
                nav.style.background = 'linear-gradient(135deg, var(--dark-slate), var(--glacier-blue))';
            }
            
            lastScroll = currentScroll;
        });
    </script>
</body>
</html>
