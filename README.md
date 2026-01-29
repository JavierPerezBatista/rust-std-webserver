# Rust Std Webserver
Webserver HTTP multithread implementado exclusivamente con la biblioteca estándar de Rust (std::net, std::thread), inspirado en el proyecto final del capítulo 21 del Rust Book. Soporta peticiones GET simples, un thread pool personalizado y parsing básico de requests HTTP/1.1, y está pensado como punto de partida para experimentar con desarrollo web de bajo nivel en Rust.


## 🚀 Características
Servidor TCP listener en puerto configurable (por defecto: 127.0.0.1:7878).

Thread pool propio para manejar conexiones concurrentes.

Parsing manual de HTTP GET (sin regex ni crates externos).

Respuestas HTTP/1.1 con estados 200 y 404 y cabeceras mínimas.

Manejo de rutas estáticas sencillas, como /hello.html.

100% biblioteca estándar, sin dependencias externas en Cargo.toml.

Tests básicos para el thread pool y/o lógica HTTP (según vaya evolucionando el proyecto).

## 📁 Estructura del proyecto
```text
rust-std-webserver/
├── src/
│ ├── main.rs # Punto de entrada, arranca el servidor
│ ├── lib.rs # Lógica compartida (por ejemplo, ThreadPool)
├── Cargo.toml
├── hello.html
├── 404.html
└── README.md
```

## 🛠️ Instalación y uso
Clonar el repositorio:

```bash
git clone https://github.com/tu-usuario/rust-std-webserver.git
cd rust-std-webserver
```

Asegurarte de tener Rust instalado (stable):

```bash
rustup default stable
```

Ejecutar el servidor:

```bash
cargo run
```

Abrir en el navegador:

URL por defecto: http://127.0.0.1:7878/

Prueba también una ruta estática como http://127.0.0.1:7878/hello.html

## 🧪 Tests

```bash
cargo test
```

## 🔮 Mejoras previstas (Roadmap)
Este proyecto nace como ejercicio del libro, pero la idea es ir iterando y acercarlo a un entorno más real:

 Soporte para método POST y lectura de cuerpo de la petición.

 Logging configurable mediante variables de entorno.

 Configuración vía argumentos de línea de comandos (sin crates externos).

 Servir ficheros estáticos desde un directorio configurable.

 Manejo sencillo de rutas (router mínimo).

 Dockerfile para levantar el servidor fácilmente.

## 📄 Licencia
El proyecto está disponible bajo la licencia MIT.

## 🙋 Sobre el proyecto
Ejercicio basado en el proyecto final del capítulo 21 del Rust Programming Language adaptado y extendido para práctica personal.