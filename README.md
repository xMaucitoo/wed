<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página interactiva con pregunta y respuesta, que muestra texto e imágenes según la opción seleccionada.">
    <meta name="keywords" content="interactivo, pregunta, respuesta, programación, HTML, CSS, JavaScript">
    <title>Pregunta con Respuestas</title>
    <style>
        body {
            background-image: url('Mi proyecto/2daf60e8-3015-4030-b6f5-ca04c784be2a.webp');
            background-size: contain;
            background-position: center top;
            color: white;
            font-family: 'Arial', sans-serif;
            text-align: center;
            padding-top: 90px;
            margin: 0;
        }
        .container {
            background-color: rgba(0, 0, 0, 0.6);
            padding: 20px;
            border-radius: 10px;
            display: inline-block;
            max-width: 50%;
            margin: auto;
            animation: fadeIn 1s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .respuesta {
            margin-top: 20px;
            display: none;
            animation: fadeIn 0.5s ease-in-out;
        }
        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
            border: none;
            color: white;
            background-color: #0066cc;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #004c99;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            display: block;
            margin: 10px auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¿Te casarias conmigo, mi bieja miada hedionda 😾?</h1>
        <button id="btnSi">Sí</button>
        <button id="btnNo">No</button>

        <div id="respuestaSi" class="respuesta">
            <h2>¡Waosss, dijiste que si! Te amo mi mujer hermosa. Bueno, desnudese que yo le hare 3 hijos si es posible!</h2>
            <img src="Mi proyecto/0bdb1489-87cd-4487-bc3c-cc11dedacb7d.webp" alt="Imagen de una persona programando">
        </div>

        <div id="respuestaNo" class="respuesta">
            <h2>¡No te preocupes! no me duele, me lastima. Pero que tanto, de todas forma usted es mia y me pertenece. No se librara de mi facilmente.....</h2>
            <img src="Mi proyecto/ea43d3f1-c2ee-4c4d-ac18-b600e0326b7f.webp" alt="Imagen de una persona relajándose">
        </div>

        <!-- Botón para reproducir música -->
        <button id="playMusic">Reproducir Música</button>
        <audio id="bgMusic" loop>
            <source src="Musica/Maucito.mp3" type="audio/mpeg">
            Tu navegador no soporta el elemento de audio.
        </audio>
    </div>

    <script>
        document.getElementById('btnSi').addEventListener('click', function() {
            mostrarRespuesta('si');
        });
        document.getElementById('btnNo').addEventListener('click', function() {
            mostrarRespuesta('no');
        });

        document.getElementById('playMusic').addEventListener('click', function() {
            document.getElementById('bgMusic').play();
        });

        function mostrarRespuesta(respuesta) {
            document.getElementById('respuestaSi').style.display = 'none';
            document.getElementById('respuestaNo').style.display = 'none';

            if (respuesta === 'si') {
                document.getElementById('respuestaSi').style.display = 'block';
            } else if (respuesta === 'no') {
                document.getElementById('respuestaNo').style.display = 'block';
            }
        }
    </script>
</body>
</html>
