**ESTRATEGIA DE PRODUCTO · EXPERIENCIA PRESENCIAL · IA RESPONSABLE**

# **SOBREMESA**

## *Análisis crítico, experiencia de usuario, viabilidad y planificación de un mediador digital para conversaciones cara a cara*

Proyecto: Sobremesa — El Mediador Digital de Presencia para Vínculos Reales.

Equipo considerado: tres diseñadoras gráficas profesionales. Horizonte: tres semanas / quince días hábiles.

Insumos revisados: ficha del proyecto, ScreenTime vs MentalWellness.csv y ScreenTime vs MentalWellness.xlsx.

Fecha de análisis: 20 de agosto de 2026\.

**TESIS DEL PROYECTO**  El éxito no debe medirse por permanencia en la aplicación, sino por la capacidad de iniciar una conversación presencial pertinente y devolver la atención a las personas.

# **Resumen ejecutivo**

Sobremesa identifica una oportunidad de diseño concreta: transformar el teléfono presente en una comida en un activador breve de conversación, en vez de competir por la atención de quienes comparten la mesa. La propuesta es pertinente, pero su ficha actual mezcla una intuición de diseño valiosa con afirmaciones que todavía no están demostradas, una audiencia demasiado amplia y una arquitectura tecnológica sobredimensionada para un equipo de tres diseñadoras y un plazo de tres semanas.

El dataset analizado contiene 400 registros y describe asociaciones entre tiempo de pantalla, sueño, estrés, productividad, horas sociales y un índice de bienestar mental. Dentro de esta muestra, mayor tiempo total de pantalla se asocia con menor bienestar; sin embargo, las horas sociales semanales casi no se asocian linealmente con ese índice. Por tanto, la base sirve para contextualizar la sobreexposición digital, pero no demuestra que conversar durante una comida mejore la salud mental ni que la aplicación produzca un efecto terapéutico.

La recomendación central es construir y validar un prototipo mobile-first que use un dispositivo compartido, presente una pregunta abierta a la vez, permita regular la profundidad y desaparezca de la interacción mientras las personas conversan. La inteligencia artificial, si se utiliza, debe complementar una biblioteca editorial curada y quedar subordinada a reglas de seguridad, consentimiento y privacidad.

# **1\. Alcance y evaluación de los insumos**

## **1.1. Qué define realmente la ficha del proyecto**

La ficha define como usuarios posibles a familias, parejas, amistades y compañeros de trabajo que comparten almuerzos, cenas u once. Propone combinar una capa analítica para interpretar composición de la mesa, vínculo y confianza, con una capa generativa para producir detonadores conversacionales y microdesafíos. También menciona modelos de texto, generación visual y video conceptual, además de un roadmap académico por clases.

La intención declarada es coherente: facilitar presencia y conversación. Sin embargo, la ficha no identifica todavía un segmento inicial prioritario, no define qué significa una conversación valiosa, no aporta una línea base observada, no describe salvaguardas para menores ni diferencia entre prototipo académico, MVP técnico y aplicación productiva.

## **1.2. Calidad técnica de los archivos entregados**

* **CSV utilizable.** Contiene 400 registros, 15 variables útiles y una columna adicional vacía. Tras eliminar exclusivamente esa columna vacía, las 15 variables relevantes no presentan datos faltantes.  
* **Excel defectuoso.** Contiene también 400 filas, pero los encabezados y cada registro aparecen concatenados en una sola columna separada por comas. No constituye una tabla analítica correctamente importada y no debe procesarse como si sus variables estuvieran separadas.  
* **Control de consistencia.** El tiempo total de pantalla coincide exactamente, registro a registro, con la suma de pantalla laboral y pantalla recreativa. Esta consistencia valida esa relación aritmética, pero no demuestra el origen, la representatividad ni la confiabilidad externa del conjunto.  
* **Trazabilidad insuficiente.** No se entregaron ficha metodológica, país, fecha de levantamiento, método de muestreo, definición clínica del índice de bienestar ni instrumento psicométrico. Tampoco es posible verificar si los datos son reales, simulados o sintéticos.

## **1.3. Hallazgos comprobables del dataset**

