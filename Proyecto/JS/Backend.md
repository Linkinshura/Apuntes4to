# Introducción al Backend con Base de Datos

## 1. ¿Qué es el backend?

El **backend** es la parte del desarrollo web que se encarga de **procesar la lógica del servidor**, **manejar la base de datos** y **responder a las solicitudes** del usuario.

Mientras el **frontend** (HTML, CSS, JavaScript) controla lo que el usuario ve en pantalla, el **backend** gestiona lo que ocurre detrás del sitio web:
- Almacenar y recuperar datos.
- Validar información.
- Controlar usuarios, sesiones y permisos.
- Comunicarse con otras aplicaciones o servicios.

El backend generalmente se desarrolla con lenguajes como **JavaScript (Node.js)**, **Python**, **PHP**, **Java**, o **C#**, entre otros.

---

## 2. Componentes básicos del backend

| Componente | Función | Ejemplo |
|-------------|----------|---------|
| **Servidor** | Atiende las peticiones que llegan desde el navegador. | Node.js con Express, Apache, Nginx |
| **Base de datos (BD)** | Guarda la información que usa la aplicación. | MySQL, PostgreSQL, MongoDB |
| **API** | Es el "puente" que permite que el frontend y el backend se comuniquen. | Rutas creadas con Express o Flask |
| **Lógica del negocio** | Contiene las reglas de funcionamiento del sistema. | Validaciones, cálculos, permisos |

---

## 3. Flujo básico de funcionamiento

1. El usuario interactúa con el **frontend** (por ejemplo, completa un formulario).  
2. El frontend envía una **solicitud HTTP** al **backend** (usando `fetch()` o AJAX).  
3. El **servidor backend** procesa la solicitud y, si es necesario, consulta o modifica datos en la **base de datos**.  
4. El backend envía una **respuesta** al frontend (por ejemplo, un mensaje de éxito o los datos solicitados).  
5. El frontend muestra la respuesta al usuario.

---

## 4. Ejemplo básico con Node.js y Express

```javascript
// server.js
const express = require("express");
const mysql = require("mysql");
const app = express();

app.use(express.json());

// Conexión a la base de datos MySQL
const conexion = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "",
  database: "ejemplo_db"
});

conexion.connect(error => {
  if (error) throw error;
  console.log("Conectado a la base de datos");
});

// Ruta para obtener todos los usuarios
app.get("/usuarios", (req, res) => {
  conexion.query("SELECT * FROM usuarios", (error, resultados) => {
    if (error) throw error;
    res.json(resultados);
  });
});

// Servidor en puerto 3000
app.listen(3000, () => {
  console.log("Servidor escuchando en http://localhost:3000");
});
```

## Conexion con Frontend

```html
<script>
fetch("http://localhost:3000/usuarios")
  .then(res => res.json())
  .then(datos => console.log(datos))
  .catch(err => console.error("Error al obtener usuarios:", err));
</script>
```
