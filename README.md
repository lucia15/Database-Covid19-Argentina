# Datos-Covid19-Argentina

Los datos presentes en esta base de datos se basan principalmente en los 
informes diarios, matutinos y vespertinos, que emite el gobierno nacional.
Puede consultar los mismos en:

https://www.argentina.gob.ar/coronavirus/informe-diario

Se actualiza diariamente con cada nuevo informe publicado.

La base de datos está compuesta de los siguientes archivos:

+ **Argentina-covid19.csv**
+ **Argentina-covid19-por-provincia.csv**
+ **Argentina-covid19-muertes.csv**

El primer data set, Argentina-covid19.csv, contiene las siguientes variables:

+ *fecha*: Fecha de los datos reportados
+ *casos_nuevos*: Casos nuevos del día
+ *casos_total*: Total de casos hasta el momento	
+ *%mujer*:	Porcentaje de mujeres del total de casos hasta el momento
+ *%varon*:	Porcentaje de varones del total de casos hasta el momento
+ *mujer_total*: Número de mujeres infectadas del total de infectados hasta el momento
+ *varon_total*: Número de varones infectados del total de infectados hasta el momento
+ *franja_etaria*: Principales franjas etarias afectadas de los casos registrados
+ *edad_prom*: Promedio de las mismas
+ *importados_total*: Cantidad de casos que son importados del total de casos
+ *importados_nuevos*: Cantidad de casos que son importados de los casos nuevos del día	
+ *local_total*: Total de contagiados que son contactos estrechos de casos confirmados
+ *local_nuevos*: Contagiados que son contactos estrechos de casos confirmados del día
+ *en_investigacion_total*:	Cantidad de casos que se encuentra en investigación epidemiológica
+ *en_investigacion_nuevos*: Casos que se encuentra en investigación epidemiológica del día
+ *comunitario_total*: Cantidad de contagios comunitarios del total de casos
+ *muertes_total*: Cantidad de fallecidos hasta el momento
+ *muertes_nuevos*:	Cantidad de fallecidos del día
+ *alta_total*:	Cantidad de casos que fueron dados de alta (recuperados) hasta el momento
+ *alta_definitiva*: Cantidad de altas que son definitivas
+ *descartados_nuevos*:	Cantidad de casos sospechosos descartados en el día
+ *descartados_total*: Cantidad de casos sospechosos descartados hasta el momento
+ *tests_realizados_nuevos*: Cantidad de tests realizados en el día
+ *tests_realizados_total*:	Cantidad de tests realizados hasta el momento
+ *test_por_millon_hab*: Cantidad de tests realizados por millón de habitantes
+ *observaciones*: Información relevante del día de la fecha

El archivo Argentina-covid19-por-provincia.csv contiene información 
sobre las 23 provincias Argentinas y de la Ciudad Autónoma de Buenos Aires (CABA),
sus variables son:

+ *fecha*: Fecha de los datos reportados
+ *provincia*: Provincia en la que se registran los casos
+ *casos_total*: Total de casos hasta el momento en la provincia
+ *casos_nuevos*: Casos nuevos del día en la provincia
+ *muertes_total*: Cantidad de fallecidos hasta el momento en la Provincia
+ *muertes_nuevos*:	Cantidad de fallecidos del día en la Provincia
+ *importados_nuevos*: Cantidad de casos que son importados de los casos nuevos del día
+ *importados_total*: Cantidad de casos que son importados del total de casos
+ *local_nuevos*: Contagiados que son contactos estrechos de casos confirmados del día
+ *observaciones*: Información relevante sobre la situación en la provincia al día de la fecha 

En Argentina-covid19-muertes.csv, tenemos un registro por cada fallecido por Coronavirus en el país.
Las variables consideradas son:

+ *fecha*: Día del deceso 
+ *provincia*: Provincia de residencia del fallecido	
+ *genero*:	Identidad de género del/a fallecido/a
+ *edad*: Edad del fallecido	
+ *tipo_caso*: Caso importado, local/conglomerado (contacto estrecho de un importado) o de contagio comunitario
+ *viajes_o_relacion_con_el_exterior*: Información sobre viajes al exterior 
del fallecido o sus allegados (en caso de tratarse de un caso local) y otras observaciones de interés
+ *comorbilidad_observaciones*: comorbilidades y otras observaciones de interés

