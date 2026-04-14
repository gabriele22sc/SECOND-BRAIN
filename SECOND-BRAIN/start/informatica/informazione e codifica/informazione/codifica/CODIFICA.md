La stessa informazione si può rappresentare in modi differenti. Stessa rappresentazione per informazioni differenti.

# Sistemi di codifica

- Usa un insieme di simboli di base(alfabeto);
- I simboli dell'alfabeto possono essere combinati ottenendo differenti **configurazioni**(codici o stati) distinguibili l'una dall'altra;
- Associa ogni configurazione ad una particolare entità di informazione (la configurazione diventa un modo per rappresentarla).

esempi:
1) alfabeto:
- cifre "0","1","2"... 
- separatore decimale(",")
- separatore delle migliaia(".")
- segni positivo("+") e negativo("-")
2) regole di composizione(sintassi) -> definiscono le combinazioni ben formate (12.318,43 o 12,318.43)
3) codice(semantica): associano ad ogni configurazione un'entità di informazione
$12.318,43=1\cdot10^4+2\cdot10^3+3\cdot10^2+1\cdot10+1\cdot10^0+4\cdot10^{-1}+3\cdot10^{-2}$ 
4) lo stesso alfabeto può essere usato per codici diversi


# La rappresentazione dei dati

Principio di funzionamento del computer è basato sulla logica binaria: opera on dati espressi utilizzando 2 stati: 0 e 1.

L'unità minima di informazione nel computer è un insieme di 8 bit: 1byte = 8bit.

## Scala dei bit

$$\begin{align} 2^0=1 \\ 2^1=2 \\ 2^2=4 \\ 2^3=8 \\ 2^4=16 \\ 2^5=32 \\ 2^6=64 \\ 2^7=128 \\ 2^8=256 \\ 2^9=512 \\ 2^{10}=1024
\end{align}$$

# Numeri binari da 1 a 16
$$\begin{align}0001 \to 1 \\ 0010 \to 2 \\ 0011 \to 3 \\ 0100 \to 4 \\ 0101 \to 5 \\ 0110 \to 6 \\ 0111 \to 7 \\ 1000 \to 8 \\ 1001 \to 9 \\ 1010 \to A \\ 1011 \to B \\ 1100 \to C \\ 1101 \to D \\ 1110 \to E \\ 1111 \to F
\end{align}$$
# Codifica binaria

1) Usa un alfabeto di 2 simboli;
2) Utilizzata nei sistemi informatici:
	- si utilizza una grandezza fisica per rappresentare un informazione(luminosità, tensione elettrica, la corrente elettrica);
	- si divide in due intervalli l'insieme dei valori che la grandezza può assumere: ogni intervallo corrisponde ad un simbolo
3) Solo 2 simboli al fine di ridurre la probabilità di errore:
	- tanto più simboli si devono distinguere e tanto meno la rivelazione sarà affidabile (gli intervalli della grandezza fisica saranno meno ampi).

[[COMPLEMENTO A DUE E MODULO E SEGNO]]
[[VIRGOLA FISSA E VIRGOLA MOBILE]]
# Sistema ottale

SIMBOLI: 0 1 2 3 4 5 6 7 8 
$35_{10}\ \rightarrow$ divisioni per 8
$35\div8=4 \ \rightarrow$ resto 3
$4\div8=0 \ \rightarrow$ resto 4
$35_{10} \ \rightarrow \ 43_8$

# Sistema esadecimale

SIMBOLI: 0 1 2 3 4 5 6 7 8 9 A B C D E F
$161_{10} \ \rightarrow \ A1_{16}$

# Le grandezze

La capacità di memoria del computer si misura in byte e nei suoi multipli
![[scala-byte.png]]

1kilobyte(KB) = 1024 byte
1megabyte(MB) = 1024Kb
1gigabyte(GB) = 1024MB
1terabyte(TB) = 1024GB

# ASCII(America Standard Code for Information Interchange)

Associare adi al calcolatore(codifica dei caratteri)

Esiste una codifica standard che si chiama ASCII, utilizza un codice di 8 bit($2^8 = da \ 0 \ a \ 255 \ codici$).

ad esempio:
"Nel mezzo del cammin di nostra vita"

in ASCII sarebbe: 078 101 108 000 109 101 122 122 111 000 100 101 108 000 099 097
109 109 105 110 000 100 105 000 110 111 115 116 114 097 000...

## Le conversioni

Proviamo a convertire un numero da decimale in binario:
$(078)_{10}=?_2$ 
![[converisone.png]]
[[conversioni binarie]]


# Codifica delle immagini

L'immagine viene digitalizzata cioè rappresentata con sequenze di pixel. Ogni pixel ha associato un numero che descrive un particolare colore (o tonalità di grigio). Si mantengono anche la dimensione, la risoluzione e il numero di colori utilizzati

## Codifica delle immagini in toni di grigio

Per ogni pixel si stabilisce il livello medio di grigio cui viene assegnata convenzionalmente una rappresentazione binaria

## Compressione delle immagini e dei dati

Lossless: senza perdite di informazione
- programmi, documenti.

Lossy: con perdita di informazione
- rapporto di compressione variabile dall'utente
- immagini: GIF, JPEG(elimina lievi cambiamenti di colore)


# Codifica di filmati/video

Video = immagini in movimento

Memorizzazione mediante sequenze di fotogrammi (sono necessarie delle tecniche per ottimizzare tale memorizzazione),
Sono sequenze di immagini compresse (ad esempio si possono registrare solo le variazioni tra un fotogramma e l'altro). Esistono vari formati(compresi i suoni): mpeg, avi, quicktime, mov...


# Codifica dei suoni

L'onda sonora viene misurata ad intervalli regolari. Minore è l'intervallo di campionamento e maggiore è la qualità del suono. ad esempio i cd musicali vanno per 44000 campionamenti al secondo, ovvero 16bit per campione. Alcuni formati:
- .mp3, .mov, .wav, .mpeg,...
- formato midi usato per l'elaborazione della musica al PC