Come riconosciamo un numero positivo da uno negativo?
- Positivo $\to$ bit più significativo 0
- Negativo $\to$ bit più significativo 1


# Primo metodo complemento a due
$$\begin{align}00100011_2=35_{10} \\ \downarrow\quad\quad\quad \\ 11011100+ \\1= \\ ----- \\ 11011101 \quad\end{align}$$
Basta aggiungere 1 al primo bit da destra

# Secondo metodo complemento a due
Il metodo più semplice è quello di partire a scrivere il nostro numero in binario:
$35_{10}=00100011_2$ 
successivamente iniziamo ad invertire tutti i nostri  numeri a partire dal primo uno:
$11011101_2 = -35_{10}$ 
