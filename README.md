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

### 1. Carga y Exploración de Datos
- Carga de datasets desde archivos Excel
- Análisis exploratorio de datos (EDA)
- Identificación de patrones y correlaciones

### 2. Selección de Variables
- **Variables de entrada (X):** Selección cuidadosa de features sin filtrar información del target
- **Variable objetivo (Y):** Puntaje de Taza como métrica de calidad

### 3. Preprocesamiento

#### Variables de Entrada (X):
- Imputación de valores faltantes
- Escalado y normalización de datos numéricos
- Codificación de variables categóricas

#### Variable Objetivo (Y):
- Revisión de distribución del Puntaje de Taza
- Aplicación de transformaciones si es necesario

### 4. Entrenamiento de Modelos
- **Modelo 1:** Regresión Lineal
- **Modelo 2:** Random Forest Regressor
- División de datos en conjuntos de entrenamiento y prueba

### 5. Evaluación de Modelos
- **Métricas utilizadas:**
  - RMSE (Root Mean Square Error)
  - MAE (Mean Absolute Error)
  - R² (Coeficiente de Determinación)
- Comparación de rendimiento entre modelos

### 6. Explicabilidad
- **LIME:** Explicaciones locales para predicciones individuales
- **SHAP:** Valores de Shapley para interpretabilidad global
- **Feature Importance:** Importancia de características en Random Forest

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
- Comparación de RMSE, MAE y R² entre modelos
- Identificación del modelo con mejor rendimiento

### Visualizaciones
- Gráficos de distribución de datos
- Matrices de correlación
- Gráficos de importancia de características
- Visualizaciones de explicabilidad (LIME/SHAP)

### Interpretabilidad
- Identificación de variables más influyentes en la calidad del café
- Explicaciones de predicciones individuales
- Insights sobre factores que determinan el Puntaje de Taza

## Autor y Licencia

**Autor:** [Tu Nombre]  
**Institución:** Universidad Nacional de Colombia - Medellín (UNALMED)  
**Curso:** Aprendizaje Automático  
**Licencia:** MIT License

---

*Este proyecto es parte del desarrollo académico en técnicas de machine learning aplicadas a la industria cafetera.*