Si utilizza un modello semplificato di elaboratore di tipo **RISC(Reduced Instruction Set Computer)**.

# Architettura del processore
![[Pasted image 20260421130415.png]]

# Caratteristiche del processore
- Parallelismo: 16 bit;
- 16 registri general purpose da 16 bit;
- 3 registri special purpose non direttamente indirizzabili dalle istruzioni: **Program Counter(PC)**, **Instruction Registrer(IR)** e **Stack Pointer(SP)**;
- Flag: **Z(zero)**, **C(carry)**, **N(negative)**, **V(overflow)**.
- Isolated I/O: 16 bit per gli indirizzi di I/O;
Macchina **"load & store"**, del tipo **RISC(Reduced Instruction Set Computer)**:
	 - le uniche istruzioni che possono accedere alla memoria sono quelle che trasferiscono i dati da e verso i registri;
	 - tutte le altre operazioni operano soltanto sui registri.

# Modi di indirizzamento
Nell'accesso alla memoria, l'indirizzo può essere espresso in tre modi:
- **Operando Immediato**: il dato si trova nella parola successiva all'istruzione(l'indirizzo del dato è contenuto nel PC);
- **Indirizzo Assoluto**: la parola dopo l'istruzione(indirizzo del PC) contiene l'indirizzo di memoria dove si trova il dato;
- **Indirizzo in Registro**: l'indirizzo del dato è contenuto nel registro specificato dal codice dell'istruzione.

# Il Control Bus

1. $R/\bar{W}$, la CU lo pone:
	- a 1 per le operazioni di lettura;
	- a 0 per le operazioni di scrittura;
2. $M/\bar{IO}$, la CU lo pone:
	- a 1 per le operazioni di lettura o scrittura in memoria;
	- a 0 per le operazioni di lettura o scrittura su dispositivi di I/O;
3. $W/\bar{B}$, la CU lo pone:
	- a 1 per le operazioni di lettura o scrittura di 1 word;
	- a 0 per le operazioni di lettura o scrittura di 1 byte;

# Memoria RAM
![[Pasted image 20260422114242.png]]

# Dispositivi I/O
![[Pasted image 20260422114403.png]]

# Ciclo di esecuzione delle Istruzioni

## Istruction Fetch:
La CU preleva l'istruzione dalla memoria all'indirizzo indicato dal PC e la carica dell'IR. Successivamente, il PC viene incrementato.
### Richiesta dell'istruzione
![[Pasted image 20260422115303.png]]
- **Puntamento**: il registro PC(Program Counter) contiene il valore `0003`. Questo è l'indirizzo della cella di memoria dove è salvata l'istruzione che vogliamo eseguire;
- **Indirizzamento**: l'indirizzo `0003` viene inviato sul bus degli indirizzi;
- **Segnali di Controllo**: la CU imposta i segnali sul bus di controllo:
	  1. $M/\bar{IO}=1$: indica che vogliamo comunicare con la memoria RAM, e non con l'I/O.
	  2. $R/\bar{W}=1$: indica che l'operazione è di lettura(Read).
	  3. $W/\bar{B}=1$: indica che stiamo leggendo una parola intera(word) di 16 bit.

### Trasferimento e Aggiornamento
![[Pasted image 20260422115318.png]]
- **Trasferimento**: la memoria risponde inviando il contenuto della cella `0003`(con valore `1000`) sul bus dei dati.
- **Caricamento**: il valore `1000` entra nella CPU e viene memorizzato nell'**IR(Istruction Register)**. Ora la CPU ha l'istruzione pronta per essere decodificata.
- **Incremento del PC**: contemporaneamente al caricamento, il PC(Program Counter) viene incrementato. Il PC passa da `0003` a `0005`, affinché, al termine dell'operazione, il processore sappia già dove andare a prendere l'istruzione o dato successivo.

## Operand Fetch:
Il processore recupera i dati necessari per completare l'operazione seguendo uno dei tre modi di indirizzamento: operando immediato, indirizzo assoluto, indirizzo in registro.

### Operando Immediato
![[Pasted image 20260422120924.png]]
Il PC(Program Counter) punta all'indirizzo `0005`. La CPU invia questo indirizzo sul bus e imposta il controllo su **Lettura**($R/\bar{W}=1$) e **Memoria**($M/\bar{IO}=1$).

