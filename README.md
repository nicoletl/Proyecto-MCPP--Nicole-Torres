# Proyecto-MCPP-
Considerando el contexto de desaceleración económica experimentado en 2023, como resultado de la transformación económica y social luego de atravesar por dos periodos de reactividación y crecimiento economico en 2021 y 2022, se propone llevar a cabo un análisis del sector de comercio al por menor en el país.

## Motivacion:
Considerando que la actividad de comercio, transporte y alojamiento tiene una participación del 20,1% en el valor agregado para el año 2022, siendo la actividad que mayor peso tiene seguido de la industria con el 13,4%, y dentro de esta actividad el sector de comercio al por mayor y menor tiene un peso de 49,2%,  y según el DANE, para el III trimestre de 2023 fue uno de los sectores que mas contribuyó al decrecimiento de -0,1% en el valor agregado, aportando -0,7p.p con una variación de -3,5% . 

A partir de allí, se ve la necesidad de realizar un analisis de la actividad a partir de la encuesta mensual de comercio minorista que realiza el DANE, tomando la encuesta a nivel de microdato que se puede obtener en la mesa DANE de la Universidad del Rosario. 

## Fuente de información:
Se toma la Encuesta Mensual de Comercio (EMC) minorista desarrollada por el DANE, la cual proporciona los principales indicadores sobre la evolución de la actividad comercial del país, por medio de resultados del comercio al por menor y de vehículos, al generar información sobre variables como ventas, personal ocupado y sueldos y salarios de empresas de comercio al por menor dedicadas a la "reventa" (venta sin transformación) de mercancías o productos, que se encuentran en el territorio nacional.

## Caracteristicas:

*La encuesta tiene cobertura a nivel nacional y a nivel regional mide los departamentos de Antioquia, Atlántico, Bogotá, Cundinamarca, Santander, Valle del Cauca. Existe además un dominio residual correspondiente a "otros departamentos".
*A nivel de microdato recoge la información de 400 variables para 2301 empresas. 
*La EMC viene del periodo de enero de 2019 a septiembre de 2023, y para objeto de analisis se toma la información de las variables que recogen las ventas reales por linea de mercancia a nivel nacional, así como de las ventas reales por actividad económica para realizar el analisis regional.

##¿cómo han sido los últimos tiempos en oferta y demanda en colombia?

A continuación se observa la evolución del consumo de los hogares en los últimos años, que está directamente relacionado con el comercio minorista. 

2019 fue un año de cotidianidad, luego, en 2020, nos enfrentamos a la incertidumbre con la llegada de la pandemia. El año 2021 marcó un periodo de reactivación, con un aumento en la compra de bienes duraderos y semiduraderos, y el regreso gradual a la presencialidad con la disminución de restricciones. Durante 2022, observamos un crecimiento significativo, impulsado por la completa normalización de la presencialidad y la tendencia de los hogares a participar en eventos y adquirir bienes y servicios fue notable. Sin embargo, al llegar a 2023, nos encontramos en un momento de ajuste, pues el consumo de bienes duraderos y no duraderos ha disminuido debido al impacto negativo del aumento de la inflación, que alcanzó máximos del 12% - 13% anual, y al incremento de las tasas de interés. Estos factores han desincentivado el consumo y se reflejan en la contracción de la actividad comercial en este año.

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/4879840d-94d6-4357-8ecb-e352977df5b3)

En linea con lo anterior, a continuación tenemos el comportamiento del sector de comercio al por mayor y menor, el agregado de comercio, transporte y alojamiento y el PIB en su serie desestacionalizada, en variaciones anuales y la serie transformada en indice base 2019.

En terminos de variaciones anuales, se resalta el decrecimiento del comercio que se empezó a observar finalizando el 2022
![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/8e56a0a6-1f64-45b4-b7ea-1de65078dcea)

Tambien vale la pena observar los resultados desestacionalizados, esta vez de las series transformadas en índices base 2019. Al utilizar un índice base, se elimina la magnitud absoluta de las cifras y se resalta la variación porcentual con respecto a un período específico (en este caso, 2019 dado que fue el periodo posterior a la pandemia). Un valor de menor a 100 indica una reducción de la actividad, mientras que un valor superior a 100 indicaría un aumento en comparación con el nivel observado en 2019. Se observa que incluso desde 2022 la actividad no ha logrado superar los resultados de 2019, sin embargo, aún no muestra tendencia negativa. 

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/93824a03-bcdb-43b4-a800-e4b17176f52f)

En adelante, vamos a seguir viendo series transformadas en indice base 2019

A continuación, se muestra el primer ejercicio realizado con la EMC en donde se calcula la serie de ventas reales minoristas 

![image](https://github.com/nicoletl/Proyecto-MCPP-/assets/69484970/117d5d35-66e9-4475-8895-f1a4ae7c4615)

Respecto a 2023 se observa una disminución en la magnitud del índice si bien se mantiene superior a 100, se observa una disminución significativa respecto a los indices de 2022, mostrando un estancamiento sin señales de recuperar la magnitud de las ventas de 2022. 

