# Definizione generale di limite
Siano $f:DOMf \to \mathbb{R},x_0\in\bar{\mathbb{R}}$ un punto di accumulazione per $DOMf$, $l$ e $\bar{\mathbb{R}}$. Si dice che $f$ ha limite $l$ per $x$ che tende a $x_0$ se per ogni intorno $I(l)$ di $l$ esiste un intorno $I(x_0)$ di $x_0$ tale che per ogni $x\in DOMf$. Con $x\in I(x_0)$ e $x\neq x_0$ si ha che $f(x)\in I(l)$. Ovvero:
$\forall I(l)$ intorno di $l \quad\exists I(x_0)$ intorno di $x_0$ tale che $x\in DOMf\cap I(x_0),x\neq x_0 \to f(x)\in I(l)$

## 1° caso
$x_0\in \mathbb{R},l\in \mathbb{R}$ gli intorni di $l$ e $x_0$ sono:
$$I(l)=I_{\epsilon}(l)=]l-\epsilon,l+\epsilon[$$
$$I(x_0)=I_{\varepsilon}(x_0)=]x_0-\varepsilon,x_0+\varepsilon[$$
## 2° caso
$x_0\in\mathbb{R},l=+\infty$ gli intorni $l$ e $x_0$ sono:
$$I(l)=]a,+\infty[$$
$$I(x_0)=I_{\varepsilon}(x_0)=]x_0-\varepsilon,x_0+\varepsilon$$ 
## 3° caso
$x_0\in\mathbb{R},l=-\infty$ gli intorni di $l$ e $x_0$ sono:
$$I(l)=]-\infty,a[$$
$$I(x_0)=I_{\varepsilon}(x_0)=]x_0-\varepsilon,x_0+\varepsilon[$$
## 4° caso
$x_0=+\infty,l\in\mathbb{R}$ gli intorni $l$ e $x_0$ sono:$$I(l)=I_{\epsilon}(l)=]l-\epsilon,l+\epsilon[$$
$$l(x_0)=]a,+\infty[$$
## 5° caso
$x_0=-\infty,l\in\mathbb{R}$ gli intorni $l$ e $x_0$ sono:$$I(l)=I_{\epsilon}(l)=]l-\epsilon,l+\epsilon[$$
$$I(x_0)=]-\infty,a[$$
## 6° caso
$x_0=+\infty,l=+\infty$ gli intorni $l$ e $x_0$ sono:$$I(l)=]a,+\infty[$$
$$I(x_0)=]b,+\infty[$$
## 7° caso
$x_0=-\infty,l=-\infty$ gli intorni $l$ e $x_0$ sono:$$I(l)=]-\infty,a[$$
$$I(x_0)=]b,+\infty[$$
## 8° caso
$x_0=-\infty,l=+\infty$ gli intorni $l$ e $x_0$ sono:$$I(l)=]a,+\infty[$$
$$I(x_0)=]-\infty,b[$$
## 9° caso
$x_0=-\infty,l=-\infty$ gli intorni $l$ e $x_0$ sono:$$I(l)=]-\infty,a[$$
$$I(x_0)=]-\infty,b[$$


# Limitatezza locale 
siano $f: DOMf\to\mathbb{R}$ e $x_0\in\bar{\mathbb{R}}$ un punto di accumulazione per $DOMf$. Si supponga che esista 
$$\lim_{x\to\infty}f(x)=l\in\mathbb{R}$$
Allora esiste un intorno $I(x_0)$ di $x_0$ tale che $f$ è limitata su $(DOMf\cap I(x_0))\ [x_0]$ 

# Teorema si unicità del limite
Siano $f:DOMf\to\mathbb{R}$ e $x_0\in\bar{\mathbb{R}}$ un punto di accumulazione per $DOMf$. Se esistono $l1,l2\in\bar{\mathbb{R}}$ tali che:$$\lim_{x\to x_0}f(x)=l_1,\lim_{x\to x_0}f(x)=l_2$$
allora $l_1=l_2$. Dimostrare o enunciare il teorema di unicità del limite

# Teorema di permanenza del segno
$$\lim_{x\to x_0}f(x)=l\in\bar{\mathbb{R}}$$
Se $l>0$ oppure $l=+\infty$ ($l<0$ o $l=-\infty$) allora esiste $I_*(x_0) di $x_0$ tale che $f(x)>0$ ($f(x)$) per ogni $x\in$($DOMf\cap I_*(x_0)$)$/[x_0]$

# Operazioni con i limiti
Siano $A\subseteq\mathbb{R}$ non vuoto,$f$,$g$:$A\to \mathbb{R}$ e $x_0\in\bar{\mathbb{R}}$ un punto di accumulazione per $A$:$$\lim_{x\to x_0}f(x)=l_1,\lim_{x\to x_0}g(x)=l_2 \quad\quad l_1,l_2\in\mathbb{R}$$
**Altre operazioni**:
$\lim_{x\to x_0} (f(x)+g(x))=l_1+l_2$

$\lim_{x\to x_0}(f(x)g(x))=l_1l_2$   

se $l_1\neq0$ allora $\lim_{x\to x_0}\frac{1}{f(x)}=\frac{1}{l_1}$ 

se $l_2\neq0$ allora $\lim_{x\to x_0}\frac{f(x)}{g(x)}=\frac{l_1}{l_2}$

# Definizione di funzione continua
Siano $f:DOMf\to\mathbb{R}$ e $x_0\in DOMf$. Si dice che $f$ è continua in $x_0$ se per ogni intorno di $I(f(x_0))$ di $f(x_0)$ esiste un intorno $I(x_0)$ di $x_0$ tale che per ogni $x\in DOMf$ con $x\in I(x_0)$ si ha che $f(x)\in I(f(x_0))$

![[def-funzione-continua.jpg]]

$$I(f(x_0))=I_{\epsilon}(f(x_0))=]f(x_0)-\epsilon,f(x_0)+\epsilon[$$
$$I(x_0)=I_{\varepsilon}(x_0)=]x_0-\varepsilon,x_0+\varepsilon[$$


# Teorema di continuità e limiti
siano $f:DOMf\to\mathbb{R}$ e $x_0\in DOMf$. Si ha che:
1) se $x_0$ è un punto di accumulazione per $domf$, allora $f$ è continua in $x_0 \to \lim_{x\to x_0}f(x)=f(x_0)$;
2) se $x_0$ è un punto isolato per $domf$, allora $f$ è continua in $x_0$.
![[teorema-di-continuità.jpg]]
$$DOMf(-\infty,x_2)\cup[x_0]\cup[x_1,+\infty)$$
$$I(x_0)=(x_0-\varepsilon,x_0+\varepsilon) \quad\quad\quad DOMf\cap I(x_0)=\{x_0\}$$

