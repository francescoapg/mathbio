[<<Home](https://francescoapg.github.io/mathbio/)

## Funciones y relaciones

**Índice**

1. [Relaciones](#relaciones)
2. [Teorema de la función implícita](#teorema)
3. [Funciones](#funciones)

### Relaciones {#relaciones}

Una **partición** de un conjunto es un conjunto de subconjuntos del primero tal que para cualquier elemento de la partición, si dichos elementos son diferentes, entonces su intersección es vacía. Además, todos los elementos del conjunto inicial pertenecen a algún elemento de la partición.

Una relación de equivalencia es una relación reflexiva (<img src="https://render.githubusercontent.com/render/math?math=(%5Cforall%20a)%20(a%5Csim%20a)">), simétrica (<img src="https://render.githubusercontent.com/render/math?math=(%5Cforall%20a%2Cb)%20(a%5Csim%20b%20%5Cimplies%20b%5Csim%20a)">) y transitiva (<img src="https://render.githubusercontent.com/render/math?math=(%5Cforall%20a%2Cb%2Cc)%20(a%5Csim%20b%5Cland%20b%5Csim%20c%20%5Cimplies%20a%5Csim%20c)">). A partir de una relación de equivalencia definida en un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large A">, la clase de quivalencia de un elemento <img src="https://render.githubusercontent.com/render/math?math=\large a\in A "> es <img src="https://render.githubusercontent.com/render/math?math=%5Ba%5D%3A%3D%5C%7Bb%5Cin%20A%3Ab%5Csim%20a%5C%7D">.

Dada una relación de equivalencia en un set, su clase de equivalencia forma una partición en dicho set. Más aún, dad una partición <img src="https://render.githubusercontent.com/render/math?math=\large B"> de <img src="https://render.githubusercontent.com/render/math?math=\large A">, si definimos una relación <img src="https://render.githubusercontent.com/render/math?math=\large \sim"> como <img src="https://render.githubusercontent.com/render/math?math=\large a\sim b\iff \exists x \in B:a,b\in x"> entonces <img src="https://render.githubusercontent.com/render/math?math=\large \sim"> es una relación de equivalencia.

**Referencias**:

- Jost, J. (2015). Mathematical concepts. Springer International Publishing.


### Teorema de la función implícita {#teorema}

### Funciones {#funciones}

Sea <img src="https://render.githubusercontent.com/render/math?math=\large f"> una función de un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large A"> a otro conjunto <img src="https://render.githubusercontent.com/render/math?math=\large B">, denotamos <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B">. Esto implica que <img src="https://render.githubusercontent.com/render/math?math=\large f"> toma **todos** los elementos de <img src="https://render.githubusercontent.com/render/math?math=\large A"> y los lleva a <img src="https://render.githubusercontent.com/render/math?math=\large B">, en otras palabras, <img src="https://render.githubusercontent.com/render/math?math=\large rango(f)\subset B">.

Podemos tener cierta idea de igualdad de **funciones** como dos funciones que asocian los mismos elementos del conjunto de partida y el de llegada.

Una función parcial es una función cuyo dominio es un subconjunto del conjunto de partida. Dadas dos funciones parciales <img src="https://render.githubusercontent.com/render/math?math=\large f"> y <img src="https://render.githubusercontent.com/render/math?math=\large g"> definidas en los mismos conjuntos de partida y llegada, <img src="https://render.githubusercontent.com/render/math?math=\large f"> extiende a <img src="https://render.githubusercontent.com/render/math?math=\large g"> (<img src="https://render.githubusercontent.com/render/math?math=\large f\succeq g">) si el dominio de <img src="https://render.githubusercontent.com/render/math?math=\large f"> incluye al dominio de <img src="https://render.githubusercontent.com/render/math?math=\large g"> y <img src="https://render.githubusercontent.com/render/math?math=\large f(x)=g(x) \forall x \in dominio(g)">. Si <img src="https://render.githubusercontent.com/render/math?math=\large A"> es el dominio de <img src="https://render.githubusercontent.com/render/math?math=\large g">, se dice que <img src="https://render.githubusercontent.com/render/math?math=\large g"> es una restricción de <img src="https://render.githubusercontent.com/render/math?math=\large f"> o <img src="https://render.githubusercontent.com/render/math?math=\large f=g_{|A}"> (Srivastava, 2008).

**Función biyectiva**:
Sea <img src="https://render.githubusercontent.com/render/math?math=\large f: A\to B">. Una función biyectiva es aquella que es inyectiva (1 a 1) y surjectiva (onto) a la vez. Se puede probar también que <img src="https://render.githubusercontent.com/render/math?math=\large f"> admite una  inversa <img src="https://render.githubusercontent.com/render/math?math=\large f^{-1}"> si y solo si <img src="https://render.githubusercontent.com/render/math?math=\large f"> es biyectiva.

**Función inyectiva**: <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y\in A,f(x)=f(y)\implies x=y">

**Función suryectiva**: <img src="https://render.githubusercontent.com/render/math?math=\large \forall b\in B,\exists a \in A : f(a)=b">

Un importante resultado sobre composiciones de funciones establece que

- La composición de dos funciones inyectivas es inyectiva
- La composición de dos funciones suryectivas es suryecyiva
- La composición de dos funciones biyectivas es biyectiva.

**Función bien definida**

**Inversa**

Dada una función <img src="https://render.githubusercontent.com/render/math?math=\large f:X\to Y">, decimos que <img src="https://render.githubusercontent.com/render/math?math=\large f"> tiene una función inversa si existe una función <img src="https://render.githubusercontent.com/render/math?math=\large g:Y\to X"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large g\circ f =id_X"> y <img src="https://render.githubusercontent.com/render/math?math=\large f\circ g=id_Y">, en el primer caso, <img src="https://render.githubusercontent.com/render/math?math=\large g"> recibe el nombre de _left inverse_, mientras que en el segundo caso, recibe el nombre de _right inverse_. Si se cumple que existe una función <img src="https://render.githubusercontent.com/render/math?math=\large g" que sea tanto  _left_> como _right_ inversa, entonces <img src="https://render.githubusercontent.com/render/math?math=\large g"> recibe el nombre de _two-sided inverse_ o simplemente _inversa_.

Ten en cuenta de que <img src="https://render.githubusercontent.com/render/math?math=\large id_X:X\to X"> está definida como <img src="https://render.githubusercontent.com/render/math?math=\large id_X(x)=x"> para todo elemento de <img src="https://render.githubusercontent.com/render/math?math=\large X">. <img src="https://render.githubusercontent.com/render/math?math=\large id_Y"> está definido de forma análoga.

Las siguientes proposiciones son relevantes:

1. <img src="https://render.githubusercontent.com/render/math?math=\large f"> es injectiva si y solo si <img src="https://render.githubusercontent.com/render/math?math=\large f"> tiene _left inverse_.
2. <img src="https://render.githubusercontent.com/render/math?math=\large f"> es suryectiva si y solo si <img src="https://render.githubusercontent.com/render/math?math=\large f"> tiene _right inverse_.
3. <img src="https://render.githubusercontent.com/render/math?math=\large f"> es biyectiva si y solo si <img src="https://render.githubusercontent.com/render/math?math=\large f"> tiene inversa.

También se demuestra que si una función tiene inversa, entonces esta inversa es única y se usa la notación <img src="https://render.githubusercontent.com/render/math?math=\large f^{-1}">.

**Función continua** 

Existen varias definiciones de continuidad y tipos de continuidad. Una definición clásica es la siguiente:

Sean <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> subconjuntos de espacios euclideanos, <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B"> una función y <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in A">. Decimos que <img src="https://render.githubusercontent.com/render/math?math=\large f"> es **contínua** en <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> si para cada <img src="https://render.githubusercontent.com/render/math?math=\large \epsilon >0">, existe <img src="https://render.githubusercontent.com/render/math?math=\large \delta>0"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large d(f(x), f(x_0))<\epsilon"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large x\in A"> para el cual <img src="https://render.githubusercontent.com/render/math?math=\large d(x,x_0)<\delta">. Más aún, decímos que <img src="https://render.githubusercontent.com/render/math?math=\large f"> es contínua si es contínua en todo punto de <img src="https://render.githubusercontent.com/render/math?math=\large A">. (Joshi, 2008)

Una función contínua es comúnmente llamada **mapeo**, aunque también se puede tomar a un mapeo como una función general y a una _función_ se puede reservar para los sistemas de números.

Otra definición alternativa es la siguiente:

Una función de valores numéricos <img src="https://render.githubusercontent.com/render/math?math=\large f">, definida en un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large D">, es **contínua** en un punto <img src="https://render.githubusercontent.com/render/math?math=\large p_0\in D"> si, dado cualquier número <img src="https://render.githubusercontent.com/render/math?math=\large \epsilon>0">, existe una vecindad <img src="https://render.githubusercontent.com/render/math?math=\large N"> alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large p_0"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large |f(p)-f(p_0)|<\epsilon"> para cada punto <img src="https://render.githubusercontent.com/render/math?math=\large p\in N\cap D">. La función <img src="https://render.githubusercontent.com/render/math?math=\large f"> es contínua en <img src="https://render.githubusercontent.com/render/math?math=\large D"> si es contínua en todos los puntos de <img src="https://render.githubusercontent.com/render/math?math=\large D"> (Buck, 1978).

Es importante señalar que una función preserva la convergencia si y solo si es continua. La definición anterior se centra en funciones de valóres numéricos, las cuales, no son sino un pequeño grupo de funciones. La siguiente definición corresponde a funciones de forma general.

Sea <img src="https://render.githubusercontent.com/render/math?math=\large f"> una función definida como <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B">, tal que <img src="https://render.githubusercontent.com/render/math?math=\large A"> está incluído en un espacio <img src="https://render.githubusercontent.com/render/math?math=\large S"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> está incluído en un espacio <img src="https://render.githubusercontent.com/render/math?math=\large S^\star">. <img src="https://render.githubusercontent.com/render/math?math=\large f"> es continua en <img src="https://render.githubusercontent.com/render/math?math=\large p_0\in A"> si, dada cualquier vecindad <img src="https://render.githubusercontent.com/render/math?math=\large V"> alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large f(p_0)=q_0">, existe una vecindad <img src="https://render.githubusercontent.com/render/math?math=\large U"> alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large p_0"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large f(p)\in V"> siempre que <img src="https://render.githubusercontent.com/render/math?math=\large p\in U\cap A">. La función <img src="https://render.githubusercontent.com/render/math?math=\large f"> es continua en <img src="https://render.githubusercontent.com/render/math?math=\large A"> si es continua en cada elemento (_punto_) de <img src="https://render.githubusercontent.com/render/math?math=\large A"> (Buck, 1978).

**Continuidad uniforme**

**Definición**: Una función <img src="https://render.githubusercontent.com/render/math?math=\large f"> es uniformemente contínua en un **conjunto** <img src="https://render.githubusercontent.com/render/math?math=\large E"> si y solo si, correspondiendo a cada <img src="https://render.githubusercontent.com/render/math?math=\large \epsilon>0">, un número <img src="https://render.githubusercontent.com/render/math?math=\large \delta>0"> puede ser encontrado tal que <img src="https://render.githubusercontent.com/render/math?math=\large |f(p)-f(q)|<\epsilon"> siempre que <img src="https://render.githubusercontent.com/render/math?math=\large p"> y <img src="https://render.githubusercontent.com/render/math?math=\large q"> estén en <img src="https://render.githubusercontent.com/render/math?math=\large E"> y <img src="https://render.githubusercontent.com/render/math?math=\large |p-q|<\delta"> (Buck, 1978).

**Teorema**: (Buck, 1978) Si <img src="https://render.githubusercontent.com/render/math?math=\large E"> es un conjunto compacto y <img src="https://render.githubusercontent.com/render/math?math=\large f"> es continuo en <img src="https://render.githubusercontent.com/render/math?math=\large E">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large f"> es uniformemente contínuo en <img src="https://render.githubusercontent.com/render/math?math=\large E">.

Si <img src="https://render.githubusercontent.com/render/math?math=\large f"> es contínua en un conjunto compacto <img src="https://render.githubusercontent.com/render/math?math=\large E">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large f(E)"> es un conjunto compacto.


**Referencias**

- Awodey, S. (2010). Category theory. Oxford university press.
- Beck, M., & Geoghegan, R. (2011). The Art of Proof. Springer.
- Buck, R. C. (1978). Advanced calculus. McGraw-Hill, Inc.
- Humphreys, J. F. (1996). A course in group theory. Oxford University Press.
- Joshi, K. D. (1983). Introduction to general topology. New Age International.
- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.
