I circuiti logici sono componenti hardware che manipolano informazioni binarie. I circuiti di base vengono chiamati Porte Logiche(logical gate).

## Scopo
Quello di descrivere i comportamenti dei circuiti digitali si può usare una algebra che specifica l’operazione di ogni porta e permette di analizzare e sintetizzare il circuito

L’Algebra Booleana può assumere due valori: 1 e 0(true o false), le variabili vengono indicate con A,B,C,X,Y,W,Z e le operazioni sono AND($\cdot$), OR(+), NOT($\bar{\phantom{x}}$ o ‘);
## Tabelle di verità 
Gli operatori AND, OR e NOT sono definiti mediante tabelle di verità


## Circuiti Elettronici
Sono sistemi caratterizzati da grandezze fisiche(segnali) che assumono due gamme distinte di livelli logici H(alto) ed L(basso). L’associazione tra livelli di tensione e livelli logici può essere fa con logica positiva e negativa.

## Porte Logiche
Le porte logiche sono circuiti elettronici che realizzano le operazioni logiche elementari.
- Operano su più segnali di ingresso e producono un segnale di uscita;
- Rispondono a due valori di rango di tensioni che sono associati ai valori logici 0 e 1.
![[Pasted image 20260217220912.png]]


## Funzioni Booleane
Possono assumere soltanto due valori:vero(1) o falso(0). Vengono rappresentate tramite le tabelle di verità ($F=X+YZ$, minimizzata o ottimizzata).
![[Pasted image 20260217221918.png]]

## Identità fondamentali
![[Pasted image 20260217222059.png]]

## Principio di Dualità
Il principio di Dualità afferma che un’equazione booleana rimane valida se si considera il duale di entrambi i lati dell’uguaglianza di un’espressione. Il duale di un’espressione si ottiene:
- <u>cambiando AND con OR e viceversa</u>;
- <u>cambiando 1 con 0 e viceversa</u>;
- Mantenendo le priorità implicate ed esplicite.
![[Pasted image 20260217222518.png]]

## Teorema di DeMorgan
Passando da un membro all’altro
- OR $\to$ AND e AND $\to$ OR
- Il complemento è eliminato dall’intera espressione e applicato a ogni variabile
- Le precedenze implicite ed esplicite sono mantenute

## Complemento di una Funzione
![[Pasted image 20260217223045.png]]


## Teorema del Consensus
 Il prodotto YZ, può essere eliso dalla somma logica in cui i due fattori Y e Z appaiono in altri due prodotti che differiscono per una unica variabile, diretta in un prodotto (X Y) e negata nell’altro (X’ Z).
 Per riconoscerlo, devi avere:
 1. una variabile normale in un termine "X" in XY;
 2. la stessa variabile negata in un altro termine $\bar{X}$ in $\bar{X}Z$;
 3. un terzo termine formato esattamente dalle due variabili rimanenti moltiplicate tra loro, $YZ$(termine del consenso).
 **Dimostrazione**![[Pasted image 20260217111215.png]]
## Tecnica della riduzione algebrica 
Riduzione algebrica sistematica(**SAR**, Systematic Algebric Reduction):
1. Esprimere la funzione in forma SOP;
2. Riordinare le variabili;
3. Per ciascuna coppia di prodotti:
	1. Applicare ripetutamente adiacenza: $exp1 exp2 + exp1 exp2’ = exp1$;
	2. Applicare ripetutamente idempotenza: $exp1 + exp1 = exp1$
4. Applicare il Consensus: $exp1 exp2 + exp1’ exp3 + exp2 exp3 = exp1 exp2 + exp1’exp3$ 


## Forme Canoniche
Le funzioni booleane possono essere espresse in forme equivalenti(aventi la stessa tabella di verità). Una forma canonica è un’espressione booleana che contenga una somma logica di prodotti(forma **SOP**, Sum Of Products) ovvero un prodotto logico di somme(forma **POS**, Product Of Sums):$$F=X’YZ’+XYZ’+(X’+Z)’$$$$SOP:F=X’YZ’+XYZ’+XZ’$$$$POS:F’=(X+Y’+Z)(X’+Y’+Z)(X’+Z)$$
## Min-termini e Max-termini

