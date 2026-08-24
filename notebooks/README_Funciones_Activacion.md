# Funciones de Activación: Introduciendo la No Linealidad en Deep Learning

## Descripción

Las funciones de activación constituyen uno de los componentes más importantes de una red neuronal artificial.

Después de que una neurona calcula una combinación lineal de sus entradas, la función de activación determina cómo se transforma dicha información antes de ser transmitida a la siguiente capa.

Sin funciones de activación, incluso una red neuronal con múltiples capas sería matemáticamente equivalente a un modelo lineal simple, limitando severamente su capacidad de aprendizaje.

Este notebook explora las funciones de activación más relevantes en la historia del Deep Learning y analiza cómo cada una de ellas contribuyó a resolver desafíos específicos asociados al entrenamiento de redes neuronales profundas.

## ¿Por qué son importantes?

La mayoría de los problemas reales presentan relaciones altamente no lineales.

Aplicaciones como:

- Reconocimiento de imágenes
- Procesamiento de lenguaje natural
- Sistemas de recomendación
- Diagnóstico médico asistido por IA
- Detección de fraude

requieren modelos capaces de representar patrones complejos imposibles de capturar mediante transformaciones lineales.

Las funciones de activación son precisamente el mecanismo que introduce esta capacidad de modelado no lineal.

## Objetivos de Aprendizaje

Al finalizar este notebook serás capaz de:

- Comprender el propósito de una función de activación.
- Explicar por qué las redes neuronales necesitan no linealidad.
- Diferenciar las principales funciones utilizadas en Deep Learning.
- Comprender las ventajas y limitaciones de Sigmoid, Tanh, ReLU y Leaky ReLU.
- Entender los conceptos de Vanishing Gradient y Dead ReLU.
- Reconocer la evolución histórica de las funciones de activación modernas.

## Funciones Estudiadas

### Sigmoid

Fue una de las primeras funciones utilizadas en redes neuronales modernas.

Su principal característica consiste en transformar cualquier valor real en una salida comprendida entre 0 y 1, permitiendo interpretaciones probabilísticas.

Aunque tuvo una enorme relevancia histórica, presenta problemas de saturación que dificultan el entrenamiento de redes profundas.

### Tanh

La función Tangente Hiperbólica fue desarrollada para superar algunas limitaciones de Sigmoid.

Su salida se encuentra centrada en cero, lo que facilita la propagación de gradientes y mejora la estabilidad del entrenamiento.

Durante muchos años fue ampliamente utilizada en redes neuronales multicapa y arquitecturas recurrentes.

### ReLU

La función Rectified Linear Unit (ReLU) marcó uno de los mayores avances en la historia reciente del Deep Learning.

Su simplicidad matemática permite entrenar redes significativamente más profundas y eficientes.

La adopción masiva de ReLU fue uno de los factores que impulsó el renacimiento moderno de las redes neuronales profundas a partir de la década de 2010.

### Leaky ReLU

Leaky ReLU surge como una mejora de ReLU.

Introduce una pequeña pendiente para valores negativos, evitando que ciertas neuronas queden permanentemente inactivas durante el entrenamiento.

Esta modificación contribuye a mantener el flujo de gradientes y mejorar la capacidad de aprendizaje del modelo.

## Problemas Clave Analizados

### Vanishing Gradient

Algunas funciones de activación producen gradientes extremadamente pequeños durante el proceso de entrenamiento.

Cuando esto ocurre, las capas profundas reciben muy poca información para actualizar sus parámetros, dificultando el aprendizaje efectivo.

Este fenómeno fue uno de los principales obstáculos para el desarrollo temprano del Deep Learning.

### Dead ReLU

Las neuronas basadas en ReLU pueden quedar atrapadas permanentemente en la región negativa de la función.

Cuando esto ocurre dejan de actualizar sus pesos y dejan de contribuir al aprendizaje de la red.

Este problema motivó el desarrollo de variantes como Leaky ReLU, Parametric ReLU y otras funciones modernas.

## Evolución hacia Arquitecturas Modernas

Las arquitecturas actuales utilizan funciones de activación más sofisticadas, entre ellas:

- GELU
- Swish
- Mish

Modelos de última generación como GPT, BERT, Gemini y Claude emplean variantes modernas diseñadas para optimizar el flujo de gradientes y mejorar la capacidad de representación de las redes profundas.

Sin embargo, comprender Sigmoid, Tanh, ReLU y Leaky ReLU continúa siendo fundamental para entender la evolución conceptual del Deep Learning.

---

## Autor

**Felipe Castillo Ducaud**

Founder & Editor — Industrial AI Review (IIAR)

MBA | Artificial Intelligence | Deep Learning | Industrial Digital Transformation
