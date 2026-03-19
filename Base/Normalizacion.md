# **Normalizacion:**

La normalización de bases de datos es el proceso de organizar datos para reducir la redundancia y mejorar la integridad, aplicando reglas conocidas como Formas Normales (1FN, 2FN, 3FN). Divide tablas grandes en estructuras más pequeñas y relacionadas, eliminando dependencias innecesarias y asegurando que cada dato se almacene una sola vez. 

## **Principales Reglas de Normalización (Formas Normales)**

### **Primera Forma Normal (1FN):**

Elimina grupos repetidos y asegura que cada celda contenga un valor atómico (único), definiendo una clave primaria. No debe haber filas ni columnas duplicadas.

### **Segunda Forma Normal (2FN):**

Cumple con la 1FN y elimina dependencias parciales; todos los atributos no clave deben depender completamente de la clave primaria, no solo de una parte de ella.

### **Tercera Forma Normal (3FN):**

Cumple con la 2FN y elimina dependencias transitivas; los atributos que no son clave no deben depender de otros atributos no clave (dependencia funcional).
