
## Dichiarazione
Nella dichiarazione di una struttura, abbiamo diversi modi con cui possiamo definirla:
1. `struct elemento{…}`: qui definiamo solo il tipo, ovvero `struct elemento`. Nella dichiarazione delle variabili avremo bisogno sempre di `struct`:
```
struct elemento a;
struct elemento *p;
```

2. `typedef struct elemento {…}elemento`: qui definiamo la struttura e crei un alias di tipo chiamato elemento. Quindi potremo dichiarare elementi senza scrivere struct:
```
elemento a;
elemento *p;
```