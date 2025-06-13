# Proyectos-Yami

<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Menú Yami</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #fceabb, #f8b500);
    }

    nav {
      background: #fff;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      border-radius: 0 0 20px 20px;
      overflow: hidden;
    }

    ul.menu {
      display: flex;
      justify-content: center;
      padding: 0;
      margin: 0;
      list-style: none;
    }

    ul.menu li {
      margin: 0;
    }

    ul.menu li a {
      display: block;
      padding: 15px 25px;
      text-decoration: none;
      color: #333;
      font-weight: bold;
      transition: all 0.3s ease;
      position: relative;
    }

    ul.menu li a::after {
      content: "";
      position: absolute;
      width: 0%;
      height: 3px;
      background: #f8b500;
      bottom: 0;
      left: 50%;
      transition: all 0.3s ease;
      transform: translateX(-50%);
    }

    ul.menu li a:hover::after {
      width: 80%;
    }

    ul.menu li a:hover {
      color: #f8b500;
    }

    @media screen and (max-width: 600px) {
      ul.menu {
        flex-direction: column;
      }

      ul.menu li a {
        text-align: center;
        border-bottom: 1px solid #eee;
      }
    }
  </style>
</head>
<body>

  <nav>
    <ul class="menu">
      <li><a href="https://github.com/ilianayamileth123/Proyectos-Yami/blob/main/estructurabctexto22.html">Estructura Basica</a></li>
      <li><a href="https://github.com/ilianayamileth123/Proyectos-Yami/blob/main/listas_y_lineas.html">Lineas y Listas</a></li>
      <li><a href="https://github.com/ilianayamileth123/Proyectos-Yami/blob/main/imagenes.html">Imagenes y Multimedia</a></li>
      <li><a href="">Hipervinculos</a></li>
      <li><a href="https://github.com/ilianayamileth123/Proyectos-Yami/blob/main/tablas.html">Tablas</a></li>
      <li><a href="https://github.com/ilianayamileth123/Proyectos-Yami/blob/main/continentes.html">Continentes</a></li>
    </ul>
  </nav>

  <!-- Aquí podrías añadir el resto de tu página -->

</body>
</html>
