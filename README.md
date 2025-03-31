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
**Ejemplo**
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




# 21/03/2025


# 28/03/2025

# **Sistemas Electricos**


# 31/03/2025


# 04/04/2025
