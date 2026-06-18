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
      "enunciado": "¿Qué característica tienen las cadenas en Python según el documento?",
      "opciones": {
        "a": "Son mutables y pueden modificarse directamente.",
        "b": "Son inmutables y no pueden cambiarse después de crearse.",
        "c": "Solo admiten caracteres ASCII.",
        "d": "Deben declararse antes de usarse."
      },
      "respuesta_correcta": "b",
      "justificacion": "Las cadenas de Python son \"inmutables\", lo que significa que no se pueden cambiar después de crearse."
    },
    {
      "id": 2,
      "tema": "Indexación de cadenas",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar",
      "enunciado": "Si s = 'hello', ¿qué valor devuelve s[1]?",
      "opciones": {
        "a": "h",
        "b": "l",
        "c": "e",
        "d": "o"
      },
      "respuesta_correcta": "c",
      "justificacion": "Si s es 'hello', s[1] es 'e'."
    },
    {
      "id": 3,
      "tema": "Conversión de tipos",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "¿Por qué se utiliza la función str() al concatenar una cadena con un número?",
      "opciones": {
        "a": "Porque convierte números en listas.",
        "b": "Porque Python convierte automáticamente cualquier tipo a cadena.",
        "c": "Porque el operador '+' no convierte automáticamente números a cadenas.",
        "d": "Porque mejora el rendimiento de la concatenación."
      },
      "respuesta_correcta": "c",
      "justificacion": "A diferencia de Java, el '+' no convierte automáticamente números u otros tipos a formato de cadena. La función str() convierte valores a un formato de cadena."
    },
    {
      "id": 4,
      "tema": "Métodos de cadena",
      "capitulo": "Métodos de cadena (String Methods)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender",
      "enunciado": "¿Qué devuelve el método s.find('other') cuando no encuentra la subcadena buscada?",
      "opciones": {
        "a": "0",
        "b": "None",
        "c": "False",
        "d": "-1"
      },
      "respuesta_correcta": "d",
      "justificacion": "s.find('other') devuelve el primer índice donde comienza, o -1 si no la encuentra."
    },
    {
      "id": 5,
      "tema": "Métodos de cadena",
      "capitulo": "Métodos de cadena (String Methods)",
      "dificultad": "Media",
      "nivel_cognitivo": "Aplicar",
      "enunciado": "¿Cuál es el resultado de 'aaa,bbb,ccc'.split(',')?",
      "opciones": {
        "a": "[['aaa'], ['bbb'], ['ccc']]",
        "b": "['aaa', 'bbb', 'ccc']",
        "c": "'aaa' 'bbb' 'ccc'",
        "d": "{'aaa','bbb','ccc'}"
      },
      "respuesta_correcta": "b",
      "justificacion": "'aaa,bbb,ccc'.split(',') -> ['aaa', 'bbb', 'ccc']."
    },
    {
      "id": 6,
      "tema": "Rebanadas de cadena",
      "capitulo": "String Slices",
      "dificultad": "Media",
      "nivel_cognitivo": "Aplicar",
      "enunciado": "Si s = 'Hello', ¿qué resultado produce la expresión s[1:4]?",
      "opciones": {
        "a": "Hell",
        "b": "ello",
        "c": "ell",
        "d": "Hel"
      },
      "respuesta_correcta": "c",
      "justificacion": "s[1:4] es 'ell' — caracteres que comienzan en el índice 1 y se extienden hasta, pero sin incluir, el índice 4."
    },
    {
      "id": 7,
      "tema": "Rebanadas de cadena",
      "capitulo": "String Slices",
      "dificultad": "Alta",
      "nivel_cognitivo": "Analizar",
      "enunciado": "¿Qué expresión devuelve los últimos tres caracteres de la cadena 'Hello'?",
      "opciones": {
        "a": "s[:-3]",
        "b": "s[-3:]",
        "c": "s[3:-1]",
        "d": "s[:3]"
      },
      "respuesta_correcta": "b",
      "justificacion": "s[-3:] es 'llo' — comenzando con el tercer carácter desde el final y extendiéndose hasta el final de la cadena."
    },
    {
      "id": 8,
      "tema": "Formateo de cadenas",
      "capitulo": "Formatted String Literals",
      "dificultad": "Alta",
      "nivel_cognitivo": "Analizar",
      "enunciado": "¿Qué permite la sintaxis {value:.2f} dentro de una f-string?",
      "opciones": {
        "a": "Convertir una cadena a entero.",
        "b": "Truncar el valor para mostrar dos decimales.",
        "c": "Codificar el valor en UTF-8.",
        "d": "Transformar el valor en una lista."
      },
      "respuesta_correcta": "b",
      "justificacion": "Hay muchas cosas útiles que se pueden hacer con el formateo, incluyendo el truncamiento."
    },
    {
      "id": 9,
      "tema": "Unicode y bytes",
      "capitulo": "Cadenas (Unicode frente a bytes)",
      "dificultad": "Alta",
      "nivel_cognitivo": "Comprender",
      "enunciado": "¿Qué método se utiliza para convertir una cadena unicode en bytes?",
      "opciones": {
        "a": "decode()",
        "b": "split()",
        "c": "encode()",
        "d": "join()"
      },
      "respuesta_correcta": "c",
      "justificacion": "Para convertir una cadena normal de Python en bytes, llama al método encode() de la cadena."
    },
    {
      "id": 10,
      "tema": "Sentencia If",
      "capitulo": "Sentencia If",
      "dificultad": "Alta",
      "nivel_cognitivo": "Analizar",
      "enunciado": "Según el documento, ¿cuál es una diferencia importante entre Python y lenguajes como Java o C al escribir una sentencia if?",
      "opciones": {
        "a": "Python exige llaves {} para delimitar bloques.",
        "b": "Python utiliza && y || para operadores booleanos.",
        "c": "La condición debe estar siempre entre paréntesis.",
        "d": "Python utiliza ':' y sangría para agrupar sentencias."
      },
      "respuesta_correcta": "d",
      "justificacion": "Python utiliza los dos puntos (:) y la sangría/espacio en blanco para agrupar sentencias."
    }
  ]
}