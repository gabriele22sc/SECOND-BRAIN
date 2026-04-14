La traiettoria è una circonferenza o un arco di circonferenza, dove l'accelerazione centripeta è sempre diversa da zero.
La posizione viene individuata da $s(t)$ o da $\theta(t)$ 

$s(t)=R\theta(t)$            $\vec{v}_r=v\vec{u}_r=0$   
$v=v_\theta=\frac{ds}{dt}=R\frac{d\theta}{dt}=R\omega$  

### Velocità angolare
$\omega=\frac{d\theta}{dt}=\frac{1}{R}\frac{ds}{dt}=\frac{v}{R}$  
### Velocità angolare media
$\omega_m=\frac{\Delta\theta}{\Delta t}$ 
### Velocità angolare istantanea
$\omega=\frac{d\theta}{dt}$
 
La velocità cambia continuamente direzione $\to$ il moto è accelerato
La velocità angolare è proporzionale alla velocità con cui è descritta la circonferenza, se $v$ è variabile lo sarà anche $\omega$.
### Accelerazione normale sempre rivolta verso il centro
$$a_N=\frac{v^2}{R}=\omega^2R$$
### Accelerazione tangente
$$a_T=\frac{dv}{dt}=R\frac{d\omega}{dt}=R\alpha$$
### Accelerazione angolare
$$\alpha=\frac{d\omega}{dt}=\frac{d^2\theta}{dt^2}=\frac{a_T}{R}$$



# Moto circolare uniforme
Il moto circolare uniforme è un moto accelerato con accelerazione costante, ortogonale alla traiettoria.

![[moto-circolare.png]]
$v=$costante,   $\omega=$costante
$a_T=0$, $\alpha=0$
$a_N=\frac{v^2}{R}=\omega^2R=$costante

**Legge oraria**:
$\theta(t)=\theta_0+\omega t$   $\theta=\theta_0$   per   $t=0$
$s(t)=s_0+vt$   $s=s_0$   per   $t=0$

**Moto periodico**:
$T=\frac{2\pi R}{v}=\frac{2\pi}{\omega}$

**Accelerazione tangenziale**:
$a_T=\frac{dv}{dt}$

**Accelerazione angolare**:
$a=a_N=\frac{v^2}{R}=\omega^2R$

**Accelerazione angolare media**:
$a_m=\frac{\Delta\omega}{\Delta t}$ 

**Accelerazione angolare istantanea**:
$a=\frac{d\omega}{dt}=\frac{d^2\theta}{dt^2}=\frac{1}{R}\frac{dv}{dt}=\frac{a_T}{R}$



Proiezioni sugli assi cartesiani:
$x(t)=Rcos\theta(t)=Rcos(\theta_0+\omega t)$
$y(t)=Rsen\theta(t)=Rsen(\theta_0+\omega t)$
Descrivono due moti armonici, tra loro in quadratura, con pulsazione NUMERICAMENTE uguale alla velocità angolare

Unità di misura$[\omega]$=radianti/secondi= $rad/s$


# Moto circolare uniformemente accelerato
$a_T=$ costante, $\alpha=$ costante

$\omega(t)=\omega_0+\alpha t$   ,   $\theta(t)=\theta_0+\omega_0t+\frac{1}{2}\alpha t^2$

**Accelerazione centripeta**:
$a_N=\omega^2R=(\omega_0+\alpha t)^2R$ 

calcolare l'incremento della velocità angolare in corrispondenza dell'incremento angolare $\theta-\theta_0$:
$\alpha=\frac{d\omega}{dt}=\frac{d\omega}{d\theta}\frac{d\theta}{dt}=\omega\frac{d\omega}{d\theta}\quad\to\quad\alpha d\theta=\omega d\omega$ 
$\int_{\theta_0}^{\theta}\alpha(\theta)d\theta=\frac{1}{2}\omega^2-\frac{1}{2}\omega_0^2$ 



$a_N(t)=\omega^2R=(\omega_0+\alpha t)^2R$ variabile

Le equazioni hanno forma analoga a quelle del moto rettilineo uniformemente accelerato
$\theta(t)$,  $\omega(t)=\frac{d\theta}{dt}$,   $a(t)=\frac{d\omega}{dt}$

$$\theta(t)=\theta_0+\int_{t_0}^{t}\omega(t)dt$$
$$\omega(t)=\omega_0+\int_{t_0}^{t}a(t)dt$$
L'unità di misura:
$[a]=rad/s^2$ 