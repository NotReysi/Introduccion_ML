> Link a Notion: <https://geode-cloud-e9e.notion.site/Proyecto-final-Introducci-n-al-Aprendizaje-M-quina-40e0ddbf187880578e9dc6a7ebb11507>

# Proyecto final: Introducción al Aprendizaje Máquina

## Proyecto Final: Clasificación de Gestos (Piedra, Papel o Tijera) mediante Redes Neuronales Convolucionales (CNN)

### Sección 1: Descarga, Carga y Preprocesamiento del Dataset

- **Objetivo:** Cargar y preparar el dataset público [**Rock, Paper, Scissors en Kaggle**](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors), aplicando un preprocesamiento básico indispensable para el modelo.
    1. **Instrucciones:** Descarga el dataset [**Rock, Paper, Scissors**](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors) de Kaggle (que contiene imágenes de manos humanas realizando los gestos de piedra, papel o tijera bajo diferentes condiciones) y cárgalo en tu entorno de trabajo en una Jupyter Notebook o Google Colab.
    2. Divide el dataset en tres conjuntos independientes: entrenamiento (_train_), validación (_validation_) y prueba (_test_).
    3. Aplica un preprocesamiento estándar: redimensiona todas las imágenes a una resolución uniforme y normaliza los valores de los píxeles dividiendo entre 255 para llevarlos a la escala [0, 1].
    4. **Pregunta:** ¿Por qué es necesario normalizar los valores de los píxeles de las imágenes en un rango numérico pequeño antes de alimentar las capas de una Red Neuronal Convolucional?

### Sección 2: Diseño y Construcción de la Arquitectura CNN desde Cero

- **Objetivo:** Definir la estructura de la Red Neuronal Convolucional construyéndola desde cero, configurando capas convolucionales, de agrupación (_pooling_) y totalmente conectadas.
    1. **Instrucciones:** Diseña y programa una CNN desde cero utilizando librerías de aprendizaje profundo (ej. TensorFlow/Keras). No utilices arquitecturas preentrenadas.
    2. Integra de manera secuencial capas convolucionales (`Conv2D`) seguidas de capas de reducción espacial (`MaxPooling2D`), aplanamiento (`Flatten`) y capas densas (`Dense`) intermedias y de salida.
    3. Compila el modelo seleccionando un optimizador adecuado (ej. Adam o SGD), una función de pérdida acorde a la clasificación multiclase (`categorical_crossentropy`) y la métrica de desempeño de precisión (_Accuracy_).

### Sección 3: Entrenamiento, Monitoreo y Visualización de Curvas de Aprendizaje

- **Objetivo:** Ejecutar el entrenamiento del modelo supervisando su evolución mediante épocas y evaluar su capacidad de generalización sobre el conjunto de prueba.
    1. **Instrucciones:** Entrena el modelo configurando un tamaño de lote (_batch size_) y un número fijo de épocas determinado.
    2. Genera gráficos utilizando `matplotlib` que muestren la evolución de la función de pérdida (_Loss_) y la precisión (_Accuracy_) a lo largo de las épocas tanto para el conjunto de entrenamiento como para el de validación.
    3. Evalúa el modelo entrenado sobre el conjunto de prueba (_Test set_) para obtener la precisión y la pérdida final.

### Sección 4: Análisis Avanzado, Matriz de Confusión y Discusión Crítica

- **Objetivo:** Interpretar el rendimiento de la Red Neuronal Convolucional mediante métricas detalladas e inspección visual de aciertos y errores entre los gestos.
    1. **Instrucciones:** Genera la **Matriz de Confusión** y calcula el reporte de clasificación detallado (_Precision_, _Recall_, _F1-score_ por cada clase: piedra, papel y tijera).
    2. Selecciona un conjunto de ejemplos visuales donde el modelo haya acertado y otros donde haya fallado, graficándolos para su análisis visual.
    3. **Pregunta final de análisis:** ¿Entre qué gestos específicos el modelo presentó mayores confusiones o tasas de error, y a qué similitudes visuales o variaciones en la posición de la mano atribuyes este comportamiento?

### Entregables para el Proyecto Final

- **Documento en formato PDF que incluya:**
    - **Portada:** Datos institucionales, nombre de la Unidad de Aprendizaje (_Introducción a la Inteligencia Artificial_), título del proyecto, nombres y matrículas de los integrantes, hora y día de clase.
    - **Introducción:** Planteamiento del problema y justificación del uso de visión por computadora en el reconocimiento de gestos.
    - **Antecedentes:** Revisión teórica sobre Redes Neuronales Convolucionales.
    - **Metodología:** Descripción del dataset ([Rock, Paper, Scissors](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors)), preprocesamiento, arquitectura de la red diseñada desde cero, hiperparámetros, enlace directo al repositorio de GitHub donde se aloja la Jupyter Notebook o Google Colab ejecutable con la solución completa.
    - **Resultados:** Gráficas de entrenamiento, matriz de confusión y métricas de evaluación.
    - **Discusión y Conclusión:** Análisis crítico de los hallazgos y limitaciones del modelo.
    - **Referencias bibliográficas:** Citadas en formato APA o IEEE.
- **Trabajo en equipo:** Todos los integrantes del equipo deberán realizar su entrega respectiva en la actividad asignada en Teams.
