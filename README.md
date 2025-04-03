# World Hapiness Report - Análisis Estadístico en Python
Este proyecto explora si existen diferencias significativas en los niveles de felicidad entre distintas regiones del mundo, utilizando métodos estadísticos paramétricos y no paramétricos sobre el conjunto de datos **World Happiness Report**.

## Objetivo
Evaluar si los puntajes de felicidad difieren entre regiones del mundo, aplicando:
* La **prueba t de Student** para comparar dos regiones específicas.
* La **prueba de Kruskall-Wallis** (no paramétrica) para comparar múltiples regiones, seguida de una **prueba de Dunn** como análisis post hoc.

## Metodología
1. Variable principal: *Happiness Score*, que representa la percepción de felicidad en cada país.
2. Comparación entre dos regiones:
   * Se verificaron los supuestos de la prueba t: normalidad, homogeneidad de varianzas, independencia y tamaños razonables.
   * Se aplicó la prueba t de Student para muestras independientes entre:
     * Europa Central y Oriental.
     * América Latina y el Caribe.
3. Comparación entre múltiples regiones.
   * Dado el desequilibrio en tamaños muestrales y algunas regiones con muy pocos datos, se descartaron regiones con menos de tres observaciones.
   * Se aplicó la prueba de Kruskall-Wallis.
   * Tras rechazar la hipótesis nula, se realizó un análisis post hoc con la prueba de Dunn (con corrección de Bonferroni).

## Fuente de datos
* Nombre: World Happiness Report.
* Provedor: Gallup World Poll.
* Disponible en: https://www.kaggle.com/datasets/unsdsn/world-happiness/data
* Año: 2015.

La variable *Happiness Score* se construye como la suma ponderada de:
* *Economy (GDP per Capita)*
* *Family*
* *Health (Life Expectancy)*
* *Freedom*
* *Trust (Government Corruption)*
* *Generosity*

## Resultados clave
* Se verificaron correctamente los supuestos para la prueba t, concluyendo una diferencia significativa en la felicidad entre Europa Central y Oriental vs América Latina y el Caribe.
* La prueba de Kruskal-Wallis mostró diferencias globales significativas entre regiones.
* El post hoc de Dunn identificó pares de regiones con diferencias estadísticamente significativas.
