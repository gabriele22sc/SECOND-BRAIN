**NAT (Network Address Translation)** permette a una rete locale, con classe di indirizzi privata, di accedere a Internet usando un solo IP fornito dall’ISP. NAT usa una tabella contenente la corrispondenza tra i socket interni ed esterni in uso.

## Router con funzionalità NAT:

rapporto 1:1 tra IP server destinazione e IP client.

![[nat.png]]

# Tecnica NAT(Network Address Translation)

Il router NAT (75.120.30.12) della LAN riceve la richiesta del client e, prima di inoltrare i pacchetti in rete sulla sua porta 3000, modifica l’intestazione dei pacchetti in modo che risultino generati dal router NAT stesso (traslazione dell’indirizzo). Contestualmente, inserisce nella tabella contenente la corrispondenza tra le socket, la relativa corrispondenza:

Client                              Router NAT                      Server Destinazione
192.168.1.1:2000    ->    75.120.30.12:3000    ->    200.92.10.10:80

## NAT per IPv6

IPv6 implementa una forma di NAT con scopi del tutto diversi dal NAT per IPv4.  Con IPv6 non serve più “risparmiare” indirizzi pubblici ma serve mettere in comunicazione reti IPv6 con reti IPv4. Per la fase di transizione da IPv4 a IPv6, IETF ha ipotizzato 3 meccanismi di possibile convivenza:
- **Dual-stack**: i dispositivi di rete sono in grado di inoltrare pacchetti IPv4 e pacchetti IPv6;
- **Conversion**: è considerato il NAT per IPv6 realizzato con il protocollo NAT-PT(Network Address Translation - Protocol Translator) che permette la comunicazione tra reti IPv6 e reti IPv4.
- **Tunneling** per IPv6 incapsula il pacchetto IPv6 in un pacchetto IPv4, permettendone il trasporto per reti IPv4. 
La tecnica del dual-stack prevede l’utilizzo del doppio stack IP nella pila di protocolli TCP/IP.

# Tecnica PAT(Port Address Translation)

La tecnica PAT (Port Address Translation) consente al router di utilizzare un singolo indirizzo IP per gestire oltre 64 000 connessioni private contemporaneamente. Questo significa che può traslare più indirizzi IP client per un medesimo indirizzo IP destinazione cambiando solo la porta.