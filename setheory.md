[<<Home](https://francescoapg.github.io/mathbio/)

## Teoría de Conjuntos

Esta teoría ve la luz en 1874, con el trabajo del matemático aleman Georg Cantor (1845-1918) titulado "Ueber eine Eigenschaft des Inbegriffs aller reellen algebraischen Zahlen". Entre las áreas de estudio en la actualidad se encuentran

- Combinatorial set theory
- Descriptive set theory
- Fuzzy set theory
- Inner model theory
- Forcing

entre otras.

### Conceptos preliminares

Antes de iniciar con el estudio de esta teoría, es necesario tener algunos conceptos de lógica matemática claros. Entre ellos, recordar que una **fórmula** (abreviación de fórmula bien formulada o _well-formed formula_) es una cadena de caracteres (elementos de un alfabeto) que siguen o cumplen con una gramática formal. El conjunto de todas las fórmulas es el **lenguaje formal**. Como ejemplo, un **teorema** es fórmula de cierta importancia en el lenguaje formal. Finalmente, una fórmula puede tener variables libres o no, una fórmula sin variables libres es conocida como una _sentence_. En el caso de las fórmulas con variables libres, se suele adoptar la notación <img src="https://render.githubusercontent.com/render/math?math=\large \phi(p_1,...,p_n)">, donde <img src="https://render.githubusercontent.com/render/math?math=\large p_1,...,p_n"> son las variables.

La teoría de conjuntos usa **fórmulas atómicas** para construir todas las fórmulas de la teoría. Estas fórmulas atómicas son <img src="https://render.githubusercontent.com/render/math?math=\large x\in y"> y <img src="https://render.githubusercontent.com/render/math?math=\large x=y">, el resto de fómulas se construye con la ayuda de conectores y cuantificadores. Los conectores son:

- Negación: <img src="https://render.githubusercontent.com/render/math?math=\large \neg\phi">.
- Conjunción: <img src="https://render.githubusercontent.com/render/math?math=\large \phi\land\psi">.
- Disyunción: <img src="https://render.githubusercontent.com/render/math?math=\large \phi\lor\psi">.
- Implicancia: <img src="https://render.githubusercontent.com/render/math?math=\large \phi\implies\psi">.
- Equivalencia: <img src="https://render.githubusercontent.com/render/math?math=\large \phi\iff\psi">.

Mientras que los cuantificadores son:

- Universal: <img src="https://render.githubusercontent.com/render/math?math=\large \forall x\phi">.
- Existencial: <img src="https://render.githubusercontent.com/render/math?math=\large \exists x\phi">.

El uso de formulas atómicas, conectores y cuantificadores se conoce como **lógica de primer orden** (first-order logic) y es el corazón de la teoría de conjuntos; la lógica de primer orden tiene como base al **cálculo proposicional** que usa únicamente fórmulas y conectores. En una nota complementaria, a partir de la lógica de primer orden se extiende la **lógica de segundo orden** y, a su vez, la **lógica de orden superior**. Las bases del cálculo proposicional o lógica proposicional son  las siguientes:

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bmatrix%7D%0A%5Cpsi%20%26%20%5Cneg%5Cpsi%5C%5C%0AV%20%26%20F%5C%5C%0AF%20%26%20V%5C%5C%0A%20%26%20%20%5C%5C%0A%20%26%20%20%20%0A%5Cend%7Bmatrix%7D">

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bmatrix%7D%0A%5Cpsi%20%26%20%5Cphi%20%26%20%5Cpsi%5Cland%5Cphi%5C%5C%0AV%20%26%20V%20%26%20V%5C%5C%0AV%20%26%20F%20%26%20F%5C%5C%0AF%20%26%20V%20%26%20F%5C%5C%0AF%20%26%20F%20%26%20F%0A%5Cend%7Bmatrix%7D">

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bmatrix%7D%0A%5Cpsi%20%26%20%5Cphi%20%26%20%5Cpsi%5Clor%5Cphi%5C%5C%0AV%20%26%20V%20%26%20V%5C%5C%0AV%20%26%20F%20%26%20V%5C%5C%0AF%20%26%20V%20%26%20V%5C%5C%0AF%20%26%20F%20%26%20F%0A%5Cend%7Bmatrix%7D">

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bmatrix%7D%0A%5Cpsi%20%26%20%5Cphi%20%26%20%5Cpsi%5Cimplies%5Cphi%5C%5C%0AV%20%26%20V%20%26%20V%5C%5C%0AV%20%26%20F%20%26%20F%5C%5C%0AF%20%26%20V%20%26%20V%5C%5C%0AF%20%26%20F%20%26%20V%0A%5Cend%7Bmatrix%7D">

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bmatrix%7D%0A%5Cpsi%20%26%20%5Cphi%20%26%20%5Cpsi%5Ciff%5Cphi%5C%5C%0AV%20%26%20V%20%26%20V%5C%5C%0AV%20%26%20F%20%26%20F%5C%5C%0AF%20%26%20V%20%26%20F%5C%5C%0AF%20%26%20F%20%26%20V%0A%5Cend%7Bmatrix%7D">

Con estos conceptos claros, veamos algunas formas de argumento generalmente usadas,

**Modus ponendo ponens**: <img src="https://render.githubusercontent.com/render/math?math=((P%5Cimplies%20Q)%5Cland%20P)%5Cimplies%20Q">.

**Modus tollendo tollens**: <img src="https://render.githubusercontent.com/render/math?math=((P%5Cimplies%20Q)%5Cland%20%5Cneg%20Q)%5Cimplies%20%5Cneg%20P">. 

**Silogismo hipotético**: <img src="https://render.githubusercontent.com/render/math?math=((P%5Cimplies%20Q)%5Cland%20(Q%5Cimplies%20R))%5Cimplies%20(P%20%5Cimplies%20R)">.

**Silogismo disyuntivo**: También llamado Modus tollendo ponens, <img src="https://render.githubusercontent.com/render/math?math=((P%5Clor%20Q)%5Cland%5Cneg%20P)%5Cimplies%20Q">.

**Leyes de Morgan**: La primera es: <img src="https://render.githubusercontent.com/render/math?math=%5Cneg%20(P%5Cland%20Q)%5Cequiv%5Cneg%20P%5Clor%5Cneg%20Q">, mientras que la segunda es: <img src="https://render.githubusercontent.com/render/math?math=%5Cneg%20(P%5Clor%20Q)%5Cequiv%20%5Cneg%20P%5Cland%5Cneg%20Q">.

Finalmente, tanto la conjunción como la disyunción son conmutativas, asociativas y ambos juntos, distributivas. Otros principios lógicos importantes son el **principio de no contradicción** y el **principio del tercero excluído**. El principio de no contradicción establece que una proposición y su negación no pueden ser simultánemanete validas, en el sentido que <img src="https://render.githubusercontent.com/render/math?math=P%5Cland%5Cneg%20P"> es siempre falso o una **contradicción**. El principio del tercero exluído establece que si una proposición establece algo y otra, su negación, entonces no existe una tercera proposición que sea verdadera más allá de las dos primeras, en otras palabras, <img src="https://render.githubusercontent.com/render/math?math=P%5Clor%5Cneg%20P"> es una tautología.


**Referencias**

- Jech, Thomas J. (2003). Set theory. Springer 3rd Millennium ed.

**Índice**

1. [Introducción](#intro)
2. [Conjuntos contables](#countable)
3. [Axiomas de Zermelo-Fraenkel](#ZF)
4. [Axioma de elección (AC)](#choice)
5. [Conjuntos bien ordenados](#wellordered)
6. [Inducción](#induction)
7. [Números cardinales](#cardinal)

### Introducción {#intro}

Empezamos con las siguientes definiciones:

1. El símbolo <img src="https://render.githubusercontent.com/render/math?math=\in"> representa pertenencia, formalmente, es una relación entre un elemento y el conjunto que lo contiene. Por ejemplo, <img src="https://render.githubusercontent.com/render/math?math=\large a\in S"> significa que <img src="https://render.githubusercontent.com/render/math?math=\large a">
es un elemento de <img src="https://render.githubusercontent.com/render/math?math=\large S">. También se utiliza el símbolo <img src="https://render.githubusercontent.com/render/math?math=\notin"> para representar que un elemento **no** está en un conjunto.
2. Un conjunto se define de la siguiente manera: <img src="https://render.githubusercontent.com/render/math?math=\large A=\{x:P(x)\}">, donde <img src="https://render.githubusercontent.com/render/math?math=\large x"> representa a los elementos del conjunto y <img src="https://render.githubusercontent.com/render/math?math=\large P(x)"> significa que sus elementos cumplen la propiedad <img src="https://render.githubusercontent.com/render/math?math=\large P">. Todo junto se lee "A es un set cuyos elementos (<img src="https://render.githubusercontent.com/render/math?math=\large x">) cumplen <img src="https://render.githubusercontent.com/render/math?math=\large P(x)">".

Con estos elementos podemos definir otras relaciones y operaciones. Un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large B"> es _subconjunto_ de <img src="https://render.githubusercontent.com/render/math?math=\large A"> si se cumple lo siguiente: <img src="https://render.githubusercontent.com/render/math?math=\large b \in B \Rightarrow b \in A">, en otras palabras, todo elemento de <img src="https://render.githubusercontent.com/render/math?math=\large B"> está en <img src="https://render.githubusercontent.com/render/math?math=\large A">. Esta relación se representa con el símbolo <img src="https://render.githubusercontent.com/render/math?math=\subset">, entonces, el enunciado anterior es equivalente a <img src="https://render.githubusercontent.com/render/math?math=\large B\subset A">.

Dicho esto, la _equivalencia de conjuntos_ se define como: <img src="https://render.githubusercontent.com/render/math?math=\large A=B\iff A\subset B \land B\subset A">. Con este concepto se hace una distinción entre subconjuntos y subconjuntos propios, un subconjunto propio es aquel subconjunto que no es equivalente al conjunto relacionado, es decir, si <img src="https://render.githubusercontent.com/render/math?math=\large B"> del ejemplo anterior fuese un subconjunto propio, debería existir algún elemento en <img src="https://render.githubusercontent.com/render/math?math=\large A"> que no pertenezca a <img src="https://render.githubusercontent.com/render/math?math=\large B">.

A continuación, definiremos la unión de dos conjuntos, la cual se representa de la siguiente manera: <img src="https://render.githubusercontent.com/render/math?math=\large A\cup B = \{x:x\in A \lor x\in B\}">. La definición de intersection es similar: <img src="https://render.githubusercontent.com/render/math?math=\large A\cap B = \{x:x\in A \land x\in B\}">.

La teoría de conjuntos pasó a su era moderna a inicios de 1960 con la aparición de los métodos de forzado  y el descubrimiento de la relación entre números cardinales grandes y los conjuntos construíbles. Los métodos de forzado (_forcing methods_) son útiles para probar **consistencia** e **independencia** de resultados. La independencia se puede entender como la improbabilidad de una sentencia a partir de otras.

- Herrlich, H. (2006). Axiom of choice. Berlin: Springer.
- Herstein, I. N. (1975). Topics in algebra. Second edition. Xerox Corporation.
- Jech, Thomas J. (2003). Set theory. Springer 3rd Millennium ed.

### Conjuntos contables {#countable}

Dos conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large A">, <img src="https://render.githubusercontent.com/render/math?math=\large B"> son **equinúmeros** o tienen la misma **cardinalidad** (<img src="https://render.githubusercontent.com/render/math?math=\large A\equiv B">) si existe un mapa bijectivo de <img src="https://render.githubusercontent.com/render/math?math=\large A"> hacia <img src="https://render.githubusercontent.com/render/math?math=\large B">.

Un set es finito si existe una bijección desde un subconjunto propio de los naturales hacia <img src="https://render.githubusercontent.com/render/math?math=\large A">; caso contrario, llamamos a <img src="https://render.githubusercontent.com/render/math?math=\large A">, infinito. Un conjunto es llamado **contable** si es finito o si existe una biyección de los naturales (todo el conjunto) a <img src="https://render.githubusercontent.com/render/math?math=\large A">; si no es contable, <img src="https://render.githubusercontent.com/render/math?math=\large A"> es incontable.

Cada conjunto infinito _X_ es _Dedekind_ infinito si y solo si permite una inyección <img src="https://render.githubusercontent.com/render/math?math=%5CN%5Cto%20X">. Cada subconjunto infinito de <img src="https://render.githubusercontent.com/render/math?math=%5CR"> es Dedekind infinito. Todo set infinito linealmente ordenado es Dedekind infinito.

**Teorema**: La unión (finita o infinita) de conjuntos contables es contable.

**Teorema**: (Cantor) Para cualquier par de números reales <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b">, con <img src="https://render.githubusercontent.com/render/math?math=\large a<b">, el intervalo <img src="https://render.githubusercontent.com/render/math?math=\large [a,b]"> es incontable.

La prueba de este teorema es dada por Cantor. Un conjunto de interés es <img src="https://render.githubusercontent.com/render/math?math=\large Y^X">, definido como el conjunto de todas las funciones de <img src="https://render.githubusercontent.com/render/math?math=\large X"> a <img src="https://render.githubusercontent.com/render/math?math=\large Y">.

Definimos una relación <img src="https://render.githubusercontent.com/render/math?math=\large \leq_c"> entre conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> si existe una función inyectiva de <img src="https://render.githubusercontent.com/render/math?math=\large A"> a <img src="https://render.githubusercontent.com/render/math?math=\large B"> (no tiene que ser _onto_ (suryectiva)). En lenguaje normal, <img src="https://render.githubusercontent.com/render/math?math=\large A\leq_c B"> si la cardinalidad de <img src="https://render.githubusercontent.com/render/math?math=\large A"> es menor o igual que la cardinalidad de <img src="https://render.githubusercontent.com/render/math?math=\large B">. También podemos definir <img src="https://render.githubusercontent.com/render/math?math=\large <_c"> entre <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> si <img src="https://render.githubusercontent.com/render/math?math=\large A\leq_c B"> y no se cumple que <img src="https://render.githubusercontent.com/render/math?math=\large A\equiv B">.

**Teorema**: (Cantor) Para cualquier conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=X%3C_c%5Cmathcal%7BP%7D(X)">.

**Teorema de Schröder-Bernstein**: Para cualquier par de conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large Y">, 

<img src="https://render.githubusercontent.com/render/math?math=X%5Cleq_cY%5Cland%20Y%5Cleq_cX%5CRightarrow%20X%5Cequiv%20Y">

La prueba fue inicialmente dada por Cantor y luego por Dedekind.

**Teorema**: Para cualquier par de conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large Y">, al menos uno de los siguientes se mantienen <img src="https://render.githubusercontent.com/render/math?math=\large X\leq_c Y"> o <img src="https://render.githubusercontent.com/render/math?math=\large Y\leq_c X">.

**Teorema**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large A"> un conjunto finito y <img src="https://render.githubusercontent.com/render/math?math=\large X"> un conjunto infinito, <img src="https://render.githubusercontent.com/render/math?math=\large X\times A \equiv X">.

Esto también parece cumplirse cuando <img src="https://render.githubusercontent.com/render/math?math=\large A=X">.

**Referencias**

- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.

### Axiomas de Zermelo-Fraenkel {#ZF}

1. **Axioma de extensionalidad**: Si dos conjuntos tienen los mismos elementos, entonces son iguales.
2. **Axioma de emparejamiento**: Para cada <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b"> existe un conjunto <img src="https://render.githubusercontent.com/render/math?math=%5C%7Ba%2Cb%5C%7D"> que contiene únicamente a ambos.
3. **Esquema del axioma de separación**: Si <img src="https://render.githubusercontent.com/render/math?math=\large P"> es una propiedad, entonces, para cualquier conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X"> y parámetro <img src="https://render.githubusercontent.com/render/math?math=\large p"> (parámetro de <img src="https://render.githubusercontent.com/render/math?math=\large P">), existe un conjunto <img src="https://render.githubusercontent.com/render/math?math=Y%3D%5C%7Bu%5Cin%20X%3AP(u%2Cp)%5C%7D"> que contiene a todos los elementos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> que cumplen la propiedad <img src="https://render.githubusercontent.com/render/math?math=\large P">.
4. **Axioma de unión**: Para cada conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X"> existe un conjunto formado por la unión de todos los elementos de <img src="https://render.githubusercontent.com/render/math?math=\large X">.
5. **Axioma del producto cartesiano**: Para cada conjunto existe un conjunto formado por todos los subconjuntos de dicho conjunto.
6. **Axioma del infinito**: Existe un conjunto infinito.
7. **Esquema del axioma de reemplazo**: Sin una clase <img src="https://render.githubusercontent.com/render/math?math=\large f"> es una función, entonces para cada <img src="https://render.githubusercontent.com/render/math?math=\large X"> existe un conjunto <img src="https://render.githubusercontent.com/render/math?math=Y%3D%5C%7Bf(x)%3Ax%5Cin%20X%5C%7D">.
8. **Axioma de regularidad**: Cada conjunto no vacío contiene al menos un elemento disjunto de sí mismo.

Es importante comentar que el esquema del axioma de separación corresponde a ser una forma débil del esquema del axioma de comprensión. El esquema del axioma de comprensión tiene la forma de "si <img src="https://render.githubusercontent.com/render/math?math=\large P"> es una propiedad, entonces el conjunto <img src="https://render.githubusercontent.com/render/math?math=Y%3D%5C%7Bx%3AP(x)%5C%7D"> existe". Este esquema lleva a la famosa paradoja de Russell, por lo que en **ZF** fue reemplazada por una forma no nociva.

**Referencias**

- Jech, Thomas J. (2003). Set theory. Springer 3rd Millennium ed.

### Axioma de elección (AC) {#choice}

**AC**: Para toda familia <img src="https://render.githubusercontent.com/render/math?math=\large (X_i)_{i\in I}"> de conjuntos no vacíos <img src="https://render.githubusercontent.com/render/math?math=\large X_i">, el conjunto producto <img src="https://render.githubusercontent.com/render/math?math=\large \Pi_{i\in I}X_i"> es no vacío.

Los elementos del conjunto producto (<img src="https://render.githubusercontent.com/render/math?math=\large \Pi_{i\in I}X_i">) son **función de elección**. Esta función de elección se aplica siempre que se use la idea de elegir un elemento.

Recuerda que el producto cartesiano de una familia <img src="https://render.githubusercontent.com/render/math?math=\large (E_i)_{i\in I}"> es definido como <img src="https://render.githubusercontent.com/render/math?math=\large \Pi_{i\in I}E_i=\{(x_i)_{i\in I}: \forall i \in I, x_i\in E_i\}">.

La existencia del axioma de elección es debatible. Hay muchos problemas cuando lo consideramos válido; sin embargo, hay más problemas cuando no lo consideramos; por lo que de momento se considera como necesario (útil pero no válido). Los constructivistas la evitan, ya que afirma la existencia de entidades elusivas (lo único que sabes es que existen). Una de las consecuencias es la **paradoja de Banach-Tarski**, la cual es extremadamente contraintuitivo. 

**Teorema**: Si <img src="https://render.githubusercontent.com/render/math?math=\large X"> es infinito y <img src="https://render.githubusercontent.com/render/math?math=\large A\subseteq X "> es finito, entonces <img src="https://render.githubusercontent.com/render/math?math=\large X \setminus A"> y <img src="https://render.githubusercontent.com/render/math?math=\large X"> tienen la misma cardinalidad.

**Lema de Zorn**: Si <img src="https://render.githubusercontent.com/render/math?math=\large P"> es un conjunto no vacío parcialmente ordenado tal que cada cadena en <img src="https://render.githubusercontent.com/render/math?math=\large P"> tiene un límite superior en <img src="https://render.githubusercontent.com/render/math?math=\large P">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large P"> tiene un elemento maximal.

El Lema de Zorn se prueba que es equivalente a AC. También es equivalente a la **condición de cadena maximal de Hausdorff**, que establece que "cada conjunto parcialmente ordenado contiene una cadena maximal".

**Hipótesis del continuo**: (Cantor) No existe conjunto cuya cardinalidad este entre los enteros y los números reales.

También se sabe que los números racionales se relacionan 1-1 con los enteros. La hipótesis del continuo plantea que los números reales tienen la mínima cardinalidad posible que sea mayor a la de los enteros. Además, los números relaes son equinúmeros con el conjunto potencia de los enteros, expresado en números de aleph, <img src="https://render.githubusercontent.com/render/math?math=%7C%5CR%7C%3D2%5E%7B%5Caleph_0%7D">. La generalización de la hipótesis del continuo es, siendo <img src="https://render.githubusercontent.com/render/math?math=\large \lambda"> un cardinal infinito, <img src="https://render.githubusercontent.com/render/math?math=\large \nexists k (\lambda < |k| < 2^\lambda)">.

**Proposición**: (König) Sean <img src="https://render.githubusercontent.com/render/math?math=\large \{X_i:i\in I\}"> y <img src="https://render.githubusercontent.com/render/math?math=\large \{Y_i:i\in I\}"> familias de conjuntos, tal que <img src="https://render.githubusercontent.com/render/math?math=\large X_i\leq_c Y_i"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large i\in I">. Entonces no existe un mapeo suryectivo de <img src="https://render.githubusercontent.com/render/math?math=\large \cup_iX_i"> a <img src="https://render.githubusercontent.com/render/math?math=\large \Pi_iY_i">.

**Axioma de fundación**: (Axioma de regularidad) Entre los axiomas de teoría de conjuntos ZF, el axioma de fundación establece que <img src="https://render.githubusercontent.com/render/math?math=\large X\neq \emptyset \Rightarrow \exists y (y\in X \land y\cap x = \emptyset)">. Se lee: todo conjunto no vacío es disjunto de uno de sus elementos.

Entre los matemáticos constructivistas, algunos aceptan formas débiles del axioma de elección. Estos son: el axioma de Elección Contable y el Principio de Elección Dependiente. El **Axioma de Elección Contable** establece que para cada secuencia <img src="https://render.githubusercontent.com/render/math?math=(X_n)_%7Bn%5Cin%5CN%7D"> de conjuntos no vacíos <img src="https://render.githubusercontent.com/render/math?math=X_n">, el conjunto producto <img src="https://render.githubusercontent.com/render/math?math=%5CPi_%7Bn%5Cin%5CN%7DX_n"> es no vacío. Existe una variante finita (<img src="https://render.githubusercontent.com/render/math?math=X_n"> finito) de este axioma.

**Axioma de elección multiple**: Para cada familia <img src="https://render.githubusercontent.com/render/math?math=(X_i)_%7Bi%5Cin%20I%7D"> de conjuntos no vacíos <img src="https://render.githubusercontent.com/render/math?math=X_i">, existe una familia <img src="https://render.githubusercontent.com/render/math?math=(F_i)_%7Bi%5Cin%20I%7D"> de subconjuntos finitos no vacíos <img src="https://render.githubusercontent.com/render/math?math=F_i"> de <img src="https://render.githubusercontent.com/render/math?math=X_i">.

**Principio de Elecciones Dependientes**: Para cada par <img src="https://render.githubusercontent.com/render/math?math=(X%2C%5Cdelta)"> cuando _X_ es un conjunto no vacío y <img src="https://render.githubusercontent.com/render/math?math=%5Cdelta"> es una relación en _X_ tal que para cada <img src="https://render.githubusercontent.com/render/math?math=x%5Cin%20X%2C%5Cexists%20y%20%5Cin%20X%20(x%5Cdelta%20y)">. Existe una secuencia <img src="https://render.githubusercontent.com/render/math?math=(X_n)"> en _X_ con <img src="https://render.githubusercontent.com/render/math?math=X_n%5Cdelta%20X_%7Bn%2B1%7D"> para cada <img src="https://render.githubusercontent.com/render/math?math=n%5Cin%20%5CN">.

**Principios de maximalidad**

1. **Teorema del ultrafiltro**: En todo conjunto cualquier filtro puede ser agrandado a un ultrafiltro.
2. **Principio del ultrafiltro débil**: Cada conjunto tiene un ultrafiltro libre.

**Ultrafiltro**: Un filtro que es maximal. Debe cumplir que

1. El vacío no está incluído en un ultrafiltro.
2. Si A y B pertenecen al ultrafiltro, entonces su unión también es un elemento.
3. Si Z está incluído en el ultrafiltro, entonces Z pertenece al ultrafiltro o su complemento en el ultrafiltro pertenece al ultrafiltro.

Los ultrafiltros se dividen en dos clases, los triviales (o fijado o principal) y los libres. Los ultrafiltros triviales son una colección de todos los subconjuntos que contienen a un elemento (el elemento está _fijo_). Los ultrafiltros libres no son fijos a cualquier elemento, para probar la existencia de un ultrafiltro se requiere el axioma de elección.

Para cada filtro hay un ultrafiltro que lo contiene. Todo filtro es la intersección de todos los ultrafiltros que lo contienen.

**Referencias**

- Herrlich, H. (2006). Axiom of choice. Berlin: Springer.
- König, J. (1905). Zum Kontinuum-Problem.
- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.


### Conjuntos bien ordenados {#wellordered}

Todo orden lineal en un conjunto finito es un buen ordenamiento.

**Definición**: Un conjunto bien ordenado _X_ es un conjunto linealmente ordenado para el cual todo subconjunto no vacío tiene un elemento minimal.

Recordemos que ___x___ es minimal en _X_ si y solo si, para todo <img src="https://render.githubusercontent.com/render/math?math=y%5Cin%20X%20(y%5Cleq%20x%20%5Cimplies%20y%3Dx)">. No debes confundirlo con un minimo (límite inferior) que se define como un elemento ___x___ tal que para todo <img src="https://render.githubusercontent.com/render/math?math=y%5Cin%20X%20(x%5Cleq%20y)">. Date cuenta que todo minimo es minimal; todo mínimo es el único minimal. Sin embargo, un único minimal no necesariamente es un mínimo. Dentro de un orden lineal, sin un elemento es minimal entonces es un mínimo.

Estar bien ordenado es una propiedad hereditaria, es decir, una propiedad que se hereda a cada subconjunto.

**Teorema**: X está bien ordenado si y solo si, dado cierto orden lineal, no existe una cada descendiente infinita de elementos de X.

Una consecuencia directa de este teorema es que el intervalo unitario <img src="https://render.githubusercontent.com/render/math?math=%5B0%2C1%5D"> no está bien ordenado, es decir, el continuo no está bien ordenado.

**Principio del buen ordenamiento**: Todo conjunto puede ser bien ordenado.

El principio del buen ordenamiento y el axioma de elección son equivalentes.

Decimos que un elemento <img src="https://render.githubusercontent.com/render/math?math=y"> es sucesor de <img src="https://render.githubusercontent.com/render/math?math=x"> si y solo si (1) <img src="https://render.githubusercontent.com/render/math?math=x%3Cy"> y (2) <img src="https://render.githubusercontent.com/render/math?math=%5Cforall%20z%5Cin%20X%20(x%3Cz%5Cimplies%20y%5Cleq%20z)">. Otra forma de denotar al sucesor de __x__ es mediante __S(x)__. Note que en un conjunto linealmente ordenado, __x__ no puede tener más de un sucesor, además, no necesarimante todo elemento tiene sucesor.

**Proposición**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> un conjunto linealmente ordenado, <img src="https://render.githubusercontent.com/render/math?math=\large x\in X">. <img src="https://render.githubusercontent.com/render/math?math=\large x"> es maximal o <img src="https://render.githubusercontent.com/render/math?math=\large x"> tiene un sucesor.

**Proposición**: Sea <img src="https://render.githubusercontent.com/render/math?math=S%5E%7Bn%2B1%7D(x)%3DS(S%5E%7Bn%7D(x))"> y <img src="https://render.githubusercontent.com/render/math?math=S%5E%7B0%7D(x)%3Dx">, si __n<m__, entonces <img src="https://render.githubusercontent.com/render/math?math=S%5E%7Bn%7D(x)%3CS%5E%7Bm%7D(x)"> para todo __x__.

Llamamos a un elemento como límite si no es el sucesor de ningún elemento.

**Proposición**: Sea __X__ un conjunto bien ordenado y <img src="https://render.githubusercontent.com/render/math?math=\large \Lambda"> el conjunto de límites en __X__. Entonces, <img src="https://render.githubusercontent.com/render/math?math=\large X\subset \{S^{n}(x):x^in\Lambda,n\in\N\}">.


**Referencias**

- Roitman, J. (1990). Introduction to modern set theory. John Wiley & Sons.
- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.

### Inducción matemática {#induction}

**Principio de Inducción Matemática** (Prueba por inducción): Para cada <img src="https://render.githubusercontent.com/render/math?math=\large n\in \mathbb{N}">, sea <img src="https://render.githubusercontent.com/render/math?math=\large P_n"> una proposición matemática. Supón que <img src="https://render.githubusercontent.com/render/math?math=\large P_0"> es verdadero y que para cualquier <img src="https://render.githubusercontent.com/render/math?math=\large n">, <img src="https://render.githubusercontent.com/render/math?math=P_%7Bn%2B1%7D"> es cierto siempre que <img src="https://render.githubusercontent.com/render/math?math=\large P_n"> es cierto. Entonces, parar cada <img src="https://render.githubusercontent.com/render/math?math=\large n">, <img src="https://render.githubusercontent.com/render/math?math=\large P_n"> es verdadero. En lógica, <img src="https://render.githubusercontent.com/render/math?math=(P_0%5Cland%20%5Cforall%20n%20(P_n%5CRightarrow%20P_%7Bn%2B1%7D))%5CRightarrow%20%5Cforall%20n%20(P_n)">.

De forma general, si 0 pertenece al conjunto __X__ y <img src="https://render.githubusercontent.com/render/math?math=\large n\in X"> implica <img src="https://render.githubusercontent.com/render/math?math=n%2B1%5Cin%20X"> para todo número natural __n__, entonces <img src="https://render.githubusercontent.com/render/math?math=\large X=\N">. Esta proposición se prueba por el buen ordenamiento de los naturales.

El siguiente teorema se prueba por inducción matemática.

**Teorema**: Si <img src="https://render.githubusercontent.com/render/math?math=\large X"> es finito, entonces <img src="https://render.githubusercontent.com/render/math?math=%5Cwp(X)"> es finito.

**Definición por inducción**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> cualquier conjunto no vacío. Supón que <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> es un punto fijo de <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large g"> es un mapeo cualquiera <img src="https://render.githubusercontent.com/render/math?math=\large g:X\to X">. Entonces, existe un mapeo único <img src="https://render.githubusercontent.com/render/math?math=\large f:\mathbb{N}\to X"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large f(0)=x_0"> y <img src="https://render.githubusercontent.com/render/math?math=f(n%2B1)%3Dg(f(n))"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large n">.

**Prueba por inducción transfinita**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large (W,\leq)"> un conjunto bien ordenado, sea <img src="https://render.githubusercontent.com/render/math?math=\large P(w)"> una proposición matemática respecto a <img src="https://render.githubusercontent.com/render/math?math=\large w\in W">. Supón que <img src="https://render.githubusercontent.com/render/math?math=\large \forall w \in W (P(v) \forall v<w)\Rightarrow P(w) "> Entonces, <img src="https://render.githubusercontent.com/render/math?math=\large P(w)"> es cierto para todo elemento de <img src="https://render.githubusercontent.com/render/math?math=\large W">.

34/274

**Referencias**

- Roitman, J. (1990). Introduction to modern set theory. John Wiley & Sons.
- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.

### Números cardinales {#carinal}

A pesar de estar en contra de AC, Russell dio una versión equivalente del axioma de elección llamada axioma de multipicación. La introducción de este axioma permitía la definición de productos arbitrarios de números cardinales, como

- <img src="https://render.githubusercontent.com/render/math?math=\large |X|\cdot |Y|=|X\times Y|">
- <img src="https://render.githubusercontent.com/render/math?math=\large k\cdot 0=0\cdot k=0">
- <img src="https://render.githubusercontent.com/render/math?math=\large k \cdot u = 0 \Rightarrow k=0\lor u=0">
- <img src="https://render.githubusercontent.com/render/math?math=\large k\cdot 1=1\cdot k=k">

**Axioma multiplicativo**: (Russell) Para cada familia <img src="https://render.githubusercontent.com/render/math?math=\large (X_i)_{i\in I}"> de conjuntos no vacíos mutuamente disjuntos, existe un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large Y"> con <img src="https://render.githubusercontent.com/render/math?math=\large |Y\cap X_i|=1"> para cada <img src="https://render.githubusercontent.com/render/math?math=\large i\in I">.

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

**Hipótesis del Aleph**: Para todo ordinal <img src="https://render.githubusercontent.com/render/math?math=%5Calpha">, <img src="https://render.githubusercontent.com/render/math?math=2%5E%7B%5Caleph_%5Calpha%7D%3D%5Caleph_%7B%5Calpha%2B1%7D">. Tanto la hipótesis del continuo como la hipótesis del aleph para un cardinal 0 se supone que son falsas.

**Referencias**

- Herrlich, H. (2006). Axiom of choice. Berlin: Springer.


### Números ordinales

Los ordinales son conjuntos bien ordenados canónicos, en realidad, cualquier conjunto bien ordenado es orden isomórfico a un ordinal; por lo que no es una exageración decir que los ordinales son centrales para el estudio de los conjuntos.
