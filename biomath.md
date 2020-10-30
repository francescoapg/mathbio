[<<Home](https://francescoapg.github.io/mathbio/)

## Biomatemática

**Índice**

1. [Estructuras algebraicas: Grupos](#semana2)
2. [Isomorfismos](#extra1)
3. [Homomorfismos](#extra2)
4. [Grupos abelianos finitos](#extra3)
5. [Látices y orden](#semana3)
6. Estructuras naturales

### Estructuras algebraicas: Grupos {#semana2}

Un Sistema Algebraico puede ser descrito como un conjunto de objetos junto con algunas operaciones para combinarlas. (Herstein, 1975) Por tal motivo, el primer paso comprender ese campo será tener cierto conocimiento de _Teoría de conjuntos_.

**Teoría de conjuntos**

Dentro de teoría de conjuntos clásica existen dos enfoques, el _naive_ o ingenuo y el axiomático. Para nuestros objetivos, nos conformaremos con el _naive_. Empezamos con las siguientes definiciones:

1. El símbolo <img src="https://render.githubusercontent.com/render/math?math=\in"> representa pertenencia, formalmente, es una relación entre un elemento y el conjunto que lo contiene. Por ejemplo, <img src="https://render.githubusercontent.com/render/math?math=\large a\in S"> significa que <img src="https://render.githubusercontent.com/render/math?math=\large a">
es un elemento de <img src="https://render.githubusercontent.com/render/math?math=\large S">. También se utiliza el símbolo <img src="https://render.githubusercontent.com/render/math?math=\notin"> para representar que un elemento **no** está en un conjunto.
2. Un conjunto se define de la siguiente manera: <img src="https://render.githubusercontent.com/render/math?math=\large A=\{x:P(x)\}">, donde <img src="https://render.githubusercontent.com/render/math?math=\large x"> representa a los elementos del conjunto y <img src="https://render.githubusercontent.com/render/math?math=\large P(x)"> significa que sus elementos cumplen la propiedad <img src="https://render.githubusercontent.com/render/math?math=\large P">. Todo junto se lee "A es un set cuyos elementos (<img src="https://render.githubusercontent.com/render/math?math=\large x">) cumplen <img src="https://render.githubusercontent.com/render/math?math=\large P(x)">".

Con estas dos definiciones ya podemos definir algunas otras relaciones y operaciones. Un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large B"> es _subconjunto_ de <img src="https://render.githubusercontent.com/render/math?math=\large A"> si se cumple lo siguiente: <img src="https://render.githubusercontent.com/render/math?math=\large b \in B \Rightarrow b \in A">, en otras palabras, todo elemento de <img src="https://render.githubusercontent.com/render/math?math=\large B"> está en <img src="https://render.githubusercontent.com/render/math?math=\large A">. Esta relación se representa con el símbolo <img src="https://render.githubusercontent.com/render/math?math=\subset">, entonces, el enunciado anterior es equivalente a <img src="https://render.githubusercontent.com/render/math?math=\large B\subset A">.

Dicho esto, la _equivalencia de conjuntos_ se define como: <img src="https://render.githubusercontent.com/render/math?math=\large A=B\iff A\subset B \land B\subset A">. Con este concepto se hace una distinción entre subconjuntos y subconjuntos propios, un subconjunto propio es aquel subconjunto que no es equivalente al conjunto relacionado, es decir, si <img src="https://render.githubusercontent.com/render/math?math=\large B"> del ejemplo anterior fuese un subconjunto propio, debería existir algún elemento en <img src="https://render.githubusercontent.com/render/math?math=\large A"> que no pertenezca a <img src="https://render.githubusercontent.com/render/math?math=\large B">.

A continuación, definiremos la unión de dos conjuntos, la cual se representa de la siguiente manera: <img src="https://render.githubusercontent.com/render/math?math=\large A\cup B = \{x:x\in A \lor x\in B\}">. La definición de intersection es similar: <img src="https://render.githubusercontent.com/render/math?math=\large A\cap B = \{x:x\in A \land x\in B\}">.

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

### Isomorfismos {#extra1}

Entre las "herramientas" que se usan para estudiar grupos están los isomorfismos; con ellos, se pueden econtrar semejanzas entre grupos que a primera vistas parecen disímiles.

**Definición**: (Judson, 2017) Dos grupos <img src="https://render.githubusercontent.com/render/math?math=\large (G, \bullet )"> y <img src="https://render.githubusercontent.com/render/math?math=\large (H, \circ )"> son isomórficos si existe un mapeo biyectivo (suryectivo e inyectivo) <img src="https://render.githubusercontent.com/render/math?math=\large \phi : G \to H">, tal que <img src="https://render.githubusercontent.com/render/math?math=\large \phi (a \bullet b)=\phi (a)\circ \phi (b)"> para cualesquiera elementos <img src="https://render.githubusercontent.com/render/math?math=\large a,b\in G">, es decir, se preservan las operaciones entre grupos. El mapa <img src="https://render.githubusercontent.com/render/math?math=\large \phi"> es llamado isomorfismo.

Note que el isomorfismo anterior está definido de <img src="https://render.githubusercontent.com/render/math?math=\large G"> hacia <img src="https://render.githubusercontent.com/render/math?math=\large H">; sin embargo, se puede probar que <img src="https://render.githubusercontent.com/render/math?math=\large \phi ^{-1}"> también es un isomorfismo. Observe también que dos grupos pueden tener dos o más isomorfismos distintos definidos entre ellos. 

Entre las consecuencias de tener definidos isomorfismos tenemos que, tal que exista un isomorfismo <img src="https://render.githubusercontent.com/render/math?math=\large \phi : G \to H"> entre dos grupos, si el primero es abeliano, el segundo también lo es; si el primero es cíclico, el segundo también lo es, y, si el primero tiene un subgrupo de orden <img src="https://render.githubusercontent.com/render/math?math=\large n">, el segundo también. Como caso especial, todos los grupos cíclicos de orden infinito son isomórficos a <img src="https://render.githubusercontent.com/render/math?math=%5Cmathbb%7B%20Z%20%7D">.

**Teorema**: La relación de isomorfismos entre grupos es una relación de equivalencia en la clase de todos los grupos.

Así es como el objetivo de la teoría de grupos se torna hacia estas clases de equivalencia generadas dentro de la clase de todos los grupos. Dentro del estudio de ellos surge otro teorema muy importante.

**Teorema de Cayley**: (_Teorema de representación_) Todo grupo es isomórfico a un grupo de permutaciones.

El isomorfismo entre ellos recibe el nombre de **representación regular izquierda** del grupo (<img src="https://render.githubusercontent.com/render/math?math=\large G">).

**Producto directo externo**

Considera el producto cartesiano de los conjuntos de dos grupos (<img src="https://render.githubusercontent.com/render/math?math=\large G \times H">), es posible definir la siguiente ley de composición dentro de este nuevo conjunto: <img src="https://render.githubusercontent.com/render/math?math=\large (g_1,h_1) \diamond (g_2,h_2)=(g_1\bullet g_2,h_1\circ h_2)">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large g_1, g_2\in G"> y <img src="https://render.githubusercontent.com/render/math?math=\large h_1,h_2\in H"> y <img src="https://render.githubusercontent.com/render/math?math=\large \bullet ,\circ"> sus respectivas leyes de composiciones. Se demuestra que <img src="https://render.githubusercontent.com/render/math?math=\large (G\times H , \diamond)"> es un grupo y es llamado _producto directo externo_ de <img src="https://render.githubusercontent.com/render/math?math=\large G"> y <img src="https://render.githubusercontent.com/render/math?math=\large H">. De forma general, 

<img src="https://render.githubusercontent.com/render/math?math=%5Clarge%0A%5Cprod_%7Bi%3D1%7D%5E%7Bn%7DG_%7Bi%7D%3DG_%7B1%7D%5Ctimes%20G_%7B2%7D%5Ctimes%20...%20%20%5Ctimes%20G_%7Bn%7D">

es el producto directo externo de los grupos <img src="https://render.githubusercontent.com/render/math?math=\large G_1, G_2,...,G_n">.

**Producto directo interno**

En el caso anterior construímos un grupo más grande a partir de dos grupos pequeños, en este caso veremos una situación inversa: dividiremos un grupo como el producto de dos subgurpos. Primero consideraremos dos subgrupos <img src="https://render.githubusercontent.com/render/math?math=\large H"> y <img src="https://render.githubusercontent.com/render/math?math=\large K"> de <img src="https://render.githubusercontent.com/render/math?math=\large G"> que cumplan con las siguientes condiciones (Judson, 2017).

1. <img src="https://render.githubusercontent.com/render/math?math=\large G=HK=\{hk:h\in H, k\in K \}">
2. <img src="https://render.githubusercontent.com/render/math?math=\large H\cap K =\{e\}">
3. <img src="https://render.githubusercontent.com/render/math?math=\large hk=kh \forall k \in K, h\in H">.

Entonces <img src="https://render.githubusercontent.com/render/math?math=\large G"> es el _producto directo interno_ de <img src="https://render.githubusercontent.com/render/math?math=\large H"> y <img src="https://render.githubusercontent.com/render/math?math=\large K">. El siguiente teorema enlaza los conceptos de productos directos internos y externos.

**Teorema**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large G"> el producto directo interno de sus subgrupos <img src="https://render.githubusercontent.com/render/math?math=\large H"> y <img src="https://render.githubusercontent.com/render/math?math=\large K">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large G"> es isomórfico a <img src="https://render.githubusercontent.com/render/math?math=\large H\times K">.

Toma en cuanta, también, que no todos los grupos pueden ser descompuestos por el producto interno directo. Finalmente, las condiciones del producto directo interno también pueden ser generalizadas a <img src="https://render.githubusercontent.com/render/math?math=\large n"> subgrupos, al igual que el teorema anterior.

Finalmente, recuerda que un **automorfismo** es un isomorfismo de un objeto matemático hacia sí mismo.

**Referencias**

- Judson, T. W. (2017) Abstract Algebra: Theory and Applications.

### Homomorfismos {#extra2}

Un homomorfismo entre dos grupos <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )"> y <img src="https://render.githubusercontent.com/render/math?math=\large (H,\bullet )"> es un mapa <img src="https://render.githubusercontent.com/render/math?math=\large \phi : G\to H">, definido como <img src="https://render.githubusercontent.com/render/math?math=%5Cphi%20(g_1%20%5Ccirc%20g_2)%3D%5Cphi%20(g_1)%5Cbullet%20%5Cphi%20(g_2)"> para cualesquiera elementos <img src="https://render.githubusercontent.com/render/math?math=\large g_1, g_2\in G">.

A diferencia de los isomorfismos, los homomorfismos no requieren ser biyecciones y, por lo tanto, se consideran una generalización del concepto de isomorfismo.

Para un homomorfismo entre dos grupos, se cumple que se preserva el elemento identidad, es decir, si <img src="https://render.githubusercontent.com/render/math?math=\large e"> es la identidad en <img src="https://render.githubusercontent.com/render/math?math=\large G">, entoces <img src="https://render.githubusercontent.com/render/math?math=\large \phi (e)"> es la identidad de <img src="https://render.githubusercontent.com/render/math?math=\large H">. Además, para cualquier elemento del grupo <img src="https://render.githubusercontent.com/render/math?math=\large G"> se cumple que <img src="https://render.githubusercontent.com/render/math?math=\large \phi (g^{-1})=(\phi (g)^{-1})">. Finalmente, cuando se aplica la función a todos los elementos de un subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large G">, el conjunto de llegada en <img src="https://render.githubusercontent.com/render/math?math=\large H"> es también un subgrupo, lo inverso también se cumple.

Otro concepto asociado es el de núcleo o **kernel** del homomorfismo, este está definido como el conjunto <img src="https://render.githubusercontent.com/render/math?math=\large ker \phi = \{g\in G : \phi(g)=e_H\}">, donde <img src="https://render.githubusercontent.com/render/math?math=\large e_H"> es el elemento identidad de <img src="https://render.githubusercontent.com/render/math?math=\large H">. Para un homomorfismo entre grupos, el kernel de <img src="https://render.githubusercontent.com/render/math?math=\large \phi"> es siempre un subgrupo normal.

A continuación veremos los teoremas de isomorfismos para grupos (existe una versión de estos para cada estructra algebraica).

**Teorema del Homomorfismo**: Dado el homomorfismo <img src="https://render.githubusercontent.com/render/math?math=\large \varphi :  G \to H">. Sea <img src="https://render.githubusercontent.com/render/math?math=\large \phi : G \to G/Ker\varphi"> el homomorfismo canónico, entonces <img src="https://render.githubusercontent.com/render/math?math=\large G/Ker\varphi"> y <img src="https://render.githubusercontent.com/render/math?math=\large \varphi (G)"> son isomórficos y ese isomorfismo es único.

Este teorema también es conocido por algunos como Primer teorema de isomorfismos o teorema fundamental de homomorfismos.

**Teorema del Isomorfismo**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large (H,\circ )"> un subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )"> y <img src="https://render.githubusercontent.com/render/math?math=\large (N,\circ )"> un subgrupo normal de <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )">. Entonces, 
- <img src="https://render.githubusercontent.com/render/math?math=\large (HN,\circ )"> es un subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )">
- <img src="https://render.githubusercontent.com/render/math?math=\large (H\cap N,\circ)"> es un subgrupo normal de <img src="https://render.githubusercontent.com/render/math?math=\large (H,\circ )">
- <img src="https://render.githubusercontent.com/render/math?math=\large (H/(H\cap N), \circ)"> y <img src="https://render.githubusercontent.com/render/math?math=\large (HN/N, \circ )"> son isomórficos.

**Teorema de correspondencia**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large (N,\circ )"> un subgrupo normal de un grupo <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )">, <img src="https://render.githubusercontent.com/render/math?math=%5Cmathcal%7BN%7D"> el conjunto de subgrupos de subgrupos de <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )"> que contienen a <img src="https://render.githubusercontent.com/render/math?math=\large (N,\circ )"> y <img src="https://render.githubusercontent.com/render/math?math=%5Cmathcal%7BG%7D"> el conjunto de subgrupos de <img src="https://render.githubusercontent.com/render/math?math=\large G/N">. Entonces, <img src="https://render.githubusercontent.com/render/math?math=%5Cphi%20%3A%20%5Cmathcal%7BN%7D%20%5Cto%20%5Cmathcal%7BG%7D"> es un mapeo inyectivo.

**Referencias**

- Judson, T. W. y Beezer R. A. (2017) Abstract Algebra: Theory and Applications.

### Grupos abelianos finitos {#extra3}

<img src="https://render.githubusercontent.com/render/math?math=%5Cmathbb%7BZ%7D_n"> es el conjunto de clases de equivalencia de los enteros _mod n_. La clase de equivalencia se define por la relación <img src="https://render.githubusercontent.com/render/math?math=\large \sim"> definida como <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b \in \mathbb{Z} (n\text{ divide }a-b\Rightarrow a \sim b)">. Por ejemplo, los enteros módulo 7 (<img src="https://render.githubusercontent.com/render/math?math=%5Cmathbb%7BZ%7D_7">) consiste en el conjunto <img src="https://render.githubusercontent.com/render/math?math=%5C%7B%5B0%5D%2C%20%5B1%5D%2C%20...%2C%20%5B6%5D%5C%7D">, donde:

<img src="https://render.githubusercontent.com/render/math?math=%5B0%5D%3D%5C%7B...%2C%20-14%2C-7%2C0%2C7%2C14%2C%20...%5C%7D%0A">

<img src="https://render.githubusercontent.com/render/math?math=%5B1%5D%3D%5C%7B...%2C%20-13%2C-6%2C1%2C8%2C15%2C%20...%5C%7D%0A">

...

<img src="https://render.githubusercontent.com/render/math?math=%5B6%5D%3D%5C%7B...%2C%20-8%2C-1%2C6%2C13%2C20%2C%20...%5C%7D%0A">

Algunas operaciones en <img src="https://render.githubusercontent.com/render/math?math=%5Cmathbb%7BZ%7D_7">, definimos la suma módulo _n_ como el resto de la división de la suma y _n_. Análogamente se puede definir la multiplicación módulo _n_.

Se demuestra que todo grupo de orden primo era un grupo cíclico e isomórfico a <img src="https://render.githubusercontent.com/render/math?math=%5Cmathbb%7BZ%7D_p">, donde _p_ es un número primo. También se demuestra que todo grupo abeliano finito es isomórfico al producto directo de grupos cíclicos de orden primo.

**Generador de grupo**

Sea <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> un grupo y <img src="https://render.githubusercontent.com/render/math?math=\large \{g_i\}\in G (i \in I)">, para un <img src="https://render.githubusercontent.com/render/math?math=\large I"> arbitrario. El subgrupo más pequeño de <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> que contiene a <img src="https://render.githubusercontent.com/render/math?math=\large \{g_i\}"> es el subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> generado por los elementos de <img src="https://render.githubusercontent.com/render/math?math=\large \{g_i\}">. Si este subgrupo es todo el grupo, entonces se dice que <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> está generado por <img src="https://render.githubusercontent.com/render/math?math=\large \{gi : i\in I\}"> y cada <img src="https://render.githubusercontent.com/render/math?math=\large g_i"> es un **generador** del grupo, si el conjunto es finito, se dice que <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> es finitamente generado. En especial, todos los grupos finitos son finitamente generados.

Lo anterior se puede expresar como una proposición.

**Proposición**: (Judson y Beezer, 2017) Sea <img src="https://render.githubusercontent.com/render/math?math=\large H"> el subgrupo de un grupo <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> que es generado por <img src="https://render.githubusercontent.com/render/math?math=\large \{g_i\in G : i\in I\}">. Entonces <img src="https://render.githubusercontent.com/render/math?math=\large h\in H"> si y solo si puede ser expresado como un producto de la forma 

<img src="https://render.githubusercontent.com/render/math?math=\large h=g_{i1}^{\alpha 1}\circ ... \circ g_{in}^{\alpha n}">

donde los <img src="https://render.githubusercontent.com/render/math?math=\large g_{ik}"> no necesariamente son diferentes.

**p-grupo**

Un grupo <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> es un **p-grupo** si todos los elementos de su conjunto tienen como orden a una potencia de un número primo (_p_). Recuerda que el orden de un **elemento** _g_ es el mínimo exponente que resuelve ecuación <img src="https://render.githubusercontent.com/render/math?math=\large a^n=e (n\in \mathbb{N})">, donde <img src="https://render.githubusercontent.com/render/math?math=\large e"> es el elemento identidad, cuando no existe tal número, se dice que el elemento tiene orden infinito.

Los _Teoremas de Sylow_ son los siguientes. Sea <img src="https://render.githubusercontent.com/render/math?math=\large p"> un número primo, <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )"> un grupo finito y <img src="https://render.githubusercontent.com/render/math?math=%7CG%7C"> el orden de <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )">.

1. Si <img src="https://render.githubusercontent.com/render/math?math=\large p"> divide <img src="https://render.githubusercontent.com/render/math?math=%7CG%7C">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )"> tiene un _p-subgrupo de Sylow_.
2. En un grupo finito, todos los _p-subgrupos de Sylow_ son conjugados de algún <img src="https://render.githubusercontent.com/render/math?math=\large p">.
3. El número de _p-subgrupos de Sylow_ para un <img src="https://render.githubusercontent.com/render/math?math=\large p"> fijo es congruente a <img src="https://render.githubusercontent.com/render/math?math=\large 1"> (_mod_ <img src="https://render.githubusercontent.com/render/math?math=\large p">).

