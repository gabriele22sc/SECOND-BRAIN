
# Dinamica dei sistemi di punti materiali

**Forze esterne**: forze che agiscono sul sistema dell’esterno
**Forze interne**: forze tra i punti materiali

Su ciascun punto la forza risultante è: $$\vec{F}_i=\vec{F}_i^{(E)}+\vec{F}_i^{(I)}$$
Per le forze interne vale la terza legge di Newton: principio di azione e reazione $$\vec{F}_{i,j}^{(I)}=-\vec{F}_{j,i}^{(I)}$$
La risultante delle forze interne che agisce su un punto materiale non è nulla $$\vec{F}_i^{(I)}=\sum_j\vec{F}_{i,j}^{(I)}\neq0$$
Per il sistema di punti la risultante delle forze interne è nulla $$\sum_i\vec{F}_i^{(I)}=0$$


# Sistema di n punti materiali
**Quantità di moto totale**:$$\vec{P}=\sum^m_i\vec{p}_i$$
**Momento angolare totale**:$$\vec{L}=\sum^n_i\vec{r}_i\cdot\vec{p}_i=\sum_i^n\vec{r}_i\cdot m_i\vec{v}_i$$
**Energia cinetica totale**:$$E_k=\sum_i^n\frac{1}{2}m_iv_i^2$$
**Momento delle forze**:$$\vec{M}=\sum_i^n\vec{r}_i\cdot\vec{F}_i=\sum_i^n\vec{r}_i\cdot\vec{F}_i^{(I)}+\sum_i^n\vec{r}_i\cdot\vec{F}_i^{(E)}=0+\sum^n_i\vec{r}_i\cdot\vec{F}_i^{(E)}=\vec{M}^{(E)}$$

## Dimostrazione(Da fare)


# Centro di massa
È il punto geometrico la cui posizione è individuata dal raggio vettore($\vec{r}_{cm}$)$$\vec{r}_{cm}=\frac{m_1\vec{r}_1+m_2\vec{r}_2+…+m_n\vec{r}_n}{m_1+m_2+…+m_n}=\frac{\sum^n_{i=1}m_i\vec{r}_i}{\sum^n_{i=1}m_i}$$

![[Centro_di_massa.jpg]]

La posizione del c.m. non dipende dal sistema di coordinate
In un sistema cartesiano:$$x_{cm}=\frac{\sum_{i=1}^nm_ix_i}{\sum_{i=1}^nm_i}$$
$$y_{cm}=\frac{\sum^n_{i=1}m_iy_i}{\sum^n_{i=1}m_i}$$
$$z_{cm}=\frac{\sum^n_{i=1}m_iz_i}{\sum^n_{i=1}m_i}$$

# Cambio di sistema di coordinate
$$\vec{r’}_i=\vec{r}_i+\vec{O’O}$$
![[Sistema_di_coordinate1.jpg]]

$$\vec{r}’_{cm}=\frac{\sum^n_{i=1}m_i\vec{r}’_i}{\sum^n_{i=1}m_i}=\frac{\sum^n_{i=1}m_i(\vec{r}+\vec{O’O})}{\sum^n_{i=1}m_i}=\frac{\sum^n_{i=1}m_i\vec{r}_i}{\sum^n_{i=1}m_i}+\vec{O’O}=\vec{r}_{cm}+\vec{O’O}$$

![[Sistema_coordinate2.jpg]]
![[Sistema_c3.jpg]]


# Velocità del centro di massa
Se i punti materiali si muovono, anche il c.m. si muove ![[V_centro_di_massa.jpg]]
$$\vec{v}_{cm}=\frac{d\vec{r}_{cm}}{dt}=\frac{\sum_im_i\frac{d\vec{r}_i}{dt}}{\sum_im_i}=\frac{\sum_im_i\vec{v}_i}{\sum_im_i}=\frac{\vec{P}}{m}$$
$\vec{P}=\sum_im_i\vec{v}_i$   o   $\vec{P}=m\vec{v}_{cm}$
$m=\sum_im_i$

Possiamo pensare il c.m. come un punto materiale in cui è concentrata tutta la massa e che possiede la quantità di moto totale

N.B.: la quantità di moto può essere nulla anche se i punti si muovono
![[V2_centro_di_massa.jpg]]

# Teorema del moto del centro di massa

