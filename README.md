<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Dilo con amor</title>
  <link rel="icon" href="favicon-16x16.jpeg" type="image/jpeg">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
    :root {
      --menta-clara:#A8DADC;
      --blanco-nieve:#F1FAEE;
      --azul-petroleo:#457B9D;
      --azul-oscuro:#1D3557;
    }

    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #FADADD; /* Rosa limonada */
      color: #000;
    }

    header {
      background: #bb79e6;
      color: var(--blanco-nieve);
      padding: 1rem;
      text-align: center;
      position: relative;
      animation: fadeDown 1s ease;
    }

    header h1 {
      display: inline-block;
      margin: 0;
      vertical-align: middle;
      font-size: 2rem;
    }

    .foto-personal {
      width: 100px;
      border-radius: 50%;
      margin-left: 1rem;
      vertical-align: middle;
    }

    nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 2rem;
      background: #5687b5;
      padding: 1rem;
    }

    nav a {
      color: var(--azul-oscuro);
      text-decoration: none;
      font-weight: bold;
      transition: color .3s;
      font-size: 1.3rem;
      cursor: pointer;
    }

    nav a:hover {
      color: var(--azul-petroleo);
    }

    section {
      display: none;
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.8s, transform 0.8s;
    }

    section.active {
      display: block;
      animation: entradaSuave 0.8s ease forwards;
    }

    @keyframes entradaSuave {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeDown {
      from {
        opacity: 0;
        transform: translateY(-20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .catalogo-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
    }

    .catalogo-item {
      flex: 1 1 300px;
    }

    .catalogo-item h3 {
      margin-top: 0;
      font-size: 1.5rem;
    }

    .catalogo-item ul {
      padding-left: 1.5rem;
      font-size: 1.1rem;
    }

    .galeria {
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      margin-top: 0;
    }

    .galeria img {
      width: 100%;
      max-width: 320px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,.5);
      transition: opacity .6s;
    }

    .social-icons {
      display: flex;
      justify-content: center;
      gap: 3rem;
      margin-top: 2rem;
      flex-wrap: wrap;
    }

    .social-icons a {
      color: var(--menta-clara);
      font-size: 48px;
      transition: color .3s;
    }

    .social-icons a:hover {
      color: var(--azul-petroleo);
    }

    .social-icons div {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .social-icons span {
      margin-top: .5rem;
      font-size: 22px;
      font-weight: bold;
      color: var(--azul-oscuro);
    }

    iframe {
      border: 0;
      width: 100%;
      height: 450px;
      margin-top: 1rem;
    }

    .center-text {
      text-align: center;
      margin-top: 1rem;
      font-style: italic;
      font-size: 1.1rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>Dilo con amor</h1>
    <img src="dana.jpeg" alt="Logo" class="foto-personal">
  </header>

  <nav>
    <a onclick="mostrarSeccion('quienes')">Inicio</a>
    <a onclick="mostrarSeccion('catalogo')">Catálogo</a>
    <a onclick="mostrarSeccion('comunicate')">Comunícate</a>
    <a onclick="mostrarSeccion('ubicacion')">Ubicación</a>
  </nav>

  <section id="quienes" class="active">
    <h2>¿Quiénes somos?</h2>
    <p>Somos una empresa que desea brindar experiencias que se recuerdan por siempre y qué mejor que un regalo eterno como flores, arreglos que se pueden conservar. Nacimos con la idea de que cada regalo debe contar una historia y por eso cuidamos cada detalle con dedicación y creatividad.</p>
    <h2>Visión</h2>
    <p>Ser reconocida como una empresa eficiente con los trabajos realizados, destacando el compromiso y dedicación que se tiene con el cliente, buscando el mejor resultado y satisfacción.</p>
    <h3>Objetivos</h3>
    <ul>
      <li>Crear arreglos personalizados que reflejen emociones.</li>
      <li>Ampliar nuestra presencia en redes.</li>
      <li>Fomentar el uso de flores preservadas.</li>
      <li>Ofrecer productos únicos para eventos.</li>
    </ul>
  </section>

  <section id="catalogo">
    <h2>Catálogo de Productos y Servicios</h2>
    <div class="catalogo-grid">
      <div class="catalogo-item">
        <h3>💐 Arreglos Florales</h3>
        <ul>
          <li>Flores eternas individuales</li>
          <li>Arreglos en cajas decorativas</li>
          <li>Jarrones con luz LED</li>
          <li>Arreglos florales personalizados</li>
          <li>Letras decorativas con flores</li>
        </ul>
        <h3>🍼 Baby Shower</h3>
        <ul>
          <li>Cintó para la mami</li>
          <li>Corsage para el papá</li>
          <li>Distintivos para los invitados</li>
          <li>Canastas decoradas</li>
        </ul>
        <h3>📦 Otros</h3>
        <ul>
          <li>Pulseras</li>
          <li>Plumas decoradas</li>
          <li>Portarretratos</li>
          <li>Ramos con dulces</li>
          <li>Frascos con flores y bombones, galletas, dulces, chocolates, etc.</li>
        </ul>
      </div>

      <div class="catalogo-item">
        <h3>💍 Bodas</h3>
        <ul>
          <li>Ramos de novia personalizados</li>
          <li>Mini ramos para lanzar</li>
          <li>Mini ramos para damas de honor</li>
          <li>Cojines para anillos</li>
          <li>Lazo matrimonial decorado</li>
          <li>Arras con estuche decorado</li>
          <li>Copas de brindis personalizadas</li>
          <li>Caja de pacto con diseño especial</li>
        </ul>
        <h3>👑 XV Años</h3>
        <ul>
          <li>Ramos de quinceañera</li>
          <li>Cojines decorativos</li>
          <li>Caja para pacto simbólico</li>
          <li>Copas de brindis</li>
        </ul>
      </div>

      <div class="catalogo-item" style="display:flex;align-items:flex-start;justify-content:center;">
        <div class="galeria">
          <img id="slideshow" src="1.jfif" alt="Galería">
        </div>
      </div>
    </div>
  </section>

  <section id="comunicate">
    <h2 style="text-align:center;">Comunícate</h2>
    <p style="text-align:center;">Síguenos o contáctanos por redes sociales:</p>
    <div class="social-icons">
      <div><a href="https://www.facebook.com/profile.php?id=61568670475896" target="_blank"><i class="fab fa-facebook"></i></a><span>Facebook</span></div>
      <div><a href="https://www.instagram.com/diloconamooor" target="_blank"><i class="fab fa-instagram"></i></a><span>Instagram</span></div>
      <div><a href="https://wa.me/5212291593502" target="_blank"><i class="fab fa-whatsapp"></i></a><span>WhatsApp</span></div>
    </div>
    <p class="center-text">Horario: lunes a domingo de 10:00 am a 17:00 pm.</p>
    <p class="center-text">¿Tienes alguna duda? Escríbenos y te responderemos cuanto antes.</p>
  </section>

  <section id="ubicacion">
    <h2>Ubicación</h2>
    <p>Para poder verlos y atenderlos en físico en esta dirección solo será con cita agendada</p>
    <p>Estamos localizados en:</p>
    <iframe src="https://www.google.com/maps/embed?pb=!1m18..." allowfullscreen="" loading="lazy"></iframe>
    <p class="center-text">¿Qué esperas para venir y obsequiar el mejor detalle?</p>
  </section>

  <script>
    function mostrarSeccion(id) {
      document.querySelectorAll('section').forEach(s => s.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }

    const imagenes = [
      '1.jfif','2.jfif','3.jfif','4.jfif','5.jfif','6.jfif','7.jfif','8.jfif','9.jfif','10.jfif',
      '11.jfif','12.jfif','13.jfif','14.jfif','15.jfif','16.jfif','17.jfif','18.jfif','19.jfif','20.jfif',
      '21.jfif','22.jfif','23.jfif','24.jfif','25.jfif','26.jfif','27.jfif','28.jfif','29.jfif','30.jfif'
    ];
    let indice = 0;
    const slide = document.getElementById('slideshow');

    function cambiarImagen() {
      slide.style.opacity = 0;
      setTimeout(() => {
        indice = (indice + 1) % imagenes.length;
        slide.src = imagenes[indice];
        slide.style.opacity = 1;
      }, 600);
    }

    setInterval(cambiarImagen, 5000);
  </script>
</body>
</html>
