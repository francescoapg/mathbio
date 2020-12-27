[<<Home](https://francescoapg.github.io/mathbio/)

## Topología General

Los objetos que estudia la Topología son \textbf{espácios topológicos}, los cuales, en términos simples, son conjuntos con propiedades adicionales.

**Índice**

1. [Espacios métricos](#met)
2. [Homeomorfismo](#homeo)
3. [Retracción](#retraction)

### Espacios métricos {#met}

Los espacios métricos son una generalización del espacio euclidiano.

**Definición**

Un espacio euclidiano es un par <img src="https://render.githubusercontent.com/render/math?math=\large (X,d)">, tal que <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un conjunto y <img src="https://render.githubusercontent.com/render/math?math=\large d"> una función de distancia abstracta definida como <img src="https://render.githubusercontent.com/render/math?math=\large d:X\times X \to \R">, de modo que se cumplen las siguientes condiciones para cualesquiera puntos <img src="https://render.githubusercontent.com/render/math?math=\large x,y,z"> de <img src="https://render.githubusercontent.com/render/math?math=\large X">.

- (M1) <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y \in X,d(x,y)\geq 0">
- (M1.5) <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y\in X, x=y\iff d(x,y)=0">
- (M2) <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y\in X, d(x,y)=d(y,x)">
- (M3) <img src="https://render.githubusercontent.com/render/math?math=\large \forall x,y,z\in X, d(x,y)+d(y,z)\geq d(x,z)">

Estas condiciones se llaman positividad, simetría e inecualidad triangular.

**Convergencia de secuencias**

Una secuencia <img src="https://render.githubusercontent.com/render/math?math=\large \{x_n\}"> en un espacio métrico <img src="https://render.githubusercontent.com/render/math?math=\large (X,d)"> se dice que **converge** a un punto <img src="https://render.githubusercontent.com/render/math?math=\large y"> en <img src="https://render.githubusercontent.com/render/math?math=\large X"> si para cada <img src="https://render.githubusercontent.com/render/math?math=\large \epsilon>0"> existe un entero positivo <img src="https://render.githubusercontent.com/render/math?math=\large N"> tal que para todos los enteros <img src="https://render.githubusercontent.com/render/math?math=\large n\geq N">, <img src="https://render.githubusercontent.com/render/math?math=\large d(x_n,y)<\epsilon">.


**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.

### Homeomorfismo {#homeo}

Ser homeomórficos es una relación de equivalencia en la clase de todos los espacios topológicos. Una propiedad o un atributo de un objeto, que es invariante ante homeomorfismos, se dice que es topológica en caracter. Estas propiedades algunas veces son denominadas invariantes topológicas.

**Definición**: Sean <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> de subconjuntos de espacios euclidianos. Un homeomorfismo entre <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> es una [biyección](https://francescoapg.github.io/mathbio/functlations#funciones) <img src="https://render.githubusercontent.com/render/math?math=\large f:A\to B"> tal que tanto <img src="https://render.githubusercontent.com/render/math?math=\large f"> como su inversa son continuos. Cuando tal <img src="https://render.githubusercontent.com/render/math?math=\large f"> existe, se dice que <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> son homeomórficos entre ellos.

El mapa de identidad (<img src="https://render.githubusercontent.com/render/math?math=\large i">) es el ejemplo más sencillo de homeomorfismo. La inversa de un homeomorfismo y la composición de dos homeomofismos también lo son.

**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.

### Retracción {#retraction}

Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> un espacio topológico y <img src="https://render.githubusercontent.com/render/math?math=\large A"> un subespacio de <img src="https://render.githubusercontent.com/render/math?math=\large X">. El mapeo (función continua)

<img src="https://render.githubusercontent.com/render/math?math=%5Ctau%20%3A%20X%20%5Cto%20A">

es una **retracción** si <img src="https://render.githubusercontent.com/render/math?math=%5Ctau_%7B%7CA%7D(x)%3Dx">.

**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.

