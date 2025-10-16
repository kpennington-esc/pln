<img src="https://github.com/hernancontigiani/ceia_memorias_especializacion/raw/master/Figures/logoFIUBA.jpg" width="500" align="center">

# Procesamiento de Lenguaje Natural
Carrera Especialización en Inteligencia Artificial - FIUBA

**Alumno**: Kevin Pennington


## Contenido
- [Procesamiento de Lenguaje Natural](#procesamiento-de-lenguaje-natural)
  - [Contenido](#contenido)
  - [Introducción](#introducción)
  - [Desafío 1: Vectorización y Clasificación de Texto](#desafío-1-vectorización-y-clasificación-de-texto)
    - [Consigna](#consigna)
    - [Implementación](#implementación)
  - [Desafío 2: Word Embeddings con Gensim](#desafío-2-word-embeddings-con-gensim)
    - [Consigna](#consigna-1)
    - [Implementación](#implementación-1)
  - [Desafío 3: Modelo de Lenguaje con LSTM](#desafío-3-modelo-de-lenguaje-con-lstm)
    - [Consigna](#consigna-2)
    - [Implementación](#implementación-2)
      - [Corpus y modelo](#corpus-y-modelo)

## Introducción

En este repositorio se encuentran los trabajos prácticos realizados durante la cursada de la materia Procesamiento de Lenguaje Natural (PLN) de la carrera de Especialización en Inteligencia Artificial de la Facultad de Ingeniería de la Universidad de Buenos Aires (FIUBA). 

Cada trabajo práctico se encuentra en su propio directorio.

## Desafío 1: Vectorización y Clasificación de Texto

### Consigna
1. **Vectorizar documentos**: Tomar 5 documentos al azar y medir similaridad con el resto. Analizar los 5 documentos más similares.
2. **Clasificación por prototipos**: Implementar modelo zero-shot comparando similitud con documentos de entrenamiento.
3. **Modelos Naïve Bayes**: Entrenar MultinomialNB y ComplementNB para maximizar F1-score macro.
4. **Similaridad entre palabras**: Transponer matriz documento-término y estudiar similaridad entre palabras seleccionadas manualmente.

### Implementación
- Vectorización TF-IDF y coseno similaridad
- Clasificación basada en prototipos (k-NN conceptual)
- Optimización de hiperparámetros para Naïve Bayes
- Análisis de similaridad semántica entre términos

link [notebook](tp_1/sol_1.ipynb)

## Desafío 2: Word Embeddings con Gensim

### Consigna
1. Crear vectores de embeddings con Gensim usando un dataset personalizado
2. Probar términos de interés y analizar similitudes en el espacio de embeddings
3. Visualizar embeddings
4. Obtener conclusiones sobre relaciones semánticas

### Implementación
- Entrenamiento de Word2Vec con corpus personalizado
- Análisis de relaciones semánticas y sintácticas
- Visualización con reducción de dimensionalidad (t-SNE)
- Estudio de analogías y clusters semánticos

link [notebook](tp_2/sol_2.ipynb)

## Desafío 3: Modelo de Lenguaje con LSTM
    the effect of the monstrous structure of the most distinguishable chambers and corridors of the town,
### Consigna
1. Seleccionar corpus de texto para entrenar modelo de lenguaje
2. Pre-procesamiento y tokenización adecuada
3. Proponer arquitecturas basadas en unidades recurrentes
4. Generar secuencias con greedy search y beam search (determinístico y estocástico)
5. Analizar efecto de la temperatura en la generación

### Implementación

#### Corpus y modelo
- **Dataset**: Obras completas de H.P. Lovecraft (Kaggle)
- **Tokenización**: Character-level
- **Tamaño del vocabulario**: 68 tokens
- **Modelo**: LSTM 
```
LSTMModel(
  (embed): Embedding(68, 128)
  (lstm): LSTM(128, 256, num_layers=2, batch_first=True, dropout=0.2)
  (fc): Linear(in_features=256, out_features=68, bias=True)
)
```
link [colab](https://colab.research.google.com/drive/1meDAQHS_HWxInT5mvWDeyB2OlSa25dBa#scrollTo=ltm5m-WCXsvp)
