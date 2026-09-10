## Comparación de respuestas: Google Colab vs. NotebookLM

Para esta actividad se realizaron las mismas tres preguntas en Google Colab y NotebookLM, con el objetivo de comparar la manera en que ambas herramientas recuperan, relacionan y presentan la información disponible.

En Google Colab se cargó la ficha del proyecto y la base de datos. En NotebookLM se incorporaron esos mismos documentos y, además, el trabajo realizado durante la Clase 23. Por lo tanto, NotebookLM contó con una fuente adicional para elaborar sus respuestas.


## Cuadro comparativo

| Pregunta | Respuesta de Google Colab | Respuesta de NotebookLM | Análisis comparativo |
| --- | --- | --- | --- |
|   |   | Identificó al mismo público, pero profundizó en sus |   |
|   | Recuperó correctamente el apartado “Usuario / cliente | características, necesidades y problemas. Explicó que | Ambas herramientas encontraron información |
|   | objetivo” de la ficha del proyecto. Señaló de manera | buscan conexión real, que sufren distracciones por las | pertinente, pero Colab se limitó a mostrar un |
| ¿Cuál es el cliente objetivo? | general que corresponde a familias, parejas, grupos de | notificaciones y que no responden bien a soluciones | fragmento del documento. NotebookLM integró varias |
|   | amigos y compañeros de trabajo que se reúnen en | restrictivas. Además, relacionó el proyecto con | fuentes y elaboró una descripción más completa del |
|   | torno a la comida. | estudiantes, empleados y trabajadores remotos o | cliente objetivo. |
|   |   | híbridos. |   |
|   |   | Respondió directamente que sí y entregó datos | En esta pregunta se observa una diferencia |
|   | Entregó nuevamente el mismo fragmento sobre el | específicos. Indicó una correlación negativa de –0,64 | importante. Colab encontró un texto relacionado de |
|   | cliente objetivo. Aunque obtuvo una similitud de 0,39, | entre el tiempo de pantalla y el bienestar mental. | manera indirecta, pero no interpretó la intención de la |
| ¿Hay algo sobre el bienestar mental? | no respondió directamente si existía información | También comparó el promedio según ocupación: | pregunta. NotebookLM identificó la información |
|   | sobre bienestar mental. | estudiantes 15,54, empleados 20,19, trabajadores | específica, explicó su significado y comparó los |
|   |   | independientes 20,48, jubilados 31,58 y desempleados | resultados de distintas categorías. |
|   |   | 34,27. |   |
|   |   | Respondió que existen 107 estudiantes en el conjunto | Colab no logró localizar el dato numérico y repitió la |
|   | Volvió a mostrar el apartado “Usuario / cliente | de datos. También señaló que corresponden al | misma respuesta anterior. NotebookLM respondió de |
| ¿Cuántos estudiantes hay? | objetivo”, con una similitud de 0,47, pero no entregó el | segundo grupo más numeroso, después de los | forma precisa y agregó contexto para comprender la |
|   | número solicitado. | empleados, y que presentan el promedio de bienestar | relevancia de ese grupo dentro del conjunto de datos. |
|   |   | mental más bajo: 15,54 sobre 100. |   |


## Análisis general

La comparación evidencia que Google Colab entregó resultados más genéricos y repetitivos. En las tres preguntas seleccionó el mismo apartado de la ficha del proyecto: “Usuario / cliente objetivo”. Esto permitió responder parcialmente la primera pregunta, pero no fue suficiente para responder las otras dos.

En este caso, Colab operó principalmente como un sistema de recuperación por similitud: buscó el fragmento de texto matemáticamente más cercano a cada pregunta y lo mostró como resultado. Sin embargo, no interpretó completamente la intención de las consultas ni combinó información proveniente de diferentes partes de los documentos. Por esta razón, aunque las puntuaciones de similitud fueron distintas —0,59, 0,39 y 0,47—, el fragmento recuperado fue prácticamente el mismo.

NotebookLM, en cambio, entregó respuestas más específicas, desarrolladas y contextualizadas. No se limitó a encontrar un fragmento similar, sino que relacionó la ficha del proyecto con la base de datos y el material de la Clase 23. Esto le permitió responder directamente, incorporar cifras concretas y establecer comparaciones entre diferentes grupos.


## Conclusión

A partir de esta prueba, NotebookLM presentó un mejor desempeño para consultar y analizar los documentos del proyecto. Sus respuestas fueron más precisas, detalladas y comparativas, especialmente en las preguntas relacionadas con el bienestar mental y la cantidad de estudiantes.

Google Colab entregó una respuesta básica que resultó útil para identificar el cliente objetivo, pero su configuración actual no logró profundizar ni encontrar datos específicos. Esto no significa necesariamente que Colab tenga menos capacidades, sino que el sistema de búsqueda implementado necesita mejoras, como recuperar más de un fragmento, buscar directamente en la base de datos y utilizar un modelo que interprete los resultados antes de generar la respuesta.

Además, la comparación no fue completamente equivalente, porque NotebookLM contó con el material adicional de la Clase 23. Para realizar una prueba más controlada, sería conveniente cargar exactamente las mismas fuentes en ambas herramientas y repetir las tres preguntas.


## Hallazgo principal

NotebookLM comprendió, relacionó y explicó la información, mientras que Colab se limitó a recuperar el fragmento con mayor similitud.


## Cierre del informe

Esta actividad permitió comparar cómo Google Colab y NotebookLM trabajan con la información de un mismo proyecto. Los resultados muestran que la calidad de las respuestas no depende solamente de los documentos cargados, sino también de la forma en que cada herramienta busca, interpreta y relaciona su contenido.

En la configuración utilizada, Google Colab recuperó fragmentos según su nivel de similitud con las preguntas, pero repitió la misma información y no respondió de manera precisa en todos los casos. NotebookLM, en cambio, integró distintas fuentes, identificó datos específicos y entregó respuestas más completas, explicativas y comparativas.

Como aprendizaje, se concluye que NotebookLM resultó más adecuado para explorar y comprender la información del proyecto Sobremesa, mientras que el sistema desarrollado en Colab necesita ajustes para mejorar la recuperación e interpretación de los datos. Entre estas mejoras se podría incorporar la búsqueda de varios fragmentos relevantes y la generación de una respuesta final que sintetice la información encontrada.

Finalmente, esta comparación permitió comprender que una herramienta de inteligencia artificial no solo debe encontrar información relacionada, sino también responder directamente a la pregunta, conectar diferentes datos y comunicar los resultados de manera clara y contextualizada.
