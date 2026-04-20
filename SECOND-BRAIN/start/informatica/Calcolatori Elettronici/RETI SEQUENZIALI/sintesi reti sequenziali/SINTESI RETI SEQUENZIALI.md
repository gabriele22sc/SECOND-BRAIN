La sintesi di una rete sequenziale inizia con una descrizione verbale dalla quale si ottiene la tabella di stato o l'equivalente diagramma di stato. Una rete sequenziale sincrona è costruita tramite l'uso di una rete combinatoria e flip-flop, il numero dei flip-flop è determinato dal numero degli stati della rete. $n$ flip-flop permettono di rappresentare $2^n$ stati.

# Riconoscitore di sequenze
Il circuito che vogliamo sintetizzare deve riconoscere occorrenze di una particolare sequenza di bit all'interno di sequenze più lunghe. Il circuito ha un ingresso X e una uscita Z, un direct reset per inizializzare lo stato dei circuiti a zero.
Il fattore chiave è che la rete deve avere memoria del passato, cioè ricordare i valori precedenti dell'ingresso.
