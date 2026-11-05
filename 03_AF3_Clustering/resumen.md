# Resumen – AF 3: Clustering

**Qué hay que hacer:** con el dataset limpio de la AF 1 y **sin** la columna `stroke`, agrupar pacientes con K-Means en un notebook.

1. **Preparar:**
   - Quitar `stroke` (guardarla aparte) e `id`.
   - Elegir variables numéricas (`age`, `avg_glucose_level`, `bmi`).
   - Escalar con `StandardScaler`.
   - Investigar por qué K-Means falla si no se escalan los datos.
2. **Elegir k:**
   - Método del codo (k de 1 a 10, con inercia).
   - Coeficiente de silueta para cada k.
   - Escoger el k óptimo con base en ambas gráficas.
3. **Entrenar K-Means** con ese k:
   - Obtener los centroides.
   - Hacer un scatter (ej. edad vs. glucosa) coloreado por clúster, con los centroides marcados con una "X".
4. **Validar:**
   - Volver a unir `stroke` al DataFrame con los clústeres.
   - Hacer `pd.crosstab` entre clúster y `stroke`.
   - Responder qué clúster concentra más derrames y si el algoritmo aisló un grupo de alto riesgo.

**Entrega (en equipo, todos entregan):** documento con portada, introducción, desarrollo (con link al repo de GitHub con el notebook), conclusión y referencias.