| Indicador | Resultado | Interpretación responsable |
| :---- | :---- | :---- |
| Registros válidos | 400 | Muestra entregada; no equivale al universo de usuarios. |
| Edad observada | 16 a 60 años; promedio 29,78 | Incluye 18 personas menores de 18 años. |
| Estudiantes | 107 personas · 26,75 % | Subgrupo identificable; no corresponde al cliente objetivo completo. |
| Pantalla total diaria | 9,02 horas promedio | Suma de uso laboral y recreativo dentro de esta base. |
| Pantalla recreativa diaria | 6,84 horas promedio | Más relevante para distraibilidad que el tiempo laboral, sin probar uso durante comidas. |
| Bienestar mental | 20,33 / 100 promedio | El índice no tiene definición metodológica ni validez clínica verificable. |
| Estrés | 8,15 / 10 promedio | 135 personas presentan el valor máximo 10\. |
| Horas sociales semanales | 7,91 horas promedio | No miden conversación, calidad vincular ni comidas compartidas. |

*Fuente: cálculo propio sobre ScreenTime vs MentalWellness.csv, archivo entregado por la usuaria.*

## **1.4. Asociaciones y una conclusión que no conviene exagerar**

| Variables comparadas | r de Pearson | Lectura |
| :---- | :---- | :---- |
| Pantalla total ↔ bienestar | −0,636 | Asociación negativa moderada a alta en esta muestra. |
| Pantalla recreativa ↔ bienestar | −0,464 | Asociación negativa moderada; no identifica el momento de uso. |
| Pantalla laboral ↔ bienestar | −0,286 | Asociación negativa menor que la del uso recreativo. |
| Estrés ↔ bienestar | −0,914 | Asociación muy alta; posible solapamiento o construcción compartida del índice. |
| Calidad de sueño ↔ bienestar | \+0,750 | Asociación positiva alta; sin inferencia causal. |
| Horas sociales ↔ bienestar | \+0,070 | Asociación lineal prácticamente nula dentro de la base. |

*Correlaciones calculadas sobre 400 registros. Asociación no implica causalidad ni eficacia del producto.*

La comparación por cuartiles refuerza el patrón descriptivo: el grupo con menor exposición registra 5,90 horas de pantalla y 38,51 puntos promedio de bienestar; el grupo con mayor exposición registra 12,11 horas y 7,52 puntos. En paralelo, el estrés promedio pasa de 6,06 a 9,60. Estas diferencias pueden coexistir con otras variables y no autorizan a afirmar que reducir pantalla sea la causa del cambio ni que una conversación guiada produzca ese resultado.

El subgrupo estudiantil contiene 107 personas, con 10,33 horas promedio de pantalla y 15,54 puntos promedio de bienestar. Puede considerarse un segmento exploratorio si el equipo decide investigarlo, pero la ficha no lo establece como usuario principal y no corresponde desplazar sin evidencia a familias, parejas, amistades o compañeros de trabajo.

**HALLAZGO INCÓMODO, PERO CENTRAL**  La relación entre horas sociales y bienestar es r \= \+0,070. Defender que “más sociabilidad mejora el bienestar” usando esta base sería metodológicamente incorrecto. Lo que Sobremesa debe investigar es la calidad de la interacción, una variable que el dataset no mide.

# **2\. Análisis experto del proyecto y mejoras**

## **2.1. Problema de diseño: oportunidad real, causalidad no demostrada**

La formulación actual afirma que la hiperconexión “ha deteriorado” el ritual de comer juntos y que las alternativas analógicas se abandonan por fricción logística. Ambas ideas son plausibles, pero los archivos entregados no contienen observaciones, entrevistas ni experimentos que las confirmen. Deben presentarse como hipótesis de diseño para validar, no como hechos establecidos.

Una formulación más precisa sería: “Durante comidas compartidas, algunas personas perciben que el uso del teléfono y las notificaciones interrumpen la conversación. Sobremesa explora si una intervención digital breve, compartida y contextual puede facilitar preguntas presenciales relevantes sin aumentar la dependencia de la pantalla”.

## **2.2. Reducir la audiencia inicial para diseñar mejor**