### Min-termine, $m_j$
- prodotto di tutte le variabili;
- appaiono una sola volta;
- in forma diretta o in forma negata.
Vale 1 soltanto nella corrispondente combinazione alla quale è associato.
Il pedice $j$ è l’equivalente decimale del numero binario ottenuto indicando con 1 le variabili dirette e con 0 quelle negate
$m_5 \to A\cdot B \cdot C\cdot D$
$5 \to 0\quad1\quad0\quad1$  $\to$  $A’\cdot B\cdot C’\cdot D$

### Max-termine,$M_j$
- somma di tutte le variabili;
- appaiono una sola volta;
- In forma diretta o in forma negata.
Vale 0 soltanto nella corrispondente combinazione alla quale è associato.
Il pedice $j$ è l’equivalente decimale del numero binario ottenuto indicando con 0 le variabili dirette e con 1 quelle negate
$m_5 \to A\cdot B \cdot C\cdot D$
$5 \to 0\quad1\quad0\quad1$  $\to$  $A\cdot B’\cdot C\cdot D’$


## Forme canoniche SOP e POS

### Somma di Prodotti(SOP)
- si individuano le righe per cui $F$ ha valore $1$;
- si scrivono tanti prodotti quante sono le righe individuate;
- ogni prodotto è il min-termine relativo alla riga;
- la funzione $F$ si esprime come somma logica dei prodotti individuati.

### Prodotto di Somme(POS)
- si individuano le righe per cui $F$ ha valore $0$;
- si scrivono tante somme quante sono le righe individuate;
- ogni somma è il Max-termine relativo alla riga;
- la funzione $F$ si esprime come prodotto logico delle somme individuate

![[Pasted image 20260218190759.png]]


## Implementazione a due livelli
Le forme canoniche consentono di esprimere una funzione booleana con soltanto due livelli di porte logiche AND o OR.
- Forma SOP $\to$ logica AND-OR;
- Forma POS $\to$ logica OR-AND.
![[Pasted image 20260218191759.png]]

# Mappe di Karnaugh
È formata da un diagramma composto da celle, dove ognuna di esse rappresenta un mintermine.
- ogni forma SOP è identificabile graficamente su una mappa di Karnaugh come l’insieme delle celle corrispondenti ai mintermini inclusi nella funzione.
- Le K-map consentono di effettuare semplificazioni soltanto per implementazioni circuitali a due livelli.
Forme SOP:
- si impostano ad 1 le celle corrispondenti ai mintermini che implicano la funzione;
- Le rimanenti celle sono impostate a 0(in assenza di non specificazioni).
Forme POS:
- si impostano a 0 le celle corrispondenti ai maxtermini che specificano la funzione;
- Le rimanenti celle zono impostate a 1.

## Dalla tabella di verità alla K-map
- Si riordinano le righe in modo che ogni riga differisca dalla successiva solo per un letterale, negato nell’una e diretto nell’altra.
- Ad ogni riga corrisponde una cella.
- Le variabili meno significative etichettano le colonne e quelle più significative le righe della K-map.![[Pasted image 20260227111101.png]]

## K-map a 2 variabili
- individuazione dei mintermini![[Pasted image 20260227111256.png]]
- Rappresentazione di funzioni della K-map![[Pasted image 20260227111349.png]]

## K-map a 3 variabili
![[Pasted image 20260227111511.png]]
![[Pasted image 20260227111547.png]]

## K-map a 4 variabili
![[Pasted image 20260227111645.png]]
![[Pasted image 20260227111719.png]]

# Adiacenza e accoppiamenti
**Adiacenza**:
- In una K-map, due celle si dicono adiacenti se hanno un lato in comune. I bordi superiore e inferiore, destro e sinistro sono coincidenti.
- In K-map, due celle adiacenti corrispondono a mintermini che differiscono solo tra loro soltanto per una variabile, che risulta in forma diretta in una cella e negata nell’altra.
1. La combinazione di celle adiacenti corrisponde ad un prodotto di letterali costituito da tutti i letterali delle celle costituenti tranne quelli che sono diretti in un prodotto e negate nell’altro;
2. Data una funzione di $n$ variabili, la k-map corrispondente contiene 2n celle(per $n>4$ la k-map è di poca utilità);
3. Data una funzione di $n$ variabili, indicato con $i$ il numero di letterali elisi a partire da un mintermine, sono possibili $N$ accoppiamenti di $2i$ celle, dove:$$N=2^{n-i}\frac{n!}{i!(n-i)!}$$
![[Pasted image 20260227112745.png]]

# Primi implicanti e primi implicanti essenziali
**Implicante**: Un prodotto $P$ è un implicante di una funzione se essa assume il valore 1 per tutti i mintermini che compongono il prodotto $P$ considerato. Tutti gli accoppiamenti di una K-map, ottenuti accoppiando celle marcate con 1, sono implicanti.

