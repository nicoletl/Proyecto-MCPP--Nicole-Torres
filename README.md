# Proyecto-MCPP-

## Análisis del sector de comercio al por menor en Colombia 2019-2023
Considerando el contexto de desaceleración económica experimentado en 2023, como resultado de la transformación económica y social luego de atravesar por dos periodos de reactividación y crecimiento economico en 2021 y 2022, se propone llevar a cabo un análisis del sector de comercio al por menor en el país.

En este readme se encuentra la descripcion de los resultados obtenidos atraves del analisis exploratorio de la EMC minorista. En el notebook encontrarán el paso a paso para obtener cada resultado.

## Motivacion:
La actividad de comercio, transporte y alojamiento tiene una participación del 20,1% en el valor agregado para el año 2022, siendo la actividad que mayor peso tiene seguido de la industria con el 13,4%; y dentro de esta actividad el sector de comercio al por mayor y menor tiene un peso de 49,2%. Para el III trimestre de 2023, el comercio fue una de las actividades económicas que más contribuyó al decrecimiento de -0,1% en el valor agregado, aportando -0,7p.p con una variación de -3,5% según los resultados publicados por el DANE.

A partir de allí, surge la necesidad de realizar un analisis de la actividad de comercio a partir de la encuesta mensual de comercio minorista que realiza el DANE y que es insumo para calcular el valor agregado de la actividad. Se toma la encuesta a nivel de microdato que se puede obtener en la mesa DANE de la Universidad del Rosario. 

## Fuente de información:
Se toma la Encuesta Mensual de Comercio (EMC) minorista desarrollada por el DANE, la cual proporciona los principales indicadores sobre la evolución de la actividad comercial del país, por medio de resultados del comercio al por menor y de vehículos, al generar información sobre variables como ventas, personal ocupado y sueldos y salarios de empresas de comercio al por menor dedicadas a la "reventa" (venta sin transformación) de mercancías o productos, que se encuentran en el territorio nacional.

## Caracteristicas:

* La encuesta tiene cobertura a nivel nacional y a nivel regional mide los departamentos de Antioquia, Atlántico, Bogotá, Cundinamarca, Santander, Valle del Cauca. Existe además un dominio residual correspondiente a "otros departamentos".
* A nivel de microdato recoge la información de 400 variables para 2301 empresas. 
* La EMC viene del periodo de enero de 2019 a septiembre de 2023, y para objeto de analisis se toma la información de las variables que recogen las ventas reales por linea de mercancia a nivel nacional, así como de las ventas reales por actividad económica para realizar el analisis regional, y el personal ocupado por departamentos.
* A raíz de la magnitud de la información que recoge la encuesta se hace mas eficiente realizar su analisis en python

## Contexto

## ¿cómo han sido los últimos años en terminos de consumo en Colombia?

A continuación se observa la evolución del consumo de los hogares en los últimos años, considernado que este tipo de consumo está directamente relacionado con el comercio minorista. 

Se destaca que 2019 fue un año de cotidianidad, luego, en 2020, nos enfrentamos a la incertidumbre con la llegada de la pandemia. El año 2021 marcó un periodo de reactivación, con un aumento en la compra de bienes durables y semidurables, y el regreso gradual a la presencialidad con la disminución de restricciones. Durante 2022, observamos un crecimiento significativo, impulsado por la completa normalización de la presencialidad y la tendencia de los hogares a participar en eventos y adquirir bienes y servicios fue notable. Sin embargo, al llegar a 2023, nos encontramos en un momento de ajuste, pues el consumo de bienes ha disminuido debido al impacto negativo del aumento de la inflación, que alcanzó máximos del 12% - 13% anual, y al incremento de las tasas de interés. Estos factores han desincentivado el consumo y se reflejan en la contracción de la actividad de comercio en este año.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/4879840d-94d6-4357-8ecb-e352977df5b3)

## Comportamiento del valor agregado de la actividad de comercio

En linea con lo anterior, con el fin de comprender como se ha comportado la actividad, a continuación tenemos el comportamiento de las series desestacionalizadas del valor agregado del sector de comercio al por mayor y menor, el total de comercio, transporte y alojamiento, y del PIB publicadas por el DANE, con el fin de entrar en contexto frente a cómo se ha comportado el sector en los ultimos años.

En primer lugar se observa el comportamiento en terminos de variaciones anuales, donde se resalta el decrecimiento del comercio que se empezó a observar finalizando el 2022.
![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/7c814b83-86f5-4b42-a31e-170380b2636f)

Por otro lado, vale la pena observar el comportamiento de las series transformadas en índices base 2019. Cabe destacar que, al utilizar un índice base, se elimina la magnitud absoluta de las cifras y se resalta la variación porcentual con respecto a un período específico (en este caso, 2019 dado que fue el periodo posterior a la pandemia). Un valor de menor a 100 indica una reducción de la actividad, mientras que un valor superior a 100 indicaría un aumento en comparación con el nivel observado en 2019, se transforma la serie en año base con el fin de obtener una mejor comparación. 

