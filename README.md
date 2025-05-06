<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inmobiliaria Pinilla y Aguilera</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background-color: #ffffff;
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background-color: #000;
            color: #fff;
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #ff6600;
        }
        
        .btn {
            display: inline-block;
            background-color: #ff6600;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #e55c00;
        }
        
        /* Hero Section */
        .hero {
            height: 70vh;
            background-image: url('/api/placeholder/1200/600');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            position: relative;
        }
        
        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            color: #fff;
            max-width: 600px;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        
        .hero p {
            font-size: 18px;
            margin-bottom: 30px;
        }
        
        /* Services Section */
        .services {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 36px;
            margin-bottom: 50px;
            color: #000;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background-color: #f9f9f9;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .service-card h3 {
            font-size: 24px;
            margin-bottom: 15px;
            color: #000;
        }
        
        .service-card p {
            margin-bottom: 20px;
        }
        
        .service-icon {
            font-size: 48px;
            margin-bottom: 20px;
            color: #ff6600;
        }
        
        /* About Section */
        .about {
            padding: 80px 0;
            background-color: #f5f5f5;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }
        
        .about-image {
            border-radius: 10px;
            overflow: hidden;
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .about-text h2 {
            font-size: 36px;
            margin-bottom: 20px;
            color: #000;
        }
        
        .about-text p {
            margin-bottom: 20px;
        }
        
        /* Contact Section */
        .contact {
            padding: 80px 0;
        }
        
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }
        
        .contact-info h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: #000;
        }
        
        .contact-info p {
            margin-bottom: 10px;
        }
        
        .contact-info a {
            color: #ff6600;
            text-decoration: none;
        }
        
        .social-links {
            margin-top: 30px;
        }
        
        .social-links a {
            display: inline-block;
            margin-right: 15px;
            color: #ff6600;
            font-size: 24px;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        
        .contact-form textarea {
            height: 150px;
        }
        
        /* Footer */
        footer {
            background-color: #000;
            color: #fff;
            padding: 40px 0;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
        }
        
        .footer-column h3 {
            font-size: 20px;
            margin-bottom: 20px;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #fff;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: #ff6600;
        }
        
        .footer-bottom {
            margin-top: 40px;
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #333;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .service-card {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">Pinilla y Aguilera</div>
                <nav>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#servicios">Servicios</a></li>
                        <li><a href="#propiedades">Propiedades</a></li>
                        <li><a href="#nosotros">Nosotros</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <section class="hero" id="inicio" style="background-image: url('https://images.unsplash.com/photo-1560518883-ce09059eeffa?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80')">
        <div class="hero-overlay"></div>
        <div class="container">
            <div class="hero-content">
                <h1>Expertos inmobiliarios a su servicio</h1>
                <p>En Pinilla y Aguilera le asesoramos en todas sus necesidades inmobiliarias dentro y fuera de Bogotá.</p>
                <a href="#contacto" class="btn">Contáctenos hoy</a>
            </div>
        </div>
    </section>

    <section class="services" id="servicios">
        <div class="container">
            <h2 class="section-title">Nuestros Servicios</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon"><img src="https://images.unsplash.com/photo-1560518883-f5139ba6a714?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Compra y Venta" style="width: 100%; height: 150px; object-fit: cover; border-radius: 5px; margin-bottom: 15px;"></div>
                    <h3>Asesoría en Venta y Compra</h3>
                    <p>Ofrecemos asesoría profesional para la compra y venta de inmuebles dentro y fuera de Bogotá.</p>
                    <a href="#contacto" class="btn">Más información</a>
                </div>
                <div class="service-card">
                    <div class="service-icon"><img src="https://images.unsplash.com/photo-1582268611958-ebfd161ef9cf?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Arriendo de Inmuebles" style="width: 100%; height: 150px; object-fit: cover; border-radius: 5px; margin-bottom: 15px;"></div>
                    <h3>Arriendo de Inmuebles</h3>
                    <p>Gestionamos el arriendo de su propiedad con garantías y seguridad para propietarios e inquilinos.</p>
                    <a href="#contacto" class="btn">Más información</a>
                </div>
                <div class="service-card">
                    <div class="service-icon"><img src="https://images.unsplash.com/photo-1542818212-9899bafcb9db?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Avalúos" style="width: 100%; height: 150px; object-fit: cover; border-radius: 5px; margin-bottom: 15px;"></div>
                    <h3>Avalúos Urbanos y Rurales</h3>
                    <p>Realizamos avalúos profesionales para determinar el valor real de su propiedad urbana o rural.</p>
                    <a href="#contacto" class="btn">Más información</a>
                </div>
                <div class="service-card">
                    <div class="service-icon"><img src="https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Seguros" style="width: 100%; height: 150px; object-fit: cover; border-radius: 5px; margin-bottom: 15px;"></div>
                    <h3>Pólizas de Seguros</h3>
                    <p>Asesoría en la adquisición de pólizas de seguros para hogar, propiedades y vehículos.</p>
                    <a href="#contacto" class="btn">Más información</a>
                </div>
                <div class="service-card">
                    <div class="service-icon"><img src="https://images.unsplash.com/photo-1548199973-03cce0bbc87b?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Seguro para Mascotas" style="width: 100%; height: 150px; object-fit: cover; border-radius: 5px; margin-bottom: 15px;"></div>
                    <h3>Seguro para Mascotas</h3>
                    <p>Ofrecemos soluciones para proteger a los miembros más peludos de su familia.</p>
                    <a href="#contacto" class="btn">Más información</a>
                </div>
            </div>
        </div>
    </section>

    <section class="about" id="nosotros">
        <div class="container">
            <div class="about-content">
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1556912172-45b7abe8b7e1?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Inmobiliaria Pinilla y Aguilera">
                </div>
                <div class="about-text">
                    <h2>Sobre Pinilla y Aguilera</h2>
                    <p>Somos una inmobiliaria comprometida con brindar el mejor servicio a nuestros clientes. Nuestra experiencia en el mercado inmobiliario de Bogotá nos permite ofrecer soluciones adaptadas a las necesidades de cada cliente.</p>
                    <p>Con un equipo de profesionales altamente capacitados, garantizamos transparencia, eficiencia y compromiso en cada uno de nuestros servicios.</p>
                    <a href="#contacto" class="btn">Conozca más sobre nosotros</a>
                </div>
            </div>
        </div>
    </section>
    
    <section class="properties" id="propiedades" style="padding: 80px 0; background-color: #f9f9f9;">
        <div class="container">
            <h2 class="section-title">Propiedades Destacadas</h2>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon"><img src="https://images.unsplash.com/photo-1605276374104-dee2a0ed3cd6?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Apartamento en Chapinero" style="width: 100%; height: 200px; object-fit: cover; border-radius: 5px; margin-bottom: 15px;"></div>
                    <h3>Apartamento en Chapinero</h3>
                    <p>Moderno apartamento de 3 habitaciones con vista panorámica. 110 m², 2 baños, parqueadero.</p>
                    <a href="#contacto" class="btn">Más información</a>
                </div>
                <div class="service-card">
                    <div class="service-icon"><img src="https://images.unsplash.com/photo-1570129477492-45c003edd2be?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Casa en Usaquén" style="width: 100%; height: 200px; object-fit: cover; border-radius: 5px; margin-bottom: 15px;"></div>
                    <h3>Casa en Usaquén</h3>
                    <p>Hermosa casa de 2 plantas, 4 habitaciones, jardín y terraza. 220 m², zona residencial exclusiva.</p>
                    <a href="#contacto" class="btn">Más información</a>
                </div>
                <div class="service-card">
                    <div class="service-icon"><img src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?ixlib=rb-4.0.3&auto=format&fit=crop&w=300&q=80" alt="Oficina en Centro" style="width: 100%; height: 200px; object-fit: cover; border-radius: 5px; margin-bottom: 15px;"></div>
                    <h3>Oficina en Centro</h3>
                    <p>Espacio corporativo de 85 m² con excelente ubicación. Ideal para empresas en crecimiento.</p>
                    <a href="#contacto" class="btn">Más información</a>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contacto">
        <div class="container">
            <h2 class="section-title">Contáctenos</h2>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Información de contacto</h3>
                    <p><strong>Dirección:</strong> Carrera 9 # 13-36 oficina 305, Bogotá</p>
                    <p><strong>Celular:</strong> <a href="tel:3041086662">304 1086662</a></p>
                    <p><strong>Correo:</strong> <a href="mailto:mauriciopinilla2012@gmail.com">mauriciopinilla2012@gmail.com</a></p>
                    
                    <div class="social-links">
                        <h3>Redes Sociales</h3>
                        <a href="https://www.facebook.com/InmobiliariaPinillayAguilera/?locale=es_LA" target="_blank">Facebook</a>
                        <a href="https://www.instagram.com/ormapium?igsh=d2dmbzgzeHpxdzh4" target="_blank">Instagram</a>
                    </div>
                    
                    <div style="margin-top: 30px;">
                        <img src="https://images.unsplash.com/photo-1579621970795-87facc2f976d?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Oficina Pinilla y Aguilera" style="width: 100%; border-radius: 10px; margin-top: 20px;">
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Envíenos un mensaje</h3>
                    <form>
                        <input type="text" placeholder="Nombre completo" required>
                        <input type="email" placeholder="Correo electrónico" required>
                        <input type="tel" placeholder="Número de teléfono">
                        <textarea placeholder="Su mensaje" required></textarea>
                        <button type="submit" class="btn">Enviar mensaje</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Pinilla y Aguilera</h3>
                    <p>Su mejor opción en servicios inmobiliarios dentro y fuera de Bogotá.</p>
                </div>
                <div class="footer-column">
                    <h3>Enlaces rápidos</h3>
                    <ul>
                        <li><a href="#inicio">Inicio</a></li>
                        <li><a href="#servicios">Servicios</a></li>
                        <li><a href="#propiedades">Propiedades</a></li>
                        <li><a href="#nosotros">Nosotros</a></li>
                        <li><a href="#contacto">Contacto</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Servicios</h3>
                    <ul>
                        <li><a href="#servicios">Compra y Venta</a></li>
                        <li><a href="#servicios">Arriendo</a></li>
                        <li><a href="#servicios">Avalúos</a></li>
                        <li><a href="#servicios">Seguros</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contacto</h3>
                    <p>Carrera 9 # 13-36 oficina 305</p>
                    <p>Bogotá, Colombia</p>
                    <p>304 1086662</p>
                    <p>mauriciopinilla2012@gmail.com</p>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 Inmobiliaria Pinilla y Aguilera. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>
</body>
</html>
