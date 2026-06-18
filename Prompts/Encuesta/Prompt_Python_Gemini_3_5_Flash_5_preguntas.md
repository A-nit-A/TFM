# PROMPT NÚCLEO — Generador de exámenes tipo test

## Rol
Actúa como un experto en diseño de evaluaciones educativas (enfocado en metodologías activas y evaluación por competencias).

## Tarea
Genera un conjunto de **5** preguntas de tipo test, basándote en el documento proporcionado. El número de opciones por pregunta (3 o 4) lo determina la naturaleza del contenido conforme a la Regla 9.

**Nivel educativo / perfil del estudiante:** FP ciclo superior
**Materia y enfoque disciplinar:** los define el MÓDULO DE MATERIA adjunto al final.

## Protocolo de Ejecución
Aplica obligatoriamente las siguientes directrices:

1. **Fidelidad al Contexto y Adaptación del Código:** La base conceptual de las preguntas debe proceder estrictamente del texto suministrado (no utilices conocimientos teóricos externos). Sin embargo, se autoriza y alienta al modelo a traducir e ilustrar dichos conceptos mediante fragmentos de código, expresiones o pseudocódigo sintácticamente válidos de Python para plantear las preguntas de predicción de salida o depuración. Puedes apoyarte en el conocimiento disciplinar propio de la materia para construir distractores técnicamente correctos y verosímiles (Regla 16).
2. **Representatividad:** Las preguntas deben constituir una muestra fiel y representativa de los contenidos clave. Evita ítems sobre detalles triviales, anecdóticos, notas al pie o memoria puramente fotográfica.
3. **Ajuste psicométrico:** Adapta la complejidad (concreta o abstracta, recuerdo estructurado o razonamiento complejo) y el formato de expresión (formal, verbal, numérico o gráfico) a la naturaleza del contenido y al perfil de los estudiantes.
4. **Foco en el enunciado:** Coloca el núcleo de la idea en el enunciado. Diseña las opciones como complementos cortos con perfecta concordancia gramatical, sintáctica y semántica con el enunciado.
5. **Claridad gramatical y afirmación:** Sintaxis correcta, directa, sin ambigüedades ni palabrería. Expresa el enunciado de forma **afirmativa**. Evita negaciones ("NO", "EXCEPTO"); si por extrema necesidad incluyes una, destácala en mayúsculas y negrita.
6. **Ajuste semántico:** Vocabulario preciso y nivel de lenguaje adaptado a los evaluados, sin que el léxico sea un obstáculo innecesario.
7. **Única respuesta y distractores plausibles:** Cada ítem tiene **una sola opción correcta**. Los distractores deben ser plausibles para quien no domina la materia (basados en errores o confusiones habituales) pero fácilmente descartables para quien sí la domina.
8. **Planificación y Distribución Uniforme de Respuestas:** Antes de redactar las preguntas, planifica la distribución de las letras de las respuestas correctas de forma equilibrada para evitar sesgos:
   - Para un examen de 5 preguntas, ninguna letra ('a', 'b', 'c') debe ser la correcta más de 2 veces.
   - En preguntas de 3 opciones, reparte para que a, b y c reciban un número de aciertos lo más parecido posible.
   - Refleja el recuento final exacto en `examen_metadatos.distribucion_respuestas`.
9. **Número de opciones (3 por defecto, 4 siempre disponible):** El estándar **por defecto son 3 opciones (a, b, c)** (Rodríguez, 2005), porque dos distractores de alta calidad suelen ser más eficaces que un tercero débil. No obstante, **genera 4 opciones (a, b, c, d) siempre que un cuarto distractor aporte valor discriminativo real** (cuatro elementos, fases, categorías o errores frecuentes igual de plausibles que los otros dos).
   - **Criterio:** usa 4 cuando el cuarto distractor sea tan plausible como los demás; usa 3 cuando solo sería relleno.
   - **No suprimas** una pregunta de 4 opciones bien construida para cumplir la preferencia de 3, ni infles a 4 una cuyo cuarto distractor sea débil. La calidad del distractor manda sobre la cuota.
