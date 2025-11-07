# Matrices (Arreglos Bidimensionales)

Una **matriz** o **arreglo bidimensional** en C es una colección de **elementos del mismo tipo**, organizados en **filas y columnas**.  
Se puede pensar como una **tabla**.

---

## Declaración

```c
tipo nombre[filas][columnas];

int matriz[3][3];
float notas[2][4];
char letras[2][2];
```

## Inicializacion

```c
int matriz[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```

## Recorer(For)

```c
#include <stdio.h>

main() {
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
}
```
