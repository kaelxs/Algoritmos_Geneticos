# 🧬 Algoritmos Genéticos Aplicados al Aprendizaje de Máquina

## 📌 Actividad 02 – Resumen Ejecutivo

📅 **Fecha de presentación:** 16 de abril de 2026
🔗 **Repositorio:** [https://github.com/kaelxs/Algoritmos_Geneticos](https://github.com/kaelxs/Algoritmos_Geneticos)

---

## 📖 1. Descripción General

Este proyecto implementa **Algoritmos Genéticos (AG)** aplicados a problemas de **Machine Learning** utilizando Python y Google Colab.

Cada implementación sigue el ciclo completo del algoritmo genético:

* Representación cromosómica
* Inicialización de población
* Función de aptitud (fitness)
* Selección
* Cruzamiento
* Mutación
* Criterio de terminación

Se utilizan datasets reales de **scikit-learn y Kaggle** para tres aplicaciones principales.

---

## 📊 2. Resumen de los Experimentos

| # | Técnica                     | Dataset                 | Modelo              | Accuracy | Resultado Principal                             |
| - | --------------------------- | ----------------------- | ------------------- | -------- | ----------------------------------------------- |
| 1 | Feature Selection           | Car Evaluation (Kaggle) | Logistic Regression | ~92%     | Selecciona 2/6 features: *persons*, *safety*    |
| 2 | Hyperparameter Optimization | Wine (sklearn)          | Random Forest       | 97.78%   | Mejora +0.57% (n_estimators=50, max_depth=None) |
| 3 | Neuroevolution              | Digits 0-9 (sklearn)    | MLP Neural Network  | 95.05%   | (256,), relu, lr=0.05, sgd → +0.67%             |

---

## ⚙️ 3. Implementación del Algoritmo Genético

### 🧪 3.1 Feature Selection

* Cromosoma: vector binario (0/1)
* Gen: feature activa o inactiva
* Fitness: Accuracy CV-5 − penalización por número de features
* Selección: aleatoria
* Cruzamiento: un punto
* Mutación: bit-flip

---

### 🧪 3.2 Hyperparameter Optimization

* Cromosoma: índices de hiperparámetros
* Fitness: Accuracy CV-5 (Random Forest)
* Selección: ruleta
* Cruzamiento: uniforme
* Mutación: cambio aleatorio dentro del rango

---

### 🧪 3.3 Neuroevolution

* Cromosoma: 7 genes (arquitectura de red neuronal)
* Fitness: Accuracy CV-3 (MLPClassifier)
* Selección: torneo (k=3)
* Cruzamiento: dos puntos
* Mutación: reemplazo aleatorio

---

## 🧠 4. Detalles Técnicos

### 🔹 Feature Selection

* Dataset categórico codificado con LabelEncoder
* Penalización para evitar exceso de features
* Resultado: 2 features mantienen ~92% accuracy

### 🔹 Hyperparameter Optimization

* Espacio de búsqueda de Random Forest
* Cruzamiento uniforme mejora diversidad
* Mejora +0.57% respecto al baseline

### 🔹 Neuroevolution

* Evolución de arquitectura de red neuronal
* Elitismo top-2 para estabilidad
* Mejora de rendimiento sin sobreajuste

---

## 📁 5. Estructura del Repositorio

```
Algoritmos_Geneticos/
│
├── tarea_02_machine_learning.ipynb
```

---

## 🚀 6. Ejecución

Cada script puede ejecutarse en **Google Colab** o localmente con Python.

### Requisitos:

```
numpy
scikit-learn
```

### Ejecución:

```bash
python ag_feature_selection.py
python ag_hyperparameter_optimization.py
python ag_neuroevolution.py
```

---

## 🧾 7. Conclusión

Este proyecto demuestra cómo los **Algoritmos Genéticos** pueden optimizar:

* Selección de variables
* Hiperparámetros de modelos
* Arquitecturas de redes neuronales

Mejorando el rendimiento de modelos de Machine Learning de forma automática.

---

## 📌 Actividad 02 – Algoritmos Genéticos en Machine Learning

📅 Presentación: Jueves 16/04/2026