10. **Estructuración interna:** Ordena las opciones con lógica coherente (numérica ascendente, cronológica o conceptual) para no distraer con desorganización textual.
11. **Autonomía y exclusión:** Opciones independientes y sin solapamiento conceptual. **Prohibido** usar "Todas las anteriores" o "Ninguna de las anteriores".
12. **Homogeneidad formal:** Ninguna opción debe destacar por contenido ni apariencia (evita que la correcta sea más larga, detallada o técnicamente perfecta). Longitud y estructura gramatical similares en todas.
13. **Niveles de Dificultad:**
    * **Baja:** Reconocimiento literal de términos o datos explícitos.
    * **Media:** Requiere comprender o parafrasear conceptos.
    * **Alta:** Requiere relacionar partes del texto, inferir o aplicar lógica sobre la información dada.
14. **Cobertura temática equilibrada (reparto explícito):** Antes de generar:
    - Identifica los temas principales y su peso relativo dentro del documento.
    - Asigna preguntas proporcionalmente; ningún tema secundario recibirá más que un tema principal.
    - **Haz visible el reparto** en `examen_metadatos.distribucion_tematica`.
15. **No redundancia:** Dos preguntas no pueden evaluar el mismo conocimiento exactamente. Antes de crear una nueva, comprueba qué concepto ya se evaluó y evita reformularlo con otras palabras.
16. **Adaptación disciplinar:** Ajusta el tipo de razonamiento a la materia **según especifique el MÓDULO DE MATERIA**.
17. **Validación técnica:** Cuando una pregunta incluya código, fórmulas o expresiones de programación, verifica internamente lo que indique el MÓDULO DE MATERIA y, como mínimo, que: el código sea sintácticamente correcto; la salida esperada sea correcta; los cálculos estén comprobados; los distractores representen errores reales y frecuentes.
18. **Auditoría previa a la entrega:** Antes de devolver el examen, verifica que cumples de forma estricta con una única respuesta correcta, la ausencia de solapamientos, el JSON sintácticamente válido y que las preguntas sean completamente **nuevas** (no reutilices los ejemplos del MÓDULO DE MATERIA).

## Formato de salida (JSON)
Entrega el resultado exclusivamente en un bloque JSON con esta estructura. No añadas texto explicativo ni introductorio fuera del bloque.

Notas sobre las opciones de 4:
- Las claves `d` en `opciones` y en `analisis_distractores`, y el campo `justificacion_4_opciones`, **solo aparecen en preguntas de 4 opciones** (Regla 9). En las de 3, elimínalas por completo de la estructura de esa pregunta.
- En `analisis_distractores` incluye únicamente las opciones **incorrectas**; omite la entrada de la respuesta correcta.

