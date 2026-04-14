# Dinamica del coro rigido
**Corpo rigido**: sistema di punti materiali in cui le distanze tra tutte le copie di punti non possono variare: indeformabile, la posizione del CM non cambia.
La solidità viene garantita dalla forza elettrica tra gli atomi e le molecole. Un corpo rigido può fare un moto di **traslazione**, **rotazione** o **rototraslazione**.

Sì possono individuare 3 tipi di sistemi di riferimento:
1. Sistema con origine in un punto esterno a corpo;
2. Sistema con origine nel CM del corpo (vede la rotazione dei punti);
3. Sistema con gli assi solidali al corpo (vede i punti fissi).
![[Dinamica-corpo-rigido.jpg]]
# Moto di traslazione
Tutti i punti descrivono traiettorie uguali, in genere curvilinee, con la stessa velocità istantanea $\vec{v}=\vec{v}_{CM}$ se è noto il moto del CM, è noto il moto di qalsiasi punto del corpo
![[Moto-traslazion.jpg]]
Alcune espressioni:
$\vec{P}=m\vec{v}_{cm}$    $\vec{R}=m\vec{a}_{cm}$   
$E_k=\frac{1}{2}mv^2_{cm}$    $\vec{L}=\vec{r}_{cm}\cdot m\vec{v}_{cm}$  non c‘è moto rispetto al CM

# Moto di rotazione
Tutti i punti del corpo descrivono un moto circolare.
**Traiettorie**: archi di circonferenze diverse che stanno su piani paralleli e hanno il centro su uno stesso asse(asse di rotazione).![[Moto-circolare.jpg]]

La velocità angolare è la stessa per tutti i punti e parallela all’asse di rotazione
$v_i=\omega r_i$ la velocità tangenziale varia a seconda della distanza all’asse di rotazione
In generale il CM non sta sull’asse di rotazione.

L’equazione dinamica di base del moto rotazionale è: $\vec{M}=\frac{d\vec{L}}{dt}$  (**legge cardinale della dinamica**)[[LEGGE CARDINALE DELLA DINAMICA]] 

Valgono le stesse espressioni del moto di traslazione in più:
$E_k=\frac{1}{2}mv^2_{cm}+E’_k$
$\vec{L}=\vec{r}_cm\cdot m\vec{v}_{cm}+\vec{L’}$
Nella rotazione c’è movimento rispetto al CM, dato che la distanza tra un punto e il CM non varia, il moto relativo è rotatorio, con la stessa $\omega$. L’asse di rotazione può essere fisso nel tempo o variare.

# Moto di rototraslazione
Lo spostamento infinitesimo nel tempo $dt$ è la somma di una traslazione e di una rotazione infinitesime.
In generale la velocità lineare e quella angolare sono variabili nel tempo.
Per descrivere il moto occorrono 6 parametri:
- 3 per il moto del CM(traslazione): interessa le coordinate del CM;
- 3 per il moto rotatorio:interesse l componenti della velocità angolare($\omega$).

# Gradi di libertà
Indicano il numero minimo di coordinate indipendenti necessarie per descrivere univocamente la posizione e l’orientamento di un sistema fisico. Un punto materiale ha 3 gradi di libertà: le tre coordinate $x,y,z$.
Un corpo rigido(composto da infiniti punti materiali) non ha infiniti gradi di libertà ma soltanto 6 gradi di libertà(i vincoli riducono i gradi di libertà):
- le 3 coordinate della posizione del CM, rappresenta il moto di traslazione: $x_{cm},y_{cm},z_{cm}$;
- le 3 componenti per dare l’orientamento del corpo(rotazione).
La composizione dei due movimenti è la **rotatraslazione**.

# Descrizione non univoca
Siano $P$ e $Q$ due punti di un corpo rigido![[Descrizione-non-univoca.jpg]]

Scegliamo un punto generico $O$ del corpo. 
$\vec{v}_P=\vec{v}_O+\omega\cdot\overrightarrow{OP}$
$\vec{v}_Q=\vec{v}_O+\vec{\omega}\cdot\overrightarrow{OQ}$
$\vec{v}_0$: velocità di traslazione del punto $O$
L’asse di rotazione istantaneo passa per $O$