Recuerda que para un subgrupo <img src="https://render.githubusercontent.com/render/math?math=\large (H,\circ )"> de <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )">, su subgrupo conjugado será de la forma <img src="https://render.githubusercontent.com/render/math?math=\large (gHg^{-1},\circ )">, dado un <img src="https://render.githubusercontent.com/render/math?math=\large g\in G">. 

**Teorema fundamental de los grupos abelianos finitos**: (Judson y Beezer, 2017) Cada grupo abeliano finito es isomórfico al producto directo de grupos cíclicos de la forma

<img src="https://render.githubusercontent.com/render/math?math=%5Cmathbb%7BZ%7D_%7Bp_1%5E%7B%5Calpha_1%7D%7D%5Ctimes%5Cmathbb%7BZ%7D_%7Bp_2%5E%7B%5Calpha_2%7D%7D%5Ctimes%20...%20%5Ctimes%20%5Cmathbb%7BZ%7D_%7Bp_n%5E%7B%5Calpha_n%7D%7D">

donde los <img src="https://render.githubusercontent.com/render/math?math=\large p_i">s son primos, no necesariamente distintos.

A continuacón, la forma más general del teorema.

**Teorema fundamental de los grupos abelianos finitamente generados**: (Judson y Beezer, 2017) Cada grupo abeliano finitamente generado es isomórfico al producto directo de grupos cíclicos de la forma