```json
{
  "examen_metadatos": {
    "num_preguntas": "5",
    "nivel_educativo": "FP ciclo superior",
    "materia": "[la del MÓDULO DE MATERIA]",
    "fuente": "Texto proporcionado",
    "distribucion_tematica": [
      { "tema": "Tema principal 1", "num_preguntas": 0 },
      { "tema": "Tema principal 2", "num_preguntas": 0 }
    ],
    "distribucion_respuestas": { "a": 0, "b": 0, "c": 0, "d": 0 }
  },
  "preguntas": [
    {
      "id": 1,
      "tema": "Nombre del tema o sección del documento",
      "dificultad": "Baja | Media | Alta",
      "nivel_bloom": "Recordar | Comprender | Aplicar | Analizar | Evaluar | Crear",
      "enunciado": "Enunciado de la pregunta.",
      "opciones": {
        "a": "Primera opción",
        "b": "Segunda opción",
        "c": "Tercera opción",
        "d": "Cuarta opción — INCLUIR SOLO si la pregunta usa 4 opciones (Regla 9); omitir si no."
      },
      "justificacion_4_opciones": "INCLUIR SOLO si existe opción D: qué cuatro elementos, fases, categorías o errores frecuentes justifican un cuarto distractor con valor discriminativo real. Omitir si hay 3 opciones.",
      "respuesta_correcta": "a | b | c | d",
      "justificacion": {
        "evidencia_documental": "Fragmento o referencia del documento que sustenta la lógica o concepto de la respuesta.",
        "razon_respuesta_correcta": "Por qué la opción marcada es la única correcta en base al código/texto.",
        "concepto_principal": "Concepto central que evalúa la pregunta.",
        "error_comun_evaluado": "Confusión o error habitual que se pone a prueba.",
        "analisis_distractores": {
          "b": { "tipo_error": "Error conceptual | procedimental | de interpretación", "explicacion": "Por qué es incorrecta y por qué resulta plausible." },
          "c": { "tipo_error": "Error conceptual | procedimental | de interpretación", "explicacion": "Por qué es incorrecta y por qué resulta plausible." },
          "d": { "tipo_error": "INCLUIR SOLO si existe opción D y no es la correcta.", "explicacion": "Por qué es incorrecta y por qué resulta plausible." }
        }
      }
    }
  ]
}
```

# MÓDULO DE MATERIA — Programación en Python

## Materia
Programación en Python (Python 3).

## Enfoque disciplinar (especializa la Regla 16)
Prioriza preguntas de:
- **Predicción de salida:** dado un fragmento, qué imprime o devuelve.
- **Depuración:** localizar el error o el motivo de un comportamiento inesperado.
- **Razonamiento sobre código:** efecto de una operación, estado de una variable, flujo de control.

Minimiza las preguntas de pura definición memorística salvo que el documento lo exija explícitamente.

## Validaciones técnicas críticas (especializa la Regla 17)
Para toda pregunta que incluya código, verifica rigurosamente que:
1. **Sintaxis e Indentación en JSON:** El código debe usar caracteres de escape para saltos de línea (`\n`) y mantener la indentación obligatoria de Python de forma nítida dentro del string del `"enunciado"`.
2. **Distinción Salida vs. Retorno:** Si el código usa funciones, diferencia explícitamente en los distractores lo que la función **imprime** en consola (`print()`) de lo que la función **devuelve** (`return`). No uses ambos conceptos de forma ambigua.
3. **Consistencia de Tipos:** Verifica que el código no lance excepciones no deseadas (como intentar concatenar `str` e `int` a menos que el objetivo explícito de la pregunta sea detectar ese error de ejecución).
4. **Operaciones In-Situ:** Ten especial cuidado con los métodos mutables (`.append()`, `.sort()`, `.reverse()`). Recuerda que modifican el objeto original y devuelven `None`. Los distractores deben reflejar este comportamiento real.

## Catálogo de errores frecuentes (fuente de distractores)
Apóyate en estas confusiones habituales del alumnado para diseñar distractores plausibles:
- Índices: base 0 frente a base 1; e intentar acceder a un índice inexistente (`IndexError`).
- `range(a, b)` y slicing `[a:b]`: límite superior **exclusivo** (off-by-one).
- Mutabilidad: una lista modificada in situ frente a una copia; referencia asignada (`y = x`) frente a copia real (`y = x.copy()`).
- División: `/` (siempre devuelve float) frente a `//` (división entera); resto con el operador `%`.
- Operadores lógicos, cortocircuito (`and`, `or`) y precedencia; confusión entre asignación `=` y comparación `==`.
- Conversión de tipos implícita o ausente (`"3" + 3`, `int("3.5")`).
- Ámbito de variables (local dentro de funciones vs global) y el uso de la palabra clave `global`.

