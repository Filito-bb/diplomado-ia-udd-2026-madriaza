# Actividad Clase 25 

### Grupo 7 

Isabel Ferrán – Victoria Madriaza – M. Ignacia Moya 

# **Prompt** 

Eres un experto diseñador/desarrollador UX/ui senior con más de 10 años de experiencia en creación de aplicacio nes e interfaces didácticas, orientadas al desarrollo comunicacional entre personas, fundamentado en psicología social y vincular. Debes hablar con un lenguaje profesional y comprensible a todo público. Te entregaré el proyecto llamado “Sobre mesa”, el cual consta de generar una interfaz en donde 

el desafío de diseño está en redefinir el rol de la pantalla del celular en la mesa, utilizándola como un mediador int eractivo, sutil y libre de fricciones físicas, que estimule y guie la conversación cara a cara en lugar de absorber la at ención de los comensales. Te entregaré 2 archivos relacionados con el proyecto. Encontrarás la ficha del proyecto y una base de datos asociada a la temática de bienestar mental versus el tiempo en pantalla. 

#### Tu tarea es 

1. Genera un análisis bajo tu ojo experto del proyecto y posibles mejoras 

2. A partir de ese análisis, identifica los 3 pilares esenciales para el correcto funcionamiento de esta interfa z según su propósito 

3. Menciona los 3 principales problemas que podríamos enfrentar al desarrollar esta aplicación 

4. Considerando lo anterior, genera una carta Gantt considerando que serán 3 semanas destinadas a este p royecto. Esta carta Gantt entrégala en formato Excel. 

5. En base a esa carta Gantt, genera una estructura de costos, considerando que son 3 diseñadoras gráfica s profesionales  encargadas del proyecto. 

6. Genera un benchmark actual con respecto al proyecto. 

7. Menciona limitaciones de temáticas en base a las conversaciones que realmente generarán un aporte a quienes utilicen la aplicación 

#### Necesito que el formato de entrega sea en un documento editable Word. 

No inventes datos ni incorpores elementos fuera del contexto de la solicitud. Que tu análisis no sea débil. No seas un agente condescendiente. 

**<mark>Se solicitó a cada agente entregar una síntesis ejecutiva para exponer los resultados incorporados en los documentos que entregó que están anexados al fnal del documento</mark>** 

## **Respuesta – ChatGPT** 

## (Síntesis ejecutiva) 

Se realizó un análisis integral del proyecto Sobremesa, identificando oportunidades de mejora y tres pilares fundamentales: atención mínima a la pantalla, adaptación de las conversaciones al tipo de vínculo y seguridad emocional de los participantes. También se definieron los principales desafíos de desarrollo, las temáticas recomendadas y aquellas que deben evitarse, junto con un benchmark de ocho referentes relacionados con la conversación y el bienestar digital. Además, se analizó una base de datos de 400 personas, incluyendo 107 estudiantes, y se desarrolló una carta Gantt de tres semanas con 24 actividades y una estructura de costos editable para tres diseñadoras. 

### Síntesis ejecutiva 

Sobremesa propone transformar el celular en un mediador discreto que fomente conversaciones presenciales durante las comidas. El análisis identificó tres pilares estratégicos: reducir la atención destinada a la pantalla, adaptar las preguntas al contexto de cada mesa y proteger la seguridad emocional y privacidad de los participantes. También estableció riesgos de implementación, oportunidades de mejora, límites temáticos y un benchmark de ocho referentes. La propuesta se complementa con el análisis de 400 registros y una planificación de tres semanas, distribuida en 24 actividades y 289 horas estimadas para tres diseñadoras, junto con una estructura de costos editable. 

## **Respuesta – Claude** 

## (Síntesis ejecutiva) 

### Hallazgo central (con datos propios, no supuesto): 

No es el tiempo compartido lo que protege el bienestar mental, es la atención. En tu dataset, más horas sociales por semana casi no mueven el bienestar (20 → 19 → 22 sobre 100), pero más horas de pantalla lo hunden con fuerza (36 → 16 → 8), y ese efecto se mantiene incluso en el grupo que más socializa (r=-0,70). Esto valida el posicionamiento de Sobremesa frente a "solo prohibir" o "solo juntar gente". 

Diagnóstico: el concepto es sólido y la arquitectura (pipeline analítico + generativo) está bien planteada, pero hay 4 decisiones sin resolver que condicionan todo el diseño posterior: cómo se capta la composición de la mesa sin cámara/micrófono invasivo ni fricción de formulario; cómo se retira el mediador una vez arranca la conversación; qué métrica de éxito reemplaza al "tiempo en pantalla" (que aquí es la métrica _equivocada_ por definición); y tratar el modelo de IA como pieza reemplazable, no como decisión fija. 

3 pilares: fricción cognitiva/física cero · inteligencia contextual con privacidad por diseño · auto-desvanecimiento progresivo (el producto debe apagarse solo). 

3 problemas críticos: (1) captar contexto de mesa sin vigilancia ni fricción — sin solución evidente aún; (2) latencia de generación en tiempo real, que puede recrear exactamente la escena que se quiere evitar (gente mirando el celular en silencio); (3) la paradoja de que el éxito del producto es que se use poco, lo cual choca con cualquier modelo de negocio estándar de app. 

