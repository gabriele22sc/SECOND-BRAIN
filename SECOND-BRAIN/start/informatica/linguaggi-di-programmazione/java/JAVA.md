## OGGETTO PER LA LETTURA DALLA TASTIERA

le API hanno un oggetto System.in che rappresenta la tastiera del calcolatore. Alcune operazioni di Scanner:
- `int nextInt()`: legge un numero intero e restituisce il numero letto;
- `double nextDouble()`: legge un numero reale e restitusce il numero letto;
- `String nextLine()`: legge una linea di testo, e la restituisce;
- `String next()`: legge un “token” (una sequenza di caratteri contigui e senza separatori), e restituisce il token letto;
- `boolean hashNextInt()` o `boolean hashNextDouble()`: verifica se il prossimo token può essere interpretato come un numero intero/reale;
- `boolean hashNextLine()` o `boolean hashNext()`: verifica se in input è disponibile una ulteriore linea/token.

## ESEMPIO COME LEGGERE DUE NUMERI DA TASTIERA:

```
import java.util.*;
		/* Applicazione che legge dalla tastiera due numeri interi
		* e ne calcola e visualizza la somma. */
class SommaDueNumeri {
public static void main(String[] args) {
int a; 		// il primo numero intero
int b; 		// il secondo numero intero
int somma; 	// la somma di a e b
Scanner in; 	// per la lettura dalla tastiera
		/* crea l’oggetto che rappresenta la tastiera */
in = new Scanner( System.in );
		/* legge i due numeri interi a e b */
System.out.println("Scrivi due numeri interi");
		/* legge due numeri interi a e b */
a = in.nextInt();
b = in.nextInt();
		/* calcola la somma di a e b e la visualizza */
somma = a+b;
System.out.print("La somma dei due numeri e ");
System.out.println(somma);
}
}
```

## DEFINIZIONI 

**CLASSE**: è una struttura o un modello di ciò che deve essere realizzato. Alla classe non viene associata alcuna locazione di memoria

**METODI**:
`Math.round()`: arrotonda ila valore specificato al valore int o long più vicino.

[Reference java](https://docs.oracle.com/javase/8/docs/api/)