Familias con menores, parejas, amigos y colegas no comparten normas de intimidad, jerarquías, riesgos ni expectativas. Diseñar una única experiencia indiferenciada aumenta la probabilidad de preguntas incómodas, lenguaje inadecuado o percepciones de invasión.

* **Foco inicial.** Escenario inicial recomendado: adultos que ya se conocen y comparten una comida; permite validar utilidad, ritmo y aceptación sin introducir todavía la complejidad de menores o jerarquías laborales.  
* **Segmentación progresiva.** Primera expansión: pareja, amistades y familia adulta como modos diferenciados; mantener una misma estructura de interacción con bibliotecas y límites específicos.  
* **Escenarios sensibles.** Familias con menores y equipos de trabajo deben considerarse modos especiales sujetos a reglas adicionales, no simples cambios de etiqueta.

## **2.3. Diseñar la pantalla para que deje de ser protagonista**

La principal contradicción de producto es intentar disminuir una distracción mediante el mismo dispositivo que la produce. La respuesta no debe consistir en una interfaz más entretenida, sino en reducir las interacciones necesarias y desplazar el valor fuera de la pantalla.

* Un teléfono compartido por mesa, sin exigir instalación o registro a todos los participantes.  
* Inicio breve con selección explícita de tipo de vínculo, presencia de menores y profundidad deseada.  
* Una sola pregunta legible por turno; sin feed, scroll infinito, chat con IA, puntos, rachas ni recompensas visuales.  
* Pantalla atenuada, modo silencioso sugerido —sin prometer control automático del sistema— y botón “siguiente” disponible solamente cuando el grupo decida continuar.  
* Opciones visibles y neutrales: cambiar pregunta, omitir tema, bajar profundidad, pausar y terminar.  
* Cierre optativo con una evaluación breve de utilidad percibida; nunca exigir responder para abandonar la experiencia.

## **2.4. Arquitectura de IA proporcional al problema**

La ficha propone un pipeline analítico y generativo, pero la información disponible no justifica entrenar un modelo predictivo. El dataset no contiene conversaciones, composición real de mesas, etiquetado de preguntas, respuestas emocionales, incidentes de seguridad ni preferencias por tipo de vínculo. Por ello, no es un conjunto válido para entrenar un clasificador de adecuación conversacional.

Para un prototipo de tres semanas, resulta más defendible utilizar reglas explícitas —edad, vínculo, profundidad y temas excluidos— junto con un banco de preguntas previamente curado. La generación con IA puede usarse como complemento controlado: producir variantes, pasar filtros temáticos y regresar a una pregunta aprobada si el resultado falla.

* Entrada mínima: tipo de mesa, grupo etario general, nivel de confianza elegido y temas que el grupo prefiere evitar.  
* Lógica analítica inicial: matriz de reglas y etiquetas editoriales; no perfilado psicológico ni inferencia de emociones.  
* Lógica generativa opcional: variante breve y abierta de una pregunta ya aprobada, con revisión de categorías prohibidas.  
* Fallback obligatorio: biblioteca local de preguntas seguras cuando no exista conexión, cuota de API o respuesta adecuada.  
* Privacidad: no activar micrófono, grabar conversaciones ni almacenar respuestas personales por defecto.  
* Modelos mencionados en la ficha: tratarlos como candidatos conceptuales aportados por el equipo, no como proveedores contratados, disponibles o presupuestados.

## **2.5. Definir éxito fuera de la lógica de retención**

Una aplicación de presencia no debería declarar éxito porque aumenta sesiones, minutos de pantalla o cantidad de tarjetas. Debe comparar si la herramienta inicia una conversación útil con una intervención digital breve y si el grupo mantiene la sensación de autonomía.

* Indicador principal propuesto: proporción de la sesión destinada a conversación presencial frente al tiempo de interacción con pantalla.  
* Indicadores complementarios: pertinencia percibida de la pregunta, facilidad de inicio, participación voluntaria, comodidad emocional y número de interrupciones atribuibles a la interfaz.  
* Indicadores de seguridad: preguntas omitidas por incomodidad, categorías bloqueadas, incidentes con menores y percepción de presión para responder.  
* Método inicial: observación consentida de pruebas, notas de facilitación y preguntas de salida; no espiar conversaciones ni prometer mediciones automáticas de contacto visual.

