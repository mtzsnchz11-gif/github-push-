# pandmuerto



<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pan de Muerto Artesanal | Manuel Martínez - Para Empresas en Querétaro</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --naranja: #E87722;
    --naranja-oscuro: #C45A15;
    --morado: #6B2D5B;
    --crema: #FFF5E6;
    --chocolate: #3D2817;
    --dorado: #D4A574;
    --negro: #1A0F0A;
    --blanco: #FFFFFF;
    --gris: #F5F0E8;
    --verde-exito: #25D366;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--crema);
    color: var(--chocolate);
    line-height: 1.6;
    overflow-x: hidden;
  }

  h1, h2, h3, h4 { font-family: 'Playfair Display', serif; }

  /* NAVBAR */
  .navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(26, 15, 10, 0.95);
    backdrop-filter: blur(10px);
    padding: 15px 5%;
    z-index: 1000;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 2px solid var(--naranja);
  }

  .logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    color: var(--crema);
    font-weight: 700;
  }

  .logo span { color: var(--naranja); }

  .nav-links {
    display: flex;
    gap: 30px;
    list-style: none;
  }

  .nav-links a {
    color: var(--crema);
    text-decoration: none;
    font-weight: 500;
    font-size: 0.95rem;
    transition: color 0.3s;
  }

  .nav-links a:hover { color: var(--naranja); }

  .nav-cta {
    background: var(--naranja);
    color: var(--blanco) !important;
    padding: 10px 20px;
    border-radius: 30px;
    font-weight: 600 !important;
  }

  .nav-cta:hover { background: var(--naranja-oscuro); }

  .menu-toggle {
    display: none;
    background: none;
    border: none;
    color: var(--crema);
    font-size: 1.8rem;
    cursor: pointer;
  }

  /* HERO */
  .hero {
    min-height: 100vh;
    background: linear-gradient(135deg, rgba(26, 15, 10, 0.85), rgba(107, 45, 91, 0.75)),
                url('https://images.unsplash.com/photo-1601000938259-9e92002320b2?w=1600') center/cover;
    display: flex;
    align-items: center;
    padding: 120px 5% 80px;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100px;
    background: linear-gradient(to top, var(--crema), transparent);
  }

  .hero-content {
    max-width: 700px;
    color: var(--blanco);
    z-index: 2;
    animation: fadeInUp 1s ease;
  }

  .hero-badge {
    display: inline-block;
    background: var(--naranja);
    color: var(--blanco);
    padding: 8px 20px;
    border-radius: 30px;
    font-size: 0.85rem;
    font-weight: 600;
    margin-bottom: 25px;
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  .hero h1 {
    font-size: clamp(2.5rem, 5vw, 4.5rem);
    line-height: 1.1;
    margin-bottom: 25px;
    font-weight: 900;
  }

  .hero h1 span { color: var(--naranja); }

  .hero p {
    font-size: 1.2rem;
    margin-bottom: 35px;
    opacity: 0.95;
    max-width: 600px;
  }

  .hero-buttons {
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
  }

  .btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 15px 30px;
    border-radius: 50px;
    text-decoration: none;
    font-weight: 600;
    font-size: 1rem;
    transition: all 0.3s;
    border: none;
    cursor: pointer;
  }

  .btn-primary {
    background: var(--naranja);
    color: var(--blanco);
    box-shadow: 0 10px 30px rgba(232, 119, 34, 0.4);
  }

  .btn-primary:hover {
    background: var(--naranja-oscuro);
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(232, 119, 34, 0.5);
  }

  .btn-secondary {
    background: transparent;
    color: var(--blanco);
    border: 2px solid var(--blanco);
  }

  .btn-secondary:hover {
    background: var(--blanco);
    color: var(--chocolate);
  }

  /* SECTIONS */
  section { padding: 80px 5%; }

  .section-header {
    text-align: center;
    max-width: 700px;
    margin: 0 auto 60px;
  }

  .section-header h2 {
    font-size: clamp(2rem, 4vw, 3rem);
    color: var(--chocolate);
    margin-bottom: 15px;
  }

  .section-header p {
    color: #6B5D4F;
    font-size: 1.1rem;
  }

  .section-divider {
    width: 80px;
    height: 4px;
    background: var(--naranja);
    margin: 20px auto;
    border-radius: 2px;
  }

  /* BENEFICIOS */
  .beneficios {
    background: var(--blanco);
  }

  .beneficios-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
    max-width: 1200px;
    margin: 0 auto;
  }

  .beneficio-card {
    background: var(--gris);
    padding: 35px 25px;
    border-radius: 20px;
    text-align: center;
    transition: all 0.4s;
    border: 2px solid transparent;
  }

  .beneficio-card:hover {
    transform: translateY(-10px);
    border-color: var(--naranja);
    box-shadow: 0 20px 40px rgba(61, 40, 23, 0.1);
  }

  .beneficio-icon {
    width: 70px;
    height: 70px;
    background: var(--naranja);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 20px;
    font-size: 2rem;
  }

  .beneficio-card h3 {
    font-size: 1.25rem;
    margin-bottom: 15px;
    color: var(--chocolate);
  }

  .beneficio-card p {
    color: #6B5D4F;
    font-size: 0.95rem;
  }

  /* CATÁLOGO */
  .catalogo {
    background: linear-gradient(180deg, var(--crema), var(--gris));
  }

  .catalogo-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    max-width: 1300px;
    margin: 0 auto;
  }

  .producto-card {
    background: var(--blanco);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 10px 30px rgba(61, 40, 23, 0.1);
    transition: all 0.4s;
    position: relative;
  }

  .producto-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 20px 50px rgba(61, 40, 23, 0.2);
  }

  .producto-img {
    width: 100%;
    height: 280px;
    object-fit: cover;
    display: block;
    transition: transform 0.5s;
  }

  .producto-card:hover .producto-img {
    transform: scale(1.05);
  }

  .producto-img-container {
    overflow: hidden;
    position: relative;
  }

  .producto-tag {
    position: absolute;
    top: 15px;
    right: 15px;
    background: var(--naranja);
    color: var(--blanco);
    padding: 6px 15px;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: 600;
    z-index: 2;
  }

  .producto-info {
    padding: 25px;
  }

  .producto-info h3 {
    font-size: 1.3rem;
    margin-bottom: 10px;
    color: var(--chocolate);
  }

  .producto-info p {
    color: #6B5D4F;
    font-size: 0.95rem;
    margin-bottom: 15px;
  }

  .producto-precio {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 15px;
    border-top: 1px solid #EEE;
  }

  .precio-item {
    text-align: center;
  }

  .precio-label {
    font-size: 0.75rem;
    color: #999;
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  .precio-valor {
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--naranja);
    font-family: 'Playfair Display', serif;
  }

  /* PRECIOS Y CONDICIONES */
  .precios {
    background: var(--chocolate);
    color: var(--crema);
    position: relative;
    overflow: hidden;
  }

  .precios::before {
    content: '';
    position: absolute;
    top: -50px;
    right: -50px;
    width: 300px;
    height: 300px;
    background: var(--naranja);
    border-radius: 50%;
    opacity: 0.1;
  }

  .precios .section-header h2 { color: var(--crema); }
  .precios .section-header p { color: var(--dorado); }

  .tabla-precios {
    max-width: 900px;
    margin: 0 auto;
    background: var(--blanco);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
  }

  .tabla-header {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    background: var(--naranja);
    color: var(--blanco);
    padding: 20px 30px;
    font-weight: 700;
    font-size: 1.1rem;
  }

  .tabla-row {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    padding: 25px 30px;
    border-bottom: 1px solid #EEE;
    align-items: center;
    transition: background 0.3s;
  }

  .tabla-row:hover { background: var(--gris); }
  .tabla-row:last-child { border-bottom: none; }

  .tabla-row .tipo {
    font-weight: 700;
    color: var(--chocolate);
    font-size: 1.05rem;
  }

  .tabla-row .cantidad {
    color: #6B5D4F;
    font-size: 0.95rem;
  }

  .tabla-row .precio {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    font-weight: 700;
    color: var(--naranja);
    text-align: right;
  }

  .tabla-row.destacada {
    background: linear-gradient(90deg, var(--crema), var(--blanco));
    border-left: 5px solid var(--naranja);
  }

  .tabla-row.destacada .tipo::after {
    content: ' ⭐';
  }

  .condiciones-comerciales {
    max-width: 900px;
    margin: 40px auto 0;
    background: rgba(255, 255, 255, 0.1);
    border: 1px solid var(--dorado);
    border-radius: 15px;
    padding: 25px;
    text-align: center;
  }

  .condiciones-comerciales h4 {
    color: var(--dorado);
    margin-bottom: 15px;
    font-size: 1.2rem;
  }

  .condiciones-comerciales ul {
    list-style: none;
    color: var(--crema);
    font-size: 0.95rem;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
  }

  .condiciones-comerciales li {
    display: flex;
    align-items: center;
    gap: 8px;
  }

  /* RECOLECCIÓN */
  .recoleccion {
    background: var(--blanco);
  }

  .recoleccion-container {
    max-width: 1000px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    align-items: center;
  }

  .recoleccion-info {
    background: var(--gris);
    padding: 35px;
    border-radius: 20px;
    border-left: 5px solid var(--naranja);
  }

  .recoleccion-info h3 {
    font-size: 1.5rem;
    margin-bottom: 20px;
    color: var(--chocolate);
  }

  .recoleccion-info p {
    color: #6B5D4F;
    margin-bottom: 15px;
    font-size: 1rem;
  }

  .recoleccion-info .highlight {
    background: var(--naranja);
    color: var(--blanco);
    padding: 15px;
    border-radius: 10px;
    margin-top: 20px;
    font-weight: 600;
  }

  .recoleccion-img {
    width: 100%;
    border-radius: 20px;
    box-shadow: 0 20px 50px rgba(61, 40, 23, 0.2);
  }

  /* CTA FINAL */
  .cta-final {
    background: linear-gradient(135deg, var(--morado), var(--naranja-oscuro));
    color: var(--blanco);
    text-align: center;
    padding: 100px 5%;
  }

  .cta-final h2 {
    font-size: clamp(2rem, 4vw, 3.5rem);
    margin-bottom: 20px;
  }

  .cta-final p {
    font-size: 1.2rem;
    margin-bottom: 35px;
    opacity: 0.95;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
  }

  .cta-final .btn-primary {
    background: var(--blanco);
    color: var(--morado);
    font-size: 1.1rem;
    padding: 18px 40px;
  }

  .cta-final .btn-primary:hover {
    background: var(--crema);
  }

  /* FOOTER */
  footer {
    background: var(--negro);
    color: var(--crema);
    padding: 60px 5% 30px;
  }

  .footer-content {
    max-width: 1200px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 40px;
    margin-bottom: 40px;
  }

  .footer-col h4 {
    font-size: 1.3rem;
    margin-bottom: 20px;
    color: var(--naranja);
  }

  .footer-col p, .footer-col a {
    color: #B8A99A;
    text-decoration: none;
    display: block;
    margin-bottom: 10px;
    transition: color 0.3s;
  }

  .footer-col a:hover { color: var(--naranja); }

  .footer-contact-item {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 15px;
  }

  .footer-contact-item .icon {
    font-size: 1.3rem;
  }

  .footer-bottom {
    border-top: 1px solid #3D2817;
    padding-top: 25px;
    text-align: center;
    color: #6B5D4F;
    font-size: 0.9rem;
  }

  /* WHATSAPP FLOTANTE */
  .whatsapp-float {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 65px;
    height: 65px;
    background: var(--verde-exito);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 10px 30px rgba(37, 211, 102, 0.4);
    z-index: 999;
    animation: pulse 2s infinite;
    text-decoration: none;
    transition: transform 0.3s;
  }

  .whatsapp-float:hover {
    transform: scale(1.1);
  }

  .whatsapp-float svg {
    width: 35px;
    height: 35px;
    fill: white;
  }

  @keyframes pulse {
    0% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7); }
    70% { box-shadow: 0 0 0 20px rgba(37, 211, 102, 0); }
    100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
  }

  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* RESPONSIVE */
  @media (max-width: 768px) {
    .nav-links {
      display: none;
      position: absolute;
      top: 100%;
      left: 0;
      right: 0;
      background: var(--negro);
      flex-direction: column;
      padding: 20px;
      gap: 15px;
    }

    .nav-links.active { display: flex; }
    .menu-toggle { display: block; }
    .hero { padding: 100px 5% 60px; }

    .tabla-header, .tabla-row {
      grid-template-columns: 1fr;
      gap: 10px;
      text-align: center;
    }

    .tabla-row .precio { text-align: center; }
    .recoleccion-container { grid-template-columns: 1fr; }
    .recoleccion-img { order: -1; }
    section { padding: 60px 5%; }
    
    .condiciones-comerciales ul {
      flex-direction: column;
      gap: 10px;
    }
  }
