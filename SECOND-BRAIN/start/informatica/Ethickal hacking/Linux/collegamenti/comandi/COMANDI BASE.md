
[[COMANDI DI RETE]]
[[DISINSTALLAZIONE SOFTWARE]]
# pwd(present working directory)
Il comando `pwd` restituisce in che punto della struttura delle directory ci si trova attualmente
```
kali>pwd
/<nomeutente>
```

# whoami
Se vi siete dimenticati con quale utente avete avuto accesso, o se volete verificare se effettivamente siete root, potete usare il comando `whoami`:
```
kali >whoami
root
```

# cd
Per cambiare director dal terminale si usa il comando change directory, `cd`. Per andare alla directori `\etc` utilizzeremo:
```
kali >cd/etc
kali:/etc 
```

per salire di un livello si usa `..`:
```
kali:/etc >cd..
kali >pwd
/
kali >
```
 per salire di due livelli si usa `../..`;
 per salire di tre livelli `../../..`


# ls(list)
Per visualizzare il contenuto di una directory si usa il comando `ls`, molto simile al comando dir di windows. Questo comando elenca sia i file sia le directory contenute all'interno di una directory.
È possibile inserire l'opzione `-l` dopo `ls` che sta per long, ovvero descrizione estesa, e fornisce molte più informazioni, indicando per esempio se un oggetto è un file o una directory, il numero di link, il proprietario, la dimensione, la data e l'ora di creazione o modifica, oltre al nome.
Per visualizzare poi i file nascosti basta mettere l'opzione `-a`:
`ls -l` oppure `ls -la`

# Guida in linea
Tutti i comandi, applicazioni e utility hanno un file di guida che ne illustra l'utilizzo, per utilizzarla basta utilizzare `--help` o `-h` dopo il comando. Ad esempio:
```
nmap -h
```

# man
Oltre al comando di guida, molte applicazioni e comandi hanno una sorta di manuale integrato, la pagina `man`, contenente maggiori informazioni, per esempio una descrizione e un riassunto delle funzioni del comando o dell'applicazione. Per visualizzarla basta digitare `man` prima del nome del comando o dell'applicazione:
```
kali >man aircrack-ng
```


# locate
Il programma più facile da usare per le ricerche è `locate`, seguito da una parola chiave con cui si specifica che cosa volete trovare, il comando esamina l'intero file system e trova ogni occorrenza della parola specificata. Per cercare aircrack-ng basta digitare:
```
kali >locate aircrack-ng
/usr/bin/aircrack-ng
/usr/share/applications/kali-aircrack-ng.desktop
/usr/share/desktop-directories/05-1-01-aircrack-ng.directory
-snip-
/var/lib/dpkg/info/aircrack-ng.md5sums
```

`locate` utilizza un database che viene solitamente aggiornato una sola volta al giorno; se avete creato un file pochi minuti fa, potrebbe non essere visualizzato nell'elenco fino al giorno successivo

# whereis
Se stai cercando un file binario, puoi utilizzare il comando `whereis` per trovarlo. Questo comando non restituisce solamente la posizione del file, ma anche di sorgente e pagina man, se esistono.
```
kali >whereis aircrack-ng
aircrack-ng: /usr/bin/aircrack-ng /usr/share/man/man1/aircrack-ng.1.gz
```



# which
Il comando `which` è ancora più specifico: restituisce solamente la posizione dei file binari nella variabile `PATH` di linux, quest'ultima contiene le directory in cui il sistema operativo va a cercare i comandi eseguiti sulla riga di comando. 
```
kali >which aircrack-ng
/usr/bin/aircrack-ng
```


# find
Il comando `find` è il più potente e flessibile per cercare le utility. È in grado di iniziare la ricerca in qualsiasi directory specificata e di cercare utilizzando diversi parametri, inclusi, ovviamente, il nome del file, ma anche la data di creazione o modifica, il proprietario, il gruppo, i permessi e la dimensione. Ecco la sintassi:
```
find directory opzoni espressione
```

Se vogliamo cercare un file di nome `apache2` partendo dalla directory radice:
```
kali >find / -type f -name apache2
```
Per prima cosa specifichiamo la directory in cui avviare la ricerca, ovvero `/`.
Si indica quindi che tipo di file cercare; in questo caso `f` che indica un file normale.
Infine si specifica il nome del file ricercato, in questo caso `apache2`.


# grep 
Per cercare una parola-chiave utilizza `grep`, spesso utilizzato quando si passano i risultati di un comando a un altro, mediante un processo detto piping, che permette di prendere l'output di un comando e inviarlo come input a un altro.

# ps 
Il comando `ps` serve a visualizzare le informazioni relative ai processi in esecuzione nella macchina. In questo caso utilizzeremo `ps` seguito da `aux`, che specifica quali informazioni dei processi visualizzare:
```
kali >ps aux
```

