# World Happiness Report – Análisis Estadístico y Visualización Interactiva

Este proyecto integra técnicas estadísticas y visualización de datos para analizar el nivel de felicidad global usando el **World Happiness Report (2015)**. Combina pruebas paramétricas y no paramétricas en Python con dashboards interactivos construidos en Tableau para explorar diferencias regionales y los factores que contribuyen a la felicidad en distintos países del mundo.

---

## Objetivos

- Evaluar si existen diferencias significativas en los niveles de felicidad entre regiones del mundo.
- Comparar estadísticamente el puntaje de felicidad entre dos regiones específicas.
- Identificar los factores que más contribuyen al nivel de felicidad en promedio por región.
- Comunicar visualmente patrones globales mediante dashboards interactivos en Tableau.

---

## Conjunto de datos

- **Nombre:** World Happiness Report (2015)
- **Fuente:** Gallup World Poll
- **Disponible en:** [Kaggle – World Happiness Report](https://www.kaggle.com/datasets/unsdsn/world-happiness)
- **Tamaño:** 158 países

### Variables principales

- `Happiness Score`: Puntaje total percibido de felicidad.
- Componentes que explican el puntaje:
  - `Economy (GDP per Capita)`
  - `Family`
  - `Health (Life Expectancy)`
  - `Freedom`
  - `Trust (Government Corruption)`
  - `Generosity`
- `Region`: Región geográfica del país.

---

## Estructura del repositorio

Este repositorio contiene los siguientes archivos y carpetas:

- `Python Notebook.ipynb`: contiene el análisis estadístico realizado en Python:
  - Prueba t para comparar dos regiones.
  - Prueba de Kruskal-Wallis y prueba de Dunn (post hoc).

- `Tableau Dashboards/`: carpeta con los tableros desarrollados en Tableau.
  - `Tableau_Workbook_Felicidad.twbx`: archivo del libro de trabajo de Tableau.
  - `Distribución Global del Nivel de Felicidad Países y Regiones`: imagen del primer dashboard.
  - `Factores que contribuyen al nivel de felicidad Análisis Regional`: imagen del segundo dashboard.

- `data/`: carpeta que contiene los datos originales.
  - `2015.csv`: archivo CSV con el World Happiness Report 2015.

---

## Análisis Estadístico (Python)

### Comparación entre dos regiones

- **Regiones comparadas:** Europa Central y Oriental vs. América Latina y el Caribe.
- **Supuestos verificados:**
  - Normalidad (Shapiro-Wilk)
  - Homogeneidad de varianzas (Levene)
- **Resultado:**  
  Se aplicó la **prueba t de Student** → se encontró una **diferencia significativa** en los niveles de felicidad entre ambas regiones (p < 0.05).

### Comparación entre múltiples regiones

- Se descartaron regiones con menos de tres observaciones.
- Se aplicó la **prueba de Kruskal-Wallis**.
- **Resultado:**  
  Se encontraron diferencias significativas globales entre regiones (p < 0.05).
- Se realizó un análisis **post hoc con prueba de Dunn** (con corrección de Bonferroni), identificando pares de regiones con diferencias estadísticamente significativas.

---

## Visualización (Tableau)

### 1. Distribución Global del Nivel de Felicidad – Países y Regiones

- Mapa mundial coroplético del puntaje de felicidad.
- Gráfico de barras con promedio regional.
- Listados del Top 10 países más y menos felices.
- Escala de color clara con leyenda explicativa.

Archivo: `Distribución Global del Nivel de Felicidad Países y Regiones`

---

### 2. Factores que Contribuyen al Nivel de Felicidad – Análisis Regional

- Seis gráficos de barras comparando regiones según los siguientes factores:
  - Economía
  - Familia
  - Salud
  - Libertad
  - Confianza en el gobierno
  - Generosidad
- Permite observar qué componentes son más fuertes o débiles según la región.

Archivo: `Factores que contribuyen al nivel de felicidad Análisis Regional`

---

## Hallazgos Clave

- Existen **diferencias estadísticas significativas** entre regiones del mundo en cuanto a niveles de felicidad.
- América Latina y el Caribe presentan mayor felicidad que Europa Central y Oriental, según la prueba t.
- El puntaje de felicidad se compone principalmente de factores como economía, salud y libertad.
- Las regiones más felices combinan altos niveles de economía, salud, libertad y confianza institucional.
- Tableau permitió comunicar estas diferencias de manera clara, interactiva y visualmente atractiva.

---

## Conclusión

Este proyecto demuestra cómo integrar análisis estadístico con visualización avanzada para responder preguntas relevantes sobre bienestar global. La combinación de Python y Tableau permite un flujo de trabajo analítico sólido, desde la exploración de datos hasta la comunicación efectiva de los hallazgos.

---

## Recomendaciones futuras

- Extender el análisis a años posteriores del World Happiness Report para evaluar evolución temporal.
- Aplicar clustering o modelos predictivos para clasificar países según patrones de felicidad.
- Incorporar variables externas como desigualdad, pobreza o educación para ampliar el análisis.
