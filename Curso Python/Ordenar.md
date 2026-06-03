# Ordenamiento en Python

La forma más sencilla de ordenar es con la función sorted(list), que toma una lista y devuelve una nueva lista con esos elementos ordenados. La lista original no se modifica.

```python
  a = [5, 1, 4, 3]
  print(sorted(a))  ## [1, 3, 4, 5]
  print(a)  ## [5, 1, 4, 3]
```

Lo más común es pasar una lista a la función sorted(), pero de hecho puede tomar como entrada cualquier tipo de colección iterable. El método list.sort() anterior es una alternativa que se detalla a continuación. La función sorted() parece más fácil de usar en comparación con sort(), por lo que recomiendo usar sorted().

La función sorted() se puede personalizar mediante argumentos opcionales. El argumento opcional reverse=True de sorted(), por ejemplo sorted(list, reverse=True), hace que se ordene a la inversa.

```python
  strs = ['aa', 'BB', 'zz', 'CC']
  print(sorted(strs))  ## ['BB', 'CC', 'aa', 'zz'] (case sensitive)
  print(sorted(strs, reverse=True))   ## ['zz', 'aa', 'CC', 'BB']
```

### Ordenamiento personalizado con key=

Para un ordenamiento personalizado más complejo, sorted() toma un parámetro opcional "key=" que especifica una función "key" (clave) que transforma cada elemento antes de la comparación. La función key toma 1 valor y devuelve 1 valor, y el valor "proxy" devuelto se utiliza para las comparaciones dentro del ordenamiento.

Por ejemplo, con una lista de cadenas, especificar key=len (la función integrada len()) ordena las cadenas por longitud, de menor a mayor. El ordenamiento llama a len() para cada cadena para obtener la lista de valores de longitud proxy y luego ordena con esos valores proxy.

```python
  strs = ['ccc', 'aaaa', 'd', 'bb']
  print(sorted(strs, key=len))  ## ['d', 'bb', 'ccc', 'aaaa']
```

