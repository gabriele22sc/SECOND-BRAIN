Un proxy è il servizio, offerto da un server, che funge da intermediario tra un client e il server di destinazione, gestisce le richieste tra quest'ultimi.
# PROXY SERVER

È il server che intercetta e gestisce il traffico tra due dispositivi, reti o protocolli; operando a livello Application. I proxy sono un gateway che opera da intermediario tra computer e siti Web principalmente. Vengono impiegati come firewall, filtri, cache o per facilitarne le connessioni vicine; le configurazioni del Proxy Server permettono loro di svolgere alcuni compiti:
- **connettività**;
- **privacy**;
- **caching**;
- **monitoraggio**;
- **amministrazione**;
- **filtraggio**;
- **restrizioni**.

# CHE COSA FA UN SERVER PROXY:

inoltra il traffico tra il tuo dispositivo e il Web, garantendo che il tuo browser non sia mai a diretto contatto con i siti che visiti. Quando viene inviata una richiesta Web, essa raggiunge prima il server proxy e poi quest'ultimo invia la richiesta al server Web e inoltra la risposta al tuo dispositivo.

# COME FUNZIONA?

Un server proxy invia le richieste Internet alle rispettive destinazioni e, dopo aver ricevuto le risposte, le inoltra al tuo dispositivo. L'unico punto di contatto tra la rete locale del tuo dispositivo e i siti Web che visiti è il proxy stesso.

# TIPI DI PROXY

- **Single Proxy**: Un singolo server proxy che gestisce tutte le richieste di rete per un client o un gruppo di client. È un punto centrale per il routing del traffico, utile per anonimato, caching e sicurezza, ma può diventare un collo di bottiglia.

- **Topology Proxy**: Si riferisce all'architettura di distribuzione dei proxy in una rete. Può includere configurazioni come **proxy inversi, proxy a cascata, bilanciamento del carico** o una rete di proxy distribuiti per migliorare scalabilità, sicurezza e prestazioni.

Ad esempio, potremmo avere più proxy disposti verticalmente con una topologia gerarchica dove:
- proxy d'ingresso che gestisce le connessioni esterne;
- proxy intermedi filtrano, memorizzano cache o bilanciano il traffico;
- proxy finali che comunicano con i server di destinazione.
Questa configurazione garantisce **scalabilità**, **sicurezza** e **gestione del traffico**.

## **Architettura Verticale (Multiple Proxy, Vertically Topology)**

**Struttura Gerarchica:** I proxy sono disposti su più livelli, formando una gerarchia in cui ogni livello gestisce specifiche funzioni prima di inoltrare il traffico al livello successivo.​

**Funzionamento:** Il traffico passa attraverso una sequenza di proxy, ciascuno responsabile di compiti come autenticazione, filtraggio dei contenuti o caching. Questo approccio permette un controllo dettagliato e una gestione modulare delle richieste.​

**Vantaggi:** Offre una gestione centralizzata delle politiche di sicurezza e può isolare diversi segmenti della rete, migliorando la sicurezza complessiva.​

**Svantaggi:** La presenza di più livelli può introdurre latenze aggiuntive e rappresentare punti singoli di guasto, riducendo la resilienza del sistema.​

## **Architettura Orizzontale (Multiple Proxy, Horizontally Topology)**

**Struttura Parallela:** I proxy sono distribuiti in parallelo, senza una gerarchia definita, e lavorano insieme per gestire il traffico in modo collaborativo.​

**Funzionamento:** Le richieste dei client possono essere instradate a qualsiasi proxy disponibile, che esegue tutte le funzioni necessarie prima di inoltrare il traffico al server di destinazione. Questo modello favorisce il bilanciamento del carico e l'efficienza nella gestione delle risorse.​

**Vantaggi:** Migliora la scalabilità e la tolleranza ai guasti, poiché il traffico può essere facilmente redistribuito tra i proxy in caso di sovraccarico o malfunzionamenti.​

**Svantaggi:** La gestione coerente delle politiche di sicurezza e delle configurazioni può risultare più complessa, richiedendo strumenti e processi aggiuntivi per garantire l'uniformità.