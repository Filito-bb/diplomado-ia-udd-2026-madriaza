**Documento de Análisis y Planificación Estratégica**  
**Proyecto: Sobremesa (El Mediador Digital de Presencia para Vínculos Reales)**

\---

1\. Análisis Experto y Recomendaciones de Mejora

El proyecto 'Sobremesa' aborda un problema contemporáneo de gran calado: la paradoja de la hiperconexión digital que erosiona la conexión humana presencial. Desde una perspectiva de diseño UX/UI y psicología social, la ficha técnica y los datos anexos revelan una oportunidad y también riesgos significativos que requieren una dirección estratégica clara.

Análisis de la Oportunidad: El dataset proporcionado (ScreenTime vs MentalWellness.csv) valida empíricamente la necesidad del proyecto. Existe una correlación negativa sólida entre el tiempo de pantalla de ocio y los índices de bienestar mental y calidad del sueño, mientras que el tiempo dedicado a actividades sociales presenciales correlaciona positivamente con una mayor productividad y menor estrés. La solución propuesta, por lo tanto, no es un producto de nicho, sino una herramienta con un potencial de impacto social y de bienestar general muy amplio. El concepto de "mediador de baja fricción" es clave, distinguiéndose de soluciones prohibitivas o de juegos de mesa tradicionales que suelen fallar por su rigidez.

Mejoras Propuestas (Enfoque Estratégico):

· Reenfocar el Modelo Generativo "Analítico": La ficha propone un agente analítico para clasificar el tono y las dinámicas de la mesa. Esa aproximación es riesgosa y puede generar incomodidad o una sensación de vigilancia. La mejora consiste en reposicionar al modelo analítico como un motor de "Adaptación Contextual Implícita". En lugar de evaluar a los usuarios, el análisis se centrará en variables de entrada simples y no invasivas (e.g., "¿Cómo te sientes hoy?" \- escala de energía; "Número de comensales"; opción de selección de "Ambiente" como 'Relajado', 'Animado', 'Íntimo') para ajustar la generación de prompts. La "edad" se usará solo para clasificar el público (infantil, juvenil, adulto) y filtrar contenido inapropiado. Esto protege la privacidad y evita una dinámica de "juego de roles" forzada, manteniendo la agencia de los usuarios sobre la experiencia.  
· Evolucionar de "Tarjetas Digitales" a una "Interfaz de Ritual": La visión de una interfaz de "tarjetas" es un punto de partida mínimo viable (MVP), pero se subestima. El diseño debe ir más allá de una simple baraja y aspirar a ser un facilitador de un "ritual". La propuesta de mejora es diseñar la UX para que el acto de pasar el teléfono sea un gesto significativo en sí mismo. La interfaz debe ser extremadamente minimalista, con animaciones suaves y sonidos táctiles (si el contexto lo permite) que otorguen un peso ceremonial al intercambio, similar a pasar un objeto simbólico en un círculo de confianza. El objetivo es que la interacción con la app sea una transición, no el foco de la atención.  
· Incorporar Dinámicas de Grupo Sincrónicas: El modelo actual parece asumir un flujo de una sola pregunta a la vez. Para un grupo más grande, esto puede ralentizar la dinámica. La mejora es incorporar modos de juego que exploten la naturaleza mediadora del teléfono:  
  · Modo "Ruleta": Cada participante registra su nombre (o un emoji) y el sistema selecciona aleatoriamente a quién le toca responder, agregando un elemento de sorpresa y asegurando que la conversación no sea monopolizada.  
  · Modo "Contador de Turnos": Un sistema de puntuación no competitivo que simplemente registra cuántas veces cada persona ha participado, incentivando una participación equilibrada.  
  · Sistema de "Me gusta" Anónimo: Un botón que permite a los comensales dar un "voto" anónimo a la respuesta que más les resonó, generando una conversación meta sobre el contenido compartido, sin complejos ni competitividad .

