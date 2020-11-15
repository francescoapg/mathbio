[<<Home](https://francescoapg.github.io/mathbio/)

## Biomatemática

Se recomienda al lector leer la introducción de [Teoría de conjuntos](https://francescoapg.github.io/mathbio/setheory#intro) antes de revisar esta sección.

**Índice**

1. [Estructuras algebraicas: Grupos](#semana2)
2. [Látices y orden](#semana3)
3. Estructuras naturales

### Estructuras algebraicas: Grupos {#semana2}

Un Sistema Algebraico puede ser descrito como un conjunto de objetos junto con algunas operaciones para combinarlas (Herstein, 1975).

**Álgebra abstracta**

Terminada nuestra (muy) breve introducción a Teoría de conjuntos inciaremos la discusión de los principales campos de Álgebra abstracta. El objeto de estudio del Álgebra abstracta será más general y rico que el de Álgebra elemental, brevemente, podemos decir que se ocupa del estudio de _estructuras algebraicas_ y sus propiedades. La definición de estructura algebraica es más específica que la de sistema algebraico; una estructura algebraica es un conjunto en el que están definidas operaciones binarias. Es importante resaltar que las operaciones binarias se definen con _axiomas_. Según el número de operaciones binarias definidas en ellos, las estructuras algebraicas se clasifican en:

- Similar a Grupo
- Similar a Anillo
- Similar a Látice
- Similar a Módulo
- Similar a Álgebra

En esta lección, nos enfocaremos en Grupos y Anillos.

**Grupos**

Una operación binaria o ley de composición en un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large G"> puede entenderse como una función <img src="https://render.githubusercontent.com/render/math?math=\large G\times G \to G"> que lleva cada par <img src="https://render.githubusercontent.com/render/math?math=\large (a,b)"> del conjunto <img src="https://render.githubusercontent.com/render/math?math=\large G\times G"> a un elemento del conjunto <img src="https://render.githubusercontent.com/render/math?math=\large G">; el elemento asignado al par se conoce como composición de <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b"> y se suele representar como <img src="https://render.githubusercontent.com/render/math?math=\large a \circ b"> o <img src="https://render.githubusercontent.com/render/math?math=\large ab">. De este modo, asociamos al conjunto con la operación binaria definida en este en un dupla <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )">, esta es la definición de grupo. Este cumple con los siguientes axiomas:

- Asociatividad de la ley de composición: <img src="https://render.githubusercontent.com/render/math?math=\large (a \circ b)\circ c=a\circ (b\circ c)"> para <img src="https://render.githubusercontent.com/render/math?math=\large a,b,c\in G">.
- Existencia del elemento identidad: <img src="https://render.githubusercontent.com/render/math?math=\large \forall a\in G \exists e \in G (e \circ a = a \circ e = a)">.
- Existencia de la inversa de cada elemento: <img src="https://render.githubusercontent.com/render/math?math=\large \forall a\in G \exists a^{-1} (a\circ a^{-1} = a^{-1}\circ a = e)">.

Existe una condición adicional llamada conmutatividad, definida como <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b \in G (a \circ b = b \circ a)">. Los grupos que cumplan con esta condición son llamados grupos abelianos o conmutativos, los que no cumplen la condición son llamados no abelianos o no conmutativos.

A partir de esta colección de axiomas, se pueden probar ciertas propiedades, una de ellas es la unicidad del elemento identidad, es decir, existe un solo elemento <img src="https://render.githubusercontent.com/render/math?math=\large e"> en <img src="https://render.githubusercontent.com/render/math?math=\large G"> que funciona como elemento identidad de todos los elementos del conjunto <img src="https://render.githubusercontent.com/render/math?math=\large G">. Otra proposición que se prueba es que las inversas (<img src="https://render.githubusercontent.com/render/math?math=\large a^{-1}">) son únicas para cada elemento, es decir, si dos elementos tienen la misma inversa entonces estos son los mismos elementos.

**Proposición**: Si <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b"> son elementos de <img src="https://render.githubusercontent.com/render/math?math=\large G">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large ax=b"> y <img src="https://render.githubusercontent.com/render/math?math=\large xa=b"> tienen soluciones únicas en <img src="https://render.githubusercontent.com/render/math?math=\large G">.

Esta proposición es usualmente asumida en Álgebra elemental. Finalmente, los grupos respetan las leyes de exponentes usuales.

Un subgrupo <img src="https://render.githubusercontent.com/render/math?math=\large (H,\circ )"> de un grupo <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )"> es un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large H"> de <img src="https://render.githubusercontent.com/render/math?math=\large G"> que es cerrado bajo la operación <img src="https://render.githubusercontent.com/render/math?math=\large \circ">. El subgrupo más pequeño o **subgrupo trivial** es aquel que tiene como único elemento al elemento identidad. A continuación, una definición de subgrupos dada como proposición en (Judson, 2017):

**Proposición**: Un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large H"> de <img src="https://render.githubusercontent.com/render/math?math=\large G"> es un subgrupo si y solo si cumple las siguientes condiciones.
1. La identidad de <img src="https://render.githubusercontent.com/render/math?math=\large G"> está en <img src="https://render.githubusercontent.com/render/math?math=\large H">.
2. Si <img src="https://render.githubusercontent.com/render/math?math=\large h1,h2\in H \Rightarrow h1\circ h2\in H">.
3. Si <img src="https://render.githubusercontent.com/render/math?math=\large h\in H\Rightarrow h^{-1}\in H">.

A continuación, hablaremos sobre un tipo especial de subgrupo: el **subgrupo cíclico**. Un subgrupo cíclico tiene una estructura particular, en él, conociendo a un elemento se pueden determinar los demás elementos, es decir, ese elemento actúa como _generador_ del resto de elementos. La definición de subgrupo cíclico es la siguiente.

**Proposición**: Un conjunto de la forma <img src="https://render.githubusercontent.com/render/math?math=\small \langle a \rangle"><img src="https://render.githubusercontent.com/render/math?math=\large =\{a\circ b: b\in G\}"> donde <img src="https://render.githubusercontent.com/render/math?math=\large a"> es cualquier elemento de <img src="https://render.githubusercontent.com/render/math?math=\large G"> es un subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large G">.

_Demostración_: El elemento identidad está en <img src="https://render.githubusercontent.com/render/math?math=\small	 \langle \large a \small	 \rangle"> ya que <img src="https://render.githubusercontent.com/render/math?math=\large a^{-1}\in G">, la composición de dos elementos de <img src="https://render.githubusercontent.com/render/math?math=\small \langle \large a \small \rangle"> tendrá la forma <img src="https://render.githubusercontent.com/render/math?math=\large (a\circ b) \circ (a\circ c)">, esto es equivalente a <img src="https://render.githubusercontent.com/render/math?math=\large a\circ (b \circ a)\circ c">, por definición del grupo <img src="https://render.githubusercontent.com/render/math?math=\large G">, <img src="https://render.githubusercontent.com/render/math?math=\large b \circ a\in G"> por lo que lo reemplazaremos por <img src="https://render.githubusercontent.com/render/math?math=\large d">, ahora <img src="https://render.githubusercontent.com/render/math?math=\large a\circ (d \circ c)">, análogamente, sería equivalente a un <img src="https://render.githubusercontent.com/render/math?math=\large a\circ e">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large e"> algún elemento de <img src="https://render.githubusercontent.com/render/math?math=\large G">; esta última expresión cumple con la definición del conjunto por lo que está incluído en él. Para la existencia de la inversa de todos sus elementos considera que si <img src="https://render.githubusercontent.com/render/math?math=\large a,b\in G"> entonces también su composición y también la inversa de su composición, por lo tanto <img src="https://render.githubusercontent.com/render/math?math=\large b^{-1}\circ a^{-1}\in G">, llamemos a este elemento como <img src="https://render.githubusercontent.com/render/math?math=\large c">, si <img src="https://render.githubusercontent.com/render/math?math=\large c"> pertenece a <img src="https://render.githubusercontent.com/render/math?math=\large G"> entonces <img src="https://render.githubusercontent.com/render/math?math=\large  a^{-1}\circ c"> también lo hace, llamemos a este último elemento como <img src="https://render.githubusercontent.com/render/math?math=\large d">. Ahora, los elementos de <img src="https://render.githubusercontent.com/render/math?math=\small \langle \large a \small \rangle"> tienen la forma general <img src="https://render.githubusercontent.com/render/math?math=\large a\circ x">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large x"> cualquier elemento de <img src="https://render.githubusercontent.com/render/math?math=\large G">, ya que <img src="https://render.githubusercontent.com/render/math?math=\large d"> es un elemento de <img src="https://render.githubusercontent.com/render/math?math=\large G">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large a\circ d \in "><img src="https://render.githubusercontent.com/render/math?math=\small \langle a \rangle">, operando este elemento, se prueba que <img src="https://render.githubusercontent.com/render/math?math=\large b^{-1}\circ a^{-1}\in"><img src="https://render.githubusercontent.com/render/math?math=\large \small \langle a \rangle">. 

Si <img src="https://render.githubusercontent.com/render/math?math=\large G"> contiene un elemento que lo genere entonces <img src="https://render.githubusercontent.com/render/math?math=\large G"> es un grupo cíclico. Se prueba que todo grupo cíclico es abeliano; también se prueba que todos los subgrupos de un grupo.

Ahora hablaremos de **grupos de permutación**, los cuales son clave para el estudio de simetría. Una permutación es un mapeo biyectivo <img src="https://render.githubusercontent.com/render/math?math=\large \pi : X \to X">. De forma general, las permutaciones de un set <img src="https://render.githubusercontent.com/render/math?math=\large X"> forman un grupo <img src="https://render.githubusercontent.com/render/math?math=\large S_X">, el cual es llamado **grupo simétrico**. Los subgrupos de <img src="https://render.githubusercontent.com/render/math?math=\large S_X"> son llamados **grupos de permutación**. 

Las permutaciones se suelen representar de la siguiente manera. Para un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X"> con elementos <img src="https://render.githubusercontent.com/render/math?math=\large a_1, a_2, ..., a_i, a_j, ...">, una permutación es la siguiente

<img src="https://render.githubusercontent.com/render/math?math=%5Cbegin%7Bpmatrix%7D%20%0Aa_1%20%26%20a_2%20%26%20...%20%5C%5C%20%0Aa_i%20%26%20a_j%20%26%20...%20%0A%5Cend%7Bpmatrix%7D">


Lo cual permuta <img src="https://render.githubusercontent.com/render/math?math=\large a_1"> con <img src="https://render.githubusercontent.com/render/math?math=\large a_i">, <img src="https://render.githubusercontent.com/render/math?math=\large a_2"> con <img src="https://render.githubusercontent.com/render/math?math=\large a_j">, y así sucesivamente. Finalmente, la composición de permutaciones no suele ser conmutativa.

El último tipo de grupo que veremos es el **grupo dihedral**. Un grupo dihedral es aquel que se forma de las permutaciones rígidas de un polígono. Dentro de sus elementos se tendrán solo rotaciones o reflexione, todas ellas respetan la vecindad de los vértices del polígono. De forma análoga, se puede establecer el grupo de movimientos rígidos de poliedros como cubos.

Finalmente, podemos incluir otras estructuras compatibles con la ley de combinación.

- Grupos topológicos
- Grupos de Lie
- Grupo algebraico
- Grupo ordenado
- Grupos libres
- Grupos completos
- Grupos residualmente finitos

Lo opuesto también puede ser logrado, si relajamos algunos de los axiomas que definen a un grupo obtenemos las siguientes estructuras similares a grupos.

- Monoide
- Monoide conmutativo
- Semigrupo
- Semigrupo inverso
- Magma
- Grupoide
- Semigrupoide

Hablaremos un poco de **Magmas** y **Monoides**. Un magma es un conjunto asociado con una ley de composición interna, se cumple que el conjunto es cerrado bajo la ley de composición, esta condición es compartida con el resto de estructuras similares a grupos y grupos, excepto por semigrupoides. Expresada en lógica, la condición es la siguiente: siendo <img src="https://render.githubusercontent.com/render/math?math=\large M"> un magma, <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b\in M (a\circ b\in M)">. Un monoide, además de la condición mencionada, cumple con la asociatividad de la ley de composición y la existencia del elemento identidad.

Continuamos con el Teorema de Lagrange, uno de los teoremas más importantes de la teoría de grupos finitos. Primero es necesario definir el concepto de _coset_. Sea <img src="https://render.githubusercontent.com/render/math?math=\large G"> un grupo y <img src="https://render.githubusercontent.com/render/math?math=\large H"> un subgrupo de este. Un coset izquierdo (o derecho) de <img src="https://render.githubusercontent.com/render/math?math=\large H"> es un set <img src="https://render.githubusercontent.com/render/math?math=\large gH=\{gh:h\in H\}"> (o <img src="https://render.githubusercontent.com/render/math?math=\large Hg=\{hg:h\in H\}">) dado <img src="https://render.githubusercontent.com/render/math?math=\large g\in G">. Note que en algunos casos, el coset izquierdo y derecho serán el mismo conjunto. También se prueba que los cosets izquierdos (y derechos) forman una patición del grupo, y que el número de cosets izquierdos y derechos de un subgrupo es el mismo.

Entre <img src="https://render.githubusercontent.com/render/math?math=\large H"> y su coset izquierdo <img src="https://render.githubusercontent.com/render/math?math=\large gH"> se puede definir un mapan bijectivo <img src="https://render.githubusercontent.com/render/math?math=\large \phi : H \to H">, con <img src="https://render.githubusercontent.com/render/math?math=\large \phi (h)=gh">. Definimos <img src="https://render.githubusercontent.com/render/math?math=%5BG%3AH%5D"> como el número de cosets izquierdos de <img src="https://render.githubusercontent.com/render/math?math=\large H"> en <img src="https://render.githubusercontent.com/render/math?math=\large G">. Esto recibirá el nombre de **índice** de <img src="https://render.githubusercontent.com/render/math?math=\large H"> en <img src="https://render.githubusercontent.com/render/math?math=\large G">.

**Teorema de Lagrange**: (Judson, 2017) Sea <img src="https://render.githubusercontent.com/render/math?math=\large G"> un grupo finito y <img src="https://render.githubusercontent.com/render/math?math=\large H"> un subgrupo de este, se cumple que <img src="https://render.githubusercontent.com/render/math?math=%5BG%5D%2F%5BH%5D%3D%5BG%3AH%5D"> es el número de cosets izquierdos distintos de <img src="https://render.githubusercontent.com/render/math?math=\large H"> en <img src="https://render.githubusercontent.com/render/math?math=\large G">. En particular, el número de elementos de <img src="https://render.githubusercontent.com/render/math?math=\large H"> debe dividir el número de elementos en <img src="https://render.githubusercontent.com/render/math?math=\large G">.

Un corolario importante de este teorema es que si un grupo finito tiene un número primo de elementos entonces es cíclico y cualquier elemento distinto al identidad es un generador.

Un subgrupo <img src="https://render.githubusercontent.com/render/math?math=\large H"> de un grupo <img src="https://render.githubusercontent.com/render/math?math=\large G"> es **normal** en <img src="https://render.githubusercontent.com/render/math?math=\large G"> si <img src="https://render.githubusercontent.com/render/math?math=\large gH=Hg"> para todo elemento <img src="https://render.githubusercontent.com/render/math?math=\large g"> de <img src="https://render.githubusercontent.com/render/math?math=\large G">, es decir, sus cosets derecho e izquierdo son iguales. Esto es facil de ver en un grupo abeliano. Si un grupo tiene únicamente grupos normales triviales, este grupo se llama grupo simple, y todos los grupos simples no abelianos tienen orden par.

A continuación, hablaremos de los **grupos cociente o factor**. Sea <img src="https://render.githubusercontent.com/render/math?math=\large H"> un subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large G">, el conjunto formado por todos los cosets (izquierdos o derechos, no ambos a menos que sean iguales) de <img src="https://render.githubusercontent.com/render/math?math=\large H"> en <img src="https://render.githubusercontent.com/render/math?math=\large G"> forman un grupo <img src="https://render.githubusercontent.com/render/math?math=\large G/H"> llamado _grupo cociente_, este grupo tiene como operación a <img src="https://render.githubusercontent.com/render/math?math=\circ : (aH)(bH)=abH">. Observe que los elementos de <img src="https://render.githubusercontent.com/render/math?math=\large G/H"> son subconjuntos de <img src="https://render.githubusercontent.com/render/math?math=\large G">. Este grupo (<img src="https://render.githubusercontent.com/render/math?math=\large G/H">) tiene como orden a <img src="https://render.githubusercontent.com/render/math?math=[G:H]">, como es evidente.

**Referencias**

- Herstein, I. N. (1975). Topics in algebra. Second edition. Xerox Corporation.
- Judson, T. W. y Beezer R. A. (2017) Abstract Algebra: Theory and Applications.

### Látices y orden {#semana3}

Empezamos esta sección con una nota sobre conjuntos parcialmente ordenados o **posets**. Un orden parcial en un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X"> es una relación binaria entre elementos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> que satisface lo siguiente.

1. <img src="https://render.githubusercontent.com/render/math?math=\large \forall a \in R (aRa)">
2. <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b,c \in R (aRb\land bRc \Rightarrow aRc)">
3. <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b\in R (aRb\land bRa \Rightarrow a=b)">

La primera condición recibe el nombre de reflexividad, la segunda, transitividad, y la tercera, antisimetría. Una relación de orden también puede cumplir que <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b\in R (aRb \lor bRa)">, si se cumple esta condición, la relación se dice que es un orden **lineal** o **total**. De este modo, un conjunto asociado a un orden parcial se llama _conjunto parcialmente ordenado_ o _poset_, y un conjunto asociado a un orden total se llama _conjunto linealmente ordenado_ o _totalmente ordenado_. 

Cuando un conjunto totalmente ordenado es subconjunto (subposet) de un poset, recibe el nombre de **cadena**. Una anticadena (<img src="https://render.githubusercontent.com/render/math?math=\large X">) está definida por la siguiente condición, <img src="https://render.githubusercontent.com/render/math?math=\large x\leq y \Rightarrow x=y \forall x, y \in X">. Si una relación de orden solo cumple 1. y 2., se conoce como _preorden_, y al objeto matemático asociado se lo conoce como _conjunto preordenado_. Nuevamente, es posible identificar un subconjunto dentro de este objeto que cumpla condiciones adicionales (como 3.), esto puede ser logrado al definir una clase de equivalencia dentro del conjunto asociada al preorden (<img src="https://render.githubusercontent.com/render/math?math=\large a\sim b \iff aRb \land bRa">). En algunos casos, identificar esta relación <img src="https://render.githubusercontent.com/render/math?math=\large \sim"> puede ser muy importante para el estudio.

Respecto a la notación, solemos usar los siguientes símbolos para referirnos a la relación de orden (y preorden).

<img src="https://render.githubusercontent.com/render/math?math=\large \leq, \preceq, \prec, \sqsubseteq">

El símbolo <img src="https://render.githubusercontent.com/render/math?math=\large <"> se reserva para el caso <img src="https://render.githubusercontent.com/render/math?math=\large a \leq b \land a\neq b">.

Se puede generar un conjunto ordenado a partir de otro mediante el **orden dual** u **orden opuesto**. Dado, <img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq)"> un poset, entonces 
<img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq ^{\ast})"> también es un conjunto odenado si se cumple que <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b \in X (a \leq ^{\ast} b \iff b \leq a)">. Otra forma de representar <img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq ^{\ast})"> es mediante los símbolos <img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq)^{op}"> o <img src="https://render.githubusercontent.com/render/math?math=\large X^{op}">.

