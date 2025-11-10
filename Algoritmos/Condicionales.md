# Condicionales y Bucles en C

En C, las **estructuras de control** permiten modificar el flujo de ejecución de un programa.  
Estas estructuras incluyen **condicionales**, que toman decisiones, y **bucles (loops)**, que repiten instrucciones.

---

## ⚙️ Condicionales

Las **estructuras condicionales** se utilizan para ejecutar un bloque de código **solo si** se cumple una condición.

### 🧩 `if`, `else if`, `else`

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
