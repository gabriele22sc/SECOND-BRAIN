Nelle reti sequenziali il valore d'uscita dipende da quello degli ingressi e dallo stato della rete.![[Pasted image 20260420145806.png]]
Possiamo distinguere gli ingressi primari e secondari e le uscite primarie e secondarie:
- gli ingressi secondari costituiscono lo stato presente;
- le uscite secondarie costituiscono lo stato futuro.

# Reti sequenziali di Mealy e reti sequenziali di Moore
In base alla dipendenza tra uscite primarie e ingressi abbiamo due tipologie di reti sequenziali:
- **Reti sequenziali di tipo Mealy**: le uscite primarie dipendono sia dagli ingressi primari che dagli ingressi secondari;
- **Reti sequenziali di tipo Moore**: le uscite primarie dipendono soltanto dagli ingressi secondari

# Circuiti di memoria
Nell'anello di retroazione sono presenti <u>elementi di memoria</u>. Un **elemento di memoria** è una rete sequenziale capace di memorizzare un bit.
I segnali di ingresso alla memoria servono per modificare lo stato di tali dispositivi. 
L'informazione in un sistema digitale può essere memorizzata in molti modi usando circuiti logici, ad esempio tramite un buffer con tempo di ritardo non nullo $t_{pd}$. L'informazione presente al tempo $t$ in ingresso verrà riproposta in uscita del buffer dopo un tempo $t+t{pd}$.
Si desidera memorizzare l'informazione per un tempo indefinito che è tipicamente maggiore del tempo di ritardo della porta logica.

L'anello di retroazione consente di mantenere l'informazione memorizzata indefinitamente. Il buffer come elemento di memoria può essere costruito mettendo due inverter identici con ritardo di propagazione in cascata.

# Diagramma degli stati
I segnali che possono essere applicati ad una rete sequenziale vengono classificati in due specie:
- **Segnali ad impulso**: segnali la cui durata è inferiore al tempo di risposta del circuito;
- **Segnali a livello**: segnali la cui durata è superiore al tempo di risposta del circuito.
È **importante** notare che la non presenza dell'impulso o del livello in un dato istante e una informazione.

Per rappresentare una rete sequenziale si utilizzano i diagrammi a stati, in cui ogni stato stabile è rappresentato da un cerchio all'interno del quale si pone la lettera che contraddistingue lo stato stesso.![[Pasted image 20260420205003.png]]
![[Pasted image 20260420205042.png]]
# Tipologie di reti sequenziali
Le **reti sequenziali asincrone** hanno le uscite dipendenti dagli ingressi in ogni momento
Le **reti sequenziali sincrone** hanno le uscite dipendenti dalla conoscenza del segnale di ingresso in intervalli specifici di tempo.

i **latch** sono elementi di memoria asincroni(le uscite dipendono dagli ingressi), ovvero una rete sequenziale capace di memorizzare un bit di informazione.

Una rete si dice funzionante in **modo fondamentale** se i cambiamenti delle variabili di ingresso si hanno solo quando la rete è in uno stato stabile, altrimenti si dice funzionante in **modo impulsivo**. In pratica per le reti funzionanti in modo fondamentale non è ammessa la contemporanea variazione delle variabili di ingresso.

## Reti Sequenziali Sincrone
Una rete sequenziale sincrona impiega segnali che agiscono sulla memoria solo in istanti discreti di tempo. La sincronizzazione è ottenuta tramite dispositivi detti **clock generator**, che producono un treno di impulsi.![[Pasted image 20260420210320.png]]

Le uscite della memoria possono cambiare i propri valori solo in presenza degli impulsi del clock. I circuiti sequenziali che usano il clock come ingresso alla memoria sono detti **clocked sequential circuits**. Gli elementi di memoria usati nei clocked sequential circuits sono detti **flip-flop**.

L’operazione di base di un latch SR può essere modificata usando un ingresso di controllo addizionale che stabilisce quando lo stato del latch può essere cambiato.![[Pasted image 20260420212050.png]]

# Latch D
![[Pasted image 20260420212130.png]]

# Flip-Flop
- **Trigger**: lo stato di un latch è progettato per cambiare in corrispondenza di una variazione dell'ingresso di controllo, chiamata trigger;
- **Trasparenza del Latch D**: Il latch D, quando l'ingresso di sincronizzazione(clock) è a livello alto, è trasparente, ovvero l'uscita segue costantemente ogni cambiamento dell'ingresso per tutta la durata del segnale alto;
- **Problema delle transizioni multiple**: a causa della trasparenza, se l'ingresso cambia più volte mentre il clock è alto, anche l'uscita cambierà più volte. Questo può causare instabilità nei circuiti sequenziali;
- **Soluzione dei flip-flop**: i flip-flop sono costruiti per operare correttamente con un solo segnale di clock, eliminando la trasparenza tipica dei latch;
- **Interruzione della connessione**: la trasparenza viene eliminata "interrompendo la connessione" tra ingressi e uscite prima che l'uscita possa effettivamente cambiare;
- **Dipendenza dallo stato precedente**: il nuovo stato del flip-flop dipenderà solo dallo stato assunto nel precedente impulso di clock, evitando transizioni multiple indesiderate durante lo stesso periodo.
Esistono due modi per combinare insieme due latch e formare un flip flop:
1. **Master-slave**: i latch sono connessi in modo che:
	- gli ingressi del flip-flop controllino lo stato solo quando il clock è alto;
	- lo stato del flip-flop cambi soltanto quando il clock è al livello basso;
2. **Edge-triggered**: i latch sono connessi in modo che:
	- il flip-flop ottenuto cambia solo in presenza del fronte di salita del clock, ovvero della sua transizione da 0 a 1;
	- positive edge-triggered flip-flop, se attivo sul fronte di salita;
	- negative edge-triggered flip-flop, se attivo sul fronte di discesa.

![[Pasted image 20260420214059.png]]

# Simboli grafici standard
![[Pasted image 20260420214203.png]]
![[Pasted image 20260420214244.png]]

# Ingressi diretti
![[Pasted image 20260420214346.png]]
