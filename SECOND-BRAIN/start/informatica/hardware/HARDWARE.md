L’hardware è la parte fisica del computer, composto da parti magnetiche, ottiche, meccaniche ed elettroniche che consentono il funzionamento del computer.
Senza il software non potrebbe esistere l’hardware, e viceversa. 
**Hardware e software = Informazione elaborata**

# Parti hardware più importanti

## CPU(Central Processing Unit)
L’Unità Centrale di Elaborazione o CPU, è il ”motore” che preleva dalla memoria, interpreta ed esegue le istruzioni del programma e governa il funzionamento delle diverse parti che compongono il computer.

![[cpu.jpg]]

- **Unità di controllo(CU)**: legge le istruzioni dalla memoria e ne determina il tipo;
- **Unità aritmetico-logica(ALU)**: esegue le operazioni necessarie per eseguire le istruzioni;
- **Registri**: memoria ad alta velocità usata per risultati temporanei, determinano il parallelismo della CPU, esistono registri generici e registri specifici.

![[Organizzazione_cpu.jpg]]

## Bus
Il bus è una linea a cui sono contemporaneamente connesse le unità del calcolatore e che consente il trasferimento di dati tra tali utilità.
- Problema: contesa su un messo condiviso.
- Soluzione: CPU = master, periferiche = Slave.

### Tipi di bus
- **Bus dati**: utilizzato per trasferire dati, tra memoria e CPU o tra interfacce I/O e CPU;
- **Bus indirizzi**: identifica posizioni di memoria in cui la CPU scrive o legge;
- **Bus di controllo**: permette il transito di segnali di controllo che consentono di selezionare le unità coinvolte in un trasferimento dati(sorgente e destinazione) E di definire la direzione dello scambio(scrittura o lettura).

# Architettura di Von Neumann
Burks, Goldstein e Von Neuman sono stati i primi a proporre che il codice di un programma potesse essere memorizzato nella stessa memoria dei dati.

**Memoria Indifferenziata per dati o istruzioni**
Solo l’interpretazione da parte della CPU che stabilisce se una data configurazione di bit è da riguardarsi come un dato o come un’istruzione.

## Svantaggi
Il ”collo di bottiglia” è un fenomeno che si verifica rango la differenza di velocità tra il microprocessore e le periferiche è molto elevata. Questa va a incidere sulle prestazioni totali del sistema poichè la velocità complessiva del lavoro dipende dal dispositivo più lento coinvolto. Le periferiche esterne, che hanno limiti fisici dovuti al loro funzionamento, spesso rappresentano un freno durante l’operazione del sistema.

# Architettura Harward
Altre organizzazioni memorizzano i dati e programmi in memorie diverse. È principalmente utilizzata nei processori ad alte prestazioni e nelle architetture dedicate per applicazioni di elaborazione digitale dei segnali

# Memoria Centrale

- **RAM(Random Access Memory)**: volatile, memoria di lavoro;
- **ROM(Read Only Memory)**: permanente, esegue le funzioni di base(BIOS).

# Memoria virtuale
I dati in eccesso rispetto allo spazio disponibile nella RAM vengono immagazzinati sull’hard disk fino al momento dell’utilizzo. All’occorrenza i dati vengono trasferiti nella RAM, mentre altri dati passano nell’hard disk per fare posto.

# Memoria cache
È una memoria temporanea, non visibile al software, che memorizza un insieme di dati che possano successivamente essere velocemente recuperati su richiesta. Quando è necessario l’accesso ad un dato, questo dato viene prima cercato nella cache. Se è presente e valido, viene utilizzata la copia presente. Viceversa, viene recuperato dalla memoria principale, e memorizzato vela cache, nel caso possa servire successivamente.

# La memoria
Nell’ottica degli utenti applicativi la memoria deve essere:
- Capiente;
- Veloce;
- Permanente(non volatile).
Queste caratteristiche sono possedute solo dall’intera gerarchia di memoria nel suo insieme. La gestione della memoria è la componente del SO incaricata a soddisfare le esigenze di memoria dei processi.
La memoria è ma risorsa limitata.

## Gerarchie di memorie
- **Disco**: capiente, più o meno lento, non volatile, più o meno economico;
- **Memoria principale**: volatile, mediamente grande, veloce e più o meno costosa;
- **Cache**: volatile, veloce, piccola e costosa.
La gerarchia di memoria è gestita dal memory manager.
![[Pasted image 20260224213329.png]]


# Motherboard
Circuito stampato estremamente complesso su cui vengono saldati dei circuiti integrati:
- **Chipset**: svolge la gran parte del lavoro di interfaccia fra i componenti principali e i bus di espansione;
- **ROM**(PROM,EEPROM);
- **Socket** per il processore;
- **Connettori** necessari per il montaggio degli altri componenti.