$\vec{v}_P-\vec{v}_Q=\vec{\omega}\cdot(\overrightarrow{OP}-\overrightarrow{OQ})=\vec{\omega}\cdot\overrightarrow{QP}$ 
$\vec{v}_P=\vec{v}_Q+\vec{\omega}\cdot\overrightarrow{QP}$
Il moto di $P$ è sempre rototraslatorio,
$\vec{\omega}$ non cambia
$\vec{v}$ cambia: dipende dall’asse di rotazione he scegliamo

# note
![[note-corpo-rigido.jpg]]

# Densità di un corpo rigido
Pensiamo il corpo come composto da “punti” di volumi infinitesimi $dV$ e massa $dm$
Definiamo la densità(distribuzione della massa nel volume del corpo): $[\rho=\frac{kg}{m^3}]$ 

$$\begin{align}\rho=\frac{dm}{dV} \\\\ m=\int dm=\int_V\rho dV\end{align}$$
Se la densità è costante:$$\begin{align}\rho=\frac{m}{V} \\\\ m=\rho V\end{align}$$
Se la massa è distribuita su una superficie: $\rho=\frac{dm}{dS} \quad\quad [\rho]=\frac{kg}{m^2}$

Se la massa è distribuita su una linea: $\rho=\frac{dm}{dl} \quad\quad [\rho]=\frac{kg}{m}$ 

# Calcolo della posizione del CM

![[Calcolo-pos-cm.jpg]]

Di sostituiscono integrali alle sommatorie: $$\vec{r}_{CM}=\frac{\int\vec{r}dm}{m}=\frac{\int\vec{r}\rho dV}{m}$$
Nei corpi simmetrici il CM sta nel centro o sull’asse o nel piano di simmetria

# Forza peso
La risultante va applicata nel CM: $\vec{R}=\int\vec{g}dm=\vec{g}\int dm=m\vec{g}$

Il momento della forza peso rispetto ad un polo O: $$\vec{M}=\int\vec{r}\cdot\vec{g}dm=(\int\vec{r}dm)\cdot\vec{g}=m\vec{r}_{cm}\cdot\vec{g}=\vec{r}_{cm}\cdot m\vec{g}=\vec{r}\cdot\vec{R}$$
L’energia potenziale gravitazionale $$E_p=\int scambio=g\int zdm=mgz_{cm}$$
Il lavoro della forza peso$$W_{peso}=-\Delta E_p=(mgz_{cm})_A-(mgz_{cm})_B$$
# Rotazione rispetto ad un asse fisso
L’asse può essere interno o esterno al corpo. In generale, il CM non è sull’asse di rotazione.
La velocità angolare $\omega$ ha direzione fissa, ma può cambiare verso e modulo: $$\vec{a}=\frac{d\omega}{dt},\vec{a}//\vec{\omega}$$
Per ciascun punto i valgono queste espressioni: la traiettoria è circolare e su un piano
$v_i=\omega R_i\quad\quad$   $\vec{a}_i=\vec{a}_{i,t}+\vec{a}_{i,c}\quad\quad$   $a_{i,t}=\alpha R_i\quad\quad$ $a_{i,c}=\omega^2R_i=v^2_i/R_i$
Il polo dei contenti conviene sceglierlo sull’asse: punto fisso in un sistema inerziale

# Calcolo del momento angolare
$z$: asse di rotazione $\vec{v}_i\perp\vec{r}_i$
$\vec{L}_i\perp$ piano che formano $\vec{v}_i,\vec{r}_i$
$$R_i=r_isen\theta_i$$
Il momento angolare di ogni punto risulta: $$\begin{align}\vec{L}_i=\vec{r}_i\cdot m_i\vec{v}_i \\\\ L_i=r_im_iv_i=m_ir_iR_i\omega\end{align}$$
La componente assiale $L_{i,z}=L_icos(\frac{\pi}{2}-\theta_i)=L_isen\theta_i$ $$L_{i,z}=m_ir_isen\theta_iR_i\omega=m_iR_i^2\omega$$
Non dipende dal polo O
La componente trasversa(ortogonale a $z$) risulta $$L_{i,\perp}=L_icos\theta_i=m_ir_iR_i\omega cos\theta_i$$
Si dipende dal polo O.
![[Calcolo_momento_angolare.jpg]]

# Momento angolare totale e momento d’inerzia
$\vec{L}=\sum_i\vec{L}_i$ 

