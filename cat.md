[<<Home](https://francescoapg.github.io/mathbio/)

## Categorias

Teoría de Categorías es el estudio del algebra de morfismos, en otras palabras, los morfismos son el corazón de esta teoría que incluso muchas veces los objetos simplemente existen para garantizar la definición de los morfismos. En una nota histórica, está teoría conoció la luz en 1945 con el trabajo _General theory of natural equivalences_ de Eilenberg y Mac Lane. Las primeras aplicaciones se vieron en Topología algebraica y Álgebra abstracta, aunque no tardó su uso en lógica, _computer science_ y muchas otras áreas. Actualmente se usa de forma casi tan extendidad como la Teoría de Conjuntos.

**Referencias**

- Awodey, S. (2010). Category theory. Oxford university press.

**Índice**

1. [Definiciones generales](#def)
2. [Functores](#funct)

### Definiciones generales {#def}

Una categoría <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> consiste en

- Una clase, denotada como <img src="https://render.githubusercontent.com/render/math?math=\large\mathcal{O}">_b_**(C)** cuyos miembros son llamados **objetos** de <img src=" https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">.
- Un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large M(X,Y)"> para cada par de objetos <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=\large Y"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> cuyos miembros son llamados **morfismos** o <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">-morfismos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> a <img src="https://render.githubusercontent.com/render/math?math=\large Y">. <img src="https://render.githubusercontent.com/render/math?math=\large M(X,Y)"> también es denotado por <img src="https://render.githubusercontent.com/render/math?math=\large Mor(X,Y)"> o por <img src="https://render.githubusercontent.com/render/math?math=\large Mor_{\mathcal{C}}(X,Y)">.
- Una función llamada composición <img src="https://render.githubusercontent.com/render/math?math=\large \circ_{X,Y,Z}: M(X,Y)\times M(Y,Z)\to M(X,Z)"> para cada triple de objetos <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=\large Y">, <img src="https://render.githubusercontent.com/render/math?math=\large Z"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">. Si <img src="https://render.githubusercontent.com/render/math?math=\large f\in M(X,Y)"> y <img src="https://render.githubusercontent.com/render/math?math=\large g\in M(Y,Z)">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large \circ_{X,Y,Z}(f,g)"> será denotado por <img src="https://render.githubusercontent.com/render/math?math=\large g\circ f">.
- Un elemento <img src="https://render.githubusercontent.com/render/math?math=\large 1_X\in M(X,X)"> para cada objeto <img src="https://render.githubusercontent.com/render/math?math=\large X"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> llamado **morfismo identidad** en <img src="https://render.githubusercontent.com/render/math?math=\large X">.

Los morfismos también son llamados _arrows_. La función composición de morfismos garantiza que estos se comporten de una forma similar a las funciones sin necesidad de serlo, se puede decir también que los morfismos son cerrados bajo composición.
Sea <img src="https://render.githubusercontent.com/render/math?math=\large 1_A"> y <img src="https://render.githubusercontent.com/render/math?math=\large 1_B"> los morfismos identidad de <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B">, respectivamente, por la función de composición, se demuestra que <img src="https://render.githubusercontent.com/render/math?math=\large f\circ 1_A =f=1_B\circ f">. Esto último en contraposición con las conmutatividad del elemento identidad en teoría de grupos (<img src="https://render.githubusercontent.com/render/math?math=\large 1_G\circ x=x\circ 1_G=x">).
Todos los elementos listados anteriormente cumplen con las siguientes condiciones:

- Los conjuntos de morfismos <img src="https://render.githubusercontent.com/render/math?math=\large M(X,Y)"> y <img src="https://render.githubusercontent.com/render/math?math=\large M(Z,W)"> son mutuamente disjuntos a menos que <img src="https://render.githubusercontent.com/render/math?math=\large X=Z"> y <img src="https://render.githubusercontent.com/render/math?math=\large Y=W"> para todos los objetos <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=\large Y">, <img src="https://render.githubusercontent.com/render/math?math=\large Z">, <img src="https://render.githubusercontent.com/render/math?math=\large W">.
- La composición es asociativa, es decir, para cualesquiera objetos <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=\large Y">, <img src="https://render.githubusercontent.com/render/math?math=\large Z">, <img src="https://render.githubusercontent.com/render/math?math=\large W"> y para cualesquiera <img src="https://render.githubusercontent.com/render/math?math=\large f \in Mor(X,Y)">, <img src="https://render.githubusercontent.com/render/math?math=\large g\in Mor(Y,Z)"> y <img src="https://render.githubusercontent.com/render/math?math=\large h\in Mor(Z,W)">, <img src="https://render.githubusercontent.com/render/math?math=\large \circ_{X,Z,W}(\circ_{X,Y,Z}(f,g),h)=\circ_{X,Y,W}(f, \circ_{Y,Z,W}(g,h))">, o, en notación simple, <img src="https://render.githubusercontent.com/render/math?math=\large h\circ (g\circ f)=(h\circ g)\circ f">.
- El morfismo identidad actúa como una identidad de dos caras, es decir, para cualesquira objetos, <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=\large Y">, <img src="https://render.githubusercontent.com/render/math?math=\large Z"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> y cualquier <img src="https://render.githubusercontent.com/render/math?math=\large f\in Mor(X,Y)"> y cualquier <img src="https://render.githubusercontent.com/render/math?math=\large g\in Mor(Y,Z)">, <img src="https://render.githubusercontent.com/render/math?math=\large 1_Y\circ f =f"> y <img src="https://render.githubusercontent.com/render/math?math=\large g\circ 1_Y=g">.


La totalidad de todos los objetos en una categoría no necesita formar un conjunto, es solamente una clase; sin embargo, para cualquier par de objetos, los morfismos de uno a otro deben fomar un conjunto.
Si dos objetos <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=\large Y"> pertenecen a más de una categoría a la vez, sea <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> y <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}">, entonces los respectivos conjuntos de morfismos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> a <img src="https://render.githubusercontent.com/render/math?math=\large Y"> son denotados por <img src="https://render.githubusercontent.com/render/math?math=\large M_{\mathcal{C}(X,Y)}"> y <img src="https://render.githubusercontent.com/render/math?math=\large M_{\mathcal{D}}(X,Y)">.
Si <img src="https://render.githubusercontent.com/render/math?math=\large f\in Mor (X,Y)"> entonces <img src="https://render.githubusercontent.com/render/math?math=\large X"> es llamado el **dominio** y <img src="https://render.githubusercontent.com/render/math?math=\large Y"> el **codominio** de <img src="https://render.githubusercontent.com/render/math?math=\large f">.
En lugar de escribir <img src="https://render.githubusercontent.com/render/math?math=\large f \in Mor(X,Y)"> también podemos escribir <img src="https://render.githubusercontent.com/render/math?math=\large f:X\to Y"> o <img src="https://render.githubusercontent.com/render/math?math=\large X\xrightarrow{f}Y">. <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large Y"> no requieren ser conjuntos e incluso si lo son, <img src="https://render.githubusercontent.com/render/math?math=\large f"> no necesariamente es una función.

Es importante resaltar el hecho de que, viendo los elementos de una categoría y las condiciones que cumplen, la mayoría del _stress_ es puesto en los morfismos y cómo se comportan. Para afianzar el hecho de que las _arrows_ no necesitan ser funciones, es posible definir una categoría en la que los objetos son conjuntos y las _arrows_ son matrices que toman como número de filas a la cardinalidad del dominio y como número de columnas a la cardinalidad del codominio.
Finalmente, ten en cuenta que no tiene sentido hablar de un morfismo o _arrow_ fuera del contexto de una categoría pues pierde propiedades, i.e., pierde su definición.

Durante la construcción de nuestra categoría, es usual establecer resticciones respecto a las composiciones como <img src="https://render.githubusercontent.com/render/math?math=\large (\forall f:A\to B,g:B\to A)(g\circ f=1_A\land f\circ g=1_B)"> para evitar composiciones infinitas como <img src="https://render.githubusercontent.com/render/math?math=\large f\circ g\circ f\circ g  ...">.

**Subcategoría**:

Una categoría <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> es llamada **subcategoría** de una categoría <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> si

- <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{O}">_b_**(D)**<img src="https://render.githubusercontent.com/render/math?math=\large \subset \mathcal{O}">_b_**(C)**, es decir, objetos de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> son también objetos de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">.
- Para cualesquiera objetos <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=\large Y"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}">, <img src="https://render.githubusercontent.com/render/math?math=\large Mor_{\mathcal{D}}(X,Y)\subset Mor_{\mathcal{C}}(X,Y)">.
- Para cualesquiera objetos <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=\large Y">, <img src="https://render.githubusercontent.com/render/math?math=\large Z"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> y <img src="https://render.githubusercontent.com/render/math?math=\large f\in Mor_{\mathcal{D}}(X,Y)">, <img src="https://render.githubusercontent.com/render/math?math=\large g\in Mor_{\mathcal{D}}(Y,Z)">, <img src="https://render.githubusercontent.com/render/math?math=\large g\circ f"> es el mismo morfismo de <img src="https://render.githubusercontent.com/render/math?math=\large X"> a <img src="https://render.githubusercontent.com/render/math?math=\large Z"> si la composición se lleva a cabo en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> o <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">.
- Para cualquier objeto <img src="https://render.githubusercontent.com/render/math?math=\large X"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}">, el morfismo identidad en <img src="https://render.githubusercontent.com/render/math?math=\large X"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> coincide con el de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">.

Si en la condición 2. de arriba tenemos igualdad en lugar de inclusión, entonces <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> es llamada una **subcategoría completa** de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">.

**Isomorfismo**:

Sea una categoría <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> cualesquiera, un morfismo <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B"> es un isomorfismo si existe un morfismo <img src="https://render.githubusercontent.com/render/math?math=\large g:A\to B"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large g\circ f=1_A"> y <img src="https://render.githubusercontent.com/render/math?math=\large f\circ g=1_B">.

Representamos esta relación como <img src="https://render.githubusercontent.com/render/math?math=\large A\cong B">.

**Epimorfismo**:

Sea una categoría <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> cualesquiera, un morfismo <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B"> es un epimorfismo si, dado cualquier par de morfismos <img src="https://render.githubusercontent.com/render/math?math=\large g,h:B\to C">, <img src="https://render.githubusercontent.com/render/math?math=\large g\circ f=h\circ f"> implica <img src="https://render.githubusercontent.com/render/math?math=\large g=h">.

**Monomorfismo**:

Sea una categoría <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> cualesquiera, un morfismo <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B"> es un epimorfismo si, dado cualquier par de morfismos <img src="https://render.githubusercontent.com/render/math?math=\large i,j:D\to A">, <img src="https://render.githubusercontent.com/render/math?math=\large f\circ i=f\circ j"> implica <img src="https://render.githubusercontent.com/render/math?math=\large i=j">.

**Categoría dual**:

Entre las formas de construir nuevas categorías sobre otrasse encuentran las categorías duales.
Sea <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> cualquier categoría. Definimos su categoría **dual** u **opuesta** <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}^{op}"> como sigue.
Los objetos de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}^{op}"> son los mismos que aquellos de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">. Sin embargo, para dos objetos <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large Y">, definimos <img src="https://render.githubusercontent.com/render/math?math=\large Mor_{\mathcal{C}^{op}}(X,Y)"> como <img src="https://render.githubusercontent.com/render/math?math=\large Mor_{\mathcal{C}}(Y,X)">. En otras palabras, intercambiamos el dominio y codominio de cada morfismo de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> y obtenemos un morfismo en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}^{op}">. La ley de composición también es cambiada consecuentemente.
Intuitivamente, las flechas en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}^{op}"> van en la dirección opuesta a aquellas de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">.

