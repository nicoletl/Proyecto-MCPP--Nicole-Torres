# Proyecto-MCPP-
Considerando el contexto de desaceleración económica experimentado en 2023, como resultado de la transformación económica y social luego de atravesar por dos periodos de reactividación y crecimiento economico en 2021 y 2022, se propone llevar a cabo un análisis del sector de comercio al por menor en el país.

En este readme se encuentra la descripcion de los resultados obtenidos atraves del analisis exploratorio de la EMC minorista. En el notebook encontrarán el paso a paso para obtener cada resultado.

## Motivacion:
Considerando que la actividad de comercio, transporte y alojamiento tiene una participación del 20,1% en el valor agregado para el año 2022, siendo la actividad que mayor peso tiene seguido de la industria con el 13,4%, y dentro de esta actividad el sector de comercio al por mayor y menor tiene un peso de 49,2%, y según el DANE, para el III trimestre de 2023 fue uno de los sectores que mas contribuyó al decrecimiento de -0,1% en el valor agregado, aportando -0,7p.p con una variación de -3,5% . 

A partir de allí, se ve la necesidad de realizar un analisis de la actividad a partir de la encuesta mensual de comercio minorista que realiza el DANE, tomando la encuesta a nivel de microdato que se puede obtener en la mesa DANE de la Universidad del Rosario. 

## Fuente de información:
Se toma la Encuesta Mensual de Comercio (EMC) minorista desarrollada por el DANE, la cual proporciona los principales indicadores sobre la evolución de la actividad comercial del país, por medio de resultados del comercio al por menor y de vehículos, al generar información sobre variables como ventas, personal ocupado y sueldos y salarios de empresas de comercio al por menor dedicadas a la "reventa" (venta sin transformación) de mercancías o productos, que se encuentran en el territorio nacional.

## Caracteristicas:

*La encuesta tiene cobertura a nivel nacional y a nivel regional mide los departamentos de Antioquia, Atlántico, Bogotá, Cundinamarca, Santander, Valle del Cauca. Existe además un dominio residual correspondiente a "otros departamentos".
*A nivel de microdato recoge la información de 400 variables para 2301 empresas. 
*La EMC viene del periodo de enero de 2019 a septiembre de 2023, y para objeto de analisis se toma la información de las variables que recogen las ventas reales por linea de mercancia a nivel nacional, así como de las ventas reales por actividad económica para realizar el analisis regional, y el personal ocupado por departamentos.

## Contexto

## ¿cómo han sido los últimos tiempos en oferta y demanda en colombia?

A continuación se observa la evolución del consumo de los hogares en los últimos años, que está directamente relacionado con el comercio minorista. 

2019 fue un año de cotidianidad, luego, en 2020, nos enfrentamos a la incertidumbre con la llegada de la pandemia. El año 2021 marcó un periodo de reactivación, con un aumento en la compra de bienes durables y semidurables, y el regreso gradual a la presencialidad con la disminución de restricciones. Durante 2022, observamos un crecimiento significativo, impulsado por la completa normalización de la presencialidad y la tendencia de los hogares a participar en eventos y adquirir bienes y servicios fue notable. Sin embargo, al llegar a 2023, nos encontramos en un momento de ajuste, pues el consumo de bienes ha disminuido debido al impacto negativo del aumento de la inflación, que alcanzó máximos del 12% - 13% anual, y al incremento de las tasas de interés. Estos factores han desincentivado el consumo y se reflejan en la contracción de la actividad de comercio en este año.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/4879840d-94d6-4357-8ecb-e352977df5b3)

## Ventas reales minoristas totales

En linea con lo anterior, con el fin de entrar en contexto, a continuación tenemos el comportamiento del sector de comercio al por mayor y menor, el agregado de comercio, transporte y alojamiento y el PIB en su serie desestacionalizada, en variaciones anuales y la serie transformada en indice base 2019.

En terminos de variaciones anuales, se resalta el decrecimiento del comercio que se empezó a observar finalizando el 2022.
![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/8e56a0a6-1f64-45b4-b7ea-1de65078dcea)

Tambien vale la pena observar los resultados desestacionalizados, esta vez de las series transformadas en índices base 2019. Al utilizar un índice base, se elimina la magnitud absoluta de las cifras y se resalta la variación porcentual con respecto a un período específico (en este caso, 2019 dado que fue el periodo posterior a la pandemia). Un valor de menor a 100 indica una reducción de la actividad, mientras que un valor superior a 100 indicaría un aumento en comparación con el nivel observado en 2019. 

