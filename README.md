# Análisis de la Población Mundial, Mortalidad Infantil y Esperanza de Vida

Proyecto del curso ofrecido por Datdata en Udemy - [Curso Power BI Análisis de Datos y Business Intelligence](https://www.udemy.com/course/power-bi-analisis-datos-business-intelligence/)

En él informe primer Población Mundial, se cargan 3 archivos .xlsx

<li><strong>Population</strong>, contiene un listado de países y cantidad de habitantes.</li>
<li><strong>Countries</strong>, contiene listado de países, código del país y su respectivo continente.</li>
<li><strong>Países</strong>, es el símil de <strong>Countries</strong> pero en español.</li>

Al querer trabajar los datos en idioma español, se ocultan todos los datos que no se van a utilizar, en este caso la tabla <strong>Countries</strong> y la columna <strong>Country</strong> de la tabla <strong>Population</strong>.

En el segundo Mortalidad y Esperanza de Vida, se cargan 2 archivos .xlsx adicionales

<li><strong>Infant+death+rate</strong>, contiene un listado de países y el promedio de muertes infantiles por cada 1000 decesos.</li>
<li><strong>Life+expectancy</strong>, contiene un listado de países y el promedio de esperanza de vida.</li>


## Informa Población Mundial


![Poblacion Mundial](https://user-images.githubusercontent.com/78714438/183322235-d212e2d8-85f7-4f64-9fc0-37b3dcd3756a.png)


En Power Query se genera una columna condicional para segmentar los países en 4 categorías:

<li>0 - 1M</li>
<li>1M - 10M</li>
<li>10M - 100M</li>
<li>100M ></li>

Con esta segmetación se agrega un filtro


![PQ Cantidad Poblacion](https://user-images.githubusercontent.com/78714438/183322924-37b7b62c-4c2e-45bc-93d7-7e98eb1ff84a.png)



