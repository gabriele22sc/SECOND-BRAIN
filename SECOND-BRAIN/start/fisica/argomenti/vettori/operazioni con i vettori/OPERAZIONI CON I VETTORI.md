
# Prodotto di uno scalare per un vettore

il prodotto di un vettore $\vec{a}$ per uno scalare $k$ ha come risultato un vettore $\vec{m}$:
$$\vec{m}=k\vec{a}$$
- Se $k>0$ il vettore $\vec{m}$ ha la stessa direzione e lo stesso verso del vettore $\vec{a}$ e modulo $m$ pari a $k$ volte il modulo di $\vec{a} \ (m=ka)$.
- Se $k<0$ il vettore $\vec{m}$ ha la stessa direzione, verso opposto del vettore $\vec{a}$ e modulo $m$ pari a $|k|$ volte il modulo di $\vec{a} \ (m=|k|a)$.

In particolare se $k=-1$, si ha $\vec{m}=-\vec{a}$. Il vettore $\vec{m}$ ha la stessa direzione e modulo di a, ma verso opposto; cioè come già detto, il vettore $\vec{m}$ è l'opposto del vettore $\vec{a}$.



![[operazione.jpg]]

# Prodotto scalare fra due vettori
$O_{x_0}=OP*cos\theta$   e   $O_{y_0}=OP*sen\theta$ 

$\frac{O_{y_0}}{O_{x_0}}=\frac{sen\theta}{cos\theta}=tan\theta$ 

## Prodotto scalare fra due vettori
$$\vec{A}*\vec{B}=|\vec{A}||\vec{B}|cos\theta_{ab}$$
![[prodotto-scalare-fra-due-vettori.jpg]]

## prodotto di a*b

$|a|cos\theta_{ab}|b|=a_b*b$ dove $a_b=|a|cos\theta_{ab}$

![[prodotto-di-ab.jpg]]

$A*B_a$
![[a-b_a.jpg]]

$$\begin{align}\hat{i}*\hat{i}=1 \\ \hat{j}*\hat{j}=1 \\ \hat{k}*\hat{k}=1\end{align}$$

$$\hat{i}*\hat{j}=0 \quad \hat{j}*\hat{k}=0$$

$$\vec{A}*\vec{B}=A_xB_x+A_yB_y+A_zB_z$$
esempio:    $\vec{A}=4\hat{i}$      $\vec{B}=-2\hat{i}+3\hat{j}$
$\vec{A}*\vec{B}=4*(-2)=-8$


# Prodotto vettoriale

$\vec{A}\times\vec{B}$ o $\vec{A}\wedge\vec{B}$     $:|\vec{A}\cdot\vec{B}|=|\vec{A}||\vec{B}|sen\theta_{ab}$


$\vec{A} \times \vec{B}=$ $\left| \begin{array}\hat{i} & \hat{j} & \hat{k} & \\ A_x & A_y & A_k \\ B_x & B_y & B_k \end{array} \right|$ $=(...)-(...)=$  



# Somma di vettori 

$a+b=c$   con  $c_x=a_x+b_x$   $c_y=a_y+b_y$ 
e poi $c=\sqrt{a^2+b^2}$ 

![[punta-coda-parallelogramma.jpg]]

## Metodo punta-coda

- Spostare un vettore mantenendolo sempre parallelo a se stesso finché la sua coda coincide con la punta dell’altro;
- Il vettore somma è il vettore la cui coda coincide con la coda del primo vettore e la cui punta coincide con la punta del secondo vettore.
![[punta-coda.png]]

## Metodo del parallelogramma

- Spostare un vettore mantenendolo sempre parallelo a se stesso finché la sua coda coincide con la coda dell’altro;
- Disegnare il parallelogramma avente per lati i due vettori così ottenuti. Il vettore somma è il vettore rappresentato dalla diagonale del parallelogramma e la cui coda coincide con la coda dei due vettori.
![[parallelogramma.png]]


## Proprietà commutativa della somma

$a+b=b+a$


![[somma.png]]

## Opposto di un vettore

![[opposto.png]]


# Differenza di vettori

![[differenza-dei-vettori.png]]

