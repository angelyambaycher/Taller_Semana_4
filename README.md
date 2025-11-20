# 📘 Explicabilidad y Análisis Ético en Modelos Predictivos (XAI)

Este proyecto aplica técnicas de *Explainable Artificial Intelligence (XAI)* para analizar la transparencia, sesgos y comportamiento de modelos supervisados entrenados sobre un conjunto de datos real de mantenimiento predictivo.
Incluye evaluación de calidad de datos, explicación de modelos, detección de sesgos y recomendaciones éticas.

---

## 📌 1. Objetivo del Proyecto

- Implementar un modelo de ML considerando calidad de datos y mitigación de sesgos.
- Aplicar técnicas de explicabilidad: **SHAP**, **Permutation Importance**, **Árboles de decisión**, etc.
- Analizar transparencia del modelo y cómo toma decisiones.
- Detectar riesgos éticos y sociales.
- Documentar correctamente el proceso completo.

---

## 📂 2. Estructura del Repositorio

📁 data/ → Dataset original
📁 src/ → Código fuente (preprocesamiento, entrenamiento, XAI)
📁 notebooks/ → Notebooks de análisis
📁 figures/ → Gráficos exportados
📁 results/ → Métricas, explicaciones y conclusiones
README.md → Documento principal


---

## 📊 3. Análisis Exploratorio del Dataset

Se analizaron variables como:

- Edad
- Ingresos
- Nivel educativo
- Zona geográfica
- Historial crediticio
- Estado civil
- Sexo
- Ocupación
- Resultado de crédito anterior

Incluyendo:

- Distribuciones
- Boxplots
- Correlaciones
- Identificación de desbalances

Las figuras se encuentran en:
📁 `figures/heatmap_correlations.png`
📁 `figures/kmeans_pca.png`
📁 `figures/dbscan_pca.png`

---

## 🤖 4. Entrenamiento del Modelo Supervisado

Se entrenaron los siguientes modelos:

- **Random Forest (modelo principal)**
- Regresión Logística
- Árbol de Decisión
- SVM (opcional)

Con técnicas de:

- Balanceo (`class_weight='balanced'`)
- Normalización / escalamiento
- Codificación de variables categóricas

Resultados principales almacenados en:

📁 `results/metrics.txt`
📁 `results/feature_importance.png`

---

## 🧠 5. Explicabilidad del Modelo (XAI)

Se aplicaron las siguientes técnicas:

### ✔ SHAP Values
- Summary Plot
- Force Plot por instancia
- Ranking de variables

📁 `figures/shap_summary.png`
📁 `figures/shap_force_example.png`

### ✔ Permutation Feature Importance
📁 `figures/permutation_importance.png`

### ✔ Visualización del Árbol de Decisión
📁 `figures/decision_tree.png`

Cada técnica muestra qué variables influyen más en la clasificación y cómo afectan la predicción.

---

## ⚠️ 6. Identificación de Sesgos Algorítmicos

Se evaluaron sesgos por:

- Género
- Zona geográfica
- Edad
- Ingresos

Se detectaron diferencias significativas en:

- Tasas de aprobación para mujeres jóvenes
- Variación por zona geográfica
- Efecto del historial crediticio

Los análisis se encuentran en:

📁 `results/bias_analysis.txt`
📁 `figures/bias_gender.png`
📁 `figures/bias_zone.png`

---

## 🛡️ 7. Propuestas de Mitigación

- Recolección de datos más representativos.
- Eliminación/codificación ética de variables sensibles.
- Reentrenamiento con técnicas de fairness.
- Ajuste de umbrales por grupo.
- Monitoreo continuo del sistema.

---

## 📌 8. Conclusiones

- El modelo presenta **sesgo detectado en género y zona**, que debe mitigarse antes de su uso real.
- Las técnicas XAI permitieron identificar **qué variables dominan la decisión**, destacando historial crediticio, temperatura del proceso y torque.
- La integración de XAI mejora la transparencia del sistema y permite una auditoría ética responsable.
- Se recomienda implementar estrategias de fairness y validar periódicamente su comportamiento.

---

## 👨‍💻 Autor
Angel Yambay M
