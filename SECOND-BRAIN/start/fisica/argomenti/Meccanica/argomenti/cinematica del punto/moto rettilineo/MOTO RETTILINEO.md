# Definizione di moto rettilineo
È un movimento che avviene lungo una retta, ovvero la traiettoria è una linea dritta).
### Accelerazione nel moto rettilineo

$a=\frac{dv}{dt}$  $\to$  $dv=a(t)dt$  $\to$  $\Delta v=v_2-v_1=\int_{v_1}^{v_2}dv=\int_{t_1}^{t_2}a(t)dt$  

**Relazione generale**: $v(t)=v_0+\int_{t_0}^{t}dt$ 


### Moti periodici
Moti la cui legge oraria è una **funzione periodica f(t)** del tempo:$$f(t+T)=f(t)$$
**Teorema di Fourier**: una qualsiasi funzione periodica è esprimibile come una serie di termini sinusoidali.

Può essere:
## 1) Moto rettilineo uniforme
Il moto è detto uniforme quando la velocità è costante sia positiva che negativa

### Legge oraria
$$s(t)=s_0+v\cdot t$$

$$x(t)=x_0+\int_{t_0}^{t}v(t)dt=x_0+v\int_{t_0}^{t}dt=x_0+v(t-t_0)$$
$$\int_{t_0}^{t}Kdt=K\int_{t_0}^{t}dt=K(t-t_0)$$

$x(t)=x_0+V(t-t_0) \to$ con $V$ costante
essendo la velocità costante l'accelerazione $=0$
$$\begin{cases}x(t)=x_0+V(t-t_0) \\ V(t)=costV \\ a(t)=0\end{cases}$$

### Esempi:
$x(t)=3+2t$  **relazione lineare** $\frac{x-3}{t}=2$ 
$x(t)=3t$  **relazione di proporzionalità diretta** $\to \frac{x(t)}{t}=3$ 
$x(t)=2t+t^2$  non è un moto rettilineo uniforme perché $V$ dipende dal tempo($t$) e quindi **moto uniformemente accelerato**


## 2) Moto rettilineo accelerato
### Accelerazione media
$$a_m=\frac{\Delta V}{\Delta t}=\frac{v_2-v_1}{t_2-t_1}$$

### Accelerazione istantanea
$$a=\lim_{\Delta t \to 0} \frac{\Delta V}{\Delta t}= \frac{dV}{dt}=\frac{d^2x}{dt^2}$$
- $a=0 \to$ v=cost $\to$ moto rettilineo uniforme
- $a=cost \to$ moto rettilineo uniformemente accelerato
- $a$ non è costante $\to$ moto vario $\to$ $a(t)$
- $a>0 \to$ la velocità cresce
- $a<0 \to$ la velocità decresce



$$a=\frac{dV}{dt} \to dV=a(t)dt=\int_{v_0}^{v}dV=\int_{t_0}^{t}a(t)dt$$

$$V(t)-V_0=\int_{t_0}^{t}a(t)dt \to V(t)=V_0\cdot t\int_{t_0}^{t}a(t)dt$$

$$a(t)=\frac{dx}{dt}=\frac{dV}{dx}\cdot\frac{dx}{dt}=\frac{dV}{dt}\cdot V=VdV$$
$$\int_{x_1}^{x_2}a(x)dx=\int_{v_1}^{v_2}Vdv=\frac{V^2_2-V^2_1}{2}$$




# Moto rettilineo uniformemente accelerato
$a=costante$   $V(t)=V_0+a\cdot(t-t_0)$ 

$$X(t)=x_0+\int_{t_0}^{t}[V_0+a\cdot (t-t_0)]dt=x_0+V_0(t-t_0)+\frac{1}{2}\cdot a(t-t_0)^2$$ $$\begin{cases}a(t)=cost=a \\ V(t)=V_0+a(t-t_0) \\ x(t)=x_0+V_0(t-t_0)+\frac{1}{2}a(t-t_o)^2\end{cases}$$
$$a(x_2-x_1)=\frac{V_2^2-V_1^2}{2}$$
$$V_f^2=V_i^2+2a(t_f-t_i)$$





