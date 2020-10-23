[<<Home](https://francescoapg.github.io/mathbio/)

## Biomatemática

**Índice**

1. [Introducción al modelamiento](#semana2)
2. Latices
3. Estructuras naturales

### Introducción al modelamiento {#semana2}

Nuestro foco de estudio será el modelamiento algebraico (no _cálculo_). Un Sistema Algebraico puede ser descrito como un set de objetos junto con algunas operaciones para combinarlas. (Herstein, 1975) Por tal motivo, el primer paso para modelar un fenómeno natural con álgebra será tener cierto conocimiento de _Teoría de conjuntos_.

**Teoría de conjuntos**

Dentro de teoría de conjuntos clásica existen dos enfoques, el _naive_ o ingenuo y el axiomático. Para nuestros objetivos, nos conformaremos con el _naive_. Empezamos con las siguientes definiciones:

1. El símbolo <img src="https://render.githubusercontent.com/render/math?math=\in"> representa pertenencia, formalmente, es una relación entre un elemento y el conjunto que lo contiene. Por ejemplo, <img src="https://render.githubusercontent.com/render/math?math=a\in S"> significa que <img src="https://render.githubusercontent.com/render/math?math=a">
es un elemento de <img src="https://render.githubusercontent.com/render/math?math=S">. También se utiliza el símbolo <img src="https://render.githubusercontent.com/render/math?math=\notin"> para representar que un elemento **no** está en un conjunto.
2. Un conjunto se define de la siguiente manera: <img src="https://render.githubusercontent.com/render/math?math=A=\{x:P(x)\}">, donde <img src="https://render.githubusercontent.com/render/math?math=x"> representa a los elementos del conjunto y <img src="https://render.githubusercontent.com/render/math?math=P(x)"> significa que sus elementos cumplen la propiedad <img src="https://render.githubusercontent.com/render/math?math=P">. Todo junto se lee "A es un set cuyos elementos (<img src="https://render.githubusercontent.com/render/math?math=x">) cumplen <img src="https://render.githubusercontent.com/render/math?math=P(x)">".

Con estas dos definiciones ya podemos definir algunas otras relaciones y operaciones. Un conjunto <img src="https://render.githubusercontent.com/render/math?math=B"> es _subconjunto_ de <img src="https://render.githubusercontent.com/render/math?math=A"> si se cumple lo siguiente: <img src="https://render.githubusercontent.com/render/math?math= b \in B \implies b \in A">, en otras palabras, todo elemento de <img src="https://render.githubusercontent.com/render/math?math=B"> está en <img src="https://render.githubusercontent.com/render/math?math=A">. Esta relación se representa con el símbolo <img src="https://render.githubusercontent.com/render/math?math=\subset">, entonces, el enunciado anterior es equivalente a <img src="https://render.githubusercontent.com/render/math?math=B\subset A">.
Dicho esto, la _equivalencia de conjuntos_ se define como: <img src="https://render.githubusercontent.com/render/math?math=A=B\iff A\subset B \land B\subset A">. Con este concepto se hace una distinción entre subconjuntos y subconjuntos propios, un subconjunto propio es aquel subconjunto que no es equivalente al conjunto relacionado, es decir, si <img src="https://render.githubusercontent.com/render/math?math=B"> del ejemplo anterior fuese un subconjunto propio, debería existir algún elemento en <img src="https://render.githubusercontent.com/render/math?math=A"> que no pertenezca a <img src="https://render.githubusercontent.com/render/math?math=B">.






**Referencias**

- Herstein, I. N. (1975). Topics in algebra. Second edition. Xerox Corporation.
