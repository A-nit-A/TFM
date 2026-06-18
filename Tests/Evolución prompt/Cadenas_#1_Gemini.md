{
  "examen_metadatos": {
    "num_preguntas": 10,
    "fuente": "Texto proporcionado"
  },
  "preguntas": [
    {
      "id": 1,
      "tema": "Cadenas en Python",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar",
      "enunciado": "¿Qué módulo de cadenas es más antiguo y NO se debe usar en Python según el texto?",
      "opciones": {
        "a": "str",
        "b": "string",
        "c": "unicode",
        "d": "bytes"
      },
      "respuesta_correcta": "b",
      "justificacion": "hay un módulo más antiguo llamado \"string\" que no debes usar"
    },
    {
      "id": 2,
      "tema": "Inmutabilidad",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "Debido a que las cadenas en Python son inmutables, ¿cómo se representan los valores calculados en el código?",
      "opciones": {
        "a": "Modificando directamente los caracteres de la cadena original mediante sus índices.",
        "b": "Construyendo nuevas cadenas a medida que avanzamos.",
        "c": "Utilizando una función especial del sistema que reescribe la memoria del objeto.",
        "d": "Convirtiéndolas automáticamente a listas mutables antes de operar."
      },
      "respuesta_correcta": "b",
      "justificacion": "Como las cadenas no se pueden modificar, construimos *nuevas* cadenas a medida que avanzamos para representar los valores calculados."
    },
    {
      "id": 3,
      "tema": "Sintaxis y Errores",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "¿Qué hace Python si se intenta acceder a un índice que está fuera de los límites de una cadena?",
      "opciones": {
        "a": "Devuelve un valor por defecto como una cadena vacía.",
        "b": "Devuelve el carácter correspondiente al último índice válido.",
        "c": "Genera un error y se detiene.",
        "d": "Asigna automáticamente un valor nulo de tipo None."
      },
      "respuesta_correcta": "c",
      "justificacion": "Si el índice está fuera de los límites de la cadena, Python genera un error. El estilo de Python (a diferencia de Perl) es detenerse si no sabe qué hacer"
    },
    {
      "id": 4,
      "tema": "Operadores de Números",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar",
      "enunciado": "En el manejo de números dentro de Python, ¿cuál de los siguientes operadores NO existe?",
      "opciones": {
        "a": "++",
        "b": "+=",
        "c": "-=",
        "d": "//"
      },
      "respuesta_correcta": "a",
      "justificacion": "No existe el operador ++, pero funcionan +=, -=, etc."
    },
    {
      "id": 5,
      "tema": "Métodos de Cadena",
      "capitulo": "Métodos de cadena (String Methods)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar",
      "enunciado": "¿Qué método se utiliza para eliminar los espacios en blanco del principio y del final de una cadena?",
      "opciones": {
        "a": "s.lower()",
        "b": "s.strip()",
        "c": "s.replace()",
        "d": "s.split()"
      },
      "respuesta_correcta": "b",
      "justificacion": "s.strip() — devuelve una cadena con los espacios en blanco eliminados del principio y del final."
    },
    {
      "id": 6,
      "tema": "Métodos de Cadena",
      "capitulo": "Métodos de cadena (String Methods)",
      "dificultad": "Media",
      "nivel_cognitivo": "Aplicar",
      "enunciado": "Si ejecutamos la expresión 'aaa,bbb,ccc'.split(','), ¿cuál es el resultado devuelto?",
      "opciones": {
        "a": "'aaa-bbb-ccc'",
        "b": "['aaa', 'bbb', 'ccc']",
        "c": "Una única cadena compactada sin comas.",
        "d": "Un error de sintaxis por usar un delimitador de texto."
      },
      "respuesta_correcta": "b",
      "justificacion": "'aaa,bbb,ccc'.split(',') -> ['aaa', 'bbb', 'ccc']"
    },
    {
      "id": 7,
      "tema": "Rebanadas de Cadena",
      "capitulo": "Rebanadas de cadena (String Slices)",
      "dificultad": "Alta",
      "nivel_cognitivo": "Analizar",
      "enunciado": "Si tenemos la cadena s = \"Hello\", ¿cuál será el resultado exacto de la rebanada s[:-3]?",
      "opciones": {
        "a": "'llo'",
        "b": "'He'",
        "c": "'Hel'",
        "d": "'Hello'"
      },
      "respuesta_correcta": "b",
      "justificacion": "s[:-3] es 'He' — yendo hasta, pero sin incluir, los últimos 3 caracteres."
    },
    {
      "id": 8,
      "tema": "Conversión Unicode y Bytes",
      "capitulo": "Cadenas (Unicode frente a bytes)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "¿Qué método se debe llamar sobre una cadena de bytes para convertirla de nuevo en una cadena unicode?",
      "opciones": {
        "a": "encode()",
        "b": "str()",
        "c": "decode()",
        "d": "format()"
      },
      "respuesta_correcta": "c",
      "justificacion": "el método decode() de la cadena de bytes convierte bytes codificados puros en una cadena unicode"
    },
    {
      "id": 9,
      "tema": "Sentencia If",
      "capitulo": "Sentencia If",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar",
      "enunciado": "¿Cuáles son los operadores booleanos basados en palabras que utiliza Python en lugar de los símbolos de estilo C (&&, ||, !)?",
      "opciones": {
        "a": "and, or, not",
        "b": "amp, pipe, excl",
        "c": "if, elif, else",
        "d": "True, False, None"
      },
      "respuesta_correcta": "a",
      "justificacion": "Los operadores booleanos son las palabras escritas *and*, *or*, *not* (Python no utiliza el estilo C && || !)."
    },
    {
      "id": 10,
      "tema": "Sentencia If",
      "capitulo": "Sentencia If",
      "dificultad": "Alta",
      "nivel_cognitivo": "Analizar",
      "enunciado": "De acuerdo con el texto, ¿cuáles de los siguientes valores cuentan como falsos en una prueba condicional de Python?",
      "opciones": {
        "a": "Únicamente el valor booleano False.",
        "b": "El número 0 y el valor booleano False exclusivamente.",
        "c": "None, 0, cadena vacía, lista vacía y diccionario vacío.",
        "d": "Cualquier número negativo, el cero y los strings sin formatear."
      },
      "respuesta_correcta": "c",
      "justificacion": "Los valores \"cero\" cuentan todos como falsos: None, 0, cadena vacía, lista vacía, diccionario vacío."
    }
  ]
}