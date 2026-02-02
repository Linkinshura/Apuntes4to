# Teoría del `if` en C

## 1. ¿Qué es el `if` en C?

El `if` **NO es un bucle**.  
Es una **estructura condicional** que permite al programa **tomar decisiones**.

Sirve para indicar:
> “Si se cumple una condición, ejecutá este código”.

---

## 2. Idea básica del `if`

Ejemplo de la vida real:
- Si llueve → llevo paraguas
- Si hace frío → uso abrigo

En programación funciona igual.

---

## 3. Sintaxis básica del `if`

```c
if (condición) {
    instrucciones;
}
