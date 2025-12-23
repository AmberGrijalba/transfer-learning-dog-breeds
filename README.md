# Transfer Learning para Clasificación de Razas de Perros 🐶

Este repositorio presenta la implementación de un modelo de **Transfer Learning** para la **clasificación de razas de perros** a partir de imágenes, utilizando redes neuronales convolucionales profundas preentrenadas en **ImageNet**. El proyecto fue desarrollado en **Google Colab** y tiene como objetivo demostrar el uso práctico del aprendizaje por transferencia, incluyendo entrenamiento, fine-tuning y evaluación del modelo.

---

## 📌 Objetivo del Proyecto

Aplicar el enfoque de **Transfer Learning** para adaptar un modelo CNN preentrenado a un nuevo problema de clasificación multiclase, logrando un desempeño adecuado con un conjunto de datos limitado y evaluando el modelo mediante métricas cuantitativas y análisis visual.

---

## 📂 Dataset

Se utiliza el dataset **Dog Breeds Dataset** disponible en Kaggle, el cual contiene imágenes de diferentes razas de perros organizadas por carpetas, donde cada carpeta representa una clase distinta. Este tipo de estructura facilita la carga automática de los datos para tareas de clasificación supervisada.

---

## 🧠 Metodología

El desarrollo del proyecto sigue las siguientes etapas:

1. **Carga del dataset** y exploración inicial de las imágenes.
2. **Preprocesamiento** de datos:
   - Redimensionamiento de imágenes.
   - Normalización de valores de píxeles.
   - Aplicación de *data augmentation* (rotaciones, flips, zoom).
3. **Selección del modelo base**:
   - Se emplea **EfficientNetB0** con pesos preentrenados en ImageNet.
4. **Transfer Learning**:
   - Se eliminan las capas finales del modelo original (`include_top=False`).
   - Se congelan las capas del modelo base.
   - Se agrega una nueva cabeza de clasificación acorde al número de razas.
5. **Entrenamiento inicial** del modelo con capas congeladas.
6. **Fine-Tuning**:
   - Se descongelan parcialmente las capas superiores del modelo base.
   - Se ajusta la tasa de aprendizaje para mejorar la generalización.
7. **Evaluación del modelo**:
   - Accuracy
   - Top-3 Accuracy
   - Matriz de confusión
   - Reporte de clasificación
8. **Análisis cualitativo**:
   - Comparación visual entre etiquetas reales y predicciones del modelo.

---

## 📊 Resultados

El modelo logró un desempeño satisfactorio en la clasificación multiclase de razas de perros, evidenciando que el uso de Transfer Learning permite aprovechar el conocimiento previo adquirido por modelos entrenados en grandes conjuntos de datos. El fine-tuning contribuyó a mejorar la precisión y la capacidad de discriminación entre razas visualmente similares.

Las visualizaciones de entrenamiento, la matriz de confusión y los ejemplos de predicciones permiten analizar tanto el comportamiento global del modelo como sus aciertos y errores específicos.

---

## 🖼️ Ejemplos de Predicción

En el notebook se incluyen ejemplos visuales donde se comparan:
- La **raza real** del perro.
- La **raza predicha** por el modelo.
- Las **predicciones Top-3** con sus probabilidades.

Estas visualizaciones facilitan una evaluación cualitativa del desempeño del modelo.

---

## 🛠️ Tecnologías Utilizadas

- **Python**
- **TensorFlow / Keras**
- **Google Colab**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**

---

## 📁 Estructura del Repositorio

