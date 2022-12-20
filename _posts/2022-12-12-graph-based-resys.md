---
layout: post
title: Graph Based Recommended Systems
---

Un grafo es una forma de representar una red, consistiendo en nodos objetos que se encuentran conectados median enlaces

es natural modelar un problema de recomendacion como un problema de grafos


Nace en al año 2008, por Scarcselli, por una red neuronal de grafos,

la idea general es poder tomar una red(grafo) y llevarla a un espacio vectorial llamado embedding, la cual representa propiedades de la red.

Filtro: es el cambio de atributos en nodos respecto a la interaccion con los vecinos

Seleccion: Cambios en el grafo respecto a operaciones sobre el grafo (ex: Pooling)


# Convolucion en un grafo

Para realizar esto se toma y se aplica una transformacion sobre los atributos del nodo en funcion de sus vecinos.


## Tipos de aprendizaje

Aprendizaje transductivo: el modelo ve los datos tanto como de entrenamiento como test, si se agrega un nuevo nodo se entrena denuevo

aprendizaje indctivo: ve solo los datos de entrenamiento y si se agrega un nodo nuevo, se puede representar mediante los datos existentes.


### Para Recomendacion

Es mas facil poder representar las interacciones y conexiones de elementos mediante grafos
Capacidad de aprender relaciones complejas


## Clases de GNN

Greaph convolutional neural networks: utilizan poooling y convoluciones para considerar la informacion de los nodos vecisnos

Gathed Graph Neural Networks: se introduce una GRU para aprender representaciones de nodos absorviendo iterativamente la influencia de otros nodos

Attention Network (GAT): Se utiliza mecanismos de atencion para aprender las distintas relevancias que tienen algunos uusarios (o items) sobre todo.


### Grapg sage

Permite escalar el aprendizaje de embeddings para los nodos a millons pero
- Para u K grande, crece exponencialmente el numero de calculos
- podemos encontrarnos con las maldiciones de nodos celebridades(que tengan demasiados vecinos)

para grap sage realiza una muestra de los vecinos, acotando la cantidad de calculos

1. muestrea vecindario, a diferentes profundidaes dependiendo de que forma esten unidos
2. Agrega informacion de features de los vecinos(conexiones)


se crean nodos agregadores
el nodo se inicialiazan con caracteristicas originales
el roceso iterativo se llama message passing