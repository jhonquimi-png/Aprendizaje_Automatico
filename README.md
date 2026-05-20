# Semana 4 – Aprendizaje No Supervisado

## Descripción

Este proyecto corresponde a la actividad de la Semana 4 de la materia Aprendizaje Automático de la Maestría en Inteligencia Artificial – UEES.

El objetivo del trabajo fue aplicar técnicas de aprendizaje no supervisado para segmentar perfiles estudiantiles utilizando modelos de clustering y reducción de dimensionalidad, gobierno de datos, eliminación de sesgos y explicabilidad de los modelos.

---

## Dataset utilizado

Archivo:
`student_performance.csv`

Características:
- 500 registros
- Variables académicas y de comportamiento estudiantil
- Variables numéricas y categóricas
  

---

## Técnicas aplicadas

- Análisis exploratorio de datos (EDA)
- Tratamiento de valores nulos y escalado con StandardScaler
- Modelado Supervisado (Regresión Lineal, Ridge, Decision Tree, Random Forest)
- Modelado No Supervisado (K-Means, DBSCAN, PCA, t-SNE)
- **Auditoría de Equidad (Fairlearn): Paridad Demográfica e Igualdad de Oportunidades**
- **Explicabilidad del Modelo (XAI con SHAP): Impactos Globales y Locales**

---

## Estructura del repositorio

```text
data/           -> Dataset utilizado (student_performance.csv)
notebooks/      -> S2_Modelos_Supervisados.ipynb
                   S3_Modelos_aprendizaje_no_supervisado.ipynb
                   S4_Gobernanza_XAI_y_Mitigacion_Sesgos.ipynb  <- NUEVO
presentacion/   -> Documentación de soporte y diapositivas
