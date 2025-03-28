# 📌 Solemne 1 - Mineria de Datos sobre Contaminacion del Aire

## 📝 Descripcion
Este proyecto realiza un **analisis de la calidad del aire** utilizando datos de **Google BigQuery** y la API de **OpenAQ**. Nos enfocamos en estudiar la contaminacion en distintas partes del mundo, con un enfoque especial en **Estados Unidos**, evaluando la calidad del aire en varias ciudades y comparando los niveles de contaminantes.

A traves de consultas SQL avanzadas y visualizaciones, buscamos identificar **patrones y tendencias** en los niveles de contaminacion, lo que permite comprender mejor los factores que afectan la calidad del aire y su evolucion en el tiempo.

En el caso de Estados Unidos, analizamos los niveles de contaminacion en diferentes ciudades, evaluando la presencia de contaminantes como **PM2.5, PM10, NO2 (dioxido de nitrogeno) y O3 (ozono troposferico)**. Ademas, realizamos estudios en diferentes periodos de tiempo, centrandonos en años especificos para observar tendencias y cambios en la calidad del aire a lo largo del tiempo.

Los códigos respectivos de este proyecto fueron hechos por separado, unificados en una sola terminal, y luego subidos a GitHub.

---

## 🔧 Requisitos
Para ejecutar el código, es necesario contar con las siguientes librerias y herramientas:

- Python 3.x
- Google Cloud SDK (para autenticación en BigQuery)
- Librerias de Python:
  - `google.cloud.bigquery`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `numpy`

Ademas, se requiere configurar las credenciales de **Google Cloud** para acceder a **BigQuery**.

---

## 🛠 Instalacion
1. **Clonar el repositorio** o descargar el archivo `.ipynb`.
2. **Instalar las librerias necesarias:**
   ```bash
   pip install google-cloud-bigquery pandas matplotlib seaborn numpy
   ```
3. **Configurar credenciales de BigQuery:**
   - Crear un proyecto en Google Cloud.
   - Habilitar la API de BigQuery.
   - Generar un archivo de credenciales JSON y exportarlo:
     ```bash
     export GOOGLE_APPLICATION_CREDENTIALS="ruta/al/archivo.json"
     ```

---

## 🚀 Uso del Codigo
1. **Ejecutar las celdas de carga de datos** para extraer informacion desde BigQuery y OpenAQ.
2. **Realizar la limpieza de datos** para eliminar valores nulos o inconsistentes.
3. **Ejecutar las consultas SQL** para obtener datos de contaminacion.
4. **Analizar los resultados** mediante tablas y visualizaciones.
5. **Generar graficos** para interpretar los niveles de contaminacion en distintas ciudades.

---

## 📂 Estructura del Proyecto
El proyecto esta dividido en varias etapas:

### 1️⃣ **Carga de Datos**
- Se extraen datos desde **BigQuery** y la API de **OpenAQ**.
- Se listan los paises y sus respectivas ciudades con datos disponibles.

### 2️⃣ **Limpieza y Transformacion**
- Se eliminan valores nulos o erroneos.
- Se ajusta el formato de fechas y nombres de columnas.

### 3️⃣ **Analisis de Contaminacion en EE.UU.**
- Se filtran los datos de ciudades de **Estados Unidos**.
- Se comparan los niveles de contaminacion entre distintos estados.
- Se identifican las ciudades con **mayor contaminacion** y sus tendencias a lo largo del tiempo.
- Se analizan los contaminantes mas comunes, como **PM2.5, PM10, NO2 y O3**.
- Se realizan estudios en diferentes periodos de tiempo para evaluar la evolucion de la contaminacion en el pais.

### 4️⃣ **Visualizacion de Datos**
- Se generan **graficos de barras, lineas y mapas** para visualizar los niveles de contaminacion.
- Se analizan patrones temporales y geograficos.

---

## 📊 Resultados Esperados
- Identificacion de los paises y ciudades con mayor contaminacion.
- Comparacion de los niveles de contaminacion en distintas ciudades de EE.UU.
- Visualizacion de tendencias temporales en la calidad del aire.
- Conclusiones sobre los factores que afectan la contaminacion en diferentes regiones.

---

## 🌍 Fuentes de Datos
- **Google BigQuery Public Datasets:** Base de datos sobre contaminacion atmosferica.
- **OpenAQ API:** Mediciones en tiempo real de calidad del aire en distintas ciudades del mundo.

-------



##  📈 Análisis de RESULTADOS De correlación
1. Ciudades mas contaminadas (2019-2022)

Se seleccionaron las 10 ciudades de USA más contaminadas por año según los niveles promedio de PM2.5 y PM10.

Algunas ciudades solo tienen datos de un contaminante (por ejemplo, Muskogee en 2019 solo tiene PM10, y BANNOCK solo tiene PM2.5),
Esto se debe a la falta de informacion del mismo archivo, cada año se encontraron distintos tipos de poluciones.
Se observan diferencias significativas en los niveles de contaminación entre años y ciudades.

2. Datos ausentes y su impacto

En varias ciudades, faltan valores de PM10 o PM2.5, lo que puede indicar:

Falta de mediciones en ciertos años.

Limitaciones en la recolección de datos en algunas ciudades.

Posible sesgo en la selección del querry o estaciones de monitoreo.

3. Correlación entre PM2.5 y PM10

La matriz de correlación muestra un valor de -0.31 entre PM2.5 y PM10.

Esto significa que, en esta selección de ciudades, cuando los niveles de PM10 aumentan, los de PM2.5 tienden a disminuir, y viceversa.

Sin embargo, una correlación negativa tan baja indica que PM2.5 y PM10 no siempre siguen el mismo patrón en estas ciudades. Pode ser a la falta de valores por año que afecta en la correlación final entre las ciudad desde el 2019 al 2022.

4. Ciudades con valores extremos

En 2020, "POWDER RIVER" tiene un PM10 de 132, mientras que en 2021, "MADISON" tiene PM2.5 de 150.8, valores muy altos en comparación con otras ciudades.

El "Centro" aparece en múltiples años con altos valores de PM10 y niveles bajos de PM2.5.

En 2022, "MONO" destaca con PM10 de 104.8 y un PM2.5 de 5.6, lo que refuerza la idea de que no siempre hay una relación fuerte entre los dos contaminantes.

---



------
## 👥 Autores y Creditos
Proyecto desarrollado para el curso de **Mineria de Datos**, basado en datos abiertos y herramientas de analisis de Google Cloud.

**Autores:** Cristobal Cabrera, Mauricio Badilla y Nicolás Concha

---


