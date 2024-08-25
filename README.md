# Taller Espacial de Amenidades de Salud en Parroquias de Ecuador

Este proyecto realiza un análisis espacial de las amenidades de salud, específicamente hospitales, en la provincia de Cotopaxi, Ecuador. Se utiliza la ciudad de Latacunga como caso de estudio para explorar la distribución de hospitales y su relación con la densidad poblacional en diferentes parroquias.

## Contenido

- **Parte 1: Identificación y Reflexión sobre las Amenidades de Salud**  
  Definición de la zona de interés (Latacunga-Cotopaxi) y obtención de los puntos de hospitales desde OpenStreetMap.

- **Parte 2: Unión de Polígonos de Zonas Censales a Nivel de Parroquias**  
  Procesamiento de datos censales, unión de polígonos y análisis de la población en parroquias.

- **Parte 3: Cálculo del Número Total de Amenidades**  
  Cálculo del número de hospitales en cada parroquia y análisis espacial de la distribución de hospitales.

- **Parte 4: Cálculo del Ratio de Amenidades por Habitante**  
  Cálculo de un indicador de hospitales por cada 1000 habitantes y visualización de los resultados.

- **Parte 5: Cálculo del Índice de Moran para el Indicador de Amenidades de Salud**  
  Evaluación de la autocorrelación espacial mediante el índice de Moran, utilizando diferentes matrices de pesos espaciales.

- **Parte 6: Actividad Opcional, Análisis de Buffers y Reflexión sobre los Límites de OpenStreetMap**  
  Análisis de accesibilidad mediante buffers alrededor de un punto de interés y reflexión sobre las limitaciones de los datos.

## Requisitos

- **Librerías R**:  
  - `osmdata`
  - `sf`
  - `tidyverse`
  - `readxl`
  - `spdep`
  - `lattice`
  - `httr2`

- **Datos**:  
  - Geodatabase Nacional 2021
  - Estructura Poblacional (INEC)
  - Codificación de parroquias (DPA)

## Instrucciones

1. **Carga de Librerías y Datos**  
   Ejecutar las librerías necesarias y cargar los datos de la geodatabase y el censo poblacional.

2. **Definición de la Zona de Interés**  
   Definir la zona de Latacunga y obtener los puntos de hospitales desde OpenStreetMap.

3. **Procesamiento de Datos Censales**  
   Filtrar y unir los datos de población y zonificación censal.

4. **Análisis Espacial y Visualización**  
   Crear mapas de distribución de hospitales y densidad poblacional, calcular el índice de Moran y realizar análisis de accesibilidad mediante buffers.

## Resultados

- **Distribución Espacial de Hospitales**  
  Mapa de distribución de hospitales en la provincia de Cotopaxi.

- **Densidad Poblacional**  
  Mapa de densidad poblacional por parroquias en Cotopaxi.

- **Indicador de Amenidades por Habitante**  
  Visualización del número de hospitales por cada 1000 habitantes.

- **Análisis de Autocorrelación Espacial**  
  Resultados del índice de Moran para evaluar la concentración espacial de hospitales.

## Reflexiones y Limitaciones

El análisis revela que la distribución de hospitales en Latacunga no es aleatoria y está influenciada por patrones espaciales específicos. Se destaca la importancia de considerar la proximidad y accesibilidad en la planificación de infraestructuras de salud.

## Contribuciones

Este proyecto fue desarrollado por **Guillermo Feijó** como parte de un taller de análisis espacial en Ecuador. Se agradece la colaboración de todos los participantes y las fuentes de datos públicas utilizadas.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