**Ten en cuenta que todo poset puede ser representado como una colección de sets ordenados por la relación de inclusión**.

Un conjunto linealmente ordenado es llamado **orden denso** si para cada <img src="https://render.githubusercontent.com/render/math?math=\large x<y">, existe un <img src="https://render.githubusercontent.com/render/math?math=\large z"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large x<z<y">. Dos conjuntos linealmente ordenados son llamados **isomórficos en orden** o, simplemente, isomórficos si existe un mapeo biyectivo de uno a otro.

A continuación definiremos otros conjuntos importantes en el estudio de posets. Para cualquier <img src="https://render.githubusercontent.com/render/math?math=\large x\in X"> en <img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq)">, definiremos 

<img src="https://render.githubusercontent.com/render/math?math=\large \downarrow x = \{y : y \leq x \}">

<img src="https://render.githubusercontent.com/render/math?math=\large \uparrow x = \{y : x \leq y \}">

Sea <img src="https://render.githubusercontent.com/render/math?math=\large M\subset X">, definimos los siguientes conjuntos llamados _down-set_ y _up-set_ de <img src="https://render.githubusercontent.com/render/math?math=\large X">, respectivamente.

<img src="https://render.githubusercontent.com/render/math?math=\large \downarrow M=\cup_{x \in M}^{} \{\downarrow x \}">

