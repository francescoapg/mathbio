[<<Home](https://francescoapg.github.io/mathbio/)

## Teoría de grupos

**Índice**

1. [Isomorfismos](#isomorphism)
2. [Homomorfismos](#homomorphism)
3. [Grupos abelianos finitos](#finiteab)
4. [Acción de grupos](#groupact)

### Isomorfismos {#isomorphism}

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

### Homomorfismos {#homomorphism}

Un homomorfismo entre dos grupos <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )"> y <img src="https://render.githubusercontent.com/render/math?math=\large (H,\bullet )"> es un mapa <img src="https://render.githubusercontent.com/render/math?math=\large \phi : G\to H">, definido como <img src="https://render.githubusercontent.com/render/math?math=%5Cphi%20(g_1%20%5Ccirc%20g_2)%3D%5Cphi%20(g_1)%5Cbullet%20%5Cphi%20(g_2)"> para cualesquiera elementos <img src="https://render.githubusercontent.com/render/math?math=\large g_1, g_2\in G">.

A diferencia de los isomorfismos, los homomorfismos no requieren ser biyecciones y, por lo tanto, se consideran una generalización del concepto de isomorfismo.

Para un homomorfismo entre dos grupos, se cumple que se preserva el elemento identidad, es decir, si <img src="https://render.githubusercontent.com/render/math?math=\large e"> es la identidad en <img src="https://render.githubusercontent.com/render/math?math=\large G">, entoces <img src="https://render.githubusercontent.com/render/math?math=\large \phi (e)"> es la identidad de <img src="https://render.githubusercontent.com/render/math?math=\large H">. Además, para cualquier elemento del grupo <img src="https://render.githubusercontent.com/render/math?math=\large G"> se cumple que <img src="https://render.githubusercontent.com/render/math?math=\large \phi (g^{-1})=(\phi (g)^{-1})">. Finalmente, cuando se aplica la función a todos los elementos de un subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large G">, el conjunto de llegada en <img src="https://render.githubusercontent.com/render/math?math=\large H"> es también un subgrupo, lo inverso también se cumple.

Otro concepto asociado es el de núcleo o **kernel** del homomorfismo, este está definido como el conjunto <img src="https://render.githubusercontent.com/render/math?math=\large ker \phi = \{g\in G : \phi(g)=e_H\}">, donde <img src="https://render.githubusercontent.com/render/math?math=\large e_H"> es el elemento identidad de <img src="https://render.githubusercontent.com/render/math?math=\large H">. Para un homomorfismo entre grupos, el kernel de <img src="https://render.githubusercontent.com/render/math?math=\large \phi"> es siempre un subgrupo normal. Como vimos, el kernel de un homomorfismo siempre incluirá al elemento identidad; si el homomorfismo es inyecto, el kenerl contendrá solo al elemento identidad.

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

### Grupos abelianos finitos {#finiteab}

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

Los _Teoremas de Sylow_ son los siguientes (Weisstein, Eric W., 2020). Sea <img src="https://render.githubusercontent.com/render/math?math=\large p"> un número primo, <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )"> un grupo finito y <img src="https://render.githubusercontent.com/render/math?math=%7CG%7C"> el orden de <img src="https://render.githubusercontent.com/render/math?math=\large (G,\circ )">.

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

, donde <img src="https://render.githubusercontent.com/render/math?math=\large H_i"> es un subgrupo normal de <img src="https://render.githubusercontent.com/render/math?math=H_%7Bi%2B1%7D">. Si cada subgrupo es normal en <img src="https://render.githubusercontent.com/render/math?math=\large G">, entonces la serie es llamada **serie normal**. La longitud de cada serie se calcula como el número de inclusiones propias.

Una serie normal (subnormal) <img src="https://render.githubusercontent.com/render/math?math=%5C%7BM_j%5C%7D"> es un _refinamiento de una serie normal (subnormal)_ <img src="https://render.githubusercontent.com/render/math?math=%5C%7BN_i%5C%7D"> si <img src="https://render.githubusercontent.com/render/math?math=%5C%7BN_i%5C%7D%5Csubset%5C%7BM_j%5C%7D">.

Dos series normales (subnormales) <img src="https://render.githubusercontent.com/render/math?math=%5C%7BH_i%5C%7D"> y <img src="https://render.githubusercontent.com/render/math?math=%5C%7BK_j%5C%7D"> de un grupo son isomórficas si hay una correspondencia 1-1 entre las colecciones de grupos factores <img src="https://render.githubusercontent.com/render/math?math=%5C%7BH_%7Bi%2B1%7D%2FH_i%5C%7D"> y <img src="https://render.githubusercontent.com/render/math?math=%5C%7BK_%7Bj%2B1%7D%2FK_j%5C%7D">.

Una serie subnormal <img src="https://render.githubusercontent.com/render/math?math=\large \{H_i\}"> de un grupo es una **serie de composición** si todos los grupos factores son simples (solo tienen grupos normales triviales). Una serie normal <img src="https://render.githubusercontent.com/render/math?math=\large \{H_i\}"> de un grupo es una **serie principal** si todos los grupos factores son simples.

**Teorema de Jordan-Hölder**: Cualquier par de series de composición de un grupo son isomórficas.

Como corolario, ambas series de composición tienen la misma longitud. 

Un grupo es **soluble** si tiene una serie subnormal <img src="https://render.githubusercontent.com/render/math?math=\large \{H_i\}"> con grupos factores <img src="https://render.githubusercontent.com/render/math?math=%5C%7BH_%7Bi%2B1%7D%2FH_i%5C%7D"> abelianos.

**Referencias**

- Judson, T. W. y Beezer R. A. (2017) Abstract Algebra: Theory and Applications.
- Weisstein, Eric W. (2020) "Sylow Theorems." From MathWorld--A Wolfram Web Resource. https://mathworld.wolfram.com/SylowTheorems.html

### Acción de grupos {#groupact}

Sea <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> un grupo y <img src="https://render.githubusercontent.com/render/math?math=\large X"> un conjunto. Una **acción (izquierda)** de <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ )"> en <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un mapeo <img src="https://render.githubusercontent.com/render/math?math=\large \phi : G \times X \to X"> dado por <img src="https://render.githubusercontent.com/render/math?math=\large (g,x_1) \mapsto x_2">, donde se cumple para todo elemento de <img src="https://render.githubusercontent.com/render/math?math=\large X"> que

1. <img src="https://render.githubusercontent.com/render/math?math=\large \forall x \in X,e\in G (\phi (e,x)=x)">
2. <img src="https://render.githubusercontent.com/render/math?math=\large \forall x \in X, \forall g_1,g_2\in G (\phi(\phi(g_1, g_2), x) = \phi (g_1 , \phi (g_2, x))">

Se considera al conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X"> como un *G-conjunto*.

Si <img src="https://render.githubusercontent.com/render/math?math=\large G"> actúa sobre un set <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large x,y\in X">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large x"> se dice que es **G-equivalente** a <img src="https://render.githubusercontent.com/render/math?math=\large y"> si existe un elemento <img src="https://render.githubusercontent.com/render/math?math=\large g"> en <img src="https://render.githubusercontent.com/render/math?math=\large G"> para el que <img src="https://render.githubusercontent.com/render/math?math=\large gx=y">.

**Proposición**: (Judson y Beezer, 2017) Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> un _G-conjunto_, entonces _G-equivalencia_ es una relación de equivalencia en <img src="https://render.githubusercontent.com/render/math?math=\large X">.

Cada partición generada en <img src="https://render.githubusercontent.com/render/math?math=\large X"> por la relación de equivalencia es llamada una **órbita** de <img src="https://render.githubusercontent.com/render/math?math=\large X"> bajo <img src="https://render.githubusercontent.com/render/math?math=\large G">. La notación para estos conjuntos será <img src="https://render.githubusercontent.com/render/math?math=%5Cmathcal%7BO%7D_x">, donde <img src="https://render.githubusercontent.com/render/math?math=\large x"> es un elemento de este conjunto.

Dada la notación anterior, el **conjunto de punto fijo** de <img src="https://render.githubusercontent.com/render/math?math=\large g"> en <img src="https://render.githubusercontent.com/render/math?math=\large X">, denotado como <img src="https://render.githubusercontent.com/render/math?math=\large X_g">, será el subconjunto de <img src="https://render.githubusercontent.com/render/math?math=\large X"> que cumpla con la condición <img src="https://render.githubusercontent.com/render/math?math=\large gx=x">.

De forma análoga se puede definir el subconjunto de <img src="https://render.githubusercontent.com/render/math?math=\large G"> que fija un elemento <img src="https://render.githubusercontent.com/render/math?math=\large x"> de <img src="https://render.githubusercontent.com/render/math?math=\large X">, es decir, el conjunto

<img src="https://render.githubusercontent.com/render/math?math=\large G_x=\{g\in G : gx=x \}">

Se prueba que este conjunto es un subgrupo de <img src="https://render.githubusercontent.com/render/math?math=\large (G, \circ)">. Este subgrupo es llamado **subgrupo estabilizador** de <img src="https://render.githubusercontent.com/render/math?math=\large x"> y, en algunos contextos, **subgrupo isotrópico**.

**Teorema**: (Judson y Beezer, 2017) Sea <img src="https://render.githubusercontent.com/render/math?math=\large G"> un grupo finito y <img src="https://render.githubusercontent.com/render/math?math=\large X"> un G-conjunto finito. Si <img src="https://render.githubusercontent.com/render/math?math=\large x\in X">, entonces <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%7C%5Cmathcal%7BO%7D_x%7C%3D%5BG%3AG_x%5D">.

**Referencias**

- Judson, T. W. y Beezer R. A. (2017) Abstract Algebra: Theory and Applications.
