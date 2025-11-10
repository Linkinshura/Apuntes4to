# Tipos de Datos en C

El lenguaje **C** utiliza diferentes tipos de datos para declarar variables y definir qué tipo de valores pueden almacenar.  
Estos tipos se dividen en **tipos primitivos**, **modificadores de tipo**, **tipos derivados** y **tipos definidos por el usuario**.

---

## 🧩 Tipos de Datos Primitivos

Los **tipos de datos primitivos** son los básicos que proporciona C de forma directa.

| Tipo | Descripción | Tamaño (aprox.) | Ejemplo |
|------|--------------|-----------------|----------|
| `int` | Números enteros (positivos o negativos) | 2 o 4 bytes | `int edad = 20;` |
| `float` | Números con decimales (poca precisión) | 4 bytes | `float altura = 1.75;` |
| `double` | Números con decimales (mayor precisión) | 8 bytes | `double pi = 3.141592;` |
| `char` | Un solo carácter o símbolo ASCII | 1 byte | `char letra = 'A';` |
| `void` | Sin valor o tipo (usado en funciones) | — | `void funcion();` |

---

## 🔧 Modificadores de Tipo

C permite modificar los tipos básicos para cambiar su **rango de valores** o **uso de memoria**.

| Modificador | Aplicable a | Descripción | Ejemplo |
|--------------|--------------|--------------|----------|
| `short` | `int` | Reduce el tamaño del entero | `short int x;` |
| `long` | `int`, `double` | Aumenta el tamaño del número | `long int n;` |
| `signed` | `int`, `char` | Permite valores negativos | `signed char c;` |
| `unsigned` | `int`, `char` | Solo valores positivos | `unsigned int edad;` |

> **Ejemplo:**  
> ```c
> unsigned int edad = 25;
> long double distancia = 123456.789;
> ```

---

## 🧱 Tipos de Datos Derivados

Son aquellos que se **construyen a partir de los tipos básicos**.

| Tipo Derivado | Descripción | Ejemplo |
|----------------|--------------|----------|
| **Array (arreglo)** | Conjunto de elementos del mismo tipo | `int numeros[5];` |
| **Pointer (puntero)** | Almacena la dirección de memoria de otra variable | `int *ptr;` |
| **Structure (struct)** | Agrupa varios tipos de datos distintos | `struct Persona { char nombre[20]; int edad; };` |
| **Union (union)** | Agrupa datos que comparten el mismo espacio de memoria | `union Dato { int entero; float decimal; };` |
| **Function** | Bloque de código reutilizable que retorna un tipo de dato | `int sumar(int a, int b);` |

---

## 🧾 Tipos Definidos por el Usuario

El programador puede **crear sus propios tipos** utilizando palabras clave.

| Palabra clave | Descripción | Ejemplo |
|----------------|--------------|----------|
| `typedef` | Asigna un alias a un tipo existente | `typedef unsigned int enteroPositivo;` |
| `enum` | Define un conjunto de constantes enteras con nombre | `enum Dias { Lunes, Martes, Miercoles };` |
| `struct` | Agrupa distintos tipos bajo un mismo nombre | `struct Alumno { char nombre[20]; int edad; };` |

---

## 📘 Ejemplo Completo

```c
#include <stdio.h>

typedef unsigned int uint;

struct Persona {
    char nombre[30];
    int edad;
    float altura;
};

int main() {
    struct Persona p1 = {"Ian", 18, 1.80};
    uint codigo = 1234;
    
    printf("Nombre: %s\n", p1.nombre);
    printf("Edad: %d\n", p1.edad);
    printf("Altura: %.2f\n", p1.altura);
    printf("Codigo: %u\n", codigo);

    return 0;
}
