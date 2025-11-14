# Funciones

Una Funcion es un bloque de codigo donde se ejecuta una tarea especifica de codigo y luego podes usarla para llamar la funcion y no tener que escribir todo el codigo devuelta ocupando mucho mas espacio de memoria que si lo hicieramos con una funcion


Ademas ayuda a que sea mas legible el codigo y mas facil de entender


## Ejemplo

```c
int suma(int a, int b){
    return a + b;
}

int main(){
    int a;
    int b;
    
    printf("Ingrese el valor del primer numero:");
    scanf("%d", &a);

    printf("\n Ingrese el valor del segundo numero:");
    scanf("%d", &b);

    suma(a, b);
}
```

Este caso es el de una suma de dos variables que uno antes de llamar la funcion le da el valor deseado a cada una y al pasarlos como parametros (entre los parentesis de la llamada) esta funcion lo lee y devuelve la suma de ambos valores sin importar su valor(mientras que sean INT)


# Funciones Recursivas

Una función recursiva es una función que se llama a sí misma para resolver un problema.

Se usa mucho cuando un problema puede dividirse en subproblemas más pequeños y similares al original.

## Ejemplo

```c
int fibonacci(int n) {
    if (n < 2) return n;
    return fibonacci(n-1) + fibonacci(n-2); 
}

int main() {
    printf("%d\n", fibonacci(6)); 
    return 0;
}
```

En este caso si n es 0 o 1 devuelve lo mismo caso diferente devuelve el valor del anterior mas el el anterior de ese mismo

En el caso puntual de ejemplo imprime 8