DESAFÍOS DE PROCESS NATURAL LANGUAGE 

Aquí se amplían los detalles de cada uno de los desafíos:

################################################################

Desafio_1_Gustavo_Unapillco_a1624

Este desafío se centra en la exploración de un conjunto de datos de texto (dataset fetch_20newsgroups) utilizando técnicas básicas de PNL. Se busca entender las relaciones entre documentos y palabras.

•	Vectorización y Similitud: El primer paso es convertir los documentos de texto en vectores numéricos. Esto se logra utilizando TfidfVectorizer, una técnica que pondera las palabras según su frecuencia en el documento y su rareza en todo el conjunto de datos. Luego, se calcula la similitud de coseno entre los vectores para determinar qué documentos son más parecidos entre sí. Se seleccionan 5 documentos aleatorios y se analizan sus 5 documentos más similares. El análisis se enfoca en determinar si la similitud numérica se corresponde con una similitud real en el contenido temático y en las etiquetas de clasificación asignadas a los documentos.

•	Clasificación con Naive Bayes: El segundo objetivo es construir un modelo predictivo para clasificar los documentos en diferentes categorías. Se utilizan los algoritmos Naive Bayes Multinomial y ComplementNB que son adecuados para la clasificación de texto. Se realiza una búsqueda de hiperparámetros para encontrar la configuración óptima del modelo, utilizando la métrica F1-score macro como medida del rendimiento en el conjunto de datos de prueba.

•	Análisis de Similitud de Palabras: El último paso es analizar las relaciones entre palabras. Para ello, se transpone la matriz documento-término, lo que produce una matriz término-documento. Esta matriz permite tratar cada palabra como un vector y calcular la similitud entre palabras. Se eligen 5 palabras clave: "people", "think", "make", "just" y "time". Se analizan las 5 palabras más similares a cada una de estas palabras clave. Las conclusiones se basan en cómo las palabras similares reflejan los temas de conversación y debate presentes en el conjunto de datos de foros de discusión.

################################################################

Desafio_2_Gustavo_Unapillco_a1624

Este desafío se enfoca en la creación y análisis de vectores de palabras (word embeddings) utilizando la biblioteca Gensim y el libro "Orgullo y Prejuicio". Se busca entender cómo los diferentes modelos de embedding capturan las relaciones semánticas entre palabras.

•	Creación de Embeddings: Se utilizan dos modelos de embedding: Word2Vec y FastText. Estos modelos aprenden a representar las palabras como vectores numéricos, donde palabras con significados similares se ubican cerca en el espacio vectorial.

•	Análisis de Similitud: Se exploran las similitudes entre palabras utilizando ambos modelos. Se eligen palabras clave ("respect" y "pride") y se analizan las palabras más similares a ellas. Se observa que FastText tiende a capturar mejor las relaciones semánticas, incluyendo palabras relacionadas por significado y por morfología.

•	Tests de Analogía: Se realizan tests de analogía para evaluar la capacidad de los modelos para capturar relaciones complejas entre palabras. Se formulan analogías del tipo "A es a B como C es a D". Los resultados muestran que ambos modelos tienen dificultades para capturar las relaciones de analogía en el contexto específico de "Orgullo y Prejuicio".

•	Visualización de Embeddings: Se utiliza t-SNE para reducir la dimensionalidad de los embeddings y visualizarlos en un gráfico 2D. Se observa que FastText tiende a agrupar palabras relacionadas con personajes, temas y emociones de la novela.

################################################################

Desafio_3_Gustavo_Unapillco_a1624

Este desafío se centra en la generación de texto utilizando una red neuronal recurrente (RNN) con una capa LSTM. El objetivo es entrenar un modelo que pueda predecir la siguiente palabra en una secuencia de texto.

•	Preparación del Dataset: Se utiliza el libro "The Adventures of Sherlock Holmes" como dataset. Se realiza un preprocesamiento para limpiar el texto, convertirlo en tokens y crear secuencias de palabras de longitud fija.

•	Arquitectura del Modelo: Se construye un modelo RNN con una capa LSTM, capas fully connected y dropout. Se utiliza CrossEntropyLoss como función de pérdida y Adam como optimizador.

•	Entrenamiento y Resultados: Se entrena el modelo durante 100 épocas. Los resultados muestran un bajo rendimiento en la precisión (accuracy), lo que indica que el modelo no está aprendiendo de forma eficaz.

•	Generación de Texto: Se implementa una función para generar nuevas secuencias de texto a partir de un texto inicial.

•	Conclusiones: Se discuten las limitaciones del modelo, incluyendo el bajo rendimiento, la falta de mejora durante el entrenamiento y la posibilidad de underfitting. Se proponen recomendaciones para mejorar el rendimiento, como ajustar hiperparámetros, utilizar técnicas de regularización y entrenar durante más tiempo.

################################################################

Desafio_4_Gustavo_Unapillco_a1624.pdf

Este desafío se centra en la construcción de un chatbot de preguntas y respuestas (QA Bot). Se utiliza un modelo encoder-decoder con una capa LSTM para procesar la pregunta del usuario y generar una respuesta adecuada.

•	Preprocesamiento: Se utiliza un dataset de conversaciones del challenge ConvAI2. Se realiza un preprocesamiento para convertir las frases de entrada y salida en secuencias de enteros y crear diccionarios de palabras a índices.

•	Embeddings: Se utilizan embeddings preentrenados de FastText para transformar los tokens de entrada en vectores de 300 dimensiones.

•	Arquitectura del Modelo: Se construye un modelo encoder-decoder con una capa LSTM. El encoder procesa la pregunta del usuario, mientras que el decoder genera la respuesta.

•	Entrenamiento: Se entrena el modelo utilizando los datos preprocesados.
•	Inferencia: Se implementa una función para realizar la inferencia del modelo, procesando la pregunta del usuario y generando una respuesta. Se describen los pasos para tokenizar la pregunta, convertir las palabras a índices y ajustar el formato de la entrada al modelo.

En resumen, los cuatro desafíos exploran diferentes aspectos del PNL, desde el análisis básico de texto hasta la construcción de modelos más complejos para la generación de texto y la creación de chatbots. Las fuentes describen el proceso de implementación, los resultados obtenidos y las conclusiones extraídas, proporcionando una visión general del desarrollo de proyectos de PNL.

