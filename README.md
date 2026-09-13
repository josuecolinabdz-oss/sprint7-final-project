# Análisis Exploratorio y Segmentación de Clientes — ConnectaTel

## Objetivo del Proyecto
El objetivo principal de este análisis es evaluar los patrones de consumo de los clientes de ConnectaTel (llamadas, minutos y mensajes) para identificar segmentos clave por edad y uso, analizar el impacto de los usuarios de consumo intensivo (*heavy users*) y generar recomendaciones estratégicas orientadas a la optimización de planes y rentabilidad del negocio.

## Datasets Utilizados
El análisis integra tres fuentes de datos principales:
* **`plans.csv`**: Información sobre los planes tarifarios actuales (precios, minutos incluidos, GB incluidos y costos por exceso).
* **`users_dates.csv`**: Datos demográficos e información de registro de los clientes (edad, ciudad, fecha de registro, plan contratado).
* **`usage_dates.csv`**: Registro detallado de uso individual de servicios móviles (duración de llamadas y conteo de mensajes).

## Etapas del Análisis Realizadas
1. **Carga y exploración inicial**: Lectura de datasets, inspección de tipos de datos y revisión de primeros registros.
2. **Limpieza y preparación de datos**: Tratamiento de valores nulos, imputación de datos incompletos y conservación estratégica de eventos de duración cero (llamadas no completadas).
3. **Análisis Exploratorio de Datos (EDA)**: Construcción de histogramas de distribución para edad, mensajes, llamadas y duración total.
4. **Identificación de Outliers**: Evaluación del límite superior mediante el método IQR en diagramas de caja (*boxplots*) y toma de decisión técnica para conservar a los *heavy users*.
5. **Segmentación de Clientes**:
   * **Por Uso**: Clasificación en *Baja gama*, *Gama media* y *Alta gama*.
   * **Por Edad**: Categorización en *Joven* (<30), *Adulto* (30-59) y *Adulto Mayor* (≥60).
6. **Insight Ejecutivo**: Redacción del informe final para stakeholders con diagnósticos y recomendaciones de negocio.

## Cómo Ejecutar el Notebook

### Opción 1: Abrir directamente en Google Colab
1. Haz clic en el archivo `.ipynb` dentro de este repositorio de GitHub.
2. Copia la URL de la página.
3. Ve a [Google Colab](https://colab.research.google.com/), selecciona la pestaña **GitHub**, pega la URL y presiona Enter.

### Opción 2: Ejecución Local (Jupyter Notebook / JupyterLab)
1. Asegúrate de tener instalado Python 3.x y Jupyter Notebook.
2. Clona este repositorio o descarga el archivo `.ipynb`.
3. Abre la terminal o consola de comandos en la carpeta del proyecto y ejecuta `jupyter notebook`.

## Guía de Reproducción
1. **Requisitos previos**: Tener instaladas las librerías `pandas`, `matplotlib`, `seaborn` y `numpy`.
2. **Estructura de archivos**: Asegúrate de mantener la ruta correcta de los archivos `.csv` en la celda inicial de carga.
3. **Ejecución secuencial**: Ejecuta las celdas en orden descendente (`Kernel` → `Restart & Run All`) para garantizar que las transformaciones se apliquen correctamente.