\---

2\. Los Tres Pilares Esenciales para la Interfaz

El éxito de 'Sobremesa' depende de una arquitectura de diseño que mantenga un equilibrio constante entre la utilidad digital y la discreción. Los pilares son:

1\. Invisibilidad Funcional: El diseño UI/UX debe tender hacia la desaparición. La interfaz debe ser de lectura instantánea, con tipografía clara y generosa, y botones de acción primarios (siguiente, pasar) de gran tamaño para minimizar el tiempo de foco visual. El objetivo es que la interacción con el teléfono sea un "glance and pass" (mirar y pasar), nunca un "stare and scroll" (quedarse mirando y desplazarse) . La paleta de colores debe ser cálida y suave, evitando el blanco brillante o los azules fríos de las redes sociales, y se deben eliminar todos los elementos de gamificación intrusivos como puntos, niveles o rankings .  
2\. Curatación Contextual y Ética: El corazón de la aplicación es su contenido. No basta con tener cientos de preguntas, estas deben ser seleccionadas y generadas con una sensibilidad psicológica y social. El sistema generativo debe ser guiado por un "System Prompt" que privilegie la empatía, la vulnerabilidad segura y la conexión, evitando temas divisivos o que generen ansiedad. La app debe permitir a los usuarios seleccionar el "tono" de la conversación, desde una 'Conexión Profunda' hasta una 'Charla Ligera', para que siempre sea un aporte y nunca una fuente de tensión .  
3\. Privacidad por Diseño y Seguridad Psicológica: Para fomentar conversaciones auténticas y significativas, el usuario debe sentir que la "mesa" es un espacio sagrado y privado . Esto se traduce en:  
   · Cero Datos: No se debe crear ninguna cuenta de usuario. La aplicación debe funcionar completamente offline. No se debe recolectar, almacenar ni transmitir ningún dato personal o de la conversación.  
   · Transparencia: La política de privacidad debe ser la característica más destacada y estar redactada en un lenguaje claro, no legalista.  
   · No Juicio: La interfaz y el contenido no deben juzgar las respuestas. Debe ser un espacio libre de evaluación, donde todas las opiniones y niveles de profundidad sean bienvenidos.

\---

3\. Los Tres Principales Problemas de Desarrollo

1\. La Paradoja de la "Interfaz de Baja Fricción": Lograr que una aplicación sea "fácil de usar" e "intuitiva" es un desafío estándar. El verdadero reto de 'Sobremesa' es diseñar una interfaz que sea tan intuitiva que se "desvanezca" en el ritual social. El mayor riesgo es que la interfaz se convierta en un "ruido" visual o táctil que interrumpa la conversación, logrando el efecto contrario al deseado. Un "paso" de más, una animación demasiado larga o una fuente ilegible, y la app fracasa en su misión principal.  
2\. Mantener la "Vida Útil" sin Fricción: La mayoría de los juegos de conversación fallan porque el usuario agota el contenido rápidamente. Para 'Sobremesa', el desafío no es solo tener mucho contenido, sino mantener la novedad y relevancia del contenido sin introducir complejidades como actualizaciones constantes, conexión a internet, o la necesidad de crear una cuenta (lo cual ya está descartado por diseño). La solución podría ser un modelo generativo que funcione offline o un sistema de "cartas" pre-cargadas que se actualicen con nuevas temáticas en cada gran actualización de la app, resolviendo el problema de raíz mediante la calidad y la variedad del contenido inicial.  
3\. El Ruido de las Notificaciones: La aplicación debe ser un oasis de desconexión. Un problema crítico es que las notificaciones de otras apps (WhatsApp, correos, etc.) interrumpan la experiencia de 'Sobremesa', arruinando el estado de flujo de la conversación y recordando al usuario el mundo digital del que busca escapar. La solución no debe ser técnica (forzar un "modo no molestar"), sino de diseño: la app debe recomendar explícitamente (a través de su onboarding y su diseño) que los usuarios activen el modo avión o no molestar de forma voluntaria, haciendo de esto un paso ritualístico. El desafío es lograr que el usuario acepte esta sugerencia como parte natural de la experiencia.

