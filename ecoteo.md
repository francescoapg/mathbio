## Ecología Teórica

A continuación veremos algunos ejemplos que nos ayudarán a entender los conceptos clave del curso

**Índice**

1. [Crecimiento poblacional](#semana2)
2. [Interacción entre poblaciones](#semana3)

### Crecimiento poblacional {#semana2}

Primero asegurate de tener los siguientes paquetes instalados

- Numpy 
- Matplotlib (generalmente viene instalado con Anaconda)

El método de instalar esos paquetes es escribir el siguiente código en _Anaconda Prompt_: `conda install numpy` y `conda install matplotlib` y escribir `y` y presionar _Enter_ luego de que aparezca el anuncio, para verificar si tienes estos paquetes instalados puedes escribir `conda list` en el _Prompt_.

A continuación, abrimos un nuevo documento en _Jupyter Notebook_. Lo primero que haremos será llamar a los paquetes que usaremos en esta lección, de la siguiente manera

```python
import numpy as np 
from matplotlib import pyplot as plt 
```

**Crecimiento discreto en poblaciones con generaciones no superpuestas**

```python
N_0=50 
X = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10] 
# Primera gráfica 
R1=1.2
Y1=[N_0*R1**(x-1) for x in X]  
plt.plot(X, Y1, label = "R=1.2") 
  
# Segunda gráfica 
R2=1
Y2=[N_0*R2**(x-1) for x in X]  
plt.plot(X, Y2, label = "R=1") 

# Tercera gráfica 
R3=0.8
Y3=[N_0*R3**(x-1) for x in X]  
plt.plot(X, Y3, label = "R=0.8") 
  
plt.xlabel('Unidades de tiempo o generaciones') 
plt.ylabel('Tamaño poblacional (N)') 
plt.title('Crecimiento discreto en poblaciones con generaciones no superpuestas') 
  
plt.legend() 
plt.show() 
```
_Ejercicio 1_:

Intenta cambiar los valores de R para obtener distintas gráficas. Recuerda que R representa la proporción de la población que se reproducirá y generará descendencia en la siguiente unidad de tiempo, se calcula como $R_t=N_{t+1}/N_t$.

```python
I = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
N_0=100
R=2.7
J=[N_0*R**(x-1) for x in I]

#I corresponde al eje X, mientras que J al eje Y,la función graficada es de la ecuación de Verhulst.

plt.plot(I,J)
plt.xlabel('Unidades de tiempo o generaciones') 
plt.ylabel('Tamaño poblacional (N)') 

plt.show()
```
**Crecimiento exponencial en poblaciones con generaciones superpuestas**

```python
x = np.arange(0, 11)
N_0=50

# Primera gráfica 
r1=0.16
y1 = N_0*np.exp(r1*(x))
plt.plot(x, y1, label = "r=0.16") 

# Segunda gráfica 
r2=0
y2 = N_0*np.exp(r2*(x))
plt.plot(x, y2, label = "r=0") 

# Tercera gráfica 
r3=-0.16
y3 = N_0*np.exp(r3*(x))
plt.plot(x, y3, label = "r=-0.16") 
  
plt.xlabel('Tiempo') 
plt.ylabel('Tamaño poblacional (N)') 
plt.title('Crecimiento exponencial en poblaciones con generaciones superpuestas') 
  
plt.legend() 
plt.show() 
```
_Ejercicio 2_:

Prueba al menos dos valores de r para observar como cambia la gráfica. Nota la diferencia entre R y r.

```python
x = np.arange(0, 11)
N_0=50
r=0.3

y = N_0*np.exp(r*(x))

plt.plot(x, y) 

dy = N_0*r*np.exp(r*(x))

plt.plot(x, dy, label='Derivada de N') 

plt.legend()
plt.show()
```

**Modelos estocasticos de crecimiento poblacional**

Veremos un ejemplo **muy** simple a continuación

```python
#Primero, vamos a agregar ruido normal a la tasa de crecimiento intrínseca r, ds corresponde a la desviación estándar.

N_0=50
X = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

#Importamos el módulo random de Phyton

import random 

#Grafico1

r0, ds = 1.2, 0.01
s = np.random.normal(r0, ds, 1000)

Y0=[N_0*random.choice(s)**(x-1) for x in X]

plt.plot(X, Y0, label = "r=1.2+LowNoise") 

#Gráfico2

r1, ds = 1.2, 0.1
s1 = np.random.normal(r1, ds, 1000)

Y1=[N_0*random.choice(s1)**(x-1) for x in X]

plt.plot(X, Y1, label = "r=1.2+Noise") 

#Gráfico3

r2, ds = 1.2, 0.3
s2 = np.random.normal(r2, ds, 1000)

Y2=[N_0*random.choice(s2)**(x-1) for x in X]

plt.plot(X, Y2, label = "r=1.2+HighNoise") 
  
plt.xlabel('Unidades de tiempo o generaciones') 
plt.ylabel('Tamaño poblacional (N)') 
plt.title('Modelos estocasticos de crecimiento poblacional discreto') 
  
plt.legend() 
plt.show()
```

_Observe el problema de las poblaciones pequeñas_:

```python
N_0=3
X = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

#A continuación R es la tasa de crecimiento y ds la desviación estándar de ese parámetro en una distribución normal.

R, ds = 1.2, 0.3
s = np.random.normal(R, ds, 1000)

Y=[N_0*random.choice(s)**(x-1) for x in X]

#El siguiente código evita que tengamos poblaciones con individuos menores a 1

for y in Y:
    if y < 1:
        f=Y.index(y)
        G=Y[f:]
        S=[0]*len(G)
        H=Y[:f]
        H+=S
        plt.plot(X, H, label = "WithNoise†")
        break

result = any(y < 1 for y in Y)

if not result:
    plt.plot(X,Y, label = "WithNoise")

#Comparamos con el escenario sin estocasticidad

Y1=[N_0*R**(x-1) for x in X]
plt.plot(X, Y1, label = "WithoutNoise")

  
plt.xlabel('Unidades de tiempo o generaciones') 
plt.ylabel('Tamaño poblacional (N)') 
plt.title('Problema de las poblaciones pequeñas') 
  
plt.legend() 
plt.show()
```

_Ejercicio 3_:

Prueba valores pequeños de $N_0$ y observa si la población se mantiene, puedes variar también el valor de R (actualmente es 1.15)

```python
N_0=10
X = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]


R, ds = 1.15, 0.5
s = np.random.normal(R, ds, 1000)

Y=[N_0*random.choice(s)**(x-1) for x in X]

for y in Y:
    if y < 1:
        f=Y.index(y)
        G=Y[f:]
        S=[0]*len(G)
        H=Y[:f]
        H+=S
        plt.plot(X, H, label = "WithNoise†")
        break

result = any(y < 1 for y in Y)

if not result:
    plt.plot(X,Y, label = "WithNoise")

plt.xlabel('Unidades de tiempo o generaciones') 
plt.ylabel('Tamaño poblacional (N)') 
plt.title('Problema de las poblaciones pequeñas') 
  
plt.legend() 
plt.show()
```

**Dependencia de densidad en poblaciones con generaciones discretas: Modelo de Beverton-Holt (1957)**

```python
N_0=50
K=400
R=1.2
N_1=(N_0*R)/(1+((N_0*(R-1))/K))
Y=[N_0]

#Acá inciamos un bucle para construir la lista de los elementos de la función mediante iteración

while len(Y) < 100:
    N_0, N_1 = N_1, (N_1*R)/(1+((N_1*(R-1))/K))
    Y.append(N_1)

X=range(1,101)

plt.plot(X, Y) 
  
plt.xlabel('Unidades de tiempo o generaciones') 
plt.ylabel('Tamaño poblacional (N)') 
plt.title('Dependencia de densidad generaciones discretas, K=400 y R=1.2') 

plt.show() 
```

_Ejercicio 4_:

Intente dando valores de N_0 superiores a K

```python
N_0=50
K=100
R=1.3
N_1=(N_0*R)/(1+((N_0*(R-1))/K))
Y=[N_0]

while len(Y) < 60:
    N_0, N_1 = N_1, (N_1*R)/(1+((N_1*(R-1))/K))
    Y.append(N_1)

X=range(1,61)

plt.plot(X, Y) 
  
plt.xlabel('Unidades de tiempo o generaciones') 
plt.ylabel('Tamaño poblacional (N)') 
plt.title('Dependencia de densidad, K=400 y R=1.3') 

plt.show() 
```

**Dependencia de densidad en poblaciones con generaciones superpuestas**

```python
x = np.arange(0, 30)
N_0=50
K=500
r=1

y = K/(1+(((K-N_0)/N_0)*np.exp(-r*(x))))

plt.plot(x, y) 

dy = r*y*(1-(y/K))

plt.plot(x, dy, label='Derivada de N') 

plt.xlabel('Tiempo') 
plt.ylabel('Tamaño poblacional (N)') 
plt.title('Dependencia de densidad en poblaciones con generaciones superpuestas') 

plt.legend()
plt.show() 
```

**Lectura recomendada :)**

Ausloos, M., & Dirickx, M. (Eds.). (2006). The logistic map and the route to chaos: From the beginnings to modern applications. Springer Science & Business Media.

### Interacción entre poblaciones {#semana3}
