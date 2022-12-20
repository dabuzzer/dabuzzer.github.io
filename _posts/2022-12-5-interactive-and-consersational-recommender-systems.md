---
layout: post
title: "Clase 8: Interactive and Conversational Recommender Systems"
---
 
Estos tipos de sistemas se basan netamente en una propuesta inicial, la cual se va refinando a través de feedback del usuario, mediante el intercambio de comunicación constante y finalmente el sistema es capaz de entregar un resultado.
 
La finalidad es poder transformar la experiencia de los usuarios en una forma natural del comportamiento de estos, por medios de interacciones no clásicas como podría ser la voz y/o texto, así ir pudiendo guiar al usuario y a su vez poder entender lo que realmente necesita y así indicar una recomendación adecuada.
 
Durante este último tiempo este tipo de sistemas ha tomado más auge ya que hoy en día existen herramientas de Reinforced Learning y Machine Learning, los cuales hacen que este sea mucho más usable, así también la cantidad de información existente es muchísima.
 
### Arquitectura Global
 
En una generalidad un sistema de este tipo posee dos componentes principales
 
1. Active listening: un engine de conversación el cual acepta una entrada del usuario este podría ser un chat y otro componente de recomendación el cual retorna resultados en función de la atención de la conversación.
 
2. Personal Insight: sistema de inferencia, entiende al usuario e infiere personalidad y este se une con el componente de recomendación para retornar resultados (recomendaciones)
 
#### Tipos de Sistemas
 
- **SAUP** - Sistema Activo, usuario pasivo: el sistema guía la conversación al preguntarle al usuario y el usuario solo puede responder directamente (alternativas)
 
- **SAUE** - Sistema Activo, Usuario participando: Existe relación y no necesariamente el usuario responde lo que quiere o pregunta el sistema, así el sistema va viendo los mensajes y puede recomendar de una mejor forma
 
- **SUAU** - Sistema Activo, Usuario Activo: ambos pueden guiar la conversación, el usuario pregunta sobre recomendación y así también pregunta para tener más información
 
 
 
## Evaluación
 
Las formas de evaluar pueden ser desde diferentes puntos:
 
1. Turn-level Metrics:
  - Calidad de las oraciones generadas por el chatbot (BLEU, ROUGE, legibilidad): métricas de machine translation y legibilidad
  - relevancia de preguntas generadas por el chatbot (ground truth de preguntas, accuracy, recall):
  - Frecuencia y distribución de acciones tomadas por el chatbot (recomendar, chatear, preguntar)
  - Nivel de cooperación del usuario( cuando responde el usuario a las preguntas del chatbot)
2. Dialogue-Level metrics:
  - Largo de los diálogos
  - Ratio diálogo satisfactorio y cumplimiento de tareas (recomendar, preguntar)
3. Business-Level metrics:
  - conversion-rate por sesión de chats
  - incremento de ventas
  - satisfacción del usuario, ratings, retención de clientes, lealtad de clientes, etc
 
 
# Modelo
 
Primeramente se acepta una entrada (user query) y luego el sistema debe responder algo, internamente se compone de cinco grandes módulos:
 
1. NLU/NLG: Módulo de natural language understanding / generation, el cual se encarga de entender la entrada del usuario y generar diálogos
2. Dialogue State Management: Controla quien es el que habla y qué acciones se va a tomar
3. Sistema recomendador: encargado de generar la recomendación deseada en función de la finalidad de este y la entrada de los datos
4. Explicación opcional: Mostrar porque al usuario se le realizó dicha recomendación
5. Knowledge: Conocimiento externo del usuario, como su perfil, clicks, compras, items, etc.
 
 
![_config.yml]({{ site.baseurl }}/images/arquitectura_conversacional.png)
 
 

