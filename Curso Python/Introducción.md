# Introducción a Python

## Introducción al lenguaje

Python es un lenguaje dinámico e interpretado (compilado a bytecode). No hay declaraciones de tipo de variables, parámetros, funciones o métodos en el código fuente. Esto hace que el código sea corto y flexible, y se pierde la comprobación de tipos en tiempo de compilación del código fuente. Python realiza un seguimiento de los tipos de todos los valores en tiempo de ejecución y marca el código que no tiene sentido a medida que se ejecuta.

Una excelente manera de ver cómo funciona el código Python es ejecutar el intérprete de Python y escribir código directamente en él. Si alguna vez tienes una pregunta como: "¿Qué pasa si añado un `int` a una `list`?", escribirlo en el intérprete de Python es una forma rápida y probablemente la mejor de ver qué sucede. (¡Mira a continuación para ver qué sucede realmente!)

```python
$ python3        ## Run the Python interpreter
Python 3.X.X (XXX, XXX XX XXXX, XX:XX:XX) [XXX] on XXX
Type "help", "copyright", "credits" or "license" for more information.
>>> a = 6       ## set a variable in this interpreter session
>>> a           ## entering an expression prints its value
6
>>> a + 2
8
>>> a = 'hi'    ## 'a' can hold a string just as well
>>> a
'hi'
>>> len(a)      ## call the len() function on a string
2
>>> a + len(a)  ## try something that doesn't work
Traceback (most recent call last):
  File "", line 1, in 
TypeError: can only concatenate str (not "int") to str
>>> a + str(len(a))  ## probably what you really wanted
'hi2'
>>> foo         ## try something else that doesn't work
Traceback (most recent call last):
  File "", line 1, in 
NameError: name 'foo' is not defined
>>> ^D          ## type CTRL-d to exit (CTRL-z in Windows/DOS terminal)
```

Las dos líneas que Python imprime después de escribir python y antes del indicador \>\>\> te informan sobre la versión de Python que estás utilizando y dónde se compiló. Siempre que lo primero que se imprima sea "Python 3.", estos ejemplos deberían funcionar en tu caso.

Como puedes ver arriba, es fácil experimentar con variables y operadores. Además, el intérprete lanza o "eleva" (raises) en la jerga de Python, un error de tiempo de ejecución si el código intenta leer una variable a la que no se le ha asignado un valor. Al igual que C++ y Java, Python distingue entre mayúsculas y minúsculas, por lo que "a" y "A" son variables diferentes. El final de una línea marca el final de una sentencia, por lo que, a diferencia de C++ y Java, Python no requiere un punto y coma al final de cada sentencia. Los comentarios comienzan con un '#' y se extienden hasta el final de la línea.

## Código fuente de Python

