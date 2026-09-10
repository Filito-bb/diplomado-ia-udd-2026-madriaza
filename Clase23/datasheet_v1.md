# **Datasheet — Sobremesa**

*Documento vivo. Se completa clase a clase.*

## **1\. Motivación**

* ¿Para qué usarás este dataset en tu proyecto?

Para proveer al agente mediador de **Sobremesa** una base de datos curada de preguntas y disparadores conversacionales que estimulen la interacción cara a cara y reduzcan el tiempo de pantalla excesivo durante comidas y reuniones familiares.

* ¿Quién lo creó originalmente? (tú, tu equipo de Unidad 2, un tercero, público)

Creado por el equipo 7 para el módulo 3\. 

## **2\. Composición**

* Tipo de datos (texto, imagen, tabla, audio, mezcla):

Tabla estructurada de texto (formato CSV).

* Cantidad de instancias:

 10 instancias iniciales en la versión v1.

* ¿Hay subgrupos identificables? (edad, género, región, otro):

Sí, clasificados por fases de la comida *(Entrada/Picoteo, Plato de fondo, Postre, Bajativo)*, niveles de profundidad emocional *(Bajo, Medio, Alto)* y un subgrupo cultural enfocado en modismos y referentes de Chile.

## **3\. Recolección**

* ¿Cómo se recolectaron? (encuesta, scraping, API, entrevistas):

Mediante curaduría manual basada en técnicas de mediación grupal y generación asistida en lenguaje natural adaptada al contexto local.

* ¿Cuándo?: 

Agosto \- Septiembre de 2026\.

* ¿Se pidió consentimiento?:

No aplica consentimiento individual, ya que no se recolectaron datos personales ni respuestas de personas reales; son enunciados sintéticos y disparadores diseñados para el proyecto.

## **4\. Sesgos identificados (mínimo 2\)**

* Sesgo 1: **Sesgo cultural local:** Las preguntas incorporan modismos y referentes gastronómicos o sociales propios de Chile, lo que puede reducir su resonancia en usuarios de otros países.

* Sesgo 2: **Sesgo etario y de estructura familiar:** Varios disparadores apelan a recuerdos de la infancia o dinámicas familiares tradicionales, lo que podría incomodar o alienar a comensales sin vínculos familiares tradicionales o personas muy jóvenes.

## **5\. Estrategias de mitigación (mínimo 2\)**

* Estrategia 1: **Diversificación de categorías:** Inclusión de categorías de humor, imaginación y debate lúdico que no dependan del pasado personal ni de estructuras familiares específicas.

* Estrategia 2: **Dosificación por nivel de intimidad y fase de la comida:** Etiquetado explícito de cada instancia por nivel de intimidad (Bajo, Medio, Alto) para que el agente filtre automáticamente los enunciados según la fase de la reunión.

## **6\. Uso recomendado / desaconsejado**

* Para qué SÍ debería usarse: Como base de conocimiento para dinámicas de bienestar digital, reuniones familiares o de amigos y talleres de convivencia donde se busque incentivar el contacto visual y la escucha activa.

* Para qué NO debería usarse: En entornos laborales jerárquicos, negociaciones formales, terapia de pareja o familiar profesional, ni en situaciones con conflictos interpersonales severos no resueltos.

## **7\. Notas para Mauricio (Unidad 4\)**

* Qué necesita saber quien use este dataset en la próxima unidad:

Este dataset es el centro conversacional de Sobremesa. Quien reciba el proyecto en la Unidad 4 debe saber que la clave de su efectividad es la **oportunidad del disparo conversacional** filtrado por la fase de la comida. Se debe mantener la estructura de columnas (\`id\`, \`pregunta\_detonante\`, \`categoria\`, \`fase\_comida\`, \`nivel\_intimidad\`) para asegurar el filtrado lógico correcto antes de desplegar el contenido en pantalla.
