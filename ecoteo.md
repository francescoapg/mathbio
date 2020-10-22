## Ecología Teórica

A continuación veremos algunas simulaciones que nos ayudarán a entender los conceptos clave del curso

**Índice**

1. [Crecimiento poblacional](#semana2)
2. [Interacción entre poblaciones](#semana3)

### Crecimiento poblacional {#semana2}

Primero asegurate de tener los siguientes paquetes instalados

- Numpy 
- Matplotlib (generalmente viene instalado con Anaconda)

El método de instalar esos paquetes es escribir el siguiente código en _Anaconda Prompt_: `conda install numpy` y `conda install matplotlib`, luego de escribir cada uno (y que te aparezca el anuncio de confirmación) escribe `y` y presiona _Enter_. Para verificar si tienes estos paquetes instalados puedes escribir `conda list` en _Anaconda Prompt_.

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

Intenta cambiar los valores de R para obtener distintas gráficas. Recuerda que R representa la proporción de la población que se reproducirá y generará descendencia en la siguiente unidad de tiempo, se calcula como R_t=N_{t+1}/N_t.

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

Prueba valores pequeños de N_0 y observa si la población se mantiene, puedes variar también el valor de R (actualmente es 1.15)

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

Para esta sesión vamos a necesitar los siguientes paquetes

```python
import numpy as np
from scipy.integrate import odeint
import matplotlib.pyplot as plt
```

**Modelo de Jacques Monod (1942)**

```python
A=0.3
e=0.1
r_p=0.16
def monod(x, t, *args):
    S, P = x
    A, e, r_p = args
    dsdt = -(1/e)*((r_p*S*P)/(A+S))
    dpdt = (r_p*S*P)/(A+S)
    return dsdt, dpdt
t = np.linspace(0, 200, 200)
S_0 = 1  
P_0 = 0.1
x_0 = S_0, P_0
sol = odeint(monod, x_0, t, args=(A, e, r_p))

plt.plot(t, sol[:, 0], 'g', label='S(t)')
plt.plot(t, sol[:, 1], 'b', label='P(t)')
plt.legend(loc='best')
plt.xlabel('Tiempo')
plt.grid()
plt.show()
```

_Ejercicio 1_:

Varía los valores de e (eficiencia energética) y observa cómo varía el valor de equilibrio de P, intentan también valores negativos de r_p.

```python
A=0.3
e=0.4
r_p=0.16
def monod(x, t, *args):
    S, P = x
    A, e, r_p = args
    dsdt = -(1/e)*((r_p*S*P)/(A+S))
    dpdt = (r_p*S*P)/(A+S)
    return dsdt, dpdt
t = np.linspace(0, 200, 200)
S_0 = 1  
P_0 = 0.1
x_0 = S_0, P_0
sol = odeint(monod, x_0, t, args=(A, e, r_p))

plt.plot(t, sol[:, 0], 'g', label='S(t)')
plt.plot(t, sol[:, 1], 'b', label='P(t)')
plt.legend(loc='best')
plt.xlabel('Tiempo')
plt.grid()
plt.show()
```

**Modelo de David Ely Contois (1959)**

```python
B=10
e=0.4
r_p=0.16
def monod(x, t, *args):
    S, P = x
    B, e, r_p = args
    dsdt = -(1/e)*((r_p*S)/(B+(S/P)))
    dpdt = (r_p*S)/(B+(S/P))
    return dsdt, dpdt
t = np.linspace(0, 200, 200)
S_0 = 1  
P_0 = 0.1
x_0 = S_0, P_0
sol = odeint(monod, x_0, t, args=(B, e, r_p))

plt.plot(t, sol[:, 0], 'g', label='S(t)')
plt.plot(t, sol[:, 1], 'b', label='P(t)')
plt.legend(loc='best')
plt.xlabel('Tiempo')
plt.grid()
plt.show()
```

_Ejercicio 2_:

Observa cómo variar el parámetro B varía la forma de las funciones.

```python
B=100
e=0.4
r_p=0.16
def monod(x, t, *args):
    S, P = x
    B, e, r_p = args
    dsdt = -(1/e)*((r_p*S)/(B+(S/P)))
    dpdt = (r_p*S)/(B+(S/P))
    return dsdt, dpdt
t = np.linspace(0, 200, 200)
S_0 = 1  
P_0 = 0.1
x_0 = S_0, P_0
sol = odeint(monod, x_0, t, args=(B, e, r_p))

plt.plot(t, sol[:, 0], 'g', label='S(t)')
plt.plot(t, sol[:, 1], 'b', label='P(t)')
plt.legend(loc='best')
plt.xlabel('Tiempo')
plt.grid()
plt.show()
```

**Modelo estándar de Lotka-Volterra (1920-1930)**

Para manipular las ecuaciones vamos a utilizar el método de integración de Euler; de modo que si las poblaciones tienen menos de un individuo, su valor sea 0. Esto es adecuado dado nuestro _set_ de parámetros y la interpretación que le damos; sin embargo, esto no será adecuado en todos los escenarios; por ejemplo, los valores de N y P pueden representar la concentración de bacterias en suspensión, valores menores a 1, en ese contexto, no serán inadecuados.

```python
r=0.16
q=0.13
e=0.1
a=0.03
dt=0.1

N = 300 
P = 30

t = 0
ts = np.empty(1001)
N1s = np.empty(1001)
P2s = np.empty(1001)
i = 0
while t<100.0:
    ts[i] = t
    N1s[i] = N
    P2s[i] = P
    N = N + (r*N-a*N*P)*dt 
    if N<1:
        N = 0
    P = P + (e*a*N*P-q*P)*dt
    if P<1:
        P = 0
    i = i + 1
    t = t + dt

# plot data

plt.figure(1)
plt.plot(ts,N1s, label="Presas")
plt.plot(ts,P2s, label="Depredadores")
plt.xlabel("Tiempo")
plt.ylabel("Tamaño poblacional")
plt.legend()
plt.show()
print("Los últimos elementos son: Número de presas = " + str(N1s[-1]) + ", Número de depredadores = " + str(P2s[-1]))
```

Comor ejercicio trata de encontrar valores de las constantes y condiciones iniciales que lleven al equilibrio.

**Respuesta funcional: Modelo de Holling (1959)**

```python
r=0.16
q=0.13
e=0.1
a=0.03
h=0.5
dt=0.1

N = 300 
P = 30

t = 0
ts = np.empty(1001)
N1s = np.empty(1001)
P2s = np.empty(1001)
i = 0
while t<100.0:
    ts[i] = t
    N1s[i] = N
    P2s[i] = P
    N = N + (r*N-((a*N)/(1+a*h*N))*P)*dt 
    if N<1:
        N = 0
    P = P + (e*((a*N)/(1+a*h*N))*P-q*P)*dt
    if P<1:
        P = 0
    i = i + 1
    t = t + dt

# plot data

plt.figure(1)
plt.plot(ts,N1s, label="Presas")
plt.plot(ts,P2s, label="Depredadores")
plt.xlabel("Tiempo")
plt.ylabel("Tamaño poblacional")
plt.legend()
plt.show()
print("Los últimos elementos son: Número de presas = " + str(N1s[-1]) + ", Número de depredadores = " + str(P2s[-1]))
```

Como ejercicio trata de encontrar valores de las constantes y condiciones iniciales que lleven al equilibrio.

**Modelo dependiente de presas: Rosenzweig y MacArthur (1963)**

```python
r=0.16
q=0.13
e=0.1
a=0.01
h=0.35
dt=0.1

N = 300 
K = 400
P = 30

t = 0
ts = np.empty(10000)
N1s = np.empty(10000)
P2s = np.empty(10000)
i = 0
while t<1000.0:
    ts[i] = t
    N1s[i] = N
    P2s[i] = P
    N = N + (r*N*(1-N/K)-((a*N)/(1+a*h*N))*P)*dt 
    if N<1:
        N = 0
    P = P + (e*((a*N)/(1+a*h*N))*P-q*P)*dt
    if P<1:
        P = 0
    i = i + 1
    t = t + dt

# plot data

plt.figure(1)
plt.plot(ts,N1s, label="Presas")
plt.plot(ts,P2s, label="Depredadores")
plt.xlabel("Tiempo")
plt.ylabel("Tamaño poblacional")
plt.legend()
plt.show()
print("Los últimos elementos son: Número de presas = " + str(N1s[-1]) + ", Número de depredadores = " + str(P2s[-1]))
```

**Modelo dependiente de razones de Arditi-Ginzburg (1989)**

```python
r=0.16
q=0.13
e=0.1
al=0.15
h=0.2
dt=0.1

N = 300 
K = 400
P = 30

t = 0
ts = np.empty(10000)
N1s = np.empty(10000)
P2s = np.empty(10000)
i = 0
while t<1000.0:
    ts[i] = t
    N1s[i] = N
    P2s[i] = P
    N = N + (r*N*(1-N/K)-((al*N)/(P+al*h*N))*P)*dt 
    if N<1:
        N = 0
    P = P + (e*((al*N)/(P+al*h*N))*P-q*P)*dt
    if P<1:
        P = 0
    i = i + 1
    t = t + dt

# plot data

plt.figure(1)
plt.plot(ts,N1s, label="Presas")
plt.plot(ts,P2s, label="Depredadores")
plt.xlabel("Tiempo")
plt.ylabel("Tamaño poblacional")
plt.legend()
plt.show()
print("Los últimos elementos son: Número de presas = " + str(N1s[-1]) + ", Número de depredadores = " + str(P2s[-1]))
```

Como ejercicio observa como manipular el valor de "al" (alpha) no incrementa la población de depredadores en el equilibrio, trata de encontrar un juego de parámetros y condiciones iniciales que sí tenga ese efecto.

**Hipótesis de la interferencia gradual: Tyutyunov et al. (2008)**

```python
r=0.16
q=0.13
e=0.1
a=0.015
h=0.07
dt=0.1

N = 300 
K = 400
P = 30
P_c = 70

t = 0
ts = np.empty(10000)
N1s = np.empty(10000)
P2s = np.empty(10000)
i = 0
while t<1000.0:
    ts[i] = t
    N1s[i] = N
    P2s[i] = P
    N = N + (r*N*(1-N/K)-((a*N)/(P/P_c+np.exp(-P/P_c)+a*h*N))*P)*dt 
    if N<1:
        N = 0
    P = P + (e*((a*N)/(P/P_c+np.exp(-P/P_c)+a*h*N))*P-q*P)*dt
    if P<1:
        P = 0
    i = i + 1
    t = t + dt

# plot data

plt.figure(1)
plt.plot(ts,N1s, label="Presas")
plt.plot(ts,P2s, label="Depredadores")
plt.xlabel("Tiempo")
plt.ylabel("Tamaño poblacional")
plt.legend()
plt.show()
print("Los últimos elementos son: Número de presas = " + str(N1s[-1]) + ", Número de depredadores = " + str(P2s[-1]))
```

**Modelo de competencia de Lotka-Volterra (1920-1930)**

El resultado que observarás es el escenario de **exclusión competitiva**.

```python
r_1=0.16
r_2=0.2
al_12=0.3
al_21=0.9
dt=0.1

N_1 = 300 
N_2 = 300
K_1 = 250
K_2 = 250

t = 0
ts = np.empty(1001)
N1s = np.empty(1001)
N2s = np.empty(1001)
i = 0
while t<100.0:
    ts[i] = t
    N1s[i] = N_1
    N2s[i] = N_2
    N_1 = N_1 + (r_1*N_1*((K_1-N_1-al_12*N_2)/(K_1)))*dt 
    if N_1<1:
        N_1 = 0
    N_2 = N_2 + (r_2*N_2*((K_2-N_2-al_21*N_1)/(K_2)))*dt 
    if N_2<1:
        N_2 = 0
    i = i + 1
    t = t + dt

# plot data

plt.figure(1)
plt.plot(ts,N1s, label="Especie 1")
plt.plot(ts,N2s, label="Especie 2")
plt.xlabel("Tiempo")
plt.ylabel("Tamaño poblacional")
plt.legend()
plt.show()
print("Población de Especie 1 = " + str(N1s[-1]) + ",Población de Especie 2 = " + str(N2s[-1]))
```
