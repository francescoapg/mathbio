[<<Home](https://francescoapg.github.io/mathbio/)

## Biomatemática

**Índice**

1. [Introducción al modelamiento](#semana2)
2. Látices
3. Estructuras naturales

### Introducción al modelamiento {#semana2}

Nuestro foco de estudio será el modelamiento algebraico (no _cálculo_). Un Sistema Algebraico puede ser descrito como un conjunto de objetos junto con algunas operaciones para combinarlas. (Herstein, 1975) Por tal motivo, el primer paso para modelar un fenómeno natural con álgebra será tener cierto conocimiento de _Teoría de conjuntos_.

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

**Proposición**: Un conjunto de la forma <img src="https://render.githubusercontent.com/render/math?math=\footnotesize \langle \large a \footnotesize \rangle\large =\{a\circ b: b\in G\}"> donde <img src="https://render.githubusercontent.com/render/math?math=\large a"> es cualquier elemento de <img src="https://render.githubusercontent.com/render/math?math=\large G"> es un subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large G">.

_Demostración_: El elemento identidad está en <img src="https://render.githubusercontent.com/render/math?math=\footnotesize	 \langle \large a \footnotesize	 \rangle"> ya que <img src="https://render.githubusercontent.com/render/math?math=\large a^{-1}\in G">, la composición de dos elementos de <img src="https://render.githubusercontent.com/render/math?math=\footnotesize \langle \large a \footnotesize \rangle\large"> tendrá la forma <img src="https://render.githubusercontent.com/render/math?math=\large (a\circ b) \circ (a\circ c)">, esto es equivalente a <img src="https://render.githubusercontent.com/render/math?math=\large a\circ (b \circ a)\circ c">, por definición del grupo <img src="https://render.githubusercontent.com/render/math?math=\large G">, <img src="https://render.githubusercontent.com/render/math?math=\large b \circ a\in G"> por lo que lo reemplazaremos por <img src="https://render.githubusercontent.com/render/math?math=\large d">, ahora <img src="https://render.githubusercontent.com/render/math?math=\large a\circ (d \circ c)">, análogamente, sería equivalente a un <img src="https://render.githubusercontent.com/render/math?math=\large a\circ e">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large e"> algún elemento de <img src="https://render.githubusercontent.com/render/math?math=\large G">; esta última expresión cumple con la definición del conjunto por lo que está incluído en él. Para la existencia de la inversa de todos sus elementos considera que si <img src="https://render.githubusercontent.com/render/math?math=\large a,b\G"> entonces también su composición y también la inversa de su composición, por lo tanto <img src="https://render.githubusercontent.com/render/math?math=\large b^{-1}\circ a^{-1}\in G">, llamemos a este elemento como <img src="https://render.githubusercontent.com/render/math?math=\large c">, si <img src="https://render.githubusercontent.com/render/math?math=\large c"> pertenece a <img src="https://render.githubusercontent.com/render/math?math=\large G"> entonces <img src="https://render.githubusercontent.com/render/math?math=\large  a^{-1}\circ c"> también lo hace, llamemos a este último elemento como <img src="https://render.githubusercontent.com/render/math?math=\large d">. Ahora, los elementos de <img src="https://render.githubusercontent.com/render/math?math=\footnotesize \langle \large a \footnotesize \rangle\large"> tienen la forma general <img src="https://render.githubusercontent.com/render/math?math=\large a\circ x">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large x"> cualquier elemento de <img src="https://render.githubusercontent.com/render/math?math=\large G">, ya que <img src="https://render.githubusercontent.com/render/math?math=\large d"> es un elemento de <img src="https://render.githubusercontent.com/render/math?math=\large G">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large a\circ d \in \footnotesize \langle \large a \footnotesize \rangle">, operando este elemento, se prueba que <img src="https://render.githubusercontent.com/render/math?math=\large b^{-1}\circ a^{-1}\in\footnotesize \langle \large a \footnotesize \rangle">. 

**Referencias**

- Herstein, I. N. (1975). Topics in algebra. Second edition. Xerox Corporation.
- Judson, T. W. (2017) Abstract Algebra—Theory and Applications.
