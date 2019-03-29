### Y cuantas ecuaciones mas de 1D vamos a ver?

#### Ejemplo: Laser de estado solido

Tengo $n = n(t)$ el numero de fotones en el campo laser y $N = N(t)$ el numero de atomos excitados que tenemos.

$$\frac{dn}{dt} = \text{ganancia} - \text{perdida}$$

$$\frac{dn}{dt} = G n N - k n$$

La tasa de emision estimulada va a ser proporcional a la cantidad de ambos que tenga, ademas tengo fotones que se escapan. Ademas tengo (no se porque)

$$N = N_0 - \alpha n$$

$$ \Rightarrow \frac{dn}{dt} = (G N_0 - k)n - \alpha G n^2$$

Que pasa si busco dibujar el espacio de fases?

Tengo distintos comportamientos dependiendo el signo de $G N_0 - k$.

* Si $G N_0 - k <= 0$ tengo un solo punto fijo en $n = 0$, y es atractivo.
* Si $G N_0 - k > 0$ tengo 2 puntos fijos, una en 0 y otra en un $n^* = \frac{G N_0 - k}{\alpha G}$. No solo me aparece una nueva solucion sino que pasa a ser el atractivo, y el otro repulsivo.

Si se tiene esa relacion de parametros, se llega a la emision estimulada y se tiene un laser.

Si se grafica $n$ en funcion del parametro $G$, se tiene que se genera una bifurcacion. Viene siendo $0$ y se combierte en una recta.

Haciendo un cambio de variable,

$$\frac{dn}{d\tau} = \frac{GN_0 - k}{\alpha G}n - n^2,\; \text{con} t = \frac{\tau}{2G}$$

En general se tienen 3 casos distintos:

* Caso de la aparicion de atractor-repultor:
  $$\frac{dx}{dt} = r + 0x - x^2 + 0x^3$$

* Transcritica (caso del laser):
  $$\frac{dx}{dt} = 0 + rx - x^2 + 0x^3$$

* Tridente (pitchfork):
  $$\frac{dx}{dt} = 0 + r x + 0 x^2 - x^3$$

Todo pareceria venir de un Taylor con algunos coeficientes nulos.

##### Podremos clasificar "formas paradigmaticas" a un orden dado, clasificando los coeficientes del desarrollo del campo vector?

#### Ejercicio:

Bolita sobre en un aro que gira.

$$m r \ddot{\theta} = -m g \sin \theta + m \omega^2 r \sin \theta \cos \theta - b \dot{\theta}$$

Para resolver, hay que como siempre dividirlo en un sistema de 2 ecuaciones de primer orden, y ademas cambiar la escala temporal para limpiar constantes.

$t = \gamma \tau$, por lo tanto $\frac{d}{dt} = \frac{1}{\gamma}\frac{1}{d\tau}$, y vale que:

$$\frac{mr}{mg \gamma^2}\frac{d^2\theta}{d\tau^2} = - \cancel{mg}\sin \theta + \frac{\cancel{m} \omega^2 r}{\cancel{m} g}\sin \theta \cos \theta - \frac{b}{mg} \frac{d\theta}{d\tau}$$

Eligiendo $\gamma = \frac{b}{mg}$, podemos elegir:

$$\frac{r}{g\gamma^2} << 1 \Rightarrow b^2 >> m^2 g r$$

Entonces tenemos Que

$$\epsilon \frac{d^2 \theta}{d \tau^2} = \sin \theta\left(\frac{r\omega^2}{g} \cos \theta -1\right)$$

Para escribir todo como un sistema de ecuaciones diferenciales de primer orden,

$$\left \{ \begin{matrix} \frac{d\theta}{d\tau} = \Omega \\ \frac{d\Omega}{d\tau} = \frac{1}{\epsilon} \left(-\frac{d\theta}{d\tau} + \sin\theta(\frac{r\omega^2}{g}\cos \theta - 1)    \right) \end{matrix} \right.$$

Definiendo $f(\theta) = \sin\theta(\frac{r\omega^2}{g}\cos \theta - 1)$, tenemos que $\frac{d\Omega}{d\tau} =\frac{1}{\epsilon}( - \Omega +f(\theta))$. Tenemos que cuando $\Omega \neq f(\theta)$, el sistema se aviolenta para volver a ese estado, por lo que tiene sentido plantear el problema como $\frac{d\theta}{d\tau} = f(\theta)$.


Pensemos en 2 casos extremos, $\omega \simeq 0$ y $\frac{r\omega^2}{g} >> 1$. Para el primero, tenemos que tenemos un punto fijo en cero que es atractor, y uno repulsor en $\pi$. Para el otro caso sin embargo, tenemos $\frac{d\theta}{d\tau} \simeq \frac{r\omega^2}{2g}\sin 2\theta$, por lo que 0 se convierte en repulsor, y aparecen los puntos fijos en $\pm\frac{\pi}{2}$ que son atractores. Esto hace acordar al caso que se nombro antes de tridente, que es lo que queda de tarea chequear. (Para chequearlo, habria que hacer el Taylor sobre el campo vector y fijarse que se anulen los coeficientes correspondientes).

#### Problema unidimensional divertido

_Pendulo fisico en un tambor rotatorio de miel_

$$\cancel{\epsilon\ddot{\theta}} + \dot{\theta} = \omega - \sin \theta$$
