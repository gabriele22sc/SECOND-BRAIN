La sintesi di una rete sequenziale inizia con una descrizione verbale dalla quale si ottiene la tabella di stato o l'equivalente diagramma di stato. Una rete sequenziale sincrona è costruita tramite l'uso di una rete combinatoria e flip-flop, il numero dei flip-flop è determinato dal numero degli stati della rete. $n$ flip-flop permettono di rappresentare $2^n$ stati.

# Riconoscitore di sequenze
Il circuito che vogliamo sintetizzare deve riconoscere occorrenze di una particolare sequenza di bit all'interno di sequenze più lunghe. Il circuito ha un ingresso X e una uscita Z, un direct reset per inizializzare lo stato dei circuiti a zero.
Il fattore chiave è che la rete deve avere memoria del passato, cioè ricordare i valori precedenti dell'ingresso.

# Costruzione del diagramma di stato
![[Pasted image 20260421113822.png]]
![[Pasted image 20260421113838.png]]
![[Pasted image 20260421113948.png]]![[Pasted image 20260421114002.png]]

# Tabelle di eccitazione 
È necessario trovare una relazione funzionale tra la tabella di stato e le input equation. Vengono utilizzate allo scopo le tabelle di eccitazione dei flip-flop, i FF possono essere descritti usando una tabella che ne descrive il comportamento. 

Durante la progettazione di una rete sequenziale, sono note le transizioni dal **present state** al **next state**, si desidera trovare le condizioni di ingresso del flip-flop che causano tali transizioni. Occorre una tabella che elenca gli ingressi necessari per ottenere un cambio di stato(tabella di eccitazione):
- una colonna indica lo stato presente $Q(t)$;
- una colonna indica lo stato futuro $Q(t+1)$;
- una colonna per ogni ingresso del flip-flop;
Nelle colonne che rappresentano gli ingressi al FF, viene riportato il valore che deve avere l'ingresso per avere la transizione dal present state al next state.
Le X indicano delle **don't care condiction**.

# Stati equivalenti
Si può dare una definizione di stati equivalenti solo per le tabelle di transizione di stato **completamente specificate**. 
*Due stati si dicono equivalenti se per ciascuna variabile di ingresso essi producono esattamente le stesse uscite ed evolvono nello stesso stato o in stati equivalenti*
Perché siano equivalenti occorre verificare(per ogni configurazione degli ingressi) che si produca la stessa uscita e si arrivi allo stesso stato o stati equivalenti. Se sono equivalenti è possibile rimuoverne uno dei due senza alterare il comportamento esterno.
