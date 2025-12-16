# Centro-de-adopci-n-de-mascotas
# 🌾 Reactive Farm Deep Dive: Pets v

##  Descripción general

Este proyecto corresponde a la actividad **Reactive Farm Deep Dive**, cuyo objetivo es analizar, comprender y extender un proyecto existente en React, para finalmente aplicar los conocimientos adquiridos en el diseño de una aplicación propia.

El repositorio base analizado es **My Reactive Farm**, una aplicación construida con **React, Vite, Tailwind CSS y MockAPI**, orientada a la gestión y visualización de animales de una granja. A lo largo de esta actividad se estudia su estructura, manejo de estado, consumo de API, formularios y buenas prácticas de desarrollo con React.

Repositorio original e guía:
👉 [https://github.com/ethan-fullstack/my-reactive-farm](https://github.com/ethan-fullstack/my-reactive-farm)

---

##  1. Análisis del repositorio

### 📁 Estructura del proyecto

El proyecto está organizado de forma modular, separando responsabilidades:

* **components/**: componentes reutilizables como tarjetas, formularios y elementos UI.
* **pages/**: componentes de página que representan vistas completas.
* **api/**: archivos dedicados al consumo de datos (ej. `animalsApi.js`).
* **styles/**: configuración y uso de Tailwind CSS.
* **main.jsx / App.jsx**: punto de entrada y enrutamiento principal.

Esta estructura facilita el mantenimiento, la escalabilidad y la reutilización de componentes.

###  Manejo del estado (useState):

`useState` se utiliza para controlar información dinámica como:

* Listado de animales.
* Estados de carga (`loading`).
* Estados de error.
* Valores de formularios y filtros.

El estado permite que la interfaz se renderice automáticamente cuando los datos cambian.

###  Efectos (useEffect):

`useEffect` se emplea principalmente para:

* Cargar datos desde MockAPI al montar el componente.
* Ejecutar efectos secundarios controlados por dependencias.

Esto garantiza que los datos se obtengan una sola vez al iniciar la aplicación o cuando cambian ciertos estados.

###  Consumo de API (Axios y MockAPI) :

El proyecto consume datos desde **MockAPI** utilizando **Axios**, centralizando las peticiones HTTP en archivos específicos. Esto permite:

* Mejor control de errores.
* Código más limpio en los componentes.
* Reutilización de funciones de acceso a datos.

###  Formularios y validaciones:

Los formularios son **controlados**, es decir, cada campo depende del estado de React. Esto permite:

* Validaciones en tiempo real.
* Control total de los datos enviados.
* Mejor experiencia de usuario.

###  Uso de Tailwind CSS:

Tailwind CSS se utiliza para estilizar completamente la aplicación mediante clases utilitarias, logrando:

* Diseño consistente.
* Código CSS mínimo.
* Desarrollo rápido y responsive.

---

##  2. Cuestionario de React

### 1. Diferencia entre componente presentacional y componente de página

Un componente presentacional se enfoca únicamente en mostrar información (por ejemplo, `AnimalCard`), mientras que un componente de página maneja lógica, estado y composición de varios componentes (por ejemplo, la página principal que lista animales).

### 2. Uso de useState en el proyecto

`useState` se utiliza para manejar el estado de `animals`, que almacena la lista de animales, y `loading`, que controla si los datos aún se están cargando.

### 3. Uso de useEffect para cargar datos

Al iniciar el componente, `useEffect` ejecuta una función que llama a la API mediante Axios, guarda los datos en el estado y actualiza `loading`.

### 4. Manejo de loading, error y lista vacía

* **Loading:** se muestra un mensaje o spinner.
* **Error:** se informa al usuario que ocurrió un problema.
* **Lista vacía:** se muestra un mensaje indicando que no hay datos disponibles.

### 5. Formulario controlado en React

Un formulario controlado es aquel donde cada input depende del estado. En el proyecto, los campos del formulario se sincronizan con `useState`.

### 6. Separación de lógica de datos

Centralizar las peticiones en archivos como `animalsApi.js` mejora la organización, reutilización y mantenimiento del código.

### 7. Reutilización de AnimalCard

`AnimalCard` es reutilizable porque recibe datos por props y no depende de un contexto específico. Podría usarse en una app de adopción o inventario.

### 8. Accesibilidad

* Uso de etiquetas semánticas.
* Inputs con labels.
* Contraste adecuado de colores.

Estos elementos facilitan el uso por parte de todos los usuarios.

### 9. Filosofía de React antes de agregar una funcionalidad

Primero se identifican los datos, luego el estado necesario y finalmente dónde debe vivir la lógica.

### 10. Conceptos reutilizables

* Componentes reutilizables.
* Manejo de estado.
* Consumo de API.
* Formularios controlados.

---

##  3. Actividades prácticas

### Reglas de trabajo con Git

* Fork del repositorio original.
* Una rama por actividad:

  * `actividad-1`
  * `actividad-2`
  * `actividad-3`
* Pull Request y merge a `main` por cada actividad.

### Actividad 1: Modificar un estado

Se modificó el valor inicial de un estado existente para observar su impacto visual en el renderizado inicial.

### Actividad 2: Agregar un filtro nuevo

Se agregó un nuevo filtro, incorporando un estado adicional, un control en la interfaz y ajustes en la lógica de filtrado.

### Actividad 3: Mejorar el formulario

Se implementaron mejoras de experiencia de usuario, como validaciones más claras y retroalimentación visual.

---

##  4. Proyecto final individual ->

###  Idea del proyecto:

**Título:** (Pets V)

**Propósito:** Resolver una necesidad específica en este caso adopción de mascotas mediante una aplicación web dinámica.

###  Modelo de datos:

Entidad principal con campos relevantes definidos según el contexto del proyecto.

### Estructura:

* Componentes de UI.
* Componentes de página.
* Servicios de API.

###  Flujo de datos:

Los datos se consumen desde MockAPI al cargar la aplicación y se envían mediante formularios controlados.

###  Estado y UI

* Loading
* Error
* Empty
* Estados de formulario y filtros

### ⭐ Mejora personal

Se implementó una funcionalidad adicional para mejorar la experiencia del usuario y ampliar el alcance de la aplicación.

---

## 📅 Fechas de la actividad

* **Apertura:** 18 de noviembre de 2025
* **Cierre:** 21 de noviembre de 2025

---