\---

4\. Diagrama de Gantt (Entregable en Excel)

A continuación, se presenta una estructura para el diagrama de Gantt. La unidad de tiempo es el "día", asumiendo una jornada laboral de 8 horas. El archivo Excel debe incluir esta información con barras de progreso para cada fase.

Fase Actividad Inicio Fin Duración Dependencia  
Semana 1       
1\. Definición y Estrategia 1.1 Refinar definición de producto y público objetivo. Día 1 Día 1 1d   
 1.2 Investigación de mercado y análisis de competidores (Benchmarking). Día 1 Día 2 2d 1.1  
 1.3 Creación del "System Prompt" para el modelo generativo. Día 2 Día 3 2d 1.2  
 1.4 Arquitectura de la información y definición de User Flows. Día 3 Día 5 3d 1.2  
Semana 2       
2\. Diseño UX/UI 2.1 Creación de wireframes de baja fidelidad (bocetos). Día 6 Día 7 2d 1.4  
 2.2 Pruebas de usabilidad con wireframes. Día 8 Día 8 1d 2.1  
 2.3 Creación de prototipos de alta fidelidad (UI). Día 8 Día 10 3d 2.2  
 2.4 Definición del sistema visual: colores, tipografías, animaciones. Día 9 Día 10 2d 2.1  
Semana 3       
3\. Desarrollo y Validación 3.1 Preparación de assets para desarrollo (guías de estilo, etc.). Día 11 Día 11 1d 2.3, 2.4  
 3.2 Desarrollo de prototipo funcional en Figma/Protopie. Día 11 Día 13 3d 3.1  
 3.3 Pruebas de usuario con prototipo funcional. Día 13 Día 14 2d 3.2  
 3.4 Iteración final y refinamiento de diseño basado en pruebas. Día 14 Día 15 2d 3.3

\---

5\. Estructura de Costos (3 Diseñadoras Gráficas Profesionales)

Se asume un proyecto de 3 semanas (15 días hábiles) y un valor de mercado para diseñadores UX/UI senior en Chile. Los costos son estimados y referenciales.

· Equipo de Diseño (3 Diseñadoras)  
  · Costo por hora (referencial): CLP 15.000 \- 25.000.  
  · Costo por día (8 horas): CLP 120.000 \- 200.000.  
  · Costo total por diseñadora (15 días): CLP 1.800.000 \- 3.000.000.  
  · Costo total del equipo de diseño (3 diseñadoras): CLP 5.400.000 \- 9.000.000.  
· Otros Costos Directos  
  · Gestión de Proyecto y Dirección de Arte (1 Líder): CLP 2.000.000 (aproximado).  
  · Prototipado y Herramientas (Figma, etc.): CLP 150.000.  
  · Investigación y pruebas de usuario (incentivos): CLP 300.000.  
  · Registro de Propiedad Intelectual (INAPI): CLP 205.944 (referencial) .  
  · Gastos Operativos (Internet, etc.): CLP 100.000.  
· Costo Total Estimado del Proyecto:  
  · Mínimo: $5.400.000 \+ $2.755.944 \= CLP 8.155.944  
  · Máximo: $9.000.000 \+ $2.755.944 \= CLP 11.755.944  
· Nota: Estos costos cubren la fase de diseño, estrategia y validación (hasta prototipo funcional listo para desarrollo). El costo de desarrollo de la app (programación) no está incluido y podría oscilar entre los CLP 25.000.000 y CLP 45.000.000 para una aplicación estable, segura y con las funcionalidades descritas .

\---

6\. Benchmark Actual de la Competencia

