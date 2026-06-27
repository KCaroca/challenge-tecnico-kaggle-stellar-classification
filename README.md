# Challenge Técnico Core — Predicción de la clase estelar

Proyecto de Machine Learning desarrollado para la competencia Kaggle **Predicting Stellar Class** (Playground Series S6E6).

## Objetivo

Construir y comparar modelos de clasificación multiclase para predecir si una observación astronómica corresponde a una:

- GALAXY
- QSO
- STAR

## Dataset

Los datos fueron obtenidos desde la competencia de Kaggle. El conjunto incluye variables fotométricas (`u`, `g`, `r`, `i`, `z`), redshift y atributos categóricos asociados a la observación astronómica.

## Metodología

El proyecto considera:

1. Exploración inicial y revisión de estructura de los datos.
2. Identificación de valores faltantes, registros duplicados y valores atípicos.
3. Análisis exploratorio mediante estadísticas descriptivas, histogramas, gráficos de barras, boxplots, matriz de correlación y gráficos de dispersión.
4. Preprocesamiento con escalamiento de variables numéricas y One-Hot Encoding para variables categóricas.
5. División estratificada en entrenamiento y prueba.
6. Benchmark con cinco modelos:
   - Regresión Logística
   - SVM Lineal
   - Árbol de Decisión
   - XGBoost
   - LightGBM
7. Validación cruzada estratificada y optimización de hiperparámetros.
8. Generación de predicciones y envío a Kaggle.

## Resultados

El modelo seleccionado fue **LightGBM base**, debido a su desempeño final sobre el conjunto de prueba reservado:

| Métrica | Resultado |
|---|---:|
| Balanced Accuracy | 0.9510 |
| F1 Macro | 0.9518 |
| Accuracy | 0.9644 |

El envío realizado en Kaggle obtuvo un puntaje público de:

**0.95198 — Balanced Accuracy**

## Archivos

- `challenge_tecnico_kaggle_stellar_classification.ipynb`: notebook con el flujo completo de análisis, preprocesamiento, benchmark, optimización y generación de submission.
- `submission_lightgbm_final.zip`: archivo utilizado para el envío exitoso a Kaggle.

## Tecnologías utilizadas

Python, Pandas, NumPy, Matplotlib, Scikit-learn, XGBoost y LightGBM.
