{
  "examen_metadatos": {
    "num_preguntas": 10,
    "fuente": "Diccionarios_Archivos.md",
    "asignatura": "PYTHON"
  },
  "preguntas": [
    {
      "id": 1,
      "tema": "Diccionarios",
      "capitulo": "Tabla Hash de Diccionarios (Dict)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar",
      "enunciado": "Según el texto proporcionado, ¿cuál es el resultado de buscar directamente una clave que no existe en un diccionario de Python sin usar métodos específicos?",
      "opciones": {
        "a": "El sistema devuelve el valor por defecto None.",
        "b": "El intérprete lanza una excepción de tipo KeyError.",
        "c": "El programa genera un error de tipo ReferenceError."
      },
      "respuesta_correcta": "b",
      "justificacion": "Buscar un valor que no está en el diccionario lanza un KeyError",
      "distractores": {
        "a": "Confunde el comportamiento directo con el comportamiento del método .get() que sí devuelve None.",
        "c": "Utiliza terminología errónea de otros lenguajes de programación en lugar del error explícito mencionado en el texto."
      }
    },
    {
      "id": 2,
      "tema": "Archivos",
      "capitulo": "Archivos",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar",
      "enunciado": "¿Qué método específico del manejador de archivos lee el archivo completo en la memoria devolviendo su contenido como una lista de sus líneas?",
      "opciones": {
        "a": "El método f.read()",
        "b": "El método f.readline()",
        "c": "El método f.readlines()"
      },
      "respuesta_correcta": "c",
      "justificacion": "El método f.readlines() lee todo el archivo en la memoria y devuelve su contenido como una lista de sus líneas.",
      "distractores": {
        "a": "Confunde este método con el que lee todo el documento en forma de una única cadena de texto continua.",
        "b": "Confunde el método con la técnica secuencial que extrae únicamente una línea por ejecución sin cargar todo el archivo."
      }
    },
    {
      "id": 3,
      "tema": "Diccionarios",
      "capitulo": "Tabla Hash de Diccionarios (Dict)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "Al iterar directamente sobre un objeto diccionario mediante un bucle for estándar, ¿qué elementos del diccionario se recorren por defecto?",
      "opciones": {
        "a": "Las claves del diccionario en un orden que resulta arbitrario.",
        "b": "Las tuplas completas de pares clave y valor ordenadas secuencialmente.",
        "c": "Los valores almacenados dentro de la estructura en un orden aleatorio."
      },
      "respuesta_correcta": "a",
      "justificacion": "Un bucle for en un diccionario itera sobre sus claves por defecto. Las claves aparecerán en un orden arbitrario.",
      "distractores": {
        "b": "Asume erróneamente que se recorren las tuplas con toda la información, lo cual corresponde al método .items().",
        "c": "Confunde las claves con los datos del contenido interno, los cuales requieren invocar explícitamente al método .values()."
      }
    },
    {
      "id": 4,
      "tema": "Diccionarios",
      "capitulo": "Tabla Hash de Diccionarios (Dict)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "Si se desea verificar la existencia de una clave en un diccionario asegurando que el programa no se interrumpa por errores, ¿cuál es la estrategia recomendada utilizando el método .get()?",
      "opciones": {
        "a": "Invocar dict.get(key) y verificar si el retorno es None o un valor alternativo especificado.",
        "b": "Utilizar el operador de pertenencia \"in\" antes de realizar cualquier extracción forzada de datos.",
        "c": "Lanzar un proceso de desarrollo incremental que detenga la ejecución con la función sys.exit(0)."
      },
      "respuesta_correcta": "a",
      "justificacion": "utiliza dict.get(key) que devuelve el valor o None si la clave no está presente (o get(key, not-found) te permite especificar qué valor devolver en el caso de no encontrarse).",
      "distractores": {
        "b": "Aunque es una forma válida descrita en el texto empleando \"in\", la pregunta pide específicamente la estrategia ligada al uso del método .get().",
        "c": "Mezcla la metodología de diseño de programas descrita al final del documento con los mecanismos técnicos de control de estructuras."
      }
    },
    {
      "id": 5,
      "tema": "Diccionarios",
      "capitulo": "Formateo de Diccionarios",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "Cuando se utiliza el operador de formateo % con un diccionario para construir una cadena, ¿cómo se asocian los valores del diccionario dentro del texto de plantilla?",
      "opciones": {
        "a": "Se insertan mediante marcadores posicionales anónimos según el orden de creación del diccionario.",
        "b": "Se especifican mediante el nombre de las claves encerrado entre paréntesis junto al tipo de datos.",
        "c": "Se referencian utilizando índices numéricos que representan la posición arbitraria de los elementos."
      },
      "respuesta_correcta": "b",
      "justificacion": "El operador % funciona convenientemente para sustituir valores de un diccionario en una cadena por su nombre: s = 'I want %(count)d copies of %(word)s' % h",
      "distractores": {
        "a": "Asume un comportamiento posicional rígido, ignorando que el texto define que el mapeo se realiza explícitamente por el nombre de la clave.",
        "c": "Traslada la lógica de indexación de listas al formateo con diccionarios, lo cual es incorrecto dada la naturaleza de tabla hash de la estructura."
      }
    },
    {
      "id": 6,
      "tema": "Diccionarios",
      "capitulo": "Del",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "¿Qué efecto produce la aplicación del operador \"del\" sobre una sección de corte o rebanada (slice) en una lista de Python?",
      "opciones": {
        "a": "Elimina de forma selectiva y exclusiva el primer elemento de la porción indicada.",
        "b": "Invalida la variable por completo haciendo que el intérprete actúe como si nunca se hubiese definido.",
        "c": "Remueve de la lista original de manera íntegra toda la secuencia de elementos que abarca dicho fragmento."
      },
      "respuesta_correcta": "c",
      "justificacion": "Del también se puede usar en elementos o rebanadas (slices) de listas para eliminar esa parte de la lista",
      "distractores": {
        "a": "Confunde la acción general sobre un rango con la eliminación aislada de un único elemento indexado como del list[0].",
        "b": "Describe la acción de \"del\" cuando se aplica a una variable directa (del var), pero no su comportamiento al operar sobre rebanadas de colecciones."
      }
    },
    {
      "id": 7,
      "tema": "Archivos",
      "capitulo": "Archivos",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "Desde el punto de vista de la optimización, ¿cuál es la principal ventaja de utilizar un bucle for directo para procesar un archivo de texto en Python?",
      "opciones": {
        "a": "Garantiza que el archivo se lea automáticamente tanto en formato de texto como en formato binario puro.",
        "b": "Permite procesar ficheros de gran volumen sin la necesidad de cargar todo el contenido simultáneamente en memoria.",
        "c": "Consigue omitir por defecto los caracteres de salto de línea sin requerir la configuración de la función print."
      },
      "respuesta_correcta": "b",
      "justificacion": "Leer una línea a la vez tiene la excelente cualidad de que no todo el archivo necesita caber en la memoria al mismo tiempo; es muy útil si deseas examinar cada línea de un archivo de 10 gigabytes sin utilizar 10 gigabytes de memoria.",
      "distractores": {
        "a": "El texto contradice directamente esta opción al explicitar de forma tajante que este bucle funciona solo para archivos de texto y no para binarios.",
        "c": "Error conceptual basado en el código de ejemplo; la línea mantiene su salto original y por ello se requiere ajustar el parámetro end='' en el print."
      }
    },
    {
      "id": 8,
      "tema": "Archivos",
      "capitulo": "Archivos Unicode",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "Al realizar la apertura de un archivo con el objetivo de gestionar cadenas de caracteres Unicode de manera explícita, ¿qué parámetros deben configurarse en la función open()?",
      "opciones": {
        "a": "Se debe definir el modo de texto 't' junto con la especificación de una codificación en el parámetro encoding.",
        "b": "Se debe forzar la lectura secuencial mediante el uso exclusivo de la función print parametrizada.",
        "c": "Se debe omitir cualquier tipo de modo y delegar la codificación al uso de la instrucción de escape \\u."
      },
      "respuesta_correcta": "a",
      "justificacion": "Para leer y escribir archivos codificados en unicode, utiliza un modo 't' y especifica explícitamente una codificación: with open('foo.txt', 'rt', encoding='utf-8') as f:",
      "distractores": {
        "b": "Confunde una herramienta de escritura opcional en ficheros abiertos con los parámetros de configuración fundamentales requeridos en la apertura.",
        "c": "Ignora las pautas del documento, el cual exige determinar una codificación textual explícitamente para asegurar que las secuencias sean interpretadas como strings Unicode."
      }
    },
    {
      "id": 9,
      "tema": "Metodología",
      "capitulo": "Ejercicio: Desarrollo incremental",
      "dificultad": "Alto",
      "nivel_cognitivo": "Aplicar",
      "enunciado": "Considera un escenario donde estás desarrollando un script que procesa datos de un archivo. Siguiendo la estrategia de desarrollo incremental descrita en el texto, ¿qué acción práctica debes realizar inmediatamente después de completar el código del primer hito?",
      "opciones": {
        "a": "Escribir la totalidad de las funciones del programa y procesar el documento en bloques de 10 gigabytes.",
        "b": "Imprimir las estructuras de datos actuales y detener la ejecución del script con un comando como sys.exit(0).",
        "c": "Eliminar las variables temporales mediante el operador del para optimizar el rendimiento de la memoria."
      },
      "respuesta_correcta": "b",
      "justificacion": "Escribe el código para alcanzar ese hito y simplemente imprime tus estructuras de datos en ese punto; luego puedes ejecutar un sys.exit(0) para que el programa no avance hacia las partes no terminadas.",
      "distractores": {
        "a": "Contradice radicalmente la metodología incremental expuesta, la cual desaconseja escribir todo el programa de una sola vez y aboga por pasos cortos.",
        "c": "Aplica de forma incorrecta el uso del operador del visto en otra sección, desviándose del objetivo del hito que consiste en inspeccionar visualmente los datos."
      }
    },
    {
      "id": 10,
      "tema": "Diccionarios",
      "capitulo": "Tabla Hash de Diccionarios (Dict)",
      "dificultad": "Alto",
      "nivel_cognitivo": "Analizar",
      "enunciado": "Analiza las siguientes declaraciones sobre las claves en los diccionarios de Python. Basándote estrictamente en el contenido del texto, ¿cuál de las siguientes opciones describe la razón fundamental por la cual las cadenas y las tuplas operan perfectamente como claves?",
      "opciones": {
        "a": "Porque ambas estructuras presentan un ordenamiento secuencial indexado que impide el lanzamiento de un KeyError.",
        "b": "Porque son tipos de datos que se caracterizan por ser inmutables dentro del entorno de ejecución.",
        "c": "Porque actúan de manera automática como listas dinámicas al invocar los métodos keys() e items()."
      },
      "respuesta_correcta": "b",
      "justificacion": "Las cadenas, los números y las tuplas funcionan como claves, y cualquier tipo puede ser un valor. Otros tipos pueden o no funcionar correctamente como claves (las cadenas y las tuplas funcionan perfectamente ya que son inmutables).",
      "distractores": {
        "a": "Asocia erróneamente el control del KeyError al orden de las colecciones, cuando el texto aduce que el error se debe a la ausencia de la clave buscada.",
        "c": "Confunde las propiedades de inmutabilidad de las claves con los métodos de extracción globales que generan listas de datos sobre la estructura hash."
      }
    }
  ]
}