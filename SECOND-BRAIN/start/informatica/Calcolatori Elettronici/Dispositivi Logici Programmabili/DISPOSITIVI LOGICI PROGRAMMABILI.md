I PLD(Programmable Logic Devices) si suddividono in tre famiglie: ROM(Read Only Memory), PLA(Programmable Logic Array) e PAL(Programmable Array Logic).

# ROM(Read Only Memory)
La ROM è una rete combinatoria con $n$ ingressi e in grado di sintetizzare una delle qualsiasi $2^n$ possibili funzioni a $n$ variabili. La ROM mantiene in maniera permanente l'informazione binaria immagazzinata anche se si stacca l'alimentazione.

È costituita da due party: AND e OR. La sezione AND della ROM è un circuito decodificatore ad $n$ ingressi e uscite (decoder). Le uscite del decoder prendono il nome di linee di parola, sono tutti i possibili min-termini legati alle $n$ variabili d'ingresso. La sezione OR ha tipicamente m=8 uscite, quindi è costituita da 8 OR gate a $2^n$ ingressi![[Pasted image 20260418190428.png]]

Dagli ingressi alla ROM si manda l'indirizzo della locazione di memoria che si vuole leggere il contenuto viene letto dalle uscite. La capacità di una ROM a 4 ingressi è di 16 byte, poiché sono 16 i min-termini ottenibili con 4 variabili, e sono quindi 16 le linee di parola.![[Pasted image 20260418190732.png]]

Il gate OR deve essere pensato come avente 32 ingressi, nella figura sottostante vengono mostrati i simboli dell'OR *Convenzionale* e del *Vettore Logico*. Ogni uscita del decoder è connessa tramite un fusibile a un ingresso di ogni OR gate. Ogni OR ha così 32 connessioni programmabili, a seconda delle funzioni che l'utente vuole realizzare.

slide 8