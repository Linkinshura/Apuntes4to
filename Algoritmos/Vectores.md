# Vectores (Arreglos)

Un **vector** o **arreglo** en C es una colección de **elementos del mismo tipo**, almacenados **en posiciones consecutivas de memoria**.


## Declaración

```c
tipo nombre[tamaño];
int numeros[5];
float notas[10];
char letras[3];
```

## Inicializacion

```c

intnumeros[3] = {10, 20, 30};
int numeros[] = {10, 20, 30, 40};
```

## Recorrer(con For)
```c
#include <stdio.h>

main() {
    int numeros[5] = {2, 4, 6, 8, 10};

    for (int i = 0; i < 5; i++) {
        printf("Elemento %d: %d\n", i, numeros[i]);
    }
}
```
