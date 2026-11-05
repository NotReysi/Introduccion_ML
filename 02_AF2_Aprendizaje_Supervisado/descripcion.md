> Link a Notion: <https://geode-cloud-e9e.notion.site/AF-2-Introducci-n-al-Aprendizaje-M-quina-4000ddbf18788024976dcd0570ccc18f>

# AF 2: Introducción al Aprendizaje Máquina

## Modelos de Aprendizaje Supervisado

Utilizando el dataset limpio de la actividad fundamental 1, desarrollar la siguiente actividad en una notebook de Python.

#### Sección 1: División de datos y Escalado (Preparación para Deep Learning)

- **Instrucciones:**
    1. Separa el dataset en variables predictoras ($X$) y la variable objetivo ($y$ = `stroke`).
    2. Divide los datos en conjuntos de entrenamiento y prueba (`train_test_split`) usando un 80/20 y asegurándote de estratificar (`stratify=y`) debido al desbalance de clases.
        1. El parámetro `stratify=y` le indica a la función `train_test_split` que divida los datos asegurando que **la proporción de las clases se mantenga idéntica** tanto en el conjunto de entrenamiento (`train`) como en el de prueba (`test`), replicando exactamente la distribución del dataset original.
    3. **Investigación:** ¿Por qué es estrictamente necesario aplicar un escalador (como `StandardScaler`) o normalizar las variables continuas antes de ingresarlas a una red neuronal, a diferencia de otros algoritmos como los árboles de decisión?

#### Sección 2: Diseño de la Arquitectura y Selección de Funciones (Keras / TensorFlow)

- **Instrucciones:**
    1. Construye un modelo secuencial (`keras.Sequential`) con al menos dos capas ocultas.
    2. Define la capa de salida.
    3. **Investigación y diseño:**
        - ¿Qué **función de activación** elegiste para las capas ocultas (ej. `ReLU`, `Tanh`) y por qué?
        - ¿Qué **función de activación** debes usar obligatoriamente en la capa de salida para un problema de clasificación binaria (`stroke` = 0 o 1), y cuál es su rango de salida?
        - Si el dataset está fuertemente desbalanceado, ¿por qué la **función de pérdida** (`loss`) debe ser `binary_crossentropy` en lugar de Error Cuadrático Medio (MSE)?

#### Sección 3: Entrenamiento, Métricas y Optimizadores

- **Instrucciones:**
    
    1. Compila el modelo seleccionando un **optimizador** (ej. `Adam`, `SGD`) y una métrica adecuada para clases desbalanceadas (por ejemplo, `AUC` o `Recall`, en lugar de solo `Accuracy`, ya que un modelo tramposo que prediga "nadie tendrá derrame" tendría 95% de _accuracy_ pero 0% de utilidad médica).
    2. Entrena el modelo (`model.fit`) usando un conjunto de validación (`validation_split`) y callbacks opcionales como `EarlyStopping`.
    3. **Investigación:**
        - ¿Qué es lo que hace la función `EarlyStopping`?
        - ¿Cuál es la diferencia fundamental entre el optimizador `SGD` (Descenso de Gradiente Estocástico) y `Adam`? ¿Por qué `Adam` suele converger más rápido en las primeras épocas?
    
    ### Entregables para Actividad Fundamental
    
    - Documento en donde se describa lo que se realizó en esta actividad:
        - Portada con los datos de las personas que realizaron actividad (Nombre completo, matrícula, hora y día de clase)
        - Introducción
        - Desarrollo (incluir link del repositorio de Github en donde se aloja notebook con la solución a estos ejercicios)
        - Conclusión
        - Referencias consultadas
    - Trabajo en equipo
    - Todos los integrantes deberán de entregar la actividad