<img src="https://render.githubusercontent.com/render/math?math=%5Cmathbb%7BZ%7D_%7Bp_1%5E%7B%5Calpha_1%7D%7D%5Ctimes%5Cmathbb%7BZ%7D_%7Bp_2%5E%7B%5Calpha_2%7D%7D%5Ctimes%20...%20%5Ctimes%20%5Cmathbb%7BZ%7D_%7Bp_n%5E%7B%5Calpha_n%7D%7D%5Ctimes%20%5Cmathbb%7BZ%7D%5Ctimes%20%0A%20...%5Ctimes%20%5Cmathbb%7BZ%7D">

donde los <img src="https://render.githubusercontent.com/render/math?math=\large p_i">s son primos, no necesariamente distintos.

**Grupos solubles**

Una serie subnormal de un grupo <img src="https://render.githubusercontent.com/render/math?math=\large G"> es una secuencia finita de subgrupos

<img src="https://render.githubusercontent.com/render/math?math=G%3DH_n%5Csupset%20H_%7Bn-1%7D%5Csupset%20...%20%5Csupset%20H_1%20%5Csupset%20H_0%20%3D%20%5C%7Be%5C%7D">

, donde <img src="https://render.githubusercontent.com/render/math?math=\large H_i"> es un subgrupo normal de <img src="https://render.githubusercontent.com/render/math?math=\large H_{i+1}">. Si cada subgrupo es normal en <img src="https://render.githubusercontent.com/render/math?math=\large G">, entonces la serie es llamada **serie normal**. La longitud de cada serie se calcula como el número de inclusiones propias.