En este caso, se observa que incluso desde 2022 la actividad no ha logrado superar los resultados de 2019, sin embargo, aún no muestra tendencia negativa. 

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/93824a03-bcdb-43b4-a800-e4b17176f52f)

En adelante, vamos a seguir viendo series transformadas en indice base 2019

A continuación, se muestra el primer ejercicio realizado con la EMC en donde se calcula la serie de ventas reales minoristas. Respecto a 2023 se observa una disminución en la magnitud del índice si bien se mantiene superior a 100, se observa una disminución significativa respecto a los indices de 2022, mostrando un estancamiento sin señales de recuperar la magnitud de las ventas de 2022. 

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/117d5d35-66e9-4475-8895-f1a4ae7c4615)

Para observar a que se debe ese comportamiento, a continuación se observa un mapa de calor que indica el comportamiento historico en terminos de variaciones anuales de las 19 lineas de mercancia que calcula la EMC, las lineas de mercancia corresponden a la agrupación de productos que define la encuesta. En el grafico se puede observar las fases del consumo mensionadas anteriormente, en donde los colores claros indican decrecimiento y los azules crecimientos altos. Se observan tres momentos marcados por la caída en 2020 de la mayoria de lineas, luego en 2021 y 2022 varias que reflejan crecimientos muy positivos y finalmente en 2023 se empezó a ver el proceso de ajuste con crecimientos más moderados.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/2538f931-e67c-46a2-badb-7f287786fcf3)

Debido a la cantidad de lineas, solo nos concentraremos en las 10 que tienen la mayor participación
![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/5e854510-1734-4b43-b4d5-8aa01d4f64dc)

A continuación, nuevamente tenemos el heatmap pero con las linas de mercancia con mayor participación, al analizar el grafico se logra determinar:

1. 2021 fue un año de crecimientos muy altos se encuentran variaciones superiores a 40% a 100% en el ciertas lineas, sin emabrgo, se debe considerar que dichos crecimientos están influenciados por el efecto base de 2020, hablar de efecto base hace referencia a que nos estamos comparando con una base muy baja en el segundo trimestre de 2020.
   
2. Sin embargo el crecimiento de 2021 y 2022 estuvo influenciado positivamente por medidas del Gobierno que tenian el objetivo de incentivar el consumo. Entre esas la política del día sin IVA buscaba impulsar la reactivación económica y en definitiva si tuvo efecto positivo en el incremento de las ventas  de los bienes cobijados por estas politicas. En particular, según Fenalco los comerciantes argumentaron que esto les permitió dinamizar sus ventas, rotar y liquidar sus inventarios. Esta medida se celebró en tres días durante el cuarto trimestre de 2021 y en marzo y junio de 2022. Aunque inicialmente la política de días sin IVA recibió críticas, ya que se percibía que beneficiaba solamente a hogares de ingresos altos que son quienes podían tomar la desicion de posponer sus compras para acceder al beneficio y quienes tienen la mayor probabilidad de acceder a credito, su eliminación durante el gobierno de Petro también generó controversias. Fenalco, el gremio de comerciantes, expresó fuertes críticas, especialmente porque se canceló la jornada de diciembre de 2022. Esto dejó a muchos comerciantes con niveles de inventario elevados, ya que se esperaba que las ventas durante ese día estuvieran entre $12 billones y $14 billones. La decisión del gobierno afectó significativamente las expectativas y estrategias de los comerciantes.
   
3. Vale la pena destacar el comportamiento historico de las ventas reales de algunas linea de mercancia:

* Alimentos: Al observar los resultados de 2023, esta es una de las lineas que mas ha explicado el decrecimiento de las ventas totales dado su peso. Esta linea empezó a mostrar una menor dinámica finalizando el 2022 cuando empezaron a crecer los precios de los alimentos, cabe destacar que la inflación de alimentos llegó a estar en 27% en abril y mayo de 2023, factor que ha representado un desincentivo en su comercialización, si bien los decrecimientos en 2023 son cercanos a cero, esto indica que los hogares han optado por no consumir algunos alimentos o trasladarse a los de menor precio pues a pesar de que el IPC de alimentos ya va en el orden del 12%, continua siendo un precio alto.

* Combustibles: En donde hemos visto una coyuntura marcada por el aumento de precios en la gasolina que ha hecho el Gobierno para contener el déficit del Fepc, este incremento empezó en octubre de 2022 y ha continuado durante todo el 2023. De enero a septiembre el combustible ha subido 3.700 pesos, desde un precio promedio de $10.253 en enero. Entonces nuevamente se observa el impacto de los precios en las ventas reales.

