La funzione `malloc` alloca un blocco di memoria di almeno `size` byte. Il blocco può essere maggiore di `size` byte a causa dello spazio necessario per le informazioni sull’allineamento e la manutenzione. La memoria viene allocata dinamicamente grazie a due tipologie di funzioni: **malloc(mentre allocation)** e **calloc(contiguous allocation)**.

# Valore restituito
`malloc()` restituisce un puntatore nota allo spazio allocato o `NULL` se è disponibile memoria insufficiente.
Entrambe le funzioni, `malloc` e `calloc`, ritornano un puntatore a carattere che punta alla memoria allocata.

# Dove vengono allocati i dati?
I dati allocati con `malloc` vengono allocati in una zona della RAM detta ”heap”, tra le variabili globali e lo stack, ovvero la memoria del processo:
```
Indirizzi bassi
      ↓
+------------------------+
|  Codice del programma  |  (.text)
+------------------------+
| Globali inizializzate  |  (.data)
+------------------------+
| Globali non inizializz.|  (.bss)
+------------------------+   ← Parte fissa, creata all’avvio
|        HEAP            |   ← Qui stanno i malloc
|   cresce verso l’alto  |
+------------------------+
|        STACK           |
|  cresce verso il basso |
+------------------------+
Indirizzi alti
```
La zona sopra le variabili globali è l’heap(data/bss), sotto abbiamo lo stack, gestito dal sistema operativo quando chiedi memoria dinamica.

# Esempio
Alloca dinamicamente un int, assegnagli un valore, stampalo e libera la memoria:
```
#include <stdio.h>
#include <stdlib.h>

int main(){
    int *n = malloc(sizeof(int));
    printf("inserisci un numero:\t");
    scanf("%d", n);

    if (*n > 100) {
        printf("\n\nil numero non puo' essere stampato");
    } else {
        printf("\n\nnumero:\t%d\tin memoria:\t%d", *n, n); // stampa del numero e dell'indirizzo
    }

    free(n);
}
```

- `int *n = malloc(sizeof(int));`    

- `int *n` dichiara `n` come puntatore a `int`.        

- `malloc(sizeof(int))` richiede dinamicamente memoria sufficiente per un `int`.        
L'indirizzo della memoria allocata viene assegnato a `n`.  
**Nota importante:** qui dovresti verificare se `malloc` ha restituito `NULL` (allocazione fallita). Esempio:  
        `if (n == NULL) { /* gestire errore */ }`
        
- `printf("inserisci un numero:\t");`  
Stampa il prompt per l'utente.
 
- `scanf("%d", n);`  
Legge un intero dall'input e lo scrive nell'indirizzo puntato da `n`.
- Questo è corretto perché `n` è un `int *`.
 Sarebbe prudente controllare il valore di ritorno di `scanf` per assicurarsi che la lettura sia andata a buon fine: `if (scanf("%d", n) != 1) { /* errore */ }`

- `if (*n > 100) {`
 `*n` dereferenzia il puntatore e prende il valore intero contenuto nella memoria allocata. Qui confronti il valore letto con 100.

- `printf("\n\nil numero non puo' essere stampato");`  
Se il valore è maggiore di 100, stampi questo messaggio.

- `} else {`      
Altrimenti esegui il ramo else.

- `printf("\n\nnumero:\t%d\tin memoria:\t%d", *n, n);`

`*n` stampa correttamente il valore intero. 
**Errore:** usi `%d` per stampare `n`, che è un puntatore. Stampare un puntatore con `%d` è sbagliato/UB (undefined behavior) su molte piattaforme. Per stampare un indirizzo usa `%p` e passa `(void *)n`, così:  
`printf("\n\nnumero:\t%d\tin memoria:\t%p", *n, (void *)n);` 
Questo mostra il valore e l'indirizzo di memoria dove è memorizzato.

- `free(n);`  
Libera la memoria precedentemente allocata con `malloc`. Senza questa chiamata avresti una perdita di memoria (memory leak).

- `}` (chiusura di `main`)  
Fine della funzione. Sarebbe buona norma ritornare un codice di uscita, ad esempio `return 0;`.