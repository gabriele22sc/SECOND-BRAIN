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
