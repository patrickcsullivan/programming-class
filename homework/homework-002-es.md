# Tarea 2

Cada problema en esa asignación, excepto el problema 5, describa una función para que implementas. Defina cada función nueva en tu archivo `main.hs`. Asegúrate de que icluyes una declaración de tipo en la definición de cada función.

Debería probar tu función en `ghci` con varias entradas para asegurarte de que funciona. Muchos de los problemas incluyen ejemplos que puedes usar para probar tus funciones. También debería probar tus funciones con entrades adiconales.

### Problema 0

Escribe un función llamada `num_sign` que toma un `Int`, `x`. La función debería devolver la cadena de texto `"POSITIVE"` si `x` es positivo, `"NEGATIVE"` si `x` es negativo, y `"ZERO"` si `x` es cero.

### Problema 1

Escribe un función llamada `num_parity` que toma un `Int`, `x`. La función debería devolver la cadena de texto `"ODD"` si `x` es un entero impar y `"EVEN"` si `x` es un entero par.

### Problema 2

Escribe un función llamada `describe_list` que toma una lista, `xs`. La función debería devolver la cadena de texto `"EMPTY"` si lista está vacía, `"SINGLETON"` si la lista contiene un solo elemento, y `"LONGER"` si la lista contiene mas que uno elemento.

### Problema 3

Escribe un función llamada `middle_element` que toma una lista de enteros llamada `xs`. La función debería devolver el elemento intermedio de la lista.

Si la lista contiene 5 elementos, La función debería devolver el elemento en índice 2 (el tercer elemento). Si la lista contiene 4 elementos, La función debería devolver el elemento en índice 1 (el segundo elemento).

**Ejemplos:**

- `middle_element [1, 2, 3, 4, 5]` debería devolver `3`.
- `middle_element [1, 2, 3, 4]` debería devolver `2`.

### Problema 4

¿Qué pasa si llamamos a la función anterior, pasando una lista vacía, así: `middle_element []`. ¡Pruébalo en `ghci`!

Debería recibir un mensaje que diga `*Exception`. En Haskell una "excepción" es un error que interrumpe la ejecución de un programa. Hará que su programa se bloquee y deje de ejecutarse. Idealmente queremos escribir nuestros programs de tal manera que una vez que el pgrama se incia, las excepiones nunca pueden ocurrir.

Solocione esto escribiendo una nueva función llamada `middle_element_or_zero`. Al igual que la función de Problema 3, esta función debería tomar una lista de enteros llamda `xs`, y debería devolver el elemento intermedio de la lista. Pero si `xs` es una lista vacía, la función debería devolver `0`.

**Ejemplos:**

- `middle_element_or_zero [1, 2, 3, 4, 5]` debería devolver `3`.
- `middle_element_or_zero [1, 2, 3, 4]` debería devolver `2`.
- `middle_element_or_zero []` debería devolver `0`.

### Problem 5

Podemos levantar una excepción y bloquear nuestro programa llamando a la función `middle_element` y pasando el valor `[]`. ¿Hay alguna manera de levantar una excepión llamando a la función `middle_element_or_zero`?

La respuesta es "no", ¡y esto es magnifico! Para cada lista posible de enteros que podríamos pasar a `middle_element_or_zero` nunca levantaremos una excepción. `middle_element_or_zero` se llama una **función total** porque funciona para todos las entradas posibles. `middle_element` se llama una **función parcial** porque hay entradas posibles que hacen que se bloquee. 

Idealmente, queremos implementar nuestras funciones de tal manera que sean funciones totales en lugar de funciones parciales, porque las funciones totales no generarán excepciones ni bloquearán nuestros programas.
 
Identifice dos funciones de [referencias de capítulo 2](../references/chapter-02.md) que son funciones parciales. Escriba un valor para cada función que hará que la función genere una excepción cuando pasemos ese valor a la función. (Por ejemplo, `middle_element` es una función y genera una excepción quando pasamos el valor `[]`.)