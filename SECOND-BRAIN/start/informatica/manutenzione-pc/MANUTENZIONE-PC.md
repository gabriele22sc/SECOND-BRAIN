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

