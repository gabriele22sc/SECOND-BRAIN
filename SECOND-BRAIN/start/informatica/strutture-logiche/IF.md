
è una delle strutture di controllo più importanti di qualsiasi linguaggio, esegue un blocco di codice dopo che viene verificata se una condizione è vera o falsa.


# Struttura logica dell'if

L'if valuta un'espressione booleana, verifica la condizione: se vera, esegue il blocco di codice tra le graffe altrimenti lo ignora. Il flusso logico è:
1. valutare l'espressione nella condizione;
2. se la condizione è `true` allora esegue il blocco di codice;
3. se la condizione è `false`, ignora il blocco `{}` o esegue il blocco `else`.

esempio in C++:

```
#include <iostream>
using namespace std;

int main() {
    int numero = 10;

    if (numero > 5) {
        cout << "Il numero è maggiore di 5" << endl;
    }

    return 0;
}
```


esempio in JS:

```
let numero = 10;

if (numero > 5) {
    console.log("Il numero è maggiore di 5");
}
```


# ELSE IF

Quando abbiamo più condizioni da verificare utilizziamo `else if`:

C++
```
int voto = 75;

if (voto >= 90) {
    cout << "Ottimo!";
} else if (voto >= 70) {
    cout << "Buono!";
} else {
    cout << "Insufficiente";
}
```


JavaScript
```
let voto = 75;

if (voto >= 90) {
    console.log("Ottimo!");
} else if (voto >= 70) {
    console.log("Buono!");
} else {
    console.log("Insufficiente");
}
```



