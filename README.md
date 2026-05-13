# 🛑 Three.js Física e Interacción 3D

![Three.js](https://img.shields.io/badge/Three.js-black?style=for-the-badge&logo=three.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap_5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)

## 📖 Acerca del Proyecto

En este proyecto desarrollé e implementé un entorno 3D interactivo utilizando **Three.js** para demostrar el uso de colisiones avanzadas mediante **Octree** y físicas de proyectiles. Diseñé la experiencia con una perspectiva en primera persona, integrando una interfaz táctica (HUD) de alto contraste estilo *cyberpunk/sci-fi* construida sobre **Bootstrap 5**.

El objetivo principal fue lograr un rendimiento fluido (60+ FPS) al calcular múltiples colisiones simultáneas entre el jugador (Cápsula), la geometría estática del nivel (Octree) y decenas de proyectiles dinámicos (Esferas físicas renderizadas como diamantes de neón).

## ✨ Características Principales

*   **Físicas y Colisiones Octree:** Mapeo eficiente de la geometría del mundo (`collision-world.glb`) para colisiones precisas con el entorno, incluyendo rampas y escaleras.
*   **Movimiento en Primera Persona (FPS):** Controles fluidos de cámara y movimiento mediante la API de `PointerLock`, simulando gravedad y saltos.
*   **Generación de Proyectiles Dinámicos:** Capacidad para lanzar diamantes de color magenta neón (`OctahedronGeometry`), los cuales calculan sus propias colisiones con el mundo, el jugador y entre ellos mismos, rebotando y rotando en el aire.
*   **Tactical HUD (Interfaz de Usuario):** 
    *   Diseño superpuesto tipo *Glassmorphism* oscuro.
    *   Retícula (Crosshair) central dinámica.
    *   Paleta de colores de alto contraste (Cyan, Naranja, Verde Neón y Magenta).
    *   Monitor de rendimiento (FPS Stats) integrado visualmente en la interfaz.

## 🎮 Controles

| Acción | Tecla / Entrada |
| :--- | :--- |
| **Mirar / Apuntar** | `Mouse` (Mover) |
| **Lanzar Diamantes** | `Clic Izquierdo` (Mantener para más fuerza) |
| **Moverse** | `W`, `A`, `S`, `D` |
| **Saltar** | `Barra Espaciadora` |
| **Salir del juego** | `ESC` (Libera el cursor) |

## 🚀 Requisitos e Instalación

Debido a que el proyecto utiliza módulos de ES6 (`type="module"`) y carga modelos 3D externos (`.glb`), **no se puede abrir el archivo HTML directamente en el navegador dando doble clic** por restricciones de seguridad (CORS). Se requiere un servidor web local.

1.  Clona este repositorio:
    ```bash
    git clone [https://github.com/TU_USUARIO/TU_REPOSITORIO.git](https://github.com/TU_USUARIO/TU_REPOSITORIO.git)

2.  Abre la carpeta del proyecto en tu editor de código (por ejemplo, VS Code).
    
3.  Inicia un servidor local. Si usas VS Code, recomiendo la extensión Live Server:
    Haz clic derecho sobre index.html y selecciona Open with Live Server.
    
4.  El proyecto se abrirá automáticamente en http://127.0.0.1:5500/.

## 📁 Estructura del Directorio
El proyecto sigue una estructura limpia, separando la lógica 3D de la interfaz gráfica y los recursos estáticos:

```text
📦 raiz-del-proyecto
 ┣ 📂 assets
 ┃ ┣ 📂 build
 ┃ ┃ ┗ 📜 three.module.js        # Librería principal
 ┃ ┣ 📂 css
 ┃ ┃ ┗ 📜 main.css               # Estilos del HUD y efectos visuales
 ┃ ┣ 📂 js
 ┃ ┃ ┗ 📜 main.js                # Lógica de renderizado, físicas y controles
 ┃ ┣ 📂 jsm                      # Addons (Stats, Octree, Capsule, Loaders)
 ┃ ┗ 📂 models
 ┃   ┗ 📂 gltf
 ┃     ┗ 📜 collision-world.glb  # Modelo 3D del escenario
 ┗ 📜 index.html                 # Estructura del HUD y contenedor del Canvas
 ```
## 👨‍💻 Autor
Desarrollado por Antonio Yáñez Hernández.
Estudiante de Ingeniería en Sistemas Computacionales.
TecNM - Instituto Tecnológico de Pachuca (ITP)