# Evaluación de diferentes tipos de agrupación en clústeres

## Entrenamiento de un modelo de agrupación en clústeres

Hay varios algoritmos que puede usar para la agrupación en clústeres. Uno de los algoritmos más usados es la agrupación en clústeres k-means que, en su forma más sencilla, comprende los pasos siguientes:

    1. Los valores de las características se vectorizan para definir coordenadas de n dimensiones (donde n es el número de características). En el ejemplo de las flores, tenemos dos características (el número de pétalos y el número de hojas), por lo que el vector de características tiene dos coordenadas que se pueden usar para trazar conceptualmente los puntos de datos en un espacio de dos dimensiones.
    2. Decida cuántos clústeres quiere usar para agrupar las flores y llame a este valor k. Por ejemplo, para crear tres clústeres, usaría un valor k de 3. Después, se representan los puntos k en coordenadas aleatorias. En última instancia, estos puntos serán los puntos centrales de cada clúster, por lo que se hace referencia a ellos como centroides.
    3. Cada punto de datos (en este caso, cada flor) se asigna a su centroide más cercano.
    4. Cada centroide se mueve al centro de los puntos de datos asignados en función de la distancia media entre los puntos.
    5. Después de mover el centroide, los puntos de datos pueden pasar a estar más cerca de otro centroide, por lo que se reasignan a los clústeres en función del nuevo centroide más cercano.
    6. Los pasos de movimiento de centroides y reasignación de clústeres se repiten hasta que los clústeres se estabilizan o se alcanza un número máximo predeterminado de iteraciones.

En la siguiente animación se ilustra este proceso:

![graph1](https://docs.microsoft.com/es-es/learn/modules/train-evaluate-cluster-models/media/k-means.gif)

## Agrupación en clústeres jerárquica

La agrupación en clústeres jerárquica es otro tipo de algoritmo de agrupación en clústeres en el que los propios clústeres pertenecen a un grupo más grande, que pertenecen a grupos incluso más grandes, y así sucesivamente. El resultado es que los puntos de datos pueden agruparse con diferentes grados de precisión: con un gran número de grupos muy pequeños y precisos, o con un pequeño número de grupos más grandes.

Por ejemplo, si aplicamos la agrupación a los significados de las palabras, podemos obtener un grupo que contenga adjetivos específicos de las emociones ("enfadado", "feliz", etc.), que a su vez pertenezca a un grupo que contenga todos los adjetivos relacionados con el ser humano ("feliz", "guapo", "joven"), y este a su vez pertenezca a un grupo aún mayor que contenga todos los adjetivos ("feliz", "verde", "guapo", "duro", etc.).

![graph2](https://docs.microsoft.com/es-es/learn/modules/train-evaluate-cluster-models/media/4-hierarchical-clustering.png)

La agrupación en clústeres jerárquicas es útil no solo para dividir los datos en grupos, sino también para comprender las relaciones entre estos grupos. Una ventaja importante de la agrupación en clústeres jerárquica es que no requiere que el número de clústeres se defina de antemano y, a veces, puede proporcionar resultados más interpretables que los enfoques no jerárquicos. El principal inconveniente es que estos enfoques pueden tardar mucho más tiempo en calcularse que los enfoques más sencillos y, a veces, no son adecuados para grandes conjuntos de datos.