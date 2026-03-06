# 🚀 WorkHub Coworking – Sistema de Gestión de Reservas

![HTML](https://img.shields.io/badge/HTML5-Structure-orange?style=for-the-badge\&logo=html5)
![CSS](https://img.shields.io/badge/CSS3-Styling-blue?style=for-the-badge\&logo=css3)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5-purple?style=for-the-badge\&logo=bootstrap)
![JavaScript](https://img.shields.io/badge/JavaScript-DOM-yellow?style=for-the-badge\&logo=javascript)

Aplicación web desarrollada como **primera iteración del sistema digital de reservas para WorkHub Coworking**, creada durante el **Módulo 1 – Fundamentos de Desarrollo Front-End**.

El sistema permite visualizar espacios de coworking, gestionar reservas y simular disponibilidad utilizando únicamente **tecnologías de frontend**.

---

# 📚 Tabla de Contenido

* [Contexto del Proyecto](#contexto-del-proyecto)
* [Objetivo del Proyecto](#objetivo-del-proyecto)
* [Tecnologias Utilizadas](#tecnologias-utilizadas)
* [Arquitectura del Proyecto](#arquitectura-del-proyecto)
* [Estructura de Carpetas](#estructura-de-carpetas)
* [Funcionalidades Implementadas](#funcionalidades-implementadas)
* [Componentes Bootstrap Utilizados](#componentes-bootstrap-utilizados)
* [Manipulacion del DOM](#manipulacion-del-dom)
* [Diseño y UX](#diseño-y-ux)
* [Como ejecutar el proyecto](#como-ejecutar-el-proyecto)
* [Estado del Proyecto](#estado-del-proyecto)
* [Mejoras Futuras](#mejoras-futuras)
* [Autores](#autores)

---

# 🧠 Contexto del Proyecto

WorkHub Coworking es una empresa que ofrece **espacios de trabajo compartidos**, salas de reuniones y oficinas privadas.

Actualmente las reservas se gestionan mediante:

* WhatsApp
* Correos electrónicos
* Hojas de cálculo

Esto genera problemas como:

* duplicación de reservas
* mala gestión de horarios
* dificultad para escalar el servicio
* pérdida de información

Por esta razón se plantea el desarrollo de un **sistema web que centralice la gestión de reservas**.

En esta primera fase se desarrolla un **MVP (Minimum Viable Product)** en frontend.

---

# 🎯 Objetivo del Proyecto

Construir una **aplicación web estática** que permita:

✔ visualizar espacios de coworking
✔ reservar espacios de trabajo
✔ gestionar reservas creadas
✔ simular disponibilidad de espacios

Utilizando:

* HTML semántico
* CSS personalizado
* Bootstrap 5
* JavaScript (DOM)

---

# 🧰 Tecnologías Utilizadas

| Tecnología   | Uso                    |
| ------------ | ---------------------- |
| HTML5        | estructura del sitio   |
| CSS3         | estilos personalizados |
| Bootstrap 5  | framework de diseño    |
| JavaScript   | manipulación del DOM   |
| Google Fonts | tipografía             |

Fuentes utilizadas:

* **Inter**
* **JetBrains Mono**

---

# 🏗 Arquitectura del Proyecto

El sistema funciona completamente en el **frontend**.

Los datos se simulan mediante **arrays en JavaScript**.

Ejemplo de datos de espacios:

```javascript
const spaces = [
{
id: 1,
name: "Suite de Cuarzo",
type: "Oficina Privada",
capacity: 4,
price: "$45/hr",
available: true
}
]
```

Las reservas se almacenan temporalmente en memoria:

```javascript
let bookings = []
```

---

# 📂 Estructura de Carpetas

```
project-root
│
├── index.html
├── registro.html
│
├── css
│   ├── style.css
│   └── acceso.css
│
├── js
│   ├── app.js
│   └── acceso.js
│
└── README.md
```

Descripción:

| Archivo       | Descripción                    |
| ------------- | ------------------------------ |
| index.html    | página principal               |
| registro.html | formulario de acceso           |
| style.css     | estilos principales            |
| acceso.css    | estilos del login              |
| app.js        | lógica del sistema             |
| acceso.js     | manejo del formulario de login |

---

# ⚙ Funcionalidades Implementadas

## 🏠 Página Principal

Incluye:

* navbar de navegación
* hero section
* carrusel de imágenes
* listado de espacios disponibles

Los espacios se muestran mediante **cards dinámicas generadas con JavaScript**.

---

# 🏢 Visualización de Espacios

Los espacios disponibles se renderizan dinámicamente:

```javascript
renderSpaces()
```

Cada espacio muestra:

* nombre
* tipo de espacio
* capacidad
* precio
* estado de disponibilidad

---

# 📅 Sistema de Reservas

El sistema permite reservar espacios mediante un formulario.

Campos disponibles:

* nombre del usuario
* espacio a reservar
* fecha
* hora

Evento utilizado:

```javascript
document.getElementById("booking-form")
.addEventListener("submit", handleBooking)
```

Al enviar el formulario:

1. se captura el evento
2. se crea un objeto reserva
3. se guarda en el array de reservas
4. se muestra confirmación
5. se limpia el formulario

---

# 📋 Gestión de Reservas

Los usuarios pueden:

* ver sus reservas
* cancelar reservas existentes

Las reservas se muestran dinámicamente en el DOM.

Ejemplo de estructura:

```
Reserva
Espacio
Usuario
Fecha
Hora
ID de referencia
```

---

# ⚙ Panel de Administración

El sistema incluye una sección **Admin**.

Permite:

* visualizar espacios
* activar o desactivar disponibilidad

Esto se controla mediante un **toggle switch**.

```javascript
toggleAvailability(id)
```

---

# 🧩 Componentes Bootstrap Utilizados

El proyecto utiliza múltiples componentes del framework.

Entre ellos:

* Navbar
* Carousel
* Cards
* Buttons
* Forms
* Grid System

Ejemplo de grid:

```
container
row
col
```

---

# 🧠 Manipulación del DOM

Durante el proyecto se utilizaron funciones como:

* `getElementById()`
* `querySelector()`
* `createElement()`
* `appendChild()`
* `innerHTML()`
* `addEventListener()`

Estas permiten **generar contenido dinámico sin backend**.

---

# 🎨 Diseño y UX

El diseño del proyecto incluye:

* interfaz moderna tipo dashboard
* animaciones CSS
* efectos glassmorphism
* sistema de notificaciones toast
* layout responsive
* tipografía profesional

El objetivo fue crear una **experiencia visual moderna y clara para el usuario**.

---

# ▶ Cómo ejecutar el proyecto

1️⃣ Clonar el repositorio

```
git clone https://github.com/tu-usuario/workhub-coworking.git
```

2️⃣ Abrir el proyecto en **VS Code**

3️⃣ Ejecutar usando **Live Server**

o abrir directamente:

```
index.html
```

---

# 📌 Estado del Proyecto

✔ MVP funcional completado
✔ interfaz responsive
✔ sistema de reservas simulado

Actualmente el sistema **no utiliza backend ni base de datos**.

---

# 🚧 Mejoras Futuras

En próximas iteraciones se planea implementar:

* backend con Node.js
* base de datos
* autenticación de usuarios
* API REST
* persistencia de reservas
* panel administrativo avanzado
* despliegue en la nube

---

# 👩‍💻 Autores

Gloria Cornelio
Sergio Salina
Valentina Medina
Marcelo Martinez
Mauricio Diaz
Rodrigo Contreras


Sistema de reservas para **WorkHub Coworking**.

---

## 🖼 Vista previa

![Preview del sitio](./asset/imagenes/Captura%20de%20pantalla%202026-03-06%20150341.png)



⭐ Proyecto educativo con fines de aprendizaje en **desarrollo Front-End**.
