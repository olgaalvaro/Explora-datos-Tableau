# Explora-datos-Tableau
Exploracion y Visualizacion de Datos (Tableau)

## Data Visualization (Tableau)

Instrucciones para cargar los datos del fichero csv airbnb-listings reducido almacenasdo en Storage de Google a un Cloud SQL y posteriormente leerlo en Tableau siguiendo las indicaciones dadas.

https://colab.research.google.com/drive/1dQVwLQ-_Uh6Afp-udWDcXRoilBONB6u9


### Dashboard airbnb Madrid

El libro de trabajo empaquetado practica_datavisualization.twbx se puede descargar por dos vías:

- Github en la carpeta PracticaTableau
- Google Drive
https://drive.google.com/file/d/14S1gVUKC4QgZpuzxHgBqscc68mPbeGTr/view?usp=sharing

Muestra por defecto el Top 12 de los barrios de Madrid con mayor promedio del precio total.  
Consta de la siguiente información definida en las hojas de trabajo:

1. POLÍTICA DE CANCELACIÓN POR BARRIOS
2. MAPA CON LOS BARRIOS 
3. Nº TOTAL DE VIVIENDAS AGRUPADAS POR HABITACIONES Y BAÑOS
4. ANILLO CON EL TOTAL DE VIVIENDAS EN DICHOS BARRIOS
5. RELACIÓN JERARQUÍA TIPO DE ALOJAMIENTO Y POLÍTICA DE CANCELACIÓN
6. PORCENTAJE TOTAL DEL PRECIO TOTAL VS FIANZA CALCULADO ENTRE 2011-2015 TRIMESTRAL
7. TENDENCIA DE ADQUISICIÓN DE NUEVAS VIVIENDAS DESDE 2011 HASTA 2017

Si el valor del Top se modifica se recalcula la información en todas las vistas (definida una acción con el cambio del valor de dicho parámetro Top N).  
La vista 1 POLÍTICA DE CANCELACIÓN POR BARRIOS actua de origen, de tal manera que si se selecciona algún barrio en concreto o alguna política de cancelación, igualmente la información se recalcula en el resto de las vistas (definido una acción como filtro).

Teniendo en cuenta:

- PRECIO TOTAL = [Price]+ ([Cleaning Fee]/365) 
- BATHROOMS (agrupación)  (vista 3)
- BEDROOMS (agrupación)  (vista 3)
- JERARQUIA TIPO ALOJAMIENTO (Property type (grupo), Room Type A, Bed Type)  (vista 5)
- Property type (grupo) define el grupo Other Agr.   
- Room Type A es campo calculado.
- PROMEDIO POR PANEL DEL PROMEDIO DEL PRECIO (vista 5)
- CALCULO DE TABLAS RAPIDO (PORCENTAJE DEL TOTAL) (vista 6)
- LÍNEAS DE TENDENCIA (vista 7) con R.Cuadrado muy próximo a 1

El nº de vistas utilizado en el dashboard excede del máximo indicado, y puede que quede algo recargado pero he intentado contemplar los distintos gráficos vistos en el módulo.




