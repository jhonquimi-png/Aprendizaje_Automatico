# Semana 4 – Gobernanza, Explicabilidad y Mitigación de Sesgos en Machine Learning

## Descripción

Este proyecto corresponde a la actividad de la Semana 4 de la materia Aprendizaje Automático de la Maestría en Inteligencia Artificial – UEES.

El objetivo del trabajo fue desarrollar un modelo supervisado orientado a la predicción de aprobación estudiantil e incorporar técnicas de explicabilidad (XAI) y evaluación de equidad para analizar transparencia, posibles sesgos y comportamiento del modelo.

---

## Dataset utilizado

Archivo:
`student_performance.csv`

Características:
- 500 registros
- Variables académicas, demográficas y de comportamiento estudiantil
- Variables numéricas y categóricas
- Variable objetivo: `passed`

---

## Técnicas aplicadas

### Preprocesamiento y Modelado
- Codificación de variables categóricas
- Escalado de datos con StandardScaler
- División Train/Test
- Modelo Random Forest Classifier

### Explicabilidad (XAI)
- SHAP:
  - Importancia global de variables
  - Explicaciones individuales
- LIME:
  - Explicabilidad local de predicciones

### Equidad y Gobernanza
- Fairlearn
- Paridad Demográfica
- Igualdad de Oportunidades
- Evaluación de métricas por género

---

## Resultados principales

- Las variables con mayor influencia fueron:
  - `study_hours_per_week`
  - `previous_score`
  - `attendance_rate`

- El modelo no presentó un sesgo severo en la asignación de aprobados, aunque se identificaron pequeñas diferencias entre grupos.

- Las técnicas XAI permitieron comprender tanto el comportamiento global del modelo como decisiones individuales específicas.

---

## Estructura del repositorio

```text
data/           -> Dataset utilizado
notebooks/      -> Notebook principal del proyecto
presentacion/   -> Diapositivas de la exposición
imagenes/       -> Imagenes extraida de los notebooks
video/          -> Video de la explicación del trabajo
