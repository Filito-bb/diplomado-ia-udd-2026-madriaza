### Ficha de proyecto - Sobremesa

*Documento vivo. Se completa clase a clase - es tu model card en version de borrador. Subelo a tu repo como docs/ficha_proyecto.md.*

#### 1. Nombre interno del proyecto
`Sobremesa` (El Mediador Digital de Presencia para Vinculos Reales).

#### 2. Problema (2-3 frases)
La hiperconexion a traves de smartphones ha deteriorado el ritual social de compartir la comida, convirtiendo los almuerzos y cenas en momentos de desconexion interpersonal. Las soluciones basadas en prohibiciones estrictas generan rechazo, mientras que los juegos analogicos impresos imponen una friccion logistica que causa que el usuario abandone la iniciativa. El desafio de diseno consiste en redefinir el rol de la pantalla del celular en la mesa, utilizandola como un mediador interactivo, sutil y libre de fricciones fisicas, que estimule y guie la conversacion cara a cara en lugar de absorber la atencion de los comensales.

#### 3. Usuario / cliente objetivo
Familias, parejas, grupos de amigos y companeros de trabajo que valoran el encuentro en torno a la comida (almuerzos, cenas, la "once") pero sufren de la distraccion constante de las notificaciones, y que buscan una herramienta cotidiana y fluida para reactivar dinamicas de conversacion profunda y distension en el mundo fisico.

#### 4. Tipo de modelo que vas a necesitar
* [X] Ambos (pipeline combinado)
  * *Analitico:* Para evaluar la composicion de la mesa (edad de los comensales, tipo de vinculo, nivel de confianza) y clasificar que dinamicas conversacionales o tonos son los mas adecuados para evitar tensiones.
  * *Generativo:* Para redactar en tiempo real los detonadores conversacionales, los micro-desafios adaptados al contexto y generar la interfaz visual de las tarjetas digitales.

#### 5. Modelos candidatos (2-3 concretos)
1. **GPT-4o / Claude 3.5 Sonnet:** Modelos principales para la generacion del contenido conversacional altamente empatico y adaptado a la mesa.
2. **Gemini 2.5 Flash Image (Nano Banana):** Para co-disenar los layouts visuales minimalistas y la interfaz movil libre de destellos molestos.
3. **Google Flow (Veo 3):** Para generar los clips de video conceptuales que demuestren el funcionamiento del mediador en un entorno real.

#### 6. Roadmap del proyecto (se completa clase a clase)
* [ ] Clase 23 - Datasheet del dataset (docs/datasheet_v1.md)
* [ ] Clase 24 - Hallazgos NotebookLM (docs/hallazgos_notebooklm.md)
* [ ] Clase 25 - System prompt (docs/system_prompt_v3.md)
* [ ] Clase 26 - Modelos HF candidatos (docs/modelos_hf_candidatos.md)
* [ ] Clase 27 - Sistema visual (docs/sistema_visual.md)
* [ ] Clase 28 - Arquitectura del agente (docs/arquitectura_agente.md)
* [ ] Clase 29 - Video generativo (docs/video_generativo.md)
* [ ] Clase 30 - Casos de uso Hermes (docs/hermes_casos_uso.md)
* [ ] Clase 31 - Antigravity Loop + cierre (docs/antigravity_loop.md)

#### 7. Notas para Mauricio (Unidad 4)
Este proyecto mide su exito no por la retencion de los usuarios en la pantalla del celular, sino por el tiempo de calidad que pasan mirandose a los ojos y conversando de manera presencial. El smartphone solo actua como un mediador de baja friccion.
