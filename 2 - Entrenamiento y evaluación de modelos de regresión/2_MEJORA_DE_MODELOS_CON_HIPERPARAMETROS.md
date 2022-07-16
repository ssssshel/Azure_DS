## Mejora de los modelos con hiperparámetros

A menudo, los modelos simples con conjuntos de datos pequeños se pueden ajustar en un solo paso, mientras que los conjuntos de datos más grandes y los modelos más complejos deben ajustarse mediante el uso repetido del modelo con datos de entrenamiento y la comparación de la salida con la etiqueta esperada. Si la predicción es lo suficientemente precisa, consideramos que el modelo está entrenado. Si no es así, se ajusta ligeramente el modelo y se vuelve a repetir.

Los hiperparámetros son valores que cambian la forma en que el modelo se ajusta durante estos bucles. La velocidad de aprendizaje, por ejemplo, es un hiperparámetro que establece cuánto se ajusta un modelo durante cada ciclo de entrenamiento. Una alta velocidad de aprendizaje significa que un modelo se puede entrenar más rápido, pero si es demasiado alta, los ajustes pueden ser tan grandes que el modelo nunca termine de ajustarse y no sea óptimo.

### Preprocesamiento de datos

El preprocesamiento hace referencia a los cambios realizados en los datos antes de pasarse al modelo. Ya hemos leído que el preprocesamiento puede implicar la limpieza del conjunto de datos. Aunque esto es importante, el preprocesamiento también puede incluir el cambio del formato de los datos para que el modelo los pueda usar más fácilmente. Por ejemplo, los datos descritos como "rojo", "naranja", "amarillo", "lima" y "verde", pueden funcionar mejor si se convierten en un formato más nativo para los equipos, como números que indican la cantidad de rojo y la cantidad de verde.

### Características de escalado

El paso de preprocesamiento más común consiste en escalar las características para se encuentren entre cero y uno. Por ejemplo, el peso de una bicicleta y la distancia que una persona recorre en una bicicleta pueden ser dos números muy diferentes, pero al escalar ambos números a entre cero y uno, los modelos pueden aprender de los datos con mayor eficacia.

### Uso de categorías como características

En el aprendizaje automático, también se pueden usar características de categorías como "bicicleta", "monopatín" o "automóvil". Estas características se representan mediante valores de 0 o 1 en vectores one-hot, vectores que tienen 0 o 1 para cada valor posible. Por ejemplo, la bicicleta, el monopatín y el automóvil podrían ser respectivamente (1,0,0), (0,1,0) y (0,0,1).