L'utente root fa parte del gruppo root per impostazione predefinita, ogni nuovo utente del sistema deve essere aggiunto a un gruppo per ereditare i permessi di quel gruppo. Abbiamo tre diversi tipi di permessi:
- `r` permesso di lettura. Concede solo il permesso di aprire e visualizzare un file;
- `w` permesso di scrittura. Consente agli utenti di visualizzare e modificare un file;
- `x` permesso di esecuzione. Consente agli utenti di eseguire un file.

# Concedere la proprietà a un singolo utente
Per passare la proprietà di un file a un altro utente, il quale può di conseguenza controllare i permessi, possiamo usare il comando `chown`(change owner):
```
kali >chown bob /tmp/bobsfile
```

# Concedere la proprietà a un gruppo
Per trasferire la proprietà di un file da un gruppo a un altro, si può usare il comando `chgrp`:
```
kali >chgrp security newIDS
```


# Controllo dei permessi
Per controllare i permessi che sono stati concessi a un utente per un file o directory basta eseguire:
```
kali >ls -l /usr/share/hashcat
drwxr-xr-x  5  root  root  4096   Dec 5 10:47  charsets
-rw-r--r--  1  root  root  33685504  June 28 2018  hashcat.hcstat
-rw-r--r--  1  root  root  33685504  June 28 2018  hashcat.hctune
```
dove rispettivamente:
- il primo carattere definisce il tipo di file: `d` sta per directory mentre `-` indica un file;
- i caratteri successivi rappresentano i permessi per il proprietario, primo set(3 caratteri), il gruppo, secondo set, e terzo set gli utenti;
- il numeri di link;
- il proprietario del file;
- la dimensione del file in byte;
- la data di creazione o ultima modifica del file;
- il nome del file.

Esistono tre tipi di caratteri:
1) `r` sta per read;
2) `w` per write;
3) `x` per execution.

# Cambiare i permessi
I permessi possono essere modificati solo dal proprietario del file o dall'utente root. Esistono diversi metodi per cambiare i permessi

## Notazione numerica
Per riferirci ai vari permessi possiamo usare un'abbreviazione che consente di usare un set di permessi `rwx`. Tramite i sistema ottale possiamo rappresentare la posizione del permesso: ON sarà 1, OFF sarà 0.
![[rwx-table.jpg]]
potremo quindi cambiare i permessi con il comando:
```
kali >chmod 774 hashcat.hcstat
```

## Cambiare i permessi con UGO
Il metodo simbolico viene indicato come la sintassi UGO(User Group Others), `-` rimuove un permesso, `+` aggiunge un permesso e `=` imposta un permesso.
```
kali >chmod u-w hashcat.hcstat
```
oppure per cambiare più permessi alla volta
```
kali >chmod u+x, o+x hashcat.hcstat
```


# Assegnare un permesso di esecuzione root a un nuovo strumento
Linux assegna di base a file e directory i permessi predefiniti 666 per i file e 777 per le directory. Ciò vuol dire che non avrai i permessi per eseguire un file dopo averlo scaricato. Nella maggior parte dei casi per eseguire un file è necessario procedere all'assegnazione manuale dei permessi di esecuzione utilizzando il comando `chmod`:
```
kali >chmod 766 newhackertool
```

# Permessi più sicuri con le maschere
È possibile cambiare i permessi base assegnati a file e directory creati da ogni utente con il metodo `umask`(user file-creation mask) e rappresenta i permessi che vuoi rimuovere dai permessi base di un file o directory così da renderli più sicuri. La maschera `umask` viene sottratto dal numero dei permessi per ottenere i nuovi permessi, ciò significa che quando vengono creati nuovi file o directory, i permessi vengono impostati sul valore predefinito, meno il valore di `umask`.

# Permessi speciali
Oltre a i tre permessi `rwx`, linux ha altri tre permessi speciali: SUID(set user ID), SGID(set group ID) e lo sticky bit.

# Concedere temporaneamente i privilegi di root con SUID
Può capitare un caso in cui un file dispone di permessi di root per tutti gli utenti, anche quelli non root, per poterlo eseguire. Ad esempio: un file che consente agli utenti di cambiare la password per accedere a `/etc/shadow`, che contiene le password utente. In questo caso è possibile concedere i privilegi del proprietario per eseguire il file: basta impostare il bit SUID.

Il bit SUID indica che qualsiasi utente può eseguire il file con i permessi del proprietario, i quali però non si estendono al di là dell'utilizzo di tale file. Per impostarlo si inserisce un 4 prima dei permessi standard: ad esempio un file con i permessi 644 viene rappresentato come 4644 quando si imposta il bit SUID.
```
kali >chmod 4644 nomefile
```

# Concedere i privilegi di root a un gruppo con SGID
SGID assegna privilegi di root temporanei, ma a differenza del precedente assegna quelli del gruppo del proprietario. Impostando il bit SGID, una persona priva dei permessi di esecuzione può eseguire un file, purché il proprietario appartenga al gruppo che detiene il permesso di esecuzione relativo a tale file.
Per quanto riguarda le directory, il bit SGID funziona diversamente: impostandolo su una directory la proprietà dei nuovi file creati in tale directory viene assegnata al gruppo di chi ha creato la directory, non a quello di chi ha creato il file.

# Sticky bit
È un bit di permesso che può essere impostato su una directory e consente agli utenti di eliminare o rinominare file al suo interno. Veniva utilizzato nei sistemi linux più vecchi, nei sistemi più moderni viene ignorato


# Permessi speciali, privilege escalation e hacker
Il *privilege escalation*(acquisizione dei privilegi amministrativi), nella quale un utente standard riesce a ottenere i privilegi di root o di sysadmin con i permessi associati. Una volta ottenuti i privilegi di root, puoi fare il cazzo che ti pare. Uno dei modi con cui puoi riuscirci è il bit SUID.
Per esempio utilizzeremo un file nel sistema con il bit SUID impostato. In questo caso, vogliamo trovare nel file system dei file, per l'utente root o altri sysadmin, sui quali siano impostati i permessi 4000:
```
kali >find / -user root -perm 4000
```
Il comando elabora tutte le sotto-directory di `/` cercando i file di proprietà di root, come specificato dall'opzione `user root`, e che abbiano il bit di permessi SUID impostato `-perm 4000`. Di seguito otterremo:
```
/usr/bin/chsh
/usr/bin/gpasswd
/usr/bin/pkexec
/usr/bin/sudo
/usr/bin/passwd
/usr/bin/kismet_capture
--snip--
```
ci andiamo a posizionare nella cartella `/usr/bin/` dove si trovano la maggior parte di questi file:
```
kali >cd /usr/bin/
kali >ls -l
-snip-
-rwxr-xr-x  1  root  root  176272  Jul 18 2018  stunnel14
-rwxr-xr-x  1  root  root  26696  Mar 17 2018  sucrack
-rwsr-xr-x  1  root  root  140944  Jul 5 2018  sudo
--snip--
```
nella riga in cui troviamo la `s`, essa significa che il SUID è impostato e chiunque esegue il file `sudo` ha i privilegi dell'utente root

