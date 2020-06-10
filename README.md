# Datos-Covid19-Argentina

Los datos presentes en esta base de datos se basan principalmente en los 
informes diarios, matutinos y vespertinos, que emite el gobierno nacional, 
y se actualiza diariamente con cada nuevo informe publicado. 
Puede consultar los mismos en: 

https://www.argentina.gob.ar/coronavirus/informe-diario

La base de datos está compuesta de los siguientes archivos:

+ **Argentina-covid19.csv**
+ **Argentina-covid19-por-provincia.csv**
+ **Argentina-covid19-fallecidos.csv**

El primer dataset, Argentina-covid19.csv, contiene las siguientes variables:

+ *fecha*: Fecha de los datos reportados
+ *dia_cuarentena*: día de cuatentena desde la resolución del DNU 260
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
+ *comunitario_total*: Cantidad de contagios comunitarios del total de casos
+ *comunitario_nuevos*: Cantidad de casos que son de contagio comunitario de los casos nuevos del día	
+ *en_investigacion_total*:	Cantidad de casos que se encuentra en investigación epidemiológica
+ *en_investigacion_nuevos*: Casos que se encuentra en investigación epidemiológica del día
+ *muertes_total*: Cantidad de fallecidos hasta el momento
+ *muertes_nuevos*:	Cantidad de fallecidos del día
+ *alta_total*:	Cantidad de casos que fueron dados de alta (recuperados) hasta el momento
+ *alta_nuevos*: Cantidad de altas del día
+ *alta_definitiva*: Cantidad de altas que son definitivas
+ *descartados_total*: Cantidad de casos sospechosos descartados hasta el momento
+ *descartados_nuevos*:	Cantidad de casos sospechosos descartados en el día
+ *tests_realizados_total*:	Cantidad de tests realizados hasta el momento
+ *tests_realizados_nuevos*: Cantidad de tests realizados en el día
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
+ *observaciones*: Información relevante sobre la situación en la provincia al día de la fecha. 


En Argentina-covid19-fallecidos.csv, tenemos un registro por cada fallecido por Coronavirus en el país.
Las variables consideradas son:

+ *fecha*: Día del deceso 
+ *provincia*: Provincia de residencia del fallecido
+ *num_caso*: Contador de casos	
+ *genero*:	Identidad de género del/a fallecido/a
+ *edad*: Edad del fallecido	
+ *tipo_caso*: Caso importado, local/conglomerado (contacto estrecho de un importado) o de contagio comunitario
+ *comorbilidades*: comorbilidades y otras observaciones de interés
+ *viajes*: Información sobre viajes al exterior 
del fallecido o sus allegados (en caso de tratarse de un caso local)
+ *observaciones*: Otras observaciones de interés

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
