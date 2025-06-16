# TFG
PREDICCIÓN DEL RESULTADO DE PARTIDOS DE LA NBA MEDIANTE MODELOS DE CLASIFICACIÓN SUPERVISADA
Predicción de Resultados de Partidos de la NBA – README
Este repositorio contiene el cuaderno Jupyter TFG.ipynb, en el que se desarrolla íntegramente el pipeline para predecir si el equipo local ganará un partido de la NBA (temporada 2023–2024) mediante modelos de clasificación supervisada.

📄 Descripción
A partir de estadísticas de partidos (puntos, porcentajes de tiro, rebotes, asistencias…), cuotas de apuestas y rachas de victorias, se construyen y comparan tres modelos de Machine Learning:

Regresión logística

Random Forest

XGBoost

Se optimizan sus hiperparámetros con GridSearchCV, se evalúan con métricas estándar (accuracy, precision, recall, F1-score, AUC) y se visualizan importancias de variables, matrices de confusión y curvas ROC.

📂 Estructura del proyecto
text
Copiar
Editar
/
├── TFG.ipynb                  # Notebook principal con todo el código
├── data/
│   └── Ingenieriadeldato_nba_2023-2024.csv  
│       └── Dataset consolidado (estadísticas + cuotas + etiquetas)
├── outputs/                   # Carpeta de gráficos y tablas exportados
├── requirements.txt           # Dependencias Python
└── README.md                  # Esta documentación
⚙️ Requisitos
Python 3.8+

Paquetes (instalables con pip install -r requirements.txt):

pandas

numpy

scikit-learn

xgboost

matplotlib

seaborn

jupyter

🔧 Instalación
Clonar el repositorio

bash
Copiar
Editar
git clone <URL-del-repo>
cd <nombre-de-la-carpeta>
Crear y activar un entorno virtual (opcional pero recomendado)

bash
Copiar
Editar

python -m venv venv
source venv/bin/activate    # Linux / macOS
.\venv\Scripts\activate     # Windows
Instalar dependencias

bash
Copiar
Editar
pip install --upgrade pip
pip install -r requirements.txt
Uso
Abrir el notebook

bash
Copiar
Editar
jupyter notebook TFG.ipynb
Ejecutar celdas de arriba hacia abajo. Cada sección está claramente comentada:

Carga y limpieza de datos

Ingeniería de variables

División Train/Test y escalado

Definición de GridSearchCV para cada modelo

Entrenamiento y evaluación

Gráficos de resultados

Exportar gráficos o tablas a outputs/, si se desea, usando las funciones de Matplotlib/Seaborn.

Pipeline paso a paso
Carga de datos

Lectura de CSV

Eliminación de duplicados

Conversión de tipos

Limpieza y consolidación

Relleno o eliminación de valores nulos

Unificación de estadísticas locales y visitantes

Inclusión de cuotas y etiquetas (Victoria_Local)

Ingeniería de características

Cálculo de 2P, 2PA, 2P%

Racha acumulada (+1/–1)

PTS_Diff (diferencia de puntos)

Redondeo de cuotas para agrupar

Preparación de X e y

Separación de variables predictoras y etiqueta

Split 80% entrenamiento / 20% test

Escalado de variables solo para regresión logística

Optimización de modelos

GridSearchCV(cv=5, scoring='roc_auc') para:

Regresión logística (C, penalty, solver)

Random Forest (n_estimators, max_depth, max_features, min_samples_split)

XGBoost (n_estimators, learning_rate, max_depth, subsample, colsample_bytree)

Evaluación

classification_report(): precision, recall, F1 por clase

roc_auc_score()

Matríz de confusión

Curvas ROC comparativas

Visualización

Importancia de variables (feature_importances_)

Histogramas de cuotas vs. porcentaje de acierto

Boxplots de outliers

Mapas de calor de correlaciones

 Datos
El archivo data/Ingenieriadeldato_nba_2023-2024.csv ya contiene:

Game ID, Date

Estadísticas locales (FG_L, 3P_L, ORB_L, etc.)

Estadísticas visitantes

Cuota_L, Cuota_V

Victoria_Local (0/1)

Variables derivadas (2P_L, 2P%_L, Racha_L, PTS_Diff…)

Contribuciones
Este cuaderno está diseñado para fines académicos.
Quedan abiertas sugerencias de:

Integración de variables de jugador (lesiones, minutos)

Extensión a datos en tiempo real vía API NBA

Añadir más modelos (Redes neuronales, SVM…)

Creación de un dashboard interactivo (Streamlit, Power BI)

Contacto
Autor: Claudia Martínez Urango
Tutor: Julio Emilio Sandubete Galán
Grado: Business Analytics · Curso 2024–2025
