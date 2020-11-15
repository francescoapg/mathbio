[<<Home](https://francescoapg.github.io/mathbio/)

## Teoría de Conjuntos

**Índice**

1. [Introducción](#intro)
2. [Conjuntos contables](#countable)
3. [Axioma de elección (AC)](#choice)
4. [Conjuntos bien ordenados](#wellordered)
5. [Inducción transfinia](#transfinite)
6. [Números cardinales](#cardinal)

### Introducción {#intro}

Empezamos con las siguientes definiciones:

1. El símbolo <img src="https://render.githubusercontent.com/render/math?math=\in"> representa pertenencia, formalmente, es una relación entre un elemento y el conjunto que lo contiene. Por ejemplo, <img src="https://render.githubusercontent.com/render/math?math=\large a\in S"> significa que <img src="https://render.githubusercontent.com/render/math?math=\large a">
es un elemento de <img src="https://render.githubusercontent.com/render/math?math=\large S">. También se utiliza el símbolo <img src="https://render.githubusercontent.com/render/math?math=\notin"> para representar que un elemento **no** está en un conjunto.
2. Un conjunto se define de la siguiente manera: <img src="https://render.githubusercontent.com/render/math?math=\large A=\{x:P(x)\}">, donde <img src="https://render.githubusercontent.com/render/math?math=\large x"> representa a los elementos del conjunto y <img src="https://render.githubusercontent.com/render/math?math=\large P(x)"> significa que sus elementos cumplen la propiedad <img src="https://render.githubusercontent.com/render/math?math=\large P">. Todo junto se lee "A es un set cuyos elementos (<img src="https://render.githubusercontent.com/render/math?math=\large x">) cumplen <img src="https://render.githubusercontent.com/render/math?math=\large P(x)">".

Con estas dos definiciones ya podemos definir algunas otras relaciones y operaciones. Un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large B"> es _subconjunto_ de <img src="https://render.githubusercontent.com/render/math?math=\large A"> si se cumple lo siguiente: <img src="https://render.githubusercontent.com/render/math?math=\large b \in B \Rightarrow b \in A">, en otras palabras, todo elemento de <img src="https://render.githubusercontent.com/render/math?math=\large B"> está en <img src="https://render.githubusercontent.com/render/math?math=\large A">. Esta relación se representa con el símbolo <img src="https://render.githubusercontent.com/render/math?math=\subset">, entonces, el enunciado anterior es equivalente a <img src="https://render.githubusercontent.com/render/math?math=\large B\subset A">.

Dicho esto, la _equivalencia de conjuntos_ se define como: <img src="https://render.githubusercontent.com/render/math?math=\large A=B\iff A\subset B \land B\subset A">. Con este concepto se hace una distinción entre subconjuntos y subconjuntos propios, un subconjunto propio es aquel subconjunto que no es equivalente al conjunto relacionado, es decir, si <img src="https://render.githubusercontent.com/render/math?math=\large B"> del ejemplo anterior fuese un subconjunto propio, debería existir algún elemento en <img src="https://render.githubusercontent.com/render/math?math=\large A"> que no pertenezca a <img src="https://render.githubusercontent.com/render/math?math=\large B">.

A continuación, definiremos la unión de dos conjuntos, la cual se representa de la siguiente manera: <img src="https://render.githubusercontent.com/render/math?math=\large A\cup B = \{x:x\in A \lor x\in B\}">. La definición de intersection es similar: <img src="https://render.githubusercontent.com/render/math?math=\large A\cap B = \{x:x\in A \land x\in B\}">.

La teoría de conjuntos pasó a su era moderna a inicios de 1960 con la aparición de los métodos de forzado  y el descubrimiento de la relación entre números cardinales grandes y los conjuntos construíbles. Los métodos de forzado (_forcing methos_) son útiles para probar **consistencia** e **independencia** de resultados. La independencia se puede entender como la improbabilidad de una sentencia a partir de otras.

- Herrlich, H. (2006). Axiom of choice. Berlin: Springer.
- Herstein, I. N. (1975). Topics in algebra. Second edition. Xerox Corporation.

### Conjuntos contables {#countable}

Dos conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large A">, <img src="https://render.githubusercontent.com/render/math?math=\large B"> son **equinúmeros** o tienen la misma **cardinalidad** (<img src="https://render.githubusercontent.com/render/math?math=\large A\equiv B">) si existe un mapa bijectivo de <img src="https://render.githubusercontent.com/render/math?math=\large A"> hacia <img src="https://render.githubusercontent.com/render/math?math=\large B">.

Un set es finito si existe una bijección desde un subconjunto propio de los naturales hacia <img src="https://render.githubusercontent.com/render/math?math=\large A">; caso contrario, llamamos a <img src="https://render.githubusercontent.com/render/math?math=\large A">, infinito. Un conjunto es llamado **contable** si es finito o si existe una biyección de los naturales (todo el conjunto) a <img src="https://render.githubusercontent.com/render/math?math=\large A">; si no es contable, <img src="https://render.githubusercontent.com/render/math?math=\large A"> es incontable.

**Teorema**: La unión (finita o infinita) de conjuntos contables es contable.

**Teorema**: (Cantor) Para cualquier par de números reales <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b">, con <img src="https://render.githubusercontent.com/render/math?math=\large a<b">, el intervalo <img src="https://render.githubusercontent.com/render/math?math=\large [a,b]"> es incontable.

La prueba de este teorema es dada por Cantor. Un conjunto de interés es <img src="https://render.githubusercontent.com/render/math?math=\large Y^X">, definido como el conjunto de todas las funciones de <img src="https://render.githubusercontent.com/render/math?math=\large X"> a <img src="https://render.githubusercontent.com/render/math?math=\large Y">.

Definimos una relación <img src="https://render.githubusercontent.com/render/math?math=\large \leq_c"> entre conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> si existe una función inyectiva de <img src="https://render.githubusercontent.com/render/math?math=\large A"> a <img src="https://render.githubusercontent.com/render/math?math=\large B"> (no tiene que ser _onto_ (suryectiva)). En lenguaje normal, <img src="https://render.githubusercontent.com/render/math?math=\large A\leq_c B"> si la cardinalidad de <img src="https://render.githubusercontent.com/render/math?math=\large A"> es menor o igual que la cardinalidad de <img src="https://render.githubusercontent.com/render/math?math=\large B">. También podemos definir <img src="https://render.githubusercontent.com/render/math?math=\large <_c"> entre <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> si <img src="https://render.githubusercontent.com/render/math?math=\large A\leq_c B"> y no se cumple que <img src="https://render.githubusercontent.com/render/math?math=\large A\equiv B">.

**Teorema**: (Cantor) Para cualquier conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=X%3C_c%5Cmathcal%7BP%7D(X)">.

**Teorema de Schröder-Bernstein**: Para cualquier par de conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large Y">, 

<img src="https://render.githubusercontent.com/render/math?math=X%5Cleq_cY%5Cland%20Y%5Cleq_cX%5CRightarrow%20X%5Cequiv%20Y">

La prueba fue inicialmente dada por Cantor y luego por Dedekind.

**Referencias**

- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.

### Axioma de elección (AC) {#choice}

**AC**: Para toda familia <img src="https://render.githubusercontent.com/render/math?math=\large (X_i)_{i\in I}"> de conjuntos no vacíos <img src="https://render.githubusercontent.com/render/math?math=\large X_i">, el conjunto producto <img src="https://render.githubusercontent.com/render/math?math=\large \Pi_{i\in I}X_i"> es no vacío.

Los elementos del conjunto producto (<img src="https://render.githubusercontent.com/render/math?math=\large \Pi_{i\in I}X_i">) son **función de elección** (<img src="https://render.githubusercontent.com/render/math?math=\large X:I\to\cup_{i\in I}X_i">).

Recuerda que el producto cartesiano de una familia <img src="https://render.githubusercontent.com/render/math?math=\large (E_i)_{i\in I}"> es definido como <img src="https://render.githubusercontent.com/render/math?math=\large \Pi_{i\in I}E_i=\{(x_i)_{i\in I}: \forall i \in I, x_i\in E_i\}">.

La existencia del axioma de elección es debatible. Hay muchos problemas cuando lo consideramos válido; sin embargo, hay más problemas cuando no lo consideramos; por lo que de momento se considera como necesario (útil pero no válido). Los constructivistas la evitan, ya que afirma la existencia de entidades elusivas (lo único que sabes es que existen). Una de las consecuencias es la **paradoja de Banach-Tarski**, la cual es extremadamente contraintuitivo. 

**Teorema**: Si <img src="https://render.githubusercontent.com/render/math?math=\large X"> es infinito y <img src="https://render.githubusercontent.com/render/math?math=\large A\subseteq X "> es finito, entonces <img src="https://render.githubusercontent.com/render/math?math=\large X \setminus A"> y <img src="https://render.githubusercontent.com/render/math?math=\large X"> tienen la misma cardinalidad.

Una función parcial es una función cuyo dominio es un subconjunto del conjunto de partida. Dadas dos funciones parciales <img src="https://render.githubusercontent.com/render/math?math=\large f"> y <img src="https://render.githubusercontent.com/render/math?math=\large g"> definidas en los mismos conjuntos de partida y llegada, <img src="https://render.githubusercontent.com/render/math?math=\large f"> extiende a <img src="https://render.githubusercontent.com/render/math?math=\large g"> (f\succeq g) si el dominio de <img src="https://render.githubusercontent.com/render/math?math=\large f"> incluye al dominio de <img src="https://render.githubusercontent.com/render/math?math=\large g"> y <img src="https://render.githubusercontent.com/render/math?math=\large f(x)=g(x) \forall x \in dominio(g)">. Si <img src="https://render.githubusercontent.com/render/math?math=\large A"> es el dominio de <img src="https://render.githubusercontent.com/render/math?math=\large g">, se dice que <img src="https://render.githubusercontent.com/render/math?math=\large g"> es una restricción de <img src="https://render.githubusercontent.com/render/math?math=\large f"> o <img src="https://render.githubusercontent.com/render/math?math=\large f=g_{|A}">.

Un conjunto linealmente ordenado es llamado **orden denso** si para cada <img src="https://render.githubusercontent.com/render/math?math=\large x<y">, existe un <img src="https://render.githubusercontent.com/render/math?math=\large z"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large x<z<y">. Dos conjuntos linealmente ordenados son llamados **isomórficos en orden** o, simplemente, isomórficos si existe un mapeo biyectivo de uno a otro.

**Lema de Zorn**: Si <img src="https://render.githubusercontent.com/render/math?math=\large P"> es un conjunto no vacío parcialmente ordenado tal que cada cadena en <img src="https://render.githubusercontent.com/render/math?math=\large P"> tiene un límite superior en <img src="https://render.githubusercontent.com/render/math?math=\large P">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large P"> tiene un elemento maximal.

**Hipótesis del continuo**: (Cantor) No existe conjunto cuya cardinalidad este entre los enteros y los números reales.

También se sabe que los números racionales se relacionan 1-1 con los enteros. La hipótesis del continuo plantea que los números reales tienen la mínima cardinalidad posible que sea mayor a la de los enteros. Además, los números relaes son equinúmeros con el conjunto potencia de los enteros, expresado en números de aleph, <img src="https://render.githubusercontent.com/render/math?math=%7C%5CR%7C%3D2%5E%7B%5Caleph_0%7D">. La generalización de la hipótesis del continuo es, siendo <img src="https://render.githubusercontent.com/render/math?math=\large \lambda"> un cardinal infinito, <img src="https://render.githubusercontent.com/render/math?math=\large \nexists k (\lambda < |k| < 2^\lambda)">.

**Teorema**: Para cualquier par de conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large Y">, al menos uno de los siguientes se mantienen <img src="https://render.githubusercontent.com/render/math?math=\large X\leq_c Y"> o <img src="https://render.githubusercontent.com/render/math?math=\large Y\leq_c X">.

**Teorema**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large A"> un conjunto finito y <img src="https://render.githubusercontent.com/render/math?math=\large X"> un conjunto infinito, <img src="https://render.githubusercontent.com/render/math?math=\large X\times A \equiv X">.

Esto también parece cumplirse cuando <img src="https://render.githubusercontent.com/render/math?math=\large A=X">.

**Proposición**: (König) Sean <img src="https://render.githubusercontent.com/render/math?math=\large \{X_i:i\in I\}"> y <img src="https://render.githubusercontent.com/render/math?math=\large \{Y_i:i\in I\}"> familias de conjuntos, tal que <img src="https://render.githubusercontent.com/render/math?math=\large X_i\leq_c Y_i"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large i\in I">. Entonces no existe un mapeo suryectivo de <img src="https://render.githubusercontent.com/render/math?math=\large \cup_iX_i"> a <img src="https://render.githubusercontent.com/render/math?math=\large \Pi_iY_i">.

**Referencias**

- Herrlich, H. (2006). Axiom of choice. Berlin: Springer.
- König, J. (1905). Zum Kontinuum-Problem.
- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.


### Conjuntos bien ordenados {#wellordered}

Un buen ordenamiento en un conjunto es un orden lineal (total) tal que todo subconjunto no vacío <img src="https://render.githubusercontent.com/render/math?math=\large A"> de él tiene un límite inferior en <img src="https://render.githubusercontent.com/render/math?math=\large A">. 

Todo orden lineal en un conjunto finito es un buen ordenamiento.

**Principio del buen ordenamiento**: Todo conjunto puede ser bien ordenado.

Sin embargo, el continuo no está bien ordenado.

### Inducción transfinita {#transfinite}

**Prueba por inducción**: Para cada <img src="https://render.githubusercontent.com/render/math?math=\large n\in \mathbb{N}">, sea <img src="https://render.githubusercontent.com/render/math?math=\large P_n"> una proposición matemática. Supón que <img src="https://render.githubusercontent.com/render/math?math=\large P_0"> es verdadero y que para cualquier <img src="https://render.githubusercontent.com/render/math?math=\large n">, <img src="https://render.githubusercontent.com/render/math?math=P_%7Bn%2B1%7D"> es cierto siempre que <img src="https://render.githubusercontent.com/render/math?math=\large P_n"> es cierto. Entonces, parar cada <img src="https://render.githubusercontent.com/render/math?math=\large n">, <img src="https://render.githubusercontent.com/render/math?math=\large P_n"> es verdadero. En lógica, <img src="https://render.githubusercontent.com/render/math?math=(P_0%5Cland%20%5Cforall%20n%20(P_n%5CRightarrow%20P_%7Bn%2B1%7D))%5CRightarrow%20%5Cforall%20n%20(P_n)">.

Esta proposición se prueba por el buen ordenamiento de los naturales.

**Definición por inducción**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> cualquier conjunto no vacío. Supón que <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> es un punto fijo de <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large g"> es un mapeo cualquiera <img src="https://render.githubusercontent.com/render/math?math=\large g:X\to X">. Entonces, existe un mapeo único <img src="https://render.githubusercontent.com/render/math?math=\large f:\mathbb{N}\to X"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large f(0)=x_0"> y <img src="https://render.githubusercontent.com/render/math?math=f(n%2B1)%3Dg(f(n))"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large n">.

**Prueba por inducción transfinita**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large (W,\leq)"> un conjunto bien ordenado, sea <img src="https://render.githubusercontent.com/render/math?math=\large P(w)"> una proposición matemática respecto a <img src="https://render.githubusercontent.com/render/math?math=\large w\in W">. Supón que <img src="https://render.githubusercontent.com/render/math?math=\large \forall w \in W (P(v) \forall v<w)\Rightarrow P(w) "> Entonces, <img src="https://render.githubusercontent.com/render/math?math=\large P(w)"> es cierto para todo elemento de <img src="https://render.githubusercontent.com/render/math?math=\large W">.

34/274

**Referencias**

- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.

### Números cardinales {#carinal}

**Alephs**

Un conjunto tiene cardinalidad  <img src="https://render.githubusercontent.com/render/math?math=\large \aleph_0"> si y solo si es contable infinito, es decir, si existe una biyeccoón entre dicho cojunto y los números naturales. Los siguientes son <img src="https://render.githubusercontent.com/render/math?math=\large \aleph_0">

- Números impares
- Números pares
- Números primos
- Números compuestos
- Enteros
- Racionales
- El conjunto de todos los subconjuntos finitos de cualquier conjunto infinito contable.

<img src="https://render.githubusercontent.com/render/math?math=\large \aleph_1"> es la cardinalidad del conjunto de todos los números ordinales contables, dicho conjunto (<img src="https://render.githubusercontent.com/render/math?math=\large \omega_1">) es incontable.

