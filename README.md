<div align="center">

  <img src="https://hwcyvqnswnhfixrlgmas.supabase.co/storage/v1/object/sign/zimoxy/Stevezimoxysaludo.png?token=eyJraWQiOiJmNmY1NDg4Zi04YTY5LTRhNmUtYTFmMi1jYTBjY2MzY2YyOWIiLCJhbGciOiJFUzI1NiJ9.eyJ1cmwiOiJ6aW1veHkvU3RldmV6aW1veHlzYWx1ZG8ucG5nIiwic2NvcGUiOiJkb3dubG9hZCIsImlhdCI6MTc5NDkxOTE0NywiZXhwIjozMzcxNzE5MTQ3fQ.ZcofHnzTk5PVYzeYvgDLyFuWNb6K1auN18r28i3ZVKeNpdMkudG5uakkWCILEqwZnJ4ymIhOgeNgkfl2TEzYkA" alt="Zimoxy Steve Mascot" width="220" />

  # ⚡ ZIMOXY CLIENT · PLATAFORMA DE MINECRAFT
  **El cliente alternativo y competitivo de Minecraft sin conexión a Microsoft.**

  [![.NET 9](https://img.shields.io/badge/.NET-9.0_WPF-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
  [![C#](https://img.shields.io/badge/C%23-100%25_Nativo-239120?style=for-the-badge&logo=c-sharp&logoColor=white)](https://dotnet.microsoft.com/)
  [![No Electron](https://img.shields.io/badge/Engine-Zero_Electron-00F5A0?style=for-the-badge&logo=speedtest&logoColor=black)](https://github.com/)
  [![Next.js 15](https://img.shields.io/badge/Web-Next.js_15-black?style=for-the-badge&logo=next.js&logoColor=white)](https://zimoxyclient.vercel.app)
  [![Discord.js](https://img.shields.io/badge/Discord-Bot_v14-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/vemQ8gAVDr)
  [![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

  <br />

  [🌐 Portal Web Oficial](https://zimoxyclient.vercel.app) • 
  [💬 Servidor de Discord](https://discord.gg/vemQ8gAVDr) • 
  [📥 Descargar Cliente](#-instalación-y-descarga) • 
  [📖 Características](#-características-del-cliente)

</div>

---

## 📌 ¿Qué es Zimoxy?

**Zimoxy** es un cliente y ecosistema de Minecraft diseñado desde cero para jugadores que buscan una experiencia competitiva de alto rendimiento con **su propio sistema de autenticación, skins y cosméticos privados**, sin ninguna necesidad ni dependencia de cuentas de Microsoft o Mojang.

Inspirado en la fluidez e interfaz de **Lunar Client**, Zimoxy prescinde por completo de tecnologías pesadas como Electron: el launcher está construido en **C# nativo sobre WPF (.NET 9)** con aceleración gráfica directa por hardware (DirectX), arranque ultra rápido y consumo inferior a **60 MB de memoria RAM**.

---

## ✨ Características del Cliente

### 🚀 Rendimiento Extremo (+340% FPS)
* **Sodium Core Integrado:** Motor gráfico moderno reescrito que multiplica los fotogramas por segundo y elimina tirones de frametime.
* **Lithium & Optimización de Física:** Reducción drástica del uso de CPU en chunks y entidades.
* **Iris Shaders Engine:** Compatibilidad total con shaders sin pérdida crítica de rendimiento.

### 🛡️ Autenticación Nativa (Sin Microsoft)
* Acceso con usuario y contraseña propios registrados en la plataforma Zimoxy.
* Inicio de sesión rápido con **Discord OAuth2** mediante callback seguro de loopback local.
* Sesión persistente cifrada en `%APPDATA%\.zimoxy\zimoxy-user.json`.

### 🎛️ Módulos & HUDs Competitivos (Estilo Lunar Client)
Interruptores (*Toggle Switches*) interactivos configurables en tiempo real:
* **Keystrokes Display:** Visualización de teclas `W`, `A`, `S`, `D`, `ESPACIO` y ratón.
* **CPS Counter:** Contador de clics por segundo en tiempo real para PvP.
* **Armor Status HUD:** Durabilidad de piezas de armadura y armas en pantalla.
* **Direction / Compass HUD:** Brújula visual superior con coordenadas y grados.
* **Fullbright (Gamma Boost):** Visibilidad al 100% en cuevas y durante la noche.
* **Freelook 360° (Perspective):** Rotación libre de cámara con la tecla `ALT`.
* **Reach Display:** Métrica exacta de distancia de impacto por bloque.
* **Motion Blur:** Desenfoque dinámico cinematográfico para giros de cámara.
* **Item Physics 3D:** Físicas realistas de objetos soltados en el suelo.
* **Zimoxy Cosmetic Core:** Motor nativo de renderizado de capas y skins.

### 👕 Armario & Cosméticos Exclusivos (Wardrobe)
* **Previsualización 3D:** Renderizado del cuerpo completo de la skin del jugador en vivo.
* **Capas Zimoxy:** Capa Fundador, Capa Galaxia Estelar, Capa Flama Neón, Capa Dragón Carmesí y Capa Esmeralda.
* **Alas y Accesorios:** Alas Angélicas Blancas, Alas de Dragón del End, Bandana Ninja Zimoxy y Corona Imperial.
* Equipamiento instantáneo desde el cliente sincronizado con la red de servidores.

### 🌐 Navegador de Servidores en Vivo
* Medición de latencia de ping en tiempo real en milisegundos (`ms`).
* Contador de jugadores en vivo y botón de conexión directa con protocolo TCP optimizado:
  * **Zimoxy Survival Privado 1.21** (`play.zimoxy.net`)
  * **Zimoxy PvP & Practice Arena** (`pvp.zimoxy.net`)
  * **Zimoxy Custom SkyBlock** (`sky.zimoxy.net`)

### ⚙️ Ajustes Avanzados
* Control deslizante (*Slider*) de asignación de RAM interactivo (de **2 GB a 16 GB**) con previsualización en vivo de flags JVM (`-Xmx`, `-Xms`, `-XX:+UseG1GC`).
* Selector de resolución de pantalla (FHD 1080p, 2K, HD o Pantalla Completa nativa).
* Integración con **Discord Rich Presence**.
* Acceso directo a la carpeta del juego con un solo clic (`📂 .zimoxy`).

---

## 🏗️ Arquitectura del Proyecto

El repositorio está estructurado en módulos desacoplados para máxima escalabilidad:

```text
Zimoxy/
├── launcher/             # Cliente nativo de escritorio en C# / WPF (.NET 9)
│   ├── App.xaml          # Estilos globales, paleta oscura y controles Lunar (Toggles, Sliders)
│   ├── MainWindow.xaml   # Interfaz principal (Header, Launch Deck, 6 Vistas dinámicas)
│   ├── MainWindow.xaml.cs# Lógica de auth, API REST, Discord OAuth y lanzamiento
│   └── ZimoxyClient.csproj
│
├── web/ & vercel/        # Portal Web Oficial (Next.js 15, Tailwind CSS, Supabase)
│   ├── src/app/          # Rutas de login, registro, dashboard de skins y tienda
│   └── src/app/api/auth/ # Endpoints de autenticación, validación y webhook de Discord
│
├── bot/ & Zimoxy-bot/    # Bot de Discord Oficial (Discord.js v14 + Gemini Flash AI)
│   ├── src/index.ts      # Verificación de miembros, tickets, roles por idioma y logs
│   └── package.json
│
├── env/                  # Plantillas de variables de entorno (Config y Secrets)
└── README.md             # Documentación principal
```

---

## 📥 Instalación y Descarga

### Para Jugadores

1. **Crear Cuenta:** Regístrate en el portal web oficial: [zimoxyclient.vercel.app/login.es](https://zimoxyclient.vercel.app/login.es).
2. **Descargar Cliente:** Descarga la versión más reciente de **Zimoxy Client**:
   * Descarga directa: [`ZimoxyClient.exe`](launcher/bin/Release/publish/ZimoxyClient.exe)
   * Paquete comprimido: [`zimoxy-client.zip`](launcher/dist/zimoxy-client.zip)
3. **Ejecutar:** Abre `ZimoxyClient.exe`, ingresa tus credenciales y presiona **JUGAR ZIMOXY 1.21**.

> **Requisitos:**
> * Windows 10 / Windows 11 (64-bit).
> * Java 21 o superior instalado.
> * 2 GB de memoria RAM libre mínima (4 GB recomendado).

---

## 🛠️ Compilación para Desarrolladores

Si deseas compilar el launcher desde el código fuente:

### Requisitos Previos
* [.NET 9.0 SDK](https://dotnet.microsoft.com/download/dotnet/9.0) instalado.
* Git.

### Pasos de Compilación

```bash
# 1. Clonar el repositorio
git clone https://github.com/FluxzyCorporations/Zimoxy.git
cd Zimoxy/launcher

# 2. Restaurar dependencias
dotnet restore

# 3. Compilar en modo Debug
dotnet build

# 4. Publicar ejecutable en Release optimizado
dotnet publish -c Release -o bin/Release/publish
```

El ejecutable standalone se generará en `launcher/bin/Release/publish/ZimoxyClient.exe`.

---

## 🌐 Servicios y Enlaces Oficiales

| Recurso | Enlace |
|---|---|
| **Portal Web & Registro** | [zimoxyclient.vercel.app](https://zimoxyclient.vercel.app) |
| **Comunidad de Discord** | [discord.gg/vemQ8gAVDr](https://discord.gg/vemQ8gAVDr) |
| **Servidor de Minecraft** | `play.zimoxy.net` (Puerto: `25565`) |
| **Servidor PvP Arena** | `pvp.zimoxy.net` |
| **Repositorio Bot de Soporte** | [Zimoxy-Support-bot](https://github.com/FluxzyCorporations/Zimoxy-Support-bot) |

---

## 📄 Licencia

Este proyecto está distribuido bajo la licencia **MIT**. Consulta el archivo `LICENSE` para más información.

---

<div align="center">
  <sub>Desarrollado con pasión para la comunidad de Minecraft · <b>Zimoxy Ecosystem © 2026</b></sub>
</div>
