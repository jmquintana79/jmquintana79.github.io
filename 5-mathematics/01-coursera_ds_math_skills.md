---
title: DS Math skills
parent: Matematicas
has_children: false
nav_order: 5
keywords:
    - Coursera
    - Mathematics
    - Probability
    - Algebra
    - Note
---

---
# [Data Science Math Skills (Coursera)](https://www.coursera.org/learn/datasciencemathskills/home/welcome)

- Instructors: Daniel Egger, Paul Bendich.
- Duke University.
- Complited on: **19 de junio de 2020**.

---

# Algebra

## Teoria basica de conjuntos:
- *Set*: conjunto de elementos.
- *Cardinalidad*: numero de elementos de un conjunto.
- **Definicion / matematizacion de un problema**:
	- definir los conjuntos segun caracteristicas / elementos.
	- definir los conjuntos de union e interseccion.
	- obtener las cardinalidades y proporciones (rates) de cardinalidades de conjuntos, uniones e intersecciones.
- Diagramas de Venn. *Inclusion-exclusion formula*: 
`card(A union B) = card(A) + card(B) - card(A inter B)`


## Numeros Reales:
- Recta Real. Mas importante division de num R (en cero): positivos, negativos.
- Valor absoluto: abs(x) = x, -x --> valores con misma distancia a cero.
- Desigualdades. **Algebra con desigualdades**:
    - SUMA: `If a < b, then a + c < b + c`.*Ej. x + 3 < 10 --> x < 7*
    - PRODUCTO: 
   ```
   Suppose a < b,
   If c > 0, then a · c < b · c.
   If c < 0, then a · c > b · c
 ```  *Ej. -2x < 10 --> x > -5*
- Intervalos abiertos, cerrados. Rays: cerrado por un lado, hacia +/- infinito por el otro. *Ej. 1 <= x + 5 < 10 --> -4 <= x < 5 --> x pertenece a [-4,5)*


## Sumatorios:
- Definicion.
- Reglas de manipulacion/simplificación: prop. distributiva. 
- Sea X = {x1, x2, ... , xn}
    - media: `mu_x = (1/n) * SUM(i=1,n) xi`
    - varianza: `(sigma_x)^2 = (1/n) * SUM(i=1,n) (xi - mu_x)^2` 
    

# Functions and Graphs

## Plano Cartesiano
- Espacio Euclideo R2. 
- **Distancia Euclidean**: `d(P1,P2) = sqrt( (x2-x1)^2 + (y2-y1)^2 )`
- **point-slope line**: `y - y0 = m * (x - x0)` 
- **slope-intercept line**: `y = m * x + b`
  
## Funciones
- A function *f: A → B* is a rule/formula/machine that transforms each element *a∈A* into *f(a)∈B*.
- Sea una funcion *f : R → R*,
    - f is **strictly increasing** if whenever *a < b*, we have *f(a) < f(b)*.
    - f is **strictly decreasing** if whenever *a < b*, we have *f(a) > f(b)*.
-  Composicion de funciones:
    -  Definition: Given functions f and g, `(g ◦ f)(x) = g(f(x)), and (f ◦ g)(x) = f(g(x))`
    -  f and g are inverses of each other si `(g ◦ f)(x) = (f ◦ g)(x)`. Esto solo sucede para funciones extrictamente creciente / decrecientes.


# Measuring Rates of Change

## Definicion de derivada en un punto
- Funciones **extrictamente crecientes / decrecientes**.
- **Pendiente de la tangente** de una función en un punto *a* es la derivada de dicha función evaluada en *a*:
```
f'(a) = lim (h --> 0) ( f(a+h) - f(a) / h )
```

## Potencias / Logaritmos

#### Reglas de simplificación Potencias
```
(x^n) * (x^m) = x^(m+n)
(x^n) / (x^m) = x^(m-n)
(x^n)^m = x^(m*n)
```
#### Logaritmos

