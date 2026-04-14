# Meccanica dei fluidi
Un corpo solido ha una forma propria. 
Un fluido assume la forma del recipiente che lo contiene.
Un fluido è un sistema continuo: $dm=\rho dV$  
Un elemento del fluido può scorrere: 
- rispetto ad un elemento adiacente
- Rispetto alla parete del recipiente

# Forze in un fluido
Viscosità: forza d’attrito interna.
Non c’è però equilibrio statico: il fluido non resiste allo scorrimento

In un fluido in quiete le forze tra gli elementi sono ortogonali alla superficie di separazione, altrimenti c’è scorrimento e non quiete.
Forze applicate ad un elemento di fluido:
1. Forze di volume: proporzionali a $dV$, esempio: $dF=gdm=g\rho dV$
2. Forze di superficie: proporzionali a $dS$:  $dF=pdS$   $p=\frac{dF}{dS}$  pressione


# Pressione 
La pressione è il rapporto tra la forza e la superficie su cui agisce la forza
In un fluido la pressione è una grandezza scalare il suo valore in un dato punto del fluido non dipende dall’orientazione di $dS$:  $p=\frac{dF}{dS}$.
La forza può essere applicata sulla superficie libera e/o dalle pareti del recipiente

L’unità di misura:  $[p]=\frac{[F]}{[S]}=\frac{N}{m^2}=$Pa (Pascal)


# Lavoro della forza di pressione
La superficie $dS$ a cui è applicata la forza $dF$ si sposta di $dh$

$dW=dFdh=pdSdh=pdV$
$W=\int pdV$
Il lavoro della forza provoca una variazione di volume
La variazione di volume di un solido o un liquido è trascurabile ma in un gas è importante(compressibilità)

# Equilibrio statico di un fluido
Su un elemento di fluido agiscono delle forze che si compensano in modo che essi sia in equilibrio.
Sull’asse z agiscono:

1) una forza di volume $dF^v_z=f_zdm=f_z\rho dV$  $f_z$: forza per unità di massa
2) Due forze di superficie dovute agli elementi di fluido che stanno sopra e sotto:$$dF^S_z=p(z)dS-p(z+dz)dS=-(p(z+dz)-p(z))dS=$$
$$=-\frac{\partial p}{\partial z}dzdS=-\frac{\partial p}{\partial z}dV$$

La condizione di equilibrio lungo l’asse z si scrive: $f_zdV-\frac{\partial p}{\partial z}dV=0$   $\quad\to\quad$   $\frac{\partial p}{\partial z}=f_z\rho$ 
Se una forza di volume tende a spostare l’elemento dm nel verso positivo z la pressione non può essere costante: essa cresce nel verso positivo z $$p(z+dz)>p(z) \quad\quad\quad dF^S_z \quad\text{equilibra}\quad dF^V_z$$
Stesso ragionamento può essere applicato agli altri assi: $$\frac{\partial p}{\partial x}=f_x\rho \quad\quad \frac{\partial p}{\partial y}=f_y\rho \quad\quad \frac{\partial p}{\partial z}=f_z\rho$$

Condizione di equilibrio statico:$$\vec{\nabla}p=\rho\vec{f}$$
Dove $f$ è una forza per unità di massa(accelerazione)


# Caso della forza peso
$$\vec{f}=\vec{g} \quad\quad\quad g_x=g_y=0 \quad\quad\quad g_z=-g$$
La pressione varia solo lungo z e aumenta nel verso di $\vec{g}$
$$\frac{\partial p}{dz}=-\rho g \quad\quad dp=-\rho gdz$$
$$\int^{p_2}_{p_1}dp=-\rho g\int^{z_2}_{z_1}dz \quad\quad\quad\text{se la densità è costante}$$

### Legge di Stevino
$p_2-p_1=-\rho g(z_2-z_1)=-\rho\Delta E_{p,m}=-\Delta E_{p,V}$

$E_{p_m}$: energia potenziale per unità di massa
$E_{p,V}$: energia potenziale per unità di volume

## Esempio: vasca d’acqua
![[Esempio_forza_peso.jpg]]
$p_1=p(h)$
$p_2=p_{atm}$

$z_2=0$
$z_1=-h$
$z_2-z_1=h$

$p_2-p_1=p_{atm}-p(-h)=-\rho g(z_2-z_1)=-\rho gh$
$p(-h)=p_{atm}+\rho gh=p_{atm}+9.8\cdot10^3h$

Ogni metro la pressione aumenta di $\Delta p=10^4Pa=0.1bar$
$$p(z)=p_0+\rho g(z_0-z)$$
Superfici equipotenziali: piani orizzontali sono anche superfici paranoiche $$mgz=costante\to z=costante$$
**Principio di Pascal**: una variazione di pressione esterna da luogo a una variazione uguale di pressione in tutto il fluido

# Manometro a U e barometro di Torricelli
## Manometro a U

