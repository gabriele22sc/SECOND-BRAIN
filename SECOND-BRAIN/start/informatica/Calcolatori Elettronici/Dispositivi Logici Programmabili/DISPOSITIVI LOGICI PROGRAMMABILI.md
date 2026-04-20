I PLD(Programmable Logic Devices) si suddividono in tre famiglie: ROM(Read Only Memory), PLA(Programmable Logic Array) e PAL(Programmable Array Logic).

# ROM(Read Only Memory)
La ROM è una rete combinatoria con $n$ ingressi e in grado di sintetizzare una delle qualsiasi $2^n$ possibili funzioni a $n$ variabili. La ROM mantiene in maniera permanente l'informazione binaria immagazzinata anche se si stacca l'alimentazione.

È costituita da due party: AND e OR. La sezione AND della ROM è un circuito decodificatore ad $n$ ingressi e uscite (decoder). Le uscite del decoder prendono il nome di linee di parola, sono tutti i possibili min-termini legati alle $n$ variabili d'ingresso. La sezione OR ha tipicamente m=8 uscite, quindi è costituita da 8 OR gate a $2^n$ ingressi![[Pasted image 20260418190428.png]]

Dagli ingressi alla ROM si manda l'indirizzo della locazione di memoria che si vuole leggere il contenuto viene letto dalle uscite. La capacità di una ROM a 4 ingressi è di 16 byte, poiché sono 16 i min-termini ottenibili con 4 variabili, e sono quindi 16 le linee di parola.![[Pasted image 20260418190732.png]]

Il gate OR deve essere pensato come avente 32 ingressi, nella figura sottostante vengono mostrati i simboli dell'OR *Convenzionale* e del *Vettore Logico*. Ogni uscita del decoder è connessa tramite un fusibile a un ingresso di ogni OR gate. Ogni OR ha così 32 connessioni programmabili, a seconda delle funzioni che l'utente vuole realizzare.

La ROM può essere inoltre utilizzata come circuito combinatorio, ottenendo una forma non minima. 
- Le PROM(Programmable-Rom): sono delle ROM programmabili una sola volta dall'utente;
- Le EPROM(Erasable-Programmable-ROM): sono memorie cancellabili e programmabili.

# PLA(Programmable Array Logic)
Sono l'evoluzione logica delle PROM, sia la sezione AND che OR sono programmabili. Le uscite della sezione AND non costituiscono necessariamente i min-termini degli ingressi, posso tratte qualunque prodotto che serve quindi far uscite dalla sezione AND i Primi Implicanti(PI), ottenendo la forma minima della funzione.![[Pasted image 20260420101929.png]]

All'ingresso dello XOR abbiamo 1 oppure 0 a seconda se vogliamo che l'uscita sia data in forma diretta oppure complementata: $1\oplus X=X'$  oppure $0\oplus X=X$ 
![[Pasted image 20260420102238.png]]


# PAL(Programmable Array Logic)
Programmable Array Logic è un PLD con la sezione OR fissa e la sezione AND programmabile, siccome solo la parte AND deve essere programmata la PAL è più semplice programmare rispetto alla PLA, ma ovviamente meno flessibile.![[Pasted image 20260420102620.png]]
Il dispositivo è composto da 4 sezioni, in ogni sezione vi sono 3 AND gate programmabili. Ogni AND ha 10 connessioni di ingresso programmabili indicati nel diagramma da 10 linee verticali intersecanti ogni linea orizzontale. L'uscita FI viene retro-azionata ed è possibile usarla come ingresso di altre sezioni del PAL.![[Pasted image 20260420103331.png]]