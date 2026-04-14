
I principali protocolli di sicurezza per le VPN sono:
- IPsec (IP security)
- SSL/TLS (SecureSockets Layer/Transport Layer Security)
- BGP/MPLS (Border Gateway Protocol/Multiprotocol Label Switching)

# IPsec

1. **Authentication Header (AH)**: garantisce autenticazione e integrità del messaggio ma non offre confidenzialità;
2. **Encapsulating Security Payload (ESP)**: fornisce autenticazione, confidenzialità e integrità del messaggio;
3. **Internet Key Exchange (IKE)**: implementa lo scambio delle chiavi per realizzare il flusso crittografato.

Quando due host devono inviarsi dei dati tramite la VPN, usando AH o ESP, è necessario instaurare prima una connessione logica tra loro, detta **Security Association(SA)** e per sta stabilirla viene usato IKE.
## Protocollo IKE

 Il **Protocollo IKE** realizza un collegamento peer-to-peer in due fasi: 
 1. Tra due i host viene creata una Security Association per IKE, ovvero un canale da utilizzare per i messaggi di IKE;
 2. Poi viene utilizzata la SA per negoziare Security Association per altri protocolli(IPsec SA);


## AH e ESP

Sia AH che ESP possono essere utilizzati in modalità trasporto oppure in modalità tunnel:
- **modalità trasporto**: si aggiungono gli header dei protocolli utilizzati tra l'header IP e l'header di protocollo di trasporto,
- **modalità tunneling**: il pacchetto IP originario viene interamente incapsulato, si effettua cioè il tunneling.

### **Protocollo AH ed ESP**

Fornisce servizi di autenticazione, integrità e protezione da attacchi di tipo replay.

### **SSL/TLS**

**TLS** è un protocollo di livello Session dello Stack ISO/OSI ed opera al di sopra del protocollo di livello Transport. **SSL** è stato originariamente proposto da Netscape Communications, ma è un protocollo open. Non sono compatibili, ma vengono implementati entrambi rendendoli interoperabili.
Il protocollo **SSL/TLS** è composto da due livelli: **Record Protocol** e **Handshake Protol**.