**Referencias**

- Judson, T. W. y Beezer R. A. (2017) Abstract Algebra: Theory and Applications.

### Látices y orden {#semana3}

Empezamos esta sección con una nota sobre conjuntos parcialmente ordenados o **posets**. Un orden parcial en un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X"> es una relación binaria entre elementos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> que satisface lo siguiente.

1. <img src="https://render.githubusercontent.com/render/math?math=\large \forall a \in R (aRa)">
2. <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b,c \in R (aRb\land bRc \Rightarrow aRc)">
3. <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b\in R (aRb\land bRa \Rightarrow a=b)">

La primera condición recibe el nombre de reflexividad, la segunda, transitividad, y la tercera, antisimetría. Una relación de orden también puede cumplir que <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b\in R (aRb \lor bRa)">, si se cumple esta condición, la relación se dice que es un orden **lineal** o **total**. De este modo, un conjunto asociado a un orden parcial se llama _conjunto parcialmente ordenado_ o _poset_, y un conjunto asociado a un orden total se llama _conjunto linealmente ordenado_ o _totalmente ordenado_. 

Cuando un conjunto totalmente ordenado es subconjunto (subposet) de un poset, recibe el nombre de **cadena**. Si una relación de orden solo cumple 1. y 2., se conoce como _preorden_, y al objeto matemático asociado se lo conoce como _conjunto preordenado_. Nuevamente, es posible identificar un subconjunto dentro de este objeto que cumpla condiciones adicionales (como 3.), esto puede ser logrado al definir una clase de equivalencia dentro del conjunto asociada al preorden (<img src="https://render.githubusercontent.com/render/math?math=\large a\sim b \iff aRb \land bRa">). En algunos casos, identificar esta relación <img src="https://render.githubusercontent.com/render/math?math=\large \sim"> puede ser muy importante para el estudio.