**Accelerazione del centro di massa**: $$\vec{a}_{cm}=\frac{d\vec{v}_{cm}}{dt}=\frac{\sum_im_i\frac{d\vec{v}_i}{dt}}{\sum_im_i}=\frac{\sum_im_i\vec{a}_i}{\sum_im_i}$$
$$\sum_im_i\vec{a}_i=\sum_i\vec{F}_i=\sum_i\vec{F}_i^{(I)}+\sum_i\vec{F}_i^{(E)}$$
$$=\vec{R}^{(E)}=m\vec{a}_{cm}=m\frac{dv_{cm}}{dt}=\frac{d\vec{P}}{dt}$$
La risultante delle forze esterne è uguale alla derivata rispetto al tempo della quantità di moto del sistema.
Le forze interne influenzano il moto dei singoli punti ma non il moto del c.m.

# Conservazione della quantità di moto
Se la risultante delle forze esterne è nulla: $\vec{R}^{(E)}=0$
$$\vec{a}_{cm}=0,\vec{v}_{cm}=\text{costante,}\vec{P}=\text{costante}$$
Quando la risultante delle forze esterne è nulla, la quantità di moto totale del sistema rimane costante nel tempo e il centro di massa si muove di moto rettilineo uniforme o resta in quiete.

# Teorema del momento angolare 
Il momento angolare totale è: $$\vec{L}=\sum^n_i\vec{r}_i\cdot\vec{p}_i=\sum_i^n\vec{r}_i\cdot m\vec{v}_i$$
Se il polo O si muove con $v_0$: $\frac{d\vec{r}_i}{dt}=\vec{v}_i-\vec{v}_0$

Quando si conserva il momento angolare:
$$\frac{d\vec{L}}{dt}=\sum^n_i\frac{d\vec{r}_i}{dt}\cdot m_i\vec{v}_i+\sum_i^n\vec{r}_i\cdot m_i\frac{d\vec{v}_i}{dt}$$
$$\frac{d\vec{L}}{dt}=\sum^n_i(\vec{v}_i-\vec{v}_0)\cdot m_i\vec{v}_i+\sum^n_i\vec{r}_i\cdot m_i\vec{a}_i$$



$\sum_im_i\vec{v}_i=\vec{P}=m\vec{v}_{cm}$    $\sum_i\vec{r}_i\cdot\vec{F}^{(I)}=\vec{M}^{(I)}=0$

$\vec{v}_i\cdot\vec{v}_i=0$ 

Se il sistema è inerziale:$$\frac{d\vec{L}}{dt}=-\vec{v}_0\cdot\sum^n_im_i\vec{v}_i+\sum^n_i\vec{r}_i\cdot(\vec{F}_i^{(I)}+\vec{F}_i^{(E)})=-\vec{v}_0\cdot m\vec{v}_{cm}+\vec{M}^{(E)}$$
$m_i\vec{a}_i=\vec{F}_i$

In un sistema di riferimento inerziale: $\frac{d\vec{L}}{dt}=\vec{M}^{(E)}$

Se $\vec{v}_0\cdot\vec{v}_{cm}=0$ la variazione del momento angolare nel tempo è dovuta all’azione del momento delle forze esterne.
Cioè se:
- il polo è fisso: $\vec{v}_0=0$
- il cm è fisso: $\vec{v}_{cm}=0$
- si prende come polo il cm: $\vec{v}_0=\vec{v}_{cm}$
- $\vec{v}_0||\vec{v}_{cm}$

**Conservazione del momento angolare**: Se $M^{(e)}$, calcolato rispetto a un dato polo $O$, è nullo allora $L$, calcolato rispetto allo stesso polo, si conserva.

Guarda problemi veloci dalla slide sistemi


# Sistema di riferimento del cm
Consideriamo un sistema con origine nel cm che non ruota ma solo trasla.
In generale è un sistema non inerziale e si verifica:$$\vec{r’}_{cm}=0, \quad\quad \vec{v’}_{cm}=0, \quad\quad \vec{a’}_{cm}=0$$

![[Sistema_di_riferimento.jpg]]

$\begin{align} \sum_im_i\vec{r’}_i=0 \\ \sum_im_i\vec{v}_i’=\vec{P}’=0 \\ \sum_im_i\vec{a}_i’=0\end{align}$  $\to$ Nel sistema del CM la quantità di moto totale è nulla.

