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

Otra matriz importante es la **matriz identidad**, esta matriz es aquella matriz <img src="https://render.githubusercontent.com/render/math?math=\large I"> que cumple <img src="https://render.githubusercontent.com/render/math?math=\large Ix=x"> siendo <img src="https://render.githubusercontent.com/render/math?math=\large x"> distinto al vector cero. Es evidente que la dimensión de la matriz identidad va a variar dependiendo de la dimensión de <img src="https://render.githubusercontent.com/render/math?math=\large x">. Adelantamos que para que dos matrices se puedan multiplicar, el número de columnas de la primera debe ser igual al número de filas de la segunda. Siendo <img src="https://render.githubusercontent.com/render/math?math=\large x"> una matriz con 3 filas, <img src="https://render.githubusercontent.com/render/math?math=\large I"> sería

<img src="https://render.githubusercontent.com/render/math?math=%5Clarge%0A%5Cbegin%7Bbmatrix%7D%0A1%26%200%260%5C%5C%0A0%261%260%5C%5C%0A0%260%261%5C%5C%0A%5Cend%7Bbmatrix%7D">

La matriz identidad es una matriz cuyos elementos son 0s a excepción de la diagonal principal que está conformada por 1s.

**Notación**

Tenga en cuenta lo siguiente:

- Las dimensiones de una matriz se escriben como <img src="https://render.githubusercontent.com/render/math?math=\large m\times n">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large m"> el número de filas y <img src="https://render.githubusercontent.com/render/math?math=\large n"> el número de columnas.
- Los elementos de una matriz <img src="https://render.githubusercontent.com/render/math?math=\large A"> se identifican por sus coordenadas en filas y columnas, <img src="https://render.githubusercontent.com/render/math?math=\large a_{ij}"> estará en la fila <img src="https://render.githubusercontent.com/render/math?math=\large i"> y columna <img src="https://render.githubusercontent.com/render/math?math=\large j">. Para una matriz de <img src="https://render.githubusercontent.com/render/math?math=\large 2\times 2">

<img src="https://render.githubusercontent.com/render/math?math=%5Clarge%0A%5Cbegin%7Bbmatrix%7D%0Aa_%7B11%7D%20%26%20a_%7B12%7D%5C%5C%0Aa_%7B21%7D%26a_%7B22%7D%20%5C%5C%0A%5Cend%7Bbmatrix%7D">

**Referencias**

- Strang, G. (2016). Introduction to Linear Algebra. Wellesley-Cambridge Press.

### Matrices y Ecuaciones Lineales {#matrx}

Una **ecuación vectorial** es una expresión de la forma <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20c_1v_1%2B...%2Bc_nv_n%3Db">. Esto se puede escribir como <img src="https://render.githubusercontent.com/render/math?math=\large A c =b">, siendo <img src="https://render.githubusercontent.com/render/math?math=\large A"> la **matriz de coeficientes** cuyas columans son los vectores <img src="https://render.githubusercontent.com/render/math?math=\large v_1,...,v_n"> y <img src="https://render.githubusercontent.com/render/math?math=\large c"> es un vector que comprende a las constantes <img src="https://render.githubusercontent.com/render/math?math=\large c_1,...,c_n">, <img src="https://render.githubusercontent.com/render/math?math=\large b"> es un vector de dimensión <img src="https://render.githubusercontent.com/render/math?math=\large m\times 1">. Ten en cuenta que el lado izquierdo de la ecuación vectorial es la llamada _combinación lineal_. Por otra parte, <img src="https://render.githubusercontent.com/render/math?math=\large b"> siempre puede ser calculado como un vector de _productos punto_:

<img src="https://render.githubusercontent.com/render/math?math=%5Clarge%0A%5Cbegin%7Bbmatrix%7D%0A(row_1)%5Ccdot%20c%5C%5C%0A(row_2)%5Ccdot%20c%5C%5C%0A...%5C%5C%0A(row_m)%5Ccdot%20c%5C%5C%0A%5Cend%7Bbmatrix%7D">

En general, la multiplicación de una matriz con un vector por la derecha es la combinación lineal de las columnas donde los escalares son los elementos del vector.

