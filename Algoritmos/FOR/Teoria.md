# Teoría del bucle `for` en C

## 1. ¿Qué es el `for` en C?

El `for` es un **bucle** o **estructura repetitiva**.  
Se utiliza cuando queremos **repetir un bloque de código una cantidad conocida de veces**.

👉 A diferencia del `if`, el `for` **no decide**, sino que **repite**.

---

## 2. Idea básica del `for`

En la vida real:
- Contar del 1 al 10
- Repetir un ejercicio 5 veces
- Mostrar los números del 0 al 100

En programación, el `for` sirve exactamente para eso.

---

## 3. Sintaxis básica del `for`

```c
for (inicialización; condición; actualización) {
    instrucciones;
}
