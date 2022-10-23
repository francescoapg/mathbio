[<<Home](https://francescoapg.github.io/mathbio/)

<script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"> </script>
  
## Cálculo Avanzado

**Índice**

1. [Números Reales](#realnumb)

### Números Reales {#realnumb}

Los números reales son aquellos elementos del conjunto \\( \mathbb{R} \\), conocido como el **conjunto de números reales**. Estos elementos satisfacen una serie de axiomas que se agrupan en (1) propiedades algebraicas de los números reales, (2) propiedades de orden de los números reales y (3) axioma de completitud. Las propiedades algebraicas también se conocen como **axiomas de campo** pues definen a una estructura algebraica conocida como **campo** (_field_, en inglés). En efecto, los números reales junto con sus operaciones son un **campo**.

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

De este modo, se define a \\( \mathbb{R} \\) como un **campo ordenado** \\( (\mathbb{R},+,\cdot,<) \\). Además, \\( (\mathbb{R},<) \\) es un **conjunto totalmente ordenado**. De hecho,  \\( (\mathbb{Q},+,\cdot,<) \\) también es un campo ordenado, por ende, es necesario añadir una propiedad más a \\( \mathbb{R} \\) para diferenciarlo de \\(\mathbb{Q} \\), esta propiedad viene en la forma del axioma siguiente.

**Axioma de completitud**

Este axioma "completa" a los números racionales en números reales, dicho de otro modo, llena los espacios de los racionales y los expande en un conjunto completo.
Entre las formas de completitud que se tienen, las más conocidas son la **propiedad de la menor cota superior** (_Least Upper Bound property_) y la **completitud de Cauchy**. Dado que  \\( \mathbb{R} \\) satisface una forma del axioma de completitud, satisface todas. De este modo, solo es necesario enunciar una. A continuación, la propiedad de la menor cota superior:

- Todo conjunto no vacío que tienen una _cota superior_ posee una _menor cota superior_ (supremo).

Cabe resaltar que este axioma no es parte del conjunto original de axiomas que propuso Hilbert en su trabajo de 1900 titulado "Über den Zahlbegriff" (_Acerca del concepto de los números_) en el que propone los axiomas de los números reales que hemos presentado acá con algunas modificaciones. En lugar de este axioma, Hilbert propuso el _Axioma Arquimeadiano_ ("Archimedisches Axiom") y el _Axioma de completitud_ ("Axiom der Vollständigkeit") que establecía que no era posible expandir el sistema axiomático de los números reales, en otras palabras, los 18 axiomas que presentó estaban **completos**. De acuerdo a Hilbert, los números reales son un sistema de cosas cuyas relaciones satisfacen los axiomas presentados (Resnil, 1974).

Con esto,  \\( (\mathbb{R},+,\cdot,<) \\) se define como un **campo ordenado completo**.

Del axioma de completitud se desprende directamente que si un conjunto no vacío tiene una cota inferior, entonces tienen un infimo (mayor cota inferior).

**Definición** (D’angelo & West, 1997):  Une secuencia \\( \left{a_n\right}\\) de números reales tiene un **límite** \\( L\in\mathbb{R}\\) si, para todo \\( \epsilon >0\\) existe un \\( N\in\mathbb{N} \\) tal que \\( n\geq N\\) implica que \\( \|a_n-L\|<\epsilon \\).

Luego, una secuencia **converge** si tiene un límite. Consecuentemente, una secuencia divergente es aquella que no tiene un límite.

**Teorema de Convergencia Monótona**

- Si una secuencia \\( \{a_n\}\\) es creciente y acotada superiormente, entonces es convergente.

**Referencias**

- D’angelo, J. P., & West, D. B. (1997). Mathematical thinking. Problem Solving and Proofs.
- Hilbert, David. (1900) "Über den Zahlbegriff." Jahresbericht der Deutschen Mathematiker-Vereinigung 8: 180-183. <http://eudml.org/doc/144659>.
- Petrovic, J. (2013). Advanced calculus: theory and practice. Chapman and Hall/CRC.
- Resnik, M. D. (1974). The Frege-Hilbert controversy. Philosophy and Phenomenological Research, 34(3), 386-403.
