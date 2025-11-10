# Introducción a React

## 1. ¿Qué es React?

**React** es una **biblioteca de JavaScript** creada por **Facebook** (ahora Meta) para construir **interfaces de usuario (UI)** dinámicas y eficientes.  
Se utiliza principalmente para desarrollar **aplicaciones web de una sola página (SPA – Single Page Applications)**.

React se basa en **componentes**, que son bloques reutilizables de código que representan partes de la interfaz (botones, formularios, menús, etc.).

---

## 2. Características principales

| Característica | Descripción |
|----------------|-------------|
| **Componentes** | La UI se divide en piezas pequeñas y reutilizables llamadas componentes. |
| **JSX** | Sintaxis que combina JavaScript y HTML para describir cómo se verá la interfaz. |
| **Virtual DOM** | React usa una copia virtual del DOM para actualizar solo lo necesario, mejorando el rendimiento. |
| **Unidireccionalidad** | Los datos fluyen en una sola dirección (de padre a hijo), lo que hace el código más predecible. |
| **Reactividad** | Cuando cambian los datos, React actualiza automáticamente la interfaz. |

---

## 3. Ejemplo básico

```jsx
// App.js
import React from "react";

function App() {
  return (
    <div>
      <h1>¡Hola, React!</h1>
      <p>Este es mi primer componente.</p>
    </div>
  );
}

export default App;
```


## Componentes

En React, todo es un componente.
Pueden ser funcionales (los más comunes) o de clase (más antiguos).

```jsx
function Saludo({ nombre }) {
  return <h2>Hola, {nombre}!</h2>;
}

// Uso en otro componente
function App() {
  return (
    <div>
      <Saludo nombre="Ian" />
      <Saludo nombre="María" />
    </div>
  );
}
```

## Estado(useState)

El estado permite que los componentes recuerden información que puede cambiar con el tiempo.

```jsx
import React, { useState } from "react";

function Contador() {
  const [contador, setContador] = useState(0);

  return (
    <div>
      <p>Has hecho clic {contador} veces</p>
      <button onClick={() => setContador(contador + 1)}>Sumar</button>
    </div>
  );
}
```

## Eventos

React maneja los eventos de forma similar a JavaScript, pero con camelCase y funciones.

```jsx
function Boton() {
  const mostrarMensaje = () => alert("¡Hiciste clic!");
  
  return <button onClick={mostrarMensaje}>Clic aquí</button>;
}
```

## Conexion con Backend

React puede conectarse a un backend usando fetch() o librerías como Axios.

```jsx
import React, { useEffect, useState } from "react";

function Usuarios() {
  const [usuarios, setUsuarios] = useState([]);

  useEffect(() => {
    fetch("http://localhost:3000/usuarios")
      .then(res => res.json())
      .then(data => setUsuarios(data))
      .catch(err => console.error("Error al cargar:", err));
  }, []);

  return (
    <div>
      <h2>Lista de usuarios</h2>
      <ul>
        {usuarios.map(u => (
          <li key={u.id}>{u.nombre}</li>
        ))}
      </ul>
    </div>
  );
}
```

### Estructura estandar de un proyecto con REACT

```pgsql
mi-proyecto/
├── public/
│   └── index.html
├── src/
│   ├── App.js
│   ├── index.js
│   ├── componentes/
│   │   ├── Navbar.js
│   │   └── Footer.js
│   └── estilos/
│       └── App.css
└── package.json
```
