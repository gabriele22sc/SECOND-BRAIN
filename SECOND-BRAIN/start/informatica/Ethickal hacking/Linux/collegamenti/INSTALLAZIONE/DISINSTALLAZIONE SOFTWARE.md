# apt-get(Advanced Packaging Tool)
`apt-get` può essere utilizzato per scaricare e installare nuovi pacchetti software, ma lo si può usare anche per gli aggiornamenti.

## Ricerca di un pacchetto
Prima di scaricare un pacchetto software, si può ,.
```
apt-cache search parolachiave
```


## Installazione di un software |
Per scaricare il software basta inserire
```
apt-get install nomepacchetto
```

## Rimozione di un software
Per rimuoverlo:
```
apt-get remove nomepacchetto
```
il comando `remove` non elimina i file di configurazione, quindi puoi reinstallare lo stesso pacchetto in futuro senza doverlo riconfigurare. Se vuoi rimuovere i file di configurazione insieme al pacchetto, puoi utilizzare l'opzione `purge`.
```
kali >apt-get purge snort
```
insieme all'istallazione di snort, nel nostro caso, vengono installate anche librerie e dipendenze che posso essere utilizzate anche da altri software. Per rimuovere anche queste utilizziamo:
```
kali >apt autoremove snort
```


## Aggiornamenti dei pacchetti
Gli aggiornamenti dei software non vengono installati automaticamente, per installarli dobbiamo richiederli. `update`(aggiornamento) e `upgrade` sono due cose diverse: un aggiornamento si limita ad aggiornare l'elenco dei pacchetti disponibili per il download dal repository, mentre con un upgrade si aggiorna il pacchetto all'ultima versione presente nel repository.
Quindi per aggiornare tutti i pacchetti non aggiornati utilizziamo `apt-get update`.
Per eseguire l'upgrade dei pacchetti del sistema si usa invece il comando `apt-get upgrade`.