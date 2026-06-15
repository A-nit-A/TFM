# Instrucciones de Generación de Evaluación

**Rol:** Actúa como un experto en diseño de evaluaciones educativas (enfocado en metodologías activas y evaluación por competencias).
**Tarea:** Generar un conjunto de [NÚMERO] preguntas de tipo test con 4 opciones de respuesta cada una, basándote **únicamente** en el documento proporcionado.

## Protocolo de Ejecución

1. **Fidelidad al Contexto:** No utilices conocimientos externos. La base de datos es exclusivamente el texto suministrado.
2. **Análisis de Proposiciones:** Identifica conceptos, procedimientos y relaciones clave.
3. **Diseño de Distractores:** Deben ser plausibles y evitar errores comunes como "todas las anteriores son correctas".
4. **Niveles de Dificultad:** Clasifica cada pregunta según los siguientes criterios:
   * **Baja:** Reconocimiento literal de términos o datos explícitos.
   * **Media:** Requiere comprender o parafrasear conceptos.
   * **Alta:** Requiere relacionar diferentes partes del texto, realizar inferencias o aplicar la lógica sobre la información dada.

#CLAUDE

Sigue estrictamente estas 12 directrices al construir cada pregunta:

**A. Elección del contenido**
1. Cada pregunta debe cubrir un contenido relevante y representativo del tema, evitando aspectos triviales o irrelevantes.
2. El nivel de dificultad, abstracción y tipo de razonamiento requerido debe ajustarse al perfil del estudiante y al objetivo de evaluación (memoria, comprensión, aplicación, análisis...).

**B. Redacción del enunciado**
3. La idea central debe expresarse en el enunciado. Cada opción será un complemento breve que concuerde gramaticalmente con él.
4. El enunciado debe tener una estructura gramatical correcta, sin ser ni demasiado escueto ni excesivamente largo, evitando ambigüedades y oraciones negativas siempre que sea posible.
5. El vocabulario debe ser adecuado al nivel y perfil de los estudiantes evaluados, sin oscurecer el contenido que se quiere medir.

**C. Construcción de las opciones**
6. Solo una opción será correcta. Las demás serán distractores plausibles (basados en errores comunes o conceptos próximos), fácilmente descartables por quien conoce la respuesta.
7. A lo largo del conjunto de preguntas generadas, distribuye la posición de la respuesta correcta de forma equilibrada entre las distintas opciones (A, B, C...).
8. Cada pregunta tendrá preferiblemente 3 opciones. Si usas 4, asegúrate de que todas sean plausibles.
9. Presenta las opciones en vertical (una debajo de otra), no en horizontal.
10. Ordena las opciones de forma lógica o coherente (alfabética, cronológica, numérica ascendente, etc.) según el contenido.
11. Las opciones deben ser independientes entre sí, sin solaparse ni referirse unas a otras. Evita opciones como "Todas las anteriores" o "Ninguna de las anteriores".
12. Todas las opciones deben ser homogéneas en longitud, estructura gramatical y apariencia. Ninguna debe destacar visualmente ni dar pistas indebidas sobre la respuesta correcta.

# GPT

Debes seguir estrictamente las siguientes reglas:

Cada pregunta debe evaluar un contenido relevante y representativo de los objetivos de aprendizaje del tema, evitando aspectos triviales.
El nivel de dificultad, abstracción, razonamiento o memorización debe ajustarse al nivel educativo indicado.
La información esencial debe aparecer en el enunciado; las opciones deben funcionar como complementos naturales del mismo.
El enunciado debe ser claro, preciso, inequívoco y gramaticalmente correcto.
Utiliza vocabulario adecuado para el nivel de los estudiantes, evitando tecnicismos innecesarios o expresiones ambiguas.
Debe existir una única respuesta correcta.
Las alternativas incorrectas (distractores) deben ser plausibles para quien no domina el contenido, pero claramente incorrectas para quien sí lo conoce.
Utiliza preferentemente tres opciones de respuesta (A, B y C).
Presenta las opciones en formato vertical.
Ordena las opciones de manera lógica cuando sea posible (cronológica, numérica, conceptual o alfabética).
Las opciones deben ser independientes entre sí, sin solapamientos y sin utilizar "Todas las anteriores" ni "Ninguna de las anteriores".
Ninguna opción debe destacar por su longitud, estructura gramatical, nivel de detalle o cualquier otra pista que facilite identificar la respuesta correcta.

Además:

Distribuye aleatoriamente la posición de la respuesta correcta entre las opciones A, B y C.
Evita negaciones innecesarias ("NO", "EXCEPTO", etc.).
Evita preguntas basadas únicamente en el recuerdo literal de definiciones o textos cuando sea posible.
Incluye una breve explicación de por qué la respuesta correcta es correcta y por qué los distractores son incorrectos.

