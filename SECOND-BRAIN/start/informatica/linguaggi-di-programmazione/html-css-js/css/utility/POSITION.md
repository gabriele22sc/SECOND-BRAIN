[posizionamento](https://www.html.it/pag/14235/posizionamento-degli-elementi/)

#POSITION PROPERTY
position è la proprietà fondamentale per la gestione della posizione degli elementi: determina la modalità di presentazione degli elementi nella pagina. Viene applicata a tutti gli elementi e non è ereditata. Esistono 4 modalità di posizionamento: <u>STATIC</u>, <u>RELATIVE</u>, <u>ABSOLUTE</u> e <u>FIXED</u>.

```position: static;``` -> valore di default, predefinito per tutti gli elementi non posizionati secondo un altro metodo. Rappresenta la posizione normale che ciascuno degli elementi occupa nel flusso del documento.

```position: relative;``` -> L'elemento viene posizionato relativamente al suo contenitore, ovvero dal posto che l'elemento avrebbe occupato nel normale flusso del documento. Viene impostato con le proprietà top, left, bottom o right, esse non indicano un punto preciso ma lo spostamento verso il quale viene spostato l'elemento(left: 30; sposterà di 30 px da sinistra l'elemento).

```position: absolute;``` -> L'elemento viene rimosso dal flusso del documento ed è posizionato in base ai valori forniti con le proprietà top, left bottom o right. Il posizionamento avviene sempre rispetto al contenitore dell'elemento, esso è rappresentato dal primo elemento antenato che abbia un posizionamento diverso da static.

