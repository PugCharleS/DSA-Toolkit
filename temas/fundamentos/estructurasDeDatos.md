## Estructuras de Datos Comunes

### Arreglos (Arrays)

Un **arreglo** es una colección de elementos identificados por índices o claves. En la mayoría de los lenguajes, los arreglos tienen un tamaño fijo y cada elemento tiene un índice específico, desde `0` hasta `n-1` (donde `n` es el número de elementos).

**Características:**
- Acceso directo a través del índice.
- Tamaño fijo en muchos lenguajes (aunque existen arreglos dinámicos como en JavaScript o ArrayList en Java).

### Listas Enlazadas (Linked Lists)

Una **lista enlazada** es una colección de nodos que juntos representan una secuencia. Cada nodo contiene un dato y una referencia (enlace) al siguiente nodo en la secuencia.

**Tipos:**
- **Lista enlazada simple:** Cada nodo apunta al siguiente nodo.
- **Lista doblemente enlazada:** Cada nodo apunta tanto al siguiente nodo como al anterior.
- **Lista circular:** El último nodo apunta de nuevo al primero.

### Pilas (Stacks)

Una **pila** es una colección de elementos con el principio de "último en entrar, primero en salir" (LIFO). Las operaciones principales son `push` (agregar) y `pop` (retirar).

**Características:**
- Se utiliza para controlar el flujo de ejecución, almacenar historiales, etc.
- Puede implementarse con arreglos o listas enlazadas.

### Colas (Queues)

Una **cola** es una colección de elementos con el principio de "primero en entrar, primero en salir" (FIFO). Las operaciones principales son `enqueue` (agregar) y `dequeue` (retirar).

**Características:**
- Se utiliza en programación para controlar tareas, eventos, etc.
- Puede implementarse con arreglos o listas enlazadas.

### Árboles (Trees)

Un **árbol** es una estructura jerárquica que consta de nodos conectados por bordes. Un nodo es la raíz, y los demás nodos son particionados en subconjuntos que son subárboles.

**Tipos comunes:**
- **Árbol binario:** Cada nodo tiene hasta dos hijos.
- **Árbol binario de búsqueda (BST):** Un árbol binario donde cada nodo tiene un valor. Los nodos a la izquierda son menores que el nodo actual y los nodos a la derecha son mayores.

### Grafos (Graphs)

Un **grafo** es un conjunto de nodos conectados por bordes. Puede ser dirigido (las conexiones tienen una dirección) o no dirigido.

**Características:**
- Se utiliza para representar redes, rutas, relaciones, etc.
- Puede ser ponderado (cada borde tiene un peso) o no ponderado.

---

Estas son descripciones básicas de cada estructura de datos. Cada una tiene sus propias aplicaciones, ventajas y desventajas. Si deseas más detalles, ejemplos de código o cualquier otro aspecto relacionado con alguna estructura en particular, no dudes en preguntar.