Producto / App Propuesta de Valor Fortalezas Debilidades Precio  
Sobremesa: Dinner Questions  Recrear el ritual de "la sobremesa" con preguntas para toda la familia. 100% offline, sin cuentas, pago único, disponible en español, enfoque familiar y de conexión profunda. Lanzada recientemente (Junio 2026). Solo iOS, precio de entrada de pago (USD 3.99). $3.99 USD (Pago Único)  
Spilld: Deep Conversations  Baraja de preguntas para conversaciones profundas. Variedad de "packs" para diferentes tipos de relaciones (pareja, amigos, familia). Modelo de suscripción Freemium (costos anuales/semanales), solo iOS. Gratis / Compras in-app  
Conversation Starters: Deep Qs  Baraja simple de preguntas para pasar el teléfono. Interfaz muy simple ("swipe"), varios decks, modelo Freemium, enfoque en "no ser el centro de atención". Contenido predefinido, puede carecer de la adaptabilidad de un modelo generativo. Gratis / Compras in-app  
Within / Deep Stories / Say It\!  Varias aplicaciones similares que ofrecen preguntas para conectar. Modelo Freemium accesible, variedad de temáticas. Pueden ser genéricas y no tener un enfoque tan claro en la desconexión total. Gratis / Compras in-app

Conclusión del Benchmark: El mercado de aplicaciones de preguntas para conversar está creciendo, con un claro enfoque hacia la desconexión y la conexión real. La competencia principal de 'Sobremesa' es Spilld y Conversation Starters, ambas con propuestas y modelos de negocio similares. La principal diferenciación de 'Sobremesa' debe ser su potente motor generativo adaptativo y su modelo de privacidad radical, que lo posicionaría como el líder en personalización y seguridad.

\---

7\. Limitaciones de Temáticas para un Aporte Real

Para que la aplicación cumpla su propósito de fortalecer vínculos, es crucial evitar temas que generen conflicto, ansiedad o que trivialicen la experiencia. Las limitaciones temáticas deben ser un mandato de diseño, no una sugerencia.

· Temas Prohibidos (Generan Fricción): Política, religión, finanzas personales detalladas, problemas de salud graves no resueltos en el grupo, y chismes sobre personas ausentes. Estos tópicos pueden derivar en discusiones polarizadas y romper la atmósfera de confianza y seguridad .  
· Temas a Evitar (No Aportan al Vínculo): Preguntas excesivamente superficiales o triviales que no fomenten la introspección o el conocimiento mutuo. "¿Cuál es tu color favorito?" es una pregunta vacía que no genera conexión.  
· Temas a Tratar con Cuidado (Bajo el Filtro "Contexto"): La muerte, las rupturas sentimentales o los traumas personales. Estos temas pueden ser profundamente significativos y generar un vínculo muy fuerte, pero solo en el contexto adecuado (ej. una pareja, un grupo de amigos íntimos). La app debe ser capaz de "medir el pulso" de la conversación (quizás con un feedback post-pregunta simple) para no recomendar temas demasiado densos en un contexto de cena familiar ligera.  
· Temas Clave para el Aporte: Preguntas sobre recuerdos de la infancia, aspiraciones futuras, experiencias compartidas, lecciones de vida, agradecimientos, y preguntas lúdicas que inviten a la imaginación o la risa. El objetivo es generar narrativas y anécdotas que permitan a los comensales verse bajo una nueva luz .

La regla de oro debe ser: "¿Esta pregunta podría hacer que alguien se sienta incómodo o a la defensiva? Si es así, no es apta para el público general de la aplicación". Un sistema de "reporte" o "calificación" de preguntas (anónimo, al final de la sesión) podría ayudar al equipo a refinar el filtro de contenido de forma continua.

\---

Nota para el Equipo: Este análisis estratégico es su guía para la construcción de la ficha de proyecto y el desarrollo de la identidad de 'Sobremesa'. Recuerden que el éxito se mide en sonrisas compartidas, no en descargas.