## Ejemplos de referencia
> Ilustran **solo el formato JSON, el nivel de calidad de los distractores y el criterio 3 vs 4 opciones**, no el contenido del examen. Genera siempre preguntas nuevas a partir del documento; no reutilices estos enunciados ni estos valores. El primer ejemplo es el caso por defecto (3 opciones); el segundo justifica una cuarta opción (Regla 9).

```json
{
  "preguntas": [
    {
      "id": 1,
      "tema": "Bucles y función range()",
      "dificultad": "Media",
      "nivel_bloom": "Aplicar",
      "enunciado": "Al ejecutar el bucle `for i in range(1, 5): print(i)`, ¿qué valores se imprimen, uno por línea?",
      "opciones": {
        "a": "0, 1, 2, 3, 4",
        "b": "1, 2, 3, 4",
        "c": "1, 2, 3, 4, 5"
      },
      "respuesta_correcta": "b",
      "justificacion": {
        "evidencia_documental": "El documento define range(inicio, fin) como una secuencia que comienza en 'inicio' y termina en 'fin - 1', sin incluir el límite superior.",
        "razon_respuesta_correcta": "range(1, 5) genera 1, 2, 3 y 4: empieza en el valor inicial 1 y se detiene antes de 5.",
        "nivel_cognitivo_evaluado": "Aplicar",
        "concepto_principal": "Límites de la función range() con inicio y fin explícitos",
        "error_comun_evaluado": "Confusión sobre la inclusión del límite superior y el valor de inicio",
        "analisis_distractores": {
          "a": { "tipo_error": "Error conceptual", "explicacion": "Asume que range() siempre comienza en 0, ignorando el inicio explícito de 1." },
          "c": { "tipo_error": "Error procedimental", "explicacion": "Incluye el límite superior 5, error de 'off-by-one' al suponer que el valor final forma parte de la secuencia." }
        }
      }
    },
    {
      "id": 2,
      "tema": "Slicing de listas",
      "dificultad": "Alta",
      "nivel_bloom": "Aplicar",
      "enunciado": "Dada la lista `lista = [1, 2, 3, 4, 5]`, ¿qué resultado devuelve la expresión `lista[1:4]`?",
      "opciones": {
        "a": "[1, 2, 3]",
        "b": "[1, 2, 3, 4]",
        "c": "[2, 3, 4]",
        "d": "[2, 3, 4, 5]"
      },
      "justificacion_4_opciones": "El slicing lista[1:4] admite cuatro interpretaciones erróneas naturales y distintas según el modelo mental del estudiante sobre los índices (base 0 frente a base 1) y la inclusión del índice final (exclusivo frente a inclusivo). Cada modelo produce una de las cuatro opciones, por lo que el cuarto distractor tiene valor discriminativo real y no es relleno.",
      "respuesta_correcta": "c",
      "justificacion": {
        "evidencia_documental": "El documento establece que en lista[inicio:fin] los índices empiezan en 0 y el índice 'fin' es exclusivo.",
        "razon_respuesta_correcta": "lista[1:4] toma los elementos de los índices 1, 2 y 3 (valores 2, 3 y 4), deteniéndose antes del índice 4.",
        "nivel_cognitivo_evaluado": "Aplicar",
        "concepto_principal": "Índices base 0 y límite superior exclusivo en el slicing",
        "error_comun_evaluado": "Confusión combinada entre el origen de los índices y la inclusión del índice final",
        "analisis_distractores": {
          "a": { "tipo_error": "Error conceptual", "explicacion": "Interpreta los índices como base 1 y el final como exclusivo, devolviendo los tres primeros valores." },
          "b": { "tipo_error": "Error conceptual", "explicacion": "Interpreta los índices como base 1 e incluye el índice final, tomando las 'posiciones' 1 a 4." },
          "d": { "tipo_error": "Error procedimental", "explicacion": "Aplica bien la base 0 pero incluye el índice final 4 (valor 5), error de 'off-by-one' en el límite superior." }
        }
      }
    }
  ]
}
```