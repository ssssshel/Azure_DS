# ¿Qué es la agrupación en clústeres?

La agrupación en clústeres es un tipo de aprendizaje automático sin supervisión en el que las observaciones se agrupan en clústeres en función de las similitudes en sus valores de datos o características. Este tipo de aprendizaje automático se considera no supervisado porque no usa valores de etiqueta conocidos previamente para entrenar un modelo. En un modelo de agrupación en clústeres, la etiqueta es el clúster al que se asigna la observación, únicamente en función en sus características.

Por ejemplo, supongamos que un botánico observa una muestra de flores y registra el número de pétalos y hojas en cada flor.

Puede ser útil agrupar estas flores en clústeres en función de las similitudes entre sus características.

Hay muchas maneras de hacerlo. Por ejemplo, si la mayoría de las flores tienen el mismo número de hojas, podrían agruparse en aquellas con muchos o pocos pétalos. Por otra parte, si el número de pétalos y hojas varía considerablemente, puede haber un patrón que detectar, como que las que tienen muchas hojas también tienen muchos pétalos. El objetivo del algoritmo de agrupación en clústeres es encontrar la manera óptima de dividir el conjunto de datos en grupos. El significado de "óptima" depende del algoritmo utilizado y del conjunto de datos que se proporciona.

Aunque este ejemplo de la flor puede ser sencillo para un humano con solo unas pocas muestras, a medida que el conjunto de datos crece a miles de muestras o a más de dos características, los algoritmos de agrupación en clústeres se vuelven muy útiles para diseccionar rápidamente un conjunto de datos en grupos.