# Resumen – AF 1: EDA y Preprocesamiento

**Qué hay que hacer:** analizar y limpiar el dataset de [Stroke Prediction](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) en Google Colab con Python.

1. **Cargar e inspeccionar** con `pandas`: `head()`, `tail()`, `info()`, `describe()` y `isnull().sum()`.
2. **Limpiar:**
   - Rellenar los nulos de `bmi` con la mediana.
   - Buscar outliers con IQR (ej. en `avg_glucose_level`).
   - Convertir variables de texto a números (`get_dummies()` o `map()`).
   - Borrar la columna `id`.
3. **Graficar** con `matplotlib`:
   - Balance de `stroke` (barras o pastel).
   - Histogramas de `age` y `avg_glucose_level` según `stroke`.
   - Dispersión edad vs. glucosa, con color según `stroke`.
   - Un párrafo de conclusión sobre los factores de riesgo más claros.

**Entrega (en equipo, todos entregan):** documento con portada, introducción, desarrollo (con link al repo de GitHub con el notebook), conclusión y referencias.
