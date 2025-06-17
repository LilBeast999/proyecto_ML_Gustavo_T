
# Proyecto de Machine Learning: Detección de Fibrilación Auricular (AFib)

Este repositorio contiene el proyecto del curso de Machine Learning, donde se entrena y evalúa un clasificador supervisado para distinguir entre señales ECG normales y con AFib.

## Objetivo
Entrenar un modelo de clasificación básico y evaluar su desempeño con métricas estándar (Accuracy, Precision, Recall, F1-score) y visualización de la matriz de confusión.

## Estructura del repositorio

```
proyecto_ML_Gustavo_T/
├── data/
│   ├── training2017/           # Archivos .mat/.hea originales de PhysioNet
│   └── ecg_features.csv        # CSV con características extraídas (30 registros)
├── notebooks/
│   ├── Semana_1_Exploracion.ipynb       # Cálculo de features y análisis exploratorio
│   └── Semana_2_Reproduccion_Baseline.ipynb  # Entrenamiento y evaluación del modelo
└── README.md
```

## Descripción de los datos
- Se trabajó con 30 registros de ECG (15 normales, 15 AFib) del conjunto `training2017`.
- Para cada registro se calculan estadísticas de amplitud (`media_mv`, `mstd_mV`, `skewness`, `kurtosis`) y de intervalos RR (`rr_mean_s`, `rr_std_s`).
- El archivo `ecg_features.csv` agrupa estas 10 características más la etiqueta `label`.

## Notebooks

1. **Semana 1: Exploración del dataset**  
   Ruta: `notebooks/Semana_1_Exploracion.ipynb`  
   - Carga y visualización de segmentos ECG.  
   - Extracción de features y guardado en CSV.  
   - Análisis de distribuciones y conclusiones sobre las variables.

2. **Semana 2: Reproducción del baseline**  
   Ruta: `notebooks/Semana_2_Reproduccion_Baseline.ipynb`  
   - División de datos en train/test con `train_test_split`.  
   - Entrenamiento de un SVM (baseline).  
   - Cálculo de Accuracy, Precision, Recall, F1-score.  
   - Visualización de la matriz de confusión.  
   - Breve análisis de los resultados.

## Instrucciones para ejecutar

1. Clonar el repositorio:  
   `git clone https://github.com/LilBeast999/proyecto_ML_Gustavo_T`

2. Instalar dependencias (idealmente en un entorno virtual):  
   ```
   pip install wfdb numpy pandas scipy matplotlib seaborn scikit-learn
   ```

3. Asegurarse de tener la carpeta `data/training2017/` con los archivos `.mat/.hea`.

4. Abrir los notebooks en VS Code o Jupyter y ejecutar célula por célula.

---

**Autor:** Gustavo  
**Fecha:** junio de 2025  