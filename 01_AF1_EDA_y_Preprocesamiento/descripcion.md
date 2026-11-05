> Link a Notion: <https://geode-cloud-e9e.notion.site/AF-1-Introducci-n-al-Aprendizaje-M-quina-3de0ddbf1878805b956ed15e1361153f>

# AF 1: Introducción al Aprendizaje Máquina

## Análisis Exploratorio y Preprocesamiento de Datos (EDA)

**Objetivo de la Actividad:**  
Desarrollar habilidades prácticas en la carga, inspección, visualización y limpieza de un conjunto de datos real utilizando Python en un entorno de Google Colab.

**Conjunto de Datos a utilizar:**

[Stroke Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset?utm_source=gemini)

Este dataset contiene variables fisiológicas y de estilo de vida para predecir el riesgo de accidentes cerebrovasculares.

### Sección 1: Carga e Inspección Inicial con `pandas`

**Objetivo:** Familiarizarse con la estructura del dataset, identificar tipos de datos y detectar anomalías iniciales.

- **Instrucciones:**
    1. Carga el dataset en un DataFrame de `pandas` .
    2. Inspecciona las primeras y últimas 5 filas (`head()` y `tail()`).
    3. Revisa la información general del DataFrame (`info()`): número de registros, columnas y tipos de datos (`int64`, `float64`, `object`).
    4. Obtén un resumen estadístico de las variables numéricas (`describe()`).
    5. Detecta la presencia de valores nulos o faltantes en todo el dataset (`isnull().sum()`).

### Sección 2: Limpieza, Transformación y Tratamiento con `pandas` y `numpy`

**Objetivo:** Tomar decisiones de ingeniería de datos para limpiar el dataset, tratar nulos y codificar variables categóricas.

- **Instrucciones:**
    1. **Tratamiento de nulos:** Los valores nulos en el IMC (`bmi`) deben ser imputados. Utiliza `numpy` o `pandas` para rellenarlos con la mediana de la columna.
    2. **Detección de valores atípicos (Outliers):** Utiliza `numpy` para calcular los cuartiles y el Rango Intercuartílico (IQR) en variables continuas como el nivel de glucosa (`avg_glucose_level`) para identificar posibles valores extremos.
        1. **¿Cómo funciona el método del Rango Intercuartílico (IQR)?**  
            En lugar de usar la media, este método se basa en **percentiles**:  
            • **$Q1$ (Primer Cuartil):** El valor que deja por debajo al 25% de los datos (el percentil 25).  
            • **$Q3$ (Tercer Cuartil):** El valor que deja por debajo al 75% de los datos (el percentil 75).  
            • **$IQR$ (Rango Intercuartílico):** Es la distancia entre el tercer y el primer cuartil ($IQR = Q3 - Q1$). Mide qué tan dispersos están los datos en el 50% central de la distribución.  
            Para definir qué es un valor anormalmente alto o bajo, se establecen **límites**:  
            • **Límite inferior:** $Q1 - (1.5 \times IQR)$  
            • **Límite superior:** $Q3 + (1.5 \times IQR)$  
            Cualquier valor que esté por debajo del límite inferior o por encima del límite superior se considera un **valor atípico**.
    3. **Codificación de variables categóricas (Encoding):** Las columnas como `gender`, `ever_married`, `work_type`, `Residence_type` y `smoking_status` están en formato texto. Utiliza [`pd.get_dummies()`](https://pandas.pydata.org/docs/reference/api/pandas.get_dummies.html) (One-Hot Encoding) o `map()` para convertir estas variables categóricas en numéricas aptas para un modelo de Machine Learning.
    4. Elimina la columna `id`, ya que no aporta información predictiva.

### Sección 3: Análisis Visual y Exploratorio con `matplotlib`

**Objetivo:** Extraer conocimiento y patrones visuales del comportamiento de los datos en relación con la variable objetivo (`stroke`).

- **Instrucciones para el alumno:**
    1. **Distribución de la variable objetivo:** Utiliza `matplotlib` para crear un gráfico de barras o de pastel que muestre el desbalance de clases (`stroke` = 0 vs `stroke` = 1).
    2. **Histogramas de variables continuas:** Genera histogramas (con `plt.hist()`) para comparar la distribución de la `age` (edad) y el `avg_glucose_level` entre las personas que sufrieron un derrame y las que no.
    3. **Relación entre variables:** Crea un diagrama de dispersión (`plt.scatter()`) relacionando la edad con el nivel de glucosa, diferenciando por color a los pacientes con y sin riesgo de derrame.
    4. **Conclusión del EDA:** Escribe un párrafo breve de conclusiones donde respondas: _¿Qué factores de riesgo parecen ser los más determinantes a simple vista según las gráficas?_

### Entregables para Actividad Fundamental

- Documento en donde se describa lo que se realizó en esta actividad:
    - Portada con los datos de las personas que realizaron actividad (Nombre completo, matrícula, hora y día de clase)
    - Introducción
    - Desarrollo (incluir link del repositorio de Github en donde se aloja notebook con la solución a estos ejercicios)
    - Conclusión
    - Referencias consultadas
- Trabajo en equipo
- Todos los integrantes deberán de entregar la actividad
