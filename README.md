"""# Predicción de Resultados de Partidos de la NBA – README  

Este repositorio contiene el cuaderno Jupyter **`TFG.ipynb`**, en el que se desarrolla íntegramente el pipeline para predecir si el equipo local ganará un partido de la NBA (temporada 2023–2024) mediante modelos de clasificación supervisada.

---

## 📄 Descripción

A partir de estadísticas de partidos (puntos, porcentajes de tiro, rebotes, asistencias…), cuotas de apuestas y rachas de victorias, se construyen y comparan tres modelos de Machine Learning:

1. **Regresión logística**  
2. **Random Forest**  
3. **XGBoost**  

Se optimizan sus hiperparámetros con **GridSearchCV**, se evalúan con métricas estándar (accuracy, precision, recall, F1-score, AUC) y se visualizan importancias de variables, matrices de confusión y curvas ROC.

---

## 📂 Estructura del proyecto

```text
/
├── TFG.ipynb                  # Notebook principal con todo el código
├── data/
│   └── Ingenieriadeldato_nba_2023-2024.csv  # Dataset consolidado
├── outputs/                   # Carpeta de gráficos y tablas
├── requirements.txt           # Dependencias Python
└── README.md                  # Esta documentación
