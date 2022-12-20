---
layout: post
title: Graph Based Recommender Systems
---

## Graph Based Recommender Systems

Nace en al año 2008, por Scarcelli, por una red neuronal de grafos, un grafo es una forma de representar una red, que consiste en nodos(objetos) que se encuentran conectados mediante vértices (enlaces) los cuales explican una relación entre estos.
 
La idea general de una red neuronal de grafos es poder tomar una red(grafo) y llevarla a un espacio vectorial llamado embedding, la cual representa propiedades de la red y cómo se relacionan entre sí.
 
Existen dos formas de realizar este cálculo:
 
1. Filtro: es el cambio de atributos en nodos respecto a la interacción con los vecinos
 
2. Seleccion: Cambios en el grafo respecto a operaciones sobre el grafo (ex: Pooling)
 
 
# Convolución en un grafo
 
Para realizar esto se toma y se aplica una transformación sobre los atributos del nodo en función de sus vecinos.
 
 
## Tipos de aprendizaje
 
Aprendizaje transductivo: el modelo ve los datos tanto como de entrenamiento como test, si se agrega un nuevo nodo se entrena de nuevo.
 
aprendizaje inductivo: ve solo los datos de entrenamiento y si se agrega un nodo nuevo, se puede representar mediante los datos existentes.
 
 
### Para Sistemas de Recomendación
 
Es más fácil poder representar las interacciones y conexiones de elementos mediante grafos y así también aporta a la capacidad de aprender relaciones complejas.
 
 
## Clases de GNN
 
**Graph convolutional neural networks**: utilizan pooling y convoluciones para considerar la información de los nodos vecinos
 
**Gathered Graph Neural Networks**: se introduce una GRU para aprender representaciones de nodos absorbiendo iterativamente la influencia de otros nodos
 
**Attention Network (GAT)**: Se utilizan mecanismos de atención para aprender las distintas relevancias que tienen algunos usuarios (o ítems) sobre todo.
 
 
### Graph Sage
 
Permite escalar el aprendizaje de embeddings para los nodos a millones pero:
- Para K-vecinos grandes, crece exponencialmente el número de cálculos
- podemos encontrarnos con las maldiciones de nodos celebridades(que tengan demasiados vecinos)
 
paraGraph Sage realiza una muestra de los vecinos, acotando la cantidad de cálculos
 
1. muestrea vecindario, a diferentes profundidades dependiendo de qué forma están unidos
2. Agrega información de features de los vecinos(conexiones)
 
 
### Tipos de Entrenamiento para el calculo de perdidas
 
**Pérdida no supervisada**: similar al BPR, nodos conectados deben quedar más cerca entre ellos que nodos no conectados
 
**Supervisada**: hay etiquetas de los nodos, se puede supervisar el aprendizaje vía clasificaciones
 
 
### NGCG y LightGCx Para Recomendaciones
 
Filtrado colaborativo tradicional no captura explícitamente información de los nodos a k-hoops
 
#### NGCF
 
![_config.yml]({{ site.baseurl }}/images/gcn_formula.png)
 
 
Red neuronal que toma como entrada un nodo y el modelo aplica transformacion de caracteristicas que se aprender generando un embedding de datos, para ello tiene tres funciones principales:
1. Update: actualización en base a pesos
2. Agregate: cálculo de sumatoria
3. Message: paso de mensajes
 
 
#### Light GCN
 
![_config.yml]({{ site.baseurl }}/images/light_gcn.png)
 
 
No es necesario tener una red neuronal para ello se puede disminuir los parámetros de las capas de parámetros de las redes neuronales. bajo el supuesto que los embedding de los vecinos son lo suficientemente representativos.
 
Por ello solo queda la fórmula de agregación y el paso de mensajes.
Finalmente realiza una agregación final a través de una suma ponderada de los embedding de cada capa
