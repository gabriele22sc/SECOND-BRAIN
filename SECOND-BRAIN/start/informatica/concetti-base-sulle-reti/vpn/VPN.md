[[Protocolli VPN]]

Una VPN(Virtual Private Network) è una rete privata virtuale creata all'interno di un'infrastruttura di rete pubblica, ad esempio Internet.

# Tipi di VPN
Esistono due tipi principali di VPN:

### **Remote-access VPN**

porta qualsiasi applicazione dati, voce o video al desktop remoto, emulando il desktop dell'ufficio principale. Viene realizzata con un server di accesso alla rete(**NAS**) e un <u>software VPN client</u>. 
#### Funzionamento 

il NAS richiede all'utente di fornire credenziali valide per accedere alla VPN.  Per autenticare le credenziali, il NAS utilizza il proprio processo di autenticazione o si avvale di un server di autenticazione separato in esecuzione sulla stessa rete come un **RADIUS AAA Server**. L'acronimo **AAA** indica i 3 servizi che il server RADIUS fornisce:
- **Authentication**;
- **Authorization**;
- **Accounting**;

### **Site-to-site VPN**
alternativa alle WAN e consente alle aziende di ampliare le risorse di rete alle filiali, agli uffici domestici e alle sedi di partner. Realizzata come **Intranet-based** o **Extranet-based**.

# La sicurezza nella VPN

### **Autenticazione dell’identità**
processo con cui un sistema informatico o un utente verifica la corretta identità di un altro
sistema informatico, applicativo o utente che vuole comunicare attraverso una connessione, per poi concedergli l’autorizzazione a usufruire dei relativi servizi associati, MultiFactor Authentication (MFA).

I protocolli per la sicurezza nelle VPN garantiscono anche integrità e autenticità dei dati, cioè che i pacchetti ricevuti non siano stati modificati e che provengano da fonte certa, mediante i meccanismi di firma digitale e certificato digitale. 
**Accounting**: azioni volte a misurare e documentare le risorse concesse a un utente in un accesso.

### **Crittografia**
Le VPN per cifrare il traffico in rete utilizzano un’ampia gamma di algoritmi di crittografia (3-DES, CAST, IDEA, ecc.), soprattutto il protocollo Internet Key Exchange (IKE), il cui compito principale è proprio implementare lo scambio delle chiavi per cifrare i pacchetti.

### **Tunneling**
Le VPN possono essere protette in modalità trasporto o in modalità tunnel (tunneling).
Lo scopo dei protocolli di tunneling è aggiungere un livello di sicurezza con l’incapsulamento al fine di proteggere ogni pacchetto nel suo viaggio su Internet. Il termine tunneling si riferisce a un insieme di tecniche per cui un protocollo viene incapsulato in un protocollo dello stesso livello o di livello superiore.


### **VPN di fiducia e VPN sicure**
Nelle **Trusted VPN** la riservatezza dei dati trasmessi attraverso Internet è controllata da un Internet Service Provider (ISP). 
Le **Secure VPN** utilizzano protocolli che consentono la cifratura e il tunneling.
Le **Hybrid VPN** rappresentano il tentativo di unire le caratteristiche delle Trusted VPN e delle Secure VPN, infatti le Secure VPN assicurano la cifratura dei dati ma non assicurano i percorsi;
le Trusted VPN assicurano le proprietà dei percorsi ma non garantiscono un alto livello di sicurezza.