- **Puntamento(da PC a bus indirizzi)**: la freccia che va dal PC(Program Counter) al bus indirizzi, indica che la CPU sta comunicando a tutto il sistema quale cella di memoria vuole consultare.
- **Attivazione della Memoria(dal bus indirizzi alla RAM)**: la freccia che va dal bus indirizzi alla memoria in corrispondenza dell'indirizzo `0005`. Questo indica che il decodificatore di indirizzi della RAM ha individuato la cella corretta.
- **Abilitazione del Controllo(dalla CU al bus di controllo)**: la freccia che va dalla CU verso il bus di controllo indica l'invio dei segnali elettrici necessari per l'operazione: in questo caso, "stai pronto a leggere"($R/\bar{W}=1$) e "stiamo parlando con la memoria"($M/\bar{IO}=1$).

![[Pasted image 20260422122359.png]]
Il valore contenuto all'indirizzo `0005`(`36CF`), viaggia sul bus dati e viene caricato direttamente nel registro di destinazione, in questo caso $R0$. Contemporaneamente, il PC(Program Counter) viene incrementato a `0007` per passare alla prossima istruzione.
- **Dalla Memoria al Registro**: la freccia che parte dal valore `36CF`, parte dal bus dati e risale fino al registro $R0$. Indica che il dato è stato memorizzato nel processore.
- **Incremento di PC**: la freccia ridondante su PC indica che la CU ha aggiornato il valore da `0005` a `0007`, preparandosi all'istruzione successiva.

### Indirizzo Assoluto
![[Pasted image 20260422123153.png]]
- **Puntamento all'indirizzo dell'indirizzo**: il PC contiene `0005`. La freccia verde che parte dal PC e va verso il bus indirizzi indica che la CPU sta chiedendo alla memoria il contenuto della cella `0005`.
- **Segnali di controllo**: la CU imposta i bus per una lettura standard:
	1. $M/\bar{IO}=1$: stiamo parlando con la RAM;
	2. $R/\bar{W}=1$: operazione di lettura;
	3. $W/\bar{B}=1$: legge una parola da 16 bit.
- **In memoria**: all'indirizzo `0005` abbiamo `00` mentre al `0006` abbiamo `00`.
![[Pasted image 20260422123834.png]]
- **Puntamento all'indirizzo**: la CU legge l'istruzione dentro l'IR e capisce cosa deve fare. La freccia che parte dalla CU al bus di controllo indica che stiamo inviando l'indirizzo `0000` sul bus. Una volta che l'indirizzo arriva alla memoria, ciò indica che la CPU sta selezionando esattamente la cella numero `0000`.
- **Dalla Memoria al bus dati**: nelle celle `0005` e `0006` della memoria sono evidenziate in verde. All'interno contengono il valore `0000`. La freccia verde indica che il valore esce dalla memoria e sale sul bus dati.
- **Dal bus dati al bus indirizzi**: invece di finire in un registro per essere usato come numero, il valore `0000` viene travasato dal bus dati al bus indirizzi. 
- **Ritorno alla memoria**: una volta che `0000` è sul bus indirizzi, la freccia verde torna verso la memoria, ma stavolta punta alla cella `0000`.
![[Pasted image 20260422125438.png]]
- **Dalla memoria al bus dati**: la freccia che parte dalla cella `0000`(contenente `51A8`) e scende al bus dati, indica che il dato sta viaggiando verso il processore.
- **Ingresso nel registro**: la freccia dal bus dati al registro $R0$ all'interno dell'ALU, registra il valore `51A8` nel registro $R0$.

### Indirizzo in registro
![[Pasted image 20260422140823.png]]
- **Dalla CU al bus di controllo**: rappresenta l'attivazione dei segnali di controllo. La CU sta comunicando al sistema di restare in attesa perché sta per avvenire una lettura. Imposta i segnali: $M/\bar{IO}=1$, parla con la memoria e $R/\bar{W}=1$, per leggere.
- **Dal R1 alla cella di memoria `0006`**: è il puntamento logico in cui, l'istruzione caricata nell'IR(`3001`) dice alla CPU che l'indirizzo del dato non è scritto nell'istruzione stessa, ma è già salvato dentro R1. La freccia che dal bus indirizzi punta alla cella `0006` della memoria serve a capire che il processore userà quel numero come coordinata per cercare nella RAM.
![[Pasted image 20260422142345.png]]
- **Trasferimento fisico del dato**: la memoria carica il valore `2297` sul bus dati. In questa fase, il bus dati porta l'informazione dalla RAM verso la CPU. Passa dal bus dati al registro R0 dell'ALU.


## Memory Store:
Se l'istruzione prevede il salvataggio di un risultato in memoria, il dato viene trasferito da un registro alla cella di memoria specificata