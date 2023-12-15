# Ngramas de canciones

Este código realiza la generación de n-gramas filtrados a partir de un conjunto de datos de canciones, considerando ciertos parámetros y restricciones. 

## Configuración de Parámetros:

Se definen varios parámetros que determinan cómo se realizará el filtrado de n-gramas, incluyendo la longitud máxima del tweet (tamano_tweet), las rutas a archivos de palabras (ruta_archivo_palabras y ruta_archivo_mujer), y la cantidad de palabras en la bolsa 1 y 2.

## Carga y Exploración del Conjunto de Datos:

Lee un archivo CSV (es_Canciones2Negativas.csv) que contiene datos sobre canciones, incluyendo columnas como 'misogynous' y 'tweet'.
Muestra los primeros registros del DataFrame y las columnas.

## Carga de Palabras y Verbos desde Archivos de Texto:

Carga palabras desde el archivo de texto especificado en ruta_archivo_palabras.
Carga términos considerados como misoginos desde el archivo de texto en ruta_archivo_mujer.

## Generación de N-gramas según Etiqueta:

Define una función llamada generar_ngramas_segun_etiqueta que genera n-gramas para tweets positivos (etiqueta 1) y negativos (etiqueta 0).
Filtra n-gramas según criterios como la presencia de palabras específicas y la cantidad de palabras consideradas misoginas.
Revuelve el índice de la lista de n-gramas negativos y selecciona el 20% de los n-gramas.

## Aplicación de Funciones a Cada Fila del DataFrame:

Itera sobre cada fila del DataFrame de canciones y aplica la función generar_ngramas_segun_etiqueta.
Almacena los n-gramas filtrados en una lista llamada ngramas_filtrados.

## Creación de DataFrame y Guardado en Archivo CSV:

Crea un nuevo DataFrame (df_ngramas) utilizando los n-gramas filtrados y las etiquetas correspondientes.
Guarda este nuevo DataFrame en un archivo CSV (ngramas_filtrados_prueba5.csv).

## Resultados y Confirmación:

Imprime un mensaje indicando la ubicación del archivo CSV donde se guardaron los n-gramas filtrados.
