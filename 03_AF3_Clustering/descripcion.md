> Link a Notion: <https://geode-cloud-e9e.notion.site/AF-3-Introducci-n-a-Aprendizaje-M-quina-4000ddbf18788057b01bee5c88e90660>

# AF 3: Introducción a Aprendizaje Máquina

## Aplicación de Clustering

Utilizando el dataset limpio de la actividad fundamental 1, pero **omitiendo la columna objetivo (`stroke`),** desarrollar la siguiente actividad en una notebook de Python.

#### Sección 1: Preparación y Escalado de Características para Distancias

- **Objetivo:** Comprender por qué los algoritmos de clustering basados en distancias (como K-Means) exigen un preprocesamiento estricto.
- **Instrucciones:**
    1. Carga el dataset limpio y **elimina** la columna objetivo (`stroke`) y la columna `id`. El algoritmo no debe saber quién sufrió un derrame.
    2. Selecciona las variables numéricas y continuas clave (ej. `age`, `avg_glucose_level`, `bmi`).
    3. Aplica un `StandardScaler` para normalizar los datos.
    4. **Investigación:** ¿Por qué si una variable está en años (0 a 100) y otra en miligramos por decilitro (50 a 300) el algoritmo de K-Means fallaría catastróficamente si no se escalan los datos?

#### Sección 2: Búsqueda del Número Óptimo de Clústeres (Método del Codo y Silueta)

- **Objetivo:** Determinar cuántos perfiles de pacientes existen de forma matemática en lugar de adivinarlo.
- **Instrucciones:**
    1. Utiliza el **Método del Codo (Elbow Method)** iterando K-Means para un $k$ desde 1 hasta 10, calculando la inercia (_inertia_ / suma de errores cuadráticos intra-clúster). Grafica los resultados con `matplotlib`.
    2. Calcula también el **Coeficiente de Silueta (Silhouette Score)** para cada valor de $k$ para evaluar qué tan bien definidos y separados están los clústeres.
    3. Con base en ambas gráficas, selecciona el valor óptimo de $k$ (por ejemplo, $k=3$ o $k=4$ perfiles de riesgo).

#### Sección 3: Entrenamiento del Modelo y Visualización de Centroides

- **Objetivo:** Agrupar a los pacientes e interpretar el significado físico de cada clúster.
- **Instrucciones:**
    1. Entrena el modelo final de `KMeans` utilizando el número óptimo de clústeres seleccionado.
    2. Obtener las coordenadas de los **centroides** (_cluster centers_).
    3. Crea un gráfico de dispersión (`scatter plot`) utilizando `matplotlib` relacionando dos variables clave (por ejemplo, Edad vs. Glucosa), pintando a cada punto según el clúster asignado y marcando con una "X" la posición de los centroides.

#### Sección 4: Validación Cruzada (El toque maestro del Aprendizaje No Supervisado)

- **Objetivo:** Evaluar si un algoritmo ciego (_sin etiquetas_) logró agrupar de manera natural a las personas con mayor propensión a enfermar.
- **Instrucciones para el alumno:**
    1. Vuelve a unir la columna `stroke` (que habías guardado al inicio) al DataFrame con las etiquetas de los clústeres asignadas por el modelo.
    2. Crea una tabla cruzada o gráfico de proporciones (`pd.crosstab`) entre los clústeres descubiertos y la variable real `stroke`.
    3. **Pregunta final de análisis:** _¿Cuál de los clústeres formados concentra el mayor porcentaje de casos reales de derrame cerebral? ¿El algoritmo de clustering fue capaz de aislar un grupo de alto riesgo médico sin haber visto nunca la etiqueta "stroke" durante su entrenamiento?_

### Entregables para Actividad Fundamental

- Documento en donde se describa lo que se realizó en esta actividad:
    - Portada con los datos de las personas que realizaron actividad (Nombre completo, matrícula, hora y día de clase)
    - Introducción
    - Desarrollo (incluir link del repositorio de Github en donde se aloja notebook con la solución a estos ejercicios)
    - Conclusión
    - Referencias consultadas
- Trabajo en equipo
- Todos los integrantes deberán de entregar la actividad
