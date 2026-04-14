
# Teorema di derivazione della funzione composta 
Siano $f:A\to\mathbb{R}$ e $g:B\to\mathbb{R}$ due funzioni con $im f \subseteq DOMg$ e $x_0$ punto interno a $A$ tale che $f(x)$ sia interno a $B$. Si supponga che $f$ sia derivabile in $x_0$ e che $g$ sia derivabile in $f(x_0)$. Allora $g$ o $f$ è derivabile in $x_0$ e si ha che:$$(g \quad o \quad f)’(x_0)=g’(f(x_0))f’(x_0)$$

# Teorema di derivazione della funzione inversa

## Definizione di funzione inversa
Siano $X$ e $Y$ due insiemi e sia $f:X\to Y$ iniettiva. Sì dice funzione inversa di $f$, e si indica con il simbolo $f^{-1}$ la funzione:
$f^{-1}:f(X)\to X,$
$f^{-1}:y\to x,$
Dove $f(x)=y$. In tal caso diremo che $f$ è invertibile in $A$.

## Derivazione della funzione inversa(teorema)
Siano $I\subseteq\mathbb{R}$ un intervallo, $f:I\to\mathbb{R}$ una funzione derivabile e invertibile e $x_0$ un punto interno a $I$. Si supponga che $f$ sia derivabile in $x_0$ con $f’(x_0)\neq0$. Allora $f^{-1}$ è derivabile n $y_0=f(x_0)$ e si ha che:$$(f^{-1})’(y_0)=\frac{1}{f’(f^{-1}(y_0))}$$
In pratica si invertono **codominio** e **dominio**.

Esempio:
$y=tan(x) \quad\to\quad x=arctan(y)$
$D[arctan(y)]=\frac{1}{D[tan(x)]}$   $\to$    $\frac{1}{1+tan^2(x)}=\frac{1}{1+y^2}$ 


# Teoremi fondamentali del calcolo differenziale

## Teorema di Fermat
### Minimo locale e massimo locale
Siano $X\subseteq\mathbb{R}$,$f:X\to\mathbb{R}$,$x_0\in X$.
- Si dice che $x_0$ è un **punto di minimo locale** di $f$ e $f(x_0)$ di dice **minimo locale** i $f$ se esiste un intorno $I_{\varepsilon}(x_0)$ del punto $x_0$ tale che $f(x_0)\leq f(x)$, per ogni $x\in I_{\varepsilon}(x_0)\cap X$, cioé:$$\exists\varepsilon>0:f(x_0)\leq f(x), \quad\quad\quad \forall x\in I_{\varepsilon}(x_0)\cap X$$
- Si dice che $x_0$ è un **punto di massimo locale** di $f$ e $f(x_0)$ si dice **massimo locale** di $f$ se esiste un intorno $I_{\varepsilon}(x_0)$ del punto $x_0$ tale che $f(x)\leq f(x_0)$, per ogni $x\in I_{\varepsilon}(x_0)\cap X$, cioé:$$\exists\varepsilon>0:f(x)\leq f(x_0), \quad\quad\quad \forall x\in I_{\varepsilon}(x_0)\cap X$$
Guarda la definizione di punto stazionario

### Teorema(Fermat, 1744)
Siano $f:domf\to\mathbb{R}$,$x_0$ punto interno a $domf$. Si supponga che:
- $f$ sia derivabile in $x_0$;
- $x_0$ un punto di minimo o massimo relativo per $f$.
Allora $f’(x_0)=0$, cioè $x_0$ è un punto stazionario per $f$.

Dimostrazione facoltativa.

