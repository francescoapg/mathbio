[<<Home](https://francescoapg.github.io/mathbio/)

## Teoría de Conjuntos

Como libro introductorio, refierase a _Naive set theory_ de Paul R. Halmos.

**Índice**

1. [Conjuntos de Borel](#borel)

### Conjuntos de Borel {#borel}

**Conjuntos contables**

Dos conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large A">, <img src="https://render.githubusercontent.com/render/math?math=\large B"> son **equinúmeros** o tienen la misma **cardinalidad** (<img src="https://render.githubusercontent.com/render/math?math=\large A\equiv B">) si existe un mapa bijectivo de <img src="https://render.githubusercontent.com/render/math?math=\large A"> hacia <img src="https://render.githubusercontent.com/render/math?math=\large B">.

Un set es finito si existe una bijección desde un subconjunto propio de los naturales hacia <img src="https://render.githubusercontent.com/render/math?math=\large A">; caso contrario, llamamos a <img src="https://render.githubusercontent.com/render/math?math=\large A">, infinito. Un conjunto es llamado **contable** si es finito o si existe una biyección de los naturales (todo el conjunto) a <img src="https://render.githubusercontent.com/render/math?math=\large A">; si no es contable, <img src="https://render.githubusercontent.com/render/math?math=\large A"> es incontable.

**Teorema**: La unión (finita o infinita) de conjuntos contables es contable.

**Teorema**: (Cantor) Para cualquier par de números reales <img src="https://render.githubusercontent.com/render/math?math=\large a"> y <img src="https://render.githubusercontent.com/render/math?math=\large b">, con <img src="https://render.githubusercontent.com/render/math?math=\large a<b">, el intervalo <img src="https://render.githubusercontent.com/render/math?math=\large [a,b]"> es incontable.

La prueba de este teorema es dada por Cantor. Un conjunto de interés es <img src="https://render.githubusercontent.com/render/math?math=\large Y^X">, definido como el conjunto de todas las funciones de <img src="https://render.githubusercontent.com/render/math?math=\large X"> a <img src="https://render.githubusercontent.com/render/math?math=\large Y">.

Definimos una relación <img src="https://render.githubusercontent.com/render/math?math=\large \leq_c"> entre conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> si existe una función inyectiva de <img src="https://render.githubusercontent.com/render/math?math=\large A"> a <img src="https://render.githubusercontent.com/render/math?math=\large B"> (no tiene que ser _onto_ (suryectiva)). En lenguaje normal, <img src="https://render.githubusercontent.com/render/math?math=\large A\leq_c B"> si la cardinalidad de <img src="https://render.githubusercontent.com/render/math?math=\large A"> es menor o igual que la cardinalidad de <img src="https://render.githubusercontent.com/render/math?math=\large B">. También podemos definir <img src="https://render.githubusercontent.com/render/math?math=\large <_c"> entre <img src="https://render.githubusercontent.com/render/math?math=\large A"> y <img src="https://render.githubusercontent.com/render/math?math=\large B"> si <img src="https://render.githubusercontent.com/render/math?math=\large A\leq_c B"> y no se cumple que <img src="https://render.githubusercontent.com/render/math?math=\large A\equiv B">.

**Teorema**: (Cantor) Para cualquier conjunto <img src="https://render.githubusercontent.com/render/math?math=\large X">, <img src="https://render.githubusercontent.com/render/math?math=X%3C_c%5Cmathcal%7BP%7D(X)">.

**Teorema**: (Teorema de Schröder-Bernstein) Para cualquier par de conjuntos <img src="https://render.githubusercontent.com/render/math?math=\large X"> y <img src="https://render.githubusercontent.com/render/math?math=\large Y">, 

<img src="https://render.githubusercontent.com/render/math?math=X%5Cleq_cY%5Cland%20Y%5Cleq_cX%5CRightarrow%20X%5Cequiv%20Y">

La prueba fue inicialmente dada por Cantor y luego por Dedekind.

**Referencias**

- 
