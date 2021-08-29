---
title: Introducción
parent: NLP
has_children: false
nav_order: 7
---

# Introducción a Natural Language Processing

## References

- [x] an easy introduction: https://builtin.com/data-science/easy-introduction-natural-language-processing
- [x] nlp wiki: https://en.wikipedia.org/wiki/Natural_language_processing
- [ ] nlp recipies (microsoft): https://github.com/sci2lab/nlp-recipes
- [ ] nlp best practices: https://www.kdnuggets.com/2020/05/natural-language-processing-recipes-best-practices-examples.html
- [ ] book: *"Natural Language Processing Recipes Unlocking Text Data with Machine Learning and Deep Learning using Python"*,  by Akshay Kulkarni, Adarsha Shivananda

---

# Introduccion

> NLP es un subcampo de la inteligencia artificial que se centra en permitir que las computadoras comprendan y procesen los lenguajes humanos (datos no estructurados).

> El procesamiento del lenguaje natural ( NLP ) es un subcampo de la lingüística , la informática y la inteligencia artificial que se ocupa de las interacciones entre las computadoras y el lenguaje humano, en particular cómo programar las computadoras para procesar y analizar grandes cantidades de datos del lenguaje natural . 

El resultado es una computadora capaz de "comprender" el contenido de los documentos, incluidos los matices contextuales del idioma que contienen. Luego, la tecnología puede extraer con precisión la información y los conocimientos contenidos en los documentos, así como categorizar y organizar los propios documentos.

### history

Hasta la década de 1980, la mayoría de los sistemas de procesamiento del lenguaje natural se basaban en conjuntos complejos de reglas escritas a mano. Sin embargo, a fines de la década de 1980, se produjo una revolución en el **procesamiento del lenguaje natural con la introducción de algoritmos de aprendizaje automático** para el procesamiento del lenguaje. Esto se debió tanto al aumento constante del poder computacional (ver la ley de Moore ) como a la disminución gradual del dominio de las teorías lingüísticas chomskyanas (por ejemplo, la gramática transformacional ), cuyos fundamentos teóricos desalentaron el tipo de lingüística de corpus que subyace al enfoque del aprendizaje automático. al procesamiento del lenguaje.

Década de 2000 : con el crecimiento de la web, desde mediados de la década de 1990 se dispone de cantidades cada vez mayores de **datos lingüísticos en bruto (sin anotar)**. Por lo tanto, la investigación se ha centrado cada vez más en **algoritmos de aprendizaje no supervisados y semi-supervisados** . Dichos algoritmos pueden aprender de los datos que no se han anotado manualmente con las respuestas deseadas o utilizando una combinación de datos anotados y no anotados. Generalmente, esta tarea es mucho más difícil que el aprendizaje supervisado y, por lo general, produce resultados menos precisos para una determinada cantidad de datos de entrada.

En la década de 2010, el **aprendizaje de representación** (por ej vision) y los métodos de aprendizaje automático de estilo de **red neuronal profunda** se generalizaron en el procesamiento del lenguaje natural, debido en parte a una serie de resultados que muestran que tales técnicas [7] [8] pueden lograr resultados de vanguardia en muchas tareas de lenguaje natural, por ejemplo en modelado de lenguaje, [9] análisis, [10] [11] y muchos otros.

### contesto: dificultad de las maquinas

¿qué crees que significa el siguiente fragmento de texto?

> “Steph Curry estuvo en llamas la pasada noche. Destruyó totalmente al otro equipo "

Para un humano probablemente sea bastante obvio lo que significa esta oración. Sabemos que Steph Curry es jugadora de baloncesto; o incluso si no sabemos que juega en algún tipo de equipo, probablemente un equipo deportivo. Cuando vemos "en llamas" y "destruido" sabemos que significa que Steph Curry jugó muy bien anoche y venció al otro equipo.

**Las computadoras tienden a tomar las cosas demasiado literalmente**. Al ver las cosas literalmente como una computadora, veríamos "Steph Curry" y, en función de las mayúsculas, asumir que es una persona, un lugar o algo importante, ¡lo cual es genial! Pero luego vemos que Steph Curry “estaba en llamas”…. ¡Una computadora podría decirle que alguien literalmente prendió fuego a Steph Curry ayer! … ¡Ay! Después de eso, la computadora podría decir que el Sr. Curry ha destruido físicamente al otro equipo…. ya no existen según esta computadora ... genial ...

### Aplicaciones de alto nivel del NLP