## Teorema di Rolle
Sia $f:[a,b]\to\mathbb{R}$ una funzione. Sì supponga che:
1. $f$ sia continua in $[a,b]$;
2. $f$ sia derivabile in $]a,b[$;
3. $f(a)=f(b)$.
Allora esiste $x_0\in]a,b[$ tale che $f’(x_0)=0$
### Dimostrazione
Essendo $f$ continua su $[a,b]$, per il teorema di Weierstrass $f$ ammette massimo e minimo assoluti in $[a,b]$. Quindi esistono $x_m$,$x_M$$\in[a,b]$ tali che$$f(x_m)=min_{[a,b]}f, \quad\quad\quad f(x_M)=max_{[a,b]}f$$
I punti $x_m$ e $x_M$ sono un punto di minimo e un punto di massimo per $f$. Ne segue che $$f(x_m)\leq f(x)\leq f(x_M), \quad\quad\quad \forall x\varepsilon\in[a,b]$$

## Teorema di Lagrange
Sia $f:[a,b]\to\mathbb{R}$ una funzione. Si supponga che:
- $f$ sia continua in $[a,b]$;
- $f$ sia derivabile in $]a,b[$
Allora esiste $x_0\in]a,b[$ tale che$$f’(x_0)=\frac{f(b)-f(a)}{b-a}$$
### Dimostrazione
Consideriamo la funzione ausiliaria $g:[a,b]\to\mathbb{R}$ definita da $$g(x)=f(x)-\frac{f(b)-f(a)}{b-a}(x-a)$$
Si ha che $g$ è continua in $[a,b]$ perché composizione di funzioni continue in $[a,b]$, $g$ è derivabile in $]a,b[$ perché composizione di funzioni derivabili in $]a,b[$ con$$g’(x)=f’(x)-\frac{f(b)-f(a)}{b-a}, \quad\quad\quad \forall x\in]a,b[$$
Inoltre: 
$g(a)=f(a)$
$g(b)=f(b)-\frac{f(b)-f(a)}{b-a}(b-a)=f(b)-f(b)+f(a)=f(a)$
Cioè $g(a)=g(b)$. Quindi $g$ soddisfa le ipotesi del Teorema di Rolle. Per il Teorema di Rolle esiste $x_0\in]a,b[$ tale che $g’(x_0)=0$, cioè $$f’(x_0)-\frac{f(b)-f(a)}{b-a}=0 \quad\quad\to\quad\quad f’(x_0)=\frac{f(b)-f(a)}{b-a}$$

# Legame tra monotonia e il segno della derivata
Siano $I\subseteq\mathbb{R}$ un intervallo, $f:I\to\mathbb{R}$ derivabile in $I$. Allora:
1. Se $f$ è crescente su $I$, allora $f’(x)\geq0$ per ogni $x\in I$;
2. Se $f’(x)\geq0$ per ogni $x\in I$, allora $f$ è crescente su $I$;
3. Se $f’(x)>0$ per ogni $x\in I$, allora $f$ è strettamente crescente su $I$.
Dimostrazione facoltativa

## Corollario
Sia $f:[a,b]\to\mathbb{R}$ una funzione. Sì supponga che $f$ sia continua in $[a,b]$ e derivabile in $]a,b[$. Allora:
1. se $f‘(x)\geq0$ per ogni $x\in]a,b[$, allora $f$ è crescente su $[a,b]$;
2. se $f’(x)>0$ per ogni $x\in]a,b[$, allora $f$ è strettamente crescente su $[a,b]$.


# Test per cercare i punti di massimo e di minimo
Siano $f:domf\to\mathbb{R}$,$I\subseteq domf$ un intervallo e $x_0$ un punto interno a $I$. Supponiamo che $f$ sia continua in $I$ e che $f$ sia derivabile in $I\backslash\{ x_0\}$. Allora:
1. Se $f’(x)>0$ per ogni $x\in I$ con $x<x_0$ e $f’(x)<0$ per ogni $x\in I$ con $x>x_0$, allora $x_0$ è un punto di massimo locale per $f$;
2. Se $f’(x)<0$ per ogni $x\in I$ con $x<x_0$ e $f’(x)>0$ per ogni $x\in I$ con $x>x_0$, allora $x_0$ è un punto di minimo locale per $f$;
3. Se $f’(x)>0$ per ogni $x\in I$ con $x\neq x_0$, allora $x_0$ non è né un punto di massimo né di minimo per $f$;
4. Se $f’(x)<0$ per ogni $x\in I$ con $x\neq x_0$, allora $x_0$ non è né un punto di massimo né di minimo per $f$;

# Caratterizzazione delle funzioni costanti
Sia $f:[a,b]\to\mathbb{R}$ una funzione derivabile. Allora $f$ è costante se e solo se $f’(x)=0$ per ogni $x\in[a,b]$.

## Dimostrazione
**Banale**. Se $f$ è costante, allora essa è derivabile e la sua derivata è identicamente nulla.
Sia $x\in[a,b]$, per il Teorema di Lagrange applicato all’intervallo $[a,x]$ sappiamo che deve esistere un $c\in(a,x)$ tale che$$f’(c)=\frac{f(x)-f(a)}{x-a}$$
Per ipotesi $f’$ è uguale a zero per ogni $x\in[a,b]$, sarà anche $f’(c)=0$ e di conseguenza avremo $f(x)-f(a)=0$. Da cui $f(x)=f(a)$ e per l’arbitrarietà nella scelta di $x$ segue la tesi.

# Forme indeterminate e Teoremi di De L’Hôpital
Le più comuni sono:

| Forma                     | Esempio                                          |
| ------------------------- | ------------------------------------------------ |
| $\frac{0}{0}$             | $\lim\frac{p(x)}{q(x)}$ quando $p(x_0)=q(x_0)=0$ |
| $\frac{\infty}{\infty}$   | polinomi con gradi diversi per $x→±∞$            |
| $0·∞, ∞−∞, 1^∞, 0^0, ∞^0$ | altre forme che richiedono tecniche specifiche   |
Quando compare una forma indeterminata non si possono usare semplici regole algebriche: servono sostituzioni, sviluppi in serie, o il Teorema di De L’Hôpital.

## Forma indeterminata $\frac{0}{0}$ 
- Se $p(x_0)=q(x_0)=0$, il binomio $(x−x_0)$ divide entrambi; si semplifica e si calcola il limite sul quoziente dei fattori rimanenti.
- Esempio: $lim_{x→2} \frac{x2−4}{3x2−x−2}$. Scomposizione e semplificazione danno il limite numerico.

$$\lim_{x\to x_0}\frac{ax^n+bx^{n-1}+…+c}{dx^m+ex^{m-1}+…+l}$$
Con $x_0\in\mathbb{R}$. 
Se il limite si ripresenta nella forma indeterminata $\frac{0}{0}$, il valore $c$ è radice di entrambi i polinomi del numeratore e del denominatore. Per risolverlo basta applicare il teorema di ruffiani per scomporre numeratore e denominatore.

## Teorema di De L’Hôpital nella forma $\frac{0}{0}$
Siano $A\subseteq\mathbb{R}$ un intervallo, $f,g:A\to\mathbb{R}$ due funzioni e $x_0\in\mathbb{R}$ un punto di accumulazione per $A$. Si supponga che
1. $\lim_{x\to x_0}f(x)=\lim_{x\to x_0}g(x)=0$;
2. Esista un intorno $I(x_0)$ di $x_0$ tale che $f$ e $g$ siano derivabili in ogni $x\in A\cap I(x_0)$,$x\neq x_0$, e che per tali $x$ si abbia $g’(x)\neq0$;
3. Esista $\lim_{x\to x_0}\frac{f’(x)}{g’(x)}=I\in\mathbb{R}$
Allora $$\lim_{x\to x_0}\frac{f(x)}{g(x)}=l$$
## Forma indeterminata $\frac{\infty}{\infty}$
$$\lim_{x\to\infty}\frac{ax^n+bx^{n-1}+…+c}{dx^m+ex^{m-1}+…+l}$$
Per calcolare i limiti di questo tipo, si raccoglie sia al numeratore che al denominatore l’incognita di grado massimo ottenendo una scrittura del tipo:$$\lim_{x\to\infty} \frac{ax^n+bx^{n-1}+…+c}{dx^m+ex^{m-1}+…+l}=\lim_{x\to\infty}\frac{x^n(a+\frac{b}{x}+…+\frac{c}{x^n})}{x^m(d+\frac{e}{x}+…+\frac{l}{x^m})}$$
Così semplifichiamo i termini $x^n$ e $x^m$ e si calcola il limite tenendo presente che i contributi frazionari a zero. In generale si può affermare che $$=\begin{cases}\infty,\quad\text{se}\quad n>m \\ \frac{a}{d},\quad\text{se}\quad n=m \\ 0\quad\text{se}\quad n<m\end{cases}$$

# Teorema di De L’Hôpital nella forma $[\frac{\infty}{\infty}]$ 
Siano $A\subseteq\mathbb{R}$ un intervallo, $f$,$g:A\to\mathbb{R}$ due funzioni e $x_0\in\mathbb{R}$ un punto di accumulazione per $A$. Si supponga che 
1. $\lim_{x\to x_0}f(x)=+\infty$ oppure $\lim_{x\to x_0}=-\infty$ e che $\lim_{x\to x_0}g(x)=+\infty$ oppure $\lim_{x\to x_0}g(x)=-\infty$;
2. Esista un intorno $I(x_0)$ di $x_0$ tale che $f$ e $g$ siano derivabili in ogni $x\in A\cap I(x_0)$,$x\neq x_0$, e che per tali $x$ si abbia $g’(x)\neq0$;
3. Esista $\lim_{x\to x_0}\frac{f’(x)}{g’(x)}=l\in\mathbb{R}$.
Allora $$\lim_{x\to x_0}\frac{f(x)}{g(x)}=l$$
# Teorema sul limite della derivata
Siano $I\subseteq\mathbb{R}$ un intervallo, $f:I\to\mathbb{R}$ due funzioni e $x_0$ un punto interno ad $I$. Sì supponga che 
1. $f$ sia continua in $I$;
2. $f$ sia derivabile in $I\backslash\{ x_0\}$;
3. Esista $\lim_{x\to x_0}f’(x)=l\in\mathbb{R}$.
Allora $f$ è derivabile in $x_0$ con $f’(x_0)=l$. Inoltre $f’$ è continua in $x_0$
## Dimostrazione


# Derivate di ordine superiore
## Derivata seconda
Siano $f:domf\to\mathbb{R}$ un funzione e $x_0\in domf$ un punto interno a $domf$. Supponiamo che $f$ sia derivabile in un intorno $I(x_)$ di $x_0$ contenuto in $domf$. Si dice che $f$ è derivabile due volte in $x_0$ se $f’$ è derivabile in $x_0$ e in tal caso si chiama derivata seconda di $f$ in $x_0$ la derivata prima di $f’$ in $x_0$ e la denotiamo con uno dei seguenti simboli:$$f’’(x_0),\quad\quad D^2f(x_0),\quad\quad \frac{d^2f}{dx^2}(x_0),\quad\quad \ddot{f}(x_0)$$
Quindi$$f’’(x_0)=(f’)’(x_0) \quad\text{se esiste finito}\quad\to\lim_{x\to x_0}\frac{f’(x)-f’(x_0)}{x-x_0}$$
## Derivata $n$-esima
Siano $f:domf\to\mathbb{R}$ un funzione e $x_0\in domf$ un punto interno a $domf$,$n\in\mathbb{N}$ con $n\geq2$ . Supponiamo che $f$ sia derivabile $n-1$ volte in un intorno $I(x_0)$ di $x_0$ contenuto in $domf$. Si dice che $f$ è derivabile $n$ volte in $x_0$ se la derivata ($n-1$)-esima di $f$ è derivabile in $x_0$ e in tal caso si chiama derivata n-esima di $f$ in $x_0$ la derivata prima della derivata (n-1)-esima di $f$ in $x_0$ e la denotiamo con uno dei seguenti simboli:$$f^{(n)}(x_0),\quad\quad D^nf(x_0),\quad\quad \frac{d^nf}{dx^n}(x_0),\quad\quad \ddot{f}(x_0)$$
quindi$$f^{(n)}(x_0)=(f^{(n-1)})’(x_0)\text{se esiste finito}\to\lim_{x\to x_0}\frac{f^{(n-1)}(x)-f^{(n-1)}(x_0)}{x-x_0}$$
La derivata $n$-esima è detta anche derivata di ordine $n$.

# Classi $C^k$ (definizione)
Siano $I\subseteq\mathbb{R}$ un intervallo, $f:I\to\mathbb{R}$ una funzione e $n\in\mathbb{N}$ con $n\geq1$. Si dice che $f$ è di classe $C^0$ su $I$ se $f$ è continua su $I$ e in tal caso si scrive $f\in C^0(I)$ oppure $f\in C(I)$. Ne segue che $C^0(I)=C(I)$ è l’insieme delle funzioni continue definite sull’intervallo $I$. Si dice che $f$ è di classe $C^1$ su $I$ se $f$ è derivabile con derivata prima continua su $I$ e in tal caso si scrive $f\in C^1(I)$. Ne segue che $C^1(I)$ è l’insieme delle funzioni derivabili con derivata continua definite sull’intervallo $I$.
Si dice che $f$ è di classe $C^n$ su $I$ se $f$ è derivabile $n$ volte con derivata $n$-esima continua $I$ e in tal caso si scrive con $f\in C^n(I)$. Ne segue che $C^n(I)$ è l’insieme delle funzioni derivabili con derivata $n$-esima continua definite sull’intervallo $I$. 
Si dice che $f$ è di classe $C^{\infty}$ su $I$ se $f$ ammette derivate di ogni ordine su $I$ e in tal caso si scrive $f\in C^{\infty}(I)$. Ne segue che $C^{\infty}(I)$ è l’insieme delle funzioni che ammettono derivate di ogni ordine definite sull’intervallo $I$.
