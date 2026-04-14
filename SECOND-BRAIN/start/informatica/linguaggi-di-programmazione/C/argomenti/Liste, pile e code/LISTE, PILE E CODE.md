# Liste lineari
Una **lista lineare** è una successione di elementi omogenei che occupano in memoria una posizione qualsiasi. Ciascun elemento contiene un’informazione e un puntatore per mezzo del quale è legato al successivo. L’accesso alla lista avviene con il puntatore al primo elemento. Avremo:
```
Elemento = informazione + puntatore
```
Successivamente indicheremo con: 
- `inf` la parte informazione di ogni elemento;
- `pun` la parte puntatore;
- `puntLista` il puntatore al primo elemento della lista.
![[Esempio_lista.jpg]]

## Lista vuota
Il campo puntatore dell’ultimo elemento della lista non fa riferimento a nessun altro elemento; il suo contenuto corrisponde a un segnale di fine lista che in C è il valore `NULL`. Una lista vuota non ha elementi ed è rappresentata da un `puntLista` che punta a `NULL`: `puntLista` $\to$ `NULL`.


# Pila 
La pila(stack) è una struttura composta da elementi omogenei ordinati in una sequenza. Le operazioni di inserimento ed eliminazione di un elemento sono effettuate a uno stesso estremo della sequenza, ovvero la <u>testa della pila</u>. 
La pila è una struttura astratta, monodimensionale e dinamica, definita dalle regole che governano le operazioni di inserimento ed eliminazione degli elementi. Utilizzo della logica LIFO(Last In, First Out): l’ultimo elemento inserito sarà quello che viene eliminato per primo.
Un esempio che potremmo fare di pila sono le matriosche, bambole russe, della quale possiamo inserire una bambola piccola all’interno di una più grande e “eliminare” quella più grande di volta in volta(testa della pila).

# Coda
La coda(queue) è una struttura composta da una sequenza di elementi omogenei ordinati. L’operazione di inserimento di un elemento avviene dopo l’ultimo elemento inserito, quella di eliminazione è effettuata sul primo elemento della sequenza.
La coda è una struttura astratta, monodimensionale e dinamica. Il tipo di logica che viene applicato alle code è detto **FIFO(First Input, First Out)**: il primo elemento inserito è quello che per primo viene estratto. Un esempio dell’applicazione del metodo descritto è dato da una fila di persone in attesa a uno sportello, in cui chi arriva primo “dovrebbe” essere servito per primo e chi arriva per ultimo dovrebbe mettersi in coda.

Similmente alla rappresentazione della pila, abbiamo:
Coda$\to$D F C R$\to$testa
Il prossimo elemento da servire è R, che è in testa:
Coda$\to$D F C$\to$testa
Il successivo è C:
Coda$\to$D F$\to$testa
Poi arriva J, che si metterà in coda:
Coda$\to$J D F$\to$testa
