##Predicción de Resultados de Partidos de la NBA – README  

Este repositorio contiene el cuaderno Jupyter **`TFG.ipynb`**, en el que se desarrolla íntegramente el pipeline para predecir si el equipo local ganará un partido de la NBA (temporada 2023–2024) mediante modelos de clasificación supervisada.

---

##  Descripción

A partir de estadísticas de partidos (puntos, porcentajes de tiro, rebotes, asistencias…), cuotas de apuestas y rachas de victorias, se construyen y comparan tres modelos de Machine Learning:

1. **Regresión logística**  
2. **Random Forest**  
3. **XGBoost**  

Se optimizan sus hiperparámetros con **GridSearchCV**, se evalúan con métricas estándar (accuracy, precision, recall, F1-score, AUC) y se visualizan importancias de variables, matrices de confusión y curvas ROC.

---

##  Estructura del proyecto

```text
/
├── TFG.ipynb                  # Notebook principal con todo el código
├── data/
│   └── Ingenieriadeldato_nba_2023-2024.csv  # Dataset consolidado
├── outputs/                   # Carpeta de gráficos y tablas
├── requirements.txt           # Dependencias Python
└── README.md                  # Esta documentación
```

---

##  Requisitos

- **Python 3.8+**  
- **Entorno virtual** (recomendado)  
- Instalación de paquetes:
  ```bash
  pip install -r requirements.txt
  ```
- **Archivo de datos**: `data/Ingenieriadeldato_nba_2023-2024.csv`

---

## Metodología

1. **Web Scraping**: obtención de datos de partidos y estadísticas desde Basketball Reference y Oddsportal.  
2. **Almacenamiento**: CSV individuales por temporada y consolidación en un solo dataset.  
3. **Limpieza**: eliminación de duplicados y tratamiento de nulos.  
4. **Ingeniería de características**: cálculo de variables derivadas (2P, 2P%, racha, diferencia de puntos, cuotas redondeadas).  
5. **Modelado**: entrenamiento con 3 algoritmos (Regresión logística, Random Forest, XGBoost).  
6. **Optimización**: búsqueda de hiperparámetros con GridSearchCV(cv=5, scoring='roc_auc').  
7. **Evaluación**: uso de métricas de clasificación y curvas ROC para selecionar el mejor modelo.  
8. **Visualización**: gráficos de importancia, matrices de confusión y análisis descriptivo.

---

## Instalación

1. **Clonar repositorio**  
   ```bash
   git clone <URL-del-repo>
   cd <nombre-de-la-carpeta>
   ```
2. **Entorno virtual**  
   ```bash
   python -m venv venv
   source venv/bin/activate    # Linux/macOS
   .\venv\Scripts\activate  # Windows
   ```
3. **Instalar dependencias**  
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

---

##  Uso

1. **Iniciar Jupyter Notebook**  
   ```bash
   jupyter notebook TFG.ipynb
   ```
2. **Ejecutar celdas** en orden:
   - Carga y limpieza de datos  
   - Ingeniería de variables  
   - División Train/Test y escalado  
   - Definición y ajuste de GridSearchCV  
   - Evaluación y métricas  
   - Generación de gráficos y reportes  
3. **Exportar resultados** a `outputs/` si se desea.

---

## Pipeline paso a paso

1. **Carga de datos**  
2. **Limpieza y consolidación**  
3. **Ingeniería de características**  
4. **Preparación de X e y**  
5. **Optimización de modelos**  
6. **Evaluación**  
7. **Visualización**  
---
## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo [LICENSE](https://github.com/claudiamartinezurango/TFG/blob/main/LICENSE) para más detalles.
---
## Contacto
* Autor : Claudia Martínez Urango
* Email : .[martinezurangoclaudia@gmail.com].(mailto:martinezurangoclaudia@gmail.com).
  
