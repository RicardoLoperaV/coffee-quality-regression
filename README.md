# Predicción de Calidad de Café

## Descripción

**Objetivo:** Predecir la calidad del café basándose en el Puntaje de Taza utilizando técnicas de aprendizaje automático y regresión.

Este proyecto forma parte de la Tarea 1 del curso de Aprendizaje Automático de UNALMED, donde se implementan modelos de regresión para predecir la calidad del café a partir de diversas características y métricas de evaluación.

## Estructura del Repositorio

```
coffee-quality-regression/
├── .gitignore                    # Archivos ignorados por Git
├── CC_FT_17_Calidad.xlsx        # Dataset de calidad del café
├── CC_FT_18_Tostion.xlsx        # Dataset de tostión del café
├── CC_FT_21_Despachos.xlsx      # Dataset de despachos
├── Coffee_Cup_Score.ipynb       # Notebook principal del proyecto
└── README.md                    # Documentación del proyecto
```

## Flujo de Trabajo

### 1. Procesamiento de datos

- **Importación de librerías**  
  Se cargan todas las librerías necesarias para análisis, visualización y modelado.

- **Carga y limpieza de datos de calidad**  
  - Importación de varias hojas del archivo Excel de calidad con `pd.read_excel()`.
  - Eliminación de columnas y filas irrelevantes (encabezados extra, pies de página).
  - Normalización de nombres de columnas y depuración de los DataFrames.

- **Unificación de datos de calidad**  
  - Concatenación de los DataFrames de las diferentes hojas en uno solo (`df_Calidad`).

- **Procesamiento de notas de catación**  
  - Limpieza y conversión de las notas en listas uniformes.
  - Aplicación de one-hot encoding para convertir cada nota en una variable binaria.

- **Carga y limpieza de datos de tostión**  
  - Importación de varias hojas del archivo Excel de tostión.
  - Eliminación de columnas y filas innecesarias.
  - Normalización de nombres de columnas y verificación de tipos de datos.

- **Unificación de datos de tostión**  
  - Concatenación de los DataFrames de tostión en uno solo (`df_Tostion`).

- **Fusión de datos de calidad y tostión**  
  - Unión de `df_Calidad` y `df_Tostion` usando la columna `LOTE` como clave para obtener un único DataFrame (`df_full`).

- **Transformación y corrección de variables**  
  - Conversión de columnas de tiempo y temperatura a formato numérico.
  - Unificación de valores categóricos inconsistentes (errores ortográficos, variantes).
  - Conversión de columnas numéricas al tipo adecuado.

---

### 2. Modelado y análisis

- **Selección de variables**  
  - Identificación de variables predictoras (X) y variable objetivo (Y).
  - Procesamiento de variables categóricas mediante pipelines y one-hot encoding.

- **Imputación de valores faltantes**  
  - Reemplazo de valores NaN en la variable objetivo.

- **División de los datos**  
  - Separación en conjuntos de entrenamiento y prueba con `train_test_split`.

- **Entrenamiento de modelos de regresión**  
  - Entrenamiento de modelos como RandomForestRegressor y XGBRegressor.

- **Evaluación de desempeño**  
  - Cálculo de métricas como MSE y R² en el conjunto de prueba.
  - Validación cruzada para evaluar la estabilidad y capacidad de generalización.

- **Interpretación y explicabilidad**  
  - Análisis de importancia de variables (feature importance).
  - Interpretación con SHAP para entender el impacto de cada variable.

- **Visualización y reporte de resultados**  
  - Gráficas de importancia de variables y comparación entre modelos.
  - Conclusiones sobre los factores que determinan

## Requisitos

### Software
- Python >= 3.8

### Librerías Necesarias
```
pandas
numpy
scikit-learn
matplotlib
seaborn
lime
shap
openpyxl
jupyter
xgboost
```

## Instrucciones de Uso

### 1. Clonar el Repositorio
```bash
git clone https://github.com/usuario/coffee-quality-regression.git
cd coffee-quality-regression
```

### 2. Instalación de Dependencias
```bash
pip install pandas numpy scikit-learn matplotlib seaborn lime shap openpyxl jupyter
```

### 3. Ejecutar el Notebook
```bash
jupyter notebook Coffee_Cup_Score.ipynb
```

## Resultados Esperados

### Métricas de Evaluación
- Cálculo y comparación de MSE (Mean Squared Error) y R² (coeficiente de determinación) para los modelos de regresión
- Evaluación de desempeño mediante validación cruzada
- Selección del modelo con mejor capacidad predictiva

### Visualizaciones
- Gráficos de distribución y limpieza de datos
- Matrices de correlación entre variables
- Gráficos de importancia de características (feature importance) para RandomForestRegressor y XGBRegressor
- Visualizaciones de explicabilidad con SHAP (SHapley Additive exPlanations)

### Interpretabilidad
- Identificación de las variables más influyentes en la predicción de la calidad del café
- Análisis detallado del impacto de cada variable en la predicción usando SHAP
- Conclusiones sobre los factores determinantes del Puntaje de Taza y recomendaciones prácticas

## Autor y Licencia

**Autor:** Ricardo Esteban Lopera Vasco

**Institución:** Universidad Nacional de Colombia - Medellín (UNALMED) 

**Curso:** Aprendizaje Automático  
