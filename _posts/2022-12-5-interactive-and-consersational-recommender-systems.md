---
layout: post
title: "Clase 8: Interactive and Conversional Recommender Systems"
---

## Sistema Recomendadores Conversasionales


### Intro motivacion

2010 es cuando fue mas explotado


Inicalmente exis sistema basado en propuestas inicial que se refina a trabes de criticas del usuario, es decir que se ve afectado por un feedback del usuario, el cual recibe la informacion junto a un input de interaccion y el usuario puede decir.


es un sistema recomendador que da sugenrencias personalizadas a traves de lenguaje natural con un sistema, podrian ser voz o texto

la finalidad es poder transformar la experiencia de los usuarios en una forma natural del comportamiento de estos, la cual podria ser la voz

principales componentes podrian ser NLP, Language Understanding y Programacion que permiten a una computadora imitar y llevar a cabo conversaciones con personas.

para ello el modelo debe ser capaz de ir guiando al usuario para la finalidad buscada

busca entendeer las necesidades del usuarios


se puede hacer un test de turing para ver identificar si este proceso es real o no
evalua la capacidad de evaluar la capacidad de un computador

Arquitectura global
se compone de dos componentes
1. Active listeting: un engine de conversacion el cual acepta una entrada del usuario este podria ser un chat y otro componente de recomendacion el cual retorna resultados en funcion de la atencion de la conversacion

2. Personal Insight: sistema de inferencia, entiende al usuario e infiere personalidad y este se unne con el componente de recomendacion para retornar resultados (recomendaciones)


Esto busca conocer la personalidad del usuario, esto quiere decir poder entender las necesidades para asi poder generar recomendaciones mas acertadas


## Porque es importante

este tiempo ha tomado mas auge gracias a las tecnicas de reinforcement learning y deep learning, ya que los hace mas usable.

sirve para extraer de manera dinamica mas feedback del usuario y asi sus patrones de uso

mas datos nos permiten mejorar mas aun estos modelos conversacionales


# formalizar el problema

input:
Historial de dialogo: ultima n interaciones con el sistema
opt preferencias del usuario: datos latentes sobre el usuario, como clicks, compra, perfil
opt informacion adicional de items: datos latentes de los items como categorias y data


salida: 
proxima respuesta del; istema para interactuar (en turnos)
items recomendadios para el usuario (una o multiples veces)
opt: una explicacion de porque esta recomendado algo

Tipo 1: Sistema Avtivo, usuario pasivo SAUP: el sistena guia la conversacion al preguntarle al usuario y el usuario solo puede responder directamente (alternativas)

1. El sistema pregunta sobre atributos de items para acotar la lista de posibles candidatos a recomendar

Tipo 2: Sistema Activo,. usuario participando SAUE: El sitema hace las preguntas y el usuario las responde, hay un mayor grado de participacion

existe relacion y no necesariamente le usuario responde lo que quiere o pregunta el sistema, asi el sistema va viendo los mensajes y puede recomendar de una mejor forma

Tipo 3: Sistema Activo, Usuario Activo SUAU: ambos pueden guiar la conversacion

el usuario pregunta sobre recomendacion y asi tambien pregunta para tener mas informacion

Usuarios es activo, Sitema pasivo (voice command, Q&A):
el sitema esta escuchadno siempre pero no interactua, el usuario guia la conversacion


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

se compone de modulos:
1. entrada de datos


![_config.yml]({{ site.baseurl }}/images/arquitectura_conversacional.png)