- *x = N  <--> log b (N) = x 8.** Por tanto, el logaritmo tiene como tarea encontrar el exponente. 
- log b (1) siempre igual a 0 independientemente del valor de b.
- Reglas simplificación Logaritmos:
```
log(x*y) = log(x) + log(y)
log(x/y) = log(x) - log(y)
log(x^n) = n * log(x)
```
- **Cambio de base de logaritmos:**
    - Sea "b" la vieja base y "a" la nueva base, entonces: `log a (x) = ( log b (x) / log b (a) )`
- **Rates de crecimiento exponencial:**
   - discreto
   - continuo: Euler's constant = número "e" = 2.71828
      - descubierto en el estudio del interés compuesto, problema abordado por Jacob Bernoulli en 1683.
      `lim (n --> infinito) (1 + (1/n))^n = e`
      - crecimiento continuo: `Poblacion_final = Poblacion_inicil * e^(rate*tiempo)` donde rate = (porcentaje de cambio por unidad de tiempo/100)
      - por decirlo así, cuando usamos como base el número e estamos pasando al mundo continuo, o del crecimiento continuo donde con buena aproximación podemos decir que estamos definiendo un crecimiento con la máxima resolución posible.
  - **Logaritmo Neperaiano:** *log e (x) = ln(x)* = logaritmo neperiano ó natural = natural log


# Introduction to Probability Theory

## PROBABILIDAD:
- *Probabilidad*: grado de creencia en la verdad (o falsedad) de una declaración.
- *Probabilidad = {0, 1}* --> verdadero / falso con certeza.
- *Probabilidad = (0 ,1)* (conjunto abierto) --> rango de incertidumbre.
> Ej. declaración (statement) = "hoy va a llover" --> probabilidad entre 0 y 1.
- **Law of excluded middle**: `P(X) + P(~X) = 1`
> Por ejemplo, dos staments *x1=x="hoy llueve"* y* x2=~X="hoy no llueve"* ya forman una Distribución de Probabilidad.
- Sea una distribucion (coleccion de statments) con todos los posibles statements *X = {x1,...,xn}*. Entonces se tiene que cumplir:
`P(x1)+...+P(xn)=1`
	- *Exclusive*: dado toda la informacion (todos los staments posibles) no mas de uno puede ser True (P=1).
	- *Exhaustive*: dada toda la informacion al menos uno debe ser True.
- **NOTACION**: Dado *X = {x1,...,xn}*
	- *xi*: statment --> *P(xi)*
	- *X*: es la coleccion de statements que puede ser exclusive y exhustive (=*mutuamente excluyente*) --> `P(X) = sum(P(xi)) = 1` -->***si es mutuamente excluyente entonces X es distribucion de probabilidad = probability distribution**.
- **Otra definicion de probabilidad**:
```
P(event A) = num. de veces que el evento A ocurre / num. de todos los eventos
```

## JOINT PROBABILITIES:

- **joint probability = AND probability = probabilidad de interseccion (diagramas de Venn) = P(A,B) = P( A is True AND B is True).**
- Dados *X={x1,...,xn}* e *Y = {y1,...,yn}*, entonces:
    - *P(X,Y) = P(Y,X)* 
    - y por ejemplo *P(x1,y1) = P(y1,x1)*
- **Definicion de INDEPENDENCIA**:
    - Si dos sucesos son independientes : `P(xi, yi) = P(xi) * P(yi)`, es decir,  por ejemplo, el echo de que *yi* sea True o False no influye para que *xi* sea True o no.
- **OR probability = probabilidad de la union:** `P(A OR B) = P(A) + P(B) - P(A,B)` 


## COMBINATORIA:
- **Permite calcular probabilidades cuando contar es demasiado tedioso.**
- El orden de los elementos en el grupo formado importa o no: *permutaciones (importa)* / *combinaciones (no importa)*.
- **Con replacement (reemplazo)** --> eventos independientes --> orden de toma de datos no importa.
- **Sin replacement** --> eventos dependientes --> orden de toma de datos si importa.
- *Factorial*: *0!=1*
- **Numero de grupos distintos con m elementos tomados de n en n sin replacement:** 
```
combinations (m, n) = m! / (m-n)! n!
```

