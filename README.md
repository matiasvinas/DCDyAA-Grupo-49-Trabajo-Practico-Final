# Diplomatura en Ciencia de Datos y Análisis Avanzado - UTN
# Trabajo Práctico Final
# Grupo 49
## Integrantes

- Matías Ezequiel Viñas
- Diana Carolina Uribe

## Proyecto: Pronóstico de ventas diarias en tiendas Rossmann

Este repositorio contiene el trabajo práctico final integrador de la Diplomatura en Ciencia de Datos y Análisis Avanzado. El objetivo del proyecto es desarrollar un modelo predictivo para estimar las ventas diarias de las tiendas Rossmann, utilizando información histórica, promocional, temporal y competitiva.

El análisis incluye:
- carga y unión de datasets,
- limpieza y tratamiento de valores faltantes,
- análisis exploratorio de datos (EDA),
- feature engineering temporal,
- prevención de data leakage,
- entrenamiento y evaluación de modelos de machine learning.

---

## Descripción del problema

Rossmann es una cadena minorista con múltiples tiendas en Europa. La capacidad de estimar ventas diarias con anticipación es clave para:
- planificación comercial,
- gestión de stock,
- optimización de promociones,
- toma de decisiones operativas,
- control de recursos y presupuestos.

El proyecto busca construir un modelo capaz de predecir ventas diarias tomando en cuenta variables como:
- promociones activas,
- días de la semana,
- feriados,
- tipo de tienda,
- distancia a la competencia,
- antigüedad de competidores,
- estacionalidad mensual y anual.

---

## Datos utilizados

Se emplea el dataset público de Rossmann Store Sales, disponible en Kaggle.

### Fuente
- https://www.kaggle.com/c/rossmann-store-sales

### Archivos principales
El conjunto de datos incluye información histórica de ventas y atributos de las tiendas, entre los principales:
- `Store`
- `Date`
- `Sales`
- `Customers`
- `Open`
- `Promo`
- `StateHoliday`
- `SchoolHoliday`
- `StoreType`
- `Assortment`
- `CompetitionDistance`
- `CompetitionOpenSinceMonth`
- `CompetitionOpenSinceYear`
- `Promo2`
- `Promo2SinceWeek`
- `Promo2SinceYear`
- `PromoInterval`

---

## Objetivos

- Analizar el comportamiento de las ventas diarias.
- Realizar limpieza y transformación de datos con criterio de negocio.
- Identificar variables relevantes para el pronóstico.
- Construir features temporales y comerciales.
- Evitar la fuga de información (data leakage).
- Entrenar modelos predictivos adecuados para regresión.
- Evaluar el desempeño de los modelos y comparar resultados.
- Extraer conclusiones útiles para la operación comercial.

---

## Metodología

El proyecto sigue una estrategia robusta de ciencia de datos:

1. Carga inicial de los datasets.
2. Unión de ventas con datos de tiendas.
3. Filtrado de registros no representativos.
4. Tratamiento de nulos y valores atípicos.
5. Análisis exploratorio de datos.
6. Feature engineering temporal.
7. Eliminación de variables con riesgo de leakage.
8. Preparación de `X` e `y` para modelado.
9. Entrenamiento de modelos.
10. Evaluación y comparación de resultados.
11. Interpretación de hallazgos y conclusiones.

---

## Preprocesamiento realizado

Se aplicaron criterios de negocio para mejorar la calidad del dataset, entre ellos:
- exclusión de días con tiendas cerradas o con ventas iguales a cero,
- imputación de distancia a la competencia cuando no existía competencia cercana,
- tratamiento de valores faltantes para promociones,
- capping de ventas extremas con percentil 99 para evitar distorsiones,
- extracción de variables temporales como mes, año, día y número de semana,
- cálculo de antigüedad de la competencia en meses,
- eliminación de la variable `Customers` para evitar fuga de datos.

---

## Modelado

Se trabajó con modelos orientados a regresión para pronosticar ventas diarias. El enfoque principal fue construir un modelo que:
- capture la estacionalidad semanal y mensual,
- considere promociones y feriados,
- incorpore atributos de la tienda,
- sea interpretable desde el punto de vista comercial,
- generalice razonablemente sobre datos nuevos.

---

## Requisitos

Para ejecutar el notebook es recomendable contar con:

- Python 3.x
- Jupyter Notebook o Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

---

## Cómo ejecutar

### Opción 1: Google Colab
1. Subir el notebook a Google Colab.
2. Montar Google Drive si se están utilizando archivos locales.
3. Cargar los CSV del dataset en la carpeta correspondiente.
4. Ejecutar las celdas del notebook en orden.

### Opción 2: Jupyter local
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/matiasvinas/DCDyAA-Grupo-49-Trabajo-Practico-Final.git
