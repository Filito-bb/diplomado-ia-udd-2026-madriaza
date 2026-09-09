**SOBREMESA**

*El Mediador Digital de Presencia para Vínculos Reales*

Análisis experto UX/UI y plan de proyecto

Preparado para: Equipo del proyecto Sobremesa

Fecha: 20 de agosto de 2026

Documento base: ficha\_proyecto.md · Dataset de referencia: ScreenTime\_vs\_MentalWellness.csv (n=400)

# **1\. Análisis experto del proyecto**

## **1.1 Diagnóstico del enfoque**

**Sobremesa** parte de un diagnóstico correcto y, dentro del panorama de soluciones para la desconexión en la mesa, poco explorado: el problema no es el tiempo de pantalla en sí, sino la ausencia de mediación intencionada durante el tiempo compartido. La ficha identifica con precisión el fracaso de dos aproximaciones previas — la prohibición estricta (que genera rechazo y no cambia el hábito subyacente) y los juegos analógicos impresos (que imponen una fricción logística que termina abandonándose) — y propone una tercera vía: convertir el propio dispositivo que causa la distracción en el instrumento que la resuelve. Esta inversión del rol del smartphone es conceptualmente sólida y coherente con cómo funciona realmente el cambio de hábitos: es más sostenible rediseñar el estímulo que pedirle fuerza de voluntad al usuario.

El pipeline combinado (analítico \+ generativo) es una decisión de arquitectura acertada. El componente analítico — que clasifica edad, vínculo y nivel de confianza de los comensales — es el que permite que el sistema sea **prudente** antes que creativo: sin esa capa, cualquier generador de preguntas corre el riesgo de introducir un tema incómodo en el peor momento posible. Esa secuencia (primero entender la mesa, luego proponer) es la que separa a Sobremesa de un simple generador de preguntas aleatorias.

## **1.2 Validación con datos: por qué “estar juntos” no basta**

Se analizó el dataset *ScreenTime\_vs\_MentalWellness.csv* (400 personas, con horas de pantalla, horas sociales semanales, estrés e índice de bienestar mental) para contrastar la premisa del proyecto contra evidencia observable. Los resultados respaldan de forma directa la tesis central de Sobremesa:

* **El tiempo social por sí solo no predice bienestar.** Al segmentar a las personas en terciles de horas sociales semanales (bajo/medio/alto), el índice de bienestar promedio apenas varía: 20,1 / 18,9 / 22,0 sobre 100\. Pasar más horas rodeado de otros no mejora el bienestar de manera consistente.

* **El tiempo de pantalla sí lo predice, y con fuerza.** Al segmentar por terciles de horas de pantalla diarias, el bienestar promedio cae de forma pronunciada: 36,5 (bajo) → 16,4 (medio) → 7,8 (alto). La correlación lineal entre horas de pantalla y bienestar es de −0,64 sobre el total de la muestra.

* **El hallazgo más relevante para el proyecto:** incluso dentro del grupo con más horas sociales a la semana, la pantalla sigue perjudicando el bienestar con fuerza casi idéntica (correlación de −0,70 entre pantalla y bienestar en ese subgrupo). Es decir, compartir mesa con otras personas no protege del efecto de la pantalla si esta acapara la atención durante ese tiempo compartido.

Este patrón es evidencia a favor del posicionamiento de Sobremesa frente a alternativas de “solo reunir gente” o “solo prohibir el celular”: el factor que mueve el bienestar no es la copresencia física, sino qué ocurre con la atención mientras se está junto a otros. Un mediador que redirige esa atención hacia la conversación — en lugar de simplemente sacar el teléfono de la mesa — ataca la variable correcta según los propios datos.

Dicho esto, el dataset no mide conversación cara a cara ni presencia atencional directamente — mide horas sociales autorreportadas y un índice compuesto de bienestar — por lo que esta lectura es una inferencia razonable, no una prueba causal del efecto específico de Sobremesa. Conviene que el equipo lo trate como hipótesis de diseño a validar con datos propios una vez exista un prototipo, no como un hecho ya demostrado.

## **1.3 Vacíos de diseño no resueltos en la ficha actual**

