[<<Home](https://francescoapg.github.io/mathbio/)

## Biomatemática

Curso introductorio a la Biomatemática. Se muestran aplicaciones básicas de teorías matemáticas de fácil entendimiento.

**Índice**

1. [Introducción a la Biomatemática](#intro)
2. [Ecuaciones de Diferencia Lineales](#EDL)
3. [Ecuaciones de Diferencia No Lineales](#EDNL)

### Introducción a la Biomatemática {#intro}

El desarrollo histórico de la Biomatemática tiene sus raíces en los desarrollos matemáticos de [Georg Cantor](https://es.wikipedia.org/wiki/Georg_Cantor) (1845-1918) acerca de los números naturales. La Biología o, mejor dicho, el fenómeno biológico es, de forma recurrente, una fuente de inspiración para el desarrollo matemático. Aunque recientemente es usual que se usen en Biología las herramientas matemáticas más básicas (Cálculo, Teoría de Grafos), ignorar todo el desarrollo matemático que fue generado para entender la naturaleza y, en particular, la biología es como mínimo un error.

Apesar de lo anterior, la palabra Biomatemática ha sido frecuentemente usada para referirse al uso de teorías o métodos estadísticos en la investigación biológica (Bartlett, 1975).

**Primeros usos de matemática como herramienta fundamental en Biología**

Entre los primeros usos en Biología tenemos a los trabajos de Lotka y Volterra (1925 y 1926) de competencia y depredación que fueron formulados como variables de tiempo continuo. Por la parte de modelos de generaciones discretas, Nicholson y Bailey en 1935 formularon sus modelos de dinámica poblacional.
Sin embargo, quizás la primera aplicación práctica de modelos matemáticos en biología, en particular en epidemiología, fue el trabajo _The Prevention of Malaria_ de Ross en 1911. El uso de modelos estocásticos fue introducido por los trabajos pioneros de McKendrick en 1914 y 1926, redescubierto en 1952 por Kendall D.G y Irwin J.O.

**Modelos**

Mientras los ingenieros usan modelos matemáticos para determinar como dirigir la operación de máquinas y computadoras, los biólogos usan el modelaje con para aprender como funciona el mundo natural. Un modelo que especifica exactamente como debe funcionar un sistema hace más facil localizar los vacíos en nuestro entendimiento; mas aún, discrepancias entre las predicciones del modelo y la naturaleza ayudan a especificar lo que no conocemos (Gordon, 2010).

_‘Los modelos son descripciones, a veces muy hermosas, de maneras en las que imaginamos que el mundo es’ (Gordon, 2010)._

La palabra _modelo_ es usada deliberadamente para implicar el remplazo de la compleja realidad biológica por algún sistema hipotético más idealizado (Bartlett, 1960).

**Referencias**

- Bartlett M.S. (1960) Stochastic Population Models
- Bartlett M.S. (1975) Biomathematics. In: Probability, Statistics and Time. Springer, Dordrecht. https://doi.org/10.1007/978-94-009-5889-0_5
- Gordon, D. M. (2010). Ant encounters. Princeton University Press.

### Ecuaciones de Diferencia Lineales {#EDL}

Una ecuación de diferencia de orden <img src="https://render.githubusercontent.com/render/math?math=\large k"> tiene la forma <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20f(x_%7Bt%2Bk%7D%2Cx_%7Bt%2Bk-1%7D%2C...%2Cx_t)%3D0"> donde <img src="https://render.githubusercontent.com/render/math?math=\large t=0,1,...">. <img src="https://render.githubusercontent.com/render/math?math=\large f"> es una función de valores reales de las variables reales <img src="https://render.githubusercontent.com/render/math?math=\large x_t"> a <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20x_%7Bt%2Bk%7D"> y <img src="https://render.githubusercontent.com/render/math?math=\large t">.

Una ecuación de diferencia es llamada _autónoma_ si no depende explícitamente de <img src="https://render.githubusercontent.com/render/math?math=\large t">. Si una ecuación de diferencia no es _autónoma_ es llamada _no autónoma_.

La representación usual es la siguiente: <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20x_%7Bt%2Bk%7D%2Ba_1%20x_%7Bt%2Bk-1%7D%2B...%2Ba_k%20x_t%3Db_t">, donde <img src="https://render.githubusercontent.com/render/math?math=\large t=0,1,..."> Los coeficientes <img src="https://render.githubusercontent.com/render/math?math=\large a_j"> pueden ser funciones de <img src="https://render.githubusercontent.com/render/math?math=\large t"> y <img src="https://render.githubusercontent.com/render/math?math=\large x_i"> para <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20i%3Dt%2C...%2Ct%2Bk-1">. La función <img src="https://render.githubusercontent.com/render/math?math=\large b_t"> puede depender de <img src="https://render.githubusercontent.com/render/math?math=\large t">.

_Ejemplo_:

<img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20x_%7Bt%2B1%7D%3Datx_t%2Bbt%5E2x_%7Bt-1%7D%2Bsen(t)">

Una ecuación de difernecia es llamada **homogénea** si <img src="https://render.githubusercontent.com/render/math?math=\large b_t=0">. En el caso anterior <img src="https://render.githubusercontent.com/render/math?math=\large b_t=sen(t)"> por lo que es una ecuación de diferencia **no homogénea**.

Si los coeficientes no dependen de las variables de estado (<img src="https://render.githubusercontent.com/render/math?math=\large x_i">s) entonces la ecuación es llamada **lineal**. En ejemplo anterior <img src="https://render.githubusercontent.com/render/math?math=\large a_1=at"> y <img src="https://render.githubusercontent.com/render/math?math=\large a_2=bt^2"> por lo que sería finalmente una ecuación no autónoma lineal no homogénea.

También podemos hablar de sistemas de ecuaciones de diferencia que son un análogo directo de los sistemas de ecuaciones y al igual que los sistemas de ecuaciones, es ameno para ser tratado con Álgebra lineal. Una de las representaciones de sistemas de ecuaciones de diferencia es la siguiente: <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20x_i(t%2B1)%3Df_i(x_1(t)%2Cx_2(t)%2C...%2Cx_k(t)%2Ct)">, donde <img src="https://render.githubusercontent.com/render/math?math=\large i=1,2,...,k">. 

La forma matricial de expresar este sistema de ecuaciones sería <img src="https://render.githubusercontent.com/render/math?math=%5Clarge%20X(t%2B1)%3DA(t)X(t)%2BB(t)"> donde <img src="https://render.githubusercontent.com/render/math?math=\large X"> es el vector <img src="https://render.githubusercontent.com/render/math?math=\large [x_1,x_2,...,x_k]^t">, la matriz <img src="https://render.githubusercontent.com/render/math?math=\large A=(a_{ij})_{ij=1}^k"> y el vector <img src="https://render.githubusercontent.com/render/math?math=\large B=[b_1,b_2,...,b_k]^t">.

**Referencias**

- Allen, L. J. (2007). An introduction to mathematical biology. Upper Saddle River, New Jersey.

### Ecuaciones de Diferencia No Lineales {#EDNL}



**Referencias**

- Allen, L. J. (2007). An introduction to mathematical biology. Upper Saddle River, New Jersey.
