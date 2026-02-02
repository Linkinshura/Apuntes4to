# Teoría de Matrices en C

## 1. ¿Qué es una matriz?

Una **matriz** en C es una estructura de datos que permite almacenar **valores del mismo tipo** en forma de **filas y columnas**.  
Puede pensarse como un **vector de vectores**.

Ejemplo visual de una matriz 2x3:

[ 1 2 3 ]

[ 4 5 6 ]



---

## 2. Características principales

- Todos los elementos son del **mismo tipo**
- Tiene **dos dimensiones** (filas y columnas)
- El tamaño es **fijo**
- Se accede mediante **dos índices**
- Los índices comienzan en **0**

---

## 3. Declaración de una matriz

Sintaxis general:

```c
tipo nombre[filas][columnas];

int matriz[3][4];

// Asignacion de valores

matriz[0][0] = 10;
matriz[0][1] = 20;

// Leer valores

printf("%d", matriz[0][0]);


// Inicializar

int m[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};

// Carga de datos

int m[2][3];

for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 3; j++) {
        scanf("%d", &m[i][j]);
    }
}

// Mostrar

for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 3; j++) {
        printf("%d ", m[i][j]);
    }
    printf("\n");
}

```
