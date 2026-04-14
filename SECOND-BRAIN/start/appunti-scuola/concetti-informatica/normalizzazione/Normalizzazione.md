La **Normalizzazione** è la fase finale che completa la progettazione di un DB relazionale; dopo aver **proggettato il Modello E/R** ed aver **derivato il modello logico relazionale**. La normalizzazione esamina le tabelle alla ricercando le incongruenze nella loro definizione. 

 Quindi consente di creare le tabelle ben definite, che riescano a facilitare le operazioni di:
 - inserimento;
 - aggiornamento;
 - cancellazione;
 - modifica.

rendendo possibili i cambiamenti nella struttura del modello con l'evolvere delle esigenze aziendali e degli utenti del DB.

# Cosa s'intende per normalizzazione?

Per evitare **ridondanza** e **inconsistenza** dei dati vengono definiti dei criteri: **Forme Normali**. 
Lo scopo della normalizzazione è ottimizzare progressivamente le relazioni non normalizzate fino raggiungere un certo livello di normalizzazione. Fornire un metodo per progettare basi di dati senza anomalie per creare tabelle corrette.

Le regole della normalizzazione sono:
- Ogni tabella ha una chiave primaria;
- Ogni campo contiene un solo valore;
- I campi di una tabella non devono dipendere da altri campi che non siano la chiave primaria;
- Evitare ripetizioni e ridondanza dei dati.


# Prima forma normale

Una relazione si dice in prima forma normale se:

- ogni **attributo** è definito su un **dominio** di valori **atomici**, cioè solo valori elementari, non ulteriormente scomponibili;
- rispetta i **requisiti fondamentali del modello relazionale**: 
	1. <u>tutte le colonne della tabella contengono valori dello stesso tipo</u>;
	2. <u>i valori delle colonne rappresentano informazioni elementari</u>;
	3. <u>tutte le righe della tabella contengono lo stesso numero di colonne</u>
	4. <u>non ci possono essere righe duplicate, quindi ci deve essere un attributo o un insieme di attributi con funzione di chiave primaria</u>;
	5. <u>l'ordine delle righe è irrilevante</u>;


# Seconda forma normale

Una relazione si dice in seconda forma normale se:
- È in prima forma normale;
- Tutti gli attributi non-chiave dipendono dall'intera chiave e non da una parte della chiave;
- La 2FN elimina la dipendenza parziale degli attributi dalla chiave e riguarda il caso di relazioni con chiavi composte.

La seconda forma normale riguarda le tabelle in cui la chiave primaria sia composta da più attributi e stabilisce che, in questo caso, tutte le colonne corrispondenti agli altri attributi dipendano dall'intera chiave primaria.

Troviamo due tematiche importanti:

## Chiavi composte

Una chiave si dice composta quando è formata da più da più attributi. La ridondanza va evitata perché spreca spazio sul disco ed è causa di **anomalie**:
- Anomalia di **aggiornamento**;
- Anomalia di **inserimento**;
- Anomalia di **cancellazione**.

![[magazzino.png]]

**ANOMALIA DI AGGIORNAMENTO**: se il magazzino CA1 cambia indirizzo servirà modificare IndirizzoMagazzino in tutte le colonne di occorrenza di CA1 di Inventario;
**ANOMALIA DI INSERIMENTO**: se viene aperto un nuovo magazzino in mancanza di merci a magazzino, mancheranno anche le informazioni sul suo indirizzo;
**ANOMALIA DI CANCELLAZIONE**: se un magazzino si svuota vengono perse pure le informazioni sul suo indirizzo.

![[suddivisione-magazzino.png]]

Avremo quindi due tabelle:
**Inventario**(<u>Prodotto</u>, <u>Magazzino</u>, Quantità);
Negozi(<u>CodiceMagazzino</u>, IndirizzoMagazzino);

Notiamo che la tabella Inventario ha una **chiave composta** formata dagli attributi Prodotto e Magazzino. Abbiamo le seguenti definizioni:
- **Chiave** o **chiave primaria**: l'insieme di uno o più attributi che identificano in modo univoco una riga della tabella;
- **Chiave candidata**: insieme minimale di attributi che possono svolgere la funzione di chiave;
- **Attributo non-chiave**: campo che non fa parte della chiave primaria.

Inventario(Numero, Prodotto, Magazzino, Quantità, IndirizzoMagazzino)
- **Numero** è chiave candidata;
- {**Prodotto, Magazzino**} è chiave candidata;
- {**Prodotto**, **Magazzino**, **Quantità**} sono un insieme di attributi come questo si dice **superchiave**.



## Dipendenza funzionale

Considerando una relazione con due attributi: **A e B**. Si dice B ha una dipendenza funzionale da A e si indica con **A -> B** se il valore di B varia al variare del valore di A. Quindi:
- B dipende funzionalmente da A;
- A è un **determinante** per B.

Esempio:
**Inventario**(Numero, Prodotto, Magazzino, Quantità, IndirizzoMagazzino)

Avremo quindi:

Numero ->(Prodotto, Magazzino, Quantità, IndirizzoMagazzino);
{Prodotto, Magazzino} -> (Numero, Quantità, IndirizzoMagazzino);
Magazzino -> IndirizzoMagazzino.

Dove:

Numero è determinante per ogni attributo di Inventario;
{Prodotto, Magazzino} è determinante per ogni attributo di Inventario;
Magazzino è determinante per IndirizzoMagazzino.

### Cosa significa?

Ogni **chiave candidata** di una relazione è **determinante** per tutti i suoi attributi. Viceversa ogni determinante per tutti gli attributi di una relazione è **chiave candidata** per quella relazione.

Si ha dipendenza transitiva tra attributi quando un attributo A determina B e B determina C; si dice allora che C dipende transitivamente da A:
	A -> B e B -> C   allora   A -> C transitivamente


# Terza forma normale

Si ha una relazione in terza forma normale quando:
- è in 2FN;
- tutti gli attributi non-chiave dipendono direttamente dalla chiave, cioè non possiede attributi non-chiave che dipendono da altri attributi non-chiave.

La 3FN elimina le dipendenze transitive degli attributi dalla chiave.

![[esempio1.png]]

![[esempio2.png]]