________________________________________________________________________________

Con esta base de datos (y posiblemente con datos internacionales agregados de alguna otra),
nos proponemos trabajar las 5 tareas descriptas a continuación.

# Práctico 1: Análisis y Visualización

### Objetivos: 
Uso de estadísticas descriptivas para el análisis del set de datos. 
Responder a distintas preguntas generales respecto al dataset, por ejemplo:

+ Cantidad de infectados (nuevos y totales, recuperados, fallecidos) por región (país o provincia) por día
+ Proporción de casos importados, locales y comunitarios en Argentina
+ Cantidad de testeos cada 100 mil habitantes, proporción positivos/negativos, negativos acumulados
+ Diferencia entre las distintas provincias en el caso de Argentina

Determinar la tasa de ocurrencia de algún fenómeno, por ejemplo:

+ Tasas de contagio, testeo, mortalidad, hospitalización, recuperación
+ Tasa de mortalidad por país y por provincia (Argentina)

Señalar si existe correlación entre dos o más variables, por ejemplo:
+ Entre mortalidad y distintas comorbilidades

Estudiar la distribución de alguna variable de interés, por ejemplo:
+ Distribución etaria de los infectados y fallecidos
+ Clasificación por género y posibles diferencias del impacto del virus en cada uno

# Práctico 2: Análisis y Curación

### Objetivos: 

Procesar el conjunto de datos para poder utilizarlos en el análisis exploratorio de los mismos. Tener en cuenta:

+ Datos faltantes, datos nulos, ¿los eliminamos? ¿nos dicen algo? ¿podemos completarlos?
+ Consistencia de los datos, ¿existe información contradictoria?
+ Outliers, ¿tenemos?, ¿cómo los tratamos?

# Práctico 3: Introducción al Machine Learning

### Objetivos:
En este práctico utilizaremos algunos algoritmos básicos de aprendizaje automático para intentar encontrar patrones en los datos, y evaluaremos los resultados usando métricas estándares para cada tipo de problema.

El objetivo del práctico es que pensemos en las distintas formas que puede tomar el modelado de un problema con datos, y en el trabajo de selección de features que debe realizarse para poder abordarlo.

Para ello intentaremos responder la siguiente pregunta:

¿Es posible predecir la cantidad de infectados que tendrá una región (país o provincia) en base a los datos que se 
encuentran presentes en este dataset?

Tener en cuenta los siguientes lineamientos: 

+ Deben decidir a partir de qué valor de una métrica determinada consideran aceptable el resultado. Esto lo tienen que hacer antes de empezar a entrenar un modelo.
+ Deberán trabajar con el problema de dos maneras diferentes: como un problema de regresión, y como un problema de clasificación.
+ A la hora de hacer selección de variables, tengan en cuenta que los modelos de Machine Learning solo reciben inputs numéricos.
+ Es importante que almacenen los resultados de alguna manera para poder comparar los distintos modelos. Recomendación: crear una función para almacenar resultados en un dataframe de pandas e imprimirlos en pantalla

# Práctico 4: Aprendizaje Supervisado

### Objetivos:

Profundizar el trabajo realizado en el práctico anterior. Intentaremos mejorar los resultados iterando sobre la ingeniería de atributos, el modelado, y el análisis de la salida de los modelos.

# Práctico 5: Aprendizaje No Supervisado

### Objetivos:
Realizar un k-means clustering para clasificar los países (o regiones) según alguna(s) variable(s) de interés.



________________________________________________________________________________

# Licencia

Esta base de datos se libera bajo una licencia Creative Commons Reconocimiento
4.0 Internacional (CC BY 4.0).

Usted es libre de:

+ *Compartir* - copiar y redistribuir el material en cualquier medio o formato.
+ *Adaptar* - remezclar, transformar y crear a partir del material para
  cualquier finalidad, incluso comercial.

Siempre y cuando reconozca adecuadamente la autoría, proporcione un enlace a la
licencia e indique si se han realizado cambios. Puede hacerlo de cualquier
manera razonable, pero no de una manera que sugiera que tiene el apoyo del
licenciador o lo recibe por el uso que hace.

Para más información lea la licencia.
