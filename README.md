# TP.-Hospitalizados. ML
Abstrat: El proyecto clasificó pacientes como hospitalizados tras una biopsia prostática. Variables clave como DIAS HOSPITALIZACION MQ, PSA y FIEBRE destacaron en el modelo de Árbol de Decisión, logrando 100% de precisión y 75% de sensibilidad, optimizando la identificación de casos críticos y priorización clínica.

# Reflexión General del Trabajo

En el proyecto solicitado, se abordaron diversos pasos del ciclo de un análisis de datos con un enfoque en modelamiento predictivo, teniendo como objetivo principal clasificar a los pacientes como hospitalizados o no hospitalizados tras una biopsia prostática. A continuación, se detallan los puntos clave en relación con los objetivos planteados:

1. Identificación de características relevantes
Objetivo: Determinar las características más importantes asociadas con la hospitalización de pacientes.

Logros:

Se identificaron variables clave, como:
DIAS HOSPITALIZACION MQ: Mostró ser la característica más importante en el modelo.
PSA y EDAD: También contribuyen significativamente, aunque en menor medida.
FIEBRE e ITU: Indicadores clínicos directos que ayudan a prever hospitalizaciones.
Las demás variables, aunque menos influyentes, aportan contexto valioso al análisis.
Conclusión: El análisis mostró que los indicadores relacionados con la duración de la hospitalización y la aparición de complicaciones infecciosas tienen mayor impacto en la predicción.

2. Clasificación de pacientes (Hospitalizado/No Hospitalizado)
Objetivo: Entrenar un modelo capaz de predecir la hospitalización.

Logros:

Se probaron y compararon varios modelos:
Árbol de Decisión: Se optimizó el hiperparámetro max_depth para maximizar rendimiento. Este modelo destacó por su alto recall (75%), útil para identificar pacientes hospitalizados.
K-Vecinos (KNN): Con un valor óptimo de k=2, mostró buena exactitud (97.27%) pero bajo recall (25%), lo que lo hace menos adecuado para identificar casos críticos.
El desempeño fue evaluado usando métricas clave como Exactitud, Sensibilidad (Recall) y Precisión, asegurando una comprensión clara del impacto de cada modelo.
Conclusión: El Árbol de Decisión optimizado fue el modelo más adecuado, equilibrando exactitud, sensibilidad y precisión, y mostrando la capacidad de identificar pacientes hospitalizados con mayor fiabilidad.

3. Estrategias para mejorar el desempeño
Logros:

Se aplicaron técnicas de manejo de datos, como:
Normalización de variables numéricas: Para asegurar consistencia en los modelos basados en distancia.
Balanceo de clases (propuesto con SMOTE): Para abordar el desbalance entre pacientes hospitalizados y no hospitalizados.
Se plantearon y comenzaron estrategias como el uso de modelos de ensamble (Random Forest), que combinan simplicidad y robustez para mejorar el rendimiento global.
Conclusión: Estas estrategias apuntan a garantizar que el modelo sea más robusto y confiable para aplicaciones en entornos clínicos.

4. Reflexión Final
Este análisis permitió no solo clasificar pacientes según su probabilidad de hospitalización, sino también comprender mejor las características clave asociadas al desenlace. Esto es crucial en un contexto clínico, donde predecir correctamente puede ayudar a priorizar recursos médicos y tomar decisiones informadas.

Recomendaciones:
Uso clínico:
Implementar el modelo con mayor recall para minimizar falsos negativos (pacientes hospitalizados no detectados).
Análisis continuo:
Revisar periódicamente el modelo con nuevos datos para garantizar su relevancia y precisión.
Acciones adicionales:
Explorar modelos avanzados como Gradient Boosting o redes neuronales si el dataset crece y se requiere mayor capacidad predictiva.
Este proyecto no solo cumple con los objetivos iniciales, sino que también sienta las bases para futuras mejoras en la gestión predictiva de pacientes hospitalizados.
