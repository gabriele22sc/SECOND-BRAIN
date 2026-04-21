# Registro
Un registro include un insieme di flip-flop. Se un flip-flop ha la capacità di memorizzare un bit di informazione, un registro ad n-bit, includente n-flip-flop, è capace di memorizzare $n$ bit di informazione binaria.
#### Definizione:
Il termine *registro* è applicato a un insieme di FF, insieme a porte logiche, che performa l'attività di processamento di dati. I flip-flop trattengono i dati, le porte logiche determinano il nuovo dato che deve essere trasferito nei FF.

## Tipologie di registro
![[Pasted image 20260421120813.png]]
![[Pasted image 20260421120840.png]]

## Registro con Caricamento parallelo
![[Pasted image 20260421120912.png]]
![[Pasted image 20260421121211.png]]
 - Per un funzionamento corretto **Load signal** deve mantenere il valore costante 0 o 1 anche quando il $clock=0$.
 - Dato che il clock è connesso al C input del registro tramite l'uso di porte logiche si parla di: **Clock-Gating**.
 - Inserendo dei gate lungo il percorso del clock si producono differenti ritardi di propagazione tra clock e gli ingressi dei FF aventi o non aventi clock-gating.
 - Se il segnale di clock arriva ai FF, o registri, in tempi differenti si dice che esiste un **clock skew**. Affinché si abbia un vero sistema sincronizzato il clock deve arrivare simultaneamente a tutti i FF. Per questo è consigliabile che le operazioni di controllo del registro avvengano senza l'uso del clock-gating se possibile, altrimenti bisogna adoperarsi in modo da rendere il clock-skew il più possibile vicino a 0.
![[Pasted image 20260421121832.png]]
- L'ingresso **Load** stabilisce l'azione che deve essere presa in presenza dell'impulso di clock;
- Quando **Load=1** i dati dai quattro ingressi sono trasferiti nei FF in presenza dell'impulso di clock;
- Quando **Load=0** i dati di ingresso sono bloccati e i D input dei FF sono connessi alle uscite;
- La retroazione è necessaria affinché sia rispettata la condizione di *"no change"*. Per lasciare le uscite invariate è necessario che il D-input sia uguale al valore presente dell'uscita;
- **Load** determina se il prossimo impulso deve accettare la nuova informazione presente agli ingressi.

## Shift Register
![[Pasted image 20260421122915.png]]
![[Pasted image 20260421122845.png]]

## Serial Transfer
- A volte è necessario controllare lo shift in modo che avvenga solo per determinati impulsi di clock, è possibile allora usare la tecnica del clock-gating sostituendo l'ingresso di load con quello di Shift;
- A causa del clock skew non è un approccio desiderabile, così vedremo che l'operazione di shift può essere controllata attraverso il D-input dei FF invece che tramite l'ingresso di controllo;
- Un sistema digitale è opera in modo seriale quando l'informazione nel sistema è trasferita o manipolata un bit alla volta;
- L'informazione è trasferita un bit alla volta tramite lo shift dei bit fuori da un registro e dentro un altro. Questo metodo di trasferimento è opposto al trasferimento parallelo.
![[Pasted image 20260421123430.png]]
![[Pasted image 20260421123538.png]]
## Shift Register con Caricamento Parallelo
![[Pasted image 20260421123637.png]]
![[Pasted image 20260421123648.png]]
- Quando $Shift=Load=0$ il terzo AND di ogni stage è abilitato e l'output di ogni FF è applicato al suo D;
- Quando $Shift=0$ e $Load=1$ il secondo AND è abilitato e D-input è applicato al corrispondente ingresso D del FF, sul fronte di salita del clock i dati vendono caricati in modo parallelo;
- Quando $Shift=1$ e $Load=x$ il primo AND è abilitato gli altri sono disabilitati, il dato presente sul SI viene trasferito all'ingresso $D0$, $q0$ a $D1$ e così via, sulla transizione positiva del clock;
- Gli Shift Register sono usati per interfacciare sistemi digitali remoti;

## Shift Register Bidirezionale
![[Pasted image 20260421124156.png]]![[Pasted image 20260421124212.png]]![[Pasted image 20260421124238.png]]



# Contatore 
Un contatore è un registro che si muove attraverso una predeterminata sequenza di stati a causa dell'applicazione dell'impulso di clock. Le porte del contatore sono connesse in modo da produrre la sequenza di stati precedente.
- Registri e contatori sono blocchi funzionali sequenziali usati per la progettazione di sistemi digitali;
- I **registri** sono utili per la memorizzazione e la manipolazione delle informazioni;
- I **contatori** servono per la sequenzializzazione e il controllo delle operazioni in un sistema digitale.

## Ripple Counter
Un registro che si muove attraverso una sequenza di stati predefinita, a seguito dell'applicazione dell'impulso di ingresso è chiamato **contatore**.
L'impulso di ingresso potrebbe essere un impulso di clock oppure originato da altre sorgenti che potrebbero occorrere ad intervalli di tempo fissati o randomici. La sequenza degli stati potrebbe seguire la sequenza dei numeri binari o anche altre sequenze.
Un contatore che segue la sequenza binaria è detto **Binary Counter**. Un n-bit binary counter consiste di n-FF e può contare da $0$ a $2^n-1$ . I contatori sono disponibili in due categorie:
1. **Ripple Counter**: dove le uscite di un FF servono per il triggering di altri FF;
2. **Synchronous Counter**: l'ingresso C di tutti i FF è controllato da un clock comune.

## Contatori Binari
![[Pasted image 20260421125238.png]]

### Contatori Binari Sincroni
- I contatori sincroni sono diversi dai ripple, l'ingrsso di Clock è applicato a tutti i FF;
- Per JKFF la decisione di complementare l'uscita del FF è determinata dal valore degli ingressi J e K;
- Se J=K=0 il FF cambia stato anche se è presente l'impulso di clock;
- Se J=K=1 lo stato prossimo è il complemento dello stato presente.

## Sintesi di un Contatore Binario
![[Pasted image 20260421125504.png]]![[Pasted image 20260421125614.png]]
![[Pasted image 20260421125639.png]]![[Pasted image 20260421125706.png]]

## Contatore Binario Up-Down
![[Pasted image 20260421125733.png]]