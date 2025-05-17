# DL-Clasificacion


Objetivo del proyecto:

Aplicar técnicas de deep learning para clasificar correos como 'spam' o 'no spam', mediante la ejecución de un análisis exploratorio de datos (EDA), la implementación de una arquitectura neuronal adecuada, la evaluación del modelo con métricas de clasificación, y el registro sistemático de resultados empleando la plataforma MLflow.

=======================================================================

Descripción del dataset: 

Dataset: Email Spam Classification Dataset CSV

Fuente: Kaggle ----> https://www.kaggle.com/datasets/balaka18/email-spam-classification-dataset-csv?utm_source=chatgpt.com

Se puede acceder a él a través del archivo: emails.rar o a través del enlace de google drive indicado den cada notebook.

Acerca del conjunto de datos

El archivo csv contiene 5172 filas, cada fila para cada correo electrónico. Hay 3002 columnas. La primera columna indica el nombre del correo electrónico. El nombre se ha establecido con números y no con el nombre de los destinatarios para proteger la privacidad. La última columna tiene las etiquetas para la predicción: 1 para spam, 0 para no spam. Las 3000 columnas restantes son las 3000 palabras más comunes en todos los correos electrónicos, después de excluir los caracteres/palabras no alfabéticos.

=======================================================================

Decisiones tomadas en el modelado:

Se seleccionó un problema clasificación binaria en procesamiento de lenguaje natural (NLP) para predecir correos spam o no spam.
El tipo de red que se usó fue: Red Neuronal Artificial (ANN), es una Red Neuronal Feedforward Multicapa (Multilayer Perceptron - MLP).
En este caso los datos fluyen en una sola dirección, desde la entrada hasta la salida. No hay ciclos o retroalimentación. 

  Capas usadas en el proyecto:
Capa de entrada: recibe vectores de entrada con input_dim características (en este caso, 3000 columnas del bag-of-words del email).

Capas ocultas:Varias capas Dense con activación ReLU (512, 256, 128 unidades).

Se agregan capas BatchNormalization para estabilizar el aprendizaje.
Se usan capas Dropout para reducir overfitting.

Capa de salida: una única neurona con activación sigmoide

=======================================================================

Resultados y métricas principales:

