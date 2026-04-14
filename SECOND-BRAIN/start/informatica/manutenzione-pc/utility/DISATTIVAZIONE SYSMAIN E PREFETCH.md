# <mark style="background: #ABF7F7A6;">DISABILITAZIONE SYSMAIN</mark>:
Per disattivare il servizio Superfetch (ora chiamato SysMain) su Windows, segui questi passaggi:

### Apri il menu "Esegui":

Premi Windows + R sulla tastiera.

### Accedi ai Servizi:

Digita services.msc nella finestra di dialogo e premi Invio.

### Trova "SysMain":

Nella finestra "Servizi", scorri verso il basso e cerca il servizio chiamato SysMain (prima era chiamato Superfetch).

## Disabilita il servizio:

Fai clic destro su SysMain e seleziona Proprietà.

Nella finestra che si apre, sotto la sezione "Tipo di avvio", seleziona Disabilitato.

Clicca su Arresta per fermare il servizio immediatamente, se è in esecuzione.

Premi OK per confermare.

Riavvia il computer (facoltativo, ma consigliato).

Così facendo, Superfetch (SysMain) sarà disattivato e non verrà avviato automaticamente al prossimo avvio del sistema. Se desideri riattivarlo in futuro, puoi ripetere il processo e impostare il tipo di avvio su "Automatica" o "Manuale".



# <mark style="background: #ADCCFFA6;">DISABILITAZIONE PREFETCH</mark>:

Il Prefetch è una funzionalità di Windows che aiuta a velocizzare l'avvio delle applicazioni memorizzando i dati relativi a quelle applicazioni per un accesso più rapido in futuro. Sebbene non ci sia un'opzione diretta nell'interfaccia grafica di Windows per disattivare il Prefetch, puoi farlo attraverso il registro di sistema.

## Ecco come disattivare il Prefetch in Windows:

### Apri l'Editor del Registro:

Premi Windows + R sulla tastiera.

Digita regedit e premi Invio. (Accetta l'UAC, se richiesto.)

### Naviga nel Registro:

Vai al seguente percorso nel Registro:

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management\PrefetchParameters

Modifica il valore di EnablePrefetcher:

Nella parte destra della finestra, trova la voce EnablePrefetcher.

Fai doppio clic su EnablePrefetcher.

Imposta il valore su 0 per disabilitare il Prefetch (i valori possibili sono 0, 1, 2, o 3).

0: Disabilita il Prefetch.

1: Abilita il Prefetch solo per l'avvio.

2: Abilita il Prefetch solo per le applicazioni.

3: Abilita il Prefetch per entrambi (avvio e applicazioni).

Salva e riavvia il sistema:

Fai clic su OK per salvare le modifiche.

Riavvia il computer per applicare le modifiche.

## Attenzione:

La disattivazione del Prefetch può rallentare il tempo di avvio di alcune applicazioni, perché Windows non caricherà in anticipo i dati relativi a tali applicazioni. È consigliato disattivarlo solo se necessario, per esempio su computer con risorse hardware limitate o per risolvere specifici problemi di prestazioni.