**CRITERIO CLAVE**  Estos indicadores son propuestas de evaluación. No existen mediciones previas ni objetivos numéricos entregados, por lo que sería improcedente inventar porcentajes de mejora, tasas de conversión o beneficios clínicos.

# **3\. Los tres pilares esenciales de la interfaz**

## **Pilar 1\. Presencia primero: mínima atención digital**

La interfaz existe para devolver la atención a la mesa. Debe facilitar un inicio breve, mostrar una pregunta comprensible y desaparecer del centro de la interacción. Su principio de diseño es que cada elemento visible justifique por qué necesita existir durante una comida compartida.

Se operacionaliza mediante teléfono compartido, navegación de un paso, tipografía legible, baja estimulación visual, ausencia de patrones adictivos y control manual del ritmo. Se valida observando cuánto tiempo exige mirar la pantalla y si la conversación continúa sin depender de nuevas instrucciones.

## **Pilar 2\. Pertinencia vincular: contexto, gradualidad y participación**

Una buena pregunta no es universal: depende del vínculo, la composición del grupo, la presencia de menores y la confianza disponible. La adaptación debe ser transparente, simple y elegida por las personas, no deducida mediante vigilancia o supuestos psicológicos.

Se operacionaliza con modos por tipo de mesa, niveles de profundidad progresivos y preguntas abiertas que favorezcan reciprocidad, escucha y participación voluntaria. El sistema no debe interpretar silencio como rechazo, presionar a una persona reservada ni medir quién “se abrió más”.

## **Pilar 3\. Seguridad conversacional: consentimiento, límites y privacidad**

La interfaz debe reducir la probabilidad de activar vergüenza, exposición, conflicto o situaciones impropias. Conversar con profundidad no equivale a exigir vulnerabilidad, y una experiencia de bienestar no debe presentarse como atención psicológica.

Se operacionaliza mediante exclusiones temáticas, opción de saltar sin explicación, lenguaje no acusatorio, modo seguro para menores, reglas particulares en contextos laborales y minimización de datos. Si surge una situación de riesgo o crisis, corresponde suspender la dinámica y recurrir a apoyo humano adecuado.

# **4\. Los tres principales problemas de desarrollo**

## **Problema 1\. La solución puede reproducir la distracción que pretende reducir**

Un onboarding extenso, una interfaz gamificada, notificaciones propias o una sucesión rápida de tarjetas trasladarían la atención desde las personas hacia el producto. El riesgo no es solamente estético: invalidaría la promesa central de Sobremesa.

Mitigación: flujo mínimo, un dispositivo compartido, ausencia de feed y rachas, intervenciones puntuales y medición de exposición real durante las pruebas. No basar el MVP en bloquear notificaciones del sistema operativo: estas funciones dependen de permisos y capacidades de plataforma que no están garantizadas.

## **Problema 2\. Preguntas inadecuadas, sesgos y exposición emocional**

Una pregunta apropiada entre amigos íntimos puede ser improcedente frente a un superior, a una familia con menores o a una pareja atravesando un conflicto. La generación abierta también puede reproducir supuestos sobre género, maternidad, religión, orientación sexual, estructura familiar o salud mental.

Mitigación: reglas por contexto, biblioteca curada, clasificación temática, consentimiento explícito para mayor profundidad, botón de omisión y validación humana. La aplicación no debe diagnosticar, recomendar tratamiento, sugerir separación, interrogar traumas ni pedir revelar información sensible.

## **Problema 3\. Alcance técnico desalineado con tiempo, equipo y evidencia**

Tres diseñadoras gráficas, en tres semanas, pueden investigar, definir contenido, diseñar una experiencia, construir un prototipo navegable y ejecutar pruebas iniciales. Ese alcance no equivale a desarrollar una aplicación segura en producción, integrar múltiples modelos, entrenar un clasificador, operar infraestructura, implementar protección robusta de menores y demostrar eficacia psicológica.

Mitigación: delimitar como resultado principal un prototipo validado y una arquitectura conceptual; separar mejoras futuras, desarrollo técnico e investigación longitudinal. Cualquier programación productiva, contratación de API, asesoría clínica o implementación de privacidad debe presupuestarse y contratarse aparte si realmente se decide realizarla.