Un análisis que no señale lo que falta es un análisis incompleto. La ficha, en su estado actual, deja sin resolver cuatro decisiones que condicionan cualquier trabajo posterior de interfaz:

1. **¿Cómo se obtiene la composición de la mesa?** El modelo analítico necesita edad, vínculo y nivel de confianza de los comensales, pero el documento no especifica el mecanismo de captura. Si es sensado (cámara o micrófono), el proyecto adquiere una carga de privacidad considerable — especialmente si hay menores de edad en la mesa, como contempla el propio dataset de referencia (edades desde 16 años) — que no está mencionada en ningún punto de la ficha. Si es autorreportado por el usuario al inicio, se reintroduce exactamente la fricción de configuración que el proyecto busca eliminar. Esta decisión debe tomarse antes de diseñar cualquier pantalla, porque determina la primera interacción completa del producto.

2. **¿Cuándo y cómo se retira el mediador?** La ficha describe cómo el sistema debe iniciar y guiar la conversación, pero no cómo debe salir de ella. Sin un mecanismo explícito de retirada, el diseño corre el riesgo de convertir el celular en un tercer comensal permanente — reemplazando la distracción por notificaciones por la distracción por una interfaz conversacional igualmente atractiva. Este punto se retoma como pilar de diseño en la sección 2\.

3. **Tensión entre la métrica de éxito declarada y un eventual modelo de negocio.** Las notas para Mauricio son explícitas: el éxito no se mide por retención en pantalla. Es un norte correcto, pero también significa que las métricas estándar de producto digital (tiempo en app, DAU, retención) no sirven para evaluar Sobremesa y, peor aún, optimizar por ellas activamente saboteraría el propósito del proyecto. Esto no invalida el proyecto, pero sí obliga a definir desde ya una métrica de éxito alternativa y medible (por ejemplo, tiempo entre interacciones con la pantalla, o frecuencia de reutilización de la mesa sin necesidad de reactivar el mediador) antes de la fase de prototipado.

4. **Dependencia de proveedores de modelos como decisión de arquitectura, no de contenido.** Los modelos candidatos listados (GPT-4o / Claude 3.5 Sonnet, Nano Banana, Veo 3\) son una fotografía de un momento específico del mercado de IA generativa, que cambia de versión cada pocos meses. Conviene que la ficha trate el modelo de lenguaje como un componente intercambiable detrás de una capa de abstracción propia, y no como una elección fija — de lo contrario cada actualización de roadmap arrastrará una revisión de arquitectura innecesaria.

## **1.4 Recomendaciones concretas**

* Definir explícitamente el mecanismo de captura de contexto de mesa (edad, vínculo, confianza) como una decisión de producto propia, con consentimiento visible y un modo por defecto conservador cuando el sistema no tiene certeza sobre quién está sentado a la mesa.

* Diseñar el “apagado” del mediador con la misma atención que su encendido: la interfaz debe poder ceder el protagonismo a la conversación humana de forma natural, no solo cuando el usuario la cierra manualmente.

* Incorporar un modo restringido automático cuando se detecta (o se declara) la presencia de menores de edad, limitando la profundidad emocional de los detonadores conversacionales.

* Establecer una métrica de éxito propia y medible antes de la Clase 25 (system prompt), de modo que el diseño conversacional se pueda evaluar contra algo distinto al tiempo de uso.

* Tratar el modelo de lenguaje como componente reemplazable, versionando el system prompt de forma independiente al modelo subyacente.

# **2\. Los 3 pilares esenciales de la interfaz**

A partir del análisis anterior, el correcto funcionamiento de Sobremesa depende de tres pilares no negociables. Los tres están vinculados: si falta uno, los otros dos pierden sentido.

## **Pilar 1 — Fricción cognitiva y física cero**

La interfaz debe poder usarse sin configuración previa, sin inicio de sesión durante la comida y sin que nadie tenga que “aprender” a usarla. Esto significa tipografía legible a distancia de mesa, brillo de pantalla adaptado a un ambiente social (sin “destellos molestos”, en palabras de la propia ficha), y una única acción de inicio — apoyar o mostrar el teléfono es suficiente, no hace falta navegar menús. Cada paso adicional de configuración es, estadísticamente, una oportunidad de abandono: es precisamente la razón por la que fracasaron los juegos analógicos impresos que Sobremesa busca reemplazar.

