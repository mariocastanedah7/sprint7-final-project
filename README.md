# sprint7-final-project Análisis de datos de ConnectaTel

**1. Objetivo del proyecto**
Analizar el comportamiento de los clientes de ConnectaTel en México y
Colombia durante 2024, a partir de sus registros de llamadas y mensajes.

El análisis busca identificar patrones de consumo, diferencias entre
segmentos de clientes, valores atípicos y oportunidades para mejorar los
planes comerciales, fortalecer la retención y adaptar la oferta a las
necesidades de los usuarios.

**2. Datasets utilizados**
El proyecto utiliza tres archivos CSV:
  
1. plans.csv             
  Catálogo de planes de  ConnectaTel  
  Nombre del plan, minutos, mensajes y GB incluidos, precio mensual y tarifas por consumo adicional.
                           

2. users_latam.csv       
  Información de los clientes.     
  Identificador, edad, ciudad, fecha de registro, plan contratado y fecha de cancelación, cuando existe.
                                       

3. usage.csv        
   Registros de actividad de los clientes.        
   Identificador del evento y del usuario, tipo de actividad (llamada o mensaje), fecha, duración y longitud.

Los archivos se cargan en el notebook mediante pandas. En el entorno
original del proyecto se encuentran en la carpeta /datasets/.

**3. Etapas del análisis realizadas**

Paso	/ Acción	/ Resultado para el negocio

1. Cargar y explorar	/ Cargar y explorar plans, users_latam, usage.	/ Visión clara de la estructura y tipos de columna de cada dataset.
2. Identificación de problemas de calidad	/ Contar nulos, detectar sentinels, revisar fechas fuera de rango.	/ Lista priorizada de problemas que pueden sesgar decisiones.
3. Limpieza básica /	Reemplazar sentinels, convertir fechas, imputar o marcar NA según reglas. /	Datos consistentes y listos para análisis estadístico.
4. Summary statistics /	Revisar las medidas clave en variables categóricas y numéricas.	/ Medidas clave (media, mediana, percentiles) que muestran el comportamiento típico y extremo
5. Visualización & outliers	/ Creación de histogramas y boxplots. /	Visualización de sesgos, patrones de usuarios o datos atípicos.
6. Segmentación	/ Crear segmentaciones basadas en reglas claras; visualizar proporciones con countplots.	/ Segmentos accionables que permiten diseñar ofertas, campañas y migraciones de plan.
7. Insight ejecutivo	/ Redactar conclusiones y recomendaciones comerciales basadas en los pasos anteriores.	/ Responder a las preguntas del negocio y proponer acciones concretas.
8. Publicación /	Subir tu notebook + README a GitHub.	/ Entrega reproducible para revisión y ejecución por stakeholders.

El análisis de actividad utiliza la columna date de usage.csv como 
referencia temporal para el periodo 2024. La fecha de registro del
cliente (reg_date) se conserva como información complementaria.

**4. Requisitos y ejecución del notebook**    

Abrirlo en Google Colab

Para reproducir los resultados:
- Utiliza los archivos CSV originales del proyecto.
- Ejecuta las celdas secuencialmente para que las transformaciones se
  apliquen antes de las agregaciones y visualizaciones.
- Verifica que las rutas de los archivos correspondan a tu entorno.
- No omitas las celdas de limpieza: las etapas posteriores utilizan
  las columnas ya preparadas.
- Si cambias los datos o los criterios de segmentación, vuelve a
  ejecutar el notebook completo para actualizar tablas, gráficos y
  conclusiones.
