# Perceptrón Multicapa (MLP): Introducción a las Redes Neuronales Feed Forward

---

## Descripción

El Perceptrón Multicapa (Multilayer Perceptron, MLP) representa la evolución natural del perceptrón simple y constituye una de las arquitecturas fundamentales del Deep Learning moderno.

Mientras que un perceptrón puede resolver únicamente problemas linealmente separables, un MLP incorpora una o más capas ocultas que permiten modelar relaciones no lineales y aprender patrones significativamente más complejos.

Este notebook presenta la construcción y entrenamiento de una red neuronal Feed Forward utilizando TensorFlow/Keras sobre el dataset MNIST, uno de los conjuntos de datos más utilizados para la enseñanza de Redes Neuronales Artificiales.

---

## ¿Por qué es importante un MLP?

Los problemas reales rara vez presentan relaciones lineales simples.

Aplicaciones como:

- Reconocimiento de imágenes
- Procesamiento de lenguaje natural
- Detección de fraude
- Diagnóstico médico
- Sistemas de recomendación

requieren arquitecturas capaces de aprender representaciones más complejas de los datos.

El MLP fue una de las primeras arquitecturas capaces de superar las limitaciones del perceptrón tradicional y sentó las bases para el desarrollo de las redes neuronales profundas actuales.

---

## Objetivos de Aprendizaje

Al finalizar este notebook serás capaz de:

- Comprender la arquitectura de una red neuronal Feed Forward.
- Diferenciar un Perceptrón simple de un Perceptrón Multicapa.
- Entender el rol de las capas ocultas.
- Aplicar funciones de activación no lineales.
- Comprender el proceso de entrenamiento mediante Backpropagation.
- Analizar métricas de desempeño de una red neuronal.
- Realizar predicciones sobre datos no observados durante el entrenamiento.

---

## Dataset Utilizado

### MNIST

MNIST es uno de los datasets más conocidos en Machine Learning y Deep Learning.

Contiene imágenes de dígitos manuscritos desde el 0 hasta el 9.

| Característica | Valor |
|---------------|--------|
| Imágenes de entrenamiento | 60.000 |
| Imágenes de prueba | 10.000 |
| Resolución | 28 × 28 píxeles |
| Número de clases | 10 |
| Tipo de problema | Clasificación multiclase |

Cada imagen se transforma en un vector de 784 características (28 × 28 píxeles) que será utilizado como entrada para la red neuronal.

---

## Arquitectura Implementada

La arquitectura desarrollada en este notebook corresponde a una red neuronal Feed Forward compuesta por múltiples capas densamente conectadas.

### Capa de Entrada

Recibe los píxeles de cada imagen.

- 784 neuronas
- Corresponde a una imagen de 28 × 28 píxeles

### Primera Capa Oculta

- 64 neuronas
- Función de activación ReLU

### Segunda Capa Oculta

- 32 neuronas
- Función de activación ReLU

### Capa de Salida

- 10 neuronas
- Función de activación Softmax

Cada neurona representa la probabilidad de pertenencia a uno de los diez dígitos posibles.

---

## Flujo de Información

```text
Imagen de Entrada
        ↓
Vector de 784 características
        ↓
Capa Oculta (64)
        ↓
Capa Oculta (32)
        ↓
Capa de Salida (10)
        ↓
Probabilidades Softmax
        ↓
Predicción Final
```

---

## Conceptos Fundamentales

### Feed Forward

La información avanza únicamente desde la entrada hacia la salida.

No existen ciclos ni retroalimentación entre neuronas.

---

### Función de Activación ReLU

La función ReLU (Rectified Linear Unit) introduce no linealidad en la red neuronal.

Gracias a ella, el modelo puede aprender relaciones complejas presentes en los datos.

---

### Softmax

Convierte las salidas de la última capa en probabilidades.

La suma de todas las probabilidades generadas es igual a 1.

---

### Backpropagation

Algoritmo utilizado para ajustar los pesos de la red neuronal.

Propaga el error desde la salida hacia las capas anteriores permitiendo mejorar progresivamente el aprendizaje.

---

### Descenso por Gradiente

Método de optimización encargado de minimizar el error del modelo actualizando los pesos en cada iteración.

---

## Entrenamiento del Modelo

El entrenamiento se realiza utilizando:

- TensorFlow / Keras
- Función de pérdida: Categorical Crossentropy
- Optimizador: SGD (Stochastic Gradient Descent)
- Métrica: Accuracy

Durante el proceso se monitorean:

- Evolución de la pérdida (Loss)
- Evolución de la precisión (Accuracy)

Estas métricas permiten evaluar la capacidad de aprendizaje del modelo a lo largo de las épocas.

---

## Relación con el Módulo 1

Este notebook corresponde al segundo paso dentro de los fundamentos de Redes Neuronales Artificiales.

```text
Perceptrón
      ↓
Perceptrón Multicapa (MLP)
      ↓
Funciones de Activación
      ↓
Backpropagation
      ↓
Gradient Descent
      ↓
Deep Learning
```

Comprender esta secuencia resulta fundamental para avanzar hacia arquitecturas más complejas como Redes Convolucionales (CNN), Redes Recurrentes (RNN) y Transformers.

---

## Estructura del Proyecto

```text
deep-learning-foundations/

├── notebooks/
│   ├── 0_2_Multilayer_Perceptron_(MLP).ipynb
│   └── README_MLP.md
│
└── images/
    └── Image_MLP_FeedForward.png
```

---

## Autor

**Felipe Castillo Ducaud**

Founder & Editor — Industrial AI Review (IIAR)

PhD Researcher | Artificial Intelligence | Deep Learning | Industrial Digital Transformation
