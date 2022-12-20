---
layout: post
title: "Clase 8: Interactive and Conversional Recommender Systems"
---

## Sistema Recomendadores Conversasionales

Estos tipos de sistemas se basan netamente en una propuesta inicial, la cual se va refinando a traves de feedback del usuario, mediante el intercambio de comunicacion constante y finalmente el sistema es capaz de entregar un resultado.

La finalidad es poder transformar la experiencia de los usuarios en una forma natural del comportamiento de estos, por medios de interacciones no clasicas como podrian ser la voz y/o texto, asi ir pudiendo guiar al usuario y a su vez poder entender lo que realmente necesita y asi indicar una recomendacion adecuada.

Durante este ultimo tiempo este tipo de sistemas a tomado mas auge ya que hoy en dia existen herramientas de Reinforced Learning y Machine Learning, los cuales hacen que este sea mucho mas usable, asi tambien la cantidad de informacion existente es muchisima.

### Arquitectura Global

En una generalidad un sistema de este tipo posee dos componentes principales

1. Active listeting: un engine de conversacion el cual acepta una entrada del usuario este podria ser un chat. y otro componente de recomendacion el cual retorna resultados en funcion de la atencion de la conversacion.

2. Personal Insight: sistema de inferencia, entiende al usuario e infiere personalidad y este se unne con el componente de recomendacion para retornar resultados (recomendaciones)

### Funcionamiento Basico

Como se menciono anteriormente el sistema se compone de dos

#### Input
Historial de dialogo: ultima n interaciones con el sistema
**Opcional** Preferencias del usuario: datos latentes sobre el usuario, como clicks, compra, perfil
**Opcional** Informacion adicional de items: datos latentes de los items como categorias y metadata


#### Output
proxima respuesta del sistema para interactuar (en turnos)
items recomendadios para el usuario (una o multiples veces)
opt: una explicacion de porque esta recomendado algo


#### Tipos de Sistemas

- **SAUP** - Sistema Avtivo, usuario pasivo: el sistena guia la conversacion al preguntarle al usuario y el usuario solo puede responder directamente (alternativas)

- **SAUE** - Sistema Activo, Usuario participando: Existe relacion y no necesariamente le usuario responde lo que quiere o pregunta el sistema, asi el sistema va viendo los mensajes y puede recomendar de una mejor forma

- **SUAU** - Sistema Activo, Usuario Activo: ambos pueden guiar la conversacion, el usuario pregunta sobre recomendacion y asi tambien pregunta para tener mas informacion

## Desafios

como se representan los dialogos y como se extraen, que fuentes se pueden utilizar

como extrar la informacion de los usuarios

decidir cuando responder y recomendar

que responder al usuario

que items recomendar

## Datos

Existen 


## Evaluacion

academia;
1. evaluar sistemas para mejorar el estado del arte
2. encontrar nuevas formas de resolver el problema
3. proponer nuevmos modelos, arquite

negocio
1. mejorar nivel de satisfaccion del usuario con la herramienta
2. mejorar metricas del negocio (ejemplo: incremento clicks, ventas, visitas)
3. demostrar el impacto del sistema a otros participanes

Evaluando la calidad de la conversacion

1. Turn-level Metrics:
   1. Calidad de las oraciones generadas por el chatbot (BLEU, ROUGE, legibilidad): metricas de machine translation y legilibidad
   2. relevancia de preguntas generadas por el chatbot (ground truth de preguntas, accuracy, recall): 
   3. Frecuencia y distrubucion de acciones tomadas por el chatbot (recomendar, chatear, preguntar)
   4. Nivel de cooperacion del usuaro( cuando responde el usuario a las preguntas del chatbot)
2. Dialogue-Level metrics:
   1. Largo de los dialogos
   2. Ratio dialogo satisfactorio y cumplimiento de tareas (recomendar, preguntar)
3. Business-Level metrics:
   1. conversion-rate por sesion de chats
   2. incremento de ventas
   3. satisfaccion del usuario, ratings, retencion de clientes, lealtard de clientes, etc


# Modelo

Primeramente se acepta una entrada (user query) y luego el sistema debe responder algo, internamente se compone de cinco grandes modulos:

1. NLU/NLG: Modulo de natural language understanding / generation, el cual se encarga de enteder la entrada del usuario y generar dialogos
2. Dialoge State Managenmente: Controla quien es el que habla y que acciones se va a tomar
3. Sistema recomendador: encargado de geneerar la recomendacion deseada en funcion de la finalidad de este y la entrada de los datos
4. Explicacion opcional: Mostrar porque al usuario se le realizo deicha recomendacion
5. Knowledge: Conocimiento externo del usuario, como su perfil, clicks, compras, items, etc.
   

![_config.yml]({{ site.baseurl }}/images/arquitectura_conversacional.png)