</style>
</head>
<body>

<!-- NAVBAR -->
<nav class="navbar">
  <div class="logo">Pan de <span>Muerto</span> MM</div>
  <ul class="nav-links" id="navLinks">
    <li><a href="#inicio">Inicio</a></li>
    <li><a href="#beneficios">Beneficios</a></li>
    <li><a href="#catalogo">Catálogo</a></li>
    <li><a href="#precios">Precios</a></li>
    <li><a href="#contacto" class="nav-cta">Cotizar</a></li>
  </ul>
  <button class="menu-toggle" onclick="toggleMenu()">☰</button>
</nav>

<!-- HERO -->
<section class="hero" id="inicio">
  <div class="hero-content">
    <span class="hero-badge">🎃 Temporada 2026</span>
    <h1>Pan de Muerto <span>Artesanal</span> para tu Empresa</h1>
    <p>Calidad, puntualidad y facturación para comedores industriales, fábricas y oficinas en Querétaro. El detalle perfecto para tus colaboradores.</p>
    <div class="hero-buttons">
      <a href="https://wa.me/527208777490?text=Hola%20Manuel,%20me%20interesa%20cotizar%20pan%20de%20muerto%20para%20mi%20empresa.%20%C2%BFPodr%C3%ADa%20enviarme%20los%20precios%20para%2050%20o%20100%20piezas?" class="btn btn-primary" target="_blank">
         Cotizar por WhatsApp
      </a>
      <a href="#catalogo" class="btn btn-secondary">Ver Catálogo</a>
    </div>
  </div>
