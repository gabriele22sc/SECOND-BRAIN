# Lavoro della forza elettrica 
## Tensione
Il lavoro di una forza $F$ per uno spostamento elementare $ds$ della carica $q_0$ è dato da:$$dW=\vec{F}\cdot d\vec{s}=q_0\vec{E}\cdot d\vec{s}=q_0E\cos(\theta)ds$$
![[Pasted image 20260309145932.png]]

Il lavoro nello spostamento da A a B lungo la curva C è:$$W=\int_CdW=\int_C\vec{F}\cdot d\vec{s}=q_0\int_C\vec{E}\cdot d\vec{s}=K\frac{Qq}{r_A}-K\frac{Qq}{r_B}$$
- $K$: è la **costante di Coulomb**, è la costante di proporzionalità che definisce l’intensità della forza tra cariche elettroniche. Nel vuoto: ha valore $8,99\cdot10^9N\cdot\frac{m^2}{C^2}$, spesso scritta anche come $\frac{1}{4\pi\varepsilon_0}$.
- $Q$: **carica sorgente**, è la carica che genera il campo elettrico nello spazio circostante.
- $q$: **carica di prova**, è la carica che viene spostata dal punto A al punto B all’interno del campo generato da $Q$.
- $r_A$ ed $r_B$: è la **distanza radiale** tra la carica sorgente $Q$ e la posizione rispettiva di $A$ o di $B$.

**Differenza di energia potenziale cinetica**: $K\frac{Qq}{r_A}-K\frac{Qq}{r_B}$
**Energia potenziale elettrica**: $U=K\frac{Qq}{r}$
**differenza di energia potenziale elettrica**: $V_B-V_A=-\int_A^B\vec{E}\cdot d\vec{s}$

**Campo elettrico di una carica puntiforme**: $\vec{E}=K\cdot\frac{q}{r^2}\hat{u}_r$ Sarebbe la legge di Coulomb applicata al campo elettrico
- $q$: carica che genera il campo;
- $r^2$: il quadrato della distanza dal punto in cui misuri il campo;
- $\hat{u}_r$: versore radiale, indica che il campo “scappa” dalla carica in tutte le direzioni come i raggi di una ruota(se la carica è positiva).

**Campo elettrico di un piano infinito di carica**: $\vec{E}=\frac{\sigma}{2\varepsilon}\hat{u}_x$ questa descrive il campo generato da una distribuzione superficiale di carica
 - $\sigma$(sigma): è la densità superficiale di carica. Indica quanta carica c’è per ogni metro quadrato di superficie($\frac{C}{m^2}$);
 - $\varepsilon$(epsilon): è la costante dielettrica del mezzo. Indica come il mezzo risponde alla presenza di cariche;
 - $2$: il piano ha 2 facce quindi il flusso del campo si divide in due direzioni opposte;
 - $\hat{u}_x$: è il versore che indica la direzione perpendicolare al piano.

### Teorema dell’Energia Meccanica: $W_{A\to B}=\Delta K=-\Delta U$
Spiega perché una carica si muove:
- $W_{A\to B}$: è il lavoro compiuto dal campo elettrico per spostare la carica dal punto A al punto B;
- $\Delta K$: energia cinetica;
- $\Delta U$: energia potenziale.

**Forza Elettrica**: $\vec{F}=q\vec{E}$ definizione del campo elettrico
- $\vec{F}$: è la forza che agisce sulla carica;
- $q$: è il valore della carica nel campo;
- $\vec{E}$: è il campo elettrico preesistente.
La tensione elettrica tra A e B relativa a percorso C è:$$T(A\to B \quad lungo C)=\frac{W}{q_0}=\int_C\vec{E}\cdot d\vec{s}\neq T’(A\to B \quad lungo C’)$$


## Potenziale
$$W=\oint\vec{F}\cdot d\vec{s}=\int_1\vec{F}\cdot d\vec{s}-\int_2\vec{F}\cdot d\vec{s}=W_1-W_2=q_0\varepsilon$$
![[Pasted image 20260309150922.png]]

**Forza elettromotrice(f.e.m)**:  $\varepsilon=\oint_C E\cdot ds$ (non è una forza)
Se la forza F è conservativa, la circuitazione è nulla(non dipende dal percorso)

La forza elettrostatica è conservativa $\to$ il campo è conservativo $\to$ si può definire un **potenziale elettrostatico**

# Potenziale ed energia potenziale
Il potenziale in un punto è determinato a meno di una costante additiva

