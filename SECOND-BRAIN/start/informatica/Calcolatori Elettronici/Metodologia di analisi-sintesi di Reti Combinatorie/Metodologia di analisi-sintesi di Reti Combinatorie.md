# Forma Minima e Irriducibile
Una espressione che non è ulteriormente semplificabile si dice irriducibile
## Teorema
Data una funzione $F$, ogni forma irridondante data come somma di prodotti è somma di primi implicanti(per ottenere una forma minima, è necessario determinare i primi implicanti).

Prendiamo: $F=\bar{x}y\bar{z}+\bar{x}\bar{y}\bar{z}+x\bar{y}\bar{z}+\bar{x}yz+xyz+x\bar{y}z$ 

### Forma irriducibile
$F=\bar{x}\bar{z}+\bar{y}\bar{z}+yz+xz$
![[Pasted image 20260307160134.png]]

### Forma minima
$F=\bar{x}\bar{z}+x\bar{y}+yz$
![[Pasted image 20260307160638.png]]
Con la **regola della selezione**

La Forma Minima ha un significato grazie al criterio di costo adottato. Ecco i tre criteri di costo classici costituiti da 5 punti:
1. Data una funzione $F(x,y,z,…w)$ trovare il circuito, o uno fra i possibili circuiti, tale che:
	1. Esso sia rappresentato come somma di prodotti o come prodotto di somme;
	2. Ogni variabile di ingresso può essere collegata contemporaneamente ad un numero non limitato di circuiti elementari. In realtà questo non è possibile, perché nessun circuito può alimentare infiniti carichi in parallelo. Il <u>fan-out</u> è il numero massimo di circuiti elementari cui ogni variabile di ingresso può collegarsi.
	3. Ogni porta logica AND o OR può accettare un numero non limitato di variabili di ingresso. Ciò non è fisicamente realizzabile. Il <u>fan-in</u> è il numero massimo di variabili di ingresso relative ad una porta.
	4. In ingresso sono disponibili contemporaneamente le variabili dirette e complementate;
	5. Il numero complessivo degli AND e OR sia minimo.
2. Data una funzione $F(x,y,z,…w)$ trovare il circuito, o uno fra i possibili circuiti, tale che:
	1. Tutti e 4 i passaggi del primo criterio
	2. Il numero totale degli ingresso ai circuiti AND e OR sia minimo.
3. Data una funzione $F(x,,y,z,…w)$ trovare il circuito, o uno fra i possibili circuiti, tale che:
	1. Tutti e 4 i passaggi del primo criterio;
	2. Il numero dei letterali sia minimo. Riducendo i letterali diminuiscono i collegamenti e quindi la complessità dei circuiti.

# Sintesi Reti Combinatorie: approccio gerarchico
Un circuito combinatorio consiste di $m$ variabili di ingresso ed $n$ variabili di uscita. Ogni variabile di ingresso e di uscita esiste fisicamente come segnale binario(1/0). Per $n$ variabili di ingresso si hanno $2^n$ combinazioni.
Quindi un circuito combinatorio può essere specificato tramite la tabella di verità elencando i valori di uscita in corrispondenza alle combinazioni degli ingressi.

Un circuito è composto da porte logiche interconnesse. Il circuito risulterebbe molto confuso, per questo si utilizza il metodo dei blocchi, si spezza il circuito in blocchi e si interconnettono questi tra loro. La **funzione** e l’**interfaccia** del blocco sono specificate.

## Design Hirarchy: disegno Gerarhico
La struttura gerarchica può essere rappresentata con un albero con *root* in cima e le foglie sono i NAND gate. I NAND sono necessari per implementare la funzione dispari a 9 ingressi sono 32.
I blocchi NAND vengono detti blocchi primitivi.
Il punto di forza della tecnica gerarchica è quello di creare un blocco poterlo riusare nel circuito.
Un blocco usato in più punti è detto istanza del blocco.
**Top-Down Design**: significa partire dall’alto e costruirei blocchi sino ad arrivare a quelli primitivi. Spesso è necessario usare contemporaneamente un approccio bottom-up.

## Analisi di una Rete Combinatoria
L’analisi di un circuito combinatorio consiste nel determinare la funzione che il circuito implementa.
L’analisi inizia con il diagramma logico dato e termina con una tabella di verità o una funzione booleana. Prima di fare l’analisi si deve essere sicuri del tipo di circuito, in un circuito combinatorio non abbiamo i feed-back o elementi di memoria: le uscite dipendono solo dagli ingressi.
### Funzione Booleana
Per ottenere la funzione Booleana di uscita a partire dallo schema logico, si deve procedere come segue:
1. Etichettare tutte le porte di uscita che sono solo funzioni delle variabili di ingresso con simboli arbitrari. Determinare la funzione booleana per ogni porta di uscita.
2. Etichettare le porte che sono funzioni delle variabili di input e delle porte precedentemente etichettate. Trovare la funzione booleana per questi gate di uscita.
3. Ripetere il passo 2 imo a che si ottiene l’uscita in termini delle sole variabili di ingresso. Semplificare tramite manipolazioni algebriche o mappe.
Esempio:
![[Pasted image 20260307172649.png]]
	1) Etichettiamo i gate T1 e T2; determiniamo le funzioni booleane per T1 e T2:$$T1=\bar{B}C\quad\quad T2=\bar{A}B$$
	2) Etichettiamo gli output secondo la regola 2. Calcoliamo le funzioni booleane di T3,T4,T5:$$\begin{align}T_3=A+T_1=A+\bar{B}C \\ T_4=T_2\oplus D=\bar{A}B\bar{D}+AD+\bar{B}D \\ T_5=T_2+D=\bar{A}B+D\end{align}$$
	3) Ripetiamo il passo 2 ottenendo $$\begin{align}F_1=T_3+T_4=A+\bar{B}C+B\bar{D}+\bar{B}D \\ F_2=T_5=\bar{A}B+D\end{align}$$
Oltre ad ottenerla a partire dalla rappresentazione analitica della funzione, possiamo ottenerla: 
- 1 determinare il numero di variabili in input nel circuito. Per n input si devono elencare le $2^n$  combinazioni possibili;
- 2 rompere il circuito in piccoli blocchi con una singola uscita ed etichettare ogni uscita del blocco con simboli arbitrari;
- 3 ottenere la tabella di verità dei blocchi con funzioni che dipendono dalle sole variabili di ingresso;
- 4 procedere per ottenere la tabella di verità dei blocchi i cui input dipendono dagli output precedentemente etichettati, procedere finché tutte le colonne non sono determinate per tutto il circuito.
# Procedura di sintesi di una Rete Combinatoria
1. A partire dalla descrizione verbale del circuito, determinare gli ingressi e ele uscite richieste;
2. Costruzione della tabella di verità;
3. Individuazione dei mintermini;
4. Costruzione della mappa di Karnaugh;
5. Individuazione dei primi implicanti;
6. Individuazione dei primi implicanti essenziali;
7. Selezione degli altri primi implicanti secondo la regola di selezione;
8. Diagramma circuitale.
9.  Verifica della correttezza.

Progettare un circuito combinatorio con tre ingressi e una uscita. L’output deve avere valore logico 1 quando il valore degli ingressi è minore di 011(3) e valore logico 0 altrimenti usare solo NAND gate.

# Convertitore
Quando il circuito combinatorio ha più uscite , ogni una di esse deve essere espressa separatamente come una funzione di tutte le variabili in ingresso. Un esempio di circuito con più uscite è il convertitore di codice. Esempio: 7 segmenti

