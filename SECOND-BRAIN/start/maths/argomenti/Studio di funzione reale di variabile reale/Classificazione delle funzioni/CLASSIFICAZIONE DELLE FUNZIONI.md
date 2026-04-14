$$f: A \rightarrow B$$
# Suriettiva
Una funzione è suriettiva se ogni elemento del secondo insieme è raggiunto da almeno una freccia che parte dal primo insieme. DEFINIZIONE: una funzione è suriettiva se l'immagine della funzione $f$ coincide con il codominio, che è l'insieme di arrivo della funzione.
$$\forall b \in B \quad \exists a\in A: f(a)=b$$
esempio:
$f:\mathbb{R}\to\mathbb{R}$,  $f(x)=2x+3$
vogliamo trovare $x$ tale che $f(x)=y$:
$y=2x+3 \quad\to\quad x=\frac{y-3}{2}$
per ogni $y$ reale esiste un $x$ reale corrispondente. Quindi ogni numero reale è coperto, quindi $f$ è suriettiva. Questa funzione è anche iniettiva, quindi è biunivoca, ma per la suriettività basta che tutti gli elementi del codominio siano immagini.

# Iniettiva
Una funzione si dice iniettiva se elementi distinti del dominio(l'insieme su cui la funzione è definita, nel nostro caso A) hanno immagini distinte

$\forall x_1,x_2 \in A \quad x_1\neq x_2 \quad => f(x_1)\neq f(x_2)$


Quando una funzione è sia iniettiva che suriettiva si dice invertibile ovvero che è possibile trovare la sua **funzione inversa**
# Funzioni algebriche

## Funzioni polinomiali
$$y=x^3+2x-1$$

## Funzioni fratte
$$y=\frac{x^2-1}{x}$$
## Funzioni irrazionali
$$y=\sqrt[3]{x^3-1}$$

# Funzioni trascendenti

## Funzioni esponenziali
fissato un numero reale $A>0$ con $A\neq1$ si chiama funzione esponenziale di base $A$, la funzione di equazione:$$y=A^x$$
dove il Dominio($D$) è $\mathbb{R}$ e il codominio $\mathbb{R}^+-{0}$ 
Se $A>1$ la funzione è crescente
se $0<A<1$ la funzione è decrescente
![[grafico-funzione esponenziale.png]]
[[PROPRIETÀ DELLA FUNZIONE ESPONENZIALE]]



$y=3^x-1$  o  $y=e^x$ 

## Funzioni trigonometriche

$y=sen(x)$

## Funzioni logaritmiche
$y=log(x+1)$

![[esempioR.jpg]]

# Regole

$y=a_nx^n+a_{n-1}x^{x-1}+...+a_1x+a_0$ 

$y=\frac{P(x)}{Q(x)}$  $\mathbb{R}\ / \ [x_0,...x_n]$ 

$y=\sqrt[n]{f(x)}$   $D: \ x\in \mathbb{R} f(x) \geq 0$ 

$y=log_a f(x) \quad a>0$   $D: \ x \in \mathbb{R}:f(x)>0$ 

$y=a^{f(x)} \quad a>0 \quad a\neq1$   

$y=[f(x)]^{g(x)}$   $D:x \in \mathbb{R} | f(x)>0, \ f(x)\neq1 \quad \cap \quad dominio \ di \ g(x)$ 

$y=f(x)^\alpha$    $\begin{align} \alpha>0 \quad f(x)\geq0 \\ \alpha<0 \quad f(x)>0 \end{align}$

$y=sex(x) \quad y=cos(x)$     $\mathbb{R}$

![[start/maths/argomenti/Studio di funzione reale di variabile reale/Classificazione delle funzioni/regole.jpg]]


# Funzione pari
Si dice pari quando $f(-x)=f(x) \ \forall x\in D$ 
$$D\subseteq \mathbb{R} \quad x\in D \quad -x\in D \quad f:D\to \mathbb{R} \quad f(-x)=f(x)$$
La parte destra del grafico combacia con quella di sinistra
es:$$y=\frac{1}{x^2} \to f(-x)=\frac{1}{x^2}=f(x)$$
# Funzione dispari
Si dice dispari quando $f(-x)=-f(x)$ 
$$D\subseteq \mathbb{R} \quad x\in D \quad -x\in D \quad f:D\to \mathbb{R} \quad f(-x)=-f(x)$$
Il dominio deve essere simmetrico rispetto a 0, ovvero se $x\in D$ anche $-x\in D$; il grafico è **simmetrico rispetto all'origine**.
es:$$y=\frac{x^3}{x^2-1} \to f(-x)=\frac{(-x)^3}{(-x)^2-1}=-\frac{x^3}{x^2-1}$$
# Funzione crescente
$$f:D\to \mathbb{R} \quad D\subseteq \mathbb{R} \quad I\subseteq D \quad \forall x_1,x_2\in I \quad x_1<x_2 \quad f(x_1)\leq f(x_2)$$
$f$ è una funzione con dominio $D$ e valori reali, il dominio è un sottoinsieme dei numeri reali, considerando un intervallo $I$ del dominio, per ogni coppia di punti $x_1,x_2$ dell'intervallo $I$, se aumenta x, non diminuisce $f(x)$

## definizione
Una funzione è crescente in un intervallo se, prendendo due qualunque punti $x_1$ e $x_2$ di quell'intervallo con $x_1<x_2$ vale:$$f(x_1)\leq f(x_2)$$
# Funzione decrescente
$$f:D\to \mathbb{R} \quad D\subseteq \mathbb{R} \quad I\subseteq D \quad \forall x_1,x_2\in I \quad x_1<x_2 \to f(x_1)\geq f(x_2)$$


# Funzione monotòna (sempre iniettiva)
È una funzione che, in un dato intervallo, è sempre crescente o sempre decrescente.
$$f:D\to\mathbb{R} \quad D\subseteq \mathbb{R} \quad I\subseteq D\subseteq \mathbb{R} \quad \forall x_1,x_2 \in I \quad x_1\neq x_2(x_1<x_2) \to f(x_1)<f(x_2) \quad\text{o}\quad f(x_1)>f(x_2)$$

# Funzione periodica($sen$ e $cos$)

$$f:D\to\mathbb{R} \quad y=f(x) \quad T>0 \quad \forall k\in\mathbb{Z} \quad f(x)=(x+kT)$$
dove T è il periodo


# Funzioni inverse
Quando ammette la sua funzione inversa si dice invertibile
$$f:A\to B \quad y=f(x) \quad x=f^{-1}(y)$$

# Funzioni composte
$$f:A\to B \quad g:B\to C \quad g\circ f\neq f\circ g$$