En este sentido, se observa que incluso desde 2022 la actividad no ha logrado superar significativamente los resultados de 2019, sin embargo, aún no muestra una tendencia negativa. 

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/f76ca8d6-99f5-42cc-b0ca-92dd5b5a8e76)

En adelante, vamos a seguir viendo series transformadas en indice base 2019

## Análisis encuesta mensual de comercio minorista (EMC)

A continuación, se muestra el primer ejercicio realizado con la EMC en donde se calcula la serie de ventas reales minoristas trimestralemente de 2019 a 2022. 

Respecto a 2023 se observa una disminución en la magnitud del índice, si bien se mantiene superior a 100, se registra una disminución significativa respecto a los indices de 2022, mostrando un estancamiento de las evtnas sin señales de recuperar la magnitud de 2022. 

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/73ce38b6-43cd-4aac-b303-e55781eaac3a)

Para observar a que se debe ese comportamiento, a continuación se observa un mapa de calor que muestra el comportamiento historico en terminos de variaciones anuales de las 19 lineas de mercancia que calcula la EMC, las lineas de mercancia corresponden a la agrupación de productos que define la encuesta. 

En el grafico, los colores claros indican decrecimiento y los azules crecimientos altos. Se puede observar las fases del consumo mencionadas anteriormente: la caída en 2020 de la mayoria de lineas, luego en 2021 y 2022 varias que reflejan crecimientos muy positivos, y finalmente en 2023 se empezó a ver el proceso de ajuste con crecimientos más moderados.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/49e0f082-4561-40ff-aa1d-fb6eeee88f6b)

Debido a la cantidad de lineas, solo nos concentraremos en las 10 que tienen la mayor participación sobre el total de ventas reales
![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/d2adf42d-30bf-4866-90ee-9d41d716d7e8)

A continuación, nuevamente tenemos el heatmap pero con las linas de mercancia con mayor participación, al analizar el grafico se logra determinar:

1. 2021 fue un año de crecimientos muy altos, pues se encuentran variaciones superiores a 40% a 100% en el ciertas lineas, sin emabrgo, se debe considerar que dichos crecimientos están influenciados por el efecto base de 2020, hablar de efecto base hace referencia a que nos estamos comparando con una base muy baja en el segundo trimestre de 2020.
   
2. Sin embargo el crecimiento de 2021 y 2022 estuvo influenciado positivamente por medidas del Gobierno que tenian el objetivo de incentivar el consumo. Entre esas la política del día sin IVA buscaba impulsar la reactivación económica y en definitiva tuvo efecto positivo en el incremento de las ventas de los bienes cobijados por estas politicas. En particular, según Fenalco los comerciantes argumentaron que esto les permitió dinamizar sus ventas, rotar y liquidar sus inventarios. Esta medida se celebró en tres días durante el cuarto trimestre de 2021 y en marzo y junio de 2022. Aunque inicialmente la política de días sin IVA recibió críticas, ya que se percibía que beneficiaba solamente a hogares de ingresos altos que son quienes podían tomar la desicion de posponer sus compras para acceder al beneficio y quienes tienen la mayor probabilidad de acceder a credito, su eliminación durante el gobierno de Petro también generó controversias. Fenalco, el gremio de comerciantes, expresó fuertes críticas, especialmente porque se canceló la jornada de diciembre de 2022. Esto dejó a muchos comerciantes con niveles de inventario elevados, ya que se esperaba que las ventas durante ese día estuvieran entre $12 billones y $14 billones. La decisión del gobierno afectó significativamente las expectativas y estrategias de los comerciantes.
   
3. Vale la pena destacar el comportamiento historico de las ventas reales de algunas linea de mercancia:

* Alimentos: Al observar los resultados de 2023, esta es una de las lineas que mas ha explicado el decrecimiento de las ventas totales dada su importante participación. Esta linea empezó a mostrar una menor dinámica finalizando el 2022 cuando empezaron a crecer los precios de los alimentos, cabe destacar que la inflación de alimentos llegó a estar en 27% en abril y mayo de 2023, factor que ha representado un desincentivo en su comercialización, si bien los decrecimientos en 2023 son cercanos a cero, esto indica que los hogares han optado por no consumir algunos alimentos o trasladarse a los de menor precio, pues a pesar de que el IPC de alimentos ya va en el orden del 12%, continua siendo un precio alto que perjudica la comercialización de estos bienes.

* Combustibles: En donde hemos visto una coyuntura marcada por el aumento de precios en la gasolina que ha hecho el Gobierno para contener el déficit del Fepc, este incremento empezó en octubre de 2022 y ha continuado durante todo el 2023. De enero a septiembre dde 2023 el combustible ha subido 3.700 pesos, desde un precio promedio de $10.253 en enero. Entonces nuevamente se observa el impacto de los precios en las ventas reales.

