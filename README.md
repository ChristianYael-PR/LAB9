# Trapping Rain Water

## Descripción

Este proyecto resuelve el problema clásico conocido como **"Trapping Rain Water"**. El objetivo es calcular cuánta agua puede quedar atrapada después de llover, dadas las alturas de una serie de columnas representadas como un arreglo de números enteros. Cada número indica la altura de una barra de ancho 1.

---

## Objetivo de la práctica

Implementar un algoritmo eficiente que determine el volumen de agua acumulada entre bloques de diferentes alturas, aplicando técnicas de programación con complejidad lineal.

---

## Fundamento teórico

La cantidad de agua que puede acumularse en una posición del arreglo depende de la altura máxima a la izquierda y a la derecha de esa posición. Si tomamos estas dos alturas y las comparamos con la altura actual, el agua que se puede retener está dada por:

agua_en_i = min(max_izquierda, max_derecha) - altura[i]

yaml

Esta cantidad debe ser mayor o igual a cero. Si no lo es, no se acumula agua en esa posición.

Ejemplo de entrada:

[0,1,0,2,1,0,1,3,2,1,2,1]

yaml

Resultado: `6` unidades de agua atrapadas.

---

## Algoritmo implementado

Se utilizó un algoritmo con la técnica de **dos punteros**, que avanza desde ambos extremos del arreglo, manteniendo actualizados los máximos a izquierda y derecha. En cada iteración se calcula el agua acumulada con base en estos máximos.

**Complejidad del algoritmo:**

- Tiempo: `O(n)`
- Espacio: `O(1)`

---

## Casos de prueba

| Entrada                     | Salida esperada |
|----------------------------|-----------------|
| [0,1,0,2,1,0,1,3,2,1,2,1]   | 6               |
| [4,2,0,3,2,5]               | 9               |
| [2,0,2]                     | 2               |
| [3,0,0,2,0,4]               | 10              |

---

## Conclusiones

El problema de *Trapping Rain Water* es una excelente aplicación de lógica algorítmica basada en análisis de máximos. Con una implementación eficiente se evita el uso innecesario de memoria adicional y se logra resolver el problema en tiempo lineal.

Este ejercicio refuerza el análisis de problemas espaciales y el uso de punteros como técnica poderosa pa