Como un ejemplo sencillo de categoría dual, vemos que si <img src="https://render.githubusercontent.com/render/math?math=\large (X,\leq)"> es un conjunto parcialmente ordenado considerado como categoría, entonces su dual es el conjunto parcialmente ordenado <img src="https://render.githubusercontent.com/render/math?math=\large (X, \geq)">. Estas categorías duales toman relevancia en teoremas de dualidad.

**Categoría morfismo**:

Una categoría **morfismo** o categoría _**arrow**_ <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}^{\to}"> de una categoría <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> toma a los morfismos de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> como objetos.

**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.
- Awodey, S. (2010). Category theory. Oxford university press.

### Functores {#funct}

Un functor <img src="https://render.githubusercontent.com/render/math?math=\large F:C\to D"> entre categorías <img src="https://render.githubusercontent.com/render/math?math=\large C"> y <img src="https://render.githubusercontent.com/render/math?math=\large D"> es un _mapeo_ (_whatever it means_) de objetos a ojetos y de morfismos a morfismos, de modo que

- <img src="https://render.githubusercontent.com/render/math?math=\large F(f:A\to B)=F(A)\to F(B)">.
- <img src="https://render.githubusercontent.com/render/math?math=\large F(1_A)=1_{F(A)}">.
- <img src="https://render.githubusercontent.com/render/math?math=\large F(g\circ f)=F(g)\circ F(f)">.

