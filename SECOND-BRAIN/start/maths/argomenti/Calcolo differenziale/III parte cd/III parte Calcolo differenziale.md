# Asintoto
**Asintoto** è un parola che deriva dal greco: ”A” significa “no” e “sympiptein“ significa congiungere cioè che non tocca, si tratta quindi di una retta che si avvicina al grafico della funzione senza mai toccarlo, per questo si dice che un asintoto è la tangente all’infinito della funzione.

# Asintoto verticale
Calcolando $\lim_{x\to x_0}f(x)$; se il limite è $+\infty$ o $-\infty$, la funzione ammette un asintoto verticale di equazione $x=x_0$. Stesso discorso nel caso in cui gli asintoti, destro e sinistro, tendono a $\pm\infty$ ma con segni opposti. 
## Definizione 
Siano $f:domf\to\mathbb{R}$ e $x_0\in\mathbb{R}$.
- Se $x_0$ è un punto di accumulazione per $domf\cup]x_0,+\infty[$ e $\lim_{x\to x_0^+}f(x)=+\infty$ oppure $-\infty$, allora la retta di equazione $x=x_0$ si dice **asintoto verticale destro** per $f$;
- Se $x_0$ è un punto di accumulazione per $domf\cup]-\infty,x_0[$ e $\lim_{x\to x_0^-}f(x)=+\infty$ oppure $-\infty$, allora la retta di equazione $x=x_0$ si dice **asintoto verticale sinistro** per $f$.
Se la retta di equazione $x=x_0$ è contemporaneamente asintoto verticale destro e sinistro per $f$, si dice semplicemente che essa è un **asintoto verticale** per $f$.

# Comportamento asintotico:asintoti orizzontali e obliqui
Quando la funzione assegnata $f$ risulta definita in insiemi illimitati, è interessante studiarne il comportamento quanto $x\to\pm\infty$. La prima operazione che ci viene in mente di fare è quindi verificare se esiste$$\lim_{x\to\pm\infty}f(x)=l\in\mathbb{R}$$
In questo caso si dirà che la funzione assegnata $f$ tende asintoticamente ad $l\in\mathbb{R}$, oppure anche che $f$ ha asintoto orizzontale di equazione $y=l$ quando $x\to\pm\infty$.
Se il limite della funzione $f$ esiste, ma si ha $\lim_{x\to\pm\infty}f(x)=\pm\infty$ non esiste asintoto orizzontale. In queste condizioni potremmo dire che la funzione tende ad un asintoto obliquo, ovvero che esistano due costanti $m$, $q\in\mathbb{R}$ per cui si abbia la situazione che il grafico della funzione $f$ si avvicina al grafico della retta di equazioni $y=mx+q$ per $x\to\pm\infty$.

# Asintoto orizzontale
Siano $f:domf\to\mathbb{R}$.
- Se $domf$ è illimitato superiormente e $\lim_{x\to+\infty}f(x)=l\in\mathbb{R}$, allora la retta di equazione $y=l$ si dice **asintoto orizzontale destro** per $f$;
- Se $domf$ è limitato inferiormente e $\lim_{x\to-\infty}f(x)=l\in\mathbb{R}$, allora la retta di equazione $y=l$ si dice **asintoto orizzontale sinistro** per $f$.
Se la retta di equazione $y=l$ è contemporaneamente asintoto orizzontale destro e sinistro per $f$, si dice semplicemente che essa è un **asintoto orizzontale** per $f$.

# Asintoto obliquo
Siano $f:domf\to\mathbb{R}$ con $domf$ illimitato superiormente e $m,q\in\mathbb{R}$ con $m\neq0$. Si dice che la retta di equazione $y=mx+q$ è un **asintoto obliquo destro**, per $x\to+\infty$, per $f$ se $$\lim_{x\to+\infty}(f(x)-mx-q)=0\quad\quad (\text{rispettivamente }x\to-\infty)$$
Se la retta di equazione $y=mx+q$ è contemporaneamente asintoto obliquo destro e sinistro per $f$, si dice semplicemente che essa è un **asintoto obliquo** per $f$.

# Proposizione
Siano $f:domf\to\mathbb{R}$ con $domf$ illimitato superiormente/inferiormente e $m,q\in\mathbb{R}$ con $m\neq0$. Allora, la retta di equazione $y=mx+q$ è un asintoto obliquo destro/sinistro per $f$ se e solo se valgono i seguenti fatti:
1. $\lim_{x\to\pm\infty}\frac{f(x)}{x}=m$;
2. $\lim_{x\to\pm\infty}(f(x)-mx)=q$.

# Punti di non derivabilità: punti angolosi e cuspidi

## Punto angoloso
Supponiamo che in $x_0$ la funzione $f$ sia continua ma non derivabile. Se esistono finiti i limiti destro e sinistro, ovvero:$$\lim_{x\to x^+_0}f’(x)=l^+,\quad\quad \lim_{x\to x_0^-}f’(x)=l^-$$
Dato che $f$ non è derivabile nel punto $x_0$, si deve avere $l^+\neq l^-$. In questo caso avremo il **punto angoloso**. Per disegnarlo correttamente è possibile rappresentare le rette tangenti destra e sinistra, ovvero le rette di equazione$$y=f(x_0)+l^{\pm}(x-x_0)$$
### Definizione
Siano $f:domf\to\mathbb{R}$ una funzione e $x_0\in domf$ un punto interno a $domf$. Sì dice che $x_0$ è un **punto angoloso** per $f$ se esistono le derivate laterali $f’_+(x_0)$ e $f’_-(x_0)$ ma sono diverse.



## Punto di flesso(cuspide)
Nel caso in cui i limiti destro e sinistro valgano $\pm\infty$ si possono avere due situazioni differenti. Se entrambi sono $+\infty$ o $-\infty$, cioè se $$\lim_{x\to x_0}f’(x)=+\infty, \quad(-\infty)$$
il punto $x_0$ è un **punto di flesso a tangente verticale**. Se invece i limiti destro e sinistro sono $\pm\infty$ ma con segni opposti, il punto $x_0$ è una cuspide del grafico di $f$.

### Definizione (cuspide)
Siano $f:domf\to\mathbb{R}$ una funzione e $x_0\in domf$ un punto interno a $domf$. Sì dice che $x_0$ è una cuspide per $f$ se $f$ è continua in $x_0$ ed esistono infiniti e diversi tra loro i limiti $$\lim_{x\to x^{\pm}_0}\frac{f(x)-f(x_0)}{x-x_0}$$
### Definizione (punto di flesso a tangente verticale)
Siano $f:domf\to\mathbb{R}$ una funzione e $x_0\in domf$ un punto interno a $domf$. Sì dice che $x_0$ è un **punto di flesso a tangente verticale** per $f$ se $f$ è continua in $x_0$ ed esistono infiniti e uguali i limiti $$\lim_{x\to x_0^{\pm}}\frac{f(x)-f(x_0)}{x-x_0}$$

# Funzioni concave e funzioni convesse

## Funzioni concave e funzioni convesse con ipotesi di derivabilità

### Funzione convessa in un intervallo 
Siamo $f:domf\to\mathbb{R}$ una funzione e $I\subseteq domf$ un intervallo tale che $f$ sia derivabile in $I$. Sì dice che $f$ è convessa in $I$ se $$f(x)\geq f(x_0)+f’(x_0)(x-x_0),\quad\quad\forall x_0,x\in I$$
Si dice che $f$ è strettamente convessa in $I$ se$$f(x)>f(x_0)+f’(x_0)(x-x_0),\quad\quad\forall x_0,x\in I,x\neq x_0$$

![[Convessa_in_intervallo.jpg]]

Se $f$ è convessa si dice anche che $f$ ha la concavità verso l’alto. 

### Funzione concava in un intervallo 
Siamo $f:domf\to\mathbb{R}$ una funzione e $I\subseteq domf$ un intervallo tale che $f$ sia derivabile in $I$. Sì dice che $f$ è concava in $I$ se $$f(x)\le f(x_0)+f’(x_0)(x-x_0),\quad\quad\forall x_0,x\in I$$
Si dice che $f$ è **strettamente concava** in $I$ se $$f(x)<f(x_0)+f’(x_0)(x-x_0),\quad\quad\forall x_0,x\in I,x\neq x_0$$
![[Concava_in_intervallo.jpg]]
Se $f$ è concava si dice anche che $f$ ha la concavità verso il basso.


### Punto di flesso ascendente
Sia $f:domf\to\mathbb{R}$ una funzione derivabile in un punto $x_0$ interno a $domf$. Sì dice che $x_0$ è un punto di flesso ascendente se esiste un intorno $]x_0-\delta,x_0+\delta[$ di $x_0$ contenuto in $domf$ tale che $$\begin{align}f(x)\leq f(x_0)+f’(x_0)(x-x_0), \quad\quad\forall x\in]x_0-\delta,x_0[ \\\\ f(x)\ge f(x_0)+f’(x_0)(x-x_0),\quad\quad\forall x\in]x_0,x_0+\delta[\end{align}$$
Da continuare