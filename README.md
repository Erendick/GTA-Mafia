# GTA-Mafia
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>La Mafia</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #0e0e0e;
      color: white;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #1a1a1a;
      padding: 20px;
      text-align: center;
    }
    h1 {
      color: crimson;
    }
    section {
      padding: 20px;
    }
    textarea {
      width: 100%;
      height: 100px;
      background-color: #222;
      color: white;
      border: none;
      padding: 10px;
    }
    .submit-btn {
      background-color: crimson;
      color: white;
      border: none;
      padding: 10px 20px;
      margin-top: 10px;
      cursor: pointer;
    }
    .report, .suggestion {
      background-color: #1a1a1a;
      padding: 10px;
      margin-top: 10px;
      border-left: 4px solid crimson;
    }
    .link-box {
      background-color: #222;
      padding: 20px;
      margin: 20px;
      border-left: 5px solid crimson;
    }
    .link-box a {
      color: cyan;
      font-weight: bold;
    }
  </style>
</head>
<body>

<header>
  <h1>La Mafia</h1>
  <p>Reporta jugadores tóxicos, deja sugerencias y descarga GTA V versión Mafia</p>
</header>

<section>
  <h2>Publicar Jugadores Tóxicos</h2>
  <textarea id="toxicInput" placeholder="Nombre del jugador, comportamiento, pruebas..."></textarea>
  <button class="submit-btn" onclick="addReport()">Publicar</button>
  <div id="toxicList"></div>
</section>

<section>
  <h2>Sugerencias</h2>
  <textarea id="suggestionInput" placeholder="¿Tienes una idea? Escríbela aquí..."></textarea>
  <button class="submit-btn" onclick="addSuggestion()">Enviar Sugerencia</button>
  <div id="suggestionList"></div>
</section>

<section class="link-box">
  <h2>Descargar GTA V Mafia</h2>
  <p>Haz clic en el siguiente enlace para descargar GTA V versión Mafia:</p>
  <a href="https://example.com/descargar-gta-mafia" target="_blank">Descargar GTA V Mafia</a>
</section>

<script>
  function addReport() {
    const input = document.getElementById("toxicInput");
    const list = document.getElementById("toxicList");
    if (input.value.trim() !== "") {
      const div = document.createElement("div");
      div.className = "report";
      div.textContent = input.value;
      list.prepend(div);
      input.value = "";
    }
  }

  function addSuggestion() {
    const input = document.getElementById("suggestionInput");
    const list = document.getElementById("suggestionList");
    if (input.value.trim() !== "") {
      const div = document.createElement("div");
      div.className = "suggestion";
      div.textContent = input.value;
      list.prepend(div);
      input.value = "";
    }
  }
</script>

</body>
</html>