La componente assiale (somma di $n$ termini paralleli):$$L_Z=\sum_iL_{i,z}=(\sum_im_iR_i^2)\omega=I_z\omega$$
Dove $I_z$ è il momento di inerzia $$I_z=\sum_im_iR^2_i$$
La componente trasversa dipende da O (somma di n termini vettoriali non paralleli)
Il momento angolare ruota intorno all’asse, assieme al corpo diciamo che L fa una precessione. Possiamo vedere L come se fosse l’asse di una trottola
![[Mom_iner_mom_tot.jpg]]
 **N.B.**: $L_z$ non dipende dal polo. La componente ortogonale $L_{\perp}$ dipende da O
# Conseguenze del disallineamento di $L$ e $\omega$
Compaiono sollecitazioni sull’asse
![[Disallineamento1.jpg]]
È necessario mantenere l’asse fisso
$L_z=2mm(rsen\theta)^2\omega$   Costante
$L_{\perp}=2mrR\omega cos\theta$   Variabile in direzione

***
 $L$ precede uniformemente e la sua variazione è legata al momento delle forze esterne (perpendicolare all’asta e alle forze).
![[disallineamento2.jpg]]
Se $\omega$ è costante $$\vec{M}=\frac{d\vec{L}}{dt}=\vec{\omega}\cdot\vec{L}\to M=\omega L_{\perp}$$
$$M=L_{\perp}\omega=2mrR\omega^2cos\theta$$
Le forze centripete tendono a ribaltare l’asse, i supporti esterni devono esercitare sull’asse un momento uguale e contrario proporzionale a $\omega^2$

# Assi principali di inerzia
(**Teorema di Poinsot**) Si dimostra che, preso un punto qualsiasi di un corpo per quel punto passano 3 assi ortogonali tra loro (assi principali di inerzia) tali che, se presi come assi di rotazione, per cuscini si ha L parallelo a $\omega$.
Se il punto è il CM, gli assi si chiamano **ASSI CENTRALI DI INERZIA**
Il momento angolare risulta parallelo a $\omega$ quando l’asse di rotazione è un asse di simmetria del corpo o, più in generale, un asse principale d’inerzia.
In tali condizioni vale:

$\vec{L}=I_z\vec{\omega}$

$L=L_z$

$L_{\perp}=0$

# Equazione del moto di rotazione
**caso 1:** 
Asse di rotazione=Asse principale di inerzia

$\vec{M}=\frac{d\vec{L}}{dt}=\frac{d(I_z\vec{\omega})}{dt}=I_z\frac{d\vec{\omega}}{dt}=I_z\vec{\alpha}$   **Equazione del moto di rotazione**

L’azione di un momento esterno, determina l’accelerazione angolare del corpo rigido

$\alpha=\frac{M}{I_Z}$   $\to$   $\omega=\omega_0+\int\alpha dt$   $\to$   $\theta=\theta_0+\int\omega dt$

Viceversa, se è noto il moto, si determina il momento M

**Moto circolare uniforme**  $M=0$
**Moto circolare uniformemente accelerato**   $\vec{M}=$ costante


# Energia cinetica e lavoro
L’energia cinetica del corpo rigido nel moto di rotazione è data da $$E_k=\sum_i\frac{1}{2}m_iv^2_i=(\sum_im_iR_i^2)\frac{1}{2}\omega^2$$
$E_k=\frac{1}{2}I_z\omega^2$
Se il corpo varia la sua velocità di rotazione viene compiuto un lavoro a seguito dell’applicazione di un momento esterno
$W=\Delta E_k=0\frac{1}{2}I_z\omega^2_B-\frac{1}{2}I_z\omega^2_A$
La relazione tra $W$ e $M$ si ricava da:
$dW=dE_k=I_z\omega d\omega=I_z\frac{d\theta}{dt}\alpha dt$  $\quad\quad$ $dW=I_z\alpha d\theta=M_zd\theta$

Integrando $W=\int_0^\theta M_z d\theta$

La potenza istantanea è data da:$$P=\frac{dW}{dt}=M_z\frac{d\theta}{dt}=M_z\omega$$
## Esempio
Corpo di massa $m$ sospeso a un filo di massa trascurabile, avvolto intorno ad una ruota di momento d’inerzia $I$ e raggio $R$. Il supporto della ruota è privo di attrito e il filo non striscia sul bordo della ruota. Trovare la tensione del filo e l’accelerazione del corpo.![[Esempio-energia-cinetica.jpg]]