</section>

<!-- BENEFICIOS -->
<section class="beneficios" id="beneficios">
  <div class="section-header">
    <h2>¿Por qué elegirnos?</h2>
    <div class="section-divider"></div>
    <p>Más de 30 años de experiencia en administración, logística y ventas al servicio de tu empresa</p>
  </div>
  <div class="beneficios-grid">
    <div class="beneficio-card">
      <div class="beneficio-icon">📄</div>
      <h3>Facturación Disponible</h3>
      <p>Contamos con facturación electrónica (CFDI). Consulta los requisitos y ajustes correspondientes.</p>
    </div>
    <div class="beneficio-card">
      <div class="beneficio-icon">🎯</div>
      <h3>Recolección Programada</h3>
      <p>Acuerda fecha y hora para recoger tu pedido fresco y en el momento exacto que lo necesites.</p>
    </div>
    <div class="beneficio-card">
      <div class="beneficio-icon">🤝</div>
      <h3>Atención B2B Profesional</h3>
      <p>Entendemos las necesidades de compras corporativas y Recursos Humanos. Trato directo y serio.</p>
    </div>
    <div class="beneficio-card">
      <div class="beneficio-icon">🍰</div>
      <h3>Degustación Sin Compromiso</h3>
      <p>¿Pedido mayor a 100 piezas? Te llevamos muestras gratis para que tu equipo valide la calidad antes de comprar.</p>
    </div>
  </div>
