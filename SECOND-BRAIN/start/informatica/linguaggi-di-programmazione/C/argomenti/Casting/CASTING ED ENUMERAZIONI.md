# Casting

Quando lavoriamo con tipi di dati diversi, potremmo aver bisogno di convertirli in un unico tipo di dato. Questa operazione viene chiamata **Casting**, assume il nome da coercizione ovvero quando si forza la conversione di un tipo ad un altro tipo.
In C per fare il casting, utilizziamo l’operatore `()`:
```
int numero;
float reale;

numero = 18;
reale = (float)numero;
```

# Enumerazioni

Permette di associare a delle costanti letterali, un valore intero. Così facendo possiamo utilizzare tali nomi per identificare il loro valore, come ad esempio per i giorni della settimana:
```
enum giorni { lun, mar, mer, gio, ven, sab, dom } settimana;
```
Abbiamo definito una variabile di nome `settimana` e di tipo enumerazioni `giorni`; l’identificatore `lun` sta per `0`, `mar` sta per `1`…
