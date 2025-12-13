<!DOCTYPE html>
<html lang="es">
<head>
    <title>Actividad 4</title>
</head>
<style>
    body{
        background-color: beige;
        font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
    }
</style>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Atrapa la Neurona - Divulgacion Cientifica</title>

  <style>
    body {
      background: #eef7ff;
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 20px;
    }

    h1 {
      color: #2c3e50;
    }

    #gameArea {
      width: 90%;
      height: 420px;
      background: #d6eaff;
      border: 3px solid #2c3e50;
      border-radius: 12px;
      margin: 20px auto;
      position: relative;
      overflow: hidden;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    #neuron {
      width: 80px;
      height: 80px;
      position: absolute;
      cursor: pointer;
      transition: 0.1s;
    }

    #score {
      font-size: 24px;
      font-weight: bold;
      color: #34495e;
    }

    button {
      padding: 10px 25px;
      font-size: 16px;
      margin-top: 15px;
      cursor: pointer;
      background: #2c3e50;
      color: #fff;
      border: none;
      border-radius: 6px;
    }

    button:hover {
      background: #3d566e;
    }
  </style>
</head>
<body>

  <h1>🧠 Atrapa la Neurona</h1>
  <p>Haz clic en la neurona para sumar puntos. ¡Activa tus reflejos sinápticos!</p>

  <div id="score">Puntaje: 0</div>

  <div id="gameArea">
    <!-- Neurona en SVG -->
    <img id="neuron" src="https://upload.wikimedia.org/wikipedia/commons/4/4c/Neuron.svg" alt="Neurona">
  </div>

  <button onclick="reiniciar()">Reiniciar Juego</button>

  <script>
    const neuron = document.getElementById("neuron");
    const gameArea = document.getElementById("gameArea");
    const scoreText = document.getElementById("score");

    let score = 0;

    function moverNeurona() {
      const maxX = gameArea.clientWidth - 80;
      const maxY = gameArea.clientHeight - 80;

      const randomX = Math.floor(Math.random() * maxX);
      const randomY = Math.floor(Math.random() * maxY);

      neuron.style.left = randomX + "px";
      neuron.style.top = randomY + "px";
    }

    neuron.addEventListener("click", () => {
      score++;
      scoreText.textContent = "Puntaje: " + score;
      moverNeurona();
    });

    function reiniciar() {
      score = 0;
      scoreText.textContent = "Puntaje: 0";
      moverNeurona();
    }

    moverNeurona(); // inicia el juego
  </script>
<body>
        <header> 
        <h1 id="Titulo"> divulgacioncientifica.com </h1>
    </header>
    <section>
        <article class="post">
            <h2>Inicio </h2> 
            <p>Descripcion</p>
            <img src="paginaweb1.webp"/>
            <p>Este sitio ofrece contenido científico médico actualizado y basado en evidencia, dirigido a profesionales de la salud, estudiantes y público interesado en comprender los avances más relevantes en medicina</p>
         <h3>La revolución de la IA en la Medicina</h3>
         <img src="La revolución de la IA en la Medicina.jpg"/>
         <br>
         <br>
            <a target="_blank" href="https://www.youtube.com/watch?v=6IRgWKbyJ5I/">La revolución de la IA en la Medicina</a>     
        </article>
        <article class="post">
            <h2>Articulos</h2>
            <p>Descripcion</p>
            <p>En esta sección encontrarás artículos seleccionados de PubMed, The Lancet, The New England Journal of Medicine y del blog AIpocrates, para mantenernos al día con la mejor evidencia y los avances en salud digital e IA</p>
            <img src="pubmed.png"/>  <a target="_blank" href="https://pubmed.ncbi.nlm.nih.gov/">PubMed</a>
            <img src="thelancet.png"/> <a target="_blank" href="https://www.thelancet.com/">thelancet</a>
            <img src="Thenewenglandjournalofmedicine.png"/> <a target="_blank" href="https://www.nejm.org/">Thenewenglandjournalofmedicine</a>
            <img src="AIpocrates.png"/> <a target="_blank" href="https://aipocrates.blog/">AIpocrates</a>
                    </article>
        <article class="post">
            <h2>Sobre Nosotros</h2>
            <p>Descripcion</p>
            <img src="SobreNosotros.jpg"/>
                        <p>Somos una plataforma dedicada a acercar el conocimiento científico médico a profesionales de la salud, estudiantes y a todas las personas interesadas en comprender los avances más importantes en la medicina moderna. Nuestro propósito es transformar información compleja en contenido claro, confiable y accesible, permitiendo que el conocimiento científico llegue a más personas de manera responsable y basada en evidencia.</p>
                        <p>Trabajamos con un enfoque en la evidencia científica, la ética y la claridad comunicativa. Seleccionamos artículos, análisis y recursos actualizados para promover la educación en salud y mejorar la comprensión de los avances médicos</p>
        </article>
            </section>
<body>

<h2>Cargar un PDF </h2>
    <p>Contribuye con la comunidad colaborativa y compate tu estudio o articulo cientifico para que nuestra linea de editores lo valide para publicarlo en la pagina</p>
<input type="file" id="pdfFile" accept="application/pdf">
<br><br>

<iframe id="viewer" width="100%" height="600px" style="border:1px solid #333"></iframe>

<script>
  document.getElementById("pdfFile").addEventListener("change", function(e) {
    const archivo = e.target.files[0];
    const url = URL.createObjectURL(archivo);
    document.getElementById("viewer").src = url;
  });
</script>

</body>
<body>
  <form action="/Formulario" method="post">
      <label form="Nombre">Nombre</label>
        <input type="text" id="Nombre" name="Nombre" placeholder="Nombre" />
              <label form="Apellido">Apellido</label>
        <input type="text" id="Apellido" name="Apellido" placeholder="Apellido" />          
      <label form="Email">Email</label>
        <input type="text" id="Email" name="Email" placeholder="Email" />  
        <br>
        <br>
        <label for="Comentario">Comentario</label>
        <textarea cols="40" id="Comentario" placeholder="Ingresar Comentario" name="Comentario"></textarea>
        <br>
        <br>
        ><input type="submit">
        <button type="button">Enviar</button>
        <button type="reset">Borrar</button>
        <button type="submit">Submit</button>
            </form>
</body>

</body>
    <footer> 
        <a href="#Titulo">Ir Al Inicio</a>
        <a href="mailto:rafael52987@hotmail.com">Contacto</a>
                <p>📍 Ubicación: Medellín, Colombia</p>
        <p>💡 Horario: L–V 8:00 am – 5:00 pm</p>
        <p>Derechos Reservados 2025</p>
    </footer>
</body>
</html>