$\vec{r}’_{cm}=\frac{\sum_im_i\vec{r}_i}{\sum_im_i}$

Dal teorema delle velocità relative: $\vec{\omega}=0$ e $\vec{v}_t=\vec{v}_{cm}$  $\to$  $\begin{align}\vec{r}_i=\vec{r}’_i+\vec{r}_{cm} \\ \vec{v}_i=\vec{v}_i’+\vec{v}_{cm}\end{align}$


# Teorema di König per l’energia cinetica
L’energia cinetica di un sistema di punti $E_k=\sum_i\frac{1}{2}m_iv_i^2$ 
$$E_k=\sum_i\frac{1}{2}m_i(\vec{v}’_i+\vec{v}_{cm})^2=\sum_i\frac{1}{2}m_i\vec{v}’^2_i+\sum_i\frac{1}{2}m_i\vec{v}^2_{cm}+(\sum_im_i\vec{v}_i)\cdot\vec{v}_{cm}=E_k’+\frac{1}{2}m\vec{v}_{cm}^2$$
$\sum_im_i\vec{v}_i\quad\quad\to\quad\quad\vec{P’}=0$ 
$m\vec{v}_{cm}\quad\quad\to\quad\quad$ energia cinetica del CM
$E_k’\quad\quad\to\quad\quad$ energia cinetica rispetto al CM
L’energia cinetica del sistema di punti rispetto ad un sistema inerziale è uguale all’energia cinetica rispetto al CM più l’energia cinetica del CM.

# Teorema di König per il momento angolare
Il momento angolare di un sistema rispetto ad un sistema di riferimento inerziale:
$$\vec{L}=\sum_i\vec{r}_i\cdot m_i\vec{v}_i=\sum_i(\vec{r’}_i+\vec{r}_{cm})\cdot m_i(\vec{v}_i+\vec{v}_{cm})=$$
$$=\sum_i\vec{r’}_i\cdot m_i\vec{v’}_i+(\sum_im_i\vec{r’}_i)\cdot\vec{v}_{cm}+\vec{r}_{cm}\cdot(\sum_im_i\vec{v’}_i)+\vec{r}_{cm}\cdot(\sum_im_i)\vec{v}_{cm}$$

$$\vec{L}=\vec{L’}+\vec{r}_{cm}\cdot m\vec{v}_{cm}=\vec{L’}+\vec{L}_{cm}$$
Il momento angolare misurato in un sistema inerziale è uguale al momento angolare misurato nel sistema CM più momento angolare del CM rispetto al sistema inerziale

# Teorema dell’energia cinetica
Lavoro compiuto dalle forze su ciascun punto:$$dW_i=\vec{F}_i^{(I)}\cdot d\vec{s}_i+\vec{F}_i^{(E)}\cdot d\vec{s}_i=dW_i^{(I)}+dW_i{(E)}$$
$dW_i=\vec{F}_i\cdot d\vec{s}$
Sommando su ogni punto e integrando lungo le traiettorie:$$W=W^{(I)}+W^{(E)}$$
Sappiamo che $dW_i=mv_idv_i$ 
$$W=\sum_i\int_A^BdW_i=\sum_i\frac{1}{2}m_iv_{i,B}^2-\sum_i\frac{1}{2}m_iv^2_{i,A}=E_{k,B}-E_{k,A}$$
$$W=W^{(I)}+W^{(E)}=E_{k,B}-E_{k,A}=\Delta E_k$$
La variazione di energia cinetica è uguale al lavoro di tutte le forze.

# Conservazione dell’energia meccanica
$$W=W^{(I)}+W^{(E)}=E_{k,B}-E_{k,A}=\Delta E_k$$
La variazione dell’energia cinetica è uguale al lavoro di tutte le forze

Se le forze interne ed esterne sono conservative:
$\begin{align}W^{(I)=-\Delta E_P^{(I)}} \\ W^{(E)}=-\Delta E_P^{(E)}\end{align}$   Avremo $\to$  $W=-\Delta E_P^{(I)}-\Delta E_P^{(E)}=-\Delta E_P=\Delta E_k$

$(E_k+E_P)_B=(E_k+E_P)_A=\text{costante}$

