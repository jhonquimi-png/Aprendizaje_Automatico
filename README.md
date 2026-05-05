En este análisis se selección na base de estudiante y features que permiten comprender y prácticar modelos Supervisados: Clasificación y Regresión.

A continuación se detalla de manera general un resumen del dataset y los resultados comparativos de los modelos clasificación y regresión con la interpretabilidad de estos.
En el detalle del notebook de googlecolab adjunto se especifica paso a paso lo realizado.


Análisis exploratorio de datos (EDA)

Describir variables y clases.
Acerca del conjunto de datos Creé este conjunto de datos para practicar la clasificación y regresión mediante aprendizaje automático. Contiene 500 registros de estudiantes con sus hábitos de estudio, datos demográficos y resultados de exámenes.
Las columnas incluyen información como horas de estudio semanales, tasa de asistencia, nivel educativo de los padres, calificaciones anteriores y calificaciones finales. La variable objetivo puede utilizarse final_scorepara regresión o passedclasificación (aprobar = puntuación >= 50).

Descripción de variables y clases
student_id:Identificador único de estudiante (STU0001-STU0500)
gender: Género del estudiante (Masculino/Femenino)
age: Edad del estudiante en años
study_hours_per_week: Horas de estudio semanales autoinformadas
attendance_rate: Porcentaje de asistencia a clase (0-100)
parent_education: Nivel educativo más alto de los padres
internet_access: Si el estudiante tiene internet en casa (Sí/No)
extracurricular: ¿El estudiante participa en actividades extracurriculares? (Sí/No)
previous_score: Puntuación del trimestre anterior (0-100)
final_score: Puntuación del examen final (0-100)
passed: aprueba o no el estudiante

Intepretación de los 3 modelos clasificación
Para esta interpretación se seleccionó 3 modelo de clasificación: Regresión Logística, Árboles de Decisión y Support Vector Machine (SVM) para predicir si los estudiante pasaron o no.
De lo que se pudo observar de la revisión y el ejercicio:
Decision Tree (Profundidad 6): Al alcanzar el máximo en Accuracy, F1-Score y AUC-ROC, es el ganador absoluto pero puede estar demasiado ajustado a los datos de entrenamiento.
Logistic Regression: Presenta un desempeño excelente y equilibrado (0.96). Su AUC-ROC de 0.9960 indica una capacidad casi perfecta para distinguir entre clases, siendo un modelo muy robusto y confiable.
SVM (rbf, 20%): Es el modelo con menor rendimiento de los tres, aunque sigue siendo alto (0.91 de Accuracy). Su F1-Score de 0.93 muestra que todavía maneja bien el balance entre precisión y sensibilidad.
Con estos resultados tomaríamos el modelo de regresión logístico y como segunda opción el SVM que maneja bien el balance entre precisión y sensibilidad


Interpretación de la comparativa de los modelos de regresión
La Regresión Lineal es el mejor modelo en este caso. Aunque la diferencia con Ridge es mínima, la Regresión Lineal obtiene el mejor (R^{2}) (0.7516) y el menor RMSE (7.3432). Esto indica que es el modelo que mejor explica la variabilidad de los datos y el que comete errores de mayor magnitud con menos frecuencia

Interpretación de las Métricas
(R^{2}) (Coeficiente de Determinación): El valor de 0.7516 significa que el modelo de Regresión Lineal logra explicar aproximadamente el 75% de la varianza de tus datos. Es un rendimiento sólido para la mayoría de los contextos prácticos.
MAE (Error Medio Absoluto): La Regresión Lineal y Ridge están prácticamente empatados (~6.27). Esto significa que, en promedio, las predicciones del modelo fallan por unas 6.27 unidades respecto al valor real.
RMSE (Raíz del Error Cuadrático Medio): Es ligeramente superior al MAE (7.34). Como el RMSE penaliza más los errores grandes, su cercanía al MAE sugiere que el modelo no tiene "outliers" o errores catastróficos muy frecuentes.
Comparativa entre Modelos
Regresión Lineal vs. Ridge: El hecho de que Ridge (con alpha=10) tenga un desempeño casi idéntico (e incluso un MAE ligeramente mejor por milésimas) indica que la penalización de Ridge no está aportando una mejora significativa. El modelo no parece sufrir de multicolinealidad severa.
Decision Tree Regressor (d=8): Es el peor modelo de la lista. Tiene el (R^{2}) más bajo (0.65) y los errores más altos. Esto sugiere que una estructura de árbol de profundidad 8 no captura la relación de los datos tan bien como una línea recta (modelo lineal), o bien está perdiendo precisión en los rangos numéricos.
