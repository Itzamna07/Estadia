# Scrapping Tumblr

Este código realiza el scraping de una página de Tumblr con el objetivo de obtener información relevante de publicaciones que contienen imágenes. A continuación, se presenta una descripción de la actividad y las funciones del código:

## Configuración y Preparación:

Importa las bibliotecas necesarias, como requests para realizar solicitudes HTTP, BeautifulSoup para el análisis HTML, PIL para el manejo de imágenes y csv para la manipulación de archivos CSV.
Define la URL de la página de Tumblr a scrapear y las rutas de la carpeta y el archivo CSV para almacenar los resultados.

## Solicitud HTTP y Análisis HTML:

Realiza una solicitud GET a la página de Tumblr.
Parsea el contenido HTML de la página utilizando BeautifulSoup.
Identifica y selecciona los elementos HTML relevantes que contienen la información de interés.

## Iteración sobre Publicaciones:

Itera sobre las publicaciones identificadas en la página.
Para cada publicación, extrae información como el texto asociado, hashtags y la URL de la imagen.
Descarga la imagen asociada a la publicación y la guarda en la carpeta especificada.

## Procesamiento de Texto e Información Adicional:

Para cada publicación, obtiene el texto completo, hashtags y el nombre de la imagen.
Almacena esta información en una lista llamada data para su posterior escritura en un archivo CSV.
Muestra en la consola información relevante, como la URL de la imagen, el texto completo y los hashtags encontrados.

## Escritura en Archivo CSV:

Abre el archivo CSV en modo de escritura ('w' o 'a' dependiendo de si el archivo ya existe).
Escribe los encabezados del CSV si es un nuevo archivo.
Escribe los datos recopilados en el archivo CSV.

## Resultados y Confirmación:

Imprime un mensaje indicando la ubicación del archivo CSV donde se guardaron los datos.
