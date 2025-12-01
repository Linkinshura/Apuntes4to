# Javascript II

### Crea una función llamada handleSubmit() que se ejecute cuando el usuario envíe el formulario.
La función debe:

Prevenir el envío por defecto del formulario.

Obtener el valor del input con id "nombre".

Mostrar en consola:
"Formulario enviado por: [nombre]"

base HTML:

<form id="form">
    <input type="text" id="nombre" placeholder="Escribe tu nombre" />
    <button type="submit">Enviar</button>
</form>


### ¿Qué método se utiliza para evitar que un formulario se envíe por defecto dentro de un handleSubmit?


### Completa la línea para obtener el valor de un input con id "email"

const email = document.______________("email").value;


### ¿Cuál de las siguientes opciones es correcta para asociar un evento submit a un formulario?

form.on("submit", handleSubmit)
form.addEvent("submit", handleSubmit)
form.addEventListener("submit", handleSubmit)
form.submitEvent(handleSubmit)

### Escribe la función para manejar el clic de un botón

function handleClick() {
    console.log("Botón presionado");
}

boton.__________________("click", handleClick);


### ¿Qué propiedad se usa para acceder al texto ingresado por el usuario en un input?

.innerHTML
.value
.textContent
.inputText

