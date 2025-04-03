# World-Happiness-Report
Práctica en Python de ANOVA y Kruskal-Wallis (método no paramétrico) para investigar si las medias (o medianas, según sea el caso) de los puntajes de felicidad difieren entre los países del mundo, usando el conjunto de datos World Happiness Report.

El **World Happiness Report** es una iniciativa internacional que evalúa y clasifica a los países del mundo según los niveles de felicidad percibida por sus ciudadanos. Este conjunto de datos proviene de encuestas realizadas anualmente por Gallup World Poll y es utilizado ampliamente en investigaciones sobre bienestar, desarrollo social, economía conductual y políticas públicas.

El **objetivo** de este estudio es averiguar si hay diferencias entre los puntajes de la felicidad entre las diferentes regiones del mundo, aplicando métodos paramétricos y no paramétricos según se requiera.

Hay 11 variables, ninguna tiene valores nulos. En este estudio nos interesa particularmente el *Happiness Score*, la puntuación de la felicidad, que es un número flotante. La puntuación de la felicidad es la suma de las seis columnas *Economy (GDP per Capita)*, *Family*, *Health (Life Expectancy)*, *Freedom*, *Trust (Government Corruption)*, *Generosity*, que describen el grado en que esos factores contribuyen a la evaluación de la felicidad en cada país.

En particular, se usará la prueba t para comparar las medias de dos muestras independientes (Europa Central y Oriental y América Latina y el Caribe); esta prueba tiene varios supuestos (normalidad de las distribuciones, homogeneidad de varianzas, independendia entre observaciones, independencia entre muestras, tamaños de muestra razonables y homogéneos), algunos de los cuales deben ser verificados. Además, se usará la prueba de Kruskall-Wallis para comparar las medianas (y con ello las distribuciones) de los puntajes de felicidad en las distintas regiones del mundo; esta es una alternativa no paramétrica al ANOVA, al no cumplirse los supuestos requeridos.

Ver conjunto de datos en: https://www.kaggle.com/datasets/unsdsn/world-happiness/data
