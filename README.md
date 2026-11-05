# Introducción al Aprendizaje Máquina

Repositorio con las instrucciones de las actividades de la materia **Introducción al Aprendizaje Máquina**. Las descripciones se copiaron desde Notion para tenerlas a la mano (por ejemplo, para trabajar con asistentes de IA que no pueden abrir los links).

## Contenido del repositorio

| Elemento | Descripción |
|---|---|
| `Actividades Machine Learning.md` | Archivo original con los links de Notion y el texto copiado de cada actividad. |
| `NN_<actividad>/descripcion.md` | Descripción exacta de la actividad, con el link a Notion al inicio. |
| `NN_<actividad>/resumen.md` | Resumen sencillo de lo que hay que hacer. |

## Contexto

- **AF 1, AF 2 y AF 3** (Actividades Fundamentales) usan el mismo dataset: [Stroke Prediction (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset).
  - La AF 1 limpia el dataset.
  - La AF 2 y la AF 3 parten del dataset ya limpio de la AF 1.
  - Por eso conviene hacer las actividades en orden.
- **Proyecto final:** clasificación de gestos (piedra, papel o tijera) con una CNN, usando el dataset [Rock, Paper, Scissors](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors).
- Las actividades se hacen en equipo, en notebooks de Python (Google Colab o Jupyter) con `pandas`, `numpy`, `matplotlib`, `scikit-learn` y `TensorFlow/Keras`.
- Cada actividad pide un documento con portada, introducción, desarrollo (con el link al repo de GitHub con el notebook), conclusión y referencias. El proyecto final se entrega en PDF.

## Actividades

| # | Actividad | Tema | Carpeta | Notion |
|---|---|---|---|---|
| 1 | AF 1: Introducción al Aprendizaje Máquina | Análisis exploratorio y preprocesamiento de datos (EDA) | [01_AF1_EDA_y_Preprocesamiento](01_AF1_EDA_y_Preprocesamiento) | [Abrir](https://geode-cloud-e9e.notion.site/AF-1-Introducci-n-al-Aprendizaje-M-quina-3de0ddbf1878805b956ed15e1361153f) |
| 2 | AF 2: Introducción al Aprendizaje Máquina | Modelos de aprendizaje supervisado (red neuronal) | [02_AF2_Aprendizaje_Supervisado](02_AF2_Aprendizaje_Supervisado) | [Abrir](https://geode-cloud-e9e.notion.site/AF-2-Introducci-n-al-Aprendizaje-M-quina-4000ddbf18788024976dcd0570ccc18f) |
| 3 | AF 3: Introducción a Aprendizaje Máquina | Aplicación de clustering (K-Means) | [03_AF3_Clustering](03_AF3_Clustering) | [Abrir](https://geode-cloud-e9e.notion.site/AF-3-Introducci-n-a-Aprendizaje-M-quina-4000ddbf18788057b01bee5c88e90660) |
| 4 | Proyecto final: Introducción al Aprendizaje Máquina | Clasificación de gestos con CNN | [04_Proyecto_Final_CNN](04_Proyecto_Final_CNN) | [Abrir](https://geode-cloud-e9e.notion.site/Proyecto-final-Introducci-n-al-Aprendizaje-M-quina-40e0ddbf187880578e9dc6a7ebb11507) |
