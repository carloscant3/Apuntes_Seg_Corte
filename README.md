# Apuntes segundo corte - Sistemas Dinamicos


$$
Jose Manuel   Ortiz   Soler - 121769
$$


$$
Nicolas   Cortes    Triana - 120883
$$


$$
Carlos   Andres   Cante   Saavedra - 122248
$$



# 14/03/2025


# **Sistemas Mecanicos**

Un sistema mecánico es básicamente un grupo de objetos que están conectados entre sí y que siguen las leyes de la mecánica. Su movimiento cambia con el tiempo y se puede describir con ecuaciones matemáticas. Estos sistemas pueden incluir cosas como masas, resortes, amortiguadores, engranajes y articulaciones, que interactúan entre sí aplicando fuerzas y torques.

Desde el punto de vista de Sistemas Dinámicos, su comportamiento se estudia usando ecuaciones diferenciales, que nos dicen cómo cambia en el tiempo. Para describirlos, se pueden usar diferentes enfoques, como la Segunda Ley de Newton, el método de Lagrange o la formulación de Hamilton, dependiendo de qué tan complejo sea el sistema. 

**Ley de Hooke**

$$
F = -k x
$$

Se utiliza siempre manteniendo el mismo marco de referencia. En el curso vamos a trabajar resortes lineales.

$$
\textcolor{blue}{\textbf{Amortiguadores}}
$$


Formula


$$
F = B X' = b (X'_1 - X'_2)
$$


Tipos de friccion:

- Friccion en seco.
- Estatica.
- Desplazamiento.
- Rodamiento.


$$
**Sistema masa - Resorte - Amortiguador**
$$


