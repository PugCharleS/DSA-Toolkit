## Notación Big O

La **Notación Big O** se utiliza para describir el rendimiento o complejidad de un algoritmo, específicamente en términos de tiempo de ejecución y cómo este crece relativo al tamaño de la entrada.

### Definición

- **O(f(n))**: Describe una función que crece en el "orden de f(n)". Aquí, "n" es el tamaño de la entrada y "f(n)" es una función que representa cómo crece el tiempo de ejecución (o espacio) en relación con "n".

### Ejemplos Comunes

1. **O(1)** - Tiempo Constante:

  - Independiente del tamaño de la entrada.
  - Ejemplo: Acceder a un elemento en un arreglo por su índice.

   ```javascript
  function getFirstElement(arr) {
      return arr[0];
  }

  const numbers = [1, 2, 3, 4, 5];
  console.log(getFirstElement(numbers));  // Output: 1
  ```

2. **O(log n)** - Tiempo Logarítmico:

  - Se reduce a la mitad (o un factor constante) en cada paso.
  - Ejemplo: Búsqueda binaria.

  ```javascript
  function binarySearch(arr, x) {
  let l = 0, r = arr.length - 1;
  while (l <= r) {
      let m = Math.floor((l + r) / 2);
      if (arr[m] === x) return m;
      if (arr[m] < x) l = m + 1;
      else r = m - 1;
  }
  return -1;
  }

  const sortedNumbers = [1, 2, 3, 4, 5];
  console.log(binarySearch(sortedNumbers, 3));  // Output: 2
  ```

3. **O(n)** - Tiempo Lineal:

  - Crece linealmente con el tamaño de la entrada.
  - Ejemplo: Búsqueda lineal.

  ```javascript
  function linearSearch(arr, x) {
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] === x) return i;
    }
    return -1;
  }

  const numbers = [1, 2, 3, 4, 5];
  console.log(linearSearch(numbers, 3));  // Output: 2
  ```

4. **O(n log n)**:

   - Más eficiente que cuadrático, pero menos que lineal y logarítmico.
   - Ejemplo: Algoritmos de ordenamiento como Merge Sort o Quick Sort.

  ```javascript
   function mergeSort(arr) {
    if (arr.length <= 1) return arr;
    const middle = Math.floor(arr.length / 2);
    const left = arr.slice(0, middle);
    const right = arr.slice(middle);
    return merge(mergeSort(left), mergeSort(right));
  }

  function merge(left, right) {
      let result = [], leftIndex = 0, rightIndex = 0;
      while (leftIndex < left.length && rightIndex < right.length) {
          if (left[leftIndex] < right[rightIndex]) {
              result.push(left[leftIndex]);
              leftIndex++;
          } else {
              result.push(right[rightIndex]);
              rightIndex++;
          }
      }
      return result.concat(left.slice(leftIndex)).concat(right.slice(rightIndex));
  }

  const numbers = [5, 4, 3, 2, 1];
  console.log(mergeSort(numbers));  // Output: [1, 2, 3, 4, 5]
  ```

5. **O(n^2), O(n^3), ...** - Tiempo Polinómico:

  - Los algoritmos con esta complejidad suelen tener bucles anidados.
  - Ejemplo: Algoritmos de ordenamiento como Bubble Sort (para O(n^2)).

  ```javascript
  function bubbleSort(arr) {
    for (let i = 0; i < arr.length; i++) {
        for (let j = 0; j < arr.length - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
            }
        }
    }
    return arr;
  } 

  const numbers = [5, 4, 3, 2, 1];
  console.log(bubbleSort(numbers));  // Output: [1, 2, 3, 4, 5]
  ```

6. **O(2^n)** - Tiempo Exponencial:
  - El tiempo de ejecución dobla con cada adición a la entrada.
  - Ejemplo: Problema del viajante (enfoque naive).

  ```javascript
  function fibonacci(n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
  }

  console.log(fibonacci(5));  // Output: 5
  ```

### Importancia

Entender la Notación Big O es crucial para:

- Elegir el algoritmo más eficiente para un problema dado.
- Optimizar código existente.
- Evaluar trade-offs entre tiempo y espacio.

### Consideraciones

- La Notación Big O se centra en el peor caso, aunque también existen notaciones para el mejor caso (Omega Ω) y el caso promedio (Theta Θ).
- Se ignoran factores constantes y términos no dominantes para simplificar el análisis.

---
