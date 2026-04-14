
# Visualizzare i processi
Per visualizzare i processi utilizziamo il comando `ps`(process status, stato dei processi):
```
kali >ps
PID      TTY      TIME      CMD
39695    pts/0    00:00:01  zsh
39665    pts/0    00:00:00  ps
```

Il kernel di linux assegna sequenzialmente un identificativo i processo(`PID`, process ID) univoco man mano che i processi vengono creati. 
Se aggiungiamo l'opzione `aux` visualizza tutti i processi in esecuzione sul sistema da parte di tutti gli utenti.
```
kali >ps aux
```
le colonne più importanti dell'output sono:
- `USER`, l'utente che ha invocato il processo;
- `PID`, l'identificativo(ID) del processo;
- `%CPU`, la percentuale di CPU utilizzata dal processo;
- `%MEM`, la percentuale di memoria utilizzata dal processo;
- `COMMAND`, il nome del comando che ha avviato il processo.

# Filtrare per il nome del processo
Dopo aver avviato un framework di exploitation Metasploit:
```
kali >msfconsole
```
proviamo ad usare il seguente comando per filtrare la ricerca:
```
kali >ps aux | grep msfconsole
1:36  ruby  /usr/bin/msfconsole
root  39892  0.0  0.0  4304  940  pts/2 S+  15:18  0:00 grep msfconsole
```
possiamo avere delle informazioni fondamentali: quante risorse sono utilizzate da Metasploit, consultando la terza colonna(CPU): nell'esempio utilizza il 35,1% della CPU, mentre la quarta colonna indica che sta usando il 15,2% della memoria.


# Trovare i processi che consumano di più con `top`
Quando utilizzi il comando `ps`, i processi vengono visualizzati nell'ordine in cui sono stati avviati. Dal momento che il kernel assegna i PID nell'ordine in cui vengono avviati, di fatto i processi sono ordinati per numero PID. A volte può essere utile sapere quali processi usano più risorse. 
A questo scopo si può usare il comando `top` che visualizza i processi ordinandoli in base alle risorse impiegate, partendo dal valore più grande. `top` aggiorna dinamicamente l'elenco ogni 3 secondi


# Cambiare la priorità dei processi con `nice` 
Questo comando serve a modificare la priorità di un processo nel kernel. Nel sistema esistono svariati processi in esecuzione contemporaneamente, i quali si contendono le risorse disponibili. Il kernel è colui che ha l'ultima parola sulla priorità di un processo, con il comando `nice` si può regolare la priorità di un processo.
I suoi valori vanno da -20 a +19, il valore predefinito è 0:
- un valore elevato indica una priorità bassa;
- un valore ridotto indica una priorità elevata.
Il proprietario del processo può abbassarne la priorità, ma non elevarla, mentre l'utente root può impostare arbitrariamente il valore di `nice` su quello che preferisce. Quando si avvia un processo, è possibile impostare il livello di proprietà con il comando `nice`, modificandolo dopo l'avvio con il comando `renice`. Il comando `nice` richiede di **incrementare** il valore di `nice`, mentre il comando `renice` richiede un **valore assoluto** di `nice`.


## Impostare la priorità all'avvio di un processo
Avendo un processo denominato `slowprocess` con la posizione `/bin/slowprocess`. Per velocizzare il completamento, lo avviamo con il comando `nice`:
```
kali >nice -n -10 /bin/slowprocess
```
il comando modifica di `-10` il valore di `nice`, aumentandone in tal modo la priorità e allocandogli più risorse. Se volessimo assegnare al processo `slowprocess` una priorità inferiore, possiamo aumentare di `10` il valore di `nice`:
```
kali >nice -n 10 /bin/slowprocess
```


## Cambiare la priorità di un processo in esecuzione con `renice`
Il comando `renice` richiede un valore tra -20 e 19 , impostando la priorità sul livello specificato invece di aumentare o diminuire rispetto al livello a cui è stato avviato. `renice` richiede il PID del processo interessato, non il nome se `slowprocess` usa una quantità di risorse sul sistema e volete quindi ridurne la priorità, consentendo ad altri processi di aumentare la propria e di usare più risorse, potete usare `renice` su `slowprocess` assegnandogli un valore `nice` più elevato, in questo modo:
```
kali >renice 19 6996
```


# Terminare i processi
Processi che occupano tante risorse, oppure che hanno comportamenti inusuali o che restano congelati. Spesso, un processo che mostra comportamenti di questo tipo viene chiamato *processo rogue*. Il sintomo più problematico è lo spreco di risorse utilizzate dal *processo rogue*, che potrebbero essere allocate, con migliori risultati, ad altri processi.
Per arrestare l'esecuzione di un processo basta eseguire il comando `kill`. Dispone di 64 diversi segnali di `kill`, ognuno di essi presenta differenze: la sua sintassi è: `kill-segnale PID`. L'opzione relativa al segnale è facoltativa e se non viene specificata, è impostata per default su `SIGTERM`.

