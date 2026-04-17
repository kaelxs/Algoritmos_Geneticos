# Algoritmos Genéticos Aplicados al Aprendizaje de Máquina

## Actividad 02 – Resumen Ejecutivo

Fecha de presentación: 16 de abril de 2026
Repositorio: [https://github.com/kaelxs/Algoritmos_Geneticos](https://github.com/kaelxs/Algoritmos_Geneticos)

---

## Colaboradores

* MAMANI MENDOZA JOSEPH ELVIS
* TAPARA CCAHUANA PAUL RENMIS
* TICONA ERQUINIGO JHOEL YOVANI

---

## 1. Descripción General

El presente proyecto implementa Algoritmos Genéticos aplicados a problemas de aprendizaje automático utilizando el lenguaje de programación Python y el entorno Google Colab.

Cada implementación sigue el ciclo completo del algoritmo genético, el cual incluye:

* Representación cromosómica
* Inicialización de la población
* Definición de la función de aptitud (fitness)
* Proceso de selección
* Operadores de cruzamiento
* Operadores de mutación
* Criterio de terminación

Se emplean conjuntos de datos reales provenientes de las bibliotecas scikit-learn y Kaggle, aplicados en tres escenarios distintos de optimización.

---

## 2. Resumen de los Experimentos

| Nº | Técnica                         | Dataset                   | Modelo              | Accuracy | Resultado Principal                             |
| -- | ------------------------------- | ------------------------- | ------------------- | -------- | ----------------------------------------------- |
| 1  | Selección de Características    | Car Evaluation (Kaggle)   | Regresión Logística | ~92%     | Selección de 2 de 6 variables: persons y safety |
| 2  | Optimización de Hiperparámetros | Wine (scikit-learn)       | Random Forest       | 97.78%   | Mejora de +0.57% respecto al modelo base        |
| 3  | Neuroevolución                  | Digits 0-9 (scikit-learn) | Red Neuronal MLP    | 95.05%   | Arquitectura óptima (256,), relu, lr=0.05, sgd  |

---

## 3. Implementación del Algoritmo Genético

### 3.1 Selección de Características

* Representación: vector binario (0/1)
* Cada gen representa la inclusión o exclusión de una característica
* Función de aptitud: precisión mediante validación cruzada menos penalización por número de variables
* Método de selección: aleatorio
* Cruzamiento: de un punto
* Mutación: cambio de bits

---

### 3.2 Optimización de Hiperparámetros

* Representación: vector de índices de hiperparámetros
* Función de aptitud: precisión media con validación cruzada utilizando Random Forest
* Método de selección: ruleta proporcional
* Cruzamiento: uniforme
* Mutación: reemplazo aleatorio dentro del rango permitido

---

### 3.3 Neuroevolución

* Representación: vector de 7 genes que define la arquitectura de la red neuronal
* Función de aptitud: precisión mediante validación cruzada con MLPClassifier
* Método de selección: torneo (k=3)
* Cruzamiento: de dos puntos
* Mutación: reemplazo aleatorio de genes

---

## 4. Detalles Técnicos

### 4.1 Selección de Características

* Codificación de variables categóricas mediante LabelEncoder
* Inclusión de penalización para evitar sobreajuste
* Reducción de dimensionalidad sin pérdida significativa de precisión

### 4.2 Optimización de Hiperparámetros

* Exploración del espacio de búsqueda de Random Forest
* Mejora del rendimiento mediante exploración genética
* Incremento de precisión respecto a configuración por defecto

### 4.3 Neuroevolución

* Evolución de arquitecturas de redes neuronales artificiales
* Uso de elitismo para preservar mejores soluciones
* Mejora progresiva del rendimiento del modelo

---

## 5. Estructura del Repositorio

Algoritmos_Geneticos/

* tarea_02_machine_learning.ipynb
* README.md

---

## 6. Ejecución

Los scripts pueden ejecutarse en Google Colab o en un entorno local con Python.

Dependencias requeridas:

* numpy
* scikit-learn

Ejecución:
tarea_02_machine_learning.ipynb

---

## 7. Conclusión

El presente trabajo demuestra la aplicación de Algoritmos Genéticos en problemas de aprendizaje automático, específicamente en:

* Selección de variables relevantes
* Optimización de hiperparámetros
* Diseño de arquitecturas de redes neuronales

Los resultados evidencian mejoras en el rendimiento de los modelos mediante técnicas evolutivas de optimización.

---

Actividad 02 – Algoritmos Genéticos en Machine Learning
Fecha de presentación: 16/04/2026