**Primo implicante**: dato un implicante $P$, se la rimozione di qualunque letterale dà luogo a un prodotto che non è un implicante della funzione, allora $P$ è un primo implicante. Per una funzione $F$ di $n$ variabili, l’insieme dei primi implicanti corrisponde sulla mappa di Karnaugh all’insieme di tutti gli accoppiamenti costruiti utilizzando $2^m$ celle, contenenti 1, in cui ciascun accoppiamento dell’insieme contiene il maggior numero possibile di celle.

**Primo implicante essenziale**: se un mintermine di una funzione è incluso solo in un primo implicante, tale termine si chiama primo implicante essenziale. Se per una data funzione $F$, una cella contenente un 1, è inclusa in un solo accoppiamento che è un primo implicante, allora quel primo implicante è essenziale.

# Funzioni non completamente specificate
Sono funzioni la cui tabella di verità prevede, oltre ala normale configurazioni dove la funzione vale 1, configurazioni per le quali sono possibili due situazioni:
1. Sono combinazioni di ingresso che non si possono presentare;
2. Sono combinazioni di ingresso che si possono presentare, ma per le quali è indifferente il valore che si attribuisce all’uscita.
I mintermini corrispondenti a tali configurazioni si chiamano **condizioni di non specificazione**, che nella mappa di Karnaugh vengono rappresentate con $X$.

La scelta di decidere quale valore attribuire alla $X$ in fase di semplificazione è legata alla possibilità di ottenere espressioni più semplici.
## Semplificazione
1. Individuare i primi implicanti che $X=1$;
2. Eliminare dall’elenco dei primi implicanti ottenuti tutti i primi implicanti costituiti da non-specificazioni;
3. Selezionare i soli primi implicanti necessari a coprire la funzione, definita dai soli mintermini che la implicano;
4. Le non specificazioni che fanno parte dei primi implicanti selezionai nella copertura saranno impostate a 1, le altre a 0.
Esempio:![[Pasted image 20260227120842.png]]

# Sintesi di funzioni con molti ingressi
Per funzioni con 4-5 variabili di ingresso, la sintassi può essere effettuata utilizzando le mappe di Karnaugh.
Limitazioni nell’uso di k-map:
- la loro applicabilità è ridotta a funzioni Booleane con meno di 5 variabili;
- Non forniscono informazioni utili ad identificare il minimo numero di primi implicanti non essenziali necessari per la copertura della funzione;
- Sono di difficile applicabilità alle funzioni Booleane multi-uscita;
- Non sono un metodo algoritmico.

# Metodo di Quine-McCluskey
È un metodo tabellare che supera le limitazioni delle k-map per la sintesi di funzioni con più di 5 variabili di ingresso.

Si applica tanto alle funzioni completamente specificate quanto a quelle non completamente specificate. Per la sintesi di funzioni completamente specificate il metodo si divide in due fasi:
- Prima fase: identificazione di tutti i primi implicanti;
- Seconda fase: determinazione della copertura minima.

## Prima fase
1. Si parte dalla specifica della funzione in forma SOP;
2. Costruzione della tabella di partenza, ottenuta riordinando tutti i mintermini della funzione in base al numero di 1 presenti, raggruppandoli per gruppi con egual numero di 1;
3. Costruzione della tabella dei primi implicanti(primo passo):
	1. Si confrontano tutte le righe di un gruppo con tutte le righe del gruppo immediatamente successivo;
	2. Per ogni coppia di configurazioni adiacenti(differiscono di una sola variabile) si costruisce una nuova riga, riportando nella prima colonna l’elenco dei mintermini che hanno contribuito alla riga, e nella parte destra la configurazione corrispondente, fatta a partire dalle configurazioni dei mintermini costituenti, in cui la variabile che cambia è sostituita da un $-$;
	3. Le righe della tabella sono ordinate e raggruppate sulla base del numero 1 presenti;
	4. Nella tabella di partenza si marcano con $\sqrt{}$ i mintermini che hanno contribuito alla riga.
4. Costruzione della tabella dei primi implicanti(secondo passo):
	- usando la tabella costruita nel primo passo, ripetiamo i passi 3.1 e 3.4, indicando una sola volta eventuali prodotti ottenuti a partire da più primi implicanti, ma marcando tutti i primi implicanti costituenti.
