Le reti wireless possono utilizzare onde radio o segnali infrarossi per comunicare attraverso l'etere e, così come le reti wired, possono essere classificate in base all'estensione dell'area fisica che sono in grado di coprire.

# WPAN

- Coprono il campo d'azione di una persona(10-15m);
- sono adatte per reti domestiche o per piccoli uffici;
- utilizza onde radio(per es. Bluethooth) oppure segnali infrarossi (es. irDA);
- utilizza per la domotica.

## Bluetooth

- 2.4 GHz e con una velocità di trasmissione massima di 2 Mbps, standard **IEEE 802.15**;
- Una connessione può essere avviata da qualunque dispositivo che assume il ruolo di **Master**(padrone) rispetto a uno **Slave**(schiavo, ossia i dispositivi connessi), creando una cosiddetta rete Bluetooth piconet; 
- I dispositivi che vogliono collegarsi ad una **piconet** ascoltano, con intervalli di 2,56 secondi, il segnale del Master. La connessione viene generalmente stabilita nel giro di 1,28 secondi. La connessione di due o più dispositivi tramite Bluetooth viene chiamata anche **pairing**(accoppiamento);
- La  **piconet** è costituita da un massimo di 8 dispositivi Bluetooth attivi. Un dispositivo Bluetooth può partecipare contemporaneamente a più piconet in qualità di Slave, ma solo in una come Master, 10 piconet formano una **scatternet**.

Con Bluetooth 5.0 i dispositivi possono utilizzare velocità di trasferimento dati fino a 2 Mbps, il doppio rispetto a Bluetooth 4.2. I dispositivi possono anche comunicare su distanze fino a 240 metri(4 volte i 60 metri consentiti da Bluetooth 4.2)

# WLAN

- sono simili alle tradizionali LAN Ethernet cablate;
- lo standard più diffuso per le WLAN è l'IEEE 802.11;

Sono composte da: 
- **Wireless Terminal(WT)**, dispositivi mobili dotati di interfaccia 802.11,
- **Access Point(AP)**, che fanno da bridge o gateway.

L'insieme formato dall'Access Point e dalle stazioni poste nella sua zona di copertura è detto **Basic Service Set(BSS)**, ovvero insieme di servizi di base e costituisce una **cella**. Due o più BSS collegati tra loro da un Wireless Distribution System costituiscono un ESS(Extended Service Set), che sarebbe un'unica WLAN.

**BSS parzialmente sovrapposti**: permettono di fornire una copertura continua;
**BSS fisicamente disgiunti**: non condividono alcuna parte della loro copertura radio;
**BSS co-locati** (diversi BSS nella stessa area): possono fornire una ridondanza alla rete o permettere prestazioni superiori;

Lo standard 802.11 gestisce la mobilità delle stazioni distinguendo 3 tipi di transizioni: **transizione statica**; **transizione tra BSS**; **transizione tra ESS**. In quest'ultimo, la connessione attiva viene chiusa in quanto ci troviamo di fronte al passaggio da una WLAN a un'altra.

La configurazione di un AP in una rete aziendale prevede l'impostazione dei parametri: 
- SSID(Service Set Identifier);
- Potenza;
- Canale;
- Crittografia;
- Incapsulamento;
- NAT e DHCP.


# WMAN

Consentono di distribuire dati su di un agglomerato di case tramite una potente antenna. Questa fornisce un'alternativa al costoso cablaggio dell'ultimo miglio. Il collegamento può essere:
- **point-to-point**, una coppia di bridge wireless collegati alla rete aziendale e a un'antenna direzionale;
- **point-to-multipoint**, un'antenna centralizzata omnidirezionale e una serie di antenne direzionali puntate verso l'antenna centrale.

Dallo standard IEEE 802.16 è nato il progetto WiMAX Forum: consorzio di imprese, con ruolo simile alla Wi-Fi alliance per IEEE 802.11.

La trasmissione può essere:
- **Non-line-of-sight**, su frequenze basse, utilizzata in ambienti urbani; il range va dai 2GHz/11GHz e il computer si connette aalla rete WiMAX tramite piccole antenne(dongle) portatili da collegare direttamente al computer;
- **Line-of-sight**, su frequenze molto più alte, utilizzata in aree dove la probabilità che il segnale venga schermato sono molto basse; questa funziona con frequenze vicine ai 60 Ghz ed è ideale per coprire aree molto estese;
- Offrono applicazioni mobili che coprono vaste aree, come uno stato o un continente;
- sono offerte a livello regionale e nazionale dai Wireless Internet Service Providers(WISP) che garantiscono la realizzazione di infrastrutture;
- accordi di roaming permettono connettività globale.


# La sicurezza nelle reti wireless

## Sniffing

Attività di intercettazione passiva dei dati che transitano in una rete. Usato per monitorare il traffico o intercettazione fraudolenta di dati sensibili. Efficaci meccanismi di crittografia consentono di mantenere la segretezza dei dati.

## Accesso non autorizzato 

Accesso a una rete privata senza esplicita autorizzazione. La tecnica più utilizzata è quella di servirsi di un **Access Point Rouge(APR)** cioè un AP non autorizzato. Per ostacolare l'accesso non autorizzato è necessaria l'autenticazione reciproca trai WT e gli AP.

**Sostituzione del SID(Security IDentifier)**: **spoofing** Sostituzione del SID(identificativo univoco a cui vengono associate delle autorizzazioni) posizionando un Wireless Terminal Rouge tra un utente e un Access Point. Per evitarlo, si può usare il protocollo **SARP**(Secure ARP), che fornisce un tunnel protetto tra client e AP o router.

**Attacco DoS(Denial of Service)**
Attacchi brute force, oppure attacchi che utilizzano forti segnali radio che si sovrappongono ai segnali della rete rendendo inutilizzabili gli AP e i wireless terminal. Per evitarli è possibile proteggere l'edificio dai segnali radio esterni con barriere fisiche.


## Crittografia

**Crittografia WEP(Wired Equivalent Privacy)**
Quando è attivata WEP, viene crittografato il payload del frame da trasmettere utilizzando l'algoritmo di cifratura a flusso, a chiave simmetrica, RC4.

**Crittografia TKIP(Temporal Key Integrity Protocol)**
Evoluzione del WEP, utilizza ancora l'RC4, ma parte con una **chiave temporale** a 128 bit condivisa tra WT e AP, rigenerata a ogni pacchetto o a ogni burst (**distribuzione dinamica**), e aggiunge un IV di altri 128 bit per creare la chiave di crittografia dei dati.

**Crittografia AES(Advanced Encryption Standard)**
Indecifrabile(uncrackabile) grazie all'utilizzo dell'algoritmo di crittografia a blocchi Rijndael al posto de dell'RC4.

**Crittografia WPA(Wi-Fi Protected Access)**
Aggiornamento WEP dotato di distribuzione dinamica delle chiavi e autenticazione reciproca.


## Autenticazione

Realizza tramite il SSID: l'AP consente l'accesso solo ai WT client il cui SSID conincide con quello inviato dall'AP stesso, l'amministratore autorizza un elenco di indirizzi MAC, gli AP rifiuteranno i frame con indirizzo MAC non in elenco;
Implementata con il protocollo **EAP(Extensible Authentication Protocol)** su parte wireless e parte cablata, che utilizza un server di autenticazione.