# Algebra delle funzioni continue
Siano $f:DOMf\to\mathbb{R}$,$g:DOMg\to\mathbb{R}$ due funzioni continue in $x_0\in DOMf\cap DOMg$. Allora:
- $f+g$ e $f_g$ sono continue in $x_0$;
- se $f(x_0)\neq0$, allora $\frac{1}{f}$ è continua in $x_0$;
- se $g(x_0)\neq0$, allora $\frac{f}{g}$ è continua in $x_0$;


# Teorema delle funzioni composte
Siano $f:DOMf\to\mathbb{R}$,$g:DOMg\to\mathbb{R}$ due funzioni, tali che $f(DOMf)\subseteq DOMg$, siano $x_0\in DOMf$(e quindi $f(x_0)\in DOMg$). Si supponga che $f$ sia continua in $x_0$ e che $g$ sia continua in $f(x_0)$. Allora $g$ o $f$ è continua in $x_0$.


# Proprietà globali delle funzioni continue 

## Teorema di esistenza degli zeri
Sia $f:[a,b]\to\mathbb{R}$. Se $f$ è continua in $[a,b]$ e $f(a)f(b)<0$, allora esiste $c\in]a,b[$ tale che $f(c)=0$. Inoltre, se $f$ è strettamente monotona, tale punto $c$ è unico.
![[teorema-esistenza-zeri.jpg]]

#### Generalizzazione del teorema degli zeri
Siano $I\subseteq\mathbb{R}$ un intervallo e $f:I\to\mathbb{R}$ una funzione continua in $I$. Si supponga che $f$ ammetta limite per $x$ che tende agli estremi dell'intervallo $I$ e che questi limiti abbiano segni opposti. Allora esiste $c\in I$ tale che $f(c)=0$. Inoltre, se $f$ è strettamente monotona, allora un siffatto numero $c$ è unico.

## Teorema dei valori intermedi
Sia $f:[a,b]\to\mathbb{R}$ una funzione continua in $[a,b]$. Allora $f$ assume tutti i valori compresi tra $f(a)$ e $f(b)$, non necessariamente in questo ordine.
![[teorema-valori-intermedi.jpg]]

### Dimostrazione

Poiché $f(x)$ assume valori $y_1$ e $y_2$ allora esistono $x_1$ e $x_2$ $\in I$ tali che $f(x_1)=y_1$ e $f(x_2)=y_2$. Possiamo supporre che $x_1<x_2$.  Grazie ai valori $x_1,x_2$ possiamo costruire un intervallo chiuso e limitato $[x_1,x_2]$, contenuto in $I$. Per ipotesi sappiamo che $f(x)$ è continua in $I$, di conseguenza sarà continua anche in $[x_1,x_2]$. Sia $y_0$ un valore compreso tra $y_1$ e $y_2$:$$y_1<y_0<y_2$$
Dalla doppia diseguaglianza abbiamo:$$y_1<y_0 \quad\to\quad y_1-y_0<0$$
$$y_0<y_2 \quad\to\quad y_2-y_0>0$$
Ora, consideriamo la funzione ausiliaria:$$g(x)=f(x)-y_0 \quad con \quad x\in[x_1,x_2]$$
Essa è una funzione continua in quanto la differenza tra le funzioni continue $y=f(x)$ e la funzione costante $y=y_0$. Inoltre:$$g(x_1)=f(x_1)-y_0=y_1-y_0<0$$
$$g(x_2)=f(x_2)-y_0=y_2-y_0>0$$
La funzione ausiliaria soddisfa le ipotesi del **teorema degli zeri**, pertanto esiste $x_0\in(x_1,x_2)$ tale che:$$g(x_0)=0 \quad ossia \quad f(x_0)-y_0=0\to f(x_0)=y_0$$
Abbiamo dimostrato che comunque si fissi $y_0$ compreso tra $y_1$ e $y_2$ esiste $x_0\in I$ la cui immagine tramite la funzione $f(x)$ coincide con $y_0$.

## Teorema di Weierstrass
Sia $f:[a,b]\to\mathbb{R}$ una funzione continua in $[a,b]$. Allora $f$ assume minimo e massimo assoluti in $[a,b]$, cioè esistono$$m=minf \quad di[a,b], \quad\quad\quad M=maxf \quad di[a,b]$$
In particolare, esistono $x_m,x_M\in[a,b]$ tali che$$f(x_m)=m=minf \quad di[a,b] \quad\quad\quad f(x_M)=M=maxf \quad di [a,b]$$
Ovviamente, $imf=[m,M]$.
![[teorema-weiestrass.jpg]]


# Iniettività e stretta monotonia per funzioni continue
Siano $I\subseteq\mathbb{R}$ un intervallo e $f:I\to\mathbb{R}$ una funzione continua $I$. Allora:
$f$ e iniettiva se e solo se $f$ è strettamente monotona
![[iniettività-stretta-monotonia.jpg]]

## Dimostrazione
Dalle definizioni di stretta monotonia e iniettività. Supponiamo che $f$ non sia strettamente monotona, essendo $f$ iniettiva, ciò implica che $f$ non è monotona. Allora esistono $x_1,x_2,x_3\in I$, con $x_1<x_2<x_3$ tali che:$$f(x_1)<f(x_2), \quad\quad f(x_2)>f(x_3)$$
o$$f(x_1)>f(x_2), \quad\quad f(x_2)<f(x_3)$$
Essendo $f$ continua su $I$, sono continue anche le restrizioni di $f$ agli intervalli $[x_1,x_2]$ e $[x_2,x_3]$