## **Pilar 2 — Inteligencia contextual con privacidad por diseño**

La capa analítica que adapta tono y profundidad según edad, vínculo y confianza solo aporta valor si es prudente por defecto: debe empezar con detonadores livianos y escalar la profundidad emocional únicamente cuando el grupo lo permite, nunca al revés. Esto no es solo un principio ético — es un principio de producto: una sola pregunta fuera de lugar (un tema doloroso frente a un desconocido, una pregunta demasiado íntima frente a un menor de edad) rompe la confianza en el mediador de forma permanente. La privacidad y la prudencia conversacional son, en este producto, la misma cosa vista desde dos ángulos.

## **Pilar 3 — Auto-desvanecimiento progresivo**

El indicador de éxito de una interacción no es que las personas se queden mirando el teléfono más tiempo, sino que dejen de necesitarlo. La interfaz debe estar diseñada para retirarse activamente: lanzar un detonador, y luego “apagarse” visualmente (oscurecerse, minimizarse) mientras dura la conversación que generó, en vez de esperar una respuesta o mostrar una siguiente pregunta de inmediato. Ningún elemento de la interfaz debe imitar mecánicas de retención (rachas, notificaciones, scroll infinito de preguntas) — eso reproduciría exactamente el patrón de enganche que el proyecto busca revertir.

# **3\. Los 3 principales problemas al desarrollar la aplicación**

## **Problema 1 — Captar el contexto de la mesa sin fricción ni vigilancia**

El Pilar 2 exige conocer edad, vínculo y confianza de los comensales, pero el Pilar 1 prohíbe pedirles que llenen un formulario. Estos dos pilares están en tensión directa y no existe, hoy, una solución evidente: sensar la mesa con cámara o micrófono resuelve la fricción pero introduce un problema serio de privacidad y de cumplimiento normativo (especialmente con menores presentes), mientras que pedir el dato manualmente resuelve la privacidad pero reintroduce la fricción de configuración que hundió a los juegos de mesa analógicos. El equipo deberá decidir explícitamente en qué punto de este espectro se ubica el producto, y diseñar el resto de la experiencia en función de esa decisión — no como un detalle técnico a resolver después, sino como la primera decisión de arquitectura del proyecto.

## **Problema 2 — Latencia y el “fantasma en la mesa”**

Un pipeline generativo en tiempo real necesita generar contenido (texto, y potencialmente una tarjeta visual) en el momento. Si esa generación toma más de uno o dos segundos, el resultado es exactamente la escena que el proyecto quiere evitar: varias personas mirando en silencio una pantalla que está “pensando”. Esto es más grave que un problema técnico de rendimiento — es un problema de diseño de experiencia, porque cada segundo de espera reproduce el gesto físico (cabeza baja, ojos en el teléfono) que Sobremesa fue creado para interrumpir. La solución probablemente combine generación anticipada (precalcular detonadores probables antes de que se necesiten) con contenido de respaldo pregenerado para los primeros segundos de cada mesa, pero es un problema de sistema que debe resolverse antes de comprometer una arquitectura 100% generativa en tiempo real.

## **Problema 3 — La paradoja de la métrica de éxito y el modelo de sostenibilidad**

Sobremesa mide su éxito por la desconexión de la pantalla, no por la permanencia en ella. Esto es correcto desde la psicología social y vincular, pero deja abierta una pregunta de sostenibilidad: ¿cómo se financia o se justifica institucionalmente un producto digital cuyo objetivo explícito es que se use lo menos posible? Los modelos de negocio habituales de una app (publicidad, suscripción ligada a uso, datos de comportamiento) empujan en la dirección opuesta a la misión del producto. Ignorar esta tensión no la elimina; solo la pospone hasta un punto del desarrollo donde corregirla es más costoso. Conviene resolverla — aunque sea de forma preliminar — al mismo tiempo que se define la arquitectura del producto, no después de construirlo.

# **4\. Carta Gantt del proyecto**

