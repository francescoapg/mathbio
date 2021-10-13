[<<Home](https://francescoapg.github.io/mathbio/)

## Álgebra Lineal

**Índice**

1. [Introducción](#intro)

### Introducción {#intro}

El foco principal del Álgebra Lineal son las **combinaciones lineales**, estas son combinaciones de dos operaciones básicas que son la multiplicación escalar y la suma. Sea <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w"> dos vectores, y <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b"> dos números. <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20av%2Bbw"> es una combinación lineal de <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w">.

La suma de vectores y la multiplicación escalar siguen algunas reglas muy sencillas. En el caso de la suma de vectores, son los siguientes:

- Los vectores deben tener la misma dimensión.
- <img src="https://render.githubusercontent.com/render/math?math=\large a_{ij}"> del primer vector se sumará solo con <img src="https://render.githubusercontent.com/render/math?math=\large b_{ij}"> del segundo vector y visceversa. En otras palabras, la suma se realiza de forma sistemática y ordenada de acuerdo a las posiciones de los elementos de los vectores.
- <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20v%2Bw%3Dw%2Bv">.

Por su parte, la multiplicación escalar, el valor a multiplicar, llámese <img src="https://render.githubusercontent.com/render/math?math=\large k"> deberá ser multiplicado en todas las posiciones de la matriz o vector. En otras palabras, si la matriz está formada por <img src="https://render.githubusercontent.com/render/math?math=\large a_{ij}"> elementos, luego de la multiplicación escalar, estará formada por <img src="https://render.githubusercontent.com/render/math?math=\large ka_{ij}"> elementos.

Naturalmente, la "resta" de los vectores <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w"> deberá ser entendida como la siguiente combinación lineal: <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20v%2B(-1)w">.

Antes de pasar a la siguiente sección piensa en qué pasaría si tienes a todas las combinaciónes lineales de un vector de dimensión 3. En otras palabras, si en <img src="https://render.githubusercontent.com/render/math?math=\large c v">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large v"> el vector, <img src="https://render.githubusercontent.com/render/math?math=\large c"> pudiese tomar cualquier valor. Es claro que este caso sería el de una línea con dirección <img src="https://render.githubusercontent.com/render/math?math=\large v">. Si tomamos dos vectores linealmente independientes de dimensión 3, <img src="https://render.githubusercontent.com/render/math?math=\large v"> y <img src="https://render.githubusercontent.com/render/math?math=\large w">, todas las combinaciones lineales llenarán un plano. De forma análoga, tres vectores linealmente idependientes llenarán todo el espacio tridimensional. Un acotación importante es que ninguno de os vectores mencionados debe ser el vector cero (_zero vector_). Combinación lineales del vector cero serán el mismo vector además, toda línea o plano que pase por el origen comprenderá al vector cero.

**Referencias**
