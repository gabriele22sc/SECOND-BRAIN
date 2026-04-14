# Link:

[[NGROK]]
[[VISUALIZZAZIONE SERVIZI-PROCESSI ATTIVI]]


# Abilitazione di #script :

-  apri Powershell come amministratore;
- ```Get-ExecutionPolicy``` -> per vedere la politica di esecuzione corrente (di base "Restricted");
-  ```Set-ExecutionPolicy RemoteSigned``` -> per permettere l'esecuzione degli script scaricati da internet solo se firmati digitalmente.


# Killa i processi con un determinato PID:

```
taskkill /PID <pid> /F
```

# Per contare tutti i file e cartelle nel pc
`cd C:\`

```
dir /s /b | find /v /c ""
```
## Per contare solo i file:
`cd C:\`

```
dir /s /b /a-d | find /v /c ""
```

## Per contare solo le cartelle:
`cd C:\`
```
dir /s /b /ad | find /v /c ""
```

## SPIEGAZIONE COMANDI:
`dir /s /b`:
`/s` -> fa sì che il comando analizzi le sottocartelle;
`/b` -> utilzza il formato "bare", mostrando il percorso completo di ogni elemento;
`|` -> reindirizza l'output del comando dir a find;
`find /v /c ""`:
`/v ""` -> seleziona tutte le righe che non contengono la stringa vuota;
`/c` -> conta il numero di righe.

# INTERROGAZIONE DNS

Per interrogare i servizi DNS ed ottenere nomi host(windows):

```
nslookup
```

# Aggiornare la Powershell
Da Powershell:
```
winget install -—id Microsoft.PowerShell —-source winget
```