# **5\. Plan de trabajo y carta Gantt de tres semanas**

La carta Gantt se entrega en un archivo Excel independiente y editable: Sobremesa\_Carta\_Gantt\_y\_Costos.xlsx. Está organizada en 15 días hábiles relativos porque no se proporcionó una fecha de inicio. Incluye 24 actividades, fase, duración, responsable, entregable y horas estimadas para cada diseñadora.

| Semana | Foco | Resultados esperados |
| :---- | :---- | :---- |
| Semana 1 · D1–D5 | Descubrimiento y definición | Auditoría de datos, benchmark, segmento inicial, journey, métricas y salvaguardas. |
| Semana 2 · D6–D10 | Contenido, arquitectura y diseño | Taxonomía, system prompt, wireframes, sistema visual, biblioteca curada y prototipo. |
| Semana 3 · D11–D15 | Validación, iteración y cierre | Pruebas moderadas, ajustes UX/UI, revisión de seguridad, video conceptual y entrega. |

Las horas consignadas son una estimación explícita de planificación, no tiempo efectivamente ejecutado ni una obligación contractual. Las actividades distribuyen responsabilidades entre investigación/estrategia, diseño UX/UI y contenido/seguridad. La visualización cambia automáticamente cuando se editan los días de inicio o término.

# **6\. Estructura de costos para tres diseñadoras profesionales**

## **6.1. Criterio: costear sin inventar tarifas**

No se informaron valores por hora, honorarios mensuales, costos de licencias, tarifas de APIs, gastos de participantes, impuestos ni condiciones de contratación. En consecuencia, entregar una cifra cerrada en pesos chilenos como si fuera real implicaría inventar datos. La estructura correcta es parametrizable y permite ingresar exclusivamente montos confirmados.

| Profesional | Responsabilidad principal | Base de cálculo |
| :---- | :---- | :---- |
| Diseñadora 1 | Investigación UX, estrategia, análisis de datos y validación. | Horas planificadas en Gantt × tarifa real acordada. |
| Diseñadora 2 | Arquitectura, sistema visual, interfaz y prototipo. | Horas planificadas en Gantt × tarifa real acordada. |
| Diseñadora 3 | Contenido, taxonomía, prompts y seguridad conversacional. | Horas planificadas en Gantt × tarifa real acordada. |

El Excel incorpora una hoja “Estructura de costos” vinculada directamente a las horas de la carta Gantt. Las tarifas por hora se dejan deliberadamente en blanco y destacadas como campos editables; el subtotal y el total se calculan solamente cuando se ingresan las tres tarifas.

## **6.2. Gastos directos posibles, no asumidos**

* Licencias adicionales de herramientas de diseño, únicamente si el equipo debe contratar alguna.  
* Consumo de modelos o APIs generativas, únicamente si se utilizan servicios pagados y existe un precio confirmado.  
* Incentivos o gastos de pruebas con participantes, únicamente cuando hayan sido aprobados.  
* Producción de un video conceptual, únicamente si requiere una herramienta o servicio adicional de pago.  
* Infraestructura o publicación, únicamente si se decide implementar y desplegar un producto real.

También se incluye una contingencia opcional, vacía por defecto. No se aplican impuestos, recargos ni porcentajes arbitrarios porque no fueron informados. El equipo puede completar estos parámetros y obtener un presupuesto trazable sin modificar las fórmulas.

# **7\. Benchmark actual y diferenciación competitiva**

Benchmark revisado el 20 de agosto de 2026 mediante sitios oficiales. Se distinguen competidores directos de conversación guiada, alternativas físicas y referentes adyacentes de presencia digital. La comparación identifica funcionalidades declaradas por cada organización; no presupone resultados clínicos ni experiencia interna de sus aplicaciones.

