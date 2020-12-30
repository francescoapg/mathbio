[<<Home](https://francescoapg.github.io/mathbio/)

## Topología General

Los objetos que estudia la Topología son **espácios topológicos**, los cuales, en términos simples, son conjuntos con propiedades adicionales.

**Índice**

1. [Nociones Introductorias](#intro)
2. [Espacios Métricos](#met)
3. [Homeomorfismo](#homeo)
4. [Espacios Topológicos](#topospace)
5. [Retracción](#retraction)

### Nociones Introductorias {#intro}

Estudiar Topología es más sencillo con un ejemplo concreto como lo es <img src="https://render.githubusercontent.com/render/math?math=\large \R">.

**Definción**: Se llama **vecindad** de <img src="https://render.githubusercontent.com/render/math?math=\large x"> a un conjunto que incluye a un intervalo abierto que a su vez incluye a <img src="https://render.githubusercontent.com/render/math?math=\large x"> (Horváth, 1969).

**Definiciones**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large M"> un subconjunto de <img src="https://render.githubusercontent.com/render/math?math=\large \R">. Un punto <img src="https://render.githubusercontent.com/render/math?math=\large x\in \R"> es **punto interior** de <img src="https://render.githubusercontent.com/render/math?math=\large M"> si existe una vecindad <img src="https://render.githubusercontent.com/render/math?math=\large V"> de <img src="https://render.githubusercontent.com/render/math?math=\large x"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large V\subset M">. Un punto <img src="https://render.githubusercontent.com/render/math?math=\large x\in\R"> es un **punto exterior** a <img src="https://render.githubusercontent.com/render/math?math=\large M"> si existe una vecindad <img src="https://render.githubusercontent.com/render/math?math=\large V"> de <img src="https://render.githubusercontent.com/render/math?math=\large x"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large V\cap M=\emptyset">. Un punto <img src="https://render.githubusercontent.com/render/math?math=\large x\in\R"> es un punto de frontera (**boundary point**) si toda vecindad <img src="https://render.githubusercontent.com/render/math?math=\large V"> de <img src="https://render.githubusercontent.com/render/math?math=\large x"> cumple que <img src="https://render.githubusercontent.com/render/math?math=\large V\cap M\neq \emptyset \land V\setminus M\neq\emptyset"> (Horváth, 1969).

**Definición**: Un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large A"> de <img src="https://render.githubusercontent.com/render/math?math=\large \R"> es abierto si todos sus elementos son interiores (Horváth, 1969).

**Referencias**

- Horváth, J. (1969). Introducción a la topología general. Matemática. Monografía (OEA).

### Espacios Métricos {#met}

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

### Espacio Topológico {#topospace}

Primero, establecemos una serie de definiciones. Considera <img src="https://render.githubusercontent.com/render/math?math=\large (X, d)"> como un espacio métrico.

**Definición**:
Sea <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in X"> y <img src="https://render.githubusercontent.com/render/math?math=\large r"> un número real positivo. Entonces, la **bola abierta** con centro en <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> y radio <img src="https://render.githubusercontent.com/render/math?math=\large r"> se define como el conjunto <img src="https://render.githubusercontent.com/render/math?math=\large \{x\in X: d(x,x_0)<r\}">. Se denota como <img src="https://render.githubusercontent.com/render/math?math=\large B_r(x_0)"> o <img src="https://render.githubusercontent.com/render/math?math=\large B(x_0,r)">. Se llama tambíén la r-bola abierta alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large x_0">. Cuando se quiere dejar en claro la métrica se usa <img src="https://render.githubusercontent.com/render/math?math=\large B_d(x_0,r)">.
    
**Definición**:
Un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large A\subset X"> se dice que es **abierto** si para cada <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in A">, existe alguna bola abierta alrededor de <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> y esta es contenida en <img src="https://render.githubusercontent.com/render/math?math=\large A">, es decir, existe <img src="https://render.githubusercontent.com/render/math?math=\large 0<r"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large B(x_0,r)\subset A">.
    
**Definición**: 
Un **espacio topológico** es un par <img src="https://render.githubusercontent.com/render/math?math=\large (X,\mathcal{T})"> donde <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un conjunto y <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> es una familia de subconjuntos de <img src="https://render.githubusercontent.com/render/math?math=\large X"> que satisfacen que:

1. <img src="https://render.githubusercontent.com/render/math?math=\large \emptyset \in \mathcal{T}$ y $X\in \mathcal{T}">.
2. <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> es cerrado bajo uniones arbitrarias.
3. <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> es cerrado bajo intersecciones arbitrarias.

La familia<img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> se dice que es una topología del conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X">. Los miembros de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> se dice que son abiertos en <img src="https://render.githubusercontent.com/render/math?math=\large X"> o que son subconjuntos abiertos de <img src="https://render.githubusercontent.com/render/math?math=\large X">.

Nos damos cuenta, entonces, que el enfoque _métrico_ es solo una manera de definir topologías; sin embargo, en general, no es necesario.

**Bases de una Topología**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large (X, \mathcal{T})"> un espacio tológico. Una subfamilia <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{B}"> de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> se dice que es una base de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> si cada miembro de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{T}"> puede ser expresado como la unión de algunos miembros de <img src="https://render.githubusercontent.com/render/math?math=\large \mathcal{B}">.

**Vecindad**: Sea <img src="https://render.githubusercontent.com/render/math?math=\large (X,\mathcal{T})"> un espacio topológico, <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in X"> y <img src="https://render.githubusercontent.com/render/math?math=\large N\subset X">. Entonces, <img src="https://render.githubusercontent.com/render/math?math=\large N"> se dice que es una **vecindad** de <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> o <img src="https://render.githubusercontent.com/render/math?math=\large x_0"> es llamado **punto interior** de <img src="https://render.githubusercontent.com/render/math?math=\large N"> si hay un conjunto abierto <img src="https://render.githubusercontent.com/render/math?math=\large V"> tal que <img src="https://render.githubusercontent.com/render/math?math=\large x_0\in V"> y <img src="https://render.githubusercontent.com/render/math?math=\large V\subset N">.

**Cercanía (_Nearness_)**

Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> un conjunto. Una **relación de cercanía** en <img src="https://render.githubusercontent.com/render/math?math=\large X"> es un subconjunto <img src="https://render.githubusercontent.com/render/math?math=\large N"> de <img src="https://render.githubusercontent.com/render/math?math=\large X\times \wp(X)"> el cual satisface ciertas propiedades.
    
_Notación_: Para <img src="https://render.githubusercontent.com/render/math?math=\large y\in X"> y <img src="https://render.githubusercontent.com/render/math?math=\large A\in \wp (X)">, escribimos <img src="https://render.githubusercontent.com/render/math?math=\large y\delta A"> para referirnos a <img src="https://render.githubusercontent.com/render/math?math=\large (y,A)\in N"> y <img src="https://render.githubusercontent.com/render/math?math=\large y \overline{\epsilon}A"> para denotar <img src="https://render.githubusercontent.com/render/math?math=\large (y,A)\notin N">; <img src="https://render.githubusercontent.com/render/math?math=\large y\delta A"> se lee como <img src="https://render.githubusercontent.com/render/math?math=\large y"> está cerca a <img src="https://render.githubusercontent.com/render/math?math=\large A">.
    
_Propiedades_:

1. <img src="https://render.githubusercontent.com/render/math?math=\large y\overline{\delta}\emptyset"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large y\in X">.
2. <img src="https://render.githubusercontent.com/render/math?math=\large y\in A\implies y\delta A"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large y\in X">, <img src="https://render.githubusercontent.com/render/math?math=\large A\subset X">.
3. <img src="https://render.githubusercontent.com/render/math?math=\large y\delta (A\cup B)\iff y\delta A\lor y\delta B">, para todo <img src="https://render.githubusercontent.com/render/math?math=\large y\in X">, <img src="https://render.githubusercontent.com/render/math?math=\large A,B \subset X">.
4. Si <img src="https://render.githubusercontent.com/render/math?math=\large y\delta A"> y (<img src="https://render.githubusercontent.com/render/math?math=\large a\delta B"> para todo <img src="https://render.githubusercontent.com/render/math?math=\large a\in A">), entonces <img src="https://render.githubusercontent.com/render/math?math=\large y\delta B">, para todo <img src="https://render.githubusercontent.com/render/math?math=\large y\in X">, <img src="https://render.githubusercontent.com/render/math?math=\large A,B\subset X">.

**Referencias**

- Joshi, K. D. (1983). Introduction to general topology. New Age International.

### Retracción {#retraction}

Sea <img src="https://render.githubusercontent.com/render/math?math=\large X"> un espacio topológico y <img src="https://render.githubusercontent.com/render/math?math=\large A"> un subespacio de <img src="https://render.githubusercontent.com/render/math?math=\large X">. El mapeo (función continua)

<img src="https://render.githubusercontent.com/render/math?math=%5Ctau%20%3A%20X%20%5Cto%20A">

es una **retracción** si <img src="https://render.githubusercontent.com/render/math?math=%5Ctau_%7B%7CA%7D(x)%3Dx">.

**Referencias**