## SUM RULE:
- **Sum rule = joint probability + marginal probabilities**.
- Sea *X = {x1, x2} y Y = {y1, y2}*. Las *joint probabilities* (intersecciones) *P(x1, y1)*, *P(x2, y1)*, *P(x1, Y2)*, *P(x2,y2)* podrían ser representadas en una tabla *x1, x2 / y1, y2*. Por tanto las Probabilidades Marginales serían:
```
P(x1) = P(x1,y1)+P(x1,y2)
P(x2) = P(x2,y1)+P(x2,y2)
P(y1) = P(x1,y1)+P(x2,y1)
P(y2) = P(x1,y2)+P(x2,y2) 
``` 
y esta suma es la que llamamos **Sum Rule**.
```
     X:
         x1         x2
Y:   y1  P(x1,y1)   P(x2, y1) 
     y2  P(x1,y2)   P(x2, y2)
```
- En el caso de ser un *binary* tendríamos por ej: `P(A) = P(A, B) + P(A, ~B)`.


## CONDITIONAL PROBABILITY:
- **P(A ¦ B) = probabilidad de que A sea True sabiendo que B es True = relevant outcomes / total outcomes in Universe when B is True.**
- `P(A ¦ B) = P(A,B) / P(B)` = Product Rule tal que P(B) es la probabilidad marginal de B.
- **Nueva definicion de Independencia entre dos sucesos**: `P(A ¦ B) = P(A)`.


## TEOREMA de BAYES:

- Teorema de Bayes:
```
P(Ai ¦ B) = P(B ¦ Ai) * P(Ai) / P(B)
```
donde `P(B) = P(B,A1) + P(B,A2) = P(B ¦ A1) * P(A1) + ... + P(B ¦ An) * P(An)` y donde *P(Ai) = prior probability*.
- Es para tipo de problema inverso:
```
 P(parameter process ¦ observed outcome) = P(observed outcome ¦ parameter process) * P(parameter processs) / P(observed outcome)
```
donde para calcular P(observed outcome) hay que usar la regla de la suma para el calculo de prob marginal del observed outcome.
- Lo  mas poderoso de Bayes es que se puede adaptar las probabilidades con nuevos datos, es decir se puede reemplantear el problema usando como Prior probabilities las obtenidas previamente.

> Ej. yo tengo dos urnas. En la primera obtener bola blanca es del 20% y en la segunda es del 10%. Si yo saco de una de las urnas y obtengo 3 blancas, probabilidad de ser de la urna 1? probabilidad de la urna 2?. EN ESTE PROBLEMA SABEMOS EL RESULTADO OBSERVADO (3 BLANCAS) PERO NO SABEMOS EL PROCESO (SI ES DE LA URNA 1 O 2 PARA OBTENER ESE OUTPUT).

- Por tanto, en `P(Oi ¦ D) = P(D ¦ Oi) * P(Oi) / P(D)`
    - *P(Oi ¦ D)* = **posterior probability**.
    - *P(Oi)* = **prior probability**.
    - *P(D ¦ Oi)* = **likehood**.
    - *P(D)* = **marginal probability**.
- Es decir nos permite ver la probabilidad de que una observacion (B) ocurreo por un proceso (A1) u otro (A2).


## THE BINOMIAL THEOREM AND BAYES THEOREM:
- **Se llama binomial porque solo hay dos posibles outcomes (success, non-success)**.
- Sea _P(x)_ la probabilidad de tener exactamente _s_ éxitos entre _n_ intentos o ensayos:
```
P(x) = (n s) * p^s (1-p)^(n-s)
```
donde:
- n = number of independent trials (with replacement)
- s = number of success / n - s = number of failures
- p = probability of success / 1 - p = q = probability of failure


> El problema de tirar moneda se puede usar con Bayes tomando B como un resultado observado, A1 binomial con una moneda "justa", A2 con una moneda trucada. 

