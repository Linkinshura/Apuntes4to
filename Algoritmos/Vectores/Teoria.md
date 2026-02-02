# Teoría de Vectores (Arrays) en C

## 1. ¿Qué es un vector en C?

Un **vector** (o *array*) es una estructura de datos que permite **almacenar varios valores del mismo tipo** en una sola variable.  
Sirve para organizar información y evitar declarar muchas variables individuales.

---

## 2. Características principales

- Todos los elementos son del **mismo tipo**
- Tienen un **tamaño fijo**
- Cada elemento se identifica mediante un **índice**
- Los índices comienzan en **0**
- Los datos se almacenan en memoria **de forma contigua**

---

## 3. Declaración de un vector

Sintaxis general:

```c
tipo nombre[tamaño];
int numeros[5];
```
Leer valores:

```c
printf("%d", numeros[0]);
```

Para cargarlo se usa generalmente un For:

```c
int v[4];

for (int i = 0; i < 4; i++) {
    scanf("%d", &v[i]);
}

// Para mostrarlo:

for (int i = 0; i < 4; i++) {
    printf("%d\n", v[i]);
}

```