# Moto uniformemente vario
$$x(t)=x_0+V_0t+\frac{1}{2}at^2$$
### Esempio:
$x(t)=3+4t+8t^2$
$x_0=3m$  $V_0=4m/s$  $a=16m/s^2$
$V(t)=4+16t$
$a(t)=\frac{dV}{dt}$  $a\cdot dt=dv$  
$\int_{v_0}^{v}dv=\int_{0}^{t}adt \to (V-V_0)=at \to V(t)=V_0+at \to V(t)=\frac{dx}{dt} \to Vdt=dx \to \int_{x_0}^{x}dx=\int_{0}^{t}Vdt$
$x-x_0=\int_{0}^{t}(V_0+at)dt=\int_{0}^{t}V_0dt+\int_{0}^{t}atdt$
$x-x_0=V_0t+\frac{1}{2}at^2$


# Moto dei gravi o moto verticale di un punto
## Moto con accelerazione costante
$a=-g=-9,81 m/s^2$
$x(t)=x_0+v_0(t-t_0)+\frac{1}{2}a(t-t_0)^2$ 

$x(t)=x_0+v_0t-1/2gt^2$ oppure $y(t)=y_0+v_0t-1/2gt^2$

$v(t)=v_0+a(t-t_0)$

## Moto verticale
Corpo lanciato da terra verso l'alto con velocità iniziale $v_0$
le condizioni sono $x_0=0,v_0>0,t_0=0,a=-g$ 
$x(t)=v_0t-\frac{1}{2}gt^2$    $v(t)=v_0-gt$

tempo di salita (v=0)  $t(v=0)=v_0/g=\sqrt{2h/g}$ 
altezza massima (v=0)  $x(v=0)=h=\frac{v_0^2}{2g}$ 



# Moto armonico semplice
Questo moto segue la legge oraria.
$x(t)=Asen(\omega t+\phi)$
$A$:ampiezza $\equiv$ max. valore di $x$
$\omega t+\phi$: fase
$\omega$: pulsazione
$\phi$: fase iniziale $\equiv$ fase per $t=0$

**Moto periodico**: la funzione seno è periodica. Il punto descrive un'oscillazione.
Il periodo T dell'oscillazione viene dato da: per definizione di periodo allora le fasi devono essere.
$$T=t_2-t_1\to x(t_2)=x(t_1)\to \omega t_2+\phi=\omega t_1+\phi+2\pi\to2-t_1=2\pi/\omega=T$$
definiamo la frequenza: $\nu=\frac{1}{T}=\frac{\omega}{2\pi}$  

## Velocità e accelerazione nel moto armonico semplice
$x(t)=Asen(\omega t+\phi)$
$v(t)=\frac{dx}{dt}\to v(t)=\omega Acos(\omega t+\phi)$

$a(t)=\frac{dv}{dt}\to a(t)=-\omega ^2 Asen(\omega t+\phi)=-\omega ^2x(t)$ 

## Equazione differenziale

$\frac{d^2x}{dt^2}=-\omega^2xt(t)$ 

$x(t)=Asen(\omega t+\phi)$
$x(t)=Acos(\omega t+\phi)$




# Moto smorzato esponenzialmente
L'accelerazione è di segno opposto alla velocità e proporzionale ad essa:
$a=-kv$

## Calcolare la velocità a partire dall'accelerazione
$a=\frac{dv}{dt}=-kv$  $\to$  $dv=-k\cdot v \cdot dt$  $\to$   $\frac{dv}{v}=-k\cdot dt$  $\to$   
$\int_{v_0}^{v}\frac{dv}{v}=-k\int_{0}^{t}dt$  $\to$  $ln\frac{v}{v_0}=-kt$  $\to$   $v(t)=v_0e^{-kt}$

## Calcolare come varia la velocità in funzione della posizione
$$a=\frac{dv}{dt}=\frac{dv}{dx}\frac{dx}{dt}=\frac{dv}{dx}v=-kv$$
$\frac{dv}{dx}=-k$  $\to$  $dv=-kdx$  $\to$  $\int_{v_0}^{v}dv=-k\int_{x_0}^{x}dx$   $v(x)=v_0-k(x-x_0)$ 

**QUANTO TEMPO IMPIEGA PER FERMARSI**:
$v(t)=v_0e^{-kt}=0 \to t \to \infty$

$x(t)=\frac{v_0}{k}(1-e^{-kt})$


# Accenni ad integrale
$V(t)=\frac{dx}{dt}$     $V(t) \to x(t)=?$

$$\int_{x_0}^{x}dx=\int_{t_0}^{t}V(t)\cdot dt \to \int_{x_0}^{x}x(t)=\int_{t_0}^{t}V(t)\cdot dt \to x(t)-x_0$$