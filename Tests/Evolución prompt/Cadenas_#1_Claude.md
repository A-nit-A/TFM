{
  "examen_metadatos": {
    "num_preguntas": 15,
    "fuente": "Cadenas en Python (Strings) - Texto proporcionado"
  },
  "preguntas": [
    {
      "id": 1,
      "tema": "Inmutabilidad de cadenas",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar (Bloom Nivel 1)",
      "enunciado": "¿Cuál de las siguientes afirmaciones describe correctamente la naturaleza de las cadenas en Python?",
      "opciones": {
        "a": "Las cadenas son mutables y pueden modificarse directamente después de crearse.",
        "b": "Las cadenas son inmutables, lo que significa que no se pueden cambiar después de crearse.",
        "c": "Las cadenas son mutables, a diferencia de Java donde son inmutables.",
        "d": "Las cadenas pueden modificarse solo si se usan comillas dobles en lugar de simples."
      },
      "respuesta_correcta": "b",
      "justificacion": "Las cadenas de Python son 'inmutables', lo que significa que no se pueden cambiar después de crearse (las cadenas de Java también usan este estilo inmutable)."
    },
    {
      "id": 2,
      "tema": "Indexación de cadenas",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar (Bloom Nivel 1)",
      "enunciado": "Si s = 'hello', ¿cuál es el valor de s[1] según la indexación de Python?",
      "opciones": {
        "a": "'h'",
        "b": "'e'",
        "c": "'l'",
        "d": "'o'"
      },
      "respuesta_correcta": "b",
      "justificacion": "Python utiliza indexación basada en cero, por lo que si s es 'hello', s[1] es 'e'."
    },
    {
      "id": 3,
      "tema": "Delimitadores de cadenas",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar (Bloom Nivel 1)",
      "enunciado": "¿Qué tipo de delimitador se debe usar para que un literal de cadena pueda abarcar varias líneas sin necesidad de una barra invertida al final de cada línea?",
      "opciones": {
        "a": "Comillas simples ' '",
        "b": "Comillas dobles \" \"",
        "c": "Comillas triples \"\"\" o '''",
        "d": "Corchetes [ ]"
      },
      "respuesta_correcta": "c",
      "justificacion": "Los literales de cadena dentro de comillas triples, \"\"\" o ''', pueden abarcar varias líneas de texto."
    },
    {
      "id": 4,
      "tema": "Función len()",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar (Bloom Nivel 1)",
      "enunciado": "¿Qué devuelve la función len() cuando se le pasa una cadena como argumento?",
      "opciones": {
        "a": "El índice del último carácter de la cadena.",
        "b": "La longitud de la cadena.",
        "c": "El número de palabras en la cadena.",
        "d": "El carácter situado en la posición central de la cadena."
      },
      "respuesta_correcta": "b",
      "justificacion": "La función len(string) devuelve la longitud de una cadena."
    },
    {
      "id": 5,
      "tema": "Métodos de cadena",
      "capitulo": "Métodos de cadena (String Methods)",
      "dificultad": "Baja",
      "nivel_cognitivo": "Recordar (Bloom Nivel 1)",
      "enunciado": "¿Qué devuelve el método s.strip() cuando se aplica a una cadena s?",
      "opciones": {
        "a": "Una cadena con todos los caracteres en mayúsculas.",
        "b": "Una cadena dividida en una lista por espacios.",
        "c": "Una cadena con los espacios en blanco eliminados del principio y del final.",
        "d": "Una cadena con todas las apariciones de un carácter reemplazadas."
      },
      "respuesta_correcta": "c",
      "justificacion": "s.strip() — devuelve una cadena con los espacios en blanco eliminados del principio y del final."
    },
    {
      "id": 6,
      "tema": "Concatenación y conversión de tipos",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender (Bloom Nivel 2)",
      "enunciado": "¿Por qué la expresión 'The value of pi is ' + 3.14 genera un error en Python?",
      "opciones": {
        "a": "Porque el operador '+' no está definido para cadenas.",
        "b": "Porque Python, a diferencia de Java, no convierte automáticamente números u otros tipos a formato de cadena.",
        "c": "Porque los números de punto flotante no pueden combinarse con ningún tipo de cadena.",
        "d": "Porque el literal de cadena usa comillas simples en lugar de dobles."
      },
      "respuesta_correcta": "b",
      "justificacion": "A diferencia de Java, el '+' no convierte automáticamente números u otros tipos a formato de cadena. La función str() convierte valores a un formato de cadena para que puedan combinarse con otras cadenas."
    },
    {
      "id": 7,
      "tema": "Cadenas crudas (raw strings)",
      "capitulo": "Cadenas en Python (Strings)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender (Bloom Nivel 2)",
      "enunciado": "Un literal de cadena cruda (raw string) tiene el prefijo 'r'. ¿Cuál es la longitud de la cadena r'x\\nx'?",
      "opciones": {
        "a": "2, porque \\n cuenta como un único carácter de salto de línea.",
        "b": "3, porque \\n se convierte en un espacio.",
        "c": "4, porque todos los caracteres se pasan directamente sin tratamiento especial para barras invertidas.",
        "d": "5, porque incluye los delimitadores de comillas."
      },
      "respuesta_correcta": "c",
      "justificacion": "Un literal de cadena 'cruda' (raw string) tiene el prefijo 'r' y pasa todos los caracteres directamente sin un tratamiento especial para las barras invertidas, por lo que r'x\\nx' se evalúa como la cadena de longitud 4 'x\\nx'."
    },
    {
      "id": 8,
      "tema": "Método s.find()",
      "capitulo": "Métodos de cadena (String Methods)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender (Bloom Nivel 2)",
      "enunciado": "¿Qué valor devuelve s.find('other') si la subcadena buscada no se encuentra dentro de s?",
      "opciones": {
        "a": "None",
        "b": "0",
        "c": "-1",
        "d": "Lanza una excepción IndexError."
      },
      "respuesta_correcta": "c",
      "justificacion": "s.find('other') — busca la otra cadena dada (no es una expresión regular) dentro de s, y devuelve el primer índice donde comienza, o -1 si no la encuentra."
    },
    {
      "id": 9,
      "tema": "Rebanadas de cadena (String Slices)",
      "capitulo": "Rebanadas de cadena (String Slices)",
      "dificultad": "Media",
      "nivel_cognitivo": "Aplicar (Bloom Nivel 3)",
      "enunciado": "Dado s = 'Hello', ¿qué devuelve s[1:4]?",
      "opciones": {
        "a": "'Hell'",
        "b": "'ello'",
        "c": "'ell'",
        "d": "'Hel'"
      },
      "respuesta_correcta": "c",
      "justificacion": "s[1:4] es 'ell' — caracteres que comienzan en el índice 1 y se extienden hasta, pero sin incluir, el índice 4."
    },
    {
      "id": 10,
      "tema": "Índices negativos en cadenas",
      "capitulo": "Rebanadas de cadena (String Slices)",
      "dificultad": "Media",
      "nivel_cognitivo": "Aplicar (Bloom Nivel 3)",
      "enunciado": "Dado s = 'Hello', ¿qué devuelve s[-3:]?",
      "opciones": {
        "a": "'He'",
        "b": "'ell'",
        "c": "'llo'",
        "d": "'ello'"
      },
      "respuesta_correcta": "c",
      "justificacion": "s[-3:] es 'llo' — comenzando con el tercer carácter desde el final y extendiéndose hasta el final de la cadena."
    },
    {
      "id": 11,
      "tema": "Método s.split() y s.join()",
      "capitulo": "Métodos de cadena (String Methods)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender (Bloom Nivel 2)",
      "enunciado": "¿Qué resultado produce la expresión '---'.join(['aaa', 'bbb', 'ccc'])?",
      "opciones": {
        "a": "['aaa---bbb---ccc']",
        "b": "'aaa---bbb---ccc'",
        "c": "'aaa', 'bbb', 'ccc'",
        "d": "'---aaa---bbb---ccc---'"
      },
      "respuesta_correcta": "b",
      "justificacion": "s.join(list) — lo contrario de split(), une los elementos de la lista dada utilizando la cadena como delimitador. Por ejemplo, '---'.join(['aaa', 'bbb', 'ccc']) -> aaa---bbb---ccc."
    },
    {
      "id": 12,
      "tema": "Unicode y bytes",
      "capitulo": "Cadenas (Unicode frente a bytes)",
      "dificultad": "Media",
      "nivel_cognitivo": "Comprender (Bloom Nivel 2)",
      "enunciado": "Para convertir una cadena unicode de Python a una cadena de bytes, ¿qué método se debe utilizar?",
      "opciones": {
        "a": "El método decode() de la cadena unicode.",
        "b": "El método encode() de la cadena unicode.",
        "c": "El prefijo 'b' delante del nombre de la variable.",
        "d": "La función str() con el parámetro 'bytes'."
      },
      "respuesta_correcta": "b",
      "justificacion": "Para convertir una cadena normal de Python en bytes, llama al método encode() de la cadena."
    },
    {
      "id": 13,
      "tema": "F-strings y formateo",
      "capitulo": "Formateo de cadenas (String formatting)",
      "dificultad": "Alta",
      "nivel_cognitivo": "Analizar (Bloom Nivel 4)",
      "enunciado": "Considerando las f-strings, ¿cuál de las siguientes afirmaciones describe mejor su comportamiento respecto al texto fuera de las llaves '{}'?",
      "opciones": {
        "a": "El texto fuera de '{}' se evalúa como una expresión Python y se convierte a cadena.",
        "b": "El texto fuera de '{}' se imprime directamente, mientras que las expresiones dentro de '{}' se evalúan con la especificación de formato.",
        "c": "El texto fuera de '{}' se ignora y solo se imprime el contenido de las llaves.",
        "d": "El texto fuera de '{}' debe ser siempre un tipo numérico para poder combinarse con las expresiones internas."
      },
      "respuesta_correcta": "b",
      "justificacion": "Cualquier texto fuera de las llaves '{}' se imprime directamente. Las expresiones contenidas en '{}' se imprimen utilizando la especificación de formato descrita en la especificación de formato."
    },
    {
      "id": 14,
      "tema": "Tipo carácter en Python",
      "capitulo": "Métodos de cadena (String Methods)",
      "dificultad": "Alta",
      "nivel_cognitivo": "Analizar (Bloom Nivel 4)",
      "enunciado": "¿Qué implicación práctica tiene el hecho de que Python no tenga un tipo de carácter ('char') separado?",
      "opciones": {
        "a": "Es imposible acceder a un carácter individual de una cadena mediante indexación.",
        "b": "El acceso a s[8] genera siempre un error de tipo en Python.",
        "c": "Una expresión como s[8] devuelve una cadena de longitud 1, con la que los operadores de comparación funcionan normalmente.",
        "d": "Para comparar caracteres individuales se deben usar módulos externos como 'string'."
      },
      "respuesta_correcta": "c",
      "justificacion": "Python no tiene un tipo de carácter separado. En su lugar, una expresión como s[8] devuelve una cadena de longitud 1 que contiene el carácter. Con esa cadena de longitud 1, los operadores ==, <=, ... funcionan todos como cabría esperar."
    },
    {
      "id": 15,
      "tema": "Regla de rebanadas y propiedades de índices",
      "capitulo": "Rebanadas de cadena (String Slices)",
      "dificultad": "Alta",
      "nivel_cognitivo": "Evaluar (Bloom Nivel 5)",
      "enunciado": "El documento establece que para cualquier índice n, s[:n] + s[n:] == s. ¿Cuál de las siguientes conclusiones se puede inferir correctamente a partir de esta regla?",
      "opciones": {
        "a": "La regla solo es válida cuando n es un índice positivo dentro del rango de la cadena.",
        "b": "La regla falla cuando n es negativo porque los índices negativos no son admitidos en las rebanadas.",
        "c": "La regla garantiza que s[:n] y s[n:] siempre dividen la cadena en dos partes conservando todos los caracteres, incluso si n es negativo o está fuera de los límites.",
        "d": "La regla implica que s[:n] y s[n:] siempre producen subcadenas de la misma longitud."
      },
      "respuesta_correcta": "c",
      "justificacion": "Es una bonita regla de las rebanadas que, para cualquier índice n, s[:n] + s[n:] == s. Esto funciona incluso si n es negativo o está fuera de los límites. O dicho de otra forma, s[:n] y s[n:] siempre dividen la cadena en dos partes, conservando todos los caracteres."
    }
  ]
}