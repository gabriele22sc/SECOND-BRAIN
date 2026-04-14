# Leggi di conservazione
In fisica, il concetto fondamentale per studiare il nostro universo è l’interazione(elettromagnetica,gravitatoria…). La massa e la forza sono grandezze fisiche che ci permettono di poter rappresentare i sistemi interagenti.
Esistono limitazioni al movimento di masse interagenti, indipendenti dal tipo d’interazione, le relazioni che rappresentano queste limitazioni si chiamano **leggi di conservazione**.
Per ognuna di queste leggi viene definita una grandezza fisica che rimane costante e che viene determinata dalle condizioni iniziali. Queste costanti di movimento servono a predire l’evoluzione di un punto materiale o sistema di punti che interagiscono tra di loro.

# Lavoro
Punto che si sposta da A a B:
![[Spostamento_a-b.jpg]]

Lavoro della forza nello spostamento AB = integrale di linea della forza$$W=\int_A^B\vec{F}\cdot d\vec{s}=\int_A^BFcos\theta ds=\int_A^BF_T ds$$
Il lavoro differenziale corrispondente a uno spostamento $ds$ è: $dW=\vec{F}\cdot ds$

Il lavoro è una grandezza scalare. Se agiscono più forze, il lavoro è la somma dei singoli lavori oppure, il lavoro della forza risultante$$W=\int_A^B\vec{R}\cdot d\vec{s}=\int_A^B\sum_i(\vec{F}_i\cdot d\vec{s})=\sum_i\int_A^B\vec{F}_i\cdot d\vec{s}=\sum_iW_i$$
$W>0$, $0\leq\theta<\frac{\pi}{2}$
$W>0$, $\frac{\pi}{2}<\theta<\pi$
$W=0$, $\theta=\frac{\pi}{2}$

Unità di misura: $[W]=$Joule$=Nm=kg\frac{m^2}{s^2}$

# Potenza
Lavoro nell’unità di tempo:$$P=\frac{dW}{dt}=\vec{F}\cdot\frac{d\vec{s}}{dt}=\vec{F}\cdot\vec{v}=F_Tv$$
Caratterizza la rapidità di produzione o assorbimento di lavoro
Unità di misura:  $[P]=$watt$=W=\frac{J}{s}$
Potenza media nell’intervallo $\Delta t$: $P_m=\frac{W}{\Delta t}$


# Energia cinetica
**Lavoro infinitesimo**: $$dW=\vec{F}\cdot d\vec{s}=Fdscos\theta=F_Tds=ma_Tds=m\frac{dv}{dt}ds=m\frac{ds}{dt}dv=mvdv$$
**Lavoro finito**:$$W=\int dW=\int_{v_1}^{v_2}mvdv=\frac{1}{2}mv^2_2-\frac{1}{2}mv^2_1=\Delta E_k$$
**Energia cinetica**:
$E_k=\frac{1}{2}mv^2$
$E_u=mgh$  o  $E_u=\frac{1}{2}kx^2$

il lavoro è uguale alla variazione di energia cinetica  $W=\Delta E_k$

L’energia cinetica è una forma di energia legata al movimento. Sono rilevanti le sue variazioni.
Il lavoro motore($W>0$) $\to$ aumenta l’energia cinetica,
Il lavoro resistente($W<0$) $\to$ diminuisce l’energia cinetica
Lavoro nullo($W=0$) $\to$ l’energia cinetica rimane costante

