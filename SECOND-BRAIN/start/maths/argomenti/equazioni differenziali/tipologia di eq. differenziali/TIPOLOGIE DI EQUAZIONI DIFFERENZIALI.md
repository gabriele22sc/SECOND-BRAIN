# Equazioni differenziali ordinarie di ordine $n$
Si chiama equazione differenziale ordinaria di ordine $n$ un'equazione della forma:$$F(x,y,y',y'',...,y^n)=0$$
dove $F$ è definita in un insieme di $A$ di $\mathbb{R}^{n+2}$.
$y=y(x)$ è la funzione incognita, $y',y'',y''',...,y^n$ le sue derivate.
Quindi $y(x)$ è soluzione di $(1)$ se $y(x)$ e le sue derivate soddisfano l'equazione $(1)$, dove $y:I\to\mathbb{R}$ è una funzione derivabile $n$ volte sull'intervallo $I$ e $x\in I$.
Diciamo che l'equazione differenziale è in forma normale se è della forma $$y^n=f(x,y,y',y'',...,y^n-1)$$
dove $f:A\to\mathbb{R}$ con $A$ insieme di $\mathbb{R}^{n+1}$.
Si dice che una funzione $\tilde{y}:I\to\mathbb{R}$ è una soluzione (o integrale) dell'equazione differenziale ordinaria $(1)$ se:
- $\tilde{y}$ è derivabile in $I$;
- $(x,\tilde{y}(x),\tilde{y'}(x),\tilde{y''}(x),...,\tilde{y^n}(x))\in A$ per ogni $x\in I$;
- $F(x,\tilde{y}(x),\tilde{y'}(x),\tilde{y''}(x),...,\tilde{y^n}(x))=0$ per ogni $x\in I$.

### Ad esempio
$$y'=f(x)$$
È del primo ordine, perché la derivata di ordine massimo della funzione incognita che compare è la derivata prima.


# Soluzione di un problema di Cauchy 
Siano $A\subseteq\mathbb{R}^{x+1}$ non vuoto, $I\subseteq\mathbb{R}$ un intervallo, $f:A\to\mathbb{R}$ una funzione e $(x_0,y_0,y_1,...,y_{n-1})\in A$. Si dice che una funzione $y:I\to\mathbb{R}$ è una **soluzione del problema di Cauchy**(o problema dei valori iniziali):
![[Pasted image 20260513100801.png]]

se $y(x)$ è una soluzione di $y^n=f(x,y,y',y'',...,y^{n-1}),x_0\in I$ e $y(x_0)=y_0,y'(x_0)=y_1,...,y^{n-1}(x_0)=y_{n-1}$; queste ultime uguaglianze vengono anche chiamate condizioni iniziali.

# Equazioni differenziali ordinarie del primo ordine in forma normale 
Siano $A\subseteq\mathbb{R}^2$ non vuoto, $I\subseteq\mathbb{R}$ un intervallo e $f:A\to\mathbb{R}$ una funzione. Una equazione differenziale ordinaria del primo ordine in forma normale è una equazione del tipo$$y'=f(x,y)$$
Si dice che una funzione $y:I\to\mathbb{R}$ è una soluzione(o un integrale) dell'equazione differenziale ordinaria del primo ordine $y'=f(x,y)$ se:
- $y$ è derivabile in $I$;
- $(x,y(x))\in A$ per ogni $x\in I$;
- $y'(x)=f(x,y(x))$ per ogni $x\in I$.

# Soluzione di un problema di Cauchy
Siano $A\subseteq\mathbb{R}^2$ non vuoto, $I\subseteq\mathbb{R}$ un intervallo, $f:A\to\mathbb{R}$ una funzione e $(x_0,y_0)\in A$. Si dice che una funzione $y:I\to\mathbb{R}$ è una soluzione del problema di Cauchy$$\begin{cases}y'=f(x,y) \\ y(x_0)=y_0\end{cases}$$
se $y$ è una soluzione di $y'=f(x,y),x_0\in I$ e $y(x_0)=y_0$

# Equazioni differenziali a variabili separabili
Siano $I,J\subseteq\mathbb{R}$ due intervalli, $f:I\to\mathbb{R}$ e $g:I\to\mathbb{R}$ due funzioni continue. Una equazione differenziale a variabili separabili è una equazione differenziale del primo ordine del seguente tipo$$y'=f(x)g(y)$$
# Teorema dell'esistenza e unicità della soluzione massimale
Siano $I,J\subseteq\mathbb{R}$ due intervalli, $f:I\to\mathbb{R}$ e $g:J\to\mathbb{R}$ due funzioni, $x_0 \in I$ e $y_0\in J$. Supponiamo che $f$ sia continua in $I$ e $g$ sia derivabile con derivata continua in $J$. 
Allora esiste una ed una sola soluzione massimale del problema di Cauchy$$\begin{cases}y'=f(x)g(y) \\ y(y_0)=y_0\end{cases}$$
definita su un intervallo contenente $x_0$ e contenuto in $I$.

# Equazioni differenziali lineari del primo ordine
Siano $I\subseteq\mathbb{R}$ un intervallo e $a,b:I\to\mathbb{R}$ due funzioni continue. Una equazione differenziale lineare del primo ordine in forma normale è un equazione differenziale del tipo$$y'=a(x)y+b(x)$$
# Teorema di esistenza e unicità della soluzione massimale
Siano $I\subseteq\mathbb{R}$ un intervallo, $a,b:I\to\mathbb{R}$ due funzioni continue, $x_0\in I$ e $y_0\in\mathbb{R}$. 
Allora esiste una e una sola soluzione massimale del problema di Cauchy $$\begin{cases}y'=a(x)y+b(x) \\ y(x_0)=y_0\end{cases}$$
definita nell'intervallo $I$.

# Equazione differenziale lineare del secondo ordine a coefficienti costanti
Siano $I\subseteq\mathbb{R}$ un intervallo, $a,b,c\in\mathbb{R}$ con $a\neq0$ e $f:I\to\mathbb{R}$ una funzione continua. Una equazione differenziale lineare del secondo ordine a coefficienti costanti è una equazione differenziale di questo tipo:$$(E):ay''+by'+cy=f(x)$$
Se $f=0$ l'equazione è detta omogenea, altrimenti non omogenea.

# Equazione caratteristica
Siano $a,b$ e $c$ tre numeri reali, con $a\neq0$. Si consideri l'equazione:$$(E_0):ay''+by'+cy=0$$
la funzione polinomiale definita da:$$P(\lambda)=a\lambda^2+b\lambda+c$$
si dice *polinomio caratteristico associato a $(E_0)$*.
L'equazione $P(\lambda)=a\lambda^2+b\lambda+c=0$ è detta *equazione caratteristica associata a $(E_0)$*.

# Teorema per la risoluzione in $\mathbb{R}$ dell'equazione $ay''+ay'+cy=0$
Siano $a,b$ e $c$ numeri reali, con $a\neq0$. 
Sia $(E_0):ay''+ay'+cy=0$ e sia il $\Delta$ discriminante dell'equazione caratteristica $a\lambda^2+b\lambda+c=0$:

1. Se $\Delta>0$, l'equazione caratteristica ammette due radici reali distinte $r_1$ e $r_2$ e le soluzioni di $(E_0)$ su $\mathbb{R}$ sono le funzioni $y:\mathbb{R}\to\mathbb{R}$ definite da: $$y(x)=Ae^{r_1x}+Be^{r_2x}, \quad\quad A,B\in\mathbb{R}$$
2. Se $\Delta=0$, l'equazione caratteristica ammette una sola radice reale $r_0$(si tratta di una radice avente molteplicità 2) e le soluzioni di $(E_0)$ su $\mathbb{R}$ sono le funzioni $y:\mathbb{R}\to\mathbb{R}$ definite da: $$y(x)=(A_x+B)e^{r_0x}, \quad\quad A,B\in\mathbb{R}$$
3. se $\Delta<0$ l'equazione caratteristica ammette due radici complesse coniugate $r_1=\alpha+i\beta$(con $\beta\neq0$) e le soluzioni di $(E_0)$ su $\mathbb{R}$ sono le funzioni $y:\mathbb{R}\to\mathbb{R}$ definite da $$y(x)=e^{\alpha x}(Acos(\beta x)+Bsen(\beta x)), \quad\quad A,B\in\mathbb{R}$$
# Teorema di esistenza e unicità della soluzione massimale
Siano $a,b,c$ numeri reali, con $a\neq0$. Sia $x_0$ un numero reale. Siano, infine, $y_0$ e $y_1$ due numeri reali assegnati. Allora una ed una soluzione massimale del problema di Cauchy
![[Pasted image 20260514002944.png]]
definita in $\mathbb{R}$


# Teorema 
Siano $I\subseteq\mathbb{R}$ un intervallo, $a,b,c\in\mathbb{R}$ con $a\ne0$ e $f:I\to\mathbb{R}$ una funzione continua.
Sia $(E):ay''+by'+cy=f(x)$ e sia $(E_0):ay''+vy'+cy=0$.
Allora l'integrale generale dell'equazione differenziale lineare del secondo ordine a coefficienti costanti non omogenea $(E)$ è dato da $$y=y_0+y_{p'}$$
dove $y_0$ è l'integrale generale dell'equazione omogenea associata $(E_0)$ e $y_p$ è un integrale particolare dell'equazione non omogenea $(E)$

# Teorema del principio di sovrapposicione
Siano $I\subseteq\mathbb{R}$ un intervallo $a,b,c\in\mathbb{R}$ con $a\neq0,n\in\mathbb{N}$ e $f_1,...f_n:I\to\mathbb{R}$ funzioni continue.
Allora un integrale particolare dell'equazione differenziale lineare del secondo ordine a coefficienti costanti non omogenea $ay''+by'+cy=f_1(x)+...+f_n(x)$ è dato da $$y=y_1+...+y_n$$
dove $y_k$ è un integrale particolare dell'equazione non omogenea $$ay''+by'+cy=f_k(x)$$
per ogni $k=1,...,n$



# Teorema dell'esistenza e unicita della soluzione massimale
Siano $a,b,c$ numeri reali, con $a\neq0$. Siano, inoltre, $I\subseteq\mathbb{R}$ un intervallo $f:I\to\mathbb{R}$ una funzione continua, $x_0\in I$ e $y_0,y_1\in\mathbb{R}$. Allora esiste una ed una soluzione massimale del problema di Cauchy
![[Pasted image 20260514003957.png]]
definita in $I$.