# cat
Esistono diversi modi per creare un file in linux, uno di questi è `cat`, abbreviazione di concatenate, che significa che si combinano due pezzi insieme. Questo comando viene di solito utilizzato per visualizzare il contenuto di un file, ma si può usare anche per creare file di piccole dimensioni. Per creare file più grossi, è meglio inserire il codice di un editor di testo come vim, emacs, mousepad, gedit o kate, quindi salvare il file.

Il comando `cat` seguito da un nome di file visualizza il contenuto del file, ma se vogliamo creare un file dobbiamo far seguire il comando cat con un redirect(>)  seguito dal nome del file:
```
kali >cat > hackingskills
L'hacking è la competenza più importante del XXI secolo!
```
premendo invio, linux entra in modalità interattiva e attende l'inserimento del contenuto del file.

Per visualizzare il contenuto basta digitare:
```
kali >cat hackingskills
```


# touch
Il secondo comando per la creazione di file è `touch`. In origine, il comando era stato ideato in modo che l'utente potesse solo ritoccare un file per apportarvi piccole modifiche, come data di creazione o di modifica. Se il file non esiste ancora, il comando lo crea.
```
kali >touch newfile
```


# mkdir
Per creare una directory in linux si usa il comando `mkdir`, che sta per make directory:
```
kali >mkdir newdirectory
```


# cp
Per copiare file, si usa il comando `cp`, che crea una nuova copia del file nella nuova posizione, senza toccare la copia precedente.
```
kali >touch oldfile
kali >cp oldfile /root/newdirectory/newfile
```

# mv
Linux non ha un comando specifico per rinominare i file come windows, puoi usare però il comando mv(move) per spostare un file o una directory in una nuova posizione, oppure cambiare il nome di un file. Per farlo basta fare questo:
```
kali >mv newfile newfile2
kali >ls
oldfile newfile2
```

# rm
Per eliminare un file puoi utilizzare rm(remove):
```
kali >rm newfile2
```

# rmdir
Il comando per l'eliminazione di una directory è simile al comando `rm` per eliminare i file, ma con l'aggiunta di `dir`:
```
kali >rmdir newdirectory
```
Questo comando non è in grado di eliminare directory che non siano vuote. Nel caso, restituisce il messaggio di avvertimento "directory non vuota", come in questo esempio. Per eliminare una directory, bisogna eliminare tutto il suo contenuto: in questo modo si evita di eliminare accidentalmente oggetti che non si intendevano eliminare.

Se vuoi eliminare una directory insieme a tutto il suo contenuto in un unico passaggio, puoi utilizzare `rm`con l'opzione `r`:
```
kali >rm -r newdirectory
```


# sudo
Per utilizzare certi programmi ti servirà avere i privilegi di root, il comando da inserire è `sudo -s`(Super User DO) e consente di diventare super-user o superutente. L'opzione `-s` esegue una shell con privilegi di superutente(root).
```
kali >sudo -s
```

Dopo aver inserito questo comando ti verrà chiesto di inserire la password
```
[sudo] password di <nomeutente>
```


# head 
Se ti serve visualizzare solo l'inizio di un file, puoi utilizzare il comando `head`. Per impostazione predefinita questo comando visualizza solo le prime 10 righe di un file:
```
kali >head /etc/snort/snort.conf
```

Se vuoi vedere più di quelle dieci righe ti basta inserire l'opzione `-20` nel caso in cui vuoi vedere le prime 20 righe oppure un altro numero per vederne di più, sempre a partire dall'inizio.
```
kali >head -20 /etc/snort/snort.conf
```

# tail
Il comando `tail` è analogo a `head`, ma invece di visualizzare le prime righe di un file visualizza le ultime. 
```
kali >tail /etc/snort/snort.conf
```
Stessa opzione di `head` se vuoi vedere più righe dal basso.

# nl 
A volte quando i file sono molto lunghi, è di grande aiuto numerare le righe così da farvi riferimento più facilmente; `nl` è il comando che fa al caso giusto:
```
kali >nl /etc/snort/snort.conf
```

# grep
Per filtrare il contenuto di un file puoi utilizzare `grep`:
```
kali >cat /etc/snort/snort.conf | grep output
```
Il comando in questo caso analizza il file `snort.conf` utilizzando una pipe(`|`) per inviare uk risultato a grep il quale riceve in input il file, cerca le righe con un'occorrenza della parola output e quindi le visualizza.

# sed
Questo comando consente di cercare le occorrenze di una parola o di un pattern di testo e quindi di eseguire delle operazioni. Il comando `sed` può essere utilizzato come la funzione trova e sostituisci di windows.

Supponiamo di voler sostituire ogni occorrenza di mysql con MySQL usando `sed`:
```
kali >sed s/mysql/MySQL/g /etc/snort/snort.conf > snort2.conf
```


# more
`more` visualizza un file una pagina alla volta, consentendo di procedere nella lettura, una riga alla volta, premendo il tasto INVIO.
```
kali >more /etc/snort/snort.conf
```

# less
Il comando `less` è molto simile a `more`, con una funzione aggiuntiva, oltre a scorrere il file è possibile filtrarlo con dei termini di ricerca.
```
kali >less /etc/snort/snort.conf
```