- Resumen automático (resumen de texto)
- Generación de libros
- Gestión del diálogo / chat bots.
- Corrección de errores gramaticales
- Máquina traductora
- Generación de lenguaje natural (NLG)
- Comprensión del lenguaje natural (NLU)
- Respuesta a preguntas
- Análisis más específicos e intrincados de documentos de texto


---

# lingüística de corpus

La lingüística de corpus estudia el lenguaje a través de ejemplos de textos reales producidos en el "mundo real".  Los partidarios de la lingüística de corpus creen que el análisis lingüístico más fiable se produce en las muestras recogidas en contextos naturales y con una interferencia mínima. 

En la filología forman los corpus aquellos textos, orales o escritos, y los documentos que los contienen, que han sido debidamente recopilados. Estos corpus constituyen las muestras que se utilizan en lingüística aplicada, entre otros, para estudiar y analizar las características del objeto de estudio, pues integran las muestras de los elementos que constituyen la realidad que se quiere observar. Tanto si es oral como escrito, un corpus deberá definirse en función de los objetivos que se persigan con el mismo.

### Corpus

**Corpora** (la forma plural de **corpus** , es un conjunto de documentos, posiblemente con **anotaciones humanas o informáticas**) de ejemplos típicos del mundo real.

En lingüística , un **corpus** ( corpora plural ) o **corpus de texto** es un recurso del lenguaje que consiste en un conjunto grande y estructurado de textos (hoy en día generalmente almacenados y procesados electrónicamente). En lingüística de corpus , se utilizan para realizar análisis estadísticos y pruebas de hipótesis , verificando ocurrencias o validando reglas lingüísticas dentro de un territorio lingüístico específico.


---


# Metodos

### Metodos simbolicos

En los primeros días, muchos sistemas de procesamiento del lenguaje se diseñaron mediante métodos simbólicos, es decir, la codificación manual de un conjunto de reglas, junto con una búsqueda en el diccionario: como escribir gramáticas o diseñar reglas heurísticas para derivación .

### Metodos del aprendizaje automatico

El paradigma del aprendizaje automático exige utilizar la **inferencia estadística** para aprender automáticamente tales reglas a través del análisis de grandes **corpora** (la forma plural de corpus , es un conjunto de documentos, posiblemente con anotaciones humanas o informáticas) de ejemplos típicos del mundo real.

- Los procedimientos de aprendizaje utilizados durante el aprendizaje automático se enfocan automáticamente en los casos más comunes.
- Los procedimientos de aprendizaje automático pueden hacer uso de algoritmos de inferencia estadística para producir modelos que son robustos a entradas desconocidas (por ejemplo, que contienen palabras o estructuras que no se han visto antes) y entradas erróneas (por ejemplo, palabras mal escritas o palabras omitidas accidentalmente).
- Los sistemas basados en el aprendizaje automático de las reglas pueden hacerse más precisos simplemente proporcionando más datos de entrada. Sin embargo, la creación de más datos para ingresar a los sistemas de aprendizaje automático simplemente requiere un aumento correspondiente en la cantidad de horas-hombre trabajadas, generalmente sin aumentos significativos en la complejidad del proceso de anotación.

### Métodos de estadística

Se han aplicado muchas clases diferentes de algoritmos de aprendizaje automático a las tareas de procesamiento del lenguaje natural. Estos algoritmos toman como entrada un gran conjunto de "features" que se generan a partir de los datos de entrada. Sin embargo, la investigación se ha centrado cada vez más en **modelos estadísticos** , que toman **decisiones probabilísticas suaves** basadas en la asignación de ponderaciones de valor real a cada característica de entrada. Tales modelos tienen la ventaja de que **pueden expresar la certeza relativa de muchas respuestas posibles diferentes** en lugar de una sola, produciendo resultados más confiables cuando dicho modelo se incluye como un componente de un sistema más grande.

Algunos de los primeros algoritmos de aprendizaje automático utilizados, como los *árboles de decisión*, produjeron sistemas de reglas estrictas si-entonces similares a las reglas escritas a mano existentes. Sin embargo, el etiquetado de parte del discurso introdujo el uso de *modelos ocultos de Markov* en el procesamiento del lenguaje natural y, cada vez más, la investigación se ha centrado en modelos estadísticos , que toman decisiones probabilísticas suaves basadas en asignar ponderaciones de valor real a las características que componen la entrada. datos. Los *modelos de lenguaje de caché* sobre los que muchos sistemas de reconocimiento de voz se basan son ejemplos de tales modelos estadísticos. Estos modelos son generalmente más robustos cuando se les da una entrada desconocida, especialmente una entrada que contiene errores (como es muy común para los datos del mundo real), y producen resultados más confiables cuando se integran en un sistema más grande que comprende múltiples subtareas.