Cuando <img src="https://render.githubusercontent.com/render/math?math=\large Ax=b"> es considerada como una **ecuación lineal** y <img src="https://render.githubusercontent.com/render/math?math=\large A"> es una matriz cuadrada (con el mismo número de filas y columnas), <img src="https://render.githubusercontent.com/render/math?math=\large x"> va a ser calculado como el producto de la inversa de la matriz con <img src="https://render.githubusercontent.com/render/math?math=\large b">, en otras palabras, <img src="https://render.githubusercontent.com/render/math?math=\large x=A^{-1}b">. Este es el escenario más sencillo; dentro de esceneario los aún más sencillo son cuando <img src="https://render.githubusercontent.com/render/math?math=\large A"> es una matriz triangular (inferior o superior) o diagonal.

Conectando el concepto de independecia de columnas y solubilidad de una ecuación matricial, decimos que 

- Si <img src="https://render.githubusercontent.com/render/math?math=\large Ax=0"> tiene solo como solución al vector 0, entonces, dado <img src="https://render.githubusercontent.com/render/math?math=\large A"> es una matriz cuadrada, <img src="https://render.githubusercontent.com/render/math?math=\large A"> es una **matriz invertible**, es decir, existe <img src="https://render.githubusercontent.com/render/math?math=\large A^{-1}">.
- Si <img src="https://render.githubusercontent.com/render/math?math=\large Ax=0"> tiene más de una solución, <img src="https://render.githubusercontent.com/render/math?math=\large A"> es una **matriz singular**. Para matrices cuadradas, si el _determinante_ es 0, dicha matriz es singular. Una **ecuación singular** tiene 0 soluciones o infinitas soluciones.

Existen dos maneras de entender las **ecuaciones lineales**:

- por Filas: <img src="https://render.githubusercontent.com/render/math?math=\large m"> ecuaciones que se intersectan en la solución (<img src="https://render.githubusercontent.com/render/math?math=\large x">).
- por Columnas: Una combinación lineal de <img src="https://render.githubusercontent.com/render/math?math=\large n"> columnas que produce <img src="https://render.githubusercontent.com/render/math?math=\large b">.

El método por filas es el más geométrico y quizás recomendable para matrices de poca dimensión, mientras que el método por columnas es recomendable para matrices de mayores dimensiones.

Un concepto importante es el _**rank**_. El _rank_ de <img src="https://render.githubusercontent.com/render/math?math=\large A"> es la dimensión del espacio vectorial de las soluciones de la ecuación lineal <img src="https://render.githubusercontent.com/render/math?math=\large Ax=0">. El _rank_ es el número de columnas linealmente independientes de la matriz y se puede calcular como el número de pivots que hay luego del proceso de eliminación.

**Eliminación**

Es un proceso por el cual transformamos un sisema de ecuaciones (<img src="https://render.githubusercontent.com/render/math?math=\large Ax=b">) cualquiera en un sistema de ecuaciones **triangular superior** (<img src="https://render.githubusercontent.com/render/math?math=\large Ux=d">). Una vez alcanzado el sistema triangular superior, el sistema es resuelto por **substitución inversa** (_back substitution_).

El corazón de este método es que apesar de ser un sistema distinto, <img src="https://render.githubusercontent.com/render/math?math=\large Ux=d"> tiene las mismas soluciones que <img src="https://render.githubusercontent.com/render/math?math=\large Ax=b">.

Para este método debes verificar primero que la primera posición (<img src="https://render.githubusercontent.com/render/math?math=\large a_{1,1}">) sea diferente de 0, de este modo, esta será tu primera __columna pivot__, caso contario hacer los cambios necesarios para que así sea, de no ser posible, este será la primera **columna libre**.

Para resolver (con una solución única) un sistema de <img src="https://render.githubusercontent.com/render/math?math=\large n"> ecuaciones es necesario tener <img src="https://render.githubusercontent.com/render/math?math=\large n"> _pivots_. Los _pivots_ son los elementos de la diagonal distintos de cero de la matriz <img src="https://render.githubusercontent.com/render/math?math=\large U">.

**Referencias**

- Strang, G. (2016). Introduction to Linear Algebra. Wellesley-Cambridge Press.