Respecto a la notación, solemos usar los siguientes símbolos para referirnos a la relación de orden (y preorden).

<img src="https://render.githubusercontent.com/render/math?math=\large \leq, \preceq, \prec, \sqsubseteq">

El símbolo <img src="https://render.githubusercontent.com/render/math?math=\large <"> se reserva para el caso <img src="https://render.githubusercontent.com/render/math?math=\large a \leq b \land a\neq b">.

Se puede generar un conjunto ordenado a partir de otro mediante el **orden dual** u **orden opuesto**. Dado, <img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq)"> un poset, entonces 
<img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq ^{\ast})"> también es un conjunto odenado si se cumple que <img src="https://render.githubusercontent.com/render/math?math=\large \forall a,b \in X (a \leq ^{\ast} b \iff b \leq a)">. Otra forma de representar <img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq ^{\ast})"> es mediante los símbolos <img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq)^{op}"> o <img src="https://render.githubusercontent.com/render/math?math=\large X^{op}">.

**Ten en cuenta que todo poset puede ser representado como una colección de sets ordenados por la relación de inclusión**.

A continuación definiremos otros conjuntos importantes en el estudio de posets. Para cualquier <img src="https://render.githubusercontent.com/render/math?math=\large x\in X"> en <img src="https://render.githubusercontent.com/render/math?math=\large (X, \leq)">, definiremos 

