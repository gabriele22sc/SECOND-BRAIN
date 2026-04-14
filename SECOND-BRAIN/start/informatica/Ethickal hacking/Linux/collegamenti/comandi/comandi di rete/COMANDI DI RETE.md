# ifconfig
Fondamentale per esaminare e interagire con le interfacce di rete attive, puoi usarlo per conoscere le connessioni di rete attive digitando `ifconfig` nel terminale. 
```
kali >ifconfig
eth0: flags=4163<UP, broadcast, RUNNING, MULTICAST> mtu 1500
inet addr:192.168.181.131 netmask 255.255.255.0
Bcast:192.168.181.255
-snip-
lo Linkencap:Local Loopback
inet addr:127.0.0.1 Mask:255.0.0.0
-snip-
wlan0 Link encap:EthernetHWaddr 00:c0:ca:3f:ee:02
```
- `eth0`: un'abbreviazione di ethernet0, è la prima connessione di rete filare. Di seguito è quindi riportato il tipo di rete in uso, seguito da `HWaddr` e da un indirizzo. Si tratta dell'indirizzo univoco a livello mondiale associato a ogni hardware di rete prodotto -in questo caso la scheda di rete, o NIC per network interface card - e noto come indirizzo MAC(Media Access Control).
- La seconda riga contiene le informazioni sull'indirizzo IP attualmente assegnato a quella interfaccia di rete, in questo caso 192.168.181.131.
- Il `Bcast` o indirizzo di broadcast, ossia l'indirizzo utilizzato per inviare informazioni a tutti gli IP della sottorete; poi la maschera di sottorete, che serve a stabilire quale parte dell'indirizzo IP è connessa alla rete locale.
- Successivamente abbiamo un'altra connessione di rete chiamata `lo`, abbreviazione di indirizzo di loopback a volte chiamato localhost. Si tratta di un indirizzo software speciale che serve a connettervi al sistema e che non può essere utilizzato da software e servizi che non sono in esecuzione nel vostro sistema.
- La terza connessione è l'interfaccia `wlan0` e viene visualizzata solo se disponete di un'interfaccia o di una scheda di rete wireless.

# iwconfig
Se hai una scheda wireless USB esterna, puoi usare il comando `iwconfig` per raccogliere informazioni essenziali per l'hacking di reti wireless, come l'indirizzo IP e MAC dell'adattatore, la modalità in cui si trova e altro.
```
kali >iwconfig
wlan0 IEEE 802.11bg ESSID:off/any
Mode:Managed Access Point: Not Associated Tx-Power=20 dBm
-snip-
lo no wireless extensions

eth0 no wireless extensions
```

# Cambiare indirizzo IP
Per cambiare indirizzo IP ti basta digitare `ifconfig` seguito dall'interfaccia di cui si desidera cambiare indirizzo e dal nuovo indirizzo IP da assegnare. Per esempio, per assegnare l'indirizzo IP `192.168.181.115` all'interfaccia `eth0` si immette questo comando:
```
kali >ifconfig eth0 192.168.181.115
```

# Cambiare maschera di rete e indirizzo di broadcast
Con il comando `ifconfig` potete anche cambiare maschera di rete(netmask) e indirizzo di broadcast. Per esempio, se desiderate assegnare alla stessa interfaccia `eth0` una maschera di rete `255.255.0.0` e un indirizzo di broadcast `192.168.1.255`, basta immettere:
```
kali >ifconfig eth0 192.168.181.115 netmask 255.255.0.0 broadcast 192.168.1.255
```

# Spoofing dell'indirizzo MAC
`ifconfig` può essere utilizzato per cambiare l'indirizzo MAC. Per mascherare il proprio indirizzo MAC con l'opzione `down` di `ifconfig`, successivamente inseriamo il comando `ifconfig` seguito dal nome dell'interfaccia(`hw` per hardware,`ether` per Ethernet) e quindi il nuovo indirizzo MAC mascherato. Come ultimo comando, si riattiva l'interfaccia con l'opzione `up` in modo da confermare le modifiche.
```
kali >ifconfig eth0 down
kali >ifconfig eth0 hw ether 00:11:22:33:44:55
kali >ifconfig eth0 up
```