| Referente | Categoría | Propuesta observable | Aprendizaje para Sobremesa |
| :---- | :---- | :---- | :---- |
| Gottman Card Decks | App de preguntas para parejas | 14 mazos y más de 1.000 tarjetas; enfoque vincular. | Aprender curaduría; diferenciarse con mesa compartida y modos no exclusivamente de pareja. |
| Paired | App de relación de pareja | Preguntas, juegos y check-ins diarios; contenido guiado. | Evitar dependencia de uso diario y respuestas centradas en cada pantalla. |
| TableTopics Family | Tarjetas físicas familiares | 135 preguntas abiertas; uso explícito durante comidas. | Digitalizar el acceso y adaptar profundidad sin requerir materiales físicos. |
| We’re Not Really Strangers | Cartas y packs digitales | Progresión: percepción, conexión y reflexión. | Adoptar gradualidad, pero no forzar revelaciones ni sesiones extensas. |
| {THE AND} · The Skin Deep | Mazos físicos y digitales | Ediciones por vínculos y preguntas de conexión. | Tomar segmentación por relación; sumar reglas de seguridad y presencia. |
| The Family Dinner Project | Recursos y tarjetas imprimibles | Detonadores de conversación vinculados con la comida. | Reducir fricción de imprimir/recortar y mantener la pregunta como apoyo sutil. |
| Timeleft | Organización de encuentros presenciales | Facilita comidas y conexiones entre personas. | Aprender mediación fuera de pantalla; no confundir organización de cenas con conversación guiada. |
| one sec | Gestión de atención digital | Pausas intencionales y herramientas contra distracciones. | Incorporar intención y atención; no asumir bloqueo de otras apps como capacidad del MVP. |

*Fuentes: sitios oficiales de cada producto o iniciativa, listados completos al final del documento.*

## **7.1. Lectura estratégica del benchmark**

La idea de usar preguntas para fortalecer vínculos no es nueva. Tampoco lo son las tarjetas familiares, los mazos digitales ni las aplicaciones de pareja. Por lo tanto, Sobremesa no puede sustentar su diferenciación en “tener preguntas profundas”, “usar inteligencia artificial” o “ayudar a conectar”.

La oportunidad específica aparece en la intersección de cuatro atributos: contexto real de comida compartida, un solo dispositivo utilizado brevemente, adaptación transparente al vínculo y restricciones de seguridad que protejan a quienes participan. Esa combinación es una hipótesis de posicionamiento; debe validarse con usuarios y no presentarse como exclusividad comprobada de mercado.

**DIFERENCIACIÓN DEFENDIBLE**  Propuesta de valor recomendada: “Una pregunta adecuada, en el momento justo, para que la conversación vuelva a la mesa y el teléfono deje de ser protagonista”.

# **8\. Temáticas útiles y límites conversacionales**

## **8.1. Qué convierte una conversación en un aporte**

Para aportar valor, una pregunta debe favorecer escucha, reciprocidad, comprensión mutua o disfrute sin exigir confesiones ni producir daño. Debe formularse de manera abierta, permitir que cualquier persona se abstenga y adecuarse al vínculo, edad y contexto. Profundidad y utilidad no son sinónimos: una pregunta ligera puede fortalecer pertenencia si invita a compartir sin presión.

* Preguntas abiertas: privilegiar “qué”, “cómo” o “cuál” y evitar interrogatorios que se respondan con sí/no.  
* Reciprocidad: evitar que la dinámica convierta a una persona en objeto de evaluación del grupo.  
* Gradualidad: comenzar con experiencias accesibles antes de invitar, solo con consentimiento, a reflexiones más personales.  
* Voluntariedad: cualquier participante puede omitir, reformular, pausar o retirarse sin justificar su decisión.  
* No evaluación: evitar puntuaciones emocionales, rankings de sinceridad, diagnósticos o juicios sobre vínculos.

## **8.2. Temas recomendados por aporte potencial**

