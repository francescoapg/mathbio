[<<Home](https://francescoapg.github.io/mathbio/)

## Funciones y relaciones

**Índice**

1. [Relaciones](#relaciones)
2. [Teorema de la función implícita](#teorema)
3. [Funciones](#funciones)

### Relaciones {#relaciones}

### Teorema de la función implícita {#teorema}

### Funciones {#funciones}

Una función parcial es una función cuyo dominio es un subconjunto del conjunto de partida. Dadas dos funciones parciales <img src="https://render.githubusercontent.com/render/math?math=\large f"> y <img src="https://render.githubusercontent.com/render/math?math=\large g"> definidas en los mismos conjuntos de partida y llegada, <img src="https://render.githubusercontent.com/render/math?math=\large f"> extiende a <img src="https://render.githubusercontent.com/render/math?math=\large g"> (<img src="https://render.githubusercontent.com/render/math?math=\large f\succeq g">) si el dominio de <img src="https://render.githubusercontent.com/render/math?math=\large f"> incluye al dominio de <img src="https://render.githubusercontent.com/render/math?math=\large g"> y <img src="https://render.githubusercontent.com/render/math?math=\large f(x)=g(x) \forall x \in dominio(g)">. Si <img src="https://render.githubusercontent.com/render/math?math=\large A"> es el dominio de <img src="https://render.githubusercontent.com/render/math?math=\large g">, se dice que <img src="https://render.githubusercontent.com/render/math?math=\large g"> es una restricción de <img src="https://render.githubusercontent.com/render/math?math=\large f"> o <img src="https://render.githubusercontent.com/render/math?math=\large f=g_{|A}"> (Srivastava, 2008).

**Función biyectiva**:
Sea <img src="https://render.githubusercontent.com/render/math?math=\large f: A\to B">. Una función biyectiva es aquella que es inyectiva (1 a 1) y surjectiva (onto) a la vez. Se puede probar también que <img src="https://render.githubusercontent.com/render/math?math=\large f"> admite una  inversa <img src="https://render.githubusercontent.com/render/math?math=\large f^{-1}"> si y solo si <img src="https://render.githubusercontent.com/render/math?math=\large f"> es biyectiva.

**Función inyectiva**: <img src="https://render.githubusercontent.com/render/math?math=\large x,y\in A,f(x)=f(y)\implies x=y">

**Función suryectiva**: <img src="https://render.githubusercontent.com/render/math?math=\large \forall b\in B,\exists a \in A : f(a)=b">

**Función continua** 

Existen varias definiciones de continuidad y tipos de continuidad. Una definición clásica es la siguiente:

Sean <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> subconjuntos de espacios euclideanos, <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B"> una función y <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in A">. Decimos que <img src="https://render.githubusercontent.com/render/math?math=\large f"> es **contínua** en <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> si para cada <img src="https://render.githubusercontent.com/render/math?math=\large \epsilon >0">, existe <img src="https://render.githubusercontent.com/render/math?math=\large \delta>0"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large d(f(x), f(x_0))<\epsilon"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large x\in A"> para el cual <img src="https://render.githubusercontent.com/render/math?math=\large d(x,x_0)<\delta">. Más aún, decímos que <img src="https://render.githubusercontent.com/render/math?math=\large f"> es contínua si es contínua en todo punto de <img src="https://render.githubusercontent.com/render/math?math=\large A">. (Joshi, 2008)

Una función contínua es comúnmente llamada **mapeo**.

Otra definición alternativa es la siguiente:

Una función de valores numéricos <img src="https://render.githubusercontent.com/render/math?math=\large f">, definida en un conjunto <img src="https://render.githubusercontent.com/render/math?math=\large D">, es **contínua** en un punto <img src="https://render.githubusercontent.com/render/math?math=\large p_0\in D"> si, dado cualquier número <img src="https://render.githubusercontent.com/render/math?math=\large \epsilon>0">, existe una vecindad <img src="https://render.githubusercontent.com/render/math?math=\large N"> alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large p_0"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large |f(p)-f(p_0)|<\epsilon"> para cada punto <img src="https://render.githubusercontent.com/render/math?math=\large p\in N\cap D">. La función <img src="https://render.githubusercontent.com/render/math?math=\large f"> es contínua en <img src="https://render.githubusercontent.com/render/math?math=\large D"> si es contínua en todos los puntos de <img src="https://render.githubusercontent.com/render/math?math=\large D"> (Buck, 1978).

Es importante señalar que una función preserva la convergencia si y solo si es continua. La definición anterior se centra en funciones de valóres numéricos, las cuales, no son sino un pequeño grupo de funciones. La siguiente definición corresponde a funciones de forma general.

Sea <img src="https://render.githubusercontent.com/render/math?math=\large f"> una función definida como <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B">, tal que <img src="https://render.githubusercontent.com/render/math?math=\large A"> está incluído en un espacio <img src="https://render.githubusercontent.com/render/math?math=\large S"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> está incluído en un espacio <img src="https://render.githubusercontent.com/render/math?math=\large S^\star">. <img src="https://render.githubusercontent.com/render/math?math=\large f"> es continua en <img src="https://render.githubusercontent.com/render/math?math=\large p_0\in A"> si, dada cualquier vecindad <img src="https://render.githubusercontent.com/render/math?math=\large V"> alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large f(p_0)=q_0">, existe una vecindad <img src="https://render.githubusercontent.com/render/math?math=\large U"> alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large p_0"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large f(p)\in V"> siempre que <img src="https://render.githubusercontent.com/render/math?math=\large p\in U\cap A">. La función <img src="https://render.githubusercontent.com/render/math?math=\large f"> es continua en <img src="https://render.githubusercontent.com/render/math?math=\large A"> si es continua en cada elemento (_punto_) de <img src="https://render.githubusercontent.com/render/math?math=\large A"> (Buck, 1978).

**Continuidad uniforme**

**Definición**: Una función <img src="https://render.githubusercontent.com/render/math?math=\large f"> es uniformemente contínua en un **conjunto** <img src="https://render.githubusercontent.com/render/math?math=\large E"> si y solo si, correspondiendo a cada <img src="https://render.githubusercontent.com/render/math?math=\large \epsilon>0">, un número <img src="https://render.githubusercontent.com/render/math?math=\large \delta>0"> puede ser encontrado tal que <img src="https://render.githubusercontent.com/render/math?math=\large |f(p)-f(q)|<\epsilon"> siempre que <img src="https://render.githubusercontent.com/render/math?math=\large p"> y <img src="https://render.githubusercontent.com/render/math?math=\large q"> estén en <img src="https://render.githubusercontent.com/render/math?math=\large E"> y <img src="https://render.githubusercontent.com/render/math?math=\large |p-q|<\delta"> (Buck, 1978).

**Teorema**: (Buck, 1978) Si <img src="https://render.githubusercontent.com/render/math?math=\large E"> es un conjunto compacto y <img src="https://render.githubusercontent.com/render/math?math=\large f"> es continuo en <img src="https://render.githubusercontent.com/render/math?math=\large E">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large f"> es uniformemente contínuo en <img src="https://render.githubusercontent.com/render/math?math=\large E">.

Si <img src="https://render.githubusercontent.com/render/math?math=\large f"> es contínua en un conjunto compacto <img src="https://render.githubusercontent.com/render/math?math=\large E">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large f(E)"> es un conjunto compacto.

**Función bien definida**



**Referencias**

- Srivastava, S. M. (2008). A course on Borel sets. Springer Science & Business Media.
- Joshi, K. D. (1983). Introduction to general topology. New Age International.
- Buck, R. C. (1978). Advanced calculus. McGraw-Hill, Inc.