![image](https://github.com/user-attachments/assets/d964cf92-942f-4673-895b-9982b4991a87)

Fenomeno fisico:

Ley de hooke


$$
F_R = K_2 \cdot X
$$


Friccion viscosa


$$
F_f = K_1 \cdot V_m
$$


Leyes de Newton


$$
F = m \cdot a
$$


$$
**Ejemplo 1**
$$

Encuéntrese la constante de resorte equivalente para el sistema
mostrado en la Figura y muéstrese que también puede obtenerse gráficamente
como lo indica la Figura

En los resortes en serie, la fuerza en cada resorte es la misma. 

![image](https://github.com/user-attachments/assets/cfb5415b-e309-486b-b972-f3fbbfdbc37a)


$$
k_1 y = F, \quad k_2 (x - y) = F
$$


La eliminación de \( y \) en estas dos ecuaciones resulta en:


$$
k_2 \left( x - \frac{F}{k_1} \right) = F
$$


o bien:


$$
k_2 x = F + \frac{k_2}{k_1} F = \frac{k_1 + k_2}{k_1} F
$$


La constante de resorte equivalente \( k_{eq} \) para este caso se encuentra entonces como:


$$
k_{eq} = \frac{F}{x} = \frac{k_1 k_2}{k_1 + k_2} = \frac{1}{\frac{1}{k_1} + \frac{1}{k_2}}
$$


Para la solución gráfica, nótese que:


$$
\frac{AC}{PQ} = \frac{AB}{PB}, \quad \frac{BD}{PQ} = \frac{AB}{AP}
$$


de la cual:


$$
PB = \frac{AB \cdot PQ}{AC}, \quad AP = \frac{AB \cdot PQ}{BD}
$$


Puesto que \( AP + PB = AB \), tenemos:


$$
\frac{AB \cdot PQ}{BD} + \frac{AB \cdot PQ}{AC} = AB
$$


o bien:


$$
\frac{PQ}{BD} + \frac{PQ}{AC} = 1
$$


Resolviendo para \( PQ \), obtenemos:


$$
PQ = \frac{1}{\frac{1}{AC} + \frac{1}{BD}}
$$


De modo que si las longitudes AC + BD representan a las constantes de resorte k, y
k,, respectivamente, entonces la longitud PX representa la constante de resorte
equivalente k,,. Esto es


$$
\bar{PQ} = \frac{1}{\frac{1}{k_1} + \frac{1}{k_2}} = k_{eq}
$$


$$
**Ejemplo 2**
$$


Hallar el modelo dinamico y las ecuaciones de estado del siguiente sistema masa-resorte-amostiguador de doble masa.

![image](https://github.com/user-attachments/assets/40e52605-f1d3-4dac-9cf3-ab9d1d34724d)


Para la masa No.1:

Realizamos el diagrama de cuerpo libre

![image](https://github.com/user-attachments/assets/4c8e01db-faac-4180-8472-b4bdd1793f5f)


La ecuación de la masa 1 quedaria:

$$
m_1 \ddot{x}_1 + b_1 \dot{x}_1 + k_1 x_1 + k_2 (x_1 - x_2) = u
$$

Para la masa No.2:

Realizamos el diagrama de cuerpo libre:

![image](https://github.com/user-attachments/assets/16ffda94-e334-411c-a5e6-80619dd24162)


La ecuación de la masa 2 quedaria: 

$$
m_2 \ddot{x}_2 + k_2 (x_2 - x_1) = 0
$$

Es decir que las ecuaciones difrenciales del sistemas son;

$$
m_1 \ddot{x}_1 + b_1 \dot{x}_1 + k_1 x_1 + k_2 (x_1 - x_2) = u
$$
$$
m_2 \ddot{x}_2 + k_2 (x_2 - x_1) = 0
$$

Definimos las variables de estado:

$$
z_1 = x_1 \quad \text{(posición de } m_1 \text{)}
$$

$$
z_2 = \dot{x}_1 \quad \text{(velocidad de } m_1 \text{)}
$$

$$
z_3 = x_2 \quad \text{(posición de } m_2 \text{)}
$$

$$
z_4 = \dot{x}_2 \quad \text{(velocidad de } m_2 \text{)}
$$

Ecuaciones de estado:

$$ 
\dot{z}_1 = z_2 
$$

$$
\dot{z}_2 = \frac{1}{m_1}\left( u - b_1 z_2 - k_1 z_1 - k_2\,(z_1 - z_3) \right) 
$$

$$ 
\dot{z}_3 = z_4 
$$

$$ 
\dot{z}_4 = -\frac{k_2}{m_2}\,(z_3 - z_1) 
$$

# 17/03/2025

$$
Ejemplo 1
$$

Una masa m está suspendida por dos resortes en la Fig. 2-40.
Uno de los resortes es una viga en cantilever con constante de resorte k, si se carga
transversalmente en su extremo. El otro resorte es uno de tensión-compresión con
constante de resorte k2. Determínese la deflexiíin estática 6 de la masa cuando se la
mide desde la posición en la cual el resorte no tiene carga. Determínese también la frecuencia natural del sistema. 


![image](https://github.com/user-attachments/assets/0083812d-c6ed-4d59-8f4e-787e0a363375)



En cierto sentido los dos resortes están conectados en serie, la constante
de resorte equivalente k_eq es:

$$
k_{eq} = \frac{k_1 k_2}{k_1 + k_2}
$$

Entonces, la deflexión \( \delta \) estática es:

$$
\delta = \frac{mg}{k_{eq}}
$$

La frecuencia natural del sistema es:

$$
\omega_n = \sqrt{\frac{k_{eq}}{m}}
$$


$$
**Ejemplo 2**
$$

Una masa 𝑚 m está suspendida mediante dos resortes, como se muestra en la figura. El primero de ellos, con constante elástica k1 ​ , está dispuesto de forma vertical y conectado al suelo. El segundo, con constante 𝑘2, está inclinado y sujeto a una estructura fija, formando un ángulo 𝜃 con la horizontal. Se pide determinar la deflexión vertical estática 𝛿 de la masa, medida desde la posición en la cual los resortes no están deformados. Asimismo, se solicita calcular la frecuencia natural de vibración del sistema para pequeñas oscilaciones en dirección vertical.

![image](https://github.com/user-attachments/assets/0a7f8fa8-3ab2-4051-918f-bc3d2eb5951c)

a) Deflexión estática \( \delta \)

Considerando equilibrio estático:

$$
mg = F_{k_1} + F_{k_2, \text{vertical}}
$$

Donde:

$$
F_{k_1} = k_1 \cdot \delta
$$

$$
F_{k_{2,\text{vertical}}} = k_2 \cdot \delta \cdot \sin^2(\theta)
$$

Entonces:

$$
mg = \delta (k_1 + k_2 \cdot \sin^2(\theta))
$$

Despejando \( \delta \):

$$
\delta = \frac{mg}{k_1 + k_2 \cdot \sin^2(\theta)}
$$

b) Frecuencia natural \( \omega_n \)

La constante equivalente del sistema en dirección vertical es:

$$
k_{eq} = k_1 + k_2 \cdot \sin^2(\theta)
$$

Entonces, la frecuencia natural (en rad/s) es:

$$
\omega_n = \sqrt{\frac{k_{eq}}{m}} = \sqrt{\frac{k_1 + k_2 \cdot \sin^2(\theta)}{m}}
$$

# 21/03/2025

**Sistemas Rotacionales**

Es un fenomeno mecanico pero la naturaleza del movimiento cambia, ahora es movimiento angular

$$
**Ejemplo 1**
$$


Un cilindro hom~o con radio de 1 m tiene una masa de 100 kg.
cuál será su aceleración angular si se le aplica un par externo de 10 N-m alrededor del
eje del cilindro? 

El momento de inercia J es


$$
J = \frac{1}{2} mR^2 = \frac{1}{2} \times 100 \times 1^2 = 50 \, \text{kg·m}^2
$$

La ecuación de movimiento del sistema es:

$$
J\ddot{\theta} = T
$$

donde \( \ddot{\theta} \) es la aceleración angular. Por lo tanto:

$$
\ddot{\theta} = \frac{T}{J} = \frac{10 \, \text{N·m}}{50 \, \text{kg·m}^2} = 0.2 \, \text{rad/s}^2
$$

(Nótese que al examinar las unidades de esta última ecuación, vemos que la unidad
de 0 no es S-"ino rad/r2. Este uso aparece porque al escribir rad/~-~ se indica que el
ángulo 8 está medido en radianes. El radián es una medida del ángulo y es la relación
de la longitud del arco con respecto al radio. Así pues, medido en radianes, el ángulo
es un número puro. En el manejo ,algebraico de upidades la unidad "radián" se añade
cuando sea necesario.)


$$
**Ejemplo 2**
$$

Supongamos que se tiene una rueda maciza, como las de un carro de supermercado, con un radio de 0.4 metros y una masa de 20 kg. Esta rueda está montada sobre un eje horizontal sin fricción y se le aplica un par constante de 8 N·m. Se quiere saber cuál será su aceleración angular cuando se le aplica ese par.

El momento de inercia \( J \) de una rueda maciza alrededor de su eje es:

$$
J = \frac{1}{2} m R^2 = \frac{1}{2} \cdot 20 \cdot (0.4)^2 = 1.6 \, \text{kg·m}^2
$$

Usamos la ecuación del movimiento rotacional:

$$
T = J \ddot{\theta} \Rightarrow \ddot{\theta} = \frac{T}{J}
$$

Entonces:

$$
\ddot{\theta} = \frac{8}{1.6} = 5 \, \text{rad/s}^2
$$

Por lo tanto, la aceleración angular de la rueda es de

$$
\( 5 \, \text{rad/s}^2 \).
$$



# 28/03/2025

# **Sistemas Electricos**

**Voltaje**

El voltaje en los sistemas eléctricos es análogo a la presión en
los sistemas hidráulicos o neumáticos. Esta es la fuerza electromotriz requerida para producir un flujo de corriente en un alambre, es como la presibn que se requiere para producir un flujo de liquido o gas en una tubería.
La unidad de voltaje es el volt (V). 

**Corriente** 

La corriente se refiere a la razón de cambio del flujo de carga. La unidad de corriente es el ampere. Si una carga de dq coulombs cruza
un área dada en dt segundos.

![image](https://github.com/user-attachments/assets/4e97def6-00f7-43bd-94af-8b5b15b41b08)


**Elementos resistivos** 

La Resistividad se define como el cambio en voltaje requerido para producir un cambio unitario en la corriente

![image](https://github.com/user-attachments/assets/b6b5d7b8-9021-4deb-999c-1e4d05611b0b)


**Elementos capacitivos** 

Dos conductores separados por un medio no
conductor (aislante o dieléctrico) forman un capacitor. De modo que dos
placas metálicas separadas por un material eléctrico muy delgado forman
un capacitor. Algunas veces el área se hace variable, como en un condensador de sintonización de un radio. 

![image](https://github.com/user-attachments/assets/58baa72b-d1a5-4a36-a4de-a9a679c514a5)


$$
Ejemplo 1
$$


Dado el circuito que se muestra, obténgase un modelo matemhtico. Aquí las corrientes 4 e S son corrientes cíclicas.

![image](https://github.com/user-attachments/assets/5e9e9804-f5aa-4791-bc34-5a2e256a2575)


$$
\begin{align*}
R_i I_1 + \frac{1}{C}\int (i_1 - i_3)\, dt &= E \\
L\frac{d i_2}{dt} + R_2 I_2 + \frac{1}{C}\int (i_2 - i_1)\, dt &= 0
\end{align*}
$$

Estas dos ecuaciones constiuyen un modelo matematico del circuito. 

$$
Ejemplo 2
$$

Análisis de circuito RLC con variables de estado

En el siguiente circuito eléctrico RLC en serie-paralelo, se desea determinar cómo evolucionan la corriente \( i_2(t) \) que circula por la resistencia \( R_2 \) y el voltaje \( V_C(t) \) en el capacitor, con el paso del tiempo.

![image](https://github.com/user-attachments/assets/06f0670d-2865-48c0-be8c-ef65ce22ff99)


El circuito cuenta con:

- Una fuente de voltaje continua de

$$
\( V(t) = 10\, \text{V} \)
$$

- Una resistencia

$$
\( R_1 = 2\, \Omega \)
$$

en serie con una inductancia

$$
\( L = 1\, \text{H} \)
$$

- Una segunda resistencia

$$
\( R_2 = 3\, \Omega \)
$$

y un capacitor

$$
\( C = 0.5\, \text{F} \)
$$

en paralelo con respecto a la bobina

Las condiciones iniciales del sistema son:  

$$
\( i_2(0) = 0\, \text{A} \)
$$ 

$$
\( V_C(0) = 0\, \text{V} \)
$$

Se pide obtener las **ecuaciones diferenciales** que describen el comportamiento dinámico del sistema usando **variables de estado**.

#### Variables de estado

$$
x(t) =
\begin{bmatrix}
i_2(t) \\
V_C(t)
\end{bmatrix}
$$

Ecuaciones dinámicas del sistema

1. Derivada de \( i_2(t) \)**

$$
\frac{di_2}{dt} =
\frac{1}{L} \left[
V -
\frac{R_1 R_2}{R_1 + R_2} i_2 +
\frac{R_1}{R_1 + R_2} V_C -
\frac{R_1}{R_1 + R_2} V
\right]
$$

Sustituyendo valores:

$$
\frac{di_2}{dt} =
10 -
\frac{6}{5} i_2 +
\frac{2}{5} V_C -
4
$$

$$
\Rightarrow \quad
\frac{di_2}{dt} =
6 - \frac{6}{5} i_2 + \frac{2}{5} V_C
$$

2. Derivada de \( V_C(t) \)**

$$
\frac{dV_C}{dt} =
\frac{1}{C} \left[
\frac{R_2}{R_1 + R_2} i_2 -
\frac{1}{R_1 + R_2} V_C +
\frac{1}{R_1 + R_2} V
\right]
$$

Sustituyendo:

$$
\frac{dV_C}{dt} =
2 \left(
\frac{3}{5} i_2 -
\frac{1}{5} V_C + 2
\right)
$$

$$
\Rightarrow \quad
\frac{dV_C}{dt} =
\frac{6}{5} i_2 - \frac{2}{5} V_C + 4
$$


Resultado final del sistema

$$
\begin{cases}
\frac{di_2}{dt} = 6 - \frac{6}{5} i_2 + \frac{2}{5} V_C \\
\frac{dV_C}{dt} = \frac{6}{5} i_2 - \frac{2}{5} V_C + 4
\end{cases}
$$


# 31/03/2025

$$
Ejemplo 1
$$

Encuéntrense las corrientes i1, i2, i3 del circuito.

![image](https://github.com/user-attachments/assets/e783f91d-e319-4fc0-9114-8d66db6e89ed)


Al aplicar la ley de voltajes y la ley de corrientes de Kirchhoff, tenemos:

$$
\begin{align*}
12 - 10i_1 - 5i_3 &= 0 \\
8 - 15i_2 - 5i_3 &= 0 \\
i_1 + i_2 - i_3 &= 0
\end{align*}
$$

Resolviéndolas para i1, i2, i3 dan:

$$
i_1 = \frac{8}{11} \, \text{A}, \quad i_2 = \frac{12}{55} \, \text{A}, \quad i_3 = \frac{52}{55} \, \text{A}
$$

Puesto que todos los valores de i resultaron positivos, las corrientes fluyen en las direcciones mostradas en el diagrama

$$
Ejemplo 2
$$

Encontrar las corrientes i1, i2 y i3 en el siguiente circuito.

Una batería de 10V está conectada en la malla izquierda con resistencias de 6Ω y 4Ω, y una batería de 5V en la malla derecha con una resistencia de 12Ω. Encuentra las corrientes i1, i2, e i_3 utilizando la Ley de Kirchhoff de Voltajes (LKV) y la Ley de Corrientes (LKC).

![image](https://github.com/user-attachments/assets/87afaeb1-0b6a-4397-bee6-3dbca1b4875e)

Al aplicar la ley de voltajes y corrientes de Kirchhoff, se obtienen las siguientes ecuaciones:

$$
10 - 6i_1 - 4i_3 = 0
$$

$$
5 - 12i_2 - 4i_3 = 0
$$

$$
i_1 + i_2 - i_3 = 0
$$

Resolviendo el sistema de ecuaciones:

1. De la primera ecuación:

$$
10 - 6i_1 - 4i_3 = 0 \Rightarrow 6i_1 + 4i_3 = 10 \Rightarrow i_1 = \frac{10 - 4i_3}{6}
$$

2. De la segunda ecuación:

$$
5 - 12i_2 - 4i_3 = 0 \Rightarrow 12i_2 + 4i_3 = 5 \Rightarrow i_2 = \frac{5 - 4i_3}{12}
$$

3. Sustituyendo \( i_1 \) e \( i_2 \) en la tercera ecuación:

$$
\left(\frac{10 - 4i_3}{6}\right) + \left(\frac{5 - 4i_3}{12}\right) - i_3 = 0
$$

Multiplicamos toda la ecuación por 12 para eliminar denominadores:

$$
2(10 - 4i_3) + (5 - 4i_3) - 12i_3 = 0
$$

$$
20 - 8i_3 + 5 - 4i_3 - 12i_3 = 0
$$

$$
25 - 24i_3 = 0 \Rightarrow i_3 = \frac{25}{24} \, A
$$

4. Reemplazamos \( i_3 \) para encontrar \( i_1 \) y \( i_2 \):

$$
i_1 = \frac{10 - 4\left(\frac{25}{24}\right)}{6} = \frac{10 - \frac{100}{24}}{6} = \frac{\frac{240 - 100}{24}}{6} = \frac{\frac{140}{24}}{6} = \frac{140}{144} = \frac{35}{36} \, A
$$

$$
i_2 = \frac{5 - 4\left(\frac{25}{24}\right)}{12} = \frac{5 - \frac{100}{24}}{12} = \frac{\frac{120 - 100}{24}}{12} = \frac{\frac{20}{24}}{12} = \frac{20}{288} = \frac{5}{72} \, A
$$

**Solución final:**

$$
i_1 = \frac{35}{36} \, A \quad ; \quad i_2 = \frac{5}{72} \, A \quad ; \quad i_3 = \frac{25}{24} \, A
$$

