# Decoder
Un decoder è un circuito combinatore con $n$ ingressi e 2^n uscite, ogni uscita è un min-termine degli ingressi considerati. Simbolo circuitale: ![[Pasted image 20260414193325.png]]
*n-to-m-line decoder* 

# Encoder
Un encoder è un circuito digitale che performa l'operazione inversa al decoder. Ha $2^n$ ingressi ed $n$ uscite. Le linee di uscita generano il codice binario corrispondente al valore di ingresso.
Di solito viene implementato con porte OR usando gli input determinati dalla tabella di verità.
![[Pasted image 20260414194822.png]]

## Casi di ambiguità
La limitazione dell'encoder è che solo un ingresso alla volta può essere attivo. Se due sono contemporaneamente attivi l'uscita produce un errore. Per evitare questo molti encoder stabiliscono una priorità tra gli ingressi, la priorità potrebbe essere che il numero più alto ha una priorità maggiore.
**Esempio di due ingressi attivi**: se D3 e D6 sono contemporaneamente attivi l'uscita sarebbe (A2,A1,A0)=(1,1,1), che non è il numero 3 né il numero 6. se entrambi, 3 e 6, fossero attivi contemporaneamente in uscita avremmo 110, cioè il numero relativo a D6.

Altra ambiguità si ha quando l'uscita è 0 quando tutti gli ingressi sono uguali a zero, infatti le tre uscite sono uguali a zero anche quando D0=1.
### Priority Encoder
È un circuito combinatorio che implementa una **funzione di priorità**: <u>se due o più ingressi sono uguali ad 1 contemporaneamente, l'ingresso con più alta priorità ha la precedenza</u>.
![[Pasted image 20260414200626.png]]
Le X delle colonne di output rappresentano *don't care condiction*, le X nelle colonne di input sono usate per rappresentare prodotti di termini che non sono min-termini.
La validità dell'uscita è indicata dall'uscita V che assume valore 1 quando uno o più ingressi sono uguali a 1, se invece tutti gli ingressi sono pari a 0 si ha che le uscite A1 e A0 non sono usate: *don't care*.
![[Pasted image 20260418183130.png]]


# Multiplexer
Anche noto con il nome di selettore dati, è spesso indicato con la sigla MUX. 

Un MUX è un circuito combinatorio che seleziona l'informazione binaria da un insieme di ingressi e dirige l'informazione verso una singola linea di uscita.
La selezione di una particolare linea di ingresso è controllata da un insieme di variabili di ingresso dette variabili di *Selezione* oppure variabili di *Comando*.

Ha $2^n$ ingressi per i dati ed $n$ ingressi di comando, la cui combinazione seleziona l'ingresso di dati.
Un MUX $2^n$ *-to-1-line* è costituito da: $2^n$ linee dati; $n$ ingressi di controllo, 1 uscita. Anche i MUX possono essere dotati di ingressi di abilitazione. Quando l'ingresso di abilitazione è inattivo il circuito è disabilitato. L'ingresso di abilitazione può essere utile per connettere più MUX insieme.


# De-multiplexer
È un circuito digitale che performa l'operazione inversa a quella del MUX. Un de-multiplexer riceve l'informazione da 1 singola linea di ingresso e trasmette essa a una delle $2^n$ possibili linee di uscita.
La selezione dello specifico output è controllata da un bit combinazione di n-linee di selezione.
