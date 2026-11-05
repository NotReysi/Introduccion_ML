# Resumen – Proyecto Final: Piedra, Papel o Tijera con CNN

**Qué hay que hacer:** clasificar imágenes de gestos de mano con una CNN construida desde cero (sin modelos preentrenados). Dataset: [Rock, Paper, Scissors](https://www.kaggle.com/datasets/drgfreeman/rockpaperscissors).

1. **Datos:**
   - Descargar y cargar el dataset.
   - Dividirlo en train, validation y test.
   - Redimensionar las imágenes y normalizarlas (÷255).
   - Responder por qué se normalizan los píxeles.
2. **Arquitectura:**
   - `Conv2D` + `MaxPooling2D`, luego `Flatten` y `Dense`.
   - Compilar con optimizador (Adam o SGD), `categorical_crossentropy` y `accuracy`.
3. **Entrenamiento:**
   - Definir `batch size` y número de épocas.
   - Graficar loss y accuracy (train vs. validation).
   - Evaluar en test.
4. **Análisis:**
   - Matriz de confusión y reporte de clasificación (precision, recall y F1 por clase).
   - Mostrar ejemplos acertados y fallados.
   - Explicar entre qué gestos hay más confusión y por qué.

**Entrega (en equipo, cada integrante entrega en Teams):** PDF con portada, introducción, antecedentes (teoría de CNN), metodología (con link al repo de GitHub con el notebook), resultados, discusión y conclusión, y referencias en APA o IEEE.