| Tema | Aporte conversacional | Ejemplo seguro |
| :---- | :---- | :---- |
| Recuerdos compartidos | Construye continuidad y pertenencia. | ¿Qué momento juntos recuerdas con más cariño? |
| Gratitud y reconocimiento | Favorece apreciación sin exigir intimidad. | ¿Qué gesto reciente de alguien te hizo sentir acompañado? |
| Intereses y curiosidades | Invita a descubrir perspectivas y afinidades. | ¿Qué te gustaría aprender si tuvieras una tarde libre? |
| Experiencias cotidianas | Permite escuchar sin dramatizar. | ¿Qué fue lo más inesperado de tu semana? |
| Sueños y planes próximos | Facilita conocer aspiraciones sin presionar. | ¿Qué experiencia te gustaría vivir durante los próximos meses? |
| Valores en situaciones simples | Estimula reflexión sin convertirla en debate. | ¿Qué gesto pequeño hace que un lugar se sienta acogedor? |
| Cuidado y apoyo cotidiano | Permite identificar necesidades accesibles. | ¿Qué te ayuda a sentirte acompañado cuando tienes un día difícil? |
| Humor respetuoso y creatividad | Disminuye tensión e incorpora participantes reservados. | Si esta mesa tuviera una tradición propia, ¿cuál podría ser? |

## **8.3. Temas excluidos o sujetos a restricciones**

| Categoría | Riesgo principal | Regla recomendada |
| :---- | :---- | :---- |
| Trauma, abuso o violencia | Reactivación, exposición y ausencia de contención profesional. | No generar preguntas exploratorias ni pedir relatos personales. |
| Autolesión o ideación suicida | Riesgo grave y necesidad de intervención especializada. | Suspender la dinámica; no ofrecer orientación clínica automática. |
| Diagnóstico y tratamiento psicológico | Confusión entre conversación y atención de salud. | No diagnosticar ni recomendar medicamentos o terapias. |
| Sexualidad explícita | Inadecuación por edad, vínculo o contexto. | Excluir por defecto; nunca en presencia de menores o en contextos laborales. |
| Infidelidad y conflictos activos | Escalada de conflicto o presión pública. | No inducir acusaciones, confesiones o decisiones de pareja. |
| Ingresos, deudas y patrimonio | Vergüenza, comparación y exposición financiera. | No solicitar cifras ni obligaciones personales. |
| Política partidaria y religión | Polarización o presión ideológica. | Excluir en trabajo y grupos mixtos salvo activación explícita y segura. |
| Fertilidad, embarazo y maternidad | Sensibilidad personal y supuestos de género. | No preguntar deseos reproductivos, pérdidas o razones para no tener hijos. |
| Cuerpo, peso o alimentación | Estigma y riesgos vinculados con imagen corporal. | Evitar comentarios evaluativos, dietas o comparaciones físicas. |
| Identidad u orientación no revelada | Exposición de información sensible y discriminación. | No inferir ni solicitar revelaciones públicas. |
| Datos privados de terceros | Violación de privacidad o confidencialidad. | No pedir nombres, secretos, antecedentes médicos ni datos laborales sensibles. |
| Evaluación de desempeño laboral | Jerarquía, represalia y coerción. | Evitar preguntas sobre sueldo, productividad, favoritismos o conflictos con jefaturas. |

## **8.4. Reglas según el tipo de mesa**

* **Familia con menores.** Lenguaje comprensible, situaciones cotidianas, creatividad y emociones básicas; excluir sexualidad, conflictos parentales, secretos, violencia y datos personales. Un adulto responsable debe seleccionar el modo.  
* **Pareja adulta.** Recuerdos, reconocimiento, acuerdos cotidianos y planes comunes; temas sensibles solamente por elección explícita de ambas personas y nunca como intervención terapéutica.  
* **Amistades.** Historias, preferencias, humor y proyectos; evitar dinámicas que obliguen a revelar intimidad, comparar cuerpos o exponer a terceros ausentes.  
* **Compañeros de trabajo.** Intereses, aprendizajes, formas de colaboración y experiencias livianas; excluir política, religión, remuneraciones, conflictos jerárquicos, evaluación del desempeño y vida íntima.

## **8.5. Tono y redacción: ejemplos de ajustes necesarios**

| Evitar | Preferir | Motivo |
| :---- | :---- | :---- |
| ¿Quién de esta mesa te decepcionó más? | ¿Qué gesto te hace sentir considerado por otras personas? | Evita señalamiento público y acusación. |
| Cuenta el trauma que marcó tu vida. | ¿Qué experiencia te enseñó algo importante sobre ti? | Permite elegir profundidad sin forzar una revelación. |
| ¿Por qué todavía no tienes hijos? | ¿Qué proyecto personal te entusiasma actualmente? | Evita supuestos reproductivos y posibles duelos. |
| ¿Quién gana más dinero aquí? | ¿Qué aprendizaje reciente te ha resultado valioso? | Protege privacidad económica y reduce comparación. |
| Demuestra cuánto quieres a tu pareja. | ¿Qué gesto cotidiano te hace sentir acompañado? | Evita presión afectiva y validación obligatoria. |