Desde el giro neuronal, los métodos estadísticos en la investigación de la PNL han sido reemplazados en gran medida por redes neuronales. Sin embargo, continúan siendo relevantes para contextos en los que se requiere transparencia e interpretación de las estadísticas.

### Redes neuronales

Un gran inconveniente de los métodos estadísticos es que requieren una compleja ingeniería de features. Desde 2015, el campo ha abandonado en gran medida los métodos estadísticos y se ha desplazado a las redes neuronales para el aprendizaje automático. 


--- 


# Tareas comunes de NLP

## RESUMEN:

- **Procesamiento del texto**: tokenizacion (separar palabras), stop words (filtrado).
    
- **Analisis morfologico (partes de una palabra)**: lematizacion (raiz), stemming (base), segmentacion (partes de palabra).

	- Converting text to features
	- using One Hot Encoding.
    - using Count Vectorizing.
    - generating N-Grams.
    - generating Co-Ocurrence Matrix.
    - Hash Vectorizing.
    - using TF-IDF.
    - implementing Word Embeddings.
    - implementing fastText.
> Esta parte de la conversion del texto en features pertenece al libro *"Natural Language Processing Recipes Unlocking Text Data with Machine Learning and Deep Learning using Python"*,  by Akshay Kulkarni, Adarsha Shivananda.

- **Analisis sintactico (jerarquia de palabras en oracion)**: inferencia de gramatica, sentence breaking, parsing (clasificacion de componentes).

- **Semantica (significado)**:
    - *Semantica lexica (significado de las palabras)*: Named entity recognition (NER), Sentiment analysis, etc.
	- *Semantica de oraciones individuales (significado sentences)*: relaciones entre fragmentos, etiquetado de significado, eliminacion de la ambigüedad.
	- *Semantica mas alla de oracion indiv (significado de discurso)*: agrupacion de palabras relacionadas, relaciones entre sentences, **reconocimiento de topic** (tema) de segmentos (fragmentos de un texto), mineria del argumento de un texto. 



## Procesamiento de texto

###  Segmentación de palabras ( tokenización ) 

Separe un fragmento de texto continuo en palabras separadas. Para un idioma como el inglés , esto es bastante trivial, ya que las palabras suelen estar separadas por espacios. Sin embargo, algunos idiomas escritos como el chino , el japonés y el tailandés no marcan los límites de las palabras de esa manera, y en esos idiomas la segmentación del texto es una tarea importante que requiere el conocimiento del vocabulario y la morfología de las palabras en el idioma. A veces, este proceso también se utiliza en casos como la creación de bolsas de palabras (BOW) en la minería de datos. 

## Análisis morfológico

> La morfología (del griego μορφo morphḗ ‘forma’, y λογία logía ‘tratado o estudio’) es la rama de la lingüística que estudia la estructura interna de las palabras para definir y clasificar sus unidades: las variantes de las palabras (morfología flexiva) y la formación de nuevas palabras (morfología derivativa y composición). 

### Lematización (raiz)

La tarea de eliminar solo las terminaciones de las palabras (genero, numero, etc) y devolver la forma de diccionario base de una palabra que también se conoce como *lema*. La lematización es otra técnica para **reducir las palabras a su forma normalizada**. Pero en este caso, la transformación en realidad usa un diccionario para asignar palabras a su forma real. 

### Segmentación morfológica (componentes de una palagra)

Separe las palabras en morfemas individuales e identifique la clase de morfemas. La dificultad de esta tarea depende en gran medida de la complejidad de la morfología ( es decir , la estructura de las palabras) del idioma que se está considerando. El inglés tiene una morfología bastante simple, especialmente una morfología flexional , por lo que a menudo es posible ignorar esta tarea por completo y simplemente modelar todas las formas posibles de una palabra ( por ejemplo , "abrir, abrir, abrir, abrir") como palabras separadas. En idiomas como el turco o el meitei , unidioma indioaltamente aglutinado , sin embargo, este enfoque no es posible, ya que cada entrada del diccionario tiene miles de formas de palabras posibles. 

### Stemming (base)

El proceso de reducir las palabras flexionadas (o en ocasiones derivadas) a una forma básica ( por ejemplo , "cerrar" será la raíz de "cerrado", "cerrar", "cerrar", "más cerca", etc.). La derivación produce resultados similares a la lematización, pero lo hace basándose en reglas, no en un diccionario. 

## Análisis sintáctico

> El análisis sintáctico es el análisis de las funciones sintácticas o relaciones de concordancia y jerarquía que guardan las palabras cuando se agrupan entre sí en forma de sintagmas, oraciones simples y oraciones compuestas de proposiciones.

