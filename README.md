# 📊 Predicción de Retraso del Time to Market (T2M) de proyectos bancarios con Machine Learning

Repositorio oficial del trabajo de tesis enfocado en la aplicación de modelos de Machine Learning y análisis de datos para predecir el *Time to Market* (TTM) y detectar de forma temprana riesgos de retraso en proyectos.

---

## 🚀 Descripción del Proyecto
Este proyecto analiza un conjunto histórico de datos de proyectos para identificar patrones de retraso en función de variables clave como el presupuesto, la complejidad técnica, el área de negocio y las dependencias asociadas. El objetivo principal es proporcionar una herramienta predictiva basada en datos que permita a los equipos anticiparse a las desviaciones en los tiempos de entrega.

---

## 🛠️ Tecnologías y Librerías Utilizadas
El proyecto está desarrollado íntegramente en **Python**, utilizando las siguientes librerías de ciencia de datos:
* **Manipulación y Limpieza de Datos:** `pandas`, `numpy`
* **Visualización:** `matplotlib`, `seaborn`
* **Modelado Predictivo (Machine Learning):** `scikit-learn` (Linear Regression, Ridge Regression, Random Forest Regressor)
* **Control de versiones:** `Git`

---

## 📂 Estructura del Repositorio

```text
├── Archivos antiguos/          # (Ignorado en el control de versiones)
├── resultados/
│   └── proyectos_evaluados.xlsx# Resultados del despliegue por lotes con alertas de retraso
├── app.ipynb                   # Jupyter Notebook principal (EDA, entrenamiento y evaluación)
├── Base de datos T2M.csv       # Dataset histórico principal
├── proyectos_data.xlsx         # Dataset de prueba para el despliegue por lotes (Batch Scoring)
└── README.md                   # Documentación del proyecto

```

## ⚙️ Metodología y Fases del Proyecto

1. **Análisis Exploratorio de Datos (EDA) y Limpieza:**
* Tratamiento de valores nulos, estandarización de formatos monetarios (`Presupuesto`) y validación de consistencia en variables categóricas.
* Extracción de características temporales (*Feature Engineering*) a partir de las fechas de inicio (`Mes_Inicio`, `Trimestre_Inicio`).


2. **Transformación de Variables:**
* Aplicación de transformación logarítmica (`np.log1p`) sobre la variable objetivo (`Time to market`) para normalizar su distribución.
* Codificación *One-Hot Encoding* para variables categóricas y estandarización numérica (`StandardScaler`).


3. **Modelado y Evaluación:**
* Entrenamiento y comparación de múltiples algoritmos de regresión.
* El modelo seleccionado como ganador fue **Random Forest Regressor**, obteniendo un rendimiento superior en métricas clave:
* **$R^2$ (Coeficiente de Determinación):** ~0.76
* **MAE (Error Absoluto Medio):** ~35 días
* **RMSE (Raíz del Error Cuadrático Medio):** ~48 días




4. **Despliegue por Lotes (*Batch Scoring*):**
* Automatización de predicciones sobre nuevos proyectos (`proyectos_data.xlsx`), calculando el desfase estimado y generando alertas automáticas (`En Tiempo` vs `Alerta: Posible Retraso`).



---

## 📈 Resultados Principales

* El modelo permite realizar proyecciones con un margen de error competitivo, sirviendo como soporte para la toma de decisiones gerenciales y de gestión de proyectos.

---

```

```

