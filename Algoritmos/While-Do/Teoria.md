# Teoría de los bucles `while` y `do while` en C

## 1. ¿Qué es un bucle?

Un **bucle** es una estructura que permite **repetir un bloque de código** mientras se cumpla una condición.

En C, los bucles más usados son:
- `for`
- `while`
- `do while`

---

## 2. Bucle `while`

### ¿Qué es el `while`?

El bucle `while` repite un conjunto de instrucciones **mientras una condición sea verdadera**.  
La condición se evalúa **antes** de ejecutar el cuerpo del bucle.

---

### Sintaxis del `while`

```c
while (condición) {
    instrucciones;
}
```

# Teoría del bucle `do while` en C

## 1. ¿Qué es el `do while`?

El `do while` es una **estructura repetitiva** (bucle) que permite ejecutar un bloque de código **al menos una vez**, independientemente de si la condición es verdadera o falsa.

La condición se evalúa **al final** del bucle.

---

## 2. Diferencia principal con `while`

- En `while`, la condición se evalúa **antes** de ejecutar el código.
- En `do while`, la condición se evalúa **después** de ejecutar el código.

Por eso, el `do while` **siempre se ejecuta al menos una vez**.

---

## 3. Sintaxis del `do while`

```c
do {
    instrucciones;
} while (condición);
```