Notamos la similaridad a [homomorfismos](https://francescoapg.github.io/mathbio/groups#homomorphism) en la última condición.

**Functor covariante**

Sean <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">, <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> categorías. Un **functor covariante** <img src="https://render.githubusercontent.com/render/math?math=\large F"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> a <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> es una asociación que asigna a cada objeto <img src="https://render.githubusercontent.com/render/math?math=\large X"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> un objeto <img src="https://render.githubusercontent.com/render/math?math=\large F(X)"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> y a cada morfismo <img src="https://render.githubusercontent.com/render/math?math=\large f:X\to Y"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">, un morfismo <img src="https://render.githubusercontent.com/render/math?math=\large F(f):F(X)\to F(Y)"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> de tal modo que

- Para cualquier <img src="https://render.githubusercontent.com/render/math?math=\large f: X\to Y"> y <img src="https://render.githubusercontent.com/render/math?math=\large g: Y\to Z"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">, <img src="https://render.githubusercontent.com/render/math?math=\large F(g\circ f)=F(g)\circ F(f)"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}">.
- Para cualquier objeto <img src="https://render.githubusercontent.com/render/math?math=\large X"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">, <img src="https://render.githubusercontent.com/render/math?math=\large F(1_X)=1_{F(X)}"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}">.

Estas condiciones son llamadas propiedades functoriales.

**Functor contravariante**

Sean <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> y <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> categorías. Un **functor contravariante** <img src="https://render.githubusercontent.com/render/math?math=\large F"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> a <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> es una asociación que asigna a cada objeto <img src="https://render.githubusercontent.com/render/math?math=\large X"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> un objeto <img src="https://render.githubusercontent.com/render/math?math=\large F(X)"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> y a cada morfismo <img src="https://render.githubusercontent.com/render/math?math=\large f:X\to Y"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">, un morfismo <img src="https://render.githubusercontent.com/render/math?math=\large F(f):F(Y)\to F(X)"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}"> de tal modo que cumplen las siguientes propiedades functoriales

- Para cualquier <img src="https://render.githubusercontent.com/render/math?math=\large f:X\to Y"> y <img src="https://render.githubusercontent.com/render/math?math=\large g:Y \to Z"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">, <img src="https://render.githubusercontent.com/render/math?math=\large F(g\circ f)=F(f)\circ F(g)">.
- Para cualquier objeto <img src="https://render.githubusercontent.com/render/math?math=\large X"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">, <img src="https://render.githubusercontent.com/render/math?math=\large F(1_X)=1_{F(X)}"> en <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}">.

Es inmediato que la composición de dos functores covariantes o dos functores contravariantes es un functor covariante, mientras que la composición de un functor covariante y un contravariantes es contravariante.

Sea <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}^{op}"> la categoría opuesta de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}">. Entonces, existe un functor contravariante, <img src="https://render.githubusercontent.com/render/math?math=\large I:\mathcal{C}\to \mathcal{C}^{op}">, definido por <img src="https://render.githubusercontent.com/render/math?math=\large I(X)=X"> para todos los objetos <img src="https://render.githubusercontent.com/render/math?math=\large X"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> y <img src="https://render.githubusercontent.com/render/math?math=\large I(f)=f"> para todos los morfismos <img src="https://render.githubusercontent.com/render/math?math=\large f">. Dado cualquier functor <img src="https://render.githubusercontent.com/render/math?math=\large F"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> a la categoría <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{D}">, existe un functor único <img src="https://render.githubusercontent.com/render/math?math=\large F^{op}: \mathcal{C}^{op}\to \mathcal{D}"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large F^{op}\circ I=F">.

Claramente, <img src="https://render.githubusercontent.com/render/math?math=\large F"> es covariante si y solo si <img src="https://render.githubusercontent.com/render/math?math=\large F^{op}"> es contravariante.
    
Dado que las propiedades de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}"> son duales a aquellas de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{C}^{op}">, es consecuente que las propiedades de <img src="https://render.githubusercontent.com/render/math?math=\large F"> y <img src="https://render.githubusercontent.com/render/math?math=\large F^{op}"> son duales entre ellas tanto en cuanto al rol de la categoría dominio concierne.

**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.
- Awodey, S. (2010). Category theory. Oxford university press.
