Il **firewall** separa la LAN aziendale dalla WAN pubblica filtrando tutti i pacchetti entranti e uscenti, da e verso una rete o un computer, secondo regole prestabilite (policy) che contribuiscono alla sicurezza della rete stessa.

Firewall in LAN aziendali: realizzato con software incluso nel router oppure implementato su hardware dedicato.

![[firewall.png]]

# Categorie di firewall
I firewall si possono distinguere sostanzialmente in tre categorie in base al livello dello stack TCP/IP cui operano:
- **Application Level Firewall**: application level, Analizza il contenuto del traffico fino al livello dell’applicazione (es. HTTP, FTP, DNS);
- **Packet Filter Firewall**: network o transport level, Controlla pacchetti in base a indirizzi IP, porte e protocolli;
- **Stateful Packet Inspection Firewall**: network e transport level, Tiene traccia dello stato delle connessioni, permettendo o bloccando pacchetti in base al contesto della connessione.

La sintassi della configurazione di un firewall è basata su un meccanismo di lista di controllo degli accessi ACL (Access Control List). Le ACL sono definite come insiemi di una o più regole, ognuna delle quali consente o nega il traffico in base ai parametri indicati.
L'ultima istruzione di una ACL è sempre una negazione implicita <u>"deny ip any any"</u> che nega qualsiasi tipo di traffico; si tratta di una regola inserita automaticamente alla fine di ogni ACL, anche se non visibile. Per questo motivo è fondamentale che in una ACL sia presente almeno un <u>“permit”</u>, diversamente l’unico risultato sarebbe la negazione di qualsiasi traffico per ogni direzione.
- vengono elaborate in maniera sequenziale in base all’ordine in cui sono state inserite;
- possono essere  **Standard ACL**, oppure estese, **Extended ACL** .