| Nome del segnale | Numero per l'opzione | Descrizione                                                                                                                                                                                                                                                           |
| ---------------- | -------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `SIGHUP`         | 1                    | è noto come segnale di Hangup(HUP), interrompe il processo interessato e lo riavvia con lo stesso PID                                                                                                                                                                 |
| `SIGINT`         | 2                    | è noto come il segnale di Interrupt(INT). È un segnale di `kill` debole che funziona nella maggior parte dei casi, ma potrebbe anche non funzionare.                                                                                                                  |
| `SIGQUIT`        | 3                    | È noto come segnale core dump. Termina il processo e ne salva le informazioni in memoria, quindi salva queste informazioni nella directory di lavoro corrente in un file di nome core. I motivi per cui può tornare utile vanno al di là dello scopo di questo libro. |
| `SIGTERM`        | 15                   | È noto come segnale di Termination(TERM). È il segnale predefinito del comando `kill`.                                                                                                                                                                                |
|                  | 9                    | È il segnale di `kill` assoluto. Forza l'arresto del processo inviandone le risorse a un device speciale, `/dev/null`                                                                                                                                                 |
Utilizzando il comando `top`, è possibile identificare quali processi perfettamente legittimi, ma in alcuni casi si può trattare di processi malevoli che si appropriano delle risorse e per questo vanno terminati. Se vuoi solo riavviare il processo con il segnale HUP, aggiungi al comando `kill` l'opzione -1, in questo modo:
```
kali >kill -1 6996
```
Nel caso di un processo rogue o malevolo, la soluzione migliore è inviare un segnale `kill -9` quello di kill assoluto, con il quale hai la certezza di terminare il processo.
```
kali >kill -9 6996
```
Se non conoscete il PID di un processo, per terminarlo puoi usare il comando `killall`, al quale puoi passare come argomento il nome del processo, invece del suo PID.
Per esempio, un processo ipotetico di nome `rogueprocess` può essere killato in questo modo:
```
kali >killall -9 rogueprocess
```



# Esecuzione di processi in background
A volte è necessario eseguire un processo in background invece di attendere il suo nel terminale. Supponiamo per esempio di voler lavorare su uno script in un editor di testi. Apriamo il nostro editor e digitiamo:
```
kali >mousepad newscript
```
In questo caso, la Z shell apre l'editor di testo Mousepad per creare il file newscript. Mentre lavoriamo nell'editor, il terminale è occupato a eseguirlo; se ritorniamo, noteremo che sta eseguendo l'editor di testo e che non possiamo inserirvi nuovi comandi.
L'esecuzione di un processo in un background significa semplicemente che il processo viene eseguito senza bisogno del terminale: in tal modo il terminale può essere usato per altri scopi. Per avviare l'editor in background, è sufficiente aggiungere una "e" commerciale(&) alla fine del comando, in questo modo:
```
kali >mousepad newscript &
```
Quando si apre l'editor di testo, il terminale ora torna al prompt dei comandi, al quale possiamo inserire altri comandi mentre continuiamo la modifica del file *newscript*. Questa pratica può tornare utile per tutti i processi che devono essere eseguiti per periodi prolungati, quando il terminale deve rimanere libero.

# Portare un processo in primo piano
Per portare in primo piano un processo puoi utilizzare il comando `fg`, esso richiede il PID del processo da portare in primo piano:
```
kali >fg 1234
```
Se non conosci il PID di un processo puoi utilizzare il comando `ps` per scoprirlo.


# Pianificazione dei processi
In Linux esistono due modi per pianificare un processo: `at` e `cron`. Il comando `at` serve a impostare il demone `atd`, che serve a pianificare l'esecuzione di un'attività in un certo momento nel futuro. Il demone `cron` è più adatto alla pianificazione di attività che devono essere eseguite ogni giorno, settimana o mese.
Il demone `atd` serve a pianificare l'esecuzione di un comando o di un insieme di comandi nel futuro. Esistono vari formati con cui può essere specificato l'argomento temporale:

| Formato temporale      | Significato                                                                           |
| ---------------------- | ------------------------------------------------------------------------------------- |
| `at 7:20pm`            | Esecuzione pianificata alle 19:20(7:20 pm in notazione americana) nel giorno corrente |
| `at 7:20pm June 25`    | Esecuzione pianificata alle 19:20 del 25 giugno                                       |
| `at noon`              | Esecuzione pianificata a mezzogiorno del giorno corrente                              |
| `at noon June 25`      | Esecuzione pianificata a mezzogiorno del 25 giungo                                    |
| `at tomorrow`          | Esecuzione pianificata domani                                                         |
| `at now + 20 minutes`  | Esecuzione pianificata fra 20 minuti da ora                                           |
| `at now + 10 hours`    | Esecuzione pianificata fra 10 ore da ora                                              |
| `at now + 5 days`      | Esecuzione pianificata fra 5 giorni da ora                                            |
| `at now + 3 weeks`     | Esecuzione pianificata fra 3 settimane da ora                                         |
| `at 7:20pm 06/25/2019` | Esecuzione pianificata alle 19:20 del 25 giugno 2019                                  |
