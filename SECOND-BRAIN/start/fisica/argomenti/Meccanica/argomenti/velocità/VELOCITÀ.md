Volendo determinare quantitativamente la rapidità dello spostamento, definiamo la velocità media:$$\begin{align}t=t_1 \to x=x_1 \\ t=t_2 \to x=x_2 \\ v_m=\frac{x_2-x_1}{t_2-t_1}=\frac{\Delta x}{\Delta t}\end{align}$$
![[velocità-media.png]]

$v_m$ dipende dall'intervallo di tempo $\Delta t$ 

L'unità di misura: $v=\frac{x}{t}=\frac{m}{s}$ (metro/secondo)


# Velocità istantanea
Se facciamo tendere $\Delta t$ a zero, il rapporto $\frac{\Delta x}{\Delta t}$ non dipende più da $\Delta t$ ma dall'istante in cui lo misuriamo:$$v=\lim_{\Delta t \to 0} \frac{\Delta x}{\Delta t}=\frac{dx}{dt}$$
![[velocità-istantanea.png]]

$v(t)=tan(\alpha(t))$

L’esistenza di questo limite (indipendentemente dal tipo di moto) è un fatto sperimentale ed implica che il moto DEVE essere continuo (e non a “salti”)

La velocità è l'ente fisico che rappresenta l'esistenza del limite, quindi la continuità del movimento.

La velocità è la tangente dell'angolo che forma la retta tangente alla curva oraria nell'istante $t_i$ con l'asse $x$.

Il segno della velocità indica il verso del moto. Se è nota $x(t)$ è sempre possibile calcolare $v(t)$ tramite derivazione.

## Problema inverso
nota $v(t)$ è possibile calcolare $x(t)$?$$\Delta x=\int_{x_0}^{x}dx=\int_{t_0}^{t}dt=x-x_0$$
$x(t)=x_0+\int_{t_0}^{t}v(t)dt$ 
Possiamo dire che:
nota $x(t)$  $\to$  derivata  $\to$  $v(t)$
nota $v(t)$  $\to$  integrale  $\to$  $x(t)$
