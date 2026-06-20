# Detección de Lesiones Cutáneas y Cáncer de Piel (ISIC 2016 - Task 3)

Este repositorio contiene el desarrollo de una solución basada en **Visión Artificial y Deep Learning** para la clasificación binaria de imágenes médicas de lesiones cutáneas (Benignas frente a Malignas) utilizando el dataset público de la competición internacional **ISIC 2016 (International Skin Imaging Collaboration)**.

El objetivo principal de este módulo inicial es realizar un Análisis Exploratorio de Datos (EDA) robusto y automatizar todo el pipeline de preprocesamiento, limpieza y estructuración jerárquica de las imágenes para prepararlas de cara al entrenamiento de Redes Neuronales Convolucionales (CNNs)[cite: 1].

## 🚀 Características del Proyecto

* **Análisis Exploratorio de Datos (EDA):** Evaluación del desbalanceo de clases y visualización analítica de las dimensiones de las muestras médicas[cite: 1].
* **Pipeline de Datos Automatizado:** Conversión y unificación automática de etiquetas heterogéneas (flotantes a cadenas de texto) entre los conjuntos de entrenamiento y prueba[cite: 1].
* **Estructuración de Directorios:** Segmentación e instanciación automatizada de las imágenes en directorios compatibles con los cargadores nativos de Keras (`image_dataset_from_directory`)[cite: 1].
* **Optimización de Hardware:** Rutina de verificación y mapeo de aceleradores por hardware (GPUs duales) utilizando el backend de TensorFlow[cite: 1].

## 📊 El Dataset[cite: 1]

El proyecto trabaja sobre el dataset **ISBI 2016 Part 3 (Task 3)**[cite: 1]. Se compone de un total de **1,279 imágenes de dermatoscopia** de alta resolución distribuidas de la siguiente manera[cite: 1]:

* **Conjunto de Entrenamiento (Train):** 900 imágenes[cite: 1]
  * *Benignas:* 727 muestras (80.78%)[cite: 1]
  * *Malignas:* 173 muestras (19.22%)[cite: 1]
* **Conjunto de Prueba (Test):** 379 imágenes[cite: 1]
  * *Benignas:* 304 muestras[cite: 1]
  * *Malignas:* 75 muestras[cite: 1]

## 📁 Estructura del Dataset Generado[cite: 1]

El script genera automáticamente la siguiente arquitectura jerárquica para un consumo eficiente por lotes (Batch processing)[cite: 1]:

```text
└── dataset/
    ├── train/
    │   ├── benign/       --> [727 imágenes]
    │   └── malignant/    --> [173 imágenes]
    └── test/
        ├── benign/       --> [304 imágenes]
        └── malignant/    --> [75 imágenes]
```[cite: 1]

## 🛠️ Stack Tecnológico

* **Core:** Python 3[cite: 1]
* **Deep Learning Framework:** TensorFlow 2.19.0 / Keras[cite: 1]
* **Procesamiento de Datos:** Pandas, NumPy[cite: 1]
* **Manejo de Archivos:** Pathlib, SHUtil[cite: 1]
* **Procesamiento de Imágenes:** PIL (Pillow)[cite: 1]
* **Visualización y Métricas:** Matplotlib, Seaborn, Scikit-Learn[cite: 1]

## 💻 Instrucciones de Ejecución

1. **Clonar el repositorio:**
```bash
   git clone [https://github.com/EnyiXZ/skin-lesion-classification-isic2016.git](https://github.com/EnyiXZ/skin-lesion-classification-isic2016.git)
   cd skin-lesion-classification-isic2016

recomendacion de usar kaggle con el accelerator GPU T4 X2
