[[GEOMETRIA]]
# Trovare il coefficiente angolare tramite i punti $A(x_1,y_1)$ $B(x_2,y_2)$

$$m_{ab}=\frac{y_2-y_1}{x_2-x_1}$$

# Condizioni di parallelismo tra due rette $r$ e $s$

Le rette sono parallele quando hanno lo stesso coefficiente angolare

$$m_r=m_s$$
1) Se abbiamo in forma esplicita:$$\begin{align}r:y=m_1x+q_1 \\ s:y=m_2x+q_2\end{align}$$
   allora:$$m_1=m_2$$
   se invece le due rette sono verticali, ovvero:$$\begin{align} r:x=x_1 \\ s:x=x_2\end{align}$$
   allora sono necessariamente parallele, perché per definizione sono parallele all'asse y.

2) se le due rette in forma implicita:$$\begin{align}r:a_1x+b_1y+c_1=0 \\ s:a_2x+b_2y+c_2=0\end{align}$$
   allora $r$ e $s$ sono parallele se e solo se:$$a_1b_2=a_2b_1$$
   per ricavare la condizione implicita di parallelismo basta ricordare la formula per il coefficiente angolare dall'equazione implicita di una retta:$$m_r=-\frac{a_1}{b_1}, \quad m_s=-\frac{a_2}{b_2}$$
   e imporre l'uguaglianza tra i coefficienti angolari:$$m_1=m_2 \quad\to\quad -\frac{a_1}{b_1}=-\frac{a_2}{b_2} \quad\to\quad a_1b_2=a_2b_1$$

## Esempi
Le rette $r:y=3x+6$ e $s:y=3x-8$ sono parallele poiché presentano lo stesso coefficiente angolare:$$m_r=3=m_s$$
oppure le rette $t:-x+2y+1=0$ e $u:-5x+10y=0$ sono parallele, infatti se applichiamo la formula per il coefficiente angolare in forma implicita avremo:$$m_t=-\frac{a}{b}=-\frac{-1}{2}=\frac{1}{2} \qquad\qquad m_y=-\frac{a}{b}=-\frac{-5}{10}=\frac{1}{2}$$
in alternativa possiamo utilizzare la formula per la condizione implicita di parallelismo:$$a_1b_2=(-1)\cdot10=-10=(-5)\cdot2=a_2b_1$$



# Condizioni di perpendicolarità tra due rette $r$ ed $s$
La condizione di perpendicolarità tra due rette nel piano cartesiano stabilisce che due rette sono perpendicolari se e solo se i coefficienti angolari sono **l'uno il reciproco dell'opposto dell'altro**.
Se indichiamo le due rette $r$ e $s$, possiamo esprimere la perpendicolarità con il simbolo $\perp$ e scrivere $r\perp s$.
$$m_r=-\frac{1}{m_s} \quad oppure \quad m_r*m_s=-1$$

1) Se le due rette sono in forma esplicita, la condizione di perpendicolarità si esprime con la formula$$m_1=-\frac{1}{m_2}$$
   in alternativa, e in modo equivalente, sono perpendicolari se e solo se il prodotto tra i due coefficienti angolari è uguale a $-1$:$$m_1m_2=-1$$
2) Riferendoci alla forma implicita, è facile vedere che la condizione di perpendicolarità equivale a:$$a_1a_2+b_1b_2=0$$
   per capirlo ci basta riscrivere la condizione esplicita, servendoci della formula per il coefficiente angolare dell'equazione implicita:$$m_1=-\frac{a_1}{b_1}, \quad\quad m_2=-\frac{a_2}{b_2}$$
   e quindi:$$m_1m_2=-1 \quad\to\quad (-\frac{a_1}{b_1})(-\frac{a_2}{b_2}) \quad\to\quad a_1a_2+b_1b_2=0$$

## Esempi

1) Le rette $r:y=-5x+12$ e $s:y=\frac{x}{5}-\frac{6}{7}$ sono perpendicolari, infatti:$$m_rm_s=(-5)\cdot \frac{1}{5}=-1$$
2) Le rette $t:4x+3y=0$ e $u:-6x+8y+5=0$ sono perpendicolari, infatti:$$a_1a_2+b_1b_2=4\cdot(-6)+3\cdot8=-24+24=0$$


# Condizione di ortogonalità

Se $a=0$ e $b\neq0$ la retta sarà parallela all'asse $x$ ($y=-\frac{c}{b}$)

Se $a\neq0$ e $b=0$ allora è una retta parallela all'asse $y$ ($x=-\frac{c}{a}$) 


# Punto in comune tra due rette

$$\begin{cases}ax+by+c=0 \\ a'x+b'y+c'=0\end{cases}$$
# Classificazione generale dei sistemi lineari in due incognite:

- **DETERMINATO** $\rightarrow$ ha una sola soluzione $\rightarrow$ le rette si intersecano in un punto $m_{r1}\neq m_{r2}$;
- **IMPOSSIBILE**  non ha soluzioni $\rightarrow$ le rette sono parallele e distinte  *es. quando 0=5* ;
- **INDETERMINATO** $\rightarrow$ ha infinite soluzioni $\rightarrow$ le rette coincidono *es. quando 0=0*.

![[posizione-reciproca-tra-due-rette.jpeg]]



# Formulario


![[1.jpg]]
![[2.jpg]]
![[3.jpg]]
![[4.jpg]]
![[5.jpg]]
![[6.jpg]]
![[7.jpg]]
![[8.jpg]]
![[9.jpg]]
![[10.jpg]]
![[riepilogo.jpg]]
![[circonferenza1.jpg]]
![[circonferenza2.jpg]]
![[circonferenza3.jpg]]
![[retta tan.jpg]]
