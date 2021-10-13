[<<Home](https://francescoapg.github.io/mathbio/)

## Álgebra Lineal

**Índice**

1. [Introducción](#intro)

### Introducción {#intro}

El foco principal del Álgebra Lineal son las **combinaciones lineales**, estas son combinaciones de dos operaciones básicas que son la multiplicación escalar y la suma. Sea <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w"> dos vectores, y <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b"> dos números. <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20av%2Bbw"> es una combinación lineal de <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w">.

La suma de vectores y la multiplicación escalar siguen algunas reglas muy sencillas. En el caso de la **suma de vectores**, son los siguientes:

- Los vectores deben tener la misma dimensión.
- <img src="https://render.githubusercontent.com/render/math?math=\large a_{ij}"> del primer vector se sumará solo con <img src="https://render.githubusercontent.com/render/math?math=\large b_{ij}"> del segundo vector y visceversa. En otras palabras, la suma se realiza de forma sistemática y ordenada de acuerdo a las posiciones de los elementos de los vectores.
- <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20v%2Bw%3Dw%2Bv">.

Por su parte, la **multiplicación escalar**, el valor a multiplicar, llámese <img src="https://render.githubusercontent.com/render/math?math=\large k"> deberá ser multiplicado en todas las posiciones de la matriz o vector. En otras palabras, si la matriz está formada por <img src="https://render.githubusercontent.com/render/math?math=\large a_{ij}"> elementos, luego de la multiplicación escalar, estará formada por <img src="https://render.githubusercontent.com/render/math?math=\large ka_{ij}"> elementos.

Naturalmente, la "resta" de los vectores <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w"> deberá ser entendida como la siguiente combinación lineal: <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20v%2B(-1)w">.

Antes de pasar a la siguiente sección piensa en qué pasaría si tienes a todas las combinaciónes lineales de un vector de dimensión 3. En otras palabras, si en <img src="https://render.githubusercontent.com/render/math?math=\large c v">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large v"> el vector, <img src="https://render.githubusercontent.com/render/math?math=\large c"> pudiese tomar cualquier valor. Es claro que este caso sería el de una línea con dirección <img src="https://render.githubusercontent.com/render/math?math=\large v">. Si tomamos dos vectores linealmente independientes de dimensión 3, <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w">, todas las combinaciones lineales llenarán un plano. De forma análoga, tres vectores linealmente idependientes llenarán todo el espacio tridimensional. Un acotación importante es que ninguno de os vectores mencionados debe ser el vector cero (_zero vector_). Combinación lineales del vector cero serán el mismo vector además, toda línea o plano que pase por el origen comprenderá al vector cero.

Una **ecuación vectorial** es una expresión de la forma <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20c_1v_1%2B...%2Bc_nv_n%3Db">. Esto se puede escribir como <img src="https://render.githubusercontent.com/render/math?math=\large A c =b">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large A"> una matriz cuyas columans son los vectores <img src="https://render.githubusercontent.com/render/math?math=\large v_1,...,v_n"> y <img src="https://render.githubusercontent.com/render/math?math=\large c"> es un vector que comprende a las constantes <img src="https://render.githubusercontent.com/render/math?math=\large c_1,...,c_n">, <img src="https://render.githubusercontent.com/render/math?math=\large b"> es un vector de dimensión <img src="https://render.githubusercontent.com/render/math?math=\large n\times 1">

La siguiente operación entre vectores es llamada **producto punto** o **producto interno**. Esta operación se representa como <img src="https://render.githubusercontent.com/render/math?math=\large v\cdot w"> y tiene como resultado a un número. La fórmula general es <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20v_%7B11%7Dw_%7B11%7D%2B...%2Bv_%7Bij%7Dw_%7Bij%7D%2B...%2Bv_%7Bmn%7Dw_%7Bmn%7D">. El producto punto es interesante por su interpretación geométrica. Por ejemplo, si el producto punto de dos vectores es 0, esto implica que ambos vectores son perpendiculares, es decir, el ángulo entre ellos es de 90°.

Con este operador definimos a la siguiente función, la **longitud** es la raiz cuadrada del producto punto del vector consigo mismo. La notación es la siguiente: <img src="https://render.githubusercontent.com/render/math?math=\large ||v||=(v\cdot v)^{1/2}">, esto sería equivalente a <img src="https://render.githubusercontent.com/render/math?math=\large v">: <img src="https://render.githubusercontent.com/render/math?math=\large (v_1^2+...+v_n^2)^{1/2}">.

**Referencias**
