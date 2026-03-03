# Ensamble de Algoritmos — Regresión con Random Forest, GBM y XGBoost

> *"No basta con que el modelo converja. Necesito entender por qué converge."*

Pipeline completo de predicción de precios inmobiliarios (Boston Housing) con selección formal de características y comparación de tres algoritmos de ensamble. Cada decisión de modelado tiene justificación matemática explícita, desarrollado de forma autodidacta.

---

## Contenido

- **Selección de características:** Fisher J, Correlación de Pearson, Covarianza Normalizada → SFS → Branch & Bound
- **Modelos:** Random Forest, Gradient Boosting (GBM), XGBoost
- **Evaluación:** RMSE, MAE, R² en test y datos nuevos (bootstrap)
- **Accionabilidad:** Segmentación en 4 cuartiles de precio + análisis de viviendas con mayor error de predicción

## Resultados

| Modelo | RMSE | MAE | R² |
|---|---|---|---|
| Random Forest | 4.124 | 2.538 | 0.828 |
| GBM | 4.061 | 2.564 | 0.825 |
| **XGBoost** | **3.668** | **2.389** | **0.861** |

XGBoost lidera el comparativo en las tres métricas con regularización L2 explícita y early stopping.

## Tecnologías

- **Lenguaje:** R
- **Reporte:** Quarto (`.qmd`) → HTML
- **Librerías principales:** `randomForest`, `gbm`, `xgboost`, `caret`, `ggplot2`, `igraph`, `dplyr`
- **Dataset:** `Boston` (MASS) — 506 observaciones, 13 variables predictoras

## Reproducibilidad

```r
# Instalar dependencias
install.packages(c("MASS","randomForest","xgboost","caret","ggplot2",
                   "gridExtra","gbm","reshape2","dplyr","igraph","scales","purrr"))

# Renderizar
quarto::quarto_render("Ensamble de Algoritmos - Regresión.qmd")
```

El dataset es nativo de R (`data(Boston)`), no requiere archivos externos. `set.seed(123)` garantiza reproducibilidad total.

## Publicación

📊 Reporte completo en RPubs: [rpubs.com/Alej5ndro](https://rpubs.com/Alej5ndro)

## Autor

**Alejandro Figueroa Rojas**  
Ingeniero Comercial — Business Intelligence & Ciencia de Datos  
Aprendizaje autodidacta con foco en rigor matemático y accionabilidad de resultados.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Alejandro%20Figueroa-blue?logo=linkedin)](https://www.linkedin.com/in/alejandrofigueroarojas)
[![RPubs](https://img.shields.io/badge/RPubs-Alej5ndro-red?logo=r)](https://rpubs.com/Alej5ndro)
[![Email](https://img.shields.io/badge/Email-alejandro.figueroa.rojas%40gmail.com-green?logo=gmail)](mailto:alejandro.figueroa.rojas@gmail.com)

---
