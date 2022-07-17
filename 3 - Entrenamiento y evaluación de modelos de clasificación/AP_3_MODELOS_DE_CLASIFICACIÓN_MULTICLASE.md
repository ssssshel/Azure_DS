# Creación de modelos de clasificación multiclase

También es posible crear modelos de clasificación multiclase, en los que hay más de dos clases posibles. Por ejemplo, el consultorio médico podría ampliar el modelo de diabetes para clasificar a los pacientes como:

    - No diabéticos
    - Diabéticos de tipo 1
    - Diabéticos de tipo 2

Los valores de probabilidad de las clases individuales aún sumarían un total de 1 (el paciente definitivamente está en una de las tres clases), y el modelo prediría la clase más probable.

### Uso de modelos de clasificación multiclase

La clasificación multiclase puede considerarse una combinación de varios clasificadores binarios. Hay dos maneras de abordar el problema:

    * Una frente al resto (OVR), en el que se crea un clasificador para cada valor de clase posible, con un resultado positivo para los casos en los que la predicción es esta clase y predicciones negativas para los casos en los que la predicción es cualquier otra clase. Por ejemplo, un problema de clasificación con cuatro clases de formas posibles (cuadrado, círculo, triángulo, hexágono) requeriría cuatro clasificadores que predigan:
        - cuadrado o no
        - círculo o no
        - triángulo o no
        - hexágono o no
    * Uno frente a uno (OVO), en el que se crea un clasificador para cada par de clases posible. El problema de clasificación con cuatro clases de formas requeriría los siguientes clasificadores binarios:
        - cuadrado o círculo
        - cuadrado o triángulo
        - cuadrado o hexágono
        - círculo o triángulo
        - círculo o hexágono
        - triángulo o hexágono

En los dos enfoques, el modelo general debe tener en cuenta todas estas predicciones para determinar a qué categoría única pertenece el elemento.

Afortunadamente, en la mayoría de los marcos de aprendizaje automático, incluido Scikit-learn, la implementación de un modelo de clasificación multiclase no es significativamente más compleja que la clasificación binaria y, en la mayoría de los casos, los estimadores utilizados para la clasificación binaria admiten implícitamente la clasificación multiclase abstrayendo un algoritmo OVR o un algoritmo OVO, o permitiendo la elección de cualquiera de ellos.