# Uso de `fetch()` en JavaScript

## 1. ¿Qué es `fetch()`?

`fetch()` es una función nativa de JavaScript que permite **realizar solicitudes HTTP** (como GET, POST, PUT o DELETE) a un servidor o API.  
Se utiliza para **obtener o enviar datos** sin recargar la página.

`fetch()` devuelve una **promesa** que se resuelve cuando la solicitud finaliza, permitiendo trabajar con **datos asíncronos**.

---

## 2. Sintaxis básica

```javascript
fetch(url)
  .then(respuesta => respuesta.json())  // Convierte la respuesta a formato JSON
  .then(datos => console.log(datos))     // Maneja los datos recibidos
  .catch(error => console.error("Error:", error)); // Captura errores
```

### GET

```html
<!DOCTYPE html>
<html>
<head>
  <title>Ejemplo Fetch GET</title>
</head>
<body>
  <h1>Usuarios desde API</h1>
  <ul id="lista"></ul>

  <script>
    fetch("https://jsonplaceholder.typicode.com/users")
      .then(respuesta => respuesta.json())
      .then(datos => {
        const lista = document.getElementById("lista");
        datos.forEach(usuario => {
          const li = document.createElement("li");
          li.textContent = usuario.name + " - " + usuario.email;
          lista.appendChild(li);
        });
      })
      .catch(error => console.error("Error al obtener datos:", error));
  </script>
</body>
</html>
```

### POST

```javascript
fetch("https://jsonplaceholder.typicode.com/posts", {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({
    title: "Nuevo post",
    body: "Contenido de ejemplo",
    userId: 1
  })
})
  .then(respuesta => respuesta.json())
  .then(datos => console.log("Respuesta del servidor:", datos))
  .catch(error => console.error("Error al enviar datos:", error));
```

### Async/Await

```javascript
async function obtenerUsuarios() {
  try {
    const respuesta = await fetch("https://jsonplaceholder.typicode.com/users");
    const datos = await respuesta.json();
    console.log("Usuarios:", datos);
  } catch (error) {
    console.error("Error al obtener usuarios:", error);
  }
}

obtenerUsuarios();
```

## Errores comunes al usar `fetch()`

| Error | Causa posible | Solución recomendada |
|--------|----------------|----------------------|
| `TypeError: Failed to fetch` | La URL es incorrecta, el servidor no responde o hay problemas de conexión a Internet. | Verificar que la URL sea válida y el servidor esté en línea. |
| `SyntaxError: Unexpected token < in JSON` | La respuesta del servidor no está en formato JSON (por ejemplo, devuelve HTML). | Usar `response.text()` en lugar de `response.json()` o revisar la respuesta del servidor. |
| `CORS policy: No 'Access-Control-Allow-Origin' header` | El servidor no permite solicitudes desde otro dominio (problema de CORS). | Configurar el servidor para permitir el dominio o usar un proxy. |
| `404 Not Found` | La dirección del recurso solicitado no existe. | Revisar la URL o endpoint en la API. |
| `500 Internal Server Error` | Error interno del servidor al procesar la solicitud. | Revisar la lógica del servidor o los datos enviados. |
| `NetworkError` | Fallo de red o conexión interrumpida. | Comprobar conexión a Internet y volver a intentar la solicitud. |
| `Unexpected end of JSON input` | El servidor envió una respuesta vacía o incompleta. | Verificar que el servidor devuelva datos válidos y completos. |
| `Uncaught (in promise)` | La promesa fue rechazada pero no se manejó con `.catch()` o `try...catch`. | Agregar un bloque `.catch()` o `try...catch` para capturar el error. |

