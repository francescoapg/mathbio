[<<Home](https://francescoapg.github.io/mathbio/)

## Topología General

Los objetos que estudia la Topología son **espacios topológicos**, los cuales, en términos simples, son conjuntos con propiedades adicionales. La Topología General también es conocida como _point-set Topology_, se enfoca principalmente en la continuidad y propiedades geométricas de espacios. Esta es la base de

- Topologia Algebraica
- Topología Diferencial
- Topología de baja dimensión (_Low-Dimensional Topology_)

**Índice**

1. [Nociones Introductorias](#intro)
2. [Espacios Métricos](#met)
3. [Homeomorfismo](#homeo)
4. [Espacios Topológicos](#topospace)
5. [Retracción](#retraction)
6. [Constructos Topológicos](#contructs)

**Elementos Adicionales**

1. [σ-Álgebras y _Set Systems_](#apen-1)

### Nociones Introductorias {#intro}

Estudiar Topología es más sencillo con un ejemplo concreto como lo es <img src="https://render.githubusercontent.com/render/math?math=\large \R">.

**Definción**: Se llama **vecindad** de <img src="https://render.githubusercontent.com/render/math?math=\large x"> a un conjunto que incluye a un intervalo abierto que a su vez incluye a <img src="https://render.githubusercontent.com/render/math?math=\large x"> (Horváth, 1969).

**Definiciones**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large M"> un subconjunto de <img src="https://render.githubusercontent.com/render/math?math=\large \R">. Un punto <img src="https://render.githubusercontent.com/render/math?math=\large x\in \R"> es **punto interior** de <img src="https://render.githubusercontent.com/render/math?math=\large M"> si existe una vecindad <img src="https://render.githubusercontent.com/render/math?math=\large V"> de <img src="https://render.githubusercontent.com/render/math?math=\large x"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large V\subset M">. Un punto <img src="https://render.githubusercontent.com/render/math?math=\large x\in\R"> es un **punto exterior** a <img src="https://render.githubusercontent.com/render/math?math=\large M"> si existe una vecindad <img src="https://render.githubusercontent.com/render/math?math=\large V"> de <img src="https://render.githubusercontent.com/render/math?math=\large x"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large V\cap M=\emptyset">. Un punto <img src="https://render.githubusercontent.com/render/math?math=\large x\in\R"> es un punto de frontera (**boundary point**) si toda vecindad <img src="https://render.githubusercontent.com/render/math?math=\large V"> de <img src="https://render.githubusercontent.com/render/math?math=\large x"> cumple que <img src="https://render.githubusercontent.com/render/math?math=\large V\cap M\neq \emptyset \land V\setminus M\neq\emptyset"> (Horváth, 1969).

**Definición**: Un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large A"> de <img src="https://render.githubusercontent.com/render/math?math=\large \R"> es abierto si todos sus elementos son interiores (Horváth, 1969).

En la sección de [espacios topológicos](https://francescoapg.github.io/mathbio/topos#topospace) vemos que la noción o idea de cálculo de conjuntos abiertos dada aquí es congruente con la definición general de _abierto_. Más aún, en base a la definición brindada, las siguientes proposiciones son demostrables:

- <img src="https://render.githubusercontent.com/render/math?math=\large \emptyset"> y <img src="https://render.githubusercontent.com/render/math?math=\large \R"> son abiertos.
- Si <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> son abiertos, también lo es <img src="https://render.githubusercontent.com/render/math?math=\large A\cap B">.
- <img src="https://render.githubusercontent.com/render/math?math=\large \cup_{i\in I}\{A_i\}"> (siendo cada <img src="https://render.githubusercontent.com/render/math?math=\large A_i"> abierto) es también un abierto.

Cada una de estas se verifica directamente de la definición general de _abierto_.

**Definiciones**: El conjunto de todos los puntos interiores de un subconjunto cualquiera de <img src="https://render.githubusercontent.com/render/math?math=\large \R"> se llama **interior** de <img src="https://render.githubusercontent.com/render/math?math=\large A"> y se denota por <img src="https://render.githubusercontent.com/render/math?math=\large A^{\circ}">, <img src="https://render.githubusercontent.com/render/math?math=\large \mathit{Int}A"> o <img src="https://render.githubusercontent.com/render/math?math=\large \langle A \rangle">. El _**boundary**_ de <img src="https://render.githubusercontent.com/render/math?math=\large A"> es el conjunto de todos los puntos de frontera de <img src="https://render.githubusercontent.com/render/math?math=\large A"> y se denota por <img src="https://render.githubusercontent.com/render/math?math=\large \delta A">, <img src="https://render.githubusercontent.com/render/math?math=\large b(A)">, <img src="https://render.githubusercontent.com/render/math?math=\large Fr(A)"> o <img src="https://render.githubusercontent.com/render/math?math=\large Fr_{\R}(A)">. 

El interior de <img src="https://render.githubusercontent.com/render/math?math=\large A"> es el complemento en <img src="https://render.githubusercontent.com/render/math?math=\large A"> del _boundary_ de <img src="https://render.githubusercontent.com/render/math?math=\large A">. El _boundary_ de <img src="https://render.githubusercontent.com/render/math?math=\large A"> es el conjunto de puntos que no están en el interior de <img src="https://render.githubusercontent.com/render/math?math=\large A"> o en el interior de <img src="https://render.githubusercontent.com/render/math?math=\large \R\setminus A">. El _boundary_ de <img src="https://render.githubusercontent.com/render/math?math=\large A"> es también <img src="https://render.githubusercontent.com/render/math?math=\large \overline{A}\setminus A^{\circ}">. Todo conjunto que contenga su _boundary_ no es abierto; análogamente, si un conjunto es disjunto a su _boundary_ es abierto. El interior de todo conjunto es abierto. 

**Definición**: Se dice que un punto <img src="https://render.githubusercontent.com/render/math?math=\large x\in\R"> es _adherente_ al conjunto <img src="https://render.githubusercontent.com/render/math?math=\large A\subset\R"> si toda vecindad de dicho elemento contiene un elemento de <img src="https://render.githubusercontent.com/render/math?math=\large A">.

Una conclusión directa es que los puntos adherentes serán los puntos interiores de <img src="https://render.githubusercontent.com/render/math?math=\large A"> y los puntos de frontera de <img src="https://render.githubusercontent.com/render/math?math=\large A">.

**Definición**: El conjunto de todos los puntos de adherencia de un conjunto es llamada la adherencia o **cerradura** de dicho conjunto. Se denota como <img src="https://render.githubusercontent.com/render/math?math=\large \overline{A}">, <img src="https://render.githubusercontent.com/render/math?math=\large \mathit{Cl}A"> o <img src="https://render.githubusercontent.com/render/math?math=\large \mathit{Cl}_{\R}A">.

La cerradura también se puede definir como el complemento del interior del complemento del conjunto.

**Definición**: Las siguientes son definiciones equivalentes de conjunto **cerrado**:

1. Un conjunto **cerrado** es el complemento en \R de un conjunto abierto.
2. Es un conjunto que es equivalente a su cerradura (A=\overline{A}).

Finalmente, un conjunto puede ser cerrado, abierto, cerrado y abierto o ninguno de los dos. Con esto, podemos concluir que

- <img src="https://render.githubusercontent.com/render/math?math=\large \emptyset"> y <img src="https://render.githubusercontent.com/render/math?math=\large \R"> son cerrados.
- Si <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> son  cerrados, también lo es <img src="https://render.githubusercontent.com/render/math?math=\large A\cup B">.
- <img src="https://render.githubusercontent.com/render/math?math=\large \cap_{i\in I}\{A_i\}"> (siendo cada <img src="https://render.githubusercontent.com/render/math?math=\large A_i"> cerrado) es también un cerrado.

**Referencias**

- Horváth, J. (1969). Introducción a la topología general. Matemática. Monografía (OEA).
- Boundary. Encyclopedia of Mathematics. URL: http://encyclopediaofmath.org/index.php?title=Boundary&oldid=39407
- Closure of a set. Encyclopedia of Mathematics. URL: http://encyclopediaofmath.org/index.php?title=Closure_of_a_set&oldid=34423

### Espacios Métricos {#met}

Los espacios métricos son una generalización del espacio euclidiano.

**Definición**

Un espacio euclidiano es un par <img src="https://render.githubusercontent.com/render/math?math=\large (X,d)">, tal que <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un conjunto y <img src="https://render.githubusercontent.com/render/math?math=\large d"> una función de distancia abstracta definida como <img src="https://render.githubusercontent.com/render/math?math=\large d:X\times X \to \R">, de modo que se cumplen las siguientes condiciones para cualesquiera puntos <img src="https://render.githubusercontent.com/render/math?math=\large x,y,z"> de <img src="https://render.githubusercontent.com/render/math?math=\large X">.

- (M1) <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y \in X,d(x,y)\geq 0">
- (M1.5) <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y\in X, x=y\iff d(x,y)=0">
- (M2) <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y\in X, d(x,y)=d(y,x)">
- (M3) <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y,z\in X, d(x,y)+d(y,z)\geq d(x,z)">

Estas condiciones se llaman positividad, simetría e inecualidad triangular.

**Convergencia de secuencias**

Una secuencia <img src="https://render.githubusercontent.com/render/math?math=\large \{x_n\}"> en un espacio métrico <img src="https://render.githubusercontent.com/render/math?math=\large (X,d)"> se dice que **converge** a un punto <img src="https://render.githubusercontent.com/render/math?math=\large y"> en <img src="https://render.githubusercontent.com/render/math?math=\large X"> si para cada <img src="https://render.githubusercontent.com/render/math?math=\large \epsilon>0"> existe un entero positivo <img src="https://render.githubusercontent.com/render/math?math=\large N"> tal que para todos los enteros <img src="https://render.githubusercontent.com/render/math?math=\large n\geq N">, <img src="https://render.githubusercontent.com/render/math?math=\large d(x_n,y)<\epsilon">.

Expresado en términos de topología, para un espacio topológico arbitrario, una secuencia <img src="https://render.githubusercontent.com/render/math?math=\large \{x_n\}"> en un espacio topológico <img src="https://render.githubusercontent.com/render/math?math=\large (X,\mathcal{T})"> converge a un punto <img src="https://render.githubusercontent.com/render/math?math=\large y"> de <img src="https://render.githubusercontent.com/render/math?math=\large X"> si para cada conjunto abierto <img src="https://render.githubusercontent.com/render/math?math=\large U"> que contiene a <img src="https://render.githubusercontent.com/render/math?math=\large y">, existe un natural <img src="https://render.githubusercontent.com/render/math?math=\large N">, tal que para todo <img src="https://render.githubusercontent.com/render/math?math=\large n\geq N">, <img src="https://render.githubusercontent.com/render/math?math=\large x_n\in U">.

Considera <img src="https://render.githubusercontent.com/render/math?math=\large (X, d)"> como un espacio métrico.

**Definición**:
Sea <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in X"> y <img src="https://render.githubusercontent.com/render/math?math=\large r"> un número real positivo. Entonces, la **bola abierta** con centro en <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> y radio <img src="https://render.githubusercontent.com/render/math?math=\large r"> se define como el conjunto <img src="https://render.githubusercontent.com/render/math?math=\large \{x\in X: d(x,x_0)<r\}">. Se denota como <img src="https://render.githubusercontent.com/render/math?math=\large B_r(x_0)"> o <img src="https://render.githubusercontent.com/render/math?math=\large B(x_0,r)">. Se llama tambíén la r-bola abierta alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large x_0">. Cuando se quiere dejar en claro la métrica se usa <img src="https://render.githubusercontent.com/render/math?math=\large B_d(x_0,r)">.
    
**Definición**:
Un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large A\subset X"> se dice que es **abierto** si para cada <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in A">, existe alguna bola abierta alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> y esta es contenida en <img src="https://render.githubusercontent.com/render/math?math=\large A">, es decir, existe <img src="https://render.githubusercontent.com/render/math?math=\large 0<r"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large B(x_0,r)\subset A">.

Vemos como los conceptos de topología surgen a partir de la métrica, en estos casos, llamamos al espacio topológico como **metrizable**.

Retomando el caso de <img src="https://render.githubusercontent.com/render/math?math=\large \R">, la **topología usual** de <img src="https://render.githubusercontent.com/render/math?math=\large \R"> es definida como la topología inducida por la métrica euclidiana. <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> en este caso está conformado por los subconjuntos de <img src="https://render.githubusercontent.com/render/math?math=\large \R"> que pueden ser expresados como la unión contable de intervalos abiertos de <img src="https://render.githubusercontent.com/render/math?math=\large \R">. Existen otras topologías definidas en <img src="https://render.githubusercontent.com/render/math?math=\large \R"> como la _topología de intervalos semi-abiertos_ o la _topología de dispersión_.

Para terminar esta sección, hablaremos de la topología de los conjuntos [linealmente ordenados](https://francescoapg.github.io/mathbio/biomath#semana3) <img src="https://render.githubusercontent.com/render/math?math=\large (X,\leq)">. Sea <img src="https://render.githubusercontent.com/render/math?math=\large A\subset X"> un abierto si <img src="https://render.githubusercontent.com/render/math?math=\large \forall x\in A">, <img src="https://render.githubusercontent.com/render/math?math=\large \exists a,b\in A (a<x<b\land"> <img src="https://render.githubusercontent.com/render/math?math=\large \{y\in X: a<y<b\}\subset A)">.

**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.

### Homeomorfismo {#homeo}

Ser homeomórficos es una relación de equivalencia en la clase de todos los espacios topológicos. Una propiedad o un atributo de un objeto, que es invariante ante homeomorfismos, se dice que es topológica en caracter. Estas propiedades algunas veces son denominadas invariantes topológicas.

**Definición**: Sean <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> de subconjuntos de espacios euclidianos. Un homeomorfismo entre <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> es una [biyección](https://francescoapg.github.io/mathbio/functlations#funciones) <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B"> tal que tanto <img src="https://render.githubusercontent.com/render/math?math=\large f"> como su inversa son continuos. Cuando tal <img src="https://render.githubusercontent.com/render/math?math=\large f"> existe, se dice que <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> son homeomórficos entre ellos.

El mapa de identidad (<img src="https://render.githubusercontent.com/render/math?math=\large i">) es el ejemplo más sencillo de homeomorfismo. La inversa de un homeomorfismo y la composición de dos homeomofismos también lo son.

**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.

### Espacio Topológico {#topospace}
    
**Definición**: 
Un **espacio topológico** es un par <img src="https://render.githubusercontent.com/render/math?math=\large (X,\mathcal{T})"> donde <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un conjunto y <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> es una familia de subconjuntos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> que satisfacen que:

1. <img src="https://render.githubusercontent.com/render/math?math=\large \emptyset \in \mathcal{T}$ y $X\in \mathcal{T}">.
2. <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> es cerrado bajo uniones arbitrarias.
3. <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> es cerrado bajo intersecciones arbitrarias.

La familia<img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> se dice que es una topología del conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X">. Los miembros de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> se dice que son abiertos en <img src="https://render.githubusercontent.com/render/math?math=\large X"> o que son subconjuntos abiertos de <img src="https://render.githubusercontent.com/render/math?math=\large X">. Es evidente que tanto <img src="https://render.githubusercontent.com/render/math?math=\large \emptyset"> como <img src="https://render.githubusercontent.com/render/math?math=\large X"> son parte de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}">.

Nos damos cuenta, entonces, que el enfoque _métrico_ es solo una manera de definir topologías; sin embargo, en general, no es necesario.

**Bases de una Topología**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large (X, \mathcal{T})"> un espacio tológico. Una subfamilia <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{B}"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> se dice que es una base de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> si cada miembro de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> puede ser expresado como la unión de algunos miembros de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{B}">.

**Vecindad**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large (X,\mathcal{T})"> un espacio topológico, <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in X"> y <img src="https://render.githubusercontent.com/render/math?math=\large N\subset X">. Entonces, <img src="https://render.githubusercontent.com/render/math?math=\large N"> se dice que es una **vecindad** de <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> o <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> es llamado **punto interior** de <img src="https://render.githubusercontent.com/render/math?math=\large N"> si hay un conjunto abierto <img src="https://render.githubusercontent.com/render/math?math=\large V"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in V"> y <img src="https://render.githubusercontent.com/render/math?math=\large V\subset N">.

**Cercanía (_Nearness_)**

Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> un conjunto. Una **relación de cercanía** en <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large N"> de <img src="https://render.githubusercontent.com/render/math?math=\large X\times \wp(X)"> el cual satisface ciertas propiedades.
    
_Notación_: Para <img src="https://render.githubusercontent.com/render/math?math=\large y\in X"> y <img src="https://render.githubusercontent.com/render/math?math=\large A\in \wp (X)">, escribimos <img src="https://render.githubusercontent.com/render/math?math=\large y\delta A"> para referirnos a <img src="https://render.githubusercontent.com/render/math?math=\large (y,A)\in N"> y <img src="https://render.githubusercontent.com/render/math?math=\large y \overline{\delta}A"> para denotar <img src="https://render.githubusercontent.com/render/math?math=\large (y,A)\notin N">; <img src="https://render.githubusercontent.com/render/math?math=\large y\delta A"> se lee como "<img src="https://render.githubusercontent.com/render/math?math=\large y"> está cerca a <img src="https://render.githubusercontent.com/render/math?math=\large A">".
    
_Propiedades_:

1. <img src="https://render.githubusercontent.com/render/math?math=\large y\overline{\delta}\emptyset"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large y\in X">.
2. <img src="https://render.githubusercontent.com/render/math?math=\large y\in A\implies y\delta A"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large y\in X">, <img src="https://render.githubusercontent.com/render/math?math=\large A\subset X">.
3. <img src="https://render.githubusercontent.com/render/math?math=\large y\delta (A\cup B)\iff y\delta A\lor y\delta B">, para todo <img src="https://render.githubusercontent.com/render/math?math=\large y\in X">, <img src="https://render.githubusercontent.com/render/math?math=\large A,B \subset X">.
4. Si <img src="https://render.githubusercontent.com/render/math?math=\large y\delta A"> y (<img src="https://render.githubusercontent.com/render/math?math=\large a\delta B"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large a\in A">), entonces <img src="https://render.githubusercontent.com/render/math?math=\large y\delta B">, para todo <img src="https://render.githubusercontent.com/render/math?math=\large y\in X">, <img src="https://render.githubusercontent.com/render/math?math=\large A,B\subset X">.

**Proposición**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> una familia de subconjuntos de <img src="https://render.githubusercontent.com/render/math?math=\large X">, entonces existe una topología <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> de <img src="https://render.githubusercontent.com/render/math?math=\large X"> que incluye a <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> y sea la más pequeña (es subconjunto de toda topología que incluya a <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> y es única).

Entonces se dice que <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> genera a <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}">. Relacionados a estos conceptos de inclusión de topologías están los conceptos comparativos de "**más pequeño** que" o "**más grande** que".

**Definición**: La topología <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}_1"> es más pequeña (o más debil o más tosca) que la topología <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}_2"> si <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}_1\subset\mathcal{T}_2">. En este caso, <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}_2"> es más grande (o más fuerte o más fina) que <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}_1">.

Note que tanto la topología <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}_1"> como <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}_2"> deben estar definidas en el mismo conjunto.

En este sentido, la topología más pequeña de todas es la **topología indiscreta** (<img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}=\{\emptyset,X\}">), mientras que la topología más grande de todas es la **topología discreta** (<img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}=\wp(X)">). Otra topología con nombre es la **topología cofinita** que en el caso de conjuntos finitos, coincide con la topología discreta, y está definida como aquella que comprende a subconjuntos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> cuyo complemento en <img src="https://render.githubusercontent.com/render/math?math=\large X"> es finito.

**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.

### Retracción {#retraction}

Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> un espacio topológico y <img src="https://render.githubusercontent.com/render/math?math=\large A"> un subespacio de <img src="https://render.githubusercontent.com/render/math?math=\large X">. El mapeo (función continua)

<img src="https://render.githubusercontent.com/render/math?math=%5Ctau%20%3A%20X%20%5Cto%20A">

es una **retracción** si <img src="https://render.githubusercontent.com/render/math?math=%5Ctau_%7B%7CA%7D(x)%3Dx">.

**Referencias**


### Constructos Topológicos {#contructs}

Un **constructo** es una categoría concreta sobre **Set**.

**Referencias**

- Preuss, G. (2011). Foundations of topology: an approach to convenient topology. Springer Science & Business Media.

## Elementos Adicionales

### σ-Álgebras y _Set Systems {#apen-1}

**σ-Álgebras**

El estudio de σ-álgebras está relacionado con probabilidades y surge como respuesta a la necesidad de medir. Al ser cerradas bajo complementación, las σ-álgebras nos brindan un marco para responder preguntas presentándonos las alternativas <img src="https://render.githubusercontent.com/render/math?math=\large P"> y <img src="https://render.githubusercontent.com/render/math?math=\large \neg P">. La definición por Jost (2015) es la siguiente,

**Definición**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> un conjunto, una σ-álgebra de subconjuntos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{A}"> de <img src="https://render.githubusercontent.com/render/math?math=\large \wp(X)"> que satisface:

- <img src="https://render.githubusercontent.com/render/math?math=\large X\in\mathcal{A}">.
- <img src="https://render.githubusercontent.com/render/math?math=\large y\in\mathcal{A}\implies X\setminus y\in\mathcal{A}">.
- Siendo <img src="https://render.githubusercontent.com/render/math?math=\large \{X_n\}"> un secuencia, si <img src="https://render.githubusercontent.com/render/math?math=\large X_i\mathcal{A}">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large \Cup_{n\in\N}X_n\in\mathcal{A}">.

**Referencias**

- Jost, J. (2015). Mathematical concepts. Berlin: Springer.
