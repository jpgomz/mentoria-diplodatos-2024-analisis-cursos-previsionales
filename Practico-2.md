### Universidad Nacional de Córdoba - Facultad de Matemática, Astronomía, Física y Computación
#### Diplomatura en Ciencia de Datos, Aprendizaje Automático y sus Aplicaciones 2024
##### Mentoría M15: Analizando cursos previsionales: búsqueda de insights para entender audiencia y mejorar ventas

# Práctico 2 - Análisis Exploratorio y Curación de Datos

Continuaremos trabajando con los datos utilizados en el práctico anterior y nos basaremos en los resultados obtenidos previamente,
Armaremos los dataframes que utilizaremos para los modelos de aprendizaje, teniendo en mente alguno(s) de los siguientes objetivos:

1.  Predecir si un determinado usuario registrado realizará una compra o no, en base a si ha realizado una consulta.
2.	Detección de tópicos de consulta.
3.	Determinar grupos de compradores.

Pueden utilizar cualquiera de las bases del dataset (orders, contacts, customers) y bases adicionales, según lo vean conveniente.

## Actividades
Se sugieren las siguientes actividades según el/los objetivo(s) seleccionados:

### General:
- ¿Qué tratamiento le darán a los datos faltantes? Explique su razonamiento y qué impacto cree que puede generar. 
- Convierta los campos de fecha/tiempo a pandas datetime para facilidad de uso.
- ¿Se pueden identificar outliers? Comentar y determine qué pasos tomar, elimínelos de considerarlo necesario.

### Orders (requerido: 1, 3):
- Construya las variables adicionales que considere convenientes para su análisis, por ejemplo: si la compra corresponde a un pack o a un curso, día de la semana, si es día laborable o no, hora de la compra.
- ¿Conviene agrupar (y/o desagrupar) la variable ‘producto’? Comente y aplique según vea conveniente.
- ¿Es necesario incluir todos los registros o conviene hacer algún filtrado? Comente y aplique según vea conveniente.

### Contacts (requerido: 2,  opcional: 1):
- Utilizando alguna librería de procesamiento de lenguaje natural (e.g. NLTK, SpaCy), realice las siguientes tareas y comente brevemente en qué consiste cada una de estas técnicas:
  - **tokenización** de los mensajes de contacto,
  - **remoción de *stopwords*** del texto tokenizado, ¿qué relación encuentra entre los resultados encontrados en el primer práctico y este paso?
  - **extracción de raíces** (***stemming***) de los tokens obtenidos,
  - **lematización** de los tokens, ¿en qué se diferencia del método de stemming? ¿qué beneficios/desventajas hay entre ambos?
- Una forma usual de tratar los datos de textos es mediante alguna representación numérica/vectorial. Para esto utilizaremos la librería scikit-learn. Aplique las siguientes transformaciones sobre el texto preprocesado y describa en simples palabras en qué consiste cada método.
  - **Bag of words (*BoW*)**, utilizando la clase CountVectorizer de scikit-learn.
  - **Term frequency – Inverse-document frequency (*TF-IDF*)**.
  *Opcional: puede explorar otros métodos como Word2Vec, Sent2Vec, etc.*

### Customers (opcional: 1, 3):
- En base al set customers, determinar para cada contacto si corresponde a un usuario registrado en la plataforma o uno externo.
- En base al set orders, determinar para cada customer si ha efectuado al menos una compra.
