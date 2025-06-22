<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elo329</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #74b9ff 0%, #0984e3 100%);
            min-height: 100vh;
            color: #333;
        }

        /* Estilos del menú */
        .navbar {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 2px solid rgba(255, 255, 255, 0.3);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 0 2rem;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 1rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .nav-item {
            cursor: pointer;
            padding: 0.7rem 1.2rem;
            color: #333;
            font-weight: 500;
            border-radius: 20px;
            transition: all 0.3s ease;
            background: rgba(116, 185, 255, 0.1);
            border: 2px solid transparent;
            font-size: 0.9rem;
        }

        .nav-item:hover {
            background: rgba(116, 185, 255, 0.2);
            transform: translateY(-2px);
            border-color: rgba(116, 185, 255, 0.3);
        }

        .nav-item.active {
            background: #74b9ff;
            color: white;
            box-shadow: 0 4px 15px rgba(116, 185, 255, 0.4);
        }

        /* Estilos del contenido */
        .content-container {
            max-width: 900px;
            margin: 2rem auto;
            padding: 0 2rem;
        }

        .section {
            display: none;
            background: white;
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
            animation: fadeIn 0.4s ease-in-out;
            margin-bottom: 2rem;
        }

        .section.active {
            display: block;
        }

        .section h1 {
            color: #2d3436;
            margin-bottom: 1.5rem;
            font-size: 2.2rem;
            border-bottom: 3px solid #74b9ff;
            padding-bottom: 0.5rem;
        }

        .section h2 {
            color: #636e72;
            margin: 1.5rem 0 1rem 0;
            font-size: 1.4rem;
        }

        .section h3 {
            color: #74b9ff;
            margin: 1rem 0 0.5rem 0;
            font-size: 1.2rem;
        }

        .section p {
            color: #636e72;
            line-height: 1.7;
            margin-bottom: 1rem;
            font-size: 1rem;
            text-align: justify;
        }

        .section ul {
            margin: 1rem 0;
            padding-left: 2rem;
        }

        .section li {
            color: #636e72;
            line-height: 1.6;
            margin-bottom: 0.5rem;
        }

        .info-box {
            background: linear-gradient(135deg, #fd79a8 0%, #fdcb6e 100%);
            padding: 1.5rem;
            border-radius: 10px;
            margin: 1.5rem 0;
            color: white;
            border-left: 4px solid #e84393;
        }

        .info-box h3 {
            color: white;
            margin-bottom: 0.5rem;
        }

        .info-box p {
            color: white;
            margin: 0;
        }

        .code-box {
            background: #2d3436;
            color: #ddd;
            padding: 1.5rem;
            border-radius: 10px;
            margin: 1.5rem 0;
            font-family: 'Courier New', monospace;
            overflow-x: auto;
        }

        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }

        .feature-card {
            background: linear-gradient(135deg, #a29bfe 0%, #6c5ce7 100%);
            padding: 1.5rem;
            border-radius: 10px;
            color: white;
            text-align: center;
        }

        .feature-card h3 {
            color: white;
            margin-bottom: 1rem;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(15px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                gap: 0.5rem;
            }

            .nav-item {
                font-size: 0.8rem;
                padding: 0.5rem 0.8rem;
            }

            .section {
                padding: 2rem 1.5rem;
            }

            .section h1 {
                font-size: 1.8rem;
            }

            .feature-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Menú de navegación -->
    <nav class="navbar">
        <div class="nav-container">
            <ul class="nav-menu">
                <li class="nav-item active" onclick="showSection('introduccion')">Inicio</li>
                <li class="nav-item" onclick="showSection('contenido')">Problema</li>
                <li class="nav-item" onclick="showSection('detalles')">Requerimientos</li>
                <li class="nav-item" onclick="showSection('informacion')">Diseño</li>
                <li class="nav-item" onclick="showSection('arquitectura')">Pruebas</li>
                <li class="nav-item" onclick="showSection('tecnologias')">Codigo</li>
            </ul>
        </div>
    </nav>

    <!-- Contenido de las secciones -->
    <div class="content-container">
        <!-- Sección Introducción -->
        <div id="introduccion" class="section active">
            <h1>TelJack</h1>            
            <h2>Nombres</h2>
            <p>Enrique Manzano</p>
            <p>Yair Flores</p>
            <p>Nicolas Sepulveda</p>
            <p>Tomás Salinas</p>   
        </div>

        <!-- Sección Contenido Principal -->
        <div id="contenido" class="section">
            <h1>Descripción del problema</h1>
            <p>En un mundo cada vez más digitalizado, los juegos clásicos también deben adaptarse a los nuevos tiempos. TelJack es una versión digital del popular juego Blackjack, que permite a los usuarios disfrutarlo desde cualquier lugar con solo contar con un dispositivo tecnológico. Este proyecto busca ofrecer una experiencia accesible y entretenida para los fanáticos del juego, combinando diversión con los principios de la programación orientada a objetos.</p>
            
            <h2>Análisis del Problema</h2>
            <p>El problema gira en torno a la digitalización del juego de carta blackjack, en el cual los que participan en el sistema es el jugador, la banca (dealer) y el mazo de cartas. El sistema consiste en una aplicación interactiva que simula una partida de Blackjack en la vida real en la cual el jugador tomará decisiones como si pedir cartas o plantarse, la banca actuará según las reglas del blackjack. El sistema se comunicará con el jugador a través de una interfaz y internamente la lógica del juego mediante clases que representan cartas, mazos, jugador y partida. Además la interacción con el medio externo al sistema se da mediante acciones del jugador y salidas visuales que muestran el estado del juego.</p>
        </div>

        <!-- Sección Detalles -->
        <div id="detalles" class="section">
            <h1>Casos de Uso</h1>
            
            <h2>Caso 1: Iniciar partida</h2>
            <p><strong>Descripción:</strong> El jugador inicia una partida, recibiendo dos cartas comenzando la ronda</p>
            <p><strong>Actor:</strong> Jugador</p>
            <p><strong>Flujo de Eventos:</strong></p>
            <ul>
                <li>El jugador selecciona "Iniciar Partida"</li>
                <li>El sistema mezcla el mazo de cartas</li>
                <li>Se reparten 2 cartas al jugador</li>
                <li>Se reparte 1 carta visible al dealer</li>
                <li>Se muestra el estado inicial del juego</li>
            </ul>

            <h2>Caso 2: Pedir carta</h2>
            <p><strong>Descripción:</strong> El jugador pide una carta adicional si aún no decide plantarse</p>
            <p><strong>Actor:</strong> Jugador</p>
            <p><strong>Flujo de Eventos:</strong></p>
            <ul>
                <li>El jugador selecciona "Pedir Carta"</li>
                <li>El sistema verifica que el jugador puede pedir carta</li>
                <li>Se reparte una nueva carta al jugador</li>
                <li>Se actualiza el puntaje del jugador</li>
                <li>Se verifica si el jugador se pasó de 21</li>
            </ul>

            <h2>Caso 3: Plantarse</h2>
            <p><strong>Descripción:</strong> El jugador decide plantarse sin aún no decide pedir carta</p>
            <p><strong>Actor:</strong> Jugador</p>
            <p><strong>Flujo de Eventos:</strong></p>
            <ul>
                <li>El jugador selecciona "Plantarse"</li>
                <li>El sistema procede con el turno del dealer</li>
                <li>Se revelan las cartas ocultas del dealer</li>
                <li>El dealer toma cartas según las reglas</li>
                <li>Se determina el ganador</li>
            </ul>
        </div>

        <!-- Sección Información Adicional -->
        <div id="informacion" class="section">
            <h1>Información Adicional</h1>
            <p>Esta sección contiene información complementaria sobre el proyecto TelJack y sus características principales.</p>
            
            <h2>Reglas del Blackjack</h2>
            <p>El objetivo del juego es obtener una puntuación lo más cercana posible a 21 sin pasarse. Las cartas tienen los siguientes valores:</p>
            <ul>
                <li>Cartas numéricas (2-10): Su valor nominal</li>
                <li>Figuras (J, Q, K): Valor de 10</li>
                <li>As: Valor de 1 u 11 (el que sea más favorable)</li>
            </ul>
            
            <h2>Características del Sistema</h2>
            <p>TelJack incluye las siguientes características principales:</p>
            <ul>
                <li>Interfaz intuitiva y fácil de usar</li>
                <li>Lógica de juego completa según reglas oficiales</li>
                <li>Manejo automático de As como 1 u 11</li>
                <li>Validaciones de movimientos legales</li>
                <li>Sistema de puntuación automático</li>
            </ul>
            
            <div class="info-box">
                <h3>Nota Importante</h3>
                <p>Este proyecto está diseñado con fines educativos para demostrar principios de programación orientada a objetos y desarrollo de software.</p>
            </div>
        </div>

        <!-- Nueva Sección: Arquitectura -->
        <div id="arquitectura" class="section">
            <h1>Arquitectura del Sistema</h1>
            <p>La arquitectura de TelJack está basada en principios de programación orientada a objetos, garantizando un código mantenible, escalable y fácil de entender.</p>
            
            <h2>Componentes Principales</h2>
            
            <h3>Clase Carta</h3>
            <p>Representa una carta individual del mazo con sus propiedades básicas:</p>
            <ul>
                <li>Palo (corazones, diamantes, tréboles, picas)</li>
                <li>Valor (A, 2-10, J, Q, K)</li>
                <li>Puntuación numérica</li>
            </ul>
            
            <h3>Clase Mazo</h3>
            <p>Gestiona el conjunto completo de cartas:</p>
            <ul>
                <li>Inicialización del mazo completo (52 cartas)</li>
                <li>Funcionalidad de mezclar cartas</li>
                <li>Repartir cartas individuales</li>
                <li>Verificar cartas restantes</li>
            </ul>
            
            <h3>Clase Jugador</h3>
            <p>Maneja el estado y acciones del jugador:</p>
            <ul>
                <li>Mano de cartas actual</li>
                <li>Cálculo de puntuación</li>
                <li>Estado del jugador (activo, plantado, perdido)</li>
                <li>Historial de movimientos</li>
            </ul>
            
            <h3>Clase Partida</h3>
            <p>Controla la lógica principal del juego:</p>
            <ul>
                <li>Inicialización de rondas</li>
                <li>Validación de movimientos</li>
                <li>Determinación de ganadores</li>
                <li>Manejo de turnos</li>
            </ul>

            <div class="info-box">
                <h3>Patrón de Diseño</h3>
                <p>El sistema implementa el patrón MVC (Modelo-Vista-Controlador) para separar la lógica de negocio de la presentación.</p>
            </div> 
        </div>

        <!-- Nueva Sección: Tecnologías -->
        <div id="tecnologias" class="section">
            <h1>Tecnologías Utilizadas</h1>
            <p>TelJack está construido utilizando tecnologías modernas y probadas que garantizan un rendimiento óptimo y una experiencia de usuario excepcional.</p>
            
            <div class="feature-grid">
                <div class="feature-card">
                    <h3>Frontend</h3>
                    <p>HTML5, CSS3 y JavaScript para crear una interfaz responsive y atractiva</p>
                </div>
                <div class="feature-card">
                    <h3>Programación OOP</h3>
                    <p>Implementación de principios de programación orientada a objetos</p>
                </div>
                <div class="feature-card">
                    <h3>Responsive Design</h3>
                    <p>Diseño adaptable para dispositivos móviles y desktop</p>
                </div>
                <div class="feature-card">
                    <h3>Animaciones CSS</h3>
                    <p>Transiciones suaves y efectos visuales atractivos</p>
                </div>
            </div>
            
            <h2>Especificaciones Técnicas</h2>
            
            <h3>Requisitos del Sistema</h3>
            <ul>
                <li>Navegador web moderno (Chrome, Firefox, Safari, Edge)</li>
                <li>JavaScript habilitado</li>
                <li>Resolución mínima: 320px de ancho</li>
                <li>Conexión a internet (para cargar recursos)</li>
            </ul>
            
            <h3>Características Técnicas</h3>
            <ul>
                <li>Código modular y reutilizable</li>
                <li>Manejo de errores robusto</li>
                <li>Optimización para rendimiento</li>
                <li>Documentación completa del código</li>
                <li>Testing unitario de componentes críticos</li>
            </ul>
            
            <div class="code-box">
                <h3>Ejemplo de Código - Clase Carta</h3>
                <pre>
class Carta {
    constructor(palo, valor) {
        this.palo = palo;
        this.valor = valor;
        this.puntuacion = this.calcularPuntuacion();
    }
    
    calcularPuntuacion() {
        if (this.valor === 'A') return 11;
        if (['J', 'Q', 'K'].includes(this.valor)) return 10;
        return parseInt(this.valor);
    }
}
                </pre>
            </div>
            
            <h2>Futuras Mejoras</h2>
            <p>El proyecto está diseñado para permitir futuras expansiones y mejoras:</p>
            <ul>
                <li>Modo multijugador en línea</li>
                <li>Sistema de estadísticas y logros</li>
                <li>Diferentes variantes de Blackjack</li>
                <li>Integración con base de datos</li>
                <li>Aplicación móvil nativa</li>
                <li>Sistema de apuestas virtuales</li>
            </ul>
        </div>
    </div>

    <script>
        // Función para mostrar una sección específica
        function showSection(sectionId) {
            // Ocultar todas las secciones
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.remove('active');
            });

            // Mostrar la sección seleccionada
            const targetSection = document.getElementById(sectionId);
            if (targetSection) {
                targetSection.classList.add('active');
            }

            // Actualizar el menú activo
            const navItems = document.querySelectorAll('.nav-item');
            navItems.forEach(item => {
                item.classList.remove('active');
            });

            // Marcar el item del menú como activo
            event.target.classList.add('active');
        }

        // Inicialización cuando se carga la página
        document.addEventListener('DOMContentLoaded', function() {
            // Asegurar que la primera sección esté activa
            const firstSection = document.querySelector('.section');
            const firstNavItem = document.querySelector('.nav-item');
            
            if (firstSection) firstSection.classList.add('active');
            if (firstNavItem) firstNavItem.classList.add('active');
        });
    </script>
</body>
</html>