### Grammar induction / inference

Generacion de una gramática formal que describa la sintaxis de un idioma. Grammar induction (or grammatical inference) is the process in machine learning of learning a formal grammar from a set of observations, thus constructing a model which accounts for the characteristics of the observed objects. More generally, grammatical inference is that branch of machine learning where the instance space consists of discrete combinatorial objects such as strings, trees and graphs. 

### Sentence breaking (also known as "sentence boundary disambiguation")

Dado un fragmento de texto, encuentre los límites de la oración. Los límites de las oraciones a menudo están marcados por puntos u otros signos de puntuación , pero estos mismos caracteres pueden servir para otros propósitos ( por ejemplo , marcar abreviaturas ). 

### Parsing

Determinar el árbol de análisis sintáctico (análisis gramatical) de una oración determinada. La gramática de los lenguajes naturales es ambigua y las oraciones típicas tienen múltiples análisis posibles: quizás sorprendentemente, para una oración típica puede haber miles de análisis potenciales (la mayoría de los cuales parecerán completamente absurdos para un humano). Hay dos tipos principales de análisis: análisis de dependencias y análisis de constituyentes. El análisis de dependencias se centra en las relaciones entre palabras en una oración (marcando cosas como objetos primarios y predicados), mientras que el análisis de constituyentes se centra en construir el árbol de análisis utilizando una gramática probabilística libre de contexto (PCFG) (ver también gramática estocástica ). 

## Lexical semantics (of individual words in context)

> Se denomina como **semántica** a la ciencia lingüística que estudia el significado de las palabras y expresiones, es decir, lo que las palabras quieren decir cuando hablamos o escribimos.
>  **Lexico** es el conjunto de las palabras y expresiones de una lengua, un grupo o una persona.
> **Semántica léxica** es el estudio de los significados de las palabras. 

### Lexical semantics

¿Cuál es el significado computacional de palabras individuales en contexto? 

### Distributional semantics

¿Cómo podemos aprender representaciones semánticas a partir de datos? 

### Named entity recognition (NER) --> Reconocimiento de *entidades*

Dado un flujo de texto, determine qué elementos del texto se asignan a nombres propios, como personas o lugares, y cuál es el tipo de cada uno de esos nombres (por ejemplo, persona, ubicación, organización). Aunque las mayúsculas pueden ayudar a reconocer entidades nombradas en idiomas como el inglés, esta información no puede ayudar a determinar el tipo de entidad nombrada y, en cualquier caso, a menudo es inexacta o insuficiente. Por ejemplo, la primera letra de una oración también se escribe en mayúscula, y las entidades nombradas a menudo abarcan varias palabras, de las cuales solo algunas están en mayúscula. Además, muchos otros idiomas en escrituras no occidentales (por ejemplo, chino o árabe) no tienen mayúsculas en absoluto, e incluso los idiomas con mayúsculas pueden no usarlas consistentemente para distinguir nombres. Por ejemplo, el alemán escribe con mayúscula todos los sustantivos , independientemente de si son nombres, y el francés y el español no escriben con mayúscula los nombres que sirven como adjetivos . 

El análisis de entidades revisará su texto e identificará todas las palabras o "entidades" importantes en el texto, es decir, aquellas palabras que tienen algún tipo de significado semántico o significado del mundo real.

```Python
import spacy

### Load spaCy's English NLP model
nlp = spacy.load('en_core_web_lg')

### The text we want to examine
text = "..."
### Our 'document' variable now contains a parsed version of text.
document = nlp(text)

### print out all the named entities that were detected
for entity in document.ents:
print(entity.text, entity.label_)
```


### Sentiment analysis (see also Multimodal sentiment analysis)

Extrae **información subjetiva** generalmente de un conjunto de documentos, a menudo usando reseñas en línea para determinar la "polaridad" sobre objetos específicos. Es especialmente útil para identificar tendencias de opinión pública en redes sociales, para marketing. 

### Terminology extraction

El objetivo de la extracción de terminología es extraer automáticamente términos relevantes de un corpus dado. 

### Word sense disambiguation (Desambiguación del sentido de la palabra)
Muchas palabras tienen más de un significado ; tenemos que seleccionar el significado que tiene más sentido en contexto. Para este problema, normalmente se nos da una lista de palabras y los sentidos de las palabras asociadas, por ejemplo, de un diccionario o un recurso en línea como WordNet . 


## Relational semantics (semantics of individual sentences)

### Relationship extraction

Dado un fragmento de texto, identifique las relaciones entre las entidades nombradas (por ejemplo, quién está casado con quién). 

### Semantic parsing

