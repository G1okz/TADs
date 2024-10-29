# Proyecto de Servicios Web y Simulación de Aeropuerto

Este repositorio contiene dos proyectos independientes: un **servicio acortador de URLs** y una **simulación de gestión de aeropuerto**. Ambos proyectos implementan estructuras de datos y técnicas de seguridad y concurrencia vistas en clase.

---

## Proyecto 1: Servicio Acortador de URLs

Este servicio web convierte URLs largas en URLs cortas y amigables para compartir en redes sociales, correos electrónicos, y más. Las funciones principales incluyen:

### Funcionalidades

1. **Gestión de Usuarios**
   - `addUser(String username, String password)`: Registra usuarios con almacenamiento seguro de contraseñas usando hashing (PBKDF2) y salt.
   - `doLogin(String username, String password)`: Autentica usuarios para acceder a funciones protegidas del servicio.

2. **Acortamiento de URLs**
   - `shortenURL(String longURL)`: Convierte una URL larga en una URL corta sin necesidad de autenticación.
   - `shortenURL(String longURL, String username, String password)`: Convierte una URL larga en corta y la asocia con el usuario autenticado.

3. **Recuperación de URLs**
   - `getOriginalURL(String shortenedURL)`: Obtiene la URL larga de una URL corta, si no ha expirado.
   - `getOriginalURL(String shortenedURL, String username, String password)`: Obtiene la URL larga asociada al usuario autenticado.
   - `getURLsByUsername(String username, String password)`: Muestra todas las URLs guardadas por un usuario autenticado.

### Tecnologías
- Hashing de contraseñas: PBKDF2 con salt y 65536 iteraciones.
- Estructuras de datos eficientes para optimizar el almacenamiento y búsqueda de URLs.

---

## Proyecto 2: Simulación de Gestión de Aeropuerto

Este proyecto simula el flujo de pasajeros en un aeropuerto con una **cola** y una **pila** para gestionar el orden de llegada de los pasajeros y su posterior embarque en los aviones.

### Funcionalidades

1. **Estructuras de datos**
   - Cola con capacidad para 2 pasajeros.
   - Pila con capacidad para 3 pasajeros.
   - Lista para almacenar pasajeros embarcados en cada avión.

2. **Flujo de Pasajeros**
   - Los pasajeros llegan al aeropuerto y se insertan en la cola o en la pila según disponibilidad.
   - Se procesan en orden de llegada (primero la cola, luego la pila) para entregar su documentación y embarcar.

3. **Simulación (Principal.java)**
   - La clase `Principal.java` realiza una simulación de llegada de pasajeros y documentaciones procesadas. Finalmente, se imprime el estado de cada avión y la lista de pasajeros embarcados.

### Estructuras y Algoritmos
Este proyecto ilustra el manejo de estructuras de datos como pilas y colas, simulando un aeropuerto funcional con un orden de atención específico para los pasajeros.

---

## Requisitos

- **Java 11 o superior**
- **Maven** (opcional para gestión de dependencias)

---

## Instalación y Ejecución

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git