5. Tutte le righe non marcate nelle tabelle via via costruite rappresentano tutti e soli i primi implicanti della funzione data.
![[Pasted image 20260307145451.png]]


## Seconda fase
1. Costruzione della tabella di copertura:
	1. È una tabella con tante righe quanti sono i mintermini della funzione e tante colonne quanti sono i primi implicanti;
	2. La posizione $i,j$ della tabella conterrà un 1 se il PI$_j$ copre il mintermine $m_j$, ovvero se tale mintermine è tra quelli che hanno generato PI$_j$.
2. Individuazione delle colonne essenziali(PIE):
	1. si cercano le righe che hanno un solo 1;
	2. La colonna in corrispondenza di tale 1 è essenziale, ed il primo implicante che le è associato è essenziale;
	3. Tutte le righe che hanno un 1 in corrispondenza di una colonna essenziale sono coperte dalla colonna essenziale.
3. Riduzione della tabella di copertura per eliminazione delle colonne essenziali e delle righe da esse coperte;
4. Riduzione della tabella per eliminazione delle colonne dominate;
5. Riduzione della tabella per eliminazione delle righe dominanti;
6. Ripetere 4 e 5 finché possibile.
![[Pasted image 20260307145622.png]]
- Sono colonne essenziali $E$ ed $F$, alle quali <u>corrispondono le righe con un solo 1</u>
- $E$ ed $F$ sono primi implicanti essenziali
- Sì eliminano $E$ e $F$ e delle righe da essi coperte
![[Pasted image 20260307150849.jpg]]
![[Pasted image 20260307151009.png]]
**Tabella di copertura ridotta**

#### Dominanza di colonna
- La colonna $B$ domina la $A$, perché contiene tutti gli 1 di $A$ più almeno un altro 1;
- La colonna $C$ domina la $D$, perché contiene tutti gli 1 di $A$ più almeno un altro 1;
Le colonne $A$ e $D$ possono essere rimosse senza per questo aumentare il costo del circuito o modificarne il funzionamento.
![[Pasted image 20260307151706.png]]
**Tabella ridotta dopo la dominanza colonna**


# Regole di dominanza
- **Dominanza di colonna**:
	- In una tabella di copertura, la colonna $i$ domina la colonna $j$ se la colonna $i$ contiene tutti gli uno della colonna $j$, ed almeno un 1 in più;
	- L’implicante associato ala colonna dominante copre quindi tutti i mintermini dell’implicante dominato, e pertanto può essere scelto senza aumentare il costo dell’implementazione.
- **Dominanza di riga**:
	- In una tabella di copertura, la riga $j$ è dominata dalla riga $i$ se ogni implicante che copre $j$ copre anche $i$, ma non viceversa;
	- Scegliere un implicante che copra un mintermine dominato, garantisce anche la copertura del mintermine dominante;
	- È quindi possibile eliminare e righe dominanti senza per questo aumentare il costo del circuito.

# Operatori funzionalmente completi
Le funzioni Booleane sono state espresse in termini di operatori AND, OR e NOT.
**Implementazioni a due livelli**:
- SOP:AND-OR;
- POS:OR-AND;
Esistono altri due operatori in grado di esprimere da soli gli altri tre:
- Operatore NAND,(NOT AND), simbolo(/);
- Operatore NOR(NOT OR), simbolo($\downarrow$).
Uno funzioni booleana può quindi essere espressa:
- In forma SOP usando solo NAND;
- In forma POS usando solo NOR.
## Proprietà NAND e NOR
![[Pasted image 20260307152431.png]]

## Operatori XOR e XNOR
![[Pasted image 20260307152544.png]]

# Funzioni dispari
Lo XOR di tre o più variabili ha valore 1 solo se le variabili che assumono valore 1 sono in numero dispari(funzione dispari). I mintermini con un numero dispari di variabili in forma diretta, sono adiacenti e differiscono al più per due letterali: <u>hanno distanza due l’uno dall’altro</u>. La funzione pari è il complemento della dispari.
![[Pasted image 20260307153231.png]]

# Generazione e controllo della parità
- Il circuito che permette l’aggiunta del bit di parità prende il nome di generatore di parità(**parity generator**);
- Il circuito che permette il controllo di parità prende il nome di controllare di parità(**parity checker**);
Usando, parità pari, si ha un errore se il parity checker genera 1 in uscita(perché un XOR di più variabili è 1 se il numero di bit 1 è dispari).
![[Pasted image 20260307154459.png]]