# Assegnazione di nuovi indirizzi IP dal server DHCP
Linux dispone di un server DHCP(Dynamic Host Configuration Protocol) che esegue un demone(daemon), ovvero un processo in esecuzione in background, chiamato `dhcpd` noto come `demone dhcp`. Solitamente per connettersi a Internet da una LAN è necessario disporre di un indirizzo IP assegnato dal server DHCP, dopo aver impostato un indirizzo IP statico, occorre farsi assegnare un nuovo indirizzo IP assegnato dal server DHCP. Per farlo basta riavviare il sistema, ma se non volete potete usare il sistema riportato di seguito per ottenere un nuovo indirizzo assegnato dal server DHCP, senza riavviare tutto.
Per chiedere un indirizzo IP al server DHCP, basta chiamarlo con il comando dhclient seguito dall'interfaccia a cui si desidera assegnare l'indirizzo. I client DHCP variano a seconda della distribuzione Linux:
```
kali >dhclient eth0
```
il comando `dhclient` invia una richiesta `DHCPDISCOVER` dall'interfaccia di rete specificata e quindi ricevere un'offerta dal server DHCP server confermando quindi al server DHCP l'assegnazione dell'indirizzo IP mediante una richiesta dhcp
```
kali >ifconfig
eth0Linkencap:EthernetHWaddr 00:0c:29:ba:82:0f
inet addr:192.168.181.131 Bcast:192.168.181.131 Mask:255.255.255.0
```


# Esaminare il DNS con `dig`
Grazie a questo comando è possibile raccogliere informazioni DNS su un dominio obiettivo. Fra le informazioni si possono trovare l'indirizzo IP del name-server obiettivo, il server e-mail dell'obiettivo e, potenzialmente, qualsiasi altri sottodominio e indirizzo IP.
```
kali >dig hackers-arise.com ns
-snip-
;; QUESTION SECTION:
;hackers-arise.com.   IN  NS

;;ANSWER SECTION:
hackers-arise.com  5  IN  NS  ns7.wixdns.net.
hackers-arise.com  5  IN  NS  ns6.wixdns.net.

;; ADDITIONAL SECTION:
ns6.wixdns.net.  5  IN  A  216.239.32.100
-snip-
```
nella sezione ADDITIONAL SECTION, si può vedere che questa query `dig` mostra l'indirizzo IP del server DNS che serve `hacker-arise.com`

Inoltre, il comando `dig` può servire anche a ottenere informazioni sui server e-mail connessi a un dominio: è sufficiente digitare l'opzione `mx`(mail exchange)
```
kali >dig hackers-arise.com mx
-snip-
;; QUESTION SECTION:
;hackers-arise.com.   IN  MX

;; AUTHORITY SECTION:
hackers-arise.com.  5  IN  SOA ns6.wixdns.net. support.wix.com 2016052216
10800 3600 604 800 3600
```
Le informazioni relative ai server e-mail di `www.hackers-arise.com` sono visualizzate nella sezione AUTHORITY SECTION


# Cambiare server DNS
In alcuni casi, può rivelarsi utile usare un server DNS diverso. A questo scopo si può modificare un file di testo sul sistema, denominato `/etc/resolv.conf`. Apri il file con un editor di testo(mousepad) inserendo:
```
kali >mousepad /etc/resolv.conf
```
successivamente cambiare la voce "nameserver" con il DNS che preferisci. Analogamente puoi eseguire questo comando:
```
kali >echo "nameserver 1.1.1.1"> /etc/resolv.conf
```


# Mappature personalizzate di indirizzi IP
Il file `hosts`, esegue a sua volta una traduzione fra il nome di dominio e indirizzo IP. Si trova in `/etc/hosts` ed è una sorta di server DNS nel quale è possibile specificare una mappatura personalizzata fra indirizzi IP e nomi di dominio. In breve puoi stabilire quale indirizzo IP apre il browser quando inserisci `www.microsoft.com` nella barra di navigazione, bypassando le decisioni del server DNS. Puoi utilizzare anche `mousepad` al posto di `leafpad`:
```
kali >leafpad /etc/hosts
```

pag-34