Los archivos de código fuente de Python utilizan la extensión ".py" y se denominan "módulos". Con un módulo de Python `hello.py`, la forma más fácil de ejecutarlo es con el comando de shell "python hello.py Alice", que llama al intérprete de Python para ejecutar el código en `hello.py`, pasándole el argumento de línea de comandos "Alice".
Consulta la [página de documentación oficial](http://docs.python.org/using/cmdline) sobre todas las diferentes opciones que tienes al ejecutar Python desde la línea de comandos.

Aquí tienes un programa `hello.py` muy simple (observa que los bloques de código se delimitan estrictamente utilizando la sangría en lugar de llaves, ¡más sobre esto más adelante!):

```python
#!/usr/bin/python3

# import modules used here -- sys is a very standard one
import sys

# Gather our code in a main() function
def main():
    print('Hello there', sys.argv[1])
    # Command line args are in sys.argv[1], sys.argv[2] ...
    # sys.argv[0] is the script name itself and can be ignored

# Standard boilerplate to call the main() function to begin
# the program.
if __name__ == '__main__':
    main()
```

Ejecutar este programa desde la línea de comandos se ve así:

```
$ python3 hello.py Guido
Hello there Guido
$ ./hello.py Alice  ## without needing 'python3' first (Unix)
Hello there Alice
```

## Importaciones, argumentos de línea de comandos y `len()`

Las sentencias más externas en un archivo de Python, o "módulo", realizan su configuración única: esas sentencias se ejecutan de arriba a abajo la primera vez que el módulo se importa en algún lugar, configurando sus variables y funciones. Un módulo de Python se puede ejecutar directamente (como se vio arriba `python3 hello.py Bob`) o puede ser importado y utilizado por algún otro módulo. Cuando un archivo de Python se ejecuta directamente, la variable especial "__name__" se establece en "__main__". Por lo tanto, es común tener la plantilla `if __name__ ==...` mostrada arriba para llamar a una función main() cuando el módulo se ejecuta directamente, pero no cuando el módulo es importado por algún otro módulo.

En un programa Python estándar, la lista `sys.argv` contiene los argumentos de la línea de comandos de la manera habitual, siendo sys.argv\[0\] el programa en sí, sys.argv\[1\] el primer argumento, y así sucesivamente. Si deseas saber la cantidad de argumentos, simplemente puedes solicitar este valor a Python con `len(sys.argv)`, al igual que hicimos en el código del intérprete interactivo de arriba al solicitar la longitud de una cadena. En general, `len()` puede decirte la longitud de una cadena, el número de elementos en listas y tuplas (otra estructura de datos similar a un array) y el número de pares clave-valor en un diccionario.

## Funciones definidas por el usuario

Las funciones en Python se definen de la siguiente manera:

```python
# Defines a "repeat" function that takes 2 arguments.
def repeat(s, exclaim):
    """
    Returns the string 's' repeated 3 times.
    If exclaim is true, add exclamation marks.
    """

    result = s + s + s # can also use "s * 3" which is faster (Why?)
    if exclaim:
        result = result + '!!!'
    return result
```

Observa también cómo las líneas que componen la función o la sentencia if se agrupan teniendo todas el mismo nivel de sangría. También presentamos 2 formas diferentes de repetir cadenas: utilizando el operador + que es más intuitivo para el usuario, o también con \* que funciona porque es el operador de "repetición" de Python, lo que significa que `'-' * 10` devuelve `'---'`, una forma excelente de crear una "línea" en pantalla. En el comentario del código, sugerimos que \* funciona más rápido que +, debido a que \* calcula el tamaño del objeto resultante una sola vez, mientras que con +, esa operación se realiza cada vez que se llama a +. Tanto + como \* se denominan operadores "sobrecargados" porque significan cosas diferentes para números frente a cadenas (y otros tipos de datos).

La palabra clave `def` define la función con sus parámetros entre paréntesis y su código sangrado. La primera línea de una función puede ser una cadena de documentación ("docstring") que describe lo que hace la función. La docstring puede ser una sola línea o una descripción de varias líneas como en el ejemplo de arriba. (¡Sí, esas son "comillas triples", una característica única de Python!) Variables definidas en la función son locales de esa función, por lo que la variable "result" en la función anterior es independiente de una variable "result" en otra función. La sentencia `return` puede tomar un argumento, en cuyo caso ese es el valor devuelto al llamador.

Aquí tienes el código que llama a la función repeat() anterior, imprimiendo lo que devuelve:

```python
def main():
    print(repeat('Yay', False))      ## YayYayYay
    print(repeat('Woo Hoo', True))   ## Woo HooWoo HooWoo Hoo!!!
```

En tiempo de ejecución, las funciones deben definirse mediante la ejecución de un "def" antes de ser llamadas. Es habitual definir la función main() hacia la parte inferior del archivo con las funciones a las que llama situadas encima de ella.

## Sangría (Indentation)

Una característica inusual de Python es que la sangría por espacios en blanco de un fragmento de código afecta su significado. Un bloque lógico de sentencias, como las que componen una función, deben tener todas la misma sangría, desplazada respecto a la sangría de su función contenedora o del "if", etc. Si una de las líneas de un grupo tiene una sangría diferente, se marcará como un error de sintaxis.

El uso de espacios en blanco en Python parece un poco extraño al principio, pero es lógico y te acostumbrarás muy rápido. Evita usar tabuladores (TABs) ya que complican enormemente el esquema de sangría (por no mencionar que los tabuladores pueden significar cosas diferentes en diferentes plataformas). Configura tu editor para insertar espacios en lugar de tabuladores al escribir código Python.

Una pregunta común de los principiantes es: "¿Cuántos espacios debo sangrar?". De acuerdo con [la guía de estilo oficial de Python (PEP 8)](http://python.org/dev/peps/pep-0008/#indentation), debes sangrar con 4 espacios. (Como dato curioso: ¡la guía de estilo interna de Google dicta sangrar con 2 espacios!)

## Código verificado en tiempo de ejecución

Python realiza muy pocas comprobaciones en tiempo de compilación, posponiendo casi todas las comprobaciones de tipo, nombres, etc. de cada línea hasta que dicha línea se ejecute. Supongamos que la función main() anterior llama a repeat() así:

```python
def main():
    if name == 'Guido':
        print(repeeeet(name) + '!!!')
    else:
        print(repeat(name))
```

La sentencia if contiene un error evidente, donde la función repeat() se escribió accidentalmente como repeeeet(). Lo curioso en Python... este código se compila y se ejecuta bien mientras que name en tiempo de ejecución no sea 'Guido'. Solo cuando una ejecución intente realmente ejecutar repeeeet(), se percatará de que no existe tal función y lanzará un error. También hay un segundo error en este fragmento: no se le asignó un valor a name antes de compararlo con 'Guido'. Python lanzará un 'NameError' si intentas evaluar una variable no asignada. Estos son algunos ejemplos que demuestran que, al ejecutar por primera vez un programa en Python, algunos de los primeros errores que verás serán simples erratas o variables no inicializadas como estas. Este es un aspecto en el que los lenguajes con un sistema de tipos más explícito, como Java, tienen ventaja... pueden detectar tales errores en tiempo de compilación (pero, por supuesto, tienes que mantener toda esa información de tipos... es una cuestión de equilibrio).

Python 3 introdujo las [indicaciones de tipo (type hints)](https://docs.python.org/3/library/typing.html).
Las indicaciones de tipo te permiten señalar cuál es el tipo de cada argumento en una función, así como cuál es el tipo del objeto devuelto por la función.
Por ejemplo, en la función anotada ` def is_positive(n: int) -> bool:`, el argumento `n` es un `int` y el valor de retorno es un `bool`.
Analizaremos lo que significan estos tipos más adelante. Sin embargo, las indicaciones de tipo son totalmente opcionales.
Verás que cada vez más código adopta indicaciones de tipo porque, si las usas, algunos editores como cider-v y VS.code pueden realizar comprobaciones para verificar que tus funciones se llamen con los tipos de argumento correctos. Incluso pueden sugerir y validar argumentos a medida que editas el código.
Este tutorial no cubrirá las indicaciones de tipo, pero queremos asegurarnos de que las conozcas en caso de que oigas hablar de ellas o las veas en la práctica.

## Nombres de variables

Dado que las variables de Python no tienen ningún tipo especificado en el código fuente, resulta de gran ayuda asignar nombres significativos a tus variables para recordar qué está sucediendo. Por lo tanto, usa "name" si es un solo nombre, "names" si es una lista de nombres y "tuples" si es una lista de tuplas. Muchos errores básicos de Python se deben a que se olvida qué tipo de valor hay en cada variable, así que usa tus nombres de variables (en realidad todo lo que tienes) para ayudar a mantener las cosas claras.

En cuanto al nombramiento real, algunos lenguajes prefieren underscored_parts (partes_separadas_por_guion_bajo) para los nombres de variables compuestos por "más de una palabra", pero otros lenguajes prefieren camelCasing. En general, Python [prefiere](http://python.org/dev/peps/pep-0008/#function-names) el método del guion bajo, pero aconseja a los desarrolladores recurrir a camelCasing si se integran en código Python existente que ya utiliza ese estilo. La legibilidad cuenta. Lee más en [la sección sobre convenciones de nomenclatura en PEP 8](https://www.python.org/dev/peps/pep-0008/#naming-conventions).

Como puedes suponer, las palabras clave como 'if' y 'while' no se pueden usar como nombres de variables; obtendrás un error de sintaxis si lo haces. Sin embargo, ten cuidado de no usar elementos integrados (built-ins) como nombres de variables. Por ejemplo, aunque 'str', 'list' y 'print' puedan parecer buenos nombres, estarías sobrescribiendo esas variables del sistema. Los elementos integrados no son palabras clave y, por lo tanto, son susceptibles de un uso involuntario por parte de los desarrolladores principiantes de Python.

## Más sobre módulos y sus espacios de nombres (namespaces)

Supongamos que tienes un módulo "binky.py" que contiene un "def foo()". El nombre totalmente calificado de esa función foo es "binky.foo". De esta manera, varios módulos de Python pueden nombrar sus funciones y variables como quieran, y los nombres de las variables no entrarán en conflicto: module1.foo es diferente de module2.foo. En el vocabulario de Python, diríamos que binky, module1 y module2 tienen cada uno sus propios "espacios de nombres" (namespaces), que, como puedes suponer, son asociaciones de nombres de variables con objetos.

Por ejemplo, tenemos el módulo estándar "sys" que contiene algunas facilidades estándar del sistema, como la lista argv y la función exit(). Con la sentencia "import sys" puedes acceder a las definiciones en el módulo sys y hacerlas disponibles por su nombre totalmente calificado, por ejemplo, sys.exit(). (¡Sí, 'sys' también tiene un espacio de nombres!)

```python
  import sys

  # Now can refer to sys.xxx facilities
  sys.exit(0)
```

Existe otra forma de importación que se ve así: "from sys import argv, exit". Eso hace que argv y exit() estén disponibles por sus nombres cortos; sin embargo, recomendamos la forma original con los nombres totalmente calificados porque es mucho más fácil determinar de dónde proviene una función o atributo.

Hay muchos módulos y paquetes que vienen incluidos con una instalación estándar del intérprete de Python, por lo que no tienes que hacer nada adicional para usarlos. Estos se conocen colectivamente como la "Biblioteca estándar de Python" (Python Standard Library). Los módulos/paquetes comúnmente utilizados incluyen:

- sys — acceso a exit(), argv, stdin, stdout, ...
- re — expresiones regulares
- os — interfaz del sistema operativo, sistema de archivos

Puedes encontrar la documentación de todos los módulos y paquetes de la Biblioteca Estándar en <http://docs.python.org/library>.

## Ayuda en línea, `help()` y `dir()`

Hay una variedad de formas de obtener ayuda para Python.

- Realiza una búsqueda en Google, comenzando con la palabra "python", como "python list" o "python string lowercase". El primer resultado suele ser la respuesta. Esta técnica parece funcionar mejor para Python que para otros lenguajes por alguna razón.
- El sitio oficial de documentación de Python — [docs.python.org](http://docs.python.org) — tiene documentación de alta calidad. No obstante, a menudo encuentro que una búsqueda en Google de un par de palabras es más rápida.
- ¡También existe una [lista de correo oficial de Tutor](http://mail.python.org/mailman/listinfo/tutor) diseñada específicamente para aquellos que son nuevos en Python y/o en la programación!
- Se pueden encontrar muchas preguntas (y respuestas) en [StackOverflow](http://stackoverflow.com/questions/tagged/python) and [Quora](http://quora.com/Python-programming-language).
- Utiliza las funciones help() y dir() (ver más abajo).

Dentro del intérprete de Python, la función help() extrae cadenas de documentación para varios módulos, funciones y métodos. Estas cadenas de documentación son similares al javadoc de Java. La función dir() te indica cuáles son los atributos de un objeto. A continuación, se muestran algunas formas de llamar a help() and dir() desde el intérprete:

- `help(len)` — cadena de ayuda para la función incorporada `len()`; ten en cuenta que es "len" y no "len()", lo cual sería una **llamada** a la función y no es lo que queremos
- `help(sys)` — cadena de ayuda para el módulo `sys` (primero debes hacer un `import sys`)
- `dir(sys)` — `dir()` es como `help()` pero solo ofrece una lista rápida de sus símbolos definidos o "atributos"
- `help(sys.exit)` — cadena de ayuda para la función `exit()` en el módulo `sys`
- `help('xyz'.split)` — cadena de ayuda para el método `split()` para objetos de tipo cadena (string). Puedes llamar a `help()` con ese objeto en sí o con un **ejemplo** de ese objeto, además de su atributo. Por ejemplo, llamar a `help('xyz'.split)` es lo mismo que llamar a `help(str.split)`.
- `help(list)` — cadena de ayuda para objetos `list`
- `dir(list)` — muestra los atributos del objeto `list`, incluidos sus métodos
- `help(list.append)` — cadena de ayuda para el método `append()` para objetos `list`