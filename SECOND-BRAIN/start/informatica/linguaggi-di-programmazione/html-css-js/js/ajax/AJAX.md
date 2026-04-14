**AJAX (Asynchronous Javascript and XML)** non è un <u>LINGUAGGIO DI PROGRAMMAZIONE</u> è l'insieme di: un oggetto **XMLhttpRequest** integrato nel browser e JavaScript and HTML DOM che riguardano l'aggiornamento di parti di una pagina web, 
senza ricaricare la stessa pagina. Lo scopo principale è quello di scambiare piccole quantità di dati con il server senza aggiornare l'intera pagina.

[COME FUNZIONA AJAX](https://www.w3schools.com/js/pic_ajax.gif)

[INVIO DATI POST SERIALIZZATI](https://www.agenziawebeureka.it/come-inviare-dati-dei-form-con-ajax-serialize/)

La maggior parte delle implementazioni AJAX usa l'API XMLhttpRequest che include un elenco di richieste del server che possono essere richiamate tramite Javascript. I dati vengono inviati al browser in formato XML. Quello che caratterizza AJAX è la leggera sfasatura tra la richiesta inviata dallo script al server web e la ricezione dei dati, perciò detti asincroni.

SINTASSI DEL METODO AJAX

```
$.ajax({url,[ settings]})
```

l'URL rappresenta il percorso file richiesto, la risorsa; 
settings è un valore opzionale che rappresenta un insieme di coppie/valore, esse consentono di specificare numerosi parametri tra cui: 
- ```method```, metodo HTTP che serve per la richiesta. Può avere questi valori: POST, GET o PUT(GET di default);
- ```dataType```: per specificare il tipo di dati che si riceve dal server web(json, xml, txt, ecc.);
- ```success```: funzione che viene eseguita in caso di successo della chiamata, i parametri opzionali che accetta sono: data ovvero i dati restituiti dal server, textStatus lo stato e l'oggetto jqXHR;
- ```error```: funzione che viene eseguita in caso di errore della chiamata effettuata, magari non accessibile. 

![[funzionamento.gif]]

## [INVIO DI DATI ASINCRONI AL DB](https://portapipe.wordpress.com/2011/10/12/salvare-dati-dentro-input-in-mysql-asincronamente-con-ajax/)


1°
```
$(document).ready(function() {
            $('#submit').on('click', function() {
                var nome_compito = $("#nome_compito").val();
                var compito = $("#compito").val();
                var data_scadenza = $("#data_scadenza").val();

                $.ajax({
                    type: "POST";
                    url: "inserimento-aggiornamento/inserimento.php";
                    data: {nome_compito: nome_compito, compito: compito, data_scadenza: data_scadenza},
                    success: function(mess){
                        <?php
                            echo "<p>Compito inserito correttamente</p>";
                            ?>
                    },
                    error: function(){
                        alert("chiamata fallita, si prega di riprovare...");
                    }
                });
            });
        });
```

Per verificare se Jquery è caricato correttamente dopo averlo installato, esegui il log dal developer tool del tuo browser(F12):
```
console.log(typeof $);
```


## Gestione asincrona

Il tipo `"module"` indica che il codice JavaScript dentro lo script è un modulo (ES6 Module). Ciò comporta alcune differenze importanti:

- **Moduli JavaScript (ESM)**: Il codice all'interno del tag `<script type="module">` è trattato come un modulo. Ciò significa che puoi utilizzare le parole chiave `import` ed `export` per caricare e condividere codice tra file JavaScript diversi.
- **Caricamento asincrono**: Gli script di tipo modulo vengono sempre caricati in modo asincrono, il che significa che non bloccano il caricamento di altre risorse (come immagini o fogli di stile). Il modulo verrà eseguito solo quando tutte le risorse saranno caricate.
- **Scope del modulo**: All'interno di un modulo, le variabili e le funzioni sono **locali** al modulo e non vengono messe nel contesto globale (window). Ciò significa che non interferiscono con altre parti del codice.
- **CORS (Cross-Origin Resource Sharing)**: Per i moduli, le risorse devono essere caricate dallo stesso dominio o avere il supporto CORS se vengono caricate da domini differenti.
- **`defer` implicito**: Gli script di tipo modulo sono automaticamente "deferiti", il che significa che verranno eseguiti dopo che il DOM è stato completamente caricato (senza dover usare l'attributo `defer`).

Esempio di codice:
```
<script type="module">
  import { myFunction } from './module.js';
  myFunction();
</script>
```


## Gestione sincrona

Il tipo `"text/javascript"` è il tipo predefinito per gli script JavaScript tradizionali e viene utilizzato per il codice JavaScript che non fa uso di moduli. Questo tipo ha alcune caratteristiche diverse:

- **No supporto per `import` ed `export`**: Non puoi usare `import` ed `export` in un `<script>` di tipo `text/javascript`. Tutto il codice viene eseguito nel contesto globale (o nel contesto in cui è stato incluso).
- **Caricamento sincrono**: Gli script di tipo `text/javascript` vengono eseguiti in modo sincrono, il che significa che il browser ferma il rendering della pagina per eseguire il JavaScript e poi continua con il caricamento della pagina. Questo può rallentare il rendering della pagina se il codice è grande o se vengono caricati molti script.
- **Scope globale**: Le variabili dichiarate all'interno di uno script di tipo `text/javascript` vengono generalmente messe nel contesto globale (oggetto `window`), a meno che tu non usi altre tecniche (come funzioni immediatamente invocate o IIFE) per isolare il codice.

Esempio di codice:
```
<script type="text/javascript">
  function myFunction() {
    console.log("Hello World!");
  }
  myFunction();
</script>
```
