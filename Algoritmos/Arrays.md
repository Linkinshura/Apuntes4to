#  Arreglos (Arrays) en C

En C, un **array** (o **arreglo**) es una estructura que permite **almacenar múltiples valores del mismo tipo** bajo un mismo nombre de variable.  
Cada valor dentro del arreglo se llama **elemento** y se accede mediante un **índice numérico**.

---

##  Características Principales

- Todos los elementos son del **mismo tipo de dato** (`int`, `float`, `char`, etc.).  
- El índice **comienza desde 0**.  
- El tamaño del array debe **definirse al declararlo**.  
- Se puede acceder, modificar o recorrer usando bucles.

---

##  Declaración y Asignación

### Declaración
```c
tipo nombre[tamaño];


int numeros[5];      // Declaración de un array de 5 enteros
float notas[3];      // Array de 3 números decimales
char letras[4];      // Array de 4 caracteres


// Inicializacion

int edades[5] = {18, 20, 25, 30, 40};
char vocales[5] = {'a', 'e', 'i', 'o', 'u'};

// Tambien se puede ignorar el tamaño y no indicarlo

int numeros[] = {10, 20, 30, 40};

```