* Vehículos: los vehículos han sido una de las lineas mas afectadas en el año, considerando que en 2022 se tenía una mayor demanda. En 2023 el decrecimiento es atribuido principalmente al encarecimiento del crédito por las altas tasas de interés han desincentivado a los hogares en la compra de estos bienes, y recientemente también hay algunos gremios que mencionan que hay un impacto negativo por las alzas en los precios de los combustibles.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/7c5ebea2-5a75-4011-8fad-0414d9ad07ba)

## Análisís regional:

La encuesta también hace una medicion a nivel regional, aunque con ciertas limitaciones, en el grafico se observa la participación por departamento en las ventas reales totales a nivel nacional, donde destaca la participación de Bogotá, Antioquia y Valle del Cauca y una agrupación adicional que ellos denominan otros departamentos

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/21161aac-6e38-4389-9c82-e6cdb4f8d8b7)

Para analizar los resultados por departamento se obtiene el total de ventas de enero a septiembre de cada año, considerando que la EMC utilizada esta disponible hasta septiembre de 2023.
De esta forma, se obtiene un grafico de barras que consolida los resultados de las ventas trasnformadas en indice base 2019 para cada año. 

Se logra ver el crecimiento de las ventas a lo largo del periodo 2020 a 2022 para todos los departamentos, sin embargo, en 2023 se estanca ese crecimiento, y si bien continuamos con ventas superiores a las de 2021, es clara la disminución significativa respecto a 2022. 

Al observar el comportamiento por departamentos, llama la atención que durante todo el periodo el comportamiento de Cundinamarca logra superar las ventas año a año respecto a los demás departamentos.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/898ec5a3-e6ed-412c-b163-b5860a2e7bdf)

Al analizar el comportamiento de Cundinamarca, podemos ver cuales son las actividades comerciales que mayores ventas presentan. Para el caso de los departamentos no se cuenta con lineas de mercancia, sino con una desagregación por actividad comercial. En el siguiente grafico se refleja la desagregación por trimestre de 2022 y 2023, en donde sobresalen las ventas de prendas de vestir y calzado, repuestos, y artículos culturales, lo que demuestra que Cundinamarca es intensivo en estos bienes. En el código se podra ver a nivel de fuente cuales son las empresas que se destacan en estas actividades. 

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/352c13c7-0a08-4e7d-815f-3db91a5d0560)

Al observar el mismo ejercio para Bogotá se observa un cambio de tendencia, podemos ver que contrario a Cundinamarca, Bogotá es más intensivo en equipo de informática y vehículos sobre todo el en 2022.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/078f8d0b-0bd6-4ebd-b617-3ce5ae7d051d)

## Comportamiento del empleo 2019-2022 por departamento

* Finalmente, se busca ver graficamente cómo se ha comportado el personal ocupado que recoge la encuesta por departamentos.  Se destaca Bogotá, Antioquia, Valle del Cauca como los más intensivos en contratación en el sector, dejando a Cundinamarca y Santander con el nivel mas bajo. 
* En términos generales, para el 2023 se observa una estabilización del empleo en todos los departamentos, no se observa una tendencia decreciente. 
* Llama la atención el comportamiento de Atlántico, que venia registrando un crecimiento sostenido en 2022 y en 2023 se estabiliza
* En 2023 solanente Santander quien muestra tendencia positiva en el personal ocupado

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/5b624066-8058-4d0f-9b6c-f8251abfdb63)
![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/125eecd5-1750-4263-8b01-18dd3268d194)

 ## ¿Qué se espera del comercio para 2024?

El análisis realizado permitió ver cómo el comercio minorista en 2023 se ha visto afectado por la coyunyura economica marcada por la inflación, en la medida en que varias lineas de mercancia presentan decrecimiento en sus ventas reales, comportamiento atribuido a los precios altos y al alza en las tasas de interés que desincentiva la adquisición de estos bienes, y por el contrario, la tendencia de los hoagres esta orientada a adquirir solamente bienes básicos como los productos de aseo personal que sí han mostrado crecimiento en 2023. 

En el futuro, se anticipa que el comercio continuará enfrentando desafíos debido a la difícil situación económica. La presión sobre el presupuesto de los hogares, combinada con la disminución de la capacidad de consumo, contribuirá a este escenario. La ausencia de incentivos, como la política del Día sin IVA, también podría impactar negativamente en el sector. 

La persistencia de la inflación y las tasas de interés elevadas son factores adicionales que podrían prolongar la debilidad en el comercio. Es necesario estar atentos a estos elementos que influyen en el entorno económico.

