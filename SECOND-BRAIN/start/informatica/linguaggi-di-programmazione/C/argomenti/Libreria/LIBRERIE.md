[[LIBRERIA _stdio.h_]]


# Creazione di una Liberia in C
Ogni libreria ha due parti fondamentali:
- File di intestazione;
- File contenente il codice.

## File di Intestazione
È denotato dal suffisso `.h`, contiene informazioni che i programmi che la utilizzeranno hanno necessità di conoscere. Contiene costanti, tipi e prototipi per le funzioni disponibili nella libreria.

```
/* util.h */
extern int rand();
extern void bubble_sort(int, int []);
```
Questi sono due prototipi di funzioni. La parola `extern` in C rappresenta funzioni che verranno collegate in un momento successivo.

## File contenente il codice
Dice cosa fanno eventuali funzioni e robe simili ha lo stesso utilizzo di un main per compilarlo serve un compilatore(Gcc Anche se sono più utilizzati i makefile per automatizzare il tutto) che compili sia questo file che il file contenente il main.