L’unica forza che esercita momento è la tensione   $RT=I\alpha$
Sul corpo agiscono la tensione e il peso   $mg-T=ma$

2 equazioni e 3 incognite…    il filo fornisce un vincolo che permette di avere una terza equazione: l’accelerazione di un punto del filo è la stessa di quella del corpo $a=R\alpha$ 
$$T=\frac{I}{I+mR^2}mg \quad\quad\quad a=\frac{mR^2}{I+mR^2}g$$



# Momento d’inerzia

Insieme di punti materiali   $I_z=\sum_im_iR^2_i=\sum_im_i(x^2+y^2)$

Corpo continuo  $I_z=\int R^2dm=\int R^2\rho dV=\int\rho(x^2+y^2)dV$ 

Dipende dalla distanza delle masse dall’asse di rotazione
Dipende dalla forma del corpo e dalla posizione dell’asse rispetto al corpo

![[Momenti_dinerzia.jpg]]

![[Momento-d‘inerzia2.jpg]]

# Momento d’inerzia e momento angolare
$$L=I\omega$$
Se il momento angolare si conserva ad una diminuzione del momento di inerzia corrisponde un aumento della velocità angolare.
![[Mom-inerzia-mom-angolare.jpg]]

# Conservazione del momento angolare

![[Conservazione-momento-angolare.jpg]]


# Teorema di Huygens-Steiner

![[Teorema-huygens-steiner.jpg]]

$P$: punto generico del corpo
$x_i=x’_i$
$y_i=y’_i+a$   $$I_z=\sum_im_i(x^2_i+y^2_i)=\sum_im_i(x’^2_i+(y’_i+a)^2)=$$ $$=\sum_im_i(x’^2_i+y’^2_i)+(\sum_im_i)a^2+2a\sum_im_iy’_i=\quad I_{z’}+ma^2+2amy’_{cm}$$
**Teorema di Huygens-Steiner**: $I_z=I_{z’}+ma^2$ 
Noto il momento d’inerzia rispetto ad un asse passante per il CM, è noto anche il momento d’inerzia rispetto ad un qualsiasi asse parallelo al precedente e distante $a$ da questo.

# Moto del corpo rigido
L’asse di rotazione non è un asse fisso, è un asse geometrico che si sposta col corpo. Esistono 3 casistiche:
1. Il corpo striscia:![[1casistica-moto.jpg]]
Tutti i punti hanno la stessa velocità parallela al piano (**moto di traslazione**).
2. Il corpo rotola e striscia:![[2casistica_moto.jpg]]
Il punto di contatto ha velocità non nulla, striscia e il corpo rotola (**moto di roto-traslazione**)
3. Moto di **puro rotolamento**:![[3casistica-moto.jpg]]
Il punto di contatto ha velocità nulla il corpo rotola senza strisciare.

# Moto di puro rotolamento
Schematizzazione del moto:
- nell’intervallo $dt$ il punto $C$ di contatto è fermo rispetto al piano $v_c=0$,
- Il corpo ruota rispetto ad un asse passante per $C$, ortogonale al disegno, con velocità angolare $\omega$,
- Nell’istante successivo c’è un diverso punto di contatto e si ripete quanto detto,
- È necessaria una forza d’attrito per tenere fermo il punto $C$, allora l’attrito è statico,
- La successione di rotazione equivale a una roto-traslazione: traslazione($v_{cm}$), rotazione rispetto al CM($\omega$).
$v_{cm}$ e $\omega$ non sono indipendenti
$$\vec{v_C}=\vec{v_{cm}}-\vec{r}\cdot\vec{\omega}$$
$$v_C=v_{cm}-\omega r=0 \quad\to\quad v_{cm}=\omega r$$
$a_{cm}=\alpha r$
![[Moto-puro-rotolamento.jpg]]


## 1° caso: agisce una forza $F$

![[Primo_caso_mpr.jpg]]

Il corpo è spinto da una forza $F$ applicata nel CM

**Moto del CM**: $F-f=ma_{cm}$     $N=mg$
**Moto di rotazione**: il polo coincide col CM, solo $f$ ha momento non nullo.
$$rf=I\alpha=I\frac{a_{cm}}{r}$$
$$a_{cm}=\frac{F}{m(1+\frac{I}{mr^2})} \quad\quad\quad f=\frac{F}{1+\frac{mr^2}{I}}$$
Il momento di inerzia $I$ è calcolato rispetto all’asse passante per CM parallelo all’asse passante per C.
La soluzione dipende da $F$ e dal tipo di corpo.