* Vehículos: los vehículos han sido una de las lineas mas afectadas en el año, considerando que en 2022 se tenía una mayor demanda. En 2023 el decrecimiento es atribuido principalmente al encarecimiento del crédito por las altas tasas de interés han desincentivado a los hogares en la compra de estos bienes, y recientemente también hay algunos gremios que mencionan que hay un impacto negativo por las alzas en los precios de los combustibles.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/47fb565a-63a7-418c-bc0f-b077886d04bb)

## Análisís regional:

La encuesta también hace una medicion a nivel regional, aunque con ciertas limitaciones. En el grafico se observa la participación por departamento en las ventas reales totales a nivel nacional, donde se destaca la participación de Bogotá, Antioquia y Valle del Cauca y una agrupación adicional que se denomina "otros departamentos" que reune las ventas de los departamentos restantes.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/aeb581d4-f3f3-4314-8e78-5c4048a02f70)

Para analizar los resultados por departamento, se obtiene el total de ventas reales desde los meses de enero a septiembre de cada año, considerando que la EMC utilizada esta disponible hasta septiembre de 2023. De esta forma, se obtiene un grafico de barras que consolida los resultados de las ventas trasnformadas en indice base 2019 para cada año. 

Se logra ver el crecimiento de las ventas a lo largo del periodo 2020 a 2022 para todos los departamentos, sin embargo, en 2023 se estanca ese crecimiento, y si bien continuamos con ventas superiores a las de 2021, es clara la disminución significativa respecto a las ventas de 2022. 

Al observar el comportamiento por departamentos, llama la atención que durante todo el periodo el departamento de Cundinamarca logra superar las ventas año a año respecto a los demás departamentos.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/898ec5a3-e6ed-412c-b163-b5860a2e7bdf)

Al analizar a que se deben dichos resultados en Cundinamarca, a continuación podemos ver cuales son las actividades comerciales que mayores ventas presentan. 

Cabe aclarar que para el caso de los departamentos no se cuenta con lineas de mercancia como a nivel nacional, sino con una desagregación por actividad comercial. En el siguiente grafico se refleja la desagregación para los trimestres de 2022 y 2023, en donde sobresalen las ventas de prendas de vestir y calzado, repuestos, y artículos culturales, lo que demuestra que Cundinamarca es intensivo en estos bienes. En el código realizado se podra ver a nivel de fuente cuales son las empresas que se destacan en estas actividades. 

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/352c13c7-0a08-4e7d-815f-3db91a5d0560)

Al realizar el mismo ejercio para Bogotá, se observa un cambio de comportamiento. Podemos ver que contrario a Cundinamarca Bogotá es más especialziada en la comercialización de bienes como equipo de informática, y vehículos sobre todo en el 2022.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/078f8d0b-0bd6-4ebd-b617-3ce5ae7d051d)

## Comportamiento del empleo 2019-2022 por departamento

Finalmente, se busca ver graficamente cómo se ha comportado el personal ocupado que recoge la encuesta por departamentos.

* Se destaca Bogotá, Antioquia y Valle del Cauca como los departamentos más intensivos en contratación en el sector, dejando a Cundinamarca y Santander con el nivel mas bajo. 
* En términos generales, para el 2023 se observa una estabilización del empleo en todos los departamentos, no se observa una tendencia decreciente a pesar del bajo crecimiento que mostraba el total de ventas minoristas. 
* Llama la atención el comportamiento de Atlántico, que venia registrando un crecimiento sostenido en 2022 y en 2023 se estabiliza.
* En 2023 solanente Santander es quien muestra tendencia positiva en el personal ocupado.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/5b624066-8058-4d0f-9b6c-f8251abfdb63)
![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/125eecd5-1750-4263-8b01-18dd3268d194)

 ## ¿Qué se espera del comercio para 2024?

El análisis realizado permitió ver cómo el comercio minorista en 2023 se ha visto afectado por la coyunyura economica marcada por la inflación, en la medida en que varias lineas de mercancia presentan decrecimiento en sus ventas reales, comportamiento atribuido a los precios altos y al alza en las tasas de interés que desincentiva la adquisición de estos bienes, y por el contrario, la tendencia de los hoagres esta orientada a adquirir solamente bienes básicos como los productos de aseo personal que sí han mostrado crecimiento en 2023. 

En el futuro, se anticipa que el comercio continuará enfrentando desafíos debido a la difícil situación económica. La presión sobre el presupuesto de los hogares, combinada con la disminución de la capacidad de consumo, contribuirá a este escenario. La ausencia de incentivos, como la política del Día sin IVA, también podría impactar negativamente en el sector. 

La persistencia de la inflación y las tasas de interés elevadas son factores adicionales que podrían prolongar la debilidad en el comercio. Es necesario estar atentos a estos elementos que influyen en el entorno económico.

