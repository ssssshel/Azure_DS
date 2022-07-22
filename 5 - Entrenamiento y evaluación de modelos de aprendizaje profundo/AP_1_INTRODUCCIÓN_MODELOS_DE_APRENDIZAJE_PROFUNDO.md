# Introducción

El aprendizaje profundo es una forma avanzada de aprendizaje automático que intenta emular el modo en que el cerebro humano aprende.

El cerebro tiene células nerviosas, las neuronas, que están conectadas entre sí por extensiones nerviosas que transmiten señales electroquímicas a través de la red.

![graph1](https://docs.microsoft.com/es-es/learn/modules/train-evaluate-deep-learn-models/media/human-brain.png)

Cuando se estimula la primera neurona de la red, se procesa la señal de entrada y, si supera un umbral determinado, el neurona se activa y transmite la señal a las neuronas con las que está conectada. A su vez, estas neuronas se pueden activar y transmitir la señal a través del resto de la red. Con el tiempo, las conexiones entre los neuronas se refuerzan por el uso frecuente a medida que aprende a responder de forma eficaz. Por ejemplo, si alguien le lanza un balón, sus conexiones neuronales le permiten procesar la información visual y coordinar los movimientos para atraparlo. Si realiza esta acción varias veces, la red de neuronas que le permite atrapar un balón será más fuerte y, por lo tanto, mejorará a la hora de atrapar un balón.

El aprendizaje profundo emula este proceso biológico mediante redes neuronal artificiales que procesan entradas numéricas en lugar de estímulos electroquímicos.

![graph2](https://docs.microsoft.com/es-es/learn/modules/train-evaluate-deep-learn-models/media/artificial-neural-network.**png**)

Las conexiones nerviosas entrantes se reemplazan por entradas numéricas que se suelen identificar como x. Cuando hay más de un valor de entrada, x se considera vector con elementos denominados x1, x2, y así sucesivamente.

Asociado con cada valor x hay un valor ponderación (w), que se usa para fortalecer o debilitar el efecto del valor x para simular el aprendizaje. Además, se agrega una entrada sesgo (b) para permitir el control específico sobre la red. Durante el proceso de entrenamiento, se ajustarán los valores w y b para optimizar la red de modo que "aprenda" a generar los resultados correctos.

La neurona misma encapsula una función que calcula una suma ponderada de x, w y b. A su vez, esta función se encuentra en una función de activación que restringe el resultado (por lo general, a un valor entre 0 y 1) a fin de determinar si la neurona transmite o no un resultado a la capa siguiente de neuronas de la red.