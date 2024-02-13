Sabemos que una métrica debe ser un tensor completamente simétrico y un tensor de esta naturaleza lo podemos expresar como:

$$
\begin{align*}
T_{ij} &= [T_{ij}]^{CT} + [T_{ij}]^{ST}, \\
%&= [T_{ij}]^{CT} + \left(\frac{T_{ij} + T_{ji}}{2}\right)
\end{align*}
$$

donde el primer término del segundo miembro de la ecuación es la parte con traza del tensor, mientras que el segundo término es la parte sin traza.

La parte con traza es simplemente la traza del tensor, que siendo un escalar, no se puede poner así nomás, así que hay que multiplicándola por la unidad de este caso, que vendría a ser la métrica $\gamma_{ij}$, para que pueda ser un tensor. Esta parte uno la escribe a conveniencia. En este caso se ha elegido como $2C$. Es como si uno tuviera un valor, $a$, de algo, pero yo lo reescribo como $a = 2b$ sólo por conveniencia y de ahí en adelante trabajo con $b$.

Ahora, para el segundo término, tengamos en cuenta que un tensor de rango dos tridimensional lo podemos expresar en términos de un tensor ($E_{ij}$) sin divergencia, un vector ($E_j$) sin divergencia y uno escalar ($E$). Si notas, esto es exactamente igual al teorema de Helmholtz, en donde un vector ($\hat{B}_i$) lo expresábamos en términos de otro vector ($B_i$) sin divergencia y un escalar ($B$). Pero el escalar es sólo eso, un escalar, así que para que sea vector, debemos aplicarle el gradiente.

Con esto tenemos que

$\hat{B}_i = B_i + D_i B.$

Y sé que estoy diciendo esto de forma bastante burda y abusando del lenguaje, pero es sólo para que se entienda la idea de lo que se hace.

Ahora, para este caso hacemos exactamente lo mismo, pero llevado a los tensores en cuestión. En este caso, el tensor quedaría más o menos expresado de esta manera: $ E_{ij} + D_i E_j + D_i D_j E $.
La cosa es que como estamos trabajando con tensores, aquí tenemos que tener en cuenta el efecto del cambio de índices, es decir, la simetría del tensor. De ahí que se incrementen el número de posibilidades. Es decir, podemos tomar no sólo $E_{ij}$, sino $E_{ji}$.

Es decir, el tensor debería considerar todas estas posibilidades. Abusando un poco de la notación, tendríamos:

$$
\begin{align*}
[T_{ij}]^{ST}
&= (E_{ij} + E_{ji}) + (D_i E_j + D_j E_i) + (D_i D_j E + D_j D_i E) \\
&= 2 E_{ij} + (D_i E_j + D_j E_i) + 2 D_i D_j E
\end{align*}
$$

Aquí $E_{ij} + E_{ji} = 2 E_{ij}$, porque como estamos descomponiendo la métrica y esta debe ser completamente simétrica, el cambio de índices no afecta. Lo mismo para $D_i D_j E$ y $D_j D_i E.$

El paréntesis de la mitad uno lo puede reescribir como para que la expresión quede más corta. Para eso uno puede tener en cuenta que un tensor completamente simétrico se puede expresar como:

$A_{(ij)} = \frac{1}{2}\left(A_{ij}+A_{ji}\right)$

Así que

$$
\begin{align*}
D_{(i} E_{j)} 
&= \frac{1}{2}\left(D_{i} E_j + D_{j} E_i\right)\\
2 D_{(i} E_{j)} 
&= \left(D_{i} E_j + D_{j} E_i\right)\\
\end{align*}
$$

Con esto tenemos una descripción más o menos completa del origen de la expresión. En cuando al término $\frac{\sigma_{ij}}{\mathcal{H}}$ que aparece en uno de los factores del primer término del miembro derecho de la ecuación 2.13, este término se añade simplemente por conveniencia, como se explica más adelante en el texto. Este se añade para que al hacer un cambio infinitesimal de coordenadas, la parte tensorial ($E_{ij}$) de las perturbaciones quede invariante. No es estrictamente necesario ponerlo, pero al hacerlo, el tensor $E_{ij}$ puede usarse entonces como una invariante de calibre. Por eso es que se introduce.
