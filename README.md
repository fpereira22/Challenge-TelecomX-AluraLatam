# 🔮 Telecom Churn Analysis & Prediction

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-ETL-150458?style=for-the-badge&logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-F7931E?style=for-the-badge&logo=scikit-learn)

## 📌 Descripción del Proyecto
Este proyecto aborda una problemática crítica en la industria de las telecomunicaciones: la **fuga de clientes (Churn)**. 

El objetivo principal fue desarrollar un flujo de trabajo completo de Data Science para identificar patrones de comportamiento y predecir qué usuarios tienen mayor probabilidad de cancelar el servicio.

El proyecto abarca desde la ingesta de datos crudos (JSON anidado) hasta la optimización de modelos de Inteligencia Artificial.

## ⚙️ Tecnologías y Herramientas
* **Lenguaje:** Python 3
* **ETL (Extracción, Transformación y Carga):**
    * `Pandas` (json_normalize, limpieza de datos, manejo de nulos).
    * `SQLite3` (Simulación de carga a Data Warehouse).
* **Análisis Exploratorio (EDA):**
    * `Matplotlib` y `Seaborn` para visualización de datos.
* **Machine Learning:**
    * `Scikit-Learn` (Random Forest, Gradient Boosting).
    * `GridSearchCV` (Optimización de hiperparámetros).

## 🚀 Pipeline del Proyecto

### 1. Extracción y Limpieza (ETL)
* **Desafío:** Los datos originales provenían de una API en formato JSON con estructuras anidadas (`customer.gender`, `account.Charges`).
* **Solución:** Se utilizó `pd.json_normalize` para aplanar la estructura.
* **Limpieza:** Se corrigieron tipos de datos erróneos en `TotalCharges` y se imputaron valores nulos en clientes nuevos.

### 2. Análisis Exploratorio (Insights)
Se descubrieron patrones clave del negocio:
* 📉 **Tasa de Fuga:** ~26.5% de la base de clientes.
* 💰 **Fuga de Valor:** Los clientes que se van pagan en promedio **$74/mes**, mientras que los fieles pagan **$61/mes**.
* ⚠️ **Factor de Riesgo:** Los contratos "Month-to-month" tienen la mayor correlación con la fuga.

### 3. Modelado Predictivo (Machine Learning)
Se entrenaron y compararon múltiples modelos para predecir el Churn:
* **Modelo Base:** Random Forest Classifier.
* **Modelo Avanzado:** Gradient Boosting con ajuste de hiperparámetros (Grid Search).
* **Resultados:** Se alcanzó una precisión (Accuracy) cercana al **80%**, superando la línea base del negocio.

## 📊 Visualización de Resultados
El proyecto incluye un dashboard final generado con código que muestra:
1.  Comparativa de rendimiento de modelos.
2.  **Curva ROC:** Para evaluar la sensibilidad del modelo.
3.  **Feature Importance:** Ranking de variables que más influyen en la decisión del cliente.

## 🛠️ Cómo ejecutar este proyecto
1.  Clonar el repositorio:
    ```bash
    git clone [https://github.com/TU_USUARIO/Telecom-Churn-Analysis.git](https://github.com/TU_USUARIO/Telecom-Churn-Analysis.git)
    ```
2.  Instalar dependencias:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  Ejecutar el Jupyter Notebook:
    ```bash
    jupyter notebook TelecomX_LATAM.ipynb
    ```

---
*Proyecto realizado como parte del Desafío de Data Science - [Fecha/Institución]*
