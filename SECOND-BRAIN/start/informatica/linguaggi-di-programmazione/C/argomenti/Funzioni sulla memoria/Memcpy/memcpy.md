`memcpy(destinazione, sorgente, n)`: copia i valori di n byte a partire dalla locazione puntata da sorgente al blocco di memoria puntato da destinazione, restituisce il puntatore all’oggetto risultante. 

Se _sorgente_ e _destinazione_ coincidono il risultato non è definito, in tali casi si usa la funzione `memove`, che restituisce un puntatore a _destinazione_. 