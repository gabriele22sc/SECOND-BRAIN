È una risorsa online, entrato a far parte dei servizi Google nel 2014, integrabile con qualsiasi progetto software web o mobile che consente la gestione di un database NoSQL con elevata disponibilità. Per consentire il funzionamento di tutto ciò è necesssaria un server che renda disponibili, tramite API che forniscano i servizi di autenticazione, storage dei dati, notifiche push, comunicazione tra utenti e altro, sempre dal lato beckend.

# Strutturare dati in Firestore

Abbiamo diverse opzioni per strutturare i dati in Cloud Firestore:
- Documenti;
- Più collezioni;
- Sotto-collezioni all'interno dei documenti.

# Aggiungere dati

Per scrivere dati in Cloud Firestore possiamo:
- Impostare i dati di un documento all'interno di una raccolta, specificando un identificativo del documento;
- Aggiungere un nuovo documento a una raccolta, Firestore genererà automaticamnete l'identificatore del documento;
- Creare un documento vuoto con identificatore generato automaticamente e assegnarvi i dati dopo.

# Transazioni e scritture in batch

Firestore supporta le operazioni atomiche per la lettura e scrittura dei dati, ovvero in una di quest'ultima tutte le operazioni devono riuscire oppure nessuna di essa viene applicata. Esistono due tipi di operazioni atomiche:
- **Transazioni**: insieme di operazioni di lettura e scrittura su uno o più documenti;
- **Scritture in batch**: insieme di operazioni di scrittura su uno o più documenti.

Le transazioni sono utili quando si vuole aggiornare il valore di un campo in base al suo valore corrente o al valore di un altro campo.
[Transazioni e operazioni di scrittura](https://firebase.google.com/docs/firestore/manage-data/transactions?hl=it)

