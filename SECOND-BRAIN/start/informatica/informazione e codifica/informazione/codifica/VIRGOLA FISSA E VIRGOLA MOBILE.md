
# Virgola fissa

Data una base B, si assegnano:
- n cifre per rappresentare la parte intera;
- m cifre per rappresentare la parte frazionaria

In base $B=2$, abbiamo quindi $m+n$ bit per parte intera e frazionaria

ad esempio: $23,625_{10}=???_2$ 

la parte sinistra viene scomposta per 2:
$23/2=11$ resto 1
$11/2=5$ resto 1
$5/2=2$ resto 1
$2/2=1$ resto 0
$1/2=0$ resto 1
$00010111_2$

mentre la parte destra va moltiplicata per due otto volte:
$0,625*2=1,25$ parte intera 1
$0,25*2=0,50$ parte intera 0
$0,50*2=1$ parte intera 1
$10100000_2$

quindi avremo: $00010111,10100000$


poi per eseguire la prova nella parte intera basta moltiplicare per 2:
$$\begin{align}0\ 0\ 0\ 1\ 0\ 1\ 1\ 1\ \\ 2^7\ 2^6\ 2^5\ 2^4\ 2^3\ 2^2\ 2^1\ 2^0 \\
16+4+2+1\end{align}$$


# Virgola mobile

Un numero reale R può essere scritto in base B come:
$$R=\pm m*B^e$$
- m = mantissa
- e = esponente
- B = base

ad esempio avendo:
$10_{10}$ in binario $1010_2$
scrivendola in forma normalizzata spostiamo la virgola dopo il primo 1:
$1010_2=1,010*2^3$
perché
$1,010_2*2^3=1*2^3+0*2^2*1+2^1+0*2^0=8+0+2+0=10$ 