Dado un fragmento de texto (típicamente una oración), produzca una representación formal de su semántica, ya sea como un gráfico (por ejemplo, en el análisis sintáctico AMR ) o de acuerdo con un formalismo lógico (por ejemplo, en el análisis sintáctico DRT ). Este desafío generalmente incluye aspectos de varias tareas más elementales de NLP de la semántica (p. Ej., Etiquetado de roles semánticos, desambiguación del sentido de las palabras) y puede extenderse para incluir un análisis del discurso completo (p. Ej., Análisis del discurso, correferencia; consulte Comprensión del lenguaje natural a continuación). 

### Semantic role labelling (see also implicit semantic role labelling)

Dada una sola oración, identifique y elimine la ambigüedad de los predicados semánticos (p. Ej., Marcos verbales ), luego identifique y clasifique los elementos del marco ( roles semánticos ). 


#### Analisis de declaraciones semiestructuradas

Extracción de declaraciones semiestructuradas.  Este algoritmo esencialmente analiza parte de la información que el modelo de NLP de spaCy pudo extraer y, en base a eso, podemos obtener información más específica sobre ciertas entidades. En pocas palabras, podemos extraer ciertos "hechos" sobre la entidad de nuestra elección.

```
import spacy
import textacy.extract

### Load spaCy's English NLP model
nlp = spacy.load('en_core_web_lg')
### The text we want to examine
text = """ sobre Washington de Wikipedia"""

### Parse the text with spaCy
### Our 'document' variable now contains a parsed version of text.
document = nlp(text)

### Extracting semi-structured statements
statements = textacy.extract.semistructured_statements(document, "Washington")

print("**** Information from Washington's Wikipedia page ****")
count = 1
for statement in statements:
subject, verb, fact = statement
print(str(count) + " - Statement: ", statement)
print(str(count) + " - Fact: ", fact)
count += 1
```

## Discurso (semántica más allá de oraciones individuales)

### Coreference resolution (agrupacion de palabras relacionadas)
Dada una oración o un fragmento de texto más grande, determina qué palabras ("menciones") se refieren a los mismos objetos ("entidades"). La resolución de anáforas es un ejemplo específico de esta tarea, y se ocupa específicamente de hacer coincidir los pronombres con los sustantivos o nombres a los que se refieren. La tarea más general de la resolución de correferencia también incluye la identificación de las llamadas "relaciones puente" que involucran expresiones de referencia.. Por ejemplo, en una oración como "Entró a la casa de John por la puerta de entrada", "la puerta de entrada" es una expresión de referencia y la relación puente que debe identificarse es el hecho de que la puerta a la que se hace referencia es la puerta de entrada de John. casa (en lugar de alguna otra estructura a la que también se podría hacer referencia). 

### Discourse analysis

Esta rúbrica incluye varias tareas relacionadas. Una tarea es analizar el discurso, es decir, identificar la estructura del discurso de un texto conectado, es decir, la naturaleza de las relaciones discursivas entre oraciones (p. Ej. Elaboración, explicación, contraste). Otra tarea posible es reconocer y clasificar los actos de habla en un fragmento de texto (por ejemplo, pregunta de sí-no, pregunta de contenido, afirmación, afirmación, etc.). 

### Implicit semantic role labelling

Dada una sola oración, identifique y elimine la ambigüedad de los predicados semánticos (p. Ej., Marcos verbales ) y sus roles semánticos explícitos en la oración actual (consulte Etiquetado de roles semánticos más arriba). Luego, identifique los roles semánticos que no se realizan explícitamente en la oración actual, clasifíquelos en argumentos que se realicen explícitamente en otras partes del texto y aquellos que no están especificados, y resuelva los primeros contra el texto local. Una tarea estrechamente relacionada es la resolución de anáforas cero, es decir, la extensión de la resolución de correferencia a lenguajes pro-drop . 

### Recognizing textual entailment (reconomicimiento de vinculacion textual)

Dados dos fragmentos de texto, determine si uno es verdadero implica al otro, implica la negación del otro o permite que el otro sea verdadero o falso. 

### Topic segmentation and recognition (segmentación y reconocimiento de temas)

Dado un fragmento de texto, sepárelo en segmentos, cada uno de los cuales esté dedicado a un tema, e identifique el tema del segmento. 

### Argument mining

El objetivo de la minería de argumentos es la extracción e identificación automática de estructuras argumentativas del texto en lenguaje natural con la ayuda de programas de computadora. Tales estructuras argumentativas incluyen la premisa, las conclusiones, el esquema del argumento y la relación entre el argumento principal y secundario, o el argumento principal y el contraargumento dentro del discurso. 


--- 