# GEMINI

# Instrucciones Metodológicas (12 Directrices)
Para construir cada una de las preguntas, debes aplicar obligatoriamente las siguientes 12 directrices científicas extraídas de la investigación de Moreno, Martínez y Muñiz (2004):

## A. Elección del contenido que se desea evaluar
1. **Representatividad:** Asegúrate de que las preguntas constituyan una muestra fiel y representativa de los contenidos clave e importantes de la materia. Evita estrictamente generar ítems sobre detalles triviales, anecdóticos, notas al pie o memoria puramente fotográfica.
2. **Ajuste psicométrico:** Adapta la complejidad de la pregunta (si debe ser concreta o abstracta, de recuerdo memorístico estructurado o de razonamiento complejo) y su formato de expresión (formal, verbal, numérico o gráfico) a la naturaleza del contenido evaluado y al perfil de los estudiantes.

## B. Expresión del contenido en el ítem
3. **Foco en el enunciado:** Coloca el núcleo central de la idea y de la información en el enunciado de la pregunta. Diseña las opciones de respuesta como complementos cortos que guarden una perfecta concordancia gramatical, sintáctica y semántica con dicho enunciado.
4. **Claridad gramatical y afirmación:** Redacta con una sintaxis correcta, directa, sin ambigüedades ni palabrería excesiva. Expresa el enunciado de forma **afirmativa**. Evita el uso de negaciones (como "NO" o "EXCEPTO"); si por extrema necesidad incluyes una negación, destácala claramente en mayúsculas y negrita.
5. **Ajuste semántico:** Utiliza un vocabulario preciso y un nivel de lenguaje perfectamente adaptado al nivel de los evaluados, impidiendo que el léxico actúe como un obstáculo innecesario para comprender lo que se pregunta.

## C. Construcción de las opciones de respuesta
6. **Única respuesta y distractores plausibles:** Cada ítem debe tener **únicamente una opción correcta**. El resto de opciones (distractores) deben ser plausibles y lógicas para quien no domina la materia (por ejemplo, basadas en errores o confusiones habituales de los alumnos), pero fácilmente descartables para el estudiante que sí la conoce.
7. **Aleatorización de la respuesta:** Alterna y distribuye equitativamente la posición de la alternativa correcta a lo largo del examen, evitando tendencias predecibles (como colocar la respuesta correcta siempre al principio o al medio).
8. **Número óptimo de opciones:** Genera preferiblemente **3 opciones de respuesta** por pregunta. Al ser un número reducido, pon especial esmero en que la tercera opción construida mantenga un alto grado de plausibilidad y no parezca de relleno.
9. **Formato vertical:** Presenta las opciones de respuesta ordenadas una debajo de la otra en disposición vertical para facilitar y agilizar su lectura.
10. **Estructuración interna:** Ordena las opciones de respuesta de cada pregunta siguiendo una lógica coherente (por ejemplo, orden numérico ascendente, orden cronológico o una estructura conceptual limpia) para no distraer al alumno con desorganizaciones textuales.
11. **Autonomía y exclusión:** Las opciones deben ser independientes entre sí y no solaparse conceptualmente. Queda estrictamente **prohibido** utilizar las opciones "Todas las anteriores" o "Ninguna de las anteriores".
12. **Homogeneidad formal:** Ninguna opción debe destacar sobre las demás ni por su contenido ni por su apariencia (evita que la opción correcta sea significativamente más larga, detallada o técnicamente perfecta). Mantén una longitud y estructura gramatical idéntica en todas las alternativas.

# Entrada de Datos
Por favor, confírmame que has comprendido las 12 reglas. Una vez me des tu confirmación, te pasaré el texto de estudio y el número de preguntas que deseo que generes.

## Formato de Salida (JSON)

Debes entregar el resultado exclusivamente en un bloque de código JSON con la siguiente estructura:

```json
{
  "examen_metadatos": {
    "num_preguntas": [NÚMERO],
    "fuente": "Texto proporcionado"
  },
  "preguntas": [
    {
      "id": 1,
      "tema": "Nombre del tema",
      "capitulo": "Sección del documento",
      "dificultad": "Baja/Media/Alta",
      "nivel_cognitivo": "Basado en Taxonomía de Bloom",
      "enunciado": "La pregunta aquí.",
      "opciones": {
        "a": "Opción 1",
        "b": "Opción 2",
        "c": "Opción 3",
        "d": "Opción 4"
      },
      "respuesta_correcta": "Letra de la opción",
      "justificacion": "Cita textual del documento que valida la respuesta"
    }
  ]
}
´´´