![[Manometro_a_U.jpg]]
Pressione diverse sui due rami del tubo   $p_1>p_2$
$$p_1=p_2+\rho gh \quad\quad\quad h=\frac{p_1-p_2}{\rho g}$$
Dalla misura di h si può ottenere il valore relativo della pressione

## Barometro di Torricelli
![[Barometro_di_Torricelli.jpg]]
Prima misura della pressione atmosferica
Si riempie il tubo con mercurio senza fare entrare l’aria
Nel ramo chiuso agisce solo la pressione dei vapori di mercurio che hanno bassissima densità, la colonna di mercurio misura la pressione atmosferica

$p_1=p_{atm}$
$p_2\approx0$
$p_1-p_2=p_{atm}=\rho gh$
$h=0,76m$


# Principio di Archimede
![[Principio_di_archimede.jpg]]

Fluido in equilibrio. In un volume V qualsiasi del fluido, la risultante delle forze di pressione equilibrano il suo peso
$$\vec{F}_V+\vec{F}_p=m\vec{g}+\vec{F}_p=0 \quad\to\quad \vec{F}_p=-m\vec{g}$$
$m=\rho V$

Sostituendo alla massa $m$, una massa $m’$ di uguale volume $V$   $m’=\rho’V$ 
$\vec{F}_p$ non varia
$m’\vec{g}+\vec{F}_p=m’\vec{g}-m\vec{g}=g(m’-m)=(\rho’-\rho)V\vec{g}$

Un corpo immerso in un fluido riceve una spinta verso l’alto pari al peso del volume di fluido spostato

$\rho’>\rho$ risultante$\downarrow$ $\quad\quad$  $\rho’<\rho$ risultante $\uparrow$  $\quad\quad$  $\rho’=\rho$  risultante nulla

# Moto di un fluido
Trattando fluidi ideali: incompressibili e non viscosi flussi laminari in regime stazionario

Linee di corrente: tangente al vettore velocità
![[Vettore_velocità.jpg]]

![[Tubo_di_flusso2.jpg]]

Portata del tubo di flusso: volume di fluido che attraversa l’area da a velocità v in un secondo
$dq=vdS$

In regime stazione e a densità costante, la portata è la stessa attraversa qualsiasi sezione del tubo(anche se cambia il diametro del tubo)
$q=\int dq=\int vdS=v_mS$

In regime stazionario e a densità costante, dove il tubo si restringe la velocità aumenta e viceversa.(Legge di Leonardo: $v_mS=$costante).

# Teorema di Bernoulli(1738)

![[Teorema_bernoulli.jpg]]

Il valore di fluido che attraversa $S_1$ nell’unità di tempo è uguale a quello che attraversa $S_2$(incompressibilità)

Volendo ricavare la relazione tra la velocità e la pressione del fluido nelle diverse sezioni del condotto
Le forze agenti sul volume sV sono il peso e le forze di pressione.

Il lavoro della forza peso è: $dW=-dE_p=-dmg(z_2-z_1)=-\rho dVg(z_2-z_1)$
Le forze di pressione delle pareti del condotto non fanno lavoro(ortogonali allo spostamento)

Le forze di pressione $F_1$ e $F_2$ fanno lavoro:$$dW_p=\vec{F_1}\cdot \vec{ds_1}+\vec{F_2}\cdot\vec{ds_2}=p_1S_1ds_1-p_2S_2ds_2=p_1dV_1-p_2dV_2=(p_1-p_2)dV$$
La variazione dell’energia cinetica è:$$dE_k=\frac{1}{2}dmv^2_2-\frac{1}{2}dmv^2_1=\frac{1}{2}\rho dV(v^2_2-v^2_1)$$
$$dW+dW_p=-\rho dVg(z_2-z_1)+(p_1-p_2)dV$$
$$=dE_k=\frac{1}{2}\rho dV(v^2_2v^2_1)$$

$$p_1+\frac{1}{2}\rho v^2_1+\rho gz_1=p_2+\frac{1}{2}\rho v^2_2+\rho gz_2$$
**Teorema di Bernoulli**:
$$p+\frac{1}{2}\rho v^2+\rho gz=costante$$

![[Teorema_di_bernoulli2.jpg]]

Se $v=0$, si ritrova la legge di Stevino   $p_2-p_1=-\rho g(z_2-z_1)$
Se il tubo è orizzontale $p+\frac{1}{2}\rho v^2=$costante

## Applicazioni
**Tubo a sezione costante**
La velocità costante   $p_1+\rho gh_1=p_2+\rho gh_2$
La pressione è massima nel punto più basso
![[IMG_0108.jpg]]

Se vogliamo far salire un fluido di una altezza $h$ con una certa portata $q=Sv_1$, la pompa deve assicurare la differenza di pressione $\Delta p=p\rho h$
$F=\rho ghS$  $\to$  la potenza della pompa deve essere  $P=Fv=\rho ghSv=\rho ghq$ 