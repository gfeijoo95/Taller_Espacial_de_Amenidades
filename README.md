# Taller_Espacial_de_Amenidades
Taller Espacial de Amenidades de Salud en parroquias de Ecuador

Parte 1: Identificación y Reflexión sobre las Amenidades de Salud
1. Obtención de datos de hospitales de OpenStreetMap (OSM):

Para la identificación de amenidades de salud, se obtuvieron datos de hospitales usando la librería osmdata. Se definió una zona de interés en Ecuador, y se buscaron puntos de interés etiquetados como amenity=hospital. Estos datos fueron descargados y almacenados en un objeto sf.

2. Carga y filtrado de datos de sectores censales:

Se cargaron las capas de la geodatabase nacional para seleccionar las zonas censales de interés. Primero, se utilizó st_layers para listar todas las capas disponibles y luego se leyó la capa específica de zonas censales usando st_read. El enfoque principal fue en la capa zon_a que contiene 5888 features con geometría de tipo MULTIPOLYGON en el sistema de referencia WGS 84 / UTM zona 17S.

3. Visualización de los hospitales en un mapa:

Se generó un mapa para mostrar la ubicación de los hospitales extraídos de OSM dentro de la zona de estudio.

Parte 2: Unión de Polígonos de Zonas Censales a Nivel de Parroquias
1. Agrupación de datos por parroquia:

Dado que los datos estaban a nivel de zona censal, se unieron los polígonos para agruparlos a nivel de parroquias. Posteriormente, se unieron estos datos con la información demográfica obtenida previamente.

2. Mapas de calor:

Se crearon mapas de calor para visualizar la distribución espacial de la población y las amenidades de salud.

Parte 3: Cálculo del Número Total de Amenidades
1. Conteo de hospitales en cada sector censal:

Los puntos de los hospitales fueron transformados al sistema de referencia de las zonas censales. A continuación, se utilizó st_join para realizar una unión espacial que permitiera contar el número de hospitales en cada sector censal. Esta información fue añadida a los datos de los sectores censales.

Parte 4: Cálculo del Ratio de Amenidades por Habitante
1. Cálculo del ratio:

Se calculó el ratio de amenidades de salud (hospitales) por cada 1000 habitantes en las parroquias, proporcionando una medida de accesibilidad a los servicios de salud.

Parte 5: Cálculo del Índice de Moran para el Indicador de Amenidades de Salud
1. Evaluación de la autocorrelación espacial:

Se utilizó el índice de Moran I para evaluar la autocorrelación espacial del indicador de amenidades de salud. El valor de Moran I obtenido fue 0.86, con un p-valor significativamente bajo, lo que indica una fuerte autocorrelación espacial.

Conclusión:

Existe una autocorrelación espacial significativa en la distribución de amenidades de salud por cada 1000 habitantes en Latacunga, lo que sugiere que estas amenidades están agrupadas en ciertas áreas. Este hallazgo tiene importantes implicaciones para las políticas de salud pública, sugiriendo que se deben implementar estrategias focalizadas para mejorar el acceso en zonas con menor cobertura.

2. Análisis con matriz de distancia inversa:

Se creó una matriz de pesos espaciales basada en la distancia inversa para analizar cómo varía el índice de Moran I al aplicar diferentes criterios de vecindad. Este análisis confirmó la existencia de agrupamientos espaciales en la distribución de amenidades de salud.