# **9\. Recomendación de MVP y criterios de aceptación**

El resultado realista de tres semanas es un prototipo navegable y una propuesta de interacción evaluada inicialmente. Su flujo mínimo puede incluir una pantalla de bienvenida, selección de tipo de mesa, confirmación de mayores/menores, elección de profundidad, presentación de una pregunta por turno, controles de omisión/pausa y cierre opcional.

* La experiencia puede iniciarse desde un dispositivo compartido sin obligar a crear cuentas múltiples.  
* Cada pregunta cabe en una sola pantalla, utiliza lenguaje claro y corresponde al contexto seleccionado.  
* Las personas pueden cambiar u omitir una pregunta sin registrar explicaciones.  
* El prototipo no escucha, graba, transcribe ni diagnostica a quienes participan.  
* Existe una biblioteca segura que funciona como fallback cuando no se utiliza IA.  
* Las pruebas evalúan pertinencia, comodidad y atención fuera de pantalla; no usan métricas de retención como criterio principal.  
* La entrega diferencia explícitamente funcionalidades prototipadas, hipótesis pendientes y componentes que requerirían desarrollo técnico posterior.

# **10\. Conclusión**

Sobremesa tiene una dirección de diseño consistente cuando entiende el celular como una intervención breve y no como el centro de la experiencia. Su mayor fortaleza potencial no reside en generar infinitas preguntas, sino en seleccionar una pregunta pertinente, proteger a las personas involucradas y retirarse para que la conversación suceda fuera de la pantalla.

La base de datos aporta evidencia descriptiva sobre asociaciones entre exposición digital, estrés y bienestar, pero no valida la hipótesis central sobre conversación presencial. El benchmark confirma que las preguntas vinculares y las tarjetas digitales ya existen, por lo que la diferenciación depende de combinar contexto de comida, atención mínima, adaptación por vínculo y seguridad conversacional.

Con tres diseñadoras y tres semanas, el alcance responsable es investigar, diseñar, prototipar y validar inicialmente; no prometer una plataforma productiva ni resultados clínicos. La carta Gantt y la estructura de costos se mantienen editables y evitan inventar tarifas, gastos o beneficios no entregados.

# **11\. Fuentes y referencias verificadas**

* **Insumo del proyecto:** ficha\_proyecto(1).md; archivo entregado por la usuaria.  
* **Dataset analizado:** ScreenTime vs MentalWellness.csv; 400 registros. El XLSX adjunto presenta las variables concatenadas en una sola columna.  
* **Gottman Card Decks:** https://www.gottman.com/couples/apps/  
* **Gottman: preguntas abiertas y contexto laboral:** https://www.gottman.com/blog/colleague-maps/  
* **Paired:** https://www.paired.com/  
* **TableTopics Family:** https://tabletopics.com/products/family  
* **We’re Not Really Strangers: reglas del juego:** https://www.werenotreallystrangers.com/pages/how-to-play-core-game  
* **The Skin Deep / {THE AND}:** https://shop.theskindeep.com/pages/the-and-conversation-card-games  
* **The Family Dinner Project: tarjetas:** https://thefamilydinnerproject.org/giving-tuesday-old/conversation-cards/  
* **The Family Dinner Project: empatía en la mesa:** https://thefamilydinnerproject.org/october-2013/  
* **Timeleft: conversación y seguridad:** https://timeleft.com/blog/safety-starts-before-the-dinner/  
* **one sec:** https://one-sec.app/  
* **one sec: limitaciones de Screen Time API:** https://tutorials.one-sec.app/en/articles/3036354

*Consulta de fuentes externas: 20 de agosto de 2026\. Las características de servicios digitales pueden cambiar; no se incorporaron precios comerciales, métricas de eficacia promocional ni funciones no verificadas.*