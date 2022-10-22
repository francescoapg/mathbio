[<<Home](https://francescoapg.github.io/mathbio/)

<script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"> </script>
  
## Cálculo Avanzado

**Índice**

1. [Números Reales](#realnumb)

### Números Reales {#realnumb}

Los números reales son aquellos elementos del conjunto \\( \mathbb{R} \\), conocido como el **conjunto de números reales**. Estos elementos satisfacen una serie de axiomas que se agrupan en (1) propiedades algebraicas de los números reales y (2) propiedades de orden de los números reales. Las propiedades algebraicas también se conocen como **axiomas de campo** pues definen a una estructura algebraica conocida como **campo** (_field_, en inglés). En efecto, los números reales junto con sus operaciones son un **campo**.

**Axiomas de campo**

Definen dos operaciones binarias en  \\( \mathbb{R} \\) representadas con  \\( + \\) (suma) y  \\( \cdot \\) (multiplicación).

- Cerradura de la suma: \\( \forall a,b\in\mathbb{R},a+b\in\mathbb{R} \\)
- Cerradura de la multiplicación: \\( \forall a,b\in\mathbb{R},a\cdot b \in\mathbb{R} \\)
- Asociatividad de la suma: \\( \forall a,b,c\in\mathbb{R},(a + b) + c = a + (b + c) \\)
- Asociatividad de la multiplicación: \\( \forall a,b,c\in\mathbb{R}, (a\cdot b)\cdot c = a\cdot (b\cdot c) \\)
- Existencia del neutro aditivo: \\( \exists 0\in\mathbb{R}, x\in\mathbb{R}\implies x+0=0+x=x \\)
- Existencia del neutro multiplicativo: \\( \exists 1\in\mathbb{R}, x\in\mathbb{R}\implies x\cdot 1=1\cdot x=x \\)
- Inverso aditivo: \\( \forall a\in\mathbb{R}\exists -a\in\mathbb{R},a+-a=-a+a=0\\)
- Inverso multiplicativo: \\( \forall a\in\mathbb{R}\exists a^{-1}\in\mathbb{R},a\cdot a^{-1}=a^{-1}\cdot a=1\\) dado que \\( a\neq 0 \\).
- Conmutatividad de la suma: \\( \forall a,b\in\mathbb{R}, a+b=b+a\\)
- Conmutatividad de la multiplicación: \\( \forall a,b\in\mathbb{R}, a\cdot b=b\cdot a\\)
- Distributividad de la multiplicación sobre la suma: \\( \forall a,b,c\in\mathbb{R}, a\cdot (b+c)=a\cdot b + a\cdot c\\)

En base a esto se define al campo \\( (\mathbb{R},+,\cdot) \\). Tome en cuenta que el símbolo "\\( - \\)" en la existencia del inverso aditivo no es la operación de resta sino una parte del símbolo \\( -a\\) que representa al inverso aditivo de \\( a \\). Del mismo modo, el "exponente" \\( -1 \\) en la existencia del inverso multiplicativo no es una potencia de \\( a \\) sino es una parte del símbolo \\( a^{-1} \\) que representa al inverso multiplicativo de \\( a \\).

Tomando únicamente a la operación de suma, la estructura algebraica \\( (\mathbb{R},+) \\) es un grupo abeliano o conmutativo.

**Axiomas de orden**

Se define la relación de orden ( \\( < \\) ) en el conjunto  \\(  \mathbb{R} \\). Esta relación se define de acuerdo a

- Tricotomía: \\( \forall a,b\in\mathbb{R}, a<b \lor a=b \lor b<a \\)
- Transitividad: \\( \forall a,b,c \in \mathbb{R}, (a<b\land b<c)\implies a<c \\)
- Monotonía de la suma: \\( \forall a,b,c \in\mathbb{R} , a<b\implies a+c<b+c \\)
- Monotonía de la multiplicación: \\( \forall a,b,c\in\mathbb{R}, (a<b\land 0<c)\implies a\cdot c< b\cdot c \\)

De este modo, se define a \\( \mathbb{R} \\) como un **campo ordenado** \\( (\mathbb{R},+,\cdot,<) \\). Además, \\( (\mathbb{R},<) \\) es un **conjunto totalmente ordenado**.

**Referencias**

- Petrovic, J. (2013). Advanced calculus: theory and practice. Chapman and Hall/CRC.