<img src="https://render.githubusercontent.com/render/math?math=\large \uparrow M=\cup_{x \in M}^{} \{\uparrow x \}">

Una forma de usar estos conceptos es para definir **minimales** y **maximales**. Si <img src="https://render.githubusercontent.com/render/math?math=\large \{x\}"> es un _up-set_, entonces <img src="https://render.githubusercontent.com/render/math?math=\large x"> es maximal, si <img src="https://render.githubusercontent.com/render/math?math=\large \{x\}"> es un _down-set_, entonces <img src="https://render.githubusercontent.com/render/math?math=\large x"> es minimal. La relación inversa también se cumple para ambos. Ahora, definiremos **_lower bound_** (límite inferior) y **_upper bound_** (límite superior) de un subset <img src="https://render.githubusercontent.com/render/math?math=\large A\subset X">, dado <img src="https://render.githubusercontent.com/render/math?math=\large (X,\leq)">.  <img src="https://render.githubusercontent.com/render/math?math=\large x"> es un límite inferior de <img src="https://render.githubusercontent.com/render/math?math=\large A"> si <img src="https://render.githubusercontent.com/render/math?math=\large \forall y\in A (x\leq y)">; de forma análoga, <img src="https://render.githubusercontent.com/render/math?math=\large x"> es un límite superior de <img src="https://render.githubusercontent.com/render/math?math=\large A"> si <img src="https://render.githubusercontent.com/render/math?math=\large \forall y\in A (y\leq x)">. **Note** que, en estas definiciones, no es necesario que <img src="https://render.githubusercontent.com/render/math?math=\large x\in A">. Algunos autores definen <img src="https://render.githubusercontent.com/render/math?math=\large lb A"> y <img src="https://render.githubusercontent.com/render/math?math=\large ub A"> como los conjuntos de _lower bounds_ y _upper bounds_ de <img src="https://render.githubusercontent.com/render/math?math=\large A">.