Plan y costos (Excel): 11 tareas / 15 días hábiles / 5 fases (Descubrimiento → Sistema visual → Prototipado → Validación → Cierre), 296 horas-persona de las 3 diseñadoras (82% de su capacidad), costo total $8.171.050 CLP ($7,4M en horas de diseño + licencias Figma + 10% de contingencia), con tarifa y tipo de cambio documentados y con fuente. 

Benchmark: nadie hace hoy lo que propone Sobremesa. Los más cercanos (TableTopics, We're Not Really Strangers) usan mazos fijos de preguntas — no leen quién está realmente en la mesa ni se adaptan en tiempo real. Ese es el espacio libre que Sobremesa puede ocupar. 

Límites temáticos: el sistema debe generar por defecto solo temas livianos (curiosidad, anécdotas, planes), habilitar temas más profundos solo con señal clara de confianza y homogeneidad de edad, y nunca sugerir de forma proactiva finanzas del grupo, conflictos no resueltos, duelo/salud de terceros, política o contenido adulto con menores presentes. 

## **Respuesta – Deepseeck** 

## (Síntesis ejecutiva) 

### Proyecto Sobremesa 

### Visión General 

Sobremesa es una aplicación mobile diseñada para transformar el teléfono inteligente de un agente de distracción en un mediador de conversación presencial. Su propósito es rescatar el ritual social de compartir la comida, ofreciendo una herramienta digital de baja fricción que genera detonadores conversacionales adaptados al contexto de la mesa, sin absorber la atención de los comensales. 

### El Problema 

La hiperconexión digital ha erosionado la calidad de los encuentros presenciales. Las personas pasan más tiempo mirando pantallas que conversando cara a cara, incluso en contextos sociales como almuerzos o cenas. Las soluciones existentes fallan porque: 

- Prohibiciones generan rechazo y resistencia. 

- Juegos análogos imponen una fricción logística que abandona la iniciativa. 

- Apps tradicionales mantienen a los usuarios atrapados en la pantalla. 

La Solución Propuesta 

Una aplicación que: 

### Característica Descripción 

Mediación contextual Genera preguntas y dinámicas adaptadas al perfil de la mesa (número de comensales, tipo de vínculo, ambiente). 

Interfaz invisible Diseño minimalista que prioriza el "mirar y pasar" (glance and pass) sobre el "quedarse mirando" (stare and scroll). 

Privacidad radical 100% offline, sin cuentas, sin almacenamiento de datos personales. 

Ritual de uso El acto de pasar el teléfono se convierte en un gesto significativo que facilita la conexión. 

### Validación de Mercado 

El dataset analizado (ScreenTime vs MentalWellness.csv) confirma: 

· Correlación negativa: Mayor tiempo de pantalla de ocio = menor bienestar mental y calidad del sueño. 

· Correlación positiva: Mayor interacción social presencial = mayor productividad y menor estrés. 

Benchmark Competitivo: 

· Competidores directos como Spilld y Conversation Starters operan bajo modelos Freemium con contenido predefinido. 

· La ventaja competitiva de Sobremesa es su motor generativo adaptativo y su modelo de privacidad radical, posicionándose como líder en personalización y seguridad. 

--- 

Pilares de Diseño 

1. Invisibilidad Funcional - Interfaz que desaparece en el ritual social. 

2. Curatación Contextual y Ética - Contenido generado con sensibilidad psicológica. 

3. Privacidad por Diseño - Espacio seguro y libre de juicios. 

--- 

Plan de Ejecución 

Fase Duración Entregables 

Definición y Estrategia Semana 1 Definición de producto, benchmarking, system prompt, arquitectura de información 

Diseño UX/UI Semana 2 Wireframes, prototipos alta fidelidad, sistema visual 

Desarrollo y Validación Semana 3 Prototipo funcional, pruebas de usuario, iteraciones finales 

- 

Estructura de Costos (Diseño) 

Concepto Costo Estimado (CLP) 

Equipo de diseño (3 diseñadoras × 15 días) $5.400.000 – $9.000.000 

Gestión de proyecto y dirección de arte $2.000.000 

Herramientas y prototipado $150.000 

Pruebas de usuario (incentivos) $300.000 

Registro propiedad intelectual (INAPI) $205.944 

Gastos operativos $100.000 

Total Diseño $8.155.944 – $11.755.944 

Nota: Desarrollo (programación) estimado entre $25M – $45M adicionales. 

--- 

Limitaciones Temáticas 

Para garantizar un aporte real a los vínculos, la aplicación debe: 

Evitar Fomentar 

Política, religión, finanzas personales Recuerdos de infancia, aspiraciones 

Chismes sobre ausentes Experiencias compartidas 

Temas polarizantes o divisivos Lecciones de vida, agradecimientos 

Preguntas superficiales sin profundidad Preguntas que generen narrativas y anécdotas --- 

Métricas de Éxito 

El éxito de Sobremesa no se mide por: 

- Tiempo de retención en pantalla. 

- Número de descargas. 

Se mide por: 

- Tiempo de calidad que los comensales pasan mirándose a los ojos. 

- Conversaciones significativas y presenciales. 

- Capacidad del smartphone para desaparecer como foco de atención. 

--- 

- "El smartphone solo actúa como un mediador de baja fricción." 

