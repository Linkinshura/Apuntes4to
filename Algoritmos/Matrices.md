#  Matrices Bidimensionales en C

Una **matriz bidimensional** (también llamada **array 2D**) es una estructura que permite almacenar datos en **filas y columnas**, similar a una tabla.  
Se utiliza para representar información en forma de cuadrícula, como notas de alumnos, tableros, o datos numéricos.

---

## 🧩 Concepto Básico

Una matriz 2D se puede ver como un **array de arrays**:

matriz[fila][columna]


Por ejemplo, una matriz de 2 filas y 3 columnas tiene esta forma:

|   | Col 0 | Col 1 | Col 2 |
|---|--------|--------|--------|
| **Fila 0** | [0][0] | [0][1] | [0][2] |
| **Fila 1** | [1][0] | [1][1] | [1][2] |

---

##  Declaración de una Matriz

### Sintaxis General

```c
tipo nombre[filas][columnas];

// Ejemplo

int matriz[2][3];

// Inicializacion

int matriz[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};

// Recorrer

#include <stdio.h>

int main() {
    int matriz[2][3] = {
        {1, 2, 3},
        {4, 5, 6}
    };

    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", matriz[i][j]);
        }
        printf("\n");
    }

    return 0;
}

```
