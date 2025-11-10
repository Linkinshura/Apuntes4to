# Condicionales y Bucles en C

En C, las **estructuras de control** permiten modificar el flujo de ejecución de un programa.  
Estas estructuras incluyen **condicionales**, que toman decisiones, y **bucles (loops)**, que repiten instrucciones.



##  Condicionales

Las **estructuras condicionales** se utilizan para ejecutar un bloque de código **solo si** se cumple una condición.

###  `if`, `else if`, `else`

Evalúa una o varias condiciones lógicas.

```c
#include <stdio.h>

int main() {
    int edad = 18;

    if (edad < 18) {
        printf("Eres menor de edad.\n");
    } else if (edad == 18) {
        printf("Tienes 18 años.\n");
    } else {
        printf("Eres mayor de edad.\n");
    }

    return 0;
}
```

#  Bucles (Loops) en C

Los **bucles** en C permiten ejecutar un bloque de código varias veces mientras se cumpla una condición.  
Son fundamentales para automatizar tareas repetitivas y optimizar el código.

---

##  Tipos de Bucles

En C existen tres tipos principales de bucles:

| Tipo | Verificación de condición | Se ejecuta al menos una vez |
|------|----------------------------|------------------------------|
| `for` | Antes del bloque |  No necesariamente |
| `while` | Antes del bloque |  No necesariamente |
| `do...while` | Después del bloque |  Sí |

---

##  Bucle `for`

Se usa cuando **se conoce la cantidad exacta de repeticiones** que se deben realizar.  
Su estructura consta de tres partes: **inicialización**, **condición**, e **incremento/decremento**.

### Sintaxis

```c
for (inicialización; condición; incremento) {
    // código a repetir
}
