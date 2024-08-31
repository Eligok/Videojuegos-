<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Página de Videojuegos</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
            color: #333;
        }
        header {
            background-color: #6a0dad;
            color: white;
            padding: 20px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #4b0082;
            padding: 10px;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
        }
        nav a:hover {
            color: #ffccff;
        }
        section {
            padding: 20px;
            margin-top: 20px;
        }
        .section-content {
            background-color: white;
            margin: 20px auto;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 800px;
        }
        .section-content h2 {
            color: #4b0082;
        }
        .juegos-recomendados {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin-top: 20px;
        }
        .juego {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin: 10px;
            width: 200px;
            text-align: center;
            padding: 15px;
        }
        .juego img {
            width: 100%;
            border-radius: 8px;
        }
        .juego p {
            color: #4b0082;
            font-weight: bold;
        }
        footer {
            background-color: #4b0082;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        .button {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 20px;
            color: white;
            background-color: #6a0dad;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        .button:hover {
            background-color: #4b0082;
        }
    </style>
</head>
<body> 

<header>
    <h1>Bienvenidos a la Página de Videojuegos</h1>
    <p>Noticias, curiosidades y más del mundo de los videojuegos</p>
</header> 

<nav>
    <a href="#noticias">Noticias</a>
    <a href="#curiosidades">Curiosidades</a>
    <a href="#juegos-recomendados">Juegos Recomendados</a>
</nav> 

<section id="noticias" class="section-content">
    <h2>Noticias</h2>
    <div id="noticia-del-dia">
        <!-- Noticia del día se generará aquí mediante JavaScript -->
    </div>
    <a href="#" class="button">Ver más noticias</a>
</section> 

<section id="curiosidades" class="section-content">
    <h2>Curiosidades</h2>
    <div id="curiosidad-del-dia">
        <!-- Curiosidad del día se generará aquí mediante JavaScript -->
    </div>
    <a href="#" class="button">Ver más curiosidades</a>
</section> 

<section id="juegos-recomendados" class="section-content">
    <h2>Juegos Recomendados</h2>
    <div class="juegos-recomendados" id="lista-juegos">
        <!-- Los juegos recomendados serán generados aquí por JavaScript -->
    </div>
</section> 

<footer>
    <p>&copy; 2024 Página de Videojuegos. Todos los derechos reservados.</p>
</footer> 

<script>
// Lista de noticias y curiosidades para cada día
const noticiasPorDia = [
    "Lanzamiento del nuevo juego RPG que está arrasando en el mercado.",
    "La actualización de verano trae nuevas características a los juegos de mundo abierto.",
    "Anunciada la remasterización de un clásico de la década de 2000.",
    "El torneo de eSports más grande del año ha comenzado hoy.",
    "Nuevo estudio muestra cómo los videojuegos ayudan a mejorar la memoria.",
    "Se confirma la secuela de uno de los juegos más esperados del año.",
    "Colaboración sorpresa entre dos grandes franquicias de videojuegos."
]; 

const curiosidadesPorDia = [
    "¿Sabías que el primer videojuego comercial fue lanzado en 1971?",
    "Los videojuegos pueden ayudar a mejorar la toma de decisiones rápidas.",
    "El juego más caro jamás desarrollado costó más de 500 millones de dólares.",
    "Existe un récord mundial Guinness para el videojuego más vendido de la historia.",
    "La industria de los videojuegos es más grande que la del cine y la música combinadas.",
    "Los desarrolladores de juegos a menudo incluyen easter eggs ocultos para los jugadores más curiosos.",
    "Los videojuegos pueden ser una excelente herramienta educativa para aprender historia y ciencias."
]; 

// Lista de juegos recomendados para cada mes
const juegosPorMes = {
    0: [ // Enero
        { titulo: "Juego A", descripcion: "Descripción del Juego A", imagen: "https://via.placeholder.com/150" },
        { titulo: "Juego B", descripcion: "Descripción del Juego B", imagen: "https://via.placeholder.com/150" },
        { titulo: "Juego C", descripcion: "Descripción del Juego C", imagen: "https://via.placeholder.com/150" }
    ],
    1: [ // Febrero
        { titulo: "Juego D", descripcion: "Descripción del Juego D", imagen: "https://via.placeholder.com/150" },
        { titulo: "Juego E", descripcion: "Descripción del Juego E", imagen: "https://via.placeholder.com/150" },
        { titulo: "Juego F", descripcion: "Descripción del Juego F", imagen: "https://via.placeholder.com/150" }
    ],
    // Añade más meses con juegos recomendados
    11: [ // Diciembre
        { titulo: "Juego X", descripcion: "Descripción del Juego X", imagen: "https://via.placeholder.com/150" },
        { titulo: "Juego Y", descripcion: "Descripción del Juego Y", imagen: "https://via.placeholder.com/150" },
        { titulo: "Juego Z", descripcion: "Descripción del Juego Z", imagen: "https://via.placeholder.com/150" }
    ]
}; 

// Obtener el día y mes actuales
const diaActual = new Date().getDay();
const mesActual = new Date().getMonth(); 

// Seleccionar la noticia y curiosidad del día
const noticiaDelDia = noticiasPorDia[diaActual % noticiasPorDia.length];
const curiosidadDelDia = curiosidadesPorDia[diaActual % curiosidadesPorDia.length]; 

// Seleccionar los juegos recomendados para el mes actual
const juegosRecomendados = juegosPorMes[mesActual]; 

// Función para mostrar los juegos recomendados
function mostrarJuegosRecomendados() {
    const contenedor = document.getElementById('lista-juegos');
    contenedor.innerHTML = ''; // Limpiar el contenedor 

    juegosRecomendados.forEach(juego => {
        const juegoDiv = document.createElement('div');
        juegoDiv.classList.add('juego');
        juegoDiv.innerHTML = `
            <img src="${juego.imagen}" alt="${juego.titulo}">
            <p>${juego.titulo}</p>
            <p>${juego.descripcion}</p>
        `;
        contenedor.appendChild(juegoDiv);
    });
} 

// Función para mostrar la noticia del día
function mostrarNoticiaDelDia() {
    const contenedorNoticia = document.getElementById('noticia-del-dia');
    contenedorNoticia.innerHTML = `<p>${noticiaDelDia}</p>`;
} 

// Función para mostrar la curiosidad del día
function mostrarCuriosidadDelDia() {
    const contenedorCuriosidad = document.getElementById('curiosidad-del-dia');
    contenedorCuriosidad.innerHTML = `<p>${curiosidadDelDia}</p>`;
} 

// Llamar a las funciones para mostrar el contenido dinámico al cargar la
