# evaluacion-movilidad-latam
Proyecto de analítica de datos orientado a evaluar el impacto de la congestión vial en la economía de 15 ciudades latinoamericanas. Mediante procesos ETL en Python y SQL.
# **Evaluación de la movilidad urbana y su relación con la productividad económica en Latinoamérica**

## Contexto del Negocio

A partir del análisis realizado, no se encontró una relación directa entre la movilidad urbana y la productividad económica. Para ello, se utilizaron variables como el retraso total en minutos (JamsDelay), que representa la congestión en vías, y los datos reportados de producto interno bruto en dólares por ciudad (City GDP/capita). Esto es relevante, ya que el análisis se realizó a nivel de grupo de ciudades; sin embargo, es importante destacar que esto no excluye que, para cada ciudad, la relación entre estas dos variables exista. En cambio, indica que no es un patrón que pueda describir de manera contundente la economía y el tránsito de una ciudad.

## Metodología

- **Exploración:** Diagnóstico inicial de las fuentes para validar la estructura y la integridad de las variables.
- **Limpieza y ETL:** Estandarización de columnas a *snake_case*, conversión de tipos de datos (`object` a `float64`/`datetime`), eliminación de caracteres especiales y ajuste del separador decimal a punto (`.`).
- **Consolidación:** Cálculo de promedios de tráfico e integración de *datasets* mediante un **INNER JOIN**, usando `ciudad` y `año` como llaves.
- **Análisis Visual (EDA):** * ***Boxplots*:** Evidenciaron valores atípicos (*outliers*) de congestión por encima de la media en todas las urbes, con **Ciudad de México, São Paulo y Bogotá** a la cabeza.
    - ***Histogramas*:** Mostraron una distribución normal y homogénea en el PIB de la muestra.
    - ***Scatter Plots*:** Confirmaron la **ausencia de una correlación global fuerte** entre el PIB y el retraso vial; salvo Ciudad de México (alta en ambos), las demás ciudades muestran un comportamiento disperso.
