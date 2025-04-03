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

![image](https://github.com/user-attachments/assets/f0d9c716-37c9-4a7f-be57-5b7aff82fa74)


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


---


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

![image](https://github.com/user-attachments/assets/1b50ce14-a89d-439b-973d-c762d332e057)

Para la masa No.1:

Realizamos el diagrama de cuerpo libre

![image](https://github.com/user-attachments/assets/4983d32d-2632-4a54-899a-9993b89a037e)

La ecuación de la masa 1 quedaria:

$$
m_1 \ddot{x}_1 + b_1 \dot{x}_1 + k_1 x_1 + k_2 (x_1 - x_2) = u
$$

Para la masa No.2:

Realizamos el diagrama de cuerpo libre:

![image](https://github.com/user-attachments/assets/88330a1d-6e34-48ee-bdee-d206fa9e922f)

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

Las ecuaciones de estado quedan de la siguiente forma:

( d(z1)/dt ) = (  z2  )  
( d(z2)/dt ) = ( (1/m1) * ( u - b1*z2 - k1*z1 - k2*(z1 - z3) ) )  
( d(z3)/dt ) = (  z4  )  
( d(z4)/dt ) = ( (-k2/m2) * (z3 - z1) )  


# 17/03/2025

$$
Ejemplo 1
$$

Una masa m está suspendida por dos resortes en la Fig. 2-40.
Uno de los resortes es una viga en cantilever con constante de resorte k, si se carga
transversalmente en su extremo. El otro resorte es uno de tensión-compresión con
constante de resorte k2. Determínese la deflexiíin estática 6 de la masa cuando se la
mide desde la posición en la cual el resorte no tiene carga. Determínese también la frecuencia natural del sistema. 


![image](https://github.com/user-attachments/assets/c8190496-ec0a-49a3-9278-57a1cd5048b5)


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
![image](https://github.com/user-attachments/assets/037c94bc-2464-444a-a09d-47adae258faa)

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



# 31/03/2025

$$
Ejemplo 1
$$

Encuéntrense las corrientes i1, i2, i3 del circuito.
![image](https://github.com/user-attachments/assets/17b7e82f-76d3-45f2-a69e-fad636d0ed22)

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


# 04/04/2025
