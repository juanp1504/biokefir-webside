<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BioKéfir Liofilizado - Probióticos Reales y Naturales</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }
        
        /* Header */
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: #ffeb3b;
        }
        
        .cta-button {
            background: #ff6b6b;
            color: white;
            padding: 0.5rem 1.5rem;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        
        .cta-button:hover {
            transform: scale(1.05);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 120px 0 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="2" fill="white" opacity="0.1"/></svg>') repeat;
            animation: float 20s infinite linear;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            100% { transform: translateY(-100px); }
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 2rem;
            position: relative;
            z-index: 1;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            animation: slideInDown 1s ease-out;
        }
        
        .hero-subtitle {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            animation: slideInUp 1s ease-out 0.2s both;
        }
        
        .hero-description {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.8;
            animation: slideInUp 1s ease-out 0.4s both;
        }
        
        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
            animation: slideInUp 1s ease-out 0.6s both;
        }
        
        .btn-primary {
            background: #ff6b6b;
            color: white;
            padding: 1rem 2rem;
            border: none;
            border-radius: 30px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }
        
        .btn-secondary {
            background: transparent;
            color: white;
            border: 2px solid white;
            padding: 1rem 2rem;
            border-radius: 30px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(255, 107, 107, 0.3);
        }
        
        .btn-secondary:hover {
            background: white;
            color: #667eea;
        }
        
        /* Features Section */
        .features {
            padding: 80px 0;
            background: #f8f9fa;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .feature-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
        }
        
        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: #667eea;
        }
        
        /* Benefits Section */
        .benefits {
            padding: 80px 0;
            background: white;
        }
        
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .benefit-item {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            padding: 1.5rem;
            background: #f8f9fa;
            border-radius: 10px;
            transition: all 0.3s;
        }
        
        .benefit-item:hover {
            background: #e3f2fd;
            transform: translateX(10px);
        }
        
        .benefit-icon {
            font-size: 2rem;
            color: #667eea;
            flex-shrink: 0;
        }
        
        .benefit-content h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: #333;
        }
        
        /* Product Section */
        .product {
            padding: 80px 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }
        
        .product-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        
        .product-image {
            background: white;
            border-radius: 20px;
            padding: 2rem;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            text-align: center;
        }
        
        .product-mockup {
            width: 100%;
            max-width: 300px;
            height: 400px;
            background: linear-gradient(45deg, #ff6b6b, #feca57);
            border-radius: 15px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }
        
        .product-info h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }
        
        .product-features {
            list-style: none;
            margin: 2rem 0;
        }
        
        .product-features li {
            margin: 1rem 0;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .product-features li::before {
            content: '✓';
            color: #4CAF50;
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        /* Testimonials */
        .testimonials {
            padding: 80px 0;
            background: #f8f9fa;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }
        
        .testimonial {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
            position: relative;
        }
        
        .testimonial::before {
            content: '"';
            font-size: 4rem;
            color: #667eea;
            position: absolute;
            top: -10px;
            left: 20px;
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1rem;
            font-size: 1.1rem;
            line-height: 1.6;
        }
        
        .testimonial-author {
            font-weight: bold;
            color: #667eea;
        }
        
        /* CTA Section */
        .cta-section {
            padding: 80px 0;
            background: linear-gradient(135deg, #ff6b6b 0%, #feca57 100%);
            color: white;
            text-align: center;
        }
        
        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .cta-section p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        /* Footer */
        .footer {
            background: #333;
            color: white;
            padding: 40px 0;
            text-align: center;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-section h3 {
            margin-bottom: 1rem;
            color: #667eea;
        }
        
        .footer-section p, .footer-section a {
            color: #ccc;
            text-decoration: none;
        }
        
        .footer-section a:hover {
            color: #667eea;
        }
        
        .footer-bottom {
            border-top: 1px solid #555;
            padding-top: 2rem;
            margin-top: 2rem;
        }
        
        /* animations */
        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
            
            .product-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .nav-links {
                display: none;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <nav class="nav">
            <div class="logo">
                🥛 BioKéfir Liofilizado
            </div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#producto">Producto</a></li>
                <li><a href="#beneficios">Beneficios</a></li>
                <li><a href="#testimonios">Testimonios</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
            <button class="cta-button">Comprar Ahora</button>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <h1>BioKéfir Liofilizado</h1>
            <p class="hero-subtitle">"Probióticos reales, naturales y portátiles. Bienestar que sí funciona."</p>
            <p class="hero-description">
                El primer kéfir de leche liofilizado que conserva todas sus propiedades probióticas 
                sin necesidad de refrigeración. Más de 30 cepas de bacterias beneficiosas en cada sobre.
            </p>
            <div class="hero-buttons">
                <a href="#producto" class="btn-primary">Conocer el Producto</a>
                <a href="#beneficios" class="btn-secondary">Ver Beneficios</a>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="producto">
        <div class="container">
            <h2 class="section-title">¿Qué hace único a BioKéfir Liofilizado?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🧬</div>
                    <h3>Probióticos Vivos Reales</h3>
                    <p>Contiene más de 30 cepas de bacterias y levaduras beneficiosas, no encapsulados ni industriales.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">❄️</div>
                    <h3>Sin Refrigeración</h3>
                    <p>Se conserva a temperatura ambiente, ideal para llevar a cualquier lugar sin perder propiedades.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⏰</div>
                    <h3>Larga Vida Útil</h3>
                    <p>Hasta 12 meses de duración gracias al proceso de liofilización avanzado.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🌿</div>
                    <h3>100% Natural</h3>
                    <p>Sin químicos, sin aditivos, sin conservantes. Producto completamente natural.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⚡</div>
                    <h3>Fácil de Usar</h3>
                    <p>Solo se disuelve en agua o tu bebida favorita y listo para consumir.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🏆</div>
                    <h3>Producto Premium</h3>
                    <p>Calidad superior que se posiciona como un producto premium saludable.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Benefits Section -->
    <section class="benefits" id="beneficios">
        <div class="container">
            <h2 class="section-title">Beneficios Comprobados del Kéfir</h2>
            <div class="benefits-grid">
                <div class="benefit-item">
                    <div class="benefit-icon">🌟</div>
                    <div class="benefit-content">
                        <h4>Mejora la Digestión</h4>
                        <p>Restaura la flora intestinal y combate el estreñimiento, hinchazón y gases.</p>
                    </div>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">🛡️</div>
                    <div class="benefit-content">
                        <h4>Fortalece el Sistema Inmunológico</h4>
                        <p>70% de tus defensas están en el intestino. Un intestino saludable = sistema inmune fuerte.</p>
                    </div>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">🔥</div>
                    <div class="benefit-content">
                        <h4>Reduce la Inflamación</h4>
                        <p>Actúa como antiinflamatorio natural desde el intestino, equilibrando el pH corporal.</p>
                    </div>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">🧠</div>
                    <div class="benefit-content">
                        <h4>Mejora el Estado de Ánimo</h4>
                        <p>Contribuye al equilibrio de neurotransmisores como la serotonina para el bienestar emocional.</p>
                    </div>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">⚖️</div>
                    <div class="benefit-content">
                        <h4>Favorece la Pérdida de Peso</h4>
                        <p>Mejora el metabolismo y aporta saciedad natural, reduciendo la ansiedad por comer.</p>
                    </div>
                </div>
                <div class="benefit-item">
                    <div class="benefit-icon">✨</div>
                    <div class="benefit-content">
                        <h4>Mejora la Piel y Cabello</h4>
                        <p>Una buena digestión se refleja en piel luminosa, menos acné y cabello más fuerte.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Product Showcase -->
    <section class="product">
        <div class="container">
            <div class="product-content">
                <div class="product-info">
                    <h2>El Futuro de los Probióticos</h2>
                    <p>BioKéfir Liofilizado combina la sabiduría ancestral del kéfir con la tecnología moderna de liofilización.</p>
                    <ul class="product-features">
                        <li>Más de 30 cepas de bacterias beneficiosas</li>
                        <li>Sin necesidad de refrigeración</li>
                        <li>12 meses de vida útil</li>
                        <li>Completamente natural y sin aditivos</li>
                        <li>Fácil de transportar y consumir</li>
                        <li>Apto para intolerantes a la lactosa</li>
                    </ul>
                    <a href="#contacto" class="btn-primary">Realizar Pedido</a>
                </div>
                <div class="product-image">
                    <div class="product-mockup">
                        <div>📦</div>
                        <div>BioKéfir</div>
                        <div>Liofilizado</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials" id="testimonios">
        <div class="container">
            <h2 class="section-title">Lo que Dicen Nuestros Clientes</h2>
            <div class="testimonial-grid">
                <div class="testimonial">
                    <p class="testimonial-text">
                        "Desde que uso BioKéfir mi digestión ha mejorado notablemente. Lo mejor es que puedo llevarlo a cualquier parte sin preocuparme por la refrigeración."
                    </p>
                    <p class="testimonial-author">- María González, Nutricionista</p>
                </div>
                <div class="testimonial">
                    <p class="testimonial-text">
                        "Excelente producto. Es súper práctico y realmente funciona. Mi familia completa lo consume diariamente."
                    </p>
                    <p class="testimonial-author">- Carlos Hernández, Padre de Familia</p>
                </div>
                <div class="testimonial">
                    <p class="testimonial-text">
                        "Como deportista, necesito productos que realmente aporten beneficios. BioKéfir ha mejorado mi recuperación y bienestar general."
                    </p>
                    <p class="testimonial-author">- Ana Martínez, Atleta</p>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta-section">
        <div class="container">
            <h2>¿Listo para Transformar tu Salud Digestiva?</h2>
            <p>Únete a miles de personas que ya han experimentado los beneficios de BioKéfir Liofilizado</p>
            <a href="#contacto" class="btn-secondary">Comprar Ahora</a>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer" id="contacto">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>BioKéfir Liofilizado</h3>
                    <p>Probióticos reales, naturales y portátiles.<br>
                    Bienestar que sí funciona.</p>
                </div>
                <div class="footer-section">
                    <h3>Contacto</h3>
                    <p>📧 info@biokefir.com<br>
                    📱 +57 300 123 4567<br>
                    📍 Dosquebradas, Risaralda, Colombia</p>
                </div>
                <div class="footer-section">
                    <h3>Síguenos</h3>
                    <p>
                        <a href="#">Facebook</a><br>
                        <a href="#">Instagram</a><br>
                        <a href="#">TikTok</a>
                    </p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 BioKéfir Liofilizado. Todos los derechos reservados.<br>
                Desarrollado por Juan Pablo Gómez Hoyos - Estudiante de Química Industrial</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling para los enlaces del menú
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

        // Animación de scroll reveal
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Aplicar animación a las cards
        document.querySelectorAll('.feature-card, .benefit-item, .testimonial').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(30px)';
            el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>
