Taller Espacial de Amenidades de Salud en Parroquias de Ecuador
Descripción del Proyecto
Este proyecto tiene como objetivo realizar un análisis espacial de la distribución de amenidades de salud, específicamente hospitales, en la provincia de Latacunga, Cotopaxi, Ecuador. Se analiza la distribución espacial de estas amenidades en relación con la población en las parroquias y sectores censales de la región. Además, se calcula el índice de Moran para evaluar la autocorrelación espacial de las amenidades de salud.

Estructura del Proyecto
Parte 1: Identificación y reflexión sobre las amenidades de salud en Latacunga-Cotopaxi.
Parte 2: Unión de polígonos de zonas censales a nivel de parroquias.
Parte 3: Cálculo del número total de amenidades.
Parte 4: Cálculo del ratio de amenidades por habitante.
Parte 5: Cálculo del índice de Moran para el indicador de amenidades de salud.
Parte 6: Actividad opcional de análisis de buffers y reflexión sobre los límites de OpenStreetMap.
Requisitos
Para ejecutar el código en este proyecto, es necesario tener instalado R y las siguientes librerías:

osmdata: Para obtener datos de OpenStreetMap.
sf: Para trabajar con datos espaciales.
tidyverse: Para manipulación y visualización de datos.
readxl: Para leer archivos de Excel.
spdep: Para análisis espacial, incluyendo el cálculo del índice de Moran.
lattice: Para la visualización de la matriz de pesos espaciales.
httr2: Para realizar solicitudes HTTP.

Archivos Necesarios
GEODATABASE_NACIONAL_2021.gdb: Base de datos geoespacial que contiene los polígonos de las zonas censales.
01_2022_CPV_Estructura_poblacional.xlsx: Contiene la estructura poblacional para las parroquias.
CODIFICACIÓN_2024.xlsx: Archivo de codificación utilizado para unir la información de población con las zonas censales.
Ejecución del Código
El código está diseñado para ser ejecutado en un entorno R Markdown, con salida en formato DOCX. Puedes ejecutar cada bloque de código secuencialmente desde un archivo .Rmd.

Carga de Librerías: El primer bloque de código carga las librerías necesarias y define la zona de interés (Latacunga).
Consulta de OpenStreetMap: Se obtienen los puntos de los hospitales en la zona de interés.
Procesamiento de Datos: Se cargan y procesan los datos de población y se unen con las zonas censales.
Visualización: Se crean mapas para visualizar la distribución de hospitales y densidad poblacional.
Análisis Espacial: Se calcula el índice de Moran para evaluar la autocorrelación espacial de las amenidades de salud.
Buffer y Análisis Opcional: Se analiza la proximidad de los hospitales a un punto de interés definido por el usuario.
Resultados Esperados
El análisis permite identificar patrones de distribución de los hospitales en la provincia de Latacunga, Cotopaxi, y evaluar la accesibilidad a estos servicios de salud mediante el cálculo del ratio de amenidades por habitante y el índice de Moran. Adicionalmente, se exploran las limitaciones de la cobertura geográfica usando buffers alrededor de un punto de interés.

Notas y Consideraciones
Precisión de los Datos: Los resultados dependen de la calidad y precisión de los datos obtenidos de OpenStreetMap y los archivos geoespaciales utilizados.
Limitaciones: Los análisis de buffers y la cobertura de amenidades pueden variar dependiendo de la exactitud de los datos de coordenadas y la proyección geográfica utilizada.