</section>

<!-- CATÁLOGO -->
<section class="catalogo" id="catalogo">
  <div class="section-header">
    <h2>Nuestro Catálogo</h2>
    <div class="section-divider"></div>
    <p>Variedad de opciones para satisfacer todos los gustos de tus colaboradores</p>
  </div>
  <div class="catalogo-grid">
    
    <!-- TIP PARA MANUEL: Cuando cambies esta foto, usa una donde el pan esté CORTADO A LA MITAD para que se vea el relleno. ¡Eso vende mucho más! -->
    <div class="producto-card">
      <div class="producto-img-container">
        <span class="producto-tag">Clásico</span>
        <img src="https://images.unsplash.com/photo-1601000938259-9e92002320b2?w=600" alt="Pan de Muerto Tradicional" class="producto-img">
      </div>
      <div class="producto-info">
        <h3>Pan de Muerto Tradicional</h3>
        <p>El clásico de siempre, suave y con el auténtico sabor a azahar. Espolvoreado con azúcar.</p>
        <div class="producto-precio">
          <div class="precio-item">
            <div class="precio-label">1-49 pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
          <div class="precio-item">
            <div class="precio-label">50+ pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
        </div>
      </div>
    </div>

    <div class="producto-card">
      <div class="producto-img-container">
        <span class="producto-tag">Premium</span>
        <!-- TIP: Foto del pan relleno de crema cortado a la mitad -->
        <img src="https://images.unsplash.com/photo-1634712282287-14ed57b9cc89?w=600" alt="Pan de Muerto Relleno de Crema" class="producto-img">
      </div>
      <div class="producto-info">
        <h3>Relleno de Crema Pastelera</h3>
        <p>Opción premium con abundante crema pastelera casera. El favorito de muchos colaboradores.</p>
        <div class="producto-precio">
          <div class="precio-item">
            <div class="precio-label">1-49 pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
          <div class="precio-item">
            <div class="precio-label">50+ pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
        </div>
      </div>
    </div>

    <div class="producto-card">
      <div class="producto-img-container">
        <span class="producto-tag">Favorito</span>
        <!-- TIP: Foto del pan relleno de chocolate cortado a la mitad -->
        <img src="https://images.unsplash.com/photo-1509440159596-0249088772ff?w=600" alt="Pan de Muerto Relleno de Chocolate" class="producto-img">
      </div>
      <div class="producto-info">
        <h3>Relleno de Chocolate</h3>
        <p>Relleno generoso de chocolate. Una delicia irresistible para los amantes del cacao.</p>
        <div class="producto-precio">
          <div class="precio-item">
            <div class="precio-label">1-49 pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
          <div class="precio-item">
            <div class="precio-label">50+ pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
        </div>
      </div>
    </div>

    <div class="producto-card">
      <div class="producto-img-container">
        <span class="producto-tag">Dulce</span>
        <!-- TIP: Foto del pan relleno de cajeta cortado a la mitad -->
        <img src="https://images.unsplash.com/photo-1586985289688-ca3cf47d3e6e?w=600" alt="Pan de Muerto Relleno de Cajeta" class="producto-img">
      </div>
      <div class="producto-info">
        <h3>Relleno de Cajeta</h3>
        <p>Sabor tradicional mexicano con relleno cremoso de cajeta. Perfecto para los paladares dulces.</p>
        <div class="producto-precio">
          <div class="precio-item">
            <div class="precio-label">1-49 pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
          <div class="precio-item">
            <div class="precio-label">50+ pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
        </div>
      </div>
    </div>

    <div class="producto-card">
      <div class="producto-img-container">
        <span class="producto-tag">Especial</span>
        <img src="https://images.unsplash.com/photo-1509365465985-25d11c17e812?w=600" alt="Pan de Muerto de Chocolate" class="producto-img">
      </div>
      <div class="producto-info">
        <h3>Pan de Muerto de Chocolate</h3>
        <p>Masa de chocolate con el sabor tradicional. Para los paladares más exigentes.</p>
        <div class="producto-precio">
          <div class="precio-item">
            <div class="precio-label">1-49 pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
          <div class="precio-item">
            <div class="precio-label">50+ pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
        </div>
      </div>
    </div>

    <div class="producto-card">
      <div class="producto-img-container">
        <span class="producto-tag">Combo</span>
        <img src="https://images.unsplash.com/photo-1572441713132-c542fc4fe282?w=600" alt="Combo Pan de Muerto con Chocolate" class="producto-img">
      </div>
      <div class="producto-info">
        <h3>Combo Merienda Completa</h3>
        <p>Pan de muerto tradicional + chocolate de taza. La experiencia completa de Día de Muertos.</p>
        <div class="producto-precio">
          <div class="precio-item">
            <div class="precio-label">1-49 pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
          <div class="precio-item">
            <div class="precio-label">50+ pzas</div>
            <div class="precio-valor">$XX</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PRECIOS Y CONDICIONES -->
