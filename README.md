## Description

En esta practica se genera un árbol de decisiones en Haskell a partir de un conjunto de datos Mushroom.
El árbol clasifica setas en venenosas o comestibles a partir de una muestra de 8124 ejemplos.

El algoritmo utilizado para la generación del arbol es ID3

## ID3
ID3 construye un árbol de decisiones a partir de un conjunto fijo de ejemplos. El árbol resultante se utiliza para clasificar muestras futuras. Los nodos hoja del árbol de decisión contienen el nombre de la clase (Comestible o venenoso), mientras que un nodo no hoja es un nodo de decisión. 

En cada iteración, el algoritmo calcula la entropia de todos los atributos no utilizados del conjunto de datos y se queda con el que tenga mayor ganancia de información. 
Posteriormente el atributo seleccionado se convierte en la raiz del subarbol y el conjunto de datos se divide por el atributo seleccionado en n subconjuntos(tantos como valores distintos tenga el atributo).
Si todos los elementos del subconjunto pertenecen a una única clase, este nodo se convierte en hoja. Si no se vuelve a realizar el procedimiento de arriba.

## Ganancia de información
Es la diferencia de la entropía antes y después de la división del conjunto. En otras palabras, cuánta incertidumbre se redujo después de dividir el conjunto por el atributo A.

![alt text](https://github.com/SoufianeAatab/PracticaLP-Haskell/blob/main/2.png)

La ganancia en la información es igual a la entropia del conjunto antes de la division menos la entropia despues de dividir el conjunto por el atributo A

## Installation
Para poder ejecutar la práctica hace falta el compilador de Haskell ghci.
Para compilar ejecuta el siguiente comando:

>ghc dts.hs

>./dts
  
## Usage
Al ejecutar el programa, este va a proceder a generar el árbol de decisiones a partir de la muestra "agaricus-lepiota.data".
Una vez generado el programa espera un input:

![alt text](https://github.com/SoufianeAatab/PracticaLP-Haskell/blob/main/1.png)


## Webgrafía

https://www.cise.ufl.edu/~ddd/cap6635/Fall-97/Short-papers/2.htm

https://en.wikipedia.org/wiki/ID3_algorithm#Entropy

https://en.wikipedia.org/wiki/Entropy_(information_theory)
