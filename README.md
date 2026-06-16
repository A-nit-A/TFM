# TFM
Proyecto fin de máster.

## Estructura del Repositorio

El repositorio está organizado en las siguientes secciones:

### 1. Apuntes del Curso de Python
En el directorio [Curso Python](./Curso%20Python) se encuentran los apuntes y materiales de estudio sobre el lenguaje de programación Python:

* **[Introducción a Python](./Curso%20Python/Introducción.md)**: Introducción al lenguaje, ejecución del intérprete interactivo, módulos, funciones definidas por el usuario, reglas de sangría y herramientas de ayuda integrada (`help()` y `dir()`).
* **[Cadenas en Python](./Curso%20Python/Cadenas.md)**: Trabajo con cadenas (`str`), inmutabilidad, indexación, métodos de cadena comunes (como `lower`, `split`, `join`), formateo de cadenas (f-strings) y condicionales `if`.
* **[Listas en Python](./Curso%20Python/Listas.md)**: Uso de listas (`list`), bucles `for ... in` e `while`, rebanado (slicing) de listas y métodos de lista estándar (como `append`, `extend`, `sort`, `pop`).
* **[Ordenamiento en Python](./Curso%20Python/Ordenar.md)**: Métodos y funciones para ordenar colecciones (`sorted()`, `sort()`), ordenamiento personalizado usando funciones clave (`key=`), uso de tuplas y comprensiones de listas.
* **[Diccionarios y Archivos en Python](./Curso%20Python/Diccionarios_Archivos.md)**: Uso de diccionarios (tablas hash `dict`), formateo con diccionarios, operador `del`, manejo de lectura y escritura de archivos (incluso en Unicode), y consejos para desarrollo incremental.
* **[Expresiones Regulares en Python](./Curso%20Python/ExpresionesRegulares.md)**: Introducción al módulo `re`, patrones básicos, metacaracteres, repeticiones codiciosas y no codiciosas, extracción de grupos con `search()` y `findall()`, y sustituciones con `sub()`.
* **[Utilidades en Python](./Curso%20Python/Utilidades.md)**: Uso de módulos estándar como `os` y `shutil` para interactuar con el sistema de archivos, ejecución de procesos externos con `subprocess`, manejo básico de excepciones (`try/except`) y consultas HTTP con `urllib.request`.

### 2. Prompts
En el directorio [Prompts](./Prompts) se almacenan las plantillas e instrucciones de prompts utilizadas para guiar a los modelos de lenguaje:
* **[Prompt #2](./Prompts/Pormpt%232.md)**: Especificación de prompt para la generación estructurada de preguntas de examen en formato JSON (metadatos, temas, dificultad y justificaciones).
* **[Prompt #3](./Prompts/Pormpt%233.md)**: Instrucciones detalladas de generación de exámenes basadas en el protocolo de fidelidad al contexto, representatividad y ajuste psicométrico, con 3 opciones de respuesta.
* **[Prompt #4](./Prompts/Pormpt%234.md)**: Extensión del Prompt #3 que incorpora la aleatorización de la respuesta correcta mediante el método de puntos de corte y la prioridad de 3 opciones de respuesta.
* **[Prompt #5](./Prompts/Prompt%235.md)**: Plantilla adaptada para la generación de exámenes estructurados en JSON, con directrices para materias de ciencias/programación y humanidades, y clasificación por dificultad basada en la taxonomía de Bloom.
* **[Prompt #6](./Prompts/Pormpt%236.md)**: Prompt avanzado en formato JSON que incluye cobertura temática equilibrada, evitación de redundancias, validación técnica de código/fórmulas y auditoría detallada de distractores.

### 3. Exámenes / Tests
En el directorio [Tests](./Tests) se guardan los exámenes y cuestionarios autogenerados:
* **[Cadenas #1 - Gemini](./Tests/Cadenas_%231_Gemini.md)**: Examen de 10 preguntas de opción múltiple generado por el modelo Gemini basado en el capítulo de Cadenas de Python.
* **[Cadenas #1 - GPT](./Tests/Cadenas_%231_GPT.md)**: Examen de 10 preguntas de opción múltiple generado por el modelo GPT basado en el capítulo de Cadenas de Python.
* **[Diccionarios y Archivos #5 - Gemini](./Tests/Diccionarios_Archivos%235_Gemini.md)**: Cuestionario de 10 preguntas de opción múltiple en formato JSON generado por el modelo Gemini basado en el capítulo de Diccionarios y Archivos de Python.
