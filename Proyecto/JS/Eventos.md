# Eventos en JavaScript

## 1. ¿Qué es un evento?

Un **evento** en JavaScript es una **acción que ocurre en la página web** y que puede ser detectada por el navegador.  
Algunos ejemplos de eventos son:

- Hacer clic en un botón.
- Pasar el mouse sobre un elemento.
- Escribir en un campo de texto.
- Cargar completamente la página.
- Presionar una tecla.

JavaScript permite **escuchar** esos eventos y **responder** ejecutando funciones cuando ocurren.

## 2. Formas de manejar eventos

### a) A través del atributo HTML

Se puede definir un evento directamente en una etiqueta HTML utilizando atributos como `onclick`, `onchange`, `onmouseover`, etc.

```html
<button onclick="mostrarMensaje()">Haz clic aquí</button>

<script>
  function mostrarMensaje() {
    alert("¡Botón presionado!");
  }
</script>
```

## Tabla de eventos en JavaScript

| Evento | Tipo de evento | Descripción | Ejemplo de uso |
|--------|----------------|--------------|----------------|
| `click` | Ratón | Ocurre cuando el usuario hace clic sobre un elemento. | `elemento.addEventListener("click", funcion)` |
| `dblclick` | Ratón | Se ejecuta cuando el usuario hace doble clic sobre un elemento. | `elemento.addEventListener("dblclick", funcion)` |
| `mouseover` | Ratón | Se activa cuando el puntero pasa sobre un elemento. | `elemento.addEventListener("mouseover", funcion)` |
| `mouseout` | Ratón | Se activa cuando el puntero sale de un elemento. | `elemento.addEventListener("mouseout", funcion)` |
| `mousemove` | Ratón | Se ejecuta cuando el puntero se mueve dentro de un elemento. | `elemento.addEventListener("mousemove", funcion)` |
| `mousedown` | Ratón | Ocurre al presionar un botón del mouse. | `elemento.addEventListener("mousedown", funcion)` |
| `mouseup` | Ratón | Ocurre al soltar un botón del mouse. | `elemento.addEventListener("mouseup", funcion)` |
| `keydown` | Teclado | Se ejecuta cuando se presiona una tecla. | `document.addEventListener("keydown", funcion)` |
| `keyup` | Teclado | Se ejecuta cuando se suelta una tecla. | `document.addEventListener("keyup", funcion)` |
| `keypress` | Teclado | Se ejecuta mientras se mantiene presionada una tecla (ya en desuso). | `document.addEventListener("keypress", funcion)` |
| `input` | Formularios | Se activa cada vez que cambia el valor de un campo de texto. | `input.addEventListener("input", funcion)` |
| `change` | Formularios | Se ejecuta cuando el valor de un campo cambia y se pierde el foco. | `select.addEventListener("change", funcion)` |
| `submit` | Formularios | Se activa cuando se envía un formulario. | `form.addEventListener("submit", funcion)` |
| `focus` | Formularios | Ocurre cuando un elemento obtiene el foco (por ejemplo, al hacer clic en un input). | `input.addEventListener("focus", funcion)` |
| `blur` | Formularios | Ocurre cuando un elemento pierde el foco. | `input.addEventListener("blur", funcion)` |
| `load` | Página | Se ejecuta cuando la página o un recurso ha cargado completamente. | `window.addEventListener("load", funcion)` |
| `resize` | Ventana | Se ejecuta cuando el tamaño de la ventana del navegador cambia. | `window.addEventListener("resize", funcion)` |
| `scroll` | Ventana | Ocurre cuando el usuario hace scroll en la página. | `window.addEventListener("scroll", funcion)` |
| `contextmenu` | Ratón | Se activa al hacer clic derecho (abrir menú contextual). | `elemento.addEventListener("contextmenu", funcion)` |
| `error` | Página | Se ejecuta cuando ocurre un error al cargar un recurso o script. | `window.addEventListener("error", funcion)` |

