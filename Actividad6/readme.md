# "Análisis de Texto en Conferencias Académicas: Visualización y Tokenización"

Este proyecto combina técnicas avanzadas de procesamiento de lenguaje natural (NLP) y herramientas de tokenización para realizar un análisis profundo de conjuntos extensos de datos textuales relacionados con conferencias académicas. 

## Limpieza y Concatenación de Texto:

Se realiza la limpieza del texto, convirtiéndolo a minúsculas y eliminando números y caracteres innecesarios.
Los textos relevantes de las conferencias, como títulos, resúmenes, introducciones y conclusiones, se concatenan para formar textos completos y representativos.

## Análisis de Comportamiento de Series Temporales:

Se utiliza el parámetro de Hurst para analizar el comportamiento de las series temporales generadas a partir de los textos.
El análisis de Hurst proporciona información sobre la autocorrelación y la naturaleza de las tendencias en los textos.

## Tokenización con Múltiples Modelos:

Se implementa una tokenización avanzada utilizando varios modelos, como BPE, Unigram, WordPiece y WordLevel.
Cada tokenizador se entrena en grandes conjuntos de datos de texto para adaptarse a la estructura y características del lenguaje utilizado en las conferencias académicas.

## Resultados y Almacenamiento:

Los resultados, que incluyen parámetros de Hurst y características tokenizadas, se almacenan en un DataFrame estructurado.
Se exportan los resultados a archivos CSV para facilitar su posterior análisis y visualización.

## Visualización de Resultados:

Se emplean visualizaciones gráficas para entender mejor los resultados del análisis.
Se utilizan boxplots y gráficos de distribución acumulada para comparar y contrastar la distribución de parámetros de Hurst entre textos aceptados y rechazados.
