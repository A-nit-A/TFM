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