$\vec{c}=\vec{a}-\vec{b}$        $\vec{b}-\vec{a}=\vec{-c}$ 

$a+b=c$   con  $c_x=a_x-b_x$   $c_y=a_y-b_y$ 
e poi $c=\sqrt{a^2+b^2}$ 
![[diff2.png]]

# Prodotto scalare

Si definisce prodotto scalare tra due vettori lo scalare dato da:
$\vec{a}*\vec{b}=\vec{b}*\vec{a}=ab\ cos\ \phi$ 
dove $\phi$ è l'angolo acuto compreso tra i due vettori.
Nel caso di due angoli:   $a*b=|a|*|b|cos(\alpha-\beta)$

![[prodotto-scalare.png]]

*NB*: Il prodotto scalare può essere visto come il prodotto del modulo di un vettore per la componente dell'altro vettore nella direzione del primo vettore
![[componenti-vett.png]]


Le componenti di a su $\vec{x},\vec{y},\vec{z}$ sono la sua proiezione su quegli asse, quindi è il prodotto scalare di a per il versore di quell'asse:
$a_x=|a|*|\vec{x}|*cos\phi$     e      $a_y=|a|*|\vec{y}|*sin\phi$ 

## Altre formule del prodotto scalare

$$\vec{a}=(a_x,a_y) \quad \vec{b}=(b_x,b_y)$$

$$\vec{a}*\vec{b}=a_x*b_x+a_y*b_y$$

$$\vec{a}*\vec{b}=a*b \ cos \ \theta$$

$$\text{se} \ \vec{a} \perp \vec{b} \rightarrow \ \vec{a}*\vec{b}=0$$

# Prodotto vettoriale 
Due vettori possono essere moltiplicati fra loro in modo da produrre un nuovo vettore. Tale operazione viene detta prodotto **prodotto vettoriale**. Il prodotto vettoriale non gode della proprietà commutativa.
Dati due vettori $a$ e $b$, il loro , indicato come:
$\vec{c}=\vec{a}*\vec{b} \ \rightarrow \ c=a*b \ sen\phi$  

![[prodotto-vettoriale.png]]

ha per risultato un vettore $c$ che ha:
- modulo c uguale al prodotto aritmetico dei moduli (a e b) dei due vettori per il seno dell'angolo φ formato dai due vettori: $c = a*b \ sin φ$ 
- direzione perpendicolare al piano $γ$ individuato dai due vettori (nell’esempio γ coincide con il piano $xz$)
- verso tale che ad esso appaia levogiro (antiorario) il senso in cui deve ruotare nel piano γ il primo vettore per sovrapporsi al secondo vettore con una rotazione di ampiezza non superiore a 180°.

## Proprietà anti-commutativa

$$\vec{b}*\vec{a}=-(\vec{a}*\vec{b})$$

Per definizione di prodotto vettoriale si ha inoltre che:   $\vec{a}*\vec{a}=0$ 
![[tabella-vett.png]]

$$\vec{a}*\vec{b}=(a_yb_z-a_zb_y)\hat{x}+(a_zb_x-a_xb_z)\hat{y}+(a_xb_y-a_yb_x)\hat{z}$$

si può riscrivere sotto forma di:

$\vec{a}*\vec{b}= \begin{vmatrix} \hat{x}&\hat{y}&\hat{z}  \\ a_x&a_y&a_z \\ b_x&b_y&b_z \end{vmatrix} =$ $\hat{x} \begin{vmatrix} a_y&a_z \\ b_y&b_z \end{vmatrix}$ $+ \ \hat{y}\begin{vmatrix} a_z&a_x \\ b_z&b_x \end{vmatrix}$ $+ \ \hat{z}\begin{vmatrix} a_x&a_y \\ b_x&b_y\end{vmatrix}$ 

# Formule trigonometriche del triangolo rettangolo

$$\begin{cases}v_x=v \ cos(\theta) \\ v_y= v \ sen(\theta) \end{cases}$$
Potremmo indicare le componenti cartesiane per indicare $$\vec{v}=(v_x,v_y)$$
# Angoli in radianti

![[start/fisica/argomenti/vettori/operazioni con i vettori/radianti.jpeg]]