A continuación hablaremos de **conjuntos direccionados**. Comunmente, se define como un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large D"> asociado con una relación <img src="https://render.githubusercontent.com/render/math?math=\large \leq"> que es reflexiva, transitiva, y cumple que <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y \in D (\exists z \in D)(x\leq z \land y\leq z)(x\neq y)">. Esta relación definida se conoce como **orden dirigido**. También se puede expresar como aquel subconjunto de (<img src="https://render.githubusercontent.com/render/math?math=\large X, \leq">) en el que cada subconjunto finito tiene un _upper bound_ en él; así, el conjunto se dice que es _up-directed_.

El **supremo** de un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large M\subset (X, \leq)"> es el menor límite superior de <img src="https://render.githubusercontent.com/render/math?math=\large M"> o, en inglés, el _least upper bound_. El **ínfimo** de <img src="https://render.githubusercontent.com/render/math?math=\large M"> es el mayor límite inferior de <img src="https://render.githubusercontent.com/render/math?math=\large M"> o el _greatest lower bound_, en inglés. Un subconjunto cualquiera no siempre tiene supremo e ínfimo, pero, si los tiene, son únicos.

Expresado en lógica, <img src="https://render.githubusercontent.com/render/math?math=\large s"> es el supremo de <img src="https://render.githubusercontent.com/render/math?math=\large M"> si 

