# Link
[[Passaggi fondamentali]]
# Definizione

Data una funzione $f(x)$, continua in $[a;b]$, l'**integrale definito** esteso all'intervallo $[a;b]$ è il valore del limite per $\Delta x_{\text{max}}$ che tende a 0 della somma: 
$$
\int_{a}^{b} f(x) \,dx = \lim_{\Delta x_{\text{max} \to 0} }S
$$

$b$ -> estremo superiore;
$a$ -> estremo inferiore;
$f(x)$ -> funzione integranda.

A differenza dell'integrale indefinito(insieme di funzioni), l'**integrale definito è un numero reale** e <u>non dipende</u> dalla variabile $x$.


# Teorema di Torricelli-Barrow

Permette di collegare l'integrale definito a quello di integrale indefinito, attraverso la funzione integrale. chiamato anche:
### Teorema fondamentale del calcolo integrale
Se una funzione $f(x)$ è continua in $[a;b]$, allora esiste la derivata della sua funzione integrale: $F(x)=\int_{a}^{x} f(t) \,dt$
per ogni punto $x$ dell'intervallo $[a;b]$ ed è uguale a $f(x)$, cioè:
$F'(x)=f(x)$
ovvero $F(x)$ è una primitiva di $f(x)$.


# 2° Teorema di Guldino

$V_\text{solido di rotazione}=\pi\int_{a}^{b} f^2(x)dx$