Se non tutte le forze sono conservative $$(E_k+E_P)_B-(E_k+E_P)_A=W_{NC}$$
Se non ci sono forze esterne, non è detto che l’energia meccanica si conservi, dipende anche dalle forze interne.

# riepilogo
![[Riepilogo_sistemi.jpg]]


# Urti
**DEFINIZIONE**: collisione tra due o più corpi che interagiscono per un periodo di tempo molto breve, durante il quale si scatenano forze interne molto intense che modificano la quantità di moto di ciascun punto.
Queste forze si dicono interne al sistema se durante l’urto non agiscono forze esterne($\vec{P}=$ costante): $$\vec{P}_i=m_1\vec{v}_{1,i}+m_2\vec{v}_{2,i}=m_1\vec{v}_{1,f}+m_2\vec{v}_{2,f}=\vec{P}_f$$
La quantità di moto del centro di massa rimane invariata nell’urto $$\vec{P}=m\vec{v}_{CM}=\vec{P}_i=\vec{P}_f$$
Ma variano le quantità di moto dei singoli punti: $$\begin{align}\Delta\vec{p}_1=m_1\vec{v}_{1,f}-m_1\vec{v}_{1,i}=\vec{J}_{2,1}=\int_{t_i}^{t_f}\vec{F}_{2,1}dt \\ \Delta\vec{p}_2=m_2\vec{v}_{2,f}-m_2\vec{v}_{2,i}=\vec{J}_{1,2}=\int_{t_i}^{t_f}\vec{F}_{1,2}dt\end{align}$$

$\vec{F}_{1,2}=-\vec{F}_{2,1}\to\vec{J}_{1,2}=-\vec{J}_{2,1}\to\Delta\vec{p}_1=-\Delta\vec{p}_2\to\Delta\vec{P}=0$ 

## Urto tra due punti materiali
- Le forze interne non sono in generale conservative;
- L’energia meccanica, in generale, non si conserva;
- Se non agiscono forze esterne, la quantità di moto si conserva.

## Urto anelastico
Dopo un urto di questo genere i corpi restano attaccati formando un unico corpo puntiforme di massa $m=m_1+m_2$.![[Prima-dopo-urto.jpg]]

Questo è ciò che succede all’energia cinetica:
$$\begin{align}K_i=\frac{1}{2}m_1v^2_{1,i}+\frac{1}{2},m_1v^2_{2,i} \\ K_f=\frac{1}{2}m_2v^2_{1,F}+\frac{1}{2}m_2v^2_{2,F}\end{align}$$
$\frac{\Delta E_k}{K_i}\cdot100=…\%$     $\Delta E_k=K_i-K_f$ 


$$E_{k,i}=\frac{1}{2}m_1v^2_{1,i}+\frac{1}{2}m_2v^2_{2,i}=\frac{1}{2}mv^2_{CM}+E’_{k,i}$$
$E_{k,f}=\frac{1}{2}mv^2_{CM}$   $\Delta E_k=-E’_{k,i}$   Si è persa l’energia cinetica $E’_k$
Energia che viene utilizzata nella deformazione permanente dei due corpi.


## Urto elastico
Durante questo tipo di urto si conserva l’energia cinetica![[Urto_elastico.jpg]]

Caso unidimensionale:
**Conservazione quantità di moto**: $$m_1v_{1,i}+m_2v_{2,i}=m_1v_{1,f}+m_2v_{2,f}$$
**Conservazione dell’energia cinetica**:$$\frac{1}{2}m_1v^2_{1,i}+\frac{1}{2}m_2v^2_{2,i}=\frac{1}{2}m_1v^2_{1,f}+\frac{1}{2}m_2v^2_{2,f}$$
$$v_{1,f}=\frac{(m_1-m_2)v_{1,i}+2m_2v_{2,i}}{m_1+m_2} \qquad\qquad v_{2,f}=\frac{(m_2-m_1)v_{2,i}+2m_1v_{1,i}}{m_1+m_2}$$
Nel sistema di riferimento del CM: $\vec{v’}_{1,f}=-\vec{v’}_{1,i}$     $\vec{v’}_{2,f}=-\vec{v’}_{2,i}$

## Urto in 2 dimensioni
![[Urto_2_dimensioni.jpg]]

# note
![[Note_urti.jpg]]