$f\le\mu_sN=\mu_smg$  $\quad\quad$ $F\le\mu_smg(1+\frac{mr^2}{I})=F_{lim}$ perché sia un puro rotolamento
Se $F>F_{lim}$ il corpo rotola e striscia

## 2° caso: agisce un momento torcente
![[secondo_caso_mpr.jpg]]
Sull’asse agisce il momento torcente $M$. L’azione del momento spinge $C$ verso sinistra allora $f$ è opposta rispetto al caso precedente($f$ spinge il corpo).

**Moto del CM**: $f=ma_{cm}$   $N=mg$ 

**Moto di rotazione**: il polo coincide col CM, solo $f$ ha momento non nullo   $M-rf=I\frac{a_{cm}}{r}$

$$a_{cm}=\frac{M}{mr(1+\frac{I}{mr^2})} \quad\quad\quad f=\frac{M}{r(1+\frac{mr^2}{I})}$$
$$f\le\mu_smg\quad\to\quad M\le\mu_smgr(1+\frac{I}{mr^2})=M_{lim}$$

## 3° caso: agiscono $F$ e $M$
![[Terzo_caso_mpr.jpg]]
Sull’asse agisce il momento $M$. L’azione del momento spinge $C$ verso sinistra. Si somma l’azione della forza $F$, allora non possiamo sapere a priori il verso di $f$.

**Moto del CM**: $F+f=ma_{cm}$    $N=mg$
**Moto di rotazione**: il polo coincide col CM, solo $f$ ha momento non nullo     $M-rf=I\frac{a_{cm}}{r}$ 
$$a_{cm}=\frac{1}{m}\frac{F+\frac{M}{r}}{1+\frac{I}{mr^2}}$$
$$f=\frac{\frac{M}{r}-\frac{I}{mr^2}F}{r(1+\frac{mr^2}{I})}$$
$f\le\mu_smg$ 
Se $M=\frac{IF}{mr}\to f=0, \quad a_{cm}=\frac{F}{m}$  **Moto accelerato senza attrito**


# Leggi di conservazione (Puro Rotolamento)
**Energia**: La forza di attrito non compie lavoro perché il punto $C$ è sempre fermo $\to$ se le altre forze agenti sono conservative $\to$ si conserva l’energia

**Attrito volvente**: dovuto alla deformazione del piano c’è una azione frenante. L’effetto è molto piccolo è molto piccolo e lo trascureremo.

**Quantità di moto**: Se la risultante delle forze esterne è nulla:$$\vec{R}=0 \quad\quad \vec{a_{cm}}=0\quad\quad\vec{v_{cm}}=costante$$
Il moto del CM è rettilineo e uniforme (non quello dei singoli punti)

**Momento angolare**: Se il momento risultato esterno è nullo: $\vec{M}=0\quad\quad\to\vec{L}=costante$ L’asse di rotazione coincide con l’asse principale d’inerzia


## Esempio 
![[Esempio_leggi_conservazione.jpg]]
Corpo che rotola senza strisciare. Calcolare la velocità finale se parte da fermo.
**Moto di puro rotolamento**: si conserva l’energia meccanica

$\Delta E_k=-\Delta E_p\quad\quad\to E_{k,f}=E_{p,i}$
Utilizzando il Teorema di König $\to \frac{1}{2}mv^2_{cm}+\frac{1}{2}I\omega^2=mgh$ 
$$v_{cm}=\sqrt{\frac{2gh}{1+\frac{I}{mr^2}}}<\sqrt{2gh}$$
Tanto minore quanto maggiore è $\frac{I}{mr^2}$
Energia potenziale:
- Energia cinetica di traslazione,
- Energia cinetica di rotazione.


# Statica del corpo rigido
Un corpo rigido, inizialmente in quiete, resta in quiete se: $\begin{cases}\vec{R}=0 \\ \vec{M}=0\end{cases}$
$M$ non dipende dal polo perché $R=0$
- $\vec{R}=0$  Equilibrio statico del CM: non c’è traslazione
- $\vec{M}=0$ Equilibrio rotazionale: non c’è rotazione

_**N.B.**_: conviene scegliere come polo un punto rispetto al quale le forze sconosciute hanno momento nullo.