<img src="https://render.githubusercontent.com/render/math?math=\large \downarrow x = \{y : y \leq x \}">

<img src="https://render.githubusercontent.com/render/math?math=\large \uparrow x = \{y : x \leq y \}">

Sea <img src="https://render.githubusercontent.com/render/math?math=\large M\subset X">, definimos los siguientes conjuntos llamados _down-set_ y _up-set_ de <img src="https://render.githubusercontent.com/render/math?math=\large X">, respectivamente.

<img src="https://render.githubusercontent.com/render/math?math=\large \downarrow M=\cup_{x \in M}^{} \{\downarrow x \}">

<img src="https://render.githubusercontent.com/render/math?math=\large \uparrow M=\cup_{x \in M}^{} \{\uparrow x \}">

Una forma de usar estos conceptos es para definir **minimales** y **maximales**. Si <img src="https://render.githubusercontent.com/render/math?math=\large \{x\}"> es un _up-set_, entonces <img src="https://render.githubusercontent.com/render/math?math=\large x"> es maximal, si <img src="https://render.githubusercontent.com/render/math?math=\large \{x\}"> es un _down-set_, entonces <img src="https://render.githubusercontent.com/render/math?math=\large x"> es minimal. La relación inversa también se cumple para ambos. Ahora, definiremos **_lower bound_** (límite inferior) y **_upper bound_** (límite superior) de un subset <img src="https://render.githubusercontent.com/render/math?math=\large A\subset X">, dado <img src="https://render.githubusercontent.com/render/math?math=\large (X,\leq)">.  <img src="https://render.githubusercontent.com/render/math?math=\large x"> es un límite inferior de <img src="https://render.githubusercontent.com/render/math?math=\large A"> si <img src="https://render.githubusercontent.com/render/math?math=\large \forall y\in A (x\leq y)">; de forma análoga, <img src="https://render.githubusercontent.com/render/math?math=\large x"> es un límite superior de <img src="https://render.githubusercontent.com/render/math?math=\large A"> si <img src="https://render.githubusercontent.com/render/math?math=\large \forall y\in A (y\leq x)">. **Note** que, en estas definiciones, no es necesario que <img src="https://render.githubusercontent.com/render/math?math=\large x\in A">. Algunos autores definen <img src="https://render.githubusercontent.com/render/math?math=\large lb A"> y <img src="https://render.githubusercontent.com/render/math?math=\large ub A"> como los conjuntos de _lower bounds_ y _upper bounds_ de <img src="https://render.githubusercontent.com/render/math?math=\large A">.

A continuación hablaremos de **conjuntos direccionados**. Comunmente, se define como un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large D"> asociado con una relación <img src="https://render.githubusercontent.com/render/math?math=\large \leq"> que es reflexiva, transitiva, y cumple que <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y \in D (\exists z \in D)(x\leq z \land y\leq z)(x\neq y)">. Esta relación definida se conoce como **orden dirigido**. También se puede expresar como aquel subconjunto de (<img src="https://render.githubusercontent.com/render/math?math=\large X, \leq">) en el que cada subconjunto finito tiene un _upper bound_ en él; así, el conjunto se dice que es _up-directed_.

**Referencias**

- Picado, J., & Pultr, A. (2011). Frames and Locales: topology without points. Springer Science & Business Media.
- Judson, T. W. y Beezer R. A. (2017) Abstract Algebra: Theory and Applications.

