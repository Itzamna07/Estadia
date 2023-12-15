# Uso de transformers para obtener similaridad de TEXTO - IMAGENES

Este código se enfoca en procesar y analizar datos provenientes de un conjunto de archivos CSV relacionados con figuras e información textual. La actividad abarca la obtención de características, en este caso, la similitud entre el texto asociado a una figura y la imagen correspondiente.

## Proceso de Obtención y Limpieza de Datos:

Lee dos archivos CSV (CSV_Papers_labeled - CSV_Papers_labeled (2).csv y CSV_Papers_labeled2.csv) y los concatena en un único DataFrame llamado df.
Define funciones para contar palabras en un texto (contar_palabras) y limpiar el texto (limpiar_texto), eliminando caracteres no en inglés, signos de puntuación y stopwords en inglés.
Añade una nueva columna llamada 'tamano' al DataFrame, que contiene la cantidad de palabras en la columna 'texto_figura'.

## Proceso de Procesamiento de Texto e Imágenes:

Utiliza la biblioteca Sentence Transformers con el modelo preentrenado 'clip-ViT-B-32'.
Itera sobre cada fila del DataFrame y, para cada texto asociado a una figura, calcula su similitud con la imagen correspondiente.
Divide el texto si su longitud supera un umbral y calcula la similitud para cada fragmento, promediando los resultados.
Almacena las puntuaciones de similitud en una lista llamada similarity_scores.

## Proceso de Actualización y Guardado del DataFrame:

Agrega una nueva columna 'similaridad' al DataFrame, que contiene las puntuaciones de similitud.
Guarda el DataFrame modificado con las columnas 'tamano' y 'similaridad' en un nuevo archivo CSV llamado dataimg_iclr_similaridad_stopwords.csv.
Lee el nuevo archivo CSV y realiza la actualización de etiquetas en la columna 'label' basándose en otro archivo CSV llamado iclr_datos_completos.csv.
Guarda el DataFrame actualizado en un nuevo archivo CSV llamado CSV_iclr_stop_labeled_2.csv.

## Resultados y Confirmación:

Muestra los primeros registros del DataFrame modificado.
Imprime un mensaje de confirmación indicando la ubicación del archivo CSV con las columnas añadidas.