La planificación del proyecto para las 3 semanas asignadas se entrega en el archivo Excel adjunto (**sobremesa\_carta\_gantt.xlsx**, hoja “Carta Gantt”), con 11 tareas distribuidas en 15 días hábiles y 5 fases. El resumen de fases es el siguiente:

| Fase | Días | Objetivo principal |
| :---- | :---- | :---- |
| Descubrimiento | Día 1 – 5 | Investigar, sintetizar el dataset y el benchmark, definir los 3 pilares y trazar la arquitectura de información y los flujos de usuario. |
| Sistema visual | Día 6 – 7 | Cerrar la paleta, tipografía y componentes definitivos, coherentes con el Pilar 1 (fricción cero, sin destellos). |
| Prototipado | Día 8 – 10 | Construir wireframes de las pantallas clave y un prototipo interactivo de alta fidelidad navegable. |
| Validación | Día 11 – 13 | Probar el prototipo en mesas piloto reales y ajustar la interfaz según los hallazgos. |
| Cierre | Día 14 – 15 | Documentar especificaciones para desarrollo y presentar la entrega final. |

Cada tarea del Gantt indica día de inicio, duración, responsable(s) asignados entre las tres diseñadoras (D1 – enfoque UX e investigación, D2 – enfoque visual, D3 – enfoque de contenido conversacional y documentación) y horas estimadas, para permitir su vínculo directo con la estructura de costos de la sección 5\.

# **5\. Estructura de costos**

El detalle completo, con fórmulas vinculadas a la Carta Gantt, está en la hoja “Estructura de Costos” del mismo archivo Excel. El resumen ejecutivo es el siguiente, para un equipo de 3 diseñadoras gráficas profesionales durante 3 semanas:

| Concepto | Base de cálculo | Costo |
| :---- | :---- | :---- |
| Horas de diseño (11 tareas) | 296 horas-persona × $25.000 CLP/hora | $7.400.000 CLP |
| Licencias Figma Professional | 3 editoras × US$15/mes × 0,75 mes | $31.050 CLP |
| Contingencia | 10% del subtotal de horas de diseño | $740.000 CLP |
| Costo total del proyecto | — | $8.171.050 CLP |

**Supuestos declarados:** la tarifa de $25.000 CLP/hora corresponde al punto medio del rango de mercado para diseño gráfico profesional en Chile ($20.000–$60.000 CLP/hora, fuente: Cronoshare Chile, 2026); la jornada se calcula en 8 horas/día; el tipo de cambio referencial USD/CLP usado para las licencias de software es de 920 (20-08-2026). Las 296 horas de diseño representan un 82,2% de la capacidad máxima disponible del equipo (360 horas-persona en 3 semanas), dejando un margen deliberado para imprevistos por sobre la contingencia explícita del 10%.

# **6\. Benchmark actual**

El mercado de herramientas para conversación presencial se divide hoy en tres categorías, ninguna de las cuales ofrece lo que propone Sobremesa: adaptación en tiempo real al contexto específico de la mesa, generada de forma dinámica en lugar de un mazo fijo de preguntas.

| Producto / referencia | Categoría | Propuesta | Diferencia con Sobremesa |
| :---- | :---- | :---- | :---- |
| TableTopics (app y cartas físicas) | Mazo de preguntas | Banco fijo de preguntas por categoría (viajes, comida, cultura geek), navegable manualmente. | Contenido estático y genérico; no se adapta a quiénes están realmente en la mesa ni a su nivel de confianza. |
| We're Not Really Strangers (app y cartas) | Mazo de preguntas por niveles | Tres niveles progresivos (percepción, conexión, reflexión) que profundizan la intimidad de las preguntas a medida que avanza el juego. | La progresión de profundidad es igual para cualquier grupo; no distingue edad ni el tipo de vínculo real entre los comensales, y requiere que alguien sostenga y opere activamente la app o el mazo. |
| DinnerCall y apps similares de “cena en familia” | App social con detonadores | Combina preguntas de conversación con difusión social del momento en redes. | El componente de compartir en redes reintroduce la lógica de atención que Sobremesa busca eliminar de la mesa. |
| Cajas de bloqueo físico (p. ej. Yondr) y “zonas sin teléfono” (hooks, cargadores dedicados) | Fricción física / prohibición | Retiran físicamente el teléfono de la mesa durante la comida. | Es la aproximación de prohibición que la propia ficha identifica como generadora de rechazo; no ofrece ninguna guía activa para la conversación, solo remueve el estímulo. |
| Guías y chatbots de “cena sin dispositivos” (p. ej. contenido tipo Screenwise) | Contenido educativo | Listas estáticas de preguntas o consejos entregados fuera del momento de la comida (antes, no durante). | No es un mediador activo en tiempo real; es material de preparación, no una interfaz que opera durante la mesa. |

