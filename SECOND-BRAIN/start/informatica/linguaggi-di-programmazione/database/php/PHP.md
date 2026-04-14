[variabili](https://www.html.it/pag/16679/le-variabili3/)

[STRUTTURA PHP](https://www.php.net/manual/en/langref.php)

[GUIDA PHP](https://guidaphp.it/)

[REFERENCE PHP](https://www.w3schools.com/php/php_ref_overview.asp)

#PHP è un linguaggio per lo scripting server-side, risiede in un server remoto e interpreta le informazioni ricevute da un client grazie al web server, le elabora e restituisce un risultato al client che aveva fatto la richiesta. Il PHP è stato creato principalmente per il Web, esso concede di accedere alle richieste HTTP di tipo GET e POST. HTTP definisce 9 tipi di metodi alcuni non usati o non supportati dal PHP stesso, i più diffusi sono: GET e POST.

#GET: metodo con cui vengono maggiormente richieste le informazioni ad un web server, queste avvengono tramite query <u>string</u>, ovvero la parte di un URL che contiene dei parametri da passare in input ad un'applicazione, ad esempio: `www.miosito.com/pagina-richiesta?id=123&page=3`.

#POST: consente di inviare dati ad un server senza mostrarli in query <u>string</u> ma in form: digitandoli direttamente da tastiera attraverso componenti grafiche, i widget.    

#COOKIE: righe di testo usate per tenere traccia di informazioni relative ad un sito web sul client dell'utente.

#SESSIONI: utilizzate per memorizzare informazioni relative all'utente, salvate sul server, utilizzate per gestire l'accesso a contenuti riservati da parte di utenti registrati. 

#SERVER-WEB: necessario per realizzare script che operano sul Web per la necessità di ricevere richieste HTTP, con risposte al client. I più diffusi sono Apache e NGINX. 
#APACHE: è il più utilizzato a livello mondiale, mentre NGINX prende sempre più piede grazie all'elevato livello di prestazioni garantite.

## **FRAMEWORK**

[[LARAVEL]]

## SCRIPT PHP

per le FUNZIONI non è richiesta né la dichiarazione del tipo di dato restituito, né il tipo dei parametri passati. 
Le #VARIABILI sono delimitate dal carattere `$` seguito da un carattere alfabetico o da (underscore).
Per visualizzare il contenuto delle variabili a video basta utilizzare l'istruzione "echo"


### SCOPE DELLE VARIABILI

Lo scope di una variabile è l'area dove essa è visibile durante l'esecuzione dello script, può essere di 3 tipi: **LOCALE**, **GLOBALE** e **STATICO**.

#SCOPE-LOCALE 
una variabile dichiarata all'interno di una funzione ha uno scope locale e non ha visibilità al di fuori di essa;
ES:
```
function test_scope() {
    $x = "scope locale";
    echo $x;  //stamperà scope locale
}
echo $x; //genererà un errore perché $x non è accessibile al di fuori della funzione
```


#SCOPE-GLOBALE
una variabile dichiarata al di fuori fi una funzione ha uno scope globale e non può essere accessibile all'interno di una funzione. Se vogliamo accedere al valore globale, all'interno della funzione possiamo utilizzare la keyword GLOBAL.
ES:
```
$x = "scope globale";
function test_scope() {
    echo $x;   //genererà un errore perché $x non è accessibile all'interno della funzione
}
echo $x;   //stamperà scope globale
```


#SCOPE-STATICO
Quando una funzione termina la sua esecuzione, il contenuto occupato dalle variabile dichiarate al suo interno viene liberato in memoria. Nel caso in cui non volessimo cancellare il suo contenuto possiamo dichiararla come STATIC. 
ES:
```
function test_static() {
    $x = 0;
    $x = $x+1;
    echo $x;
}
test_static(); //stamperà 1
test_static(); //stamperà 1
test_static(); //stamperà 1
```

ES: definendo una variabile statica
```
function test_static() {
    static $x = 0;
    $x = $x+1;
    echo $x;
}
test_static(); //stamperà 1
test_static(); //stamperà 2
test_static(); //stamperà 3
```


#FOREACH
è una struttura di controllo che consente di iterare attraverso tutti gli elementi di un array o di un oggetto. Durante le iterazioni viene assegnato il valore corrente dell'elemento ad una variabile specificata, operando su ciascun elemento in modo sequenziale. ES:
```
<?php
$numbers = [1, 2, 3, 4, 5];

foreach ($numbers as $number) {
    echo $number . " ";
}
?>
```
[foreach-sintax](https://www.html.it/pag/55677/ciclo-foreach-in-php/)




#STRINGHE 

```strlen()```: restituisce il numero dei caratteri che compongono la stringa.
```strrev()```: inverte una stringa.
```sprintf()```: genera stringhe formattate/concatenate. 
ES:
```
$nome = 'Simone';
$eta = 29;
$citta = 'Forli';
$provincia = 'Forli-Cesena';
$regione = 'Emilia-Romagna';
$formato = '%s ha %d anni ed abita a %s in provincia di %s, nella regione %s';
$stringa = sprintf($formato, $nome, $eta, $citta, $provincia, $regione);
```

 I #COOKIE 
servono ai siti Web per memorizzare informazioni relative agli utenti nei loro stessi computer, possono essere creati meccanismi di autenticazione, riconoscere se un utente è ancora loggato sul sito o meno. I cookie  vengono memorizzati automaticamente dal browser e potranno identificare l'utente fino alla cancellazione. 
Vengono definiti come header HTTP inviati al server client, composti da una coppia chiave/valore e da direttive opzionali.
Per accedere al valore di un cookie basta stamparlo.
[REFERENCE-COOKIE](https://www.html.it/pag/62725/gestire-i-cookie-con-php/)

LE #SESSIONI 
sono un meccanismo alternativo ai cookie per memorizzare informazioni sull'utente. Diversamente dai cookie, la sessione memorizza le informazioni sul server che ospita l'applicazione. Di base la sessione salva i dati in file testuali salvati nel file system del server, è possibile modificare questa configurazione in maniera da salvarle anche su database. 
Quando viene avviata una sessione, PHP crea un identificatore univoco per quella sessione in particolare, detta PHPSESSID e rappresentato da una stringa casuale generata da una funzione di <u>hash</u>(funzione che mappa una stringa di lunghezza arbitraria in una stringa di lunghezza predefinita). Nello stesso modo viene creato e memorizzato nel server un file temporaneo in una directory per il salvataggio delle sessioni. Quando uno script PHP vuole recuperare il valore da una variabile di sessione, PHP preleva il valore dell'identificatore di sessione e lo confronta con quello memorizzato sul server per vedere se sono uguali. La sessione può terminare quando viene chiuso il browser, dopo aver fatto il logout dalla propria area personale o dopo un certo periodo di inattività.
[REFERENCE-SESSIONI](https://www.html.it/pag/62981/gestire-le-sessioni-in-php/)

#PREPARED: diviso in 2 fasi(**prepare** ed **execute**)

```prepare```: invialo statement al server che fa il controllo della sintassi e ottimizza la query salvandola per dopo.

```execute```: mi vengono mandati i valori e poi verrà ripreso lo statement ed eseguito.


COMANDI UTILI

```real_escape-string```: è un metodo che esegue l'escaping delle stringhe utilizzate in una query SQL, prevenendo attacchi di tipo SQL injection. In parole povere aggiunge uno slash inverso (\) davanti ai caratteri speciali che potrebbero essere interpretati in modo diverso dal database, grazie a questo metodo rendiamo i caratteri speciali parte della stringa inserita.
[real_escape-string](https://www.w3schools.com/php/func_mysqli_real_escape_string.asp)