Il lavoro è nullo($\Delta E_k=0$) quando:
1. Non ci sono forze
2. Ci sono forze ma la risultante è nulla
3. Ci sono forze ma la risultante è ortogonale alla traiettoria(moto circolare uniforme


# Lavoro della forza peso
$$dW=m\vec{g}\cdot d\vec{s}=(-mg\vec{u}_z)\cdot d\vec{s}=-mgds_z=-mgdz$$
$$W=-\int_A^Bmgdz=-(mgz_B-mgz_A)=-\Delta E_P$$
![[Lavoro_forza_peso.jpg]]

Energia potenziale: $E_p=mgz$

**N.B.**: Il lavoro della forza peso è uguale all’opposto della variazione dell’energia potenziale della forza peso.

Se $z_A>z_B$, lavoro motore($W>0$) $\to$ **diminuisce** l’energia potenziale;
Se $z_A<z_B$, lavoro resistente($W<0$) $\to$ **aumenta** l’energia potenziale;
Se $z_A=z_B$, lavoro nullo($W=0$) $\to$ l’energia potenziale rimane **costante**.


# Lavoro della forza elastica
$$W=\int_A^B-kx\vec{u}_x\cdot d\vec{x}=-k\int_A^Bxdx=-(\frac{1}{2}kx^2_B-\frac{1}{2}kx^2_A)=\Delta E_p$$

![[start/fisica/argomenti/Meccanica/argomenti/Dinamica/Dinamica2/Forza_elastica.jpg]]
$$\vec{F}=-kx\vec{u}_x$$
$$E_p=\frac{1}{2}kx^2$$
Il lavoro della forza elastica è uguale all’opposto della variazione della funzione $E_p$ delle coordinate, detta energia potenziale della forza elastica.

Quando il punto si avvicina al centro $\Delta E_p<0$ e $W>0$: spostamento naturale
Quando il punto si allontana dal centro $\Delta E_p>0$ e $W<0$: bisogna tirare la molla


# Lavoro della forza di attrito radente
$$W=\int_A^B-\mu_dN\vec{u}_v\cdot d\vec{s}=-\mu_dN\int_A^Bds=-\mu_dNs_{AB}$$
$s_{AB}$ è la lunghezza della traiettoria AB

Nel caso della forza peso e della forza elastica $W=-\Delta E_p=E_p(A)-E_p(B)$
- Il lavoro dipende solo dalle coordinate dello stato iniziale e dello stato finale: **non dipende dalla traiettoria**;
- Invece, nel caso dell’attrito, il lavoro dipende dal percorso, cioé dalla sua lunghezza: **non esiste una $E_p$ per l’attrito**.

$W=\Delta E_k$ vale sempre
$W=\Delta E_p$ vale solo per alcune forze


# Forze conservative
Sì chiamano così le forze il cui lavoro non dipende dal percorso
$$W=\int_A^B\vec{F}\cdot d\vec{s}=-\Delta E_p$$
Ha lo stesso valore qualunque sia la sua traiettoria AB. Per esempio: forza peso, forza elastica, forza gravitazionale, forze centrali, forza elettrostatica

$\int_{A,C_1}^B\vec{F}\cdot d\vec{s}=\int_{A,C_1}^B\vec{F}\cdot d\vec{s}$   indipendenza dal percorso

$\int_{A,C_1}^B\vec{F}\cdot d\vec{s}=-\int_{A,C_1}^B\vec{F}\cdot d\vec{s}$   proprietà degli integrali

$\int_{A,C_1}^B\vec{F}\cdot d\vec{s}+\int_{B,C_2}^A\vec{F}\cdot d\vec{s}=\int_{A,C_1}^B\vec{F}\cdot d\vec{s}-\int_{A,C_2}^B\vec{F}\cdot d\vec{s}=0$
$\int\vec{F}\cdot d\vec{s}=0$
Equivalente all’indipendenza dal percorso


# Conservazione dell’energia meccanica
L’energia meccanica si conserva quando agiscono solo **FORZE CONSERVATIVE**
$W=\Delta E_k=-\Delta E_p$
$E_{K,B}-E_{K,A}=E_{P,A}-E_{P,B}$ 
$E_{M,A}=E_{K,A}+E_{P,A}=E_{K,B}+E_{P,B}=E_{M,B}$
La somma dell’**energia cinetica** e dell’**energia potenziale** resta costante durante il moto.
L’energia meccanica si conserva
Ciascuna forma di energia cambia, però la somma resta costante, Se una diminuisce, l’altra aumenta e viceversa

# Forze non conservative
Sono forze il cui lavoro dipende dalla traiettoria $$\int\vec{F}\cdot d\vec{s}\neq0$$
Se il lavoro è sempre negativo, si parla di forze dissipative(attrito)$$\Delta E_k=W=W_{NC}+W_c=W_{NC}-\Delta E_p$$
$W_{NC}=\Delta E_k+\Delta E_p=\Delta E_m$
Il lavoro delle forze non conservative è uguale alla variazione dell’energia meccanica
In presenza di forze dissipative, l’energia meccanica diminuisce

# Momento di una forza
Momento di una forza: $\vec{M}_O=\vec{r}\cdot\vec{F}$ ![[Momento_di_una_forza.jpg]]

In modulo: $M=rFsen\theta$
Se il polo passa da $O$ a $O’$:  $\vec{M}_{O’}=\vec{r}\cdot\vec{F}=(\vec{O’O}+\vec{r})\cdot\vec{F}=\vec{M}_O+\vec{O’O}\cdot\vec{F}$

Se al punto sono applicate più forze: $$\vec{M}=\vec{r}\cdot\vec{F}_1+\vec{r}\cdot\vec{F}_2+…+\vec{r}\cdot\vec{F}_n=\vec{r}\cdot(\vec{F}_1+\vec{F}_2+…+\vec{F}_n)=\vec{r}\cdot\vec{R}$$

Unità di misura: $[M]=[r]\cdot[F]=Nm=kg \frac{m^2}{s^2}$

# Momento angolare
Momento angolare $\vec{L}=\vec{r}\cdot\vec{p}=\vec{r}\cdot m\vec{v}$
Il momento angolare è sempre perpendicolare al raggio vettore e alla velocità.

Nel moto curvilineo piano: $\vec{v}=\vec{v}_r+\vec{v}_{\theta}$
$\vec{L}=\vec{r}\cdot m(\vec{v}_r+\vec{v}_{\theta})=\vec{r}\cdot m\vec{v}_{\theta}$

In modulo: $L=mr^2\frac{d\theta}{dt}=mr^2\omega$
Unità di misura: $[L]=[r]\cdot[p]=kg\frac{m^2}{s}$

# Teorema del momento angolare
Polo fisso O, massa costante $$\frac{d\vec{L}}{dt}=\frac{d\vec{r}}{dt}\cdot m\vec{v}+\vec{r}\cdot m\frac{d\vec{v}}{dt}=\vec{v}\cdot m\vec{v}+\vec{r}\cdot m\vec{a}=0+\vec{r}\cdot\vec{F}=\vec{M}$$
Il momento della forza è uguale alla derivata rispetto al tempo del momento angolare $\frac{d\vec{L}}{dt}=\vec{M}$

Il momento angolare si conserva $\frac{dL}{dt}=0$ quando il momento delle forze esterne è nullo:$$\vec{L}=cost \quad\to\quad \vec{M}=0 \quad\to\quad \vec{F}=0,\vec{r}||\vec{F}$$
Conservazione della quantità di moto: $$\frac{d\vec{p}}{dt}=\vec{F} \quad\to\quad \vec{p}=\text{cost} \quad\to\quad \vec{F}=0$$