1. <img src="https://render.githubusercontent.com/render/math?math=\large \forall m \in M (m\leq s)">
2. <img src="https://render.githubusercontent.com/render/math?math=\large \forall m \in M (m\leq x \Rightarrow s\leq x)">

Análogamente, <img src="https://render.githubusercontent.com/render/math?math=\large r"> es el ínfimo de <img src="https://render.githubusercontent.com/render/math?math=\large M"> si

1. <img src="https://render.githubusercontent.com/render/math?math=\large \forall m \in M (r\leq m)">
2. <img src="https://render.githubusercontent.com/render/math?math=\large \forall m \in M (x\leq m \Rightarrow x\leq r)"> 

El supremo también recibe el nombre de **join** de <img src="https://render.githubusercontent.com/render/math?math=\large M"> y el ínfimo recibe el nombre de **meet** de <img src="https://render.githubusercontent.com/render/math?math=\large M">. La notación de supremo es <img src="https://render.githubusercontent.com/render/math?math=\large sup M"> o <img src="https://render.githubusercontent.com/render/math?math=\large \vee M">, también se puede usar como operador binario para subconjuntos finitos (<img src="https://render.githubusercontent.com/render/math?math=\large a\lor b"> para el conjunto <img src="https://render.githubusercontent.com/render/math?math=\large \{a,b\}">). Por otro lado, se denota <img src="https://render.githubusercontent.com/render/math?math=\large inf M"> o <img src="https://render.githubusercontent.com/render/math?math=\large \wedge M"> al ínfimo de <img src="https://render.githubusercontent.com/render/math?math=\large M">, también se puede usar la notación de operador binario <img src="https://render.githubusercontent.com/render/math?math=\large a\land b">.

**Semilátices y Látices**

Un poset <img src="https://render.githubusercontent.com/render/math?math=\large X"> es llamado un _meet-semilátice_ (o _join-semilátice_) si existe un ínfimo <img src="https://render.githubusercontent.com/render/math?math=\large a\land b"> (o <img src="https://render.githubusercontent.com/render/math?math=\large a\lor b">) para cualquier <img src="https://render.githubusercontent.com/render/math?math=\large a,b\in X">.

Un poset <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un **látice** si existe un ínfimo y supremo para cualquier <img src="https://render.githubusercontent.com/render/math?math=\large a,b\in X">. Un **látice acotado** (también llamado _látice con 0 y 1_) es un poset que tiene un elemento mayor y un elemento menor. Donde, <img src="https://render.githubusercontent.com/render/math?math=\large a"> es el elemento mayor de <img src="https://render.githubusercontent.com/render/math?math=\large X"> si <img src="https://render.githubusercontent.com/render/math?math=\large \forall m \in X (m\leq a)">, el elemento menor se define análogamente.
Un lattice es **completo** si todos sus subconjuntos tienen supremo e ínfimo.

**Teorema del punto dijo de Knaster-Tarski**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large L"> un látice completo, entonces cada mapeo monótono <img src="https://render.githubusercontent.com/render/math?math=\large f : L\to L"> tiene un punto fijo <img src="https://render.githubusercontent.com/render/math?math=\large x\in L"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large f(x)=x">.

Una función monótona no decreciente es tal que si <img src="https://render.githubusercontent.com/render/math?math=\large x\leq y"> entonces <img src="https://render.githubusercontent.com/render/math?math=\large f(x)\leq f(y)">, una función monótona no creciente es aquella en la que si <img src="https://render.githubusercontent.com/render/math?math=\large x\leq y"> entonces <img src="https://render.githubusercontent.com/render/math?math=\large f(y)\leq f(x)">. El término _mapeo monótono_ se puede referir a cualquiera de los dos casos.

_Demostración del teorema del punto fijo_: (Picado y Pultr, 2011) Sea <img src="https://render.githubusercontent.com/render/math?math=\large M=\{x : x \leq f(x)\}"> y <img src="https://render.githubusercontent.com/render/math?math=\large s=sup M">. Si <img src="https://render.githubusercontent.com/render/math?math=\large x\in M"> entonces <img src="https://render.githubusercontent.com/render/math?math=\large x\leq s"> y, así, <img src="https://render.githubusercontent.com/render/math?math=\large x\leq f(x)\leq f(s)">. Así, <img src="https://render.githubusercontent.com/render/math?math=\large f(s)"> es un límite superior de <img src="https://render.githubusercontent.com/render/math?math=\large M">; por lo tanto <img src="https://render.githubusercontent.com/render/math?math=\large s\leq f(s)">, por lo tanto, <img src="https://render.githubusercontent.com/render/math?math=\large s\in M">.

Por lo tanto, si <img src="https://render.githubusercontent.com/render/math?math=\large x\in M">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large x\leq f(x)"> y así <img src="https://render.githubusercontent.com/render/math?math=\large f(x)\leq f(f(x))"> de modo que <img src="https://render.githubusercontent.com/render/math?math=\large f(x)\in M">. Por lo tanto, <img src="https://render.githubusercontent.com/render/math?math=\large f(s)\in M">, concluímos que <img src="https://render.githubusercontent.com/render/math?math=\large f(s)\leq s \leq f(s)">.


**Referencias**

- Judson, T. W. y Beezer R. A. (2017) Abstract Algebra: Theory and Applications.
- Picado, J., & Pultr, A. (2011). Frames and Locales: topology without points. Springer Science & Business Media.
- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.
