[<<Home](https://francescoapg.github.io/mathbio/)

## Álgebra Lineal

**Índice**

1. [Introducción](#intro)
2. [Matrices y Ecuaciones Lineales](#matrx)

### Introducción {#intro}

El foco principal del Álgebra Lineal son las **combinaciones lineales**, estas son combinaciones de dos operaciones básicas que son la multiplicación escalar y la suma. Sea <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w"> dos vectores, y <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b"> dos números. <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20av%2Bbw"> es una combinación lineal de <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w">. Estas dos operaciones llevan vectores a vectores, es decir, todo resultado de una combinación lineal es un vector.

La suma de vectores y la multiplicación escalar siguen algunas reglas muy sencillas. En el caso de la **suma de vectores**, son las siguientes:

- Los vectores deben tener la misma dimensión.
- <img src="https://render.githubusercontent.com/render/math?math=\large a_{ij}"> del primer vector se sumará solo con <img src="https://render.githubusercontent.com/render/math?math=\large b_{ij}"> del segundo vector y visceversa. En otras palabras, la suma se realiza de forma sistemática y ordenada de acuerdo a las posiciones de los elementos de los vectores.
- <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20v%2Bw%3Dw%2Bv">.

Por su parte, la **multiplicación escalar**, el valor a multiplicar, llámese <img src="https://render.githubusercontent.com/render/math?math=\large k"> deberá ser multiplicado en todas las posiciones de la matriz o vector. En otras palabras, si la matriz está formada por <img src="https://render.githubusercontent.com/render/math?math=\large a_{ij}"> elementos, luego de la multiplicación escalar, estará formada por <img src="https://render.githubusercontent.com/render/math?math=\large ka_{ij}"> elementos.

Naturalmente, la "resta" de los vectores <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w"> deberá ser entendida como la siguiente combinación lineal: <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20v%2B(-1)w">.

Ahora bien, ¿qué pasaría si tienes a todas las combinaciónes lineales de un vector de dimensión 3?. En otras palabras, si en <img src="https://render.githubusercontent.com/render/math?math=\large c v">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large v"> el vector, <img src="https://render.githubusercontent.com/render/math?math=\large c"> pudiese tomar cualquier valor. Es claro que este caso sería el de una línea con dirección <img src="https://render.githubusercontent.com/render/math?math=\large v">. Si tomamos dos vectores linealmente independientes de dimensión 3, <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w">, todas las combinaciones lineales llenarán un plano. De forma análoga, tres vectores linealmente idependientes llenarán todo el espacio tridimensional. Un acotación importante es que ninguno de los vectores mencionados debe ser el vector cero (_zero vector_). Combinación lineales del vector cero serán el mismo vector además, toda línea o plano que pase por el origen comprenderá al vector cero.

La siguiente operación entre vectores es llamada **producto punto** o **producto interno**. Esta operación se representa como <img src="https://render.githubusercontent.com/render/math?math=\large v\cdot w"> y tiene como resultado a un número. La fórmula general es <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20v_%7B11%7Dw_%7B11%7D%2B...%2Bv_%7Bij%7Dw_%7Bij%7D%2B...%2Bv_%7Bmn%7Dw_%7Bmn%7D">. El producto punto es interesante por su interpretación geométrica. Por ejemplo, si el producto punto de dos vectores es 0, esto implica que ambos vectores son perpendiculares, es decir, el ángulo entre ellos es de 90°. De forma general, sea <img src="https://render.githubusercontent.com/render/math?math=\large \theta"> el ángulo entre el vector <img src="https://render.githubusercontent.com/render/math?math=\large u"> y <img src="https://render.githubusercontent.com/render/math?math=\large v">, <img src="https://render.githubusercontent.com/render/math?math=\large cos(\theta)=(||u||||v||)^{-1}u\cdot v">. Apartir de esta igualdad obtenemos las siguientes inecuaciones:
1. **Inecuación de Schwarz**: <img src="https://render.githubusercontent.com/render/math?math=\large |u\cdot v|\leq ||u||||v||">.
2. **Inecuación triangular**: <img src="https://render.githubusercontent.com/render/math?math=\large ||u+v||\leq ||u||+||v||">.

Con el operador producto punto definimos a la siguiente función, la **longitud** es la raiz cuadrada del producto punto del vector consigo mismo. La notación es la siguiente: <img src="https://render.githubusercontent.com/render/math?math=\large ||v||=(v\cdot v)^{1/2}">, esto sería equivalente a <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20(v_1%5E2%2B...%2Bv_n%5E2)%5E%7B1%2F2%7D">.

El operador producto punto también sirve para definir al **vector unitario**, este es un vector que cumple la siguiente ecuación: <img src="https://render.githubusercontent.com/render/math?math=\large v\cdot v =1">. Vectores unitarios son: <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%0A%5B1%2C0%5D%5ET%2C%5B0%2C1%5D%5ET%2C%5Bsen(%5Ctheta)%2Ccos(%5Ctheta)%5D%5ET%2C%5B1%2F2%2C1%2F2%2C1%2F2%2C1%2F2%5D%5ET">. Una forma para obtener un vector unitario en la dirección del vector <img src="https://render.githubusercontent.com/render/math?math=\large v"> es <img src="https://render.githubusercontent.com/render/math?math=\large (1/||v||)v">.

**Proposición**: Solo existe un vector unitario en la dirección <img src="https://render.githubusercontent.com/render/math?math=\large u">.

_Prueba_: Sea <img src="https://render.githubusercontent.com/render/math?math=\large v"> un vector unitario en direccíon <img src="https://render.githubusercontent.com/render/math?math=\large u"> obtenido de acuerdo a <img src="https://render.githubusercontent.com/render/math?math=\large (1/||u||)u">, si existe un vector unitario <img src="https://render.githubusercontent.com/render/math?math=\large w"> en la misma dirección, esto imploca que <img src="https://render.githubusercontent.com/render/math?math=\large v\cdot v=1=w\cdot w">, esto implica que <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%0Av_1%5E2%2B...%2Bv_n%5E2%3Dw_1%5E2%2B...%2Bw_n%5E2">. Sabemos también que para que dos vectores tengan la misma dirección, es necesario que <img src="https://render.githubusercontent.com/render/math?math=\large (||u||||v||)^{-1}u\cdot v=cos(0)=1">; naturalmente, <img src="https://render.githubusercontent.com/render/math?math=\large w"> también cumple esta igualdad, por lo que <img src="https://render.githubusercontent.com/render/math?math=\large (||u||||v||)^{-1}u\cdot v =(||u||||w||)^{-1} u \cdot w">; sin embargo sabemos que <img src="https://render.githubusercontent.com/render/math?math=\large |||v||=||w||=1">, entonces <img src="https://render.githubusercontent.com/render/math?math=\large u\cdot v=u\cdot w">. También sabemos que <img src="https://render.githubusercontent.com/render/math?math=\large v\cdot w=1">. _continuará_

**Referencias**

- Strang, G. (2016). Introduction to Linear Algebra. Wellesley-Cambridge Press.

### Matrices y Ecuaciones Lineales {#matrx}

Una **ecuación vectorial** es una expresión de la forma <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20c_1v_1%2B...%2Bc_nv_n%3Db">. Esto se puede escribir como <img src="https://render.githubusercontent.com/render/math?math=\large A c =b">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large A"> una matriz cuyas columans son los vectores <img src="https://render.githubusercontent.com/render/math?math=\large v_1,...,v_n"> y <img src="https://render.githubusercontent.com/render/math?math=\large c"> es un vector que comprende a las constantes <img src="https://render.githubusercontent.com/render/math?math=\large c_1,...,c_n">, <img src="https://render.githubusercontent.com/render/math?math=\large b"> es un vector de dimensión <img src="https://render.githubusercontent.com/render/math?math=\large n\times 1">.

En general, la multiplicación de una matriz con un vector por la derecha es la combinación lineal de las columnas donde los escalares son los elementos del vector.


**Referencias**

- Strang, G. (2016). Introduction to Linear Algebra. Wellesley-Cambridge Press.
