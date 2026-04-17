<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sebastián Araya | Automatización Digital</title>
  
  <!-- Tipografía Google Fonts: Inter -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  
  <!-- Iconos FontAwesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <style>
    :root {
      --bg-color: #0f172a;
      --card-bg: #1e293b;
      --text-primary: #f1f5f9;
      --text-secondary: #94a3b8;
      --accent: #38bdf8; /* Azul Cyan */
      --whatsapp: #25D366;
      --whatsapp-hover: #1ebc57;
      --border: #334155;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background-color: var(--bg-color);
      color: var(--text-primary);
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    .container {
      width: 90%;
      max-width: 1100px;
      margin: 0 auto;
      padding: 20px;
    }

    /* Header / Hero Section */
    header {
      text-align: center;
      padding: 80px 0 40px;
      background: radial-gradient(circle at center, #1e293b 0%, #0f172a 70%);
    }

    h1 {
      font-size: 3rem;
      margin-bottom: 10px;
      background: linear-gradient(90deg, #38bdf8, #818cf8);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      font-weight: 800;
    }

    .subtitle {
      font-size: 1.25rem;
      color: var(--text-secondary);
      max-width: 600px;
      margin: 0 auto 40px;
    }

    .intro-card {
      background: rgba(30, 41, 59, 0.6);
      border: 1px solid var(--border);
      padding: 30px;
      border-radius: 16px;
      margin-bottom: 50px;
      text-align: center;
      backdrop-filter: blur(10px);
    }

    /* Services Grid */
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 25px;
      margin-bottom: 60px;
    }

    .card {
      background: var(--card-bg);
      padding: 30px;
      border-radius: 16px;
      border: 1px solid var(--border);
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
      display: flex;
      flex-direction: column;
      justify-content: space-between; /* Mantiene el botón abajo */
      position: relative;
      overflow: hidden;
    }

    .card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 4px;
      background: var(--accent);
      opacity: 0;
      transition: opacity 0.3s ease;
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 20px 40px -10px rgba(0, 0, 0, 0.5);
      border-color: var(--accent);
    }

    .card:hover::before {
      opacity: 1;
    }

    .card-icon {
      font-size: 2rem;
      color: var(--accent);
      margin-bottom: 20px;
    }

    h2 {
      font-size: 1.5rem;
      margin-bottom: 15px;
      color: var(--text-primary);
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .card p {
      color: var(--text-secondary);
      margin-bottom: 20px;
      font-size: 0.95rem;
    }

    .features {
      list-style: none;
      margin: 20px 0;
      padding-top: 20px;
      border-top: 1px solid var(--border);
    }

    .features li {
      margin-bottom: 10px;
      color: #cbd5e1;
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 0.9rem;
    }

    .features li i {
      color: var(--whatsapp);
      font-size: 0.8rem;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      padding: 14px 20px;
      background: var(--whatsapp);
      color: white;
      text-decoration: none;
      border-radius: 10px;
      font-weight: 600;
      transition: all 0.3s ease;
      gap: 10px;
      margin-top: auto; /* Empuja el botón al fondo si hay espacio */
    }

    .btn:hover {
      background: var(--whatsapp-hover);
      transform: scale(1.02);
    }

    /* Info Section */
    .info-section {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
      margin-bottom: 60px;
    }

    @media (max-width: 768px) {
      h1 { font-size: 2.2rem; }
      .info-section { grid-template-columns: 1fr; }
      .container { width: 95%; }
    }

    footer {
      text-align: center;
      padding: 40px 0;
      border-top: 1px solid var(--border);
      color: var(--text-secondary);
      font-size: 0.9rem;
    }
  </style>
</head>

<body>

  <header>
    <div class="container">
      <h1>Sebastián Araya</h1>
      <p class="subtitle">Automatización Digital para negocios que quieren crecer.</p>
      <div class="intro-card">
        <h2><i class="fa-solid fa-magnifying-glass-chart"></i> ¿En qué te puedo ayudar hoy?</h2>
        <p style="margin-bottom: 0;">
          Si pierdes tiempo respondiendo mensajes, organizando pedidos o agendando clientes manualmente,
          tengo la solución para recuperar tus horas.
        </p>
      </div>
    </div>
  </header>
  
  <main class="container">
    <!-- Grid de Servicios -->
    <div class="services-grid">
      <!-- Servicio 1 -->
      <div class="card">
        <div>
          <div class="card-icon"><i class="fa-brands fa-whatsapp"></i></div>
          <h2>Automatización WhatsApp</h2>
          <p>Responde mensajes 24/7 y muestra tu catálogo de productos o servicios sin tocar el celular.</p>
          <ul class="features">
            <li><i class="fa-solid fa-check"></i> Respuestas automáticas</li>
            <li><i class="fa-solid fa-check"></i> Catálogo integrado</li>
            <li><i class="fa-solid fa-check"></i> Atención inmediata</li>
          </ul>
        </div>
        <div>
          <!-- Eliminado el precio -->
          <a class="btn" href="https://wa.me/56954330427?text=Hola,%20quiero%20cotizar%20automatización%20de%20WhatsApp">
            <i class="fa-brands fa-whatsapp"></i> Cotizar ahora
          </a>
        </div>
      </div>
      <!-- Servicio 2 -->
      <div class="card">
        <div>
          <div class="card-icon"><i class="fa-regular fa-calendar-check"></i></div>
          <h2>Agenda Automática</h2>
          <p>Deja que tus clientes agenden sus citas y tú solo recibe las notificaciones.</p>
          <ul class="features">
            <li><i class="fa-solid fa-check"></i> Agenda 24/7</li>
            <li><i class="fa-solid fa-check"></i> Recordatorios automáticos</li>
            <li><i class="fa-solid fa-check"></i> Sincronización</li>
          </ul>
        </div>
        <div>
          <!-- Eliminado el precio -->
          <a class="btn" href="https://wa.me/56954330427?text=Hola,%20quiero%20cotizar%20una%20agenda%20automática">
            <i class="fa-brands fa-whatsapp"></i> Consultar Agenda
          </a>
        </div>
      </div>
      <!-- Servicio 3 -->
      <div class="card">
        <div>
          <div class="card-icon"><i class="fa-solid fa-cart-shopping"></i></div>
          <h2>Pedidos Automatizados</h2>
          <p>Recibe pedidos organizados en una hoja de cálculo o correo automáticamente.</p>
          <ul class="features">
            <li><i class="fa-solid fa-check"></i> Formularios web</li>
            <li><i class="fa-solid fa-check"></i> Confirmación al cliente</li>
            <li><i class="fa-solid fa-check"></i> Control de stock</li>
          </ul>
        </div>
        <div>
          <!-- Eliminado el precio -->
          <a class="btn" href="https://wa.me/56954330427?text=Hola,%20quiero%20cotizar%20sistema%20de%20pedidos">
            <i class="fa-brands fa-whatsapp"></i> Ver soluciones
          </a>
        </div>
      </div>
      <!-- Servicio 4 -->
      <div class="card">
        <div>
          <div class="card-icon"><i class="fa-solid fa-robot"></i></div>
          <h2>Chatbots Inteligentes</h2>
          <p>Agentes virtuales que contestan preguntas frecuentes y derivan ventas complejas.</p>
          <ul class="features">
            <li><i class="fa-solid fa-check"></i> IA Conversacional</li>
            <li><i class="fa-solid fa-check"></i> Derivación a humanos</li>
          </ul>
        </div>
        <div>
          <!-- Eliminado el precio -->
          <a class="btn" href="https://wa.me/56954330427?text=Hola,%20quiero%20información%20sobre%20chatbots">
            <i class="fa-brands fa-whatsapp"></i> Cotizar Chatbot
          </a>
        </div>
      </div>
    </div>
    <!-- Sección de Información Adicional -->
    <div class="info-section">
      <div class="card">
        <h2><i class="fa-solid fa-credit-card"></i> Medios de Pago</h2>
        <p style="margin-top:15px;">Facilidades para empezar tu proyecto:</p>
        <ul class="features">
          <li><i class="fa-solid fa-money-bill"></i> Pago completo</li>
          <li><i class="fa-solid fa-hand-holding-dollar"></i> Pago en 2 cuotas</li>
          <li><i class="fa-solid fa-file-invoice"></i> Factura si corresponde</li>
        </ul>
      </div>
      <div class="card">
        <h2><i class="fa-solid fa-user-astronaut"></i> Sobre Mí</h2>
        <p style="margin-top:15px;">
          Hola, soy Sebastián. Me dedico a desarrollar soluciones simples y efectivas utilizando herramientas de automatización digital.
        </p>
        <p style="margin-top:10px;">
          Cada negocio es único, por eso realizo <strong>cotizaciones personalizadas</strong> para ajustarme a tu realidad.
        </p>
      </div>
    </div>
  </main>
  <footer>
    <div class="container">
      <p>&copy; 2023 Sebastián Araya. Todos los derechos reservados.</p>
      <p style="font-size: 0.8rem; margin-top: 10px; opacity: 0.6;">
        Diseñado para automatizar el éxito.
      </p>
    </div>
  </footer>

</body>
</html>
