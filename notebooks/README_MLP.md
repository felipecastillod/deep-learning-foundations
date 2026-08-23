# Perceptrón Multicapa (MLP) – Red Neuronal Feed Forward

## Descripción General

Este notebook presenta la construcción y entrenamiento de una Red Neuronal Feed Forward utilizando la arquitectura Multilayer Perceptron (MLP).

El objetivo es comprender cómo múltiples capas de neuronas permiten aprender patrones complejos a partir de datos y resolver problemas de clasificación multiclase.

La implementación utiliza TensorFlow/Keras y se aplica al conjunto de datos MNIST, uno de los datasets más utilizados para la enseñanza de Deep Learning.

---

## Objetivos de Aprendizaje

- Comprender la arquitectura de una red neuronal Feed Forward.
- Entender la función de las capas ocultas.
- Aplicar funciones de activación ReLU y Softmax.
- Entrenar una red neuronal mediante descenso de gradiente estocástico (SGD).
- Analizar la evolución de la pérdida (Loss).
- Evaluar la precisión (Accuracy) del modelo.
- Realizar predicciones sobre imágenes no vistas.

---

## Dataset Utilizado

### MNIST

El conjunto de datos MNIST contiene imágenes de dígitos manuscritos del 0 al 9.

Características:

- 60.000 imágenes para entrenamiento.
- 10 clases de salida.
- Imágenes de 28 x 28 píxeles.
- Problema de clasificación multiclase.

---

## Arquitectura de la Red

La red neuronal implementada posee tres capas:

### Capa de Entrada

- 784 neuronas (28 × 28 píxeles)

### Primera Capa Oculta

- 64 neuronas
- Función de activación ReLU

### Segunda Capa Oculta

- 32 neuronas
- Función de activación ReLU

### Capa de Salida

- 10 neuronas
- Función de activación Softmax

Representación conceptual:

Entrada (784)
↓
Dense (64) + ReLU
↓
Dense (32) + ReLU
↓
Dense (10) + Softmax
↓
Clasificación de Dígitos

---

## Tecnologías Utilizadas

- Python
- NumPy
- TensorFlow
- Keras
- Matplotlib

---

## Proceso de Entrenamiento

El modelo se entrena utilizando:

- Función de pérdida: Categorical Crossentropy
- Optimizador: SGD (Stochastic Gradient Descent)
- Métrica: Accuracy
- Épocas: 5

Durante el entrenamiento se monitorean:

- Evolución de la pérdida (Loss)
- Evolución de la precisión (Accuracy)

---

## Conceptos Relacionados

- Perceptrón
- Redes Neuronales Artificiales
- Feed Forward Neural Networks
- Funciones de Activación
- ReLU
- Softmax
- Backpropagation
- Descenso por Gradiente
- Clasificación Multiclase

---

## Estructura del Proyecto

```text
deep-learning-foundations/

├── notebooks/
│   ├── 0_2_Multilayer_Perceptron_(MLP).ipynb
│   └── README_MLP_FeedForward.md
│
└── images/
    └── Image_MLP_FeedForward.png
```

---

## Autor

Felipe Castillo Ducaud

Industrial AI Review (IIAR)