**Lectura del benchmark:** la categoría de mazos de preguntas (TableTopics, We're Not Really Strangers) es la más cercana en intención, pero todos comparten la misma limitación estructural: el contenido es fijo y no razona sobre quién está sentado a la mesa. El espacio que Sobremesa puede ocupar — un mediador que decide qué preguntar según la composición real del grupo, y que se retira activamente una vez que la conversación arranca — no tiene, hasta donde permite establecer esta búsqueda, un competidor directo hoy.

# **7\. Limitaciones temáticas: qué conversaciones aportan valor real**

No todo detonador conversacional es beneficioso solo por generar diálogo. Desde la psicología social y vincular, una conversación de mesa aporta valor cuando fortalece la confianza y la cercanía sin generar una carga emocional que el grupo no pidió ni puede sostener en ese momento. Esto exige que el sistema clasifique los temas posibles en tres niveles de riesgo, y que la capa analítica del Pilar 2 solo habilite los niveles más profundos cuando detecta señales claras de confianza y homogeneidad de edad en la mesa.

## **Temas de alto valor y bajo riesgo (uso por defecto)**

Los que generan curiosidad genuina sin exponer vulnerabilidades: recuerdos compartidos, anécdotas, preferencias, planes futuros, historia familiar liviana, aprendizajes recientes, opiniones sobre temas cotidianos. Es el nivel adecuado para mesas nuevas, mixtas en edad, o cuando el sistema no tiene certeza sobre el vínculo entre los comensales.

## **Temas de valor alto pero riesgo condicional (requieren señal de confianza y homogeneidad)**

Preguntas que invitan a la reflexión personal o a compartir emociones: miedos, decisiones importantes de vida, relaciones significativas, momentos de vulnerabilidad pasada. Aportan el tipo de cercanía que buscan mazos como We're Not Really Strangers, pero solo deben activarse cuando el sistema tiene evidencia razonable de que el grupo es homogéneo en edad adulta y existe un vínculo previo — nunca por defecto ante desconocidos o en presencia de menores.

## **Temas que el sistema debe evitar generar de forma proactiva**

Existe una categoría de temas donde el riesgo de daño supera el valor conversacional que un generador automático puede aportar de forma responsable, y que Sobremesa debería excluir de su generación espontánea — dejándolos, si acaso, a que surjan orgánicamente entre las personas, nunca sugeridos por el mediador:

* Finanzas personales del grupo (deudas, sueldos, herencias): genera comparación y tensión sin ningún beneficio vincular claro.

* Conflictos familiares no resueltos o rupturas recientes: el sistema no tiene forma de saber si un tema está efectivamente cerrado para todos los presentes.

* Duelo, pérdidas y salud (física o mental) de terceros: son temas que solo deben surgir por decisión explícita de las personas, nunca sugeridos por un algoritmo que no puede evaluar el estado emocional real de cada comensal.

* Política y temas de alta polarización social: el objetivo de la mesa es cohesión, no debate; introducir el tema activamente contradice el propósito del producto aunque genere conversación.

* Cualquier tema de contenido adulto o romántico cuando hay menores de edad en la mesa, incluso si el resto del grupo es adulto.

Esta clasificación no es una lista cerrada, sino el criterio con el que debe evaluarse cada detonador antes de incorporarlo al sistema generativo: un tema aporta valor real cuando profundiza un vínculo que las personas ya eligieron tener, no cuando simplemente llena el silencio.
