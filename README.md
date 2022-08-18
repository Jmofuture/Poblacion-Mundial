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

## En el modelo de datos se generan las siguientes relaciones:

![Modelo](https://user-images.githubusercontent.com/78714438/183323234-96476e3c-1479-4464-a92a-c42ee2ff55c1.png)

## Informe Población Mundial

<ol>
<li>Un Treemap con la cantidad de habitantes por país</li>
<li>Una Matriz donde podemos ver el detalle de habitantes por continente y país</li>
<li>Un Mapa donde se puede observar la distribución de países por continente, las burbujas están condicionas al tamaño de la población de cada país </li>
</ol>

Adicional al filtro segmentado la cantidad de habitantes se agregó uno por continente

![Poblacion Mundial](https://user-images.githubusercontent.com/78714438/183322235-d212e2d8-85f7-4f64-9fc0-37b3dcd3756a.png)


En Power Query se genera una columna condicional para segmentar los países en 4 categorías:

<li>0 - 1M</li>
<li>1M - 10M</li>
<li>10M - 100M</li>
<li>100M ></li>

Con esta segmetación se agrega un filtro


![PQ Cantidad Poblacion](https://user-images.githubusercontent.com/78714438/183322924-37b7b62c-4c2e-45bc-93d7-7e98eb1ff84a.png)


## Informe Mortalidad Infantil y Esperanza de Vida

<ol>
<li>Una Matriz donde podemos ver el detalle de habitantes por continente y país, promedio de Esperenza de Vida y promedio de Mortalidad Infantil</li>
<li>Gráfico de dispersión, estudiando la relación entre la esperanza de vida y la mortalidad infantil</li>
<li>Un Mapa donde se puede observar la distribución de países por continente, las burbujas están condicionas al tamaño de la Mortalidad Infantil</li>
</ol>

![Mortalidad](https://user-images.githubusercontent.com/78714438/183323901-c8d1445b-70a7-4f77-a55b-c5fa9c3c2e59.png)

En Power Query se genera una columna condicional en cada tabla para segmentar:

#### Mortalidad Infantil

<li>0 a 10</li>
<li>10 a 25</li>
<li>25 0 50</li>
<li>50 ></li>


![PQ Mortalidad](https://user-images.githubusercontent.com/78714438/183324096-59351366-7bb9-4727-8f09-4306672c1857.png)


#### Esperanza de Vida

<li>0 a 60</li>
<li>60 a 70</li>
<li>70 a 80</li>
<li>80 ></li>


![Esperanza de vida promedio](https://user-images.githubusercontent.com/78714438/183324178-fb946ad3-c66e-4f9d-81be-d1b5eb7fe4b0.png)


Estos dos segmetaciones se usan como filtro sumadas a los dos anteriores.

#### Algunas conclusiones que se pueden sacar de este informe

<li>A menor esperanza de vida mayor es la mortalidad infantil, siendo el continente africano el más afectado por esta tendencia.</li>

<li>Angola representa el país más afectado ya que su esperanza de vida promedio es de 56 años y una mortalidad infantil de 191 por cada 1000 decesos.</li>

<li>El país menos afectado en Mónaco perteneciente al continente Europeo con una esperanza de vida promedio de 89 años y una mortalidad infantil de 5 por cada 1000 decesos.</li>
