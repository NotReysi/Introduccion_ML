# Resumen – AF 2: Aprendizaje Supervisado

**Qué hay que hacer:** con el dataset limpio de la AF 1, entrenar una red neuronal (Keras/TensorFlow) que prediga `stroke`, en un notebook.

1. **Preparar los datos:**
   - Separar `X` y `y` (`stroke`).
   - Hacer `train_test_split` 80/20 con `stratify=y`.
   - Escalar con `StandardScaler`.
   - Investigar por qué las redes neuronales necesitan escalado y los árboles no.
2. **Diseñar el modelo:** `keras.Sequential` con al menos 2 capas ocultas y una capa de salida. Responder:
   - Qué activación usaste en las capas ocultas y por qué.
   - Qué activación va en la salida (sigmoide) y cuál es su rango.
   - Por qué `binary_crossentropy` y no MSE.
3. **Entrenar:**
   - Compilar con un optimizador (`Adam` o `SGD`).
   - Usar una métrica para clases desbalanceadas (`AUC` o `Recall`).
   - Hacer `model.fit` con `validation_split` y, opcionalmente, `EarlyStopping`.
   - Investigar qué hace `EarlyStopping` y en qué se diferencian `SGD` y `Adam`.

**Entrega (en equipo, todos entregan):** documento con portada, introducción, desarrollo (con link al repo de GitHub con el notebook), conclusión y referencias.