Il lavoro della forza per portare $q_0$ da A a B si può scrivere: $$W_{AB}=-q_0(V_B-V_A)=-q_0\Delta V$$
Ad ogni forza conservativa è associata un’energia potenziale. Il lavoro della forza è pari all’opposto della variazione dell’energia potenziale.$$W_{AB}=-\Delta U_e=-(U_e(B)-U_e(A))\quad\to\quad \Delta U_e=q_0\Delta V$$
**Energia elettrostatica**: $U_e=q_0V$
In un campo elettrostatico la f.e.m è sempre nulla e quindi è nullo il lavoro della forza elettrica per ogni spostamento che riporti la carica nella posizione iniziale

### Lavoro tra due punti: $W_{A\to B}=U_A-U_B=\frac{KQq}{r_A}-\frac{KQq}{r_B}$
### Spostamento all’infinito: $W_{r\to\infty}=U(r)-U(\infty)=\int_r^\infty\vec{F}\cdot d\vec{s}$
In fisica, per comodità, stabiliamo che a distanza infinita dalla carica sorgente l'energia potenziale sia zero($U(\infty)=0$).
- Questa formula ci dice che l’energia potenziale $U(r)$ in un punto non è altro che il lavoro che il campo farebbe per spingere la carica da quel punto $r$ fino ad una distanza infinita.
- l’integrale serve a sommare tutti i piccoli contributi di forza lungo questo lunghissimo viaggio.
### Definizione di Energia Potenziale e Potenziale
$$U(r)=\int_r^\infty\vec{F}\cdot d\vec{r}$$ L’energia potenziale $U$ in un punto $r$ è l’integrale della forza da quel punto all’infinito.
$$U(r)=q\cdot V(r)$$
Dice che l’energia potenziale è uguale alla carica $q$ moltiplicata per il potenziale elettrico $V$.

La differenza sottile: Mentre l'energia ($U$) dipende da quale carica $q$ metti nel campo, il potenziale ($V$) dipende solo dalla carica sorgente $Q$ e dalla posizione. Il potenziale è come una "caratteristica del terreno", l'energia è quanto un oggetto fatica a starci sopra.

Potenziale: $V(r)=\frac{KQ}{r}$

# Il lavoro non dipende dal percorso
Il lavoro della forza $F$ per uno spostamento ds della carica $q_0$ nel campo generato dalla carica puntiforme $q$ è:$$dW=q_0\vec{E}\cdot d\vec{s}=\frac{q_0q}{4\pi\varepsilon_0}\frac{\vec{u}\cdot d\vec{s}}{r^2}=\frac{q_0q}{4\pi\varepsilon_0}\frac{dr}{r^2}$$
$\vec{E}\cdot d\vec{s}=\frac{q}{4\pi\varepsilon_0}\frac{dr}{r^2}$
$dr=\vec{u}\cdot d\vec{s}=ds cos\theta$

### Dimostrazione matematica del lavoro compiuto dal campo elettrico quando spostiamo una carica da un punto A ad un punto B

$$W_{AB}=q_0\int_A^B\vec{E}\cdot d\vec{s}=\frac{q_0q}{4\pi\varepsilon_0}\int_{r_A}^{r_B}\frac{dr}{r^2}=-(\frac{q_0q}{4\pi\varepsilon_0r_B}-\frac{q_0q}{4\pi\varepsilon_0r_A})$$
**Il lavoro non dipende dal percorso**

1. Definizione generale:($W_{AB}=q_0\int_A^B\vec{E}\cdot d\vec{s}$) il lavoro è l’integrale del prodotto tra la carica di prova($q_0$) e il campo elettrico($\vec{E}$) lungo il cammino $d\vec{s}$.
2. L’inserimento della legge di Coulomb: $\frac{q_0q}{4\pi\varepsilon_0}\int_{r_A}^{r_B}\frac{dr}{r^2}$ il campo elettrico $\vec{E}$ è stato sostituito con la sua formula per una carica puntiforme. I termini costanti ($\frac{q_0q}{4\pi\varepsilon_0}$) sono stati portati fuori dall’integrale. Nota che $4\pi\varepsilon_0$ non è altro che il modo esteso di scrivere la costante $K$ che abbiamo visto prima.
3. Risoluzione dell’integrale:($-(\frac{q_0q}{4\pi\varepsilon_0r_B}-\frac{q_0q}{4\pi\varepsilon_0r_A})$) l’integrale di $\frac{1}{r^2}$ è $-\frac{1}{r}$. Applicando gli estremi di integrazione, otteniamo il risultato finale.

Il lavoro fatto dal campo è uguale all’energia potenziale iniziale meno quella finale. Se il lavoro è positivo, l’energia potenziale del sistema è diminuita.