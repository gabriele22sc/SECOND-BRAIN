# Definizione di derivata
Siano $f:DOMf\to\mathbb{R}$ una funzione e $x_0\in DOMf$ un punto interno a $DOMf$. La funzione $f$ si definisce derivabile in $x_0$ se esiste finito il limite$$\lim_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}$$
In tal caso tale limite verrà indicato con uno dei simboli$$f’(x_0),\quad Df(x_0),\quad \frac{df}{dx},\quad f(x_0)$$
E verrà chiamato derivata(prima) di $f$ in $x_0$.


## Rapporto incrementale
Sì dice rapporto incrementale di $f$ in $x_0$ ed è definito in $DOMf \textbackslash\{x_0\}$. Questo rapporto rappresenta la variazione relativa di $f$ rispetto a quella della variabile indipendente $x$ nel passare da $x_0$ a $x$.
Il limite di tale rapporto incrementale, se esiste in $\mathbb{R}$, è la derivata prima di $f$ in $x_0$. Se il limite è $+\infty$ oppure $-\infty$ o non esiste, allora $f$ **non è derivabile** in $x_0$.

$$\lim_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0} \quad\quad=\quad\quad \lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}$$
![[rapporto-incrementale.png]]

Se $A\subseteq DOMf$ si dice che $f$ è derivabile in $A$ se $f$ è derivabile in ogni punto di $A$.
In tal caso è definita una funzione, detta **funzione derivata prima** di $f$ denotata con $f’$.

## Interpretazione geometrica
![[interpretazione-geometrica.png]]

Sia $h>0$ e consideriamo i punti $P_0(x_0,f(x_0))$ e $P_h(x_0+h,f(x_0+h))$. 
Il rapporto incrementale $\frac{f(x_0+h)-f(x_0)}{h}$ è il coefficiente angolare della retta passante per $P_0$ e $P_h$. Questa coincide con la retta tangente dell’angolo $\alpha_h$ che tale retta forma con l’asse delle ascisse. La sua equazione è:$$r_h:y=f(x_0)+\frac{f(x_0+h-f(x_0))}{h}(x-x_0)$$
## Interpretazione cinematica
Guarda slide “1° parte Calcolo Differenziale”






# Legame tra continuità e derivabilità
Siano $f:DOMf\to\mathbb{R}$ una funzione e $x_0\in DOMf$ un punto interno a $DOMf$. Sì supponga che $f$ sia derivabile in $x_0$. Allora $f$ continua in $x_0$.

## Dimostrazione
Dal momento che $x_0$ è un punto interno al dominio di $f$, ha senso calcolare $\lim_{x\to x_0}f(x)$. Quindi, per provare che $f$ è continua in $x_0$, dimostriamo che:$$\lim_{x\to x_0}f(x)=f(x_0)$$
Cioè che:$$\lim_{x\to x_0}(f(x)-f(x_0))=0$$
Moltiplicando e dividendo per $x-x_0$ si ha che: $$\lim_{x\to x_0}(f(x)-f(x_0))=\lim_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}\cdot(x-x_0)=0$$
Quindi $f$ continua in $x_0$.
Se una funzione è **derivabile** allora sarà **continua** mentre il contrario non è vero.



# Derivate delle funzioni elementari

1) $f(x)=c,c\in\mathbb{R}\quad\to\quad f’(x)=0,\forall \in\mathbb{R}$ avendo $x_0\in\mathbb{R}$ avremo:$$\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}=\lim_{h\to0}\frac{c-c}{h}=\lim_{h\to0}0=0$$
2) $f(x)=x^n,n\in\mathbb{N} \quad\to\quad f’(x)=nx^{n-1},\forall x\in\mathbb{R}$ (con la convenzione che $0^0=1$). Per $n\geq1$ 
Se $x_0=0$ allora $$\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}=\lim_{h\to0}\frac{h^n}{h}=\lim_{h\to0}h^{n-1}=$$
$$\begin{cases}1 \quad\text{se n}=1 \\ 0 \quad\text{se n}\geq2\end{cases}$$
Se $x_0\neq0$, allora$$\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}=\lim_{h\to0}\frac{(x_0+h)^n-x_0^n}{h}=\lim_{h\to0}\frac{x_0^n(1+\frac{h}{x_0})^n-x_0^n}{h}=\lim_{h\to0}x_0^{n-1}\frac{(1+\frac{h}{x_0})^n-1}{\frac{h}{x_0}}=nx^{n-1}_0$$
3) In generale $f(x)=x^{\alpha},\alpha\in\mathbb{R} \quad\to\quad f’(x)=\alpha x^{\alpha-1}$, per tutti i valori di $x\in DOMf$ per i quali ha senso $f’(x)$
4) $f(x)=a^x,a>0 \quad\to\quad f’(x)=a^xlna,\forall x\in\mathbb{R}$ infatti, se $x_0\in\mathbb{R}$, si ha:$$\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}=\lim_{h\to0}\frac{a^{x_0+h}-a^{x_0}}{h}=\lim_{h\to0}a^{x_0}\frac{a^h-1}{h}=a^{x_0}lna$$
5) $f(x)=senx \quad\to\quad f’(x)=cosx,\forall x\in\mathbb{R}$ infatti se $x_0>0$ si ha $$\lim_{h\to0}\frac{f(x_0+h)-f(x_0)}{h}=\lim_{h\to0}\frac{sen(x_0+h)-senx_0}{h}=$$ $$\lim_{h\to0}\frac{senx_0cosh+senhcosx_0-senx_0}{h}=\lim_{h\to0}senx_0\frac{cosh-1}{h}+cosx_0\frac{senh}{h}=\lim_{h\to0}-(senx_0\frac{1-cosh}{h}+cosx_0\frac{senh}{h})$$
6) $f(x)=cosx \quad\to\quad f’(x)=-senx,\forall x\in\mathbb{R}$ si procede come nel caso prima.

# Derivate laterali
Siano $f:DOMf\to\mathbb{R}$ una funzione, $x_0\in DOMf$ e $\varepsilon>0$ tale che $[x_0,x_0+\varepsilon[\subseteq DOMf$.
Si dice che $f$ è derivabile da destra in $x_0$ se esiste finito:$$\lim_{x\to x_0^+}\frac{f(x)-f(x_0)}{x-x_0}$$
Viene denotato come $f’_+(x_0)$ o $D^+f(x_0)$, e si chiama **derivata destra** di $f$ in $x_0$. 

Se esiste $\varepsilon>0$ tale che $]x_0-\varepsilon,x_0[\subseteq DOMf$, si dice che $f$ è derivabile da sinistra in $x_0$ se esiste finito:$$\lim_{x\to x_0^-}\frac{f(x)-f(x_0)}{x-x_0}$$
In tal caso questo limite si denota con $f’_-(x_0)$ o $D^-f(x_0)$, e si chiama **derivata sinistra** di $f$ in $x_0$. 
Entrambe le derivate(sinistra e destra), sono dette **derivate laterali**.
1. Le derivate laterali esistono solo se il limite laterale esiste finito. In caso contrario(limite che non esiste oppure che risulta $+\infty$ o $-\infty$ ), allora la derivata non esiste.
2. Se $f$ è definita per $x\geq x_0$ e non per $x<x_0$, allora non si può parlare di derivabilità ma di derivabilità da destra.






# Legame fra la derivata e le derivate laterali
Siano $f:DOMf\to\mathbb{R}$ una funzione e $x_0\in DOMf$ un punto interno a $DOMf$. Si supponga che esistano le derivate laterali $f’_+(x_0)$ e $f’_-(x_0)$.
Allora, $f$ è continua in $x_0$. Inoltre, $f$ è derivabile in $x_0$ se e solo se $f’_+(x_0)=f’_-(x_0)$ e in tal caso $f’(x_0)=f’ _+(x_0)=f’ _-(x_0)$.


# Algebra delle derivate 
Nota: regole a memoria, dimostrazioni a piacere

Siano $f:DOMf\to\mathbb{R}$ e $g:DOMg\to\mathbb{R}$ due funzioni derivabili in $x_0$, punto interno a $DOMf\cap DOMg$. Allora:
1. $f+g$ è derivabile in $x_0$ e si ha che:$$(f+g)’(x_0)=f’(x_0)+g’(x_0)$$
2. $fg$ è derivabile in $x_0$ e si ha che:$$(fg)’(x_0)=f’(x_0)g(x_0)+f(x_0)g’(x_0)$$
3. Se $f(x_0)\neq0$, allora $\frac{1}{f}$ è derivabile in $x_0$ e si ha che:$$(\frac{1}{f})’(x_0)=-\frac{f’(x_0)}{[f(x_0)]^2}$$
4. Se $g(x_0)\neq0$, allora $\frac{f}{g}$ è derivabile in $x_0$ e si ha che:$$(\frac{f}{g})’(x_0)=\frac{f’(x_0)g(x_0)-f(x_0)g’(x_0)}{[g(x_0)]^2}$$
### Dimostrazione(Da fare)
Abbiamo:$$\lim_{x\to x_0}\frac{f(x)-f(x_0)}{x-x_0}=f’(x_0)\in\mathbb{R},\quad\quad\quad \lim_{x\to x_0}\frac{g(x)-g(x_0)}{x-x_0}=g’(x_0)\in\mathbb{R}.$$
1. Si ha:![[Di-algebra-derivate1.jpg]]
Quindi $f+g$ è derivabile in $x_0$ e si ha:$$(f+g)’(x_0)=f’(x_0)+g’(x_0)$$
2. Dato che $g$ derivabile in $x_0$, risulta che $g$ è continua in $x_0$, dunque:$$\lim_{x\to x_0}g(x)=g(x_0)$$
Tenendo conto di ciò e delle ipotesi di derivabilità di $f$ e $g$ in $x_0$, si ha:![[D-algebra-derivate2.jpg]]

Quindi $fg$ è derivabile in $x_0$ e si ha:$$(fg)’(x_0)=f’(x_0)g(x_0)+f(x_0)g’(x_0)$$
3. Osservando che essendo $f$ derivabile in $x_0$, risulta che $f$ è continua in $x_0$, dunque:$$\lim_{x\to x_0}f(x)=f(x_0)$$ Dal fatto che $f(x_0)\neq0$ e delle ipotesi di derivabilità di $f$ e $g$ in $x_0$, si ha:![[Dimostrazione-algebra-derivate3.jpg]]
Quindi $\frac{1}{f}$ è derivabile in $x_0$ e si ha:$$(\frac{1}{f})’(x_0)=-\frac{f’(x_0)}{[f(x_0)]^2}$$
4. Segue immediatamente dalle regole 2., 3. non appena hai:$$\frac{f(x_0)}{g(x_0)}=f(x_0)\cdot\frac{1}{g(x_0)}$$
