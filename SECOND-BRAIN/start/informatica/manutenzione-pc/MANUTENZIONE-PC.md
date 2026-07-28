# Manutenzione software
[[DISATTIVAZIONE SYSMAIN E PREFETCH]]

# Ottimizzazione e gestione dei processi
[[GESTIONE E OTTIMIZZAZIONE PC]]
# 1️⃣ Pulizia dei file temporanei e inutili

Apri Esegui (`Win + R`), digita `%temp%`, e premi Invio. 
-> Cancella tutto il possibile. 
-> Ripeti con `%temp%` e `prefetch`. 
-> Usa Pulizia Disco (cleanmgr): Premi `Win + R`, digita `cleanmgr`, scegli l'unità C: e seleziona tutto.

# 2️⃣ Eliminazione di programmi inutili

Vai su Impostazioni > App > App installate e rimuovi programmi che non usi. Oppure usa il comando:

```
wmic product get name
```

o

```
wmic product where "name like 'NomeProgramma%%'" call uninstall /nointeractive

```

# 3️⃣ Disattivare programmi all'avvio

## Troppi programmi all’avvio rallentano il PC. Per disattivarli:

Apri Gestione Attività (Ctrl + Shift + Esc)
-> Vai su Avvio, disabilita i programmi non essenziali.

# 4️⃣ Controllare i processi in background

In Gestione Attività (Ctrl + Shift + Esc), nella scheda Processi, chiudi quelli inutili. Per vedere i servizi attivi: -> Tasklist.

## Puoi terminare un processo con:

```
taskkill /F /IM nomeprocesso.exe
```

# 5️⃣ Deframmentazione e ottimizzazione disco (solo HDD)

Per gli HDD: cerca Deframmenta e ottimizza unità e avvia l’ottimizzazione. Per gli SSD, non serve deframmentare, ma puoi usare il comando:

    Win + R → "dfrgui" → Ottimizza

# 6️⃣ Pulizia del registro di sistema (facoltativa)

Usa un tool sicuro come CCleaner per rimuovere voci obsolete dal registro di sistema.


# 7️⃣ Controllare e rimuovere malware

Usa Windows Defender (Windows Security > Protezione da virus e minacce). Per una scansione più approfondita, usa [Malwarebytes](https://www.malwarebytes.com/).

# 8️⃣ Aggiornare driver e sistema operativo

Aggiorna Windows (`Win + I` > `Windows Update`). Aggiorna driver con Gestione dispositivi (`Win + X` > `Gestione dispositivi`).

# 9️⃣ Controllare lo stato del disco

Digita nel Prompt dei Comandi (cmd) come amministratore:

```
chkdsk /f /r
```

Riavvia il PC e lascia che il controllo si completi.

# 🔹 Manutenzione hardware (facoltativa ma consigliata)

- Pulisci la polvere dentro il case (soprattutto ventole e dissipatore).

- Controlla la temperatura della CPU e GPU (puoi usare HWMonitor o MSI Afterburner).

- Usa una pasta termica nuova sulla CPU ogni 1-2 anni se il PC scalda troppo.

---


DISABILITAZIONE SYSMAIN:
Per disattivare il servizio Superfetch (ora chiamato SysMain) su Windows, segui questi passaggi:

Apri il menu "Esegui":

Premi Windows + R sulla tastiera.

Accedi ai Servizi:

Digita services.msc nella finestra di dialogo e premi Invio.

Trova "SysMain":

Nella finestra "Servizi", scorri verso il basso e cerca il servizio chiamato SysMain (prima era chiamato Superfetch).

Disabilita il servizio:

Fai clic destro su SysMain e seleziona Proprietà.

Nella finestra che si apre, sotto la sezione "Tipo di avvio", seleziona Disabilitato.

Clicca su Arresta per fermare il servizio immediatamente, se è in esecuzione.

Premi OK per confermare.

Riavvia il computer (facoltativo, ma consigliato).

Così facendo, Superfetch (SysMain) sarà disattivato e non verrà avviato automaticamente al prossimo avvio del sistema. Se desideri riattivarlo in futuro, puoi ripetere il processo e impostare il tipo di avvio su "Automatica" o "Manuale".



DISABILITAZIONE PREFETCH:
Il Prefetch è una funzionalità di Windows che aiuta a velocizzare l'avvio delle applicazioni memorizzando i dati relativi a quelle applicazioni per un accesso più rapido in futuro. Sebbene non ci sia un'opzione diretta nell'interfaccia grafica di Windows per disattivare il Prefetch, puoi farlo attraverso il registro di sistema.

Ecco come disattivare il Prefetch in Windows:

Passaggi per disattivare il Prefetch:

Apri l'Editor del Registro:

Premi Windows + R sulla tastiera.

Digita regedit e premi Invio. (Accetta l'UAC, se richiesto.)

Naviga nel Registro:

Vai al seguente percorso nel Registro:

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\Memory Management\PrefetchParameters

Modifica il valore di EnablePrefetcher:

Nella parte destra della finestra, trova la voce EnablePrefetcher.

Fai doppio clic su EnablePrefetcher.

Imposta il valore su 0 per disabilitare il Prefetch (i valori possibili sono 0, 1, 2, o 3).

0: Disabilita il Prefetch.

1: Abilita il Prefetch solo per l'avvio.

2: Abilita il Prefetch solo per le applicazioni.

3: Abilita il Prefetch per entrambi (avvio e applicazioni).

Salva e riavvia il sistema:

Fai clic su OK per salvare le modifiche.

Riavvia il computer per applicare le modifiche.

Attenzione:

La disattivazione del Prefetch può rallentare il tempo di avvio di alcune applicazioni, perché Windows non caricherà in anticipo i dati relativi a tali applicazioni. È consigliato disattivarlo solo se necessario, per esempio su computer con risorse hardware limitate o per risolvere specifici problemi di prestazioni.