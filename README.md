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
En el directorio [Prompts](./Prompts) se almacenan las plantillas e instrucciones de prompts organizadas en las siguientes fases:

* **[Evolución del Prompt](./Prompts/Evolución)**: Documenta el desarrollo incremental y la evolución del generador de prompts generales.
  * Contiene los prompts históricos del 1 al 8 ([Prompt #1](./Prompts/Evolución/Prompt%231.md) a [Prompt #8](./Prompts/Evolución/Prompt%238.md)), la [Guía de Creación de Materia](./Prompts/Evolución/GuiaCrearMateria.md), el [Prompt Kernel](./Prompts/Evolución/Prompt_Kernel.md) y configuraciones específicas por materia ([Matemáticas](./Prompts/Evolución/Prompt_Materia_Matematicas.md) y [Python 3](./Prompts/Evolución/Prompt_Materia_Python_3.md)).
* **[Encuesta Docente](./Prompts/Encuesta)**: Prompts específicos adaptados para la generación estructurada de 5 preguntas orientadas a la evaluación y encuesta docente en Python para diferentes modelos de lenguaje:
  * **[Python Completo (5 preguntas)](./Prompts/Encuesta/Prompt_Python_Completo_5_preguntas.md)**: Plantilla base completa para la generación.
  * **[ChatGPT](./Prompts/Encuesta/Prompt_Python_ChatGP_5_preguntas.md)**: Prompt adaptado para OpenAI ChatGPT.
  * **[Claude 4.6 Opus](./Prompts/Encuesta/Prompt_Python_Claude_4_6_Opus_5_preguntas.md)**: Prompt adaptado para Anthropic Claude.
  * **[Gemini 3.5 Flash](./Prompts/Encuesta/Prompt_Python_Gemini_3_5_Flash_5_preguntas.md)**: Prompt adaptado para Google Gemini.
  * **[Mistral 3.5 Medium](./Prompts/Encuesta/Prompt_Python_Mistral_3_5_Medium.md)**: Prompt adaptado para Mistral.

### 3. Exámenes / Tests
En el directorio [Tests](./Tests) se guardan los exámenes y cuestionarios autogenerados:

* **[Evolución del Prompt](./Tests/Evolución%20prompt)**: Exámenes generados durante la fase de evolución del prompt general:
  * **[Cadenas (Claude)](./Tests/Evolución%20prompt/Cadenas_%231_Claude.md)**
  * **[Cadenas (Gemini)](./Tests/Evolución%20prompt/Cadenas_%231_Gemini.md)**
  * **[Cadenas (GPT)](./Tests/Evolución%20prompt/Cadenas_%231_GPT.md)**
  * **[Diccionarios y Archivos (Gemini)](./Tests/Evolución%20prompt/Diccionarios_Archivos%235_Gemini.md)**
* **[Encuesta Docente](./Tests/Encuesta)**: Cuestionarios generados a partir de los prompts específicos para la encuesta docente en formato JSON, organizados por modelo de lenguaje:
  * **ChatGPT (5.5)**: [Cadenas (nombrado Cademas)](./Tests/Encuesta/ChatGPT_5_5/Cademas.json) y [Diccionarios](./Tests/Encuesta/ChatGPT_5_5/Diccionarios.json).
  * **Claude 4.6 Opus**: [Cadenas](./Tests/Encuesta/Claude_4_6_Opus/Cadenas.json) y [Diccionarios](./Tests/Encuesta/Claude_4_6_Opus/Diccionarios.json).
  * **Gemini 3.5 Flash**: [Cadenas](./Tests/Encuesta/Gemini_3_5_flash/Cadenas.json).
  * **Mistral 3.5 Medium**: [Cadenas](./Tests/Encuesta/Mistral_3_5_Medium/Cadenas.json), [Diccionarios](./Tests/Encuesta/Mistral_3_5_Medium/Diccionarios.json), [Expresiones Regulares](./Tests/Encuesta/Mistral_3_5_Medium/ExpresionesRegulares.json) y [Utilidades](./Tests/Encuesta/Mistral_3_5_Medium/Utilidades.json).
