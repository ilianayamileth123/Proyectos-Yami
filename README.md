<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Menú Yami con Íconos y Hamburguesa</title>

  <!-- Font Awesome CDN para íconos -->
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    integrity="sha512-pV4JbSsVgcQ8H40+UE3NjIrMxykGkCjIN+bKqjzNN8F3a89wzwVL/f4kaC1KwqJRe61/1xkOiPjkI3CwCFl1Hg=="
    crossorigin="anonymous"
    referrerpolicy="no-referrer"
  />

  <style>
    :root {
      --color-primario: #f8b500;
      --color-fondo: #fceabb;
      --color-texto: #333;
      --color-blanco: #fff;
      --transicion: 0.3s ease;
      --radio-bordes: 20px;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, var(--color-fondo), var(--color-primario));
      color: var(--color-texto);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: flex-start;
      padding: 20px;
    }

    nav[aria-label="Menú principal"] {
      background-color: var(--color-blanco);
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      border-radius: 0 0 var(--radio-bordes) var(--radio-bordes);
      overflow: hidden;
      width: 100%;
      max-width: 900px;
      position: relative;
    }

    /* Botón hamburguesa */
    .menu-toggle {
      display: none;
      position: absolute;
      top: 15px;
      right: 20px;
      background: none;
      border: none;
      font-size: 1.8rem;
      cursor: pointer;
      color: var(--color-texto);
      transition: color var(--transicion);
      z-index: 10;
    }

    .menu-toggle:focus {
      outline: 3px solid var(--color-primario);
      outline-offset: 2px;
    }

    .menu-toggle:hover {
      color: var(--color-primario);
    }

    ul.menu {
      display: flex;
      justify-content: center;
      list-style: none;
      margin: 0;
      padding: 0;
      transition: max-height 0.3s ease;
    }

    ul.menu li {
      margin: 0;
    }

    ul.menu li a {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 15px 30px;
      text-decoration: none;
      color: var(--color-texto);
      font-weight: 700;
      position: relative;
      transition: color var(--transicion);
      outline-offset: 4px;
    }

    ul.menu li a::after {
      content: "";
      position: absolute;
      bottom: 4px;
      left: 50%;
      width: 0;
      height: 3px;
      background-color: var(--color-primario);
      transition: width var(--transicion), left var(--transicion);
      transform: translateX(-50%);
      border-radius: 2px;
    }

    ul.menu li a:hover,
    ul.menu li a:focus-visible {
      color: var(--color-primario);
    }

    ul.menu li a:hover::after,
    ul.menu li a:focus-visible::after {
      width: 80%;
      left: 50%;
    }

    /* Íconos color */
    ul.menu li a i {
      color: var(--color-primario);
      transition: color var(--transicion);
    }

    ul.menu li a:hover i,
    ul.menu li a:focus-visible i {
      color: #c69000;
    }

    /* Responsive */
    @media (max-width: 600px) {
      .menu-toggle {
        display: block;
      }

      ul.menu {
        flex-direction: column;
        max-height: 0;
        overflow: hidden;
        width: 100%;
      }

      ul.menu.active {
        max-height: 500px; /* suficiente para mostrar todos */
      }

      ul.menu li a {
        padding: 12px 20px;
        border-bottom: 1px solid #eee;
        text-align: left;
      }

      ul.menu li:last-child a {
        border-bottom: none;
      }
    }
  </style>
</head>
<body>
  <nav aria-label="Menú principal">
    <button class="menu-toggle" aria-expanded="false" aria-controls="menu">
      <span class="sr-only">Abrir menú</span>
      <i class="fas fa-bars" aria-hidden="true"></i>
    </button>
    <ul id="menu" class="menu">
      <li><a href="estructurabctexto22.html"><i class="fas fa-layer-group"></i> Estructura Básica</a></li>
      <li><a href="listas_y_lineas.html"><i class="fas fa-list"></i> Líneas y Listas</a></li>
      <li><a href="imagenes.html"><i class="fas fa-image"></i> Imágenes y Multimedia</a></li>
      <li><a href="hipervinculos.html"><i class="fas fa-link"></i> Hipervínculos</a></li>
      <li><a href="tablas.html"><i class="fas fa-table"></i> Tablas</a></li>
      <li><a href="continentes.html"><i class="fas fa-globe-americas"></i> Continentes</a></li>
    </ul>
  </nav>

  <script>
    const toggleButton = document.querySelector('.menu-toggle');
    const menu = document.getElementById('menu');

    toggleButton.addEventListener('click', () => {
      const expanded = toggleButton.getAttribute('aria-expanded') === 'true' || false;
      toggleButton.setAttribute('aria-expanded', !expanded);
      menu.classList.toggle('active');
    });
  </script>
</body>
</html>
