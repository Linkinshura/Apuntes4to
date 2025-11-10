# DOM

El DOM (Document Object Model) es una representación del documento HTML en forma de árbol de objetos.

Este HTML se ve en el DOM:

```html
<body>
  <h1 id="titulo">Bienvenidos</h1>
  <p class="texto">Esto es un párrafo.</p>
</body>
```

Document
 └── html
      └── body
           ├── h1 (id="titulo")
           └── p (class="texto")

## Métodos principales del DOM

| Método | Descripción | Ejemplo de uso |
|--------|--------------|----------------|
| `getElementById("id")` | Selecciona un elemento por su atributo `id`. | `document.getElementById("titulo")` |
| `getElementsByClassName("clase")` | Selecciona todos los elementos que tienen una clase específica (devuelve una colección). | `document.getElementsByClassName("item")` |
| `getElementsByTagName("etiqueta")` | Selecciona todos los elementos con una etiqueta determinada. | `document.getElementsByTagName("p")` |
| `querySelector("selector")` | Devuelve el primer elemento que coincide con el selector CSS especificado. | `document.querySelector(".texto")` |
| `querySelectorAll("selector")` | Devuelve todos los elementos que coinciden con el selector CSS (como una lista). | `document.querySelectorAll("div")` |
| `createElement("etiqueta")` | Crea un nuevo elemento HTML. | `document.createElement("li")` |
| `appendChild(elemento)` | Agrega un elemento dentro de otro como hijo. | `lista.appendChild(nuevoItem)` |
| `removeChild(elemento)` | Elimina un elemento hijo de otro. | `contenedor.removeChild(parrafo)` |
| `remove()` | Elimina un elemento directamente del DOM. | `elemento.remove()` |
| `setAttribute("atributo", "valor")` | Cambia o agrega un atributo a un elemento. | `img.setAttribute("src", "imagen.jpg")` |
| `getAttribute("atributo")` | Obtiene el valor de un atributo de un elemento. | `link.getAttribute("href")` |
| `classList.add("clase")` | Agrega una clase CSS al elemento. | `div.classList.add("activo")` |
| `classList.remove("clase")` | Quita una clase CSS del elemento. | `div.classList.remove("activo")` |
| `textContent` | Cambia o obtiene el texto interno de un elemento. | `titulo.textContent = "Nuevo texto"` |
| `innerHTML` | Cambia o obtiene el contenido HTML interno de un elemento. | `caja.innerHTML = "<b>Hola</b>"` |
| `style.propiedad` | Modifica estilos CSS directamente desde JS. | `titulo.style.color = "red"` |