![calling sorted with key=len](https://developers.google.com/static/edu/python/images/sorted-key.png)

Como otro ejemplo, especificar "str.lower" como la función key es una forma de forzar a que el ordenamiento trate las mayúsculas y las minúsculas por igual:

```python
  ## "key" argument specifying str.lower function to use for sorting
  print(sorted(strs, key=str.lower))  ## ['aa', 'BB', 'CC', 'zz']
```

También puedes pasar tu propia función MyFn como la función key, de esta manera:

```python
  ## Say we have a list of strings we want to sort by the last letter of the string.
  strs = ['xc', 'zb', 'yd' ,'wa']

  ## Write a little function that takes a string, and returns its last letter.
  ## This will be the key function (takes in 1 value, returns 1 value).
  def MyFn(s):
    return s[-1]

  ## Now pass key=MyFn to sorted() to sort by the last letter:
  print(sorted(strs, key=MyFn))  ## ['wa', 'zb', 'xc', 'yd']
```

Para ordenamientos más complejos, como ordenar por apellido y luego por nombre, puedes usar las funciones [itemgetter or attrgetter](https://docs.python.org/3/howto/sorting.html#operator-module-functions) como:

```python
  from operator import itemgetter

  # (first name, last name, score) tuples
  grade = [('Freddy', 'Frank', 3), ('Anil', 'Frank', 100), ('Anil', 'Wang', 24)]
  sorted(grade, key=itemgetter(1,0))
  # [('Anil', 'Frank', 100), ('Freddy', 'Frank', 3), ('Anil', 'Wang', 24)]

  sorted(grade, key=itemgetter(0,-1))
  #[('Anil', 'Wang', 24), ('Anil', 'Frank', 100), ('Freddy', 'Frank', 3)]
```

### Método sort()

Como alternativa a sorted(), el método sort() en una lista ordena esa lista en orden ascendente, por ejemplo, list.sort(). El método sort() modifica la lista subyacente y devuelve None, así que utilízalo de esta manera:

```python
  alist.sort()            ## correct
  alist = blist.sort()    ## Incorrect. sort() returns None
```

Lo anterior es un malentendido muy común con sort(): *no devuelve* la lista ordenada. El método sort() debe ser llamado sobre una lista; no funciona en ninguna colección enumerable (mientras que la función sorted() de arriba funciona en cualquiera). El método sort() es anterior a la función sorted(), por lo que es probable que lo veas en código más antiguo. El método sort() no necesita crear una lista nueva, por lo que puede ser un poco más rápido en el caso de que los elementos a ordenar ya estén en una lista.

## Tuplas

Una tupla es una agrupación de elementos de tamaño fijo, como una coordenada (x, y). Las tuplas son como las listas, excepto que son inmutables y no cambian de tamaño (las tuplas no son estrictamente inmutables ya que uno de los elementos contenidos podría ser mutable). Las tuplas desempeñan una especie de rol de "struct" en Python: una forma conveniente de pasar un pequeño conjunto lógico de valores de tamaño fijo. Una función que necesita devolver múltiples valores simplemente puede devolver una tupla de dichos valores. Por ejemplo, si quisiera tener una lista de coordenadas 3D, la representación natural en Python sería una lista de tuplas, donde cada tupla tiene tamaño 3 y contiene un grupo (x, y, z).

Para crear una tupla, simplemente enumera los valores entre paréntesis separados por comas. La tupla "vacía" es simplemente un par de paréntesis vacíos. El acceso a los elementos de una tupla es igual que en una lista: len(), [ ], for, in, etc., funcionan todos de la misma manera.

```python
  tuple = (1, 2, 'hi')
  print(len(tuple))  ## 3
  print(tuple[2])    ## hi
  tuple[2] = 'bye'  ## NO, tuples cannot be changed
  tuple = (1, 2, 'bye')  ## this works
```

Para crear una tupla de tamaño 1, el único elemento debe ir seguido de una coma.

```python
  tuple = ('hi',)   ## size-1 tuple
```

Es un caso curioso en la sintaxis, pero la coma es necesaria para distinguir la tupla del caso ordinario de poner una expresión entre paréntesis. En algunos casos puedes omitir los paréntesis y Python deducirá por las comas que te refieres a una tupla.

Asignar una tupla a una tupla de nombres de variables de idéntico tamaño asigna todos los valores correspondientes. Si las tuplas no son del mismo tamaño, genera un error. Esta característica también funciona para las listas.

```python
  (x, y, z) = (42, 13, "hike")
  print(z)  ## hike
  (err_string, err_code) = Foo()  ## Foo() returns a length-2 tuple
```

## Comprensión de listas (opcional)

La comprensión de listas (list comprehensions) es una característica más avanzada que resulta muy útil en algunos casos, pero no es necesaria para los ejercicios ni es algo que debas aprender al principio (es decir, puedes omitir esta sección). Una comprensión de listas es una forma compacta de escribir una expresión que se expande a una lista completa. Supongamos que tenemos una lista nums [1, 2, 3, 4], aquí está la comprensión de listas para calcular una lista de sus cuadrados [1, 4, 9, 16]:

```python
  nums = [1, 2, 3, 4]

  squares = [ n * n for n in nums ]   ## [1, 4, 9, 16]
```

La sintaxis es `[ *expr* for var in list ]` -- el `for var in list` parece un bucle for normal, pero sin los dos puntos (:). La *expr* a su izquierda se evalúa una vez para cada elemento para dar los valores de la nueva lista. Aquí hay un ejemplo con cadenas, donde cada cadena se convierte a mayúsculas con '!!!' añadido:

```python
  strs = ['hello', 'and', 'goodbye']

  shouting = [ s.upper() + '!!!' for s in strs ]
  ## ['HELLO!!!', 'AND!!!', 'GOODBYE!!!']
```

Puedes añadir una prueba if a la derecha del bucle for para filtrar el resultado. La prueba if se evalúa para cada elemento, incluyendo solo los elementos para los cuales la prueba es verdadera.

```python
  ## Select values <= 2
  nums = [2, 8, 1, 6]
  small = [ n for n in nums if n <= 2 ]  ## [2, 1]

  ## Select fruits containing 'a', change to upper case
  fruits = ['apple', 'cherry', 'banana', 'lemon']
  afruits = [ s.upper() for s in fruits if 'a' in s ]
  ## ['APPLE', 'BANANA']
```