<section class="precios" id="precios">
  <div class="section-header">
    <h2>Tabla de Precios y Condiciones</h2>
    <div class="section-divider"></div>
    <p>Precios especiales para empresas. A mayor volumen, mejor precio.</p>
  </div>
  
  <div class="tabla-precios">
    <div class="tabla-header">
      <div>Tipo de Pedido</div>
      <div>Cantidad</div>
      <div style="text-align: right;">Precio por Pieza</div>
    </div>
    <div class="tabla-row">
      <div class="tipo">Menudeo / Grupos Pequeños</div>
      <div class="cantidad">1 a 49 piezas</div>
      <div class="precio">$ [Precio 1]</div>
    </div>
    <div class="tabla-row destacada">
      <div class="tipo">Mayoreo / Empresas</div>
      <div class="cantidad">50 piezas en adelante</div>
      <div class="precio">$ [Precio 2]</div>
    </div>
  </div>

  <!-- SECCIÓN DE CONDICIONES COMERCIALES (PRUDENCIA) -->
  <div class="condiciones-comerciales">
    <h4> Condiciones Comerciales Claras y Transparentes</h4>
    <ul>
      <li>💳 <strong>Pago:</strong> 50% de anticipo para agendar producción, 50% al recoger el pedido.</li>
      <li>📄 <strong>Facturación:</strong> Contamos con facturación electrónica (CFDI). Consulta requisitos y ajustes.</li>
      <li> <strong>Recolección:</strong> Acuerda fecha y hora para recoger tu pedido en punto acordado.</li>
    </ul>
  </div>

  <p style="text-align: center; margin-top: 30px; color: var(--dorado); font-size: 0.95rem;">
    Los precios se actualizan semanalmente según el mercado. Solicita tu cotización personalizada hoy mismo.
  </p>
</section>

<!-- RECOLECCIÓN -->
<section class="recoleccion">
  <div class="section-header">
    <h2>Recolección de Pedidos</h2>
    <div class="section-divider"></div>
    <p>Programa la recolección de tu pedido fresco y en el momento que lo necesites</p>
  </div>
  <div class="recoleccion-container">
    <div class="recoleccion-info">
      <h3>📍 ¿Cómo funciona?</h3>
      <p><strong>1. Haz tu pedido:</strong> Cotiza y aparta tu pan de muerto con al menos 48 horas de anticipación.</p>
      <p><strong>2. Agenda la recolección:</strong> Acuerda el día y hora exacta para recoger tu pedido en el punto acordado en Querétaro.</p>
      <p><strong>3. Recoge fresco:</strong> Tu pan estará listo y empacado, fresco para tus colaboradores.</p>
      <div class="highlight">
         Pedidos empresariales: Coordinamos la recolección directamente en tu empresa para tu comodidad (sujeto a zona y volumen del pedido).
      </div>
    </div>
    <img src="https://images.unsplash.com/photo-1556910103-1c02745aae8d?w=600" alt="Recolección de pan fresco" class="recoleccion-img">
  </div>
</section>

<!-- CTA FINAL -->
<section class="cta-final" id="contacto">
  <h2>¿Listo para hacer tu pedido?</h2>
  <p>Contáctanos directamente para cotizar, agendar tu degustación o resolver dudas sobre facturación. Atención personalizada y respuesta inmediata.</p>
  <a href="https://wa.me/527208777490?text=Hola%20Manuel,%20vi%20su%20p%C3%A1gina%20web%20y%20me%20interesa%20cotizar%20pan%20de%20muerto%20para%20mi%20empresa.%20%C2%BFPodr%C3%ADa%20indicarme%20los%20precios%20por%20mayoreo%20y%20los%20detalles%20de%20recolecci%C3%B3n?" class="btn btn-primary" target="_blank">
    📱 Escríbenos por WhatsApp Ahora
  </a>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-content">
    <div class="footer-col">
      <h4>Pan de Muerto MM</h4>
      <p>Servicio profesional de venta de pan de muerto artesanal para empresas, comedores industriales y oficinas en Querétaro. Calidad y confianza en cada pedido.</p>
    </div>
    <div class="footer-col">
      <h4>Contacto Directo</h4>
      <div class="footer-contact-item">
        <span class="icon">📱</span>
        <a href="tel:7208777490">720 877 7490</a>
      </div>
      <div class="footer-contact-item">
        <span class="icon">✉️</span>
        <a href="mailto:mtzsnchz11@gmail.com">mtzsnchz11@gmail.com</a>
      </div>
      <div class="footer-contact-item">
        <span class="icon">📍</span>
        <span>Querétaro, Qro.</span>
      </div>
    </div>
    <div class="footer-col">
      <h4>Enlaces Rápidos</h4>
      <a href="#inicio">Inicio</a>
      <a href="#catalogo">Catálogo</a>
      <a href="#precios">Precios y Condiciones</a>
      <a href="#contacto">Contacto</a>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2026 Manuel Asbel Martínez Sánchez. Todos los derechos reservados. | Hecho con ❤️ en Querétaro</p>
  </div>
</footer>

<!-- WHATSAPP FLOTANTE -->
<a href="https://wa.me/527208777490?text=Hola%20Manuel,%20vi%20su%20p%C3%A1gina%20web%20y%20me%20interesa%20cotizar%20pan%20de%20muerto%20para%20mi%20empresa.%20%C2%BFPodr%C3%ADa%20indicarme%20los%20precios%20por%20mayoreo%20y%20los%20detalles%20de%20recolecci%C3%B3n?" class="whatsapp-float" target="_blank" aria-label="WhatsApp">
  <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
  </svg>
</a>

<script>
  function toggleMenu() {
    document.getElementById('navLinks').classList.toggle('active');
  }

  document.querySelectorAll('.nav-links a').forEach(link => {
    link.addEventListener('click', () => {
      document.getElementById('navLinks').classList.remove('active');
    });
  });

  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) {
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.beneficio-card, .producto-card').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(30px)';
    el.style.transition = 'all 0.6s ease';
    observer.observe(el);
  });
</script>

</body>
</html>