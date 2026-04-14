[[LIVEWIRE]]
## STRUTTURA

`APP`:	   Rappresenta il cuore pulsante dell’applicazione, tutti i file che implementano la business-logic verranno creati in questa cartella; all’interno della cartella verranno posizionati anche i vari model

`APP/CONSOLE`:		Contiene i comandi personalizzati che verranno eseguiti nella console

`APP/EVENTS`:		Contiene eventuali eventi personalizzati che si possono creare per far comunicare diversi componenti tra di loro

`APP/EXCEPTION`:		Contiene eventuali eccezioni custom utili

`APP/Http`:		Contiene tutta la logica Web dell’applicazione suddivisa in sottocomponenti

`APP/Http/Controllers`:	Contiene tutti controller

`APP/Http/Middleware`:	Contiene tutti i middleware e i filtri

`APP/Http/Request`:	Contiene tutti gli oggetti request definiti secondo lo standard PSR-7

`APP/Jobs`:		Contiene tutti i queueable job dell’applicazione

`APP/Listeners`:		Contiene tutti le classi handler di eventi applicativi

`APP/Providers`:		Contiene tutti i Service Providers custom

`bootstrap`:		Contiene i file principali per l’avvio di Laravel e una cartella cache per motivi di performance

`config`:			Contiene tutte le configurazioni a livello applicativo

`database`:		Contiene tutti i file relativi alla definizione del database

`database/factories`:	Contiene le factory in grado di creare massivamente dei contenuti di test

`database/migrations`:	Contiene le definizioni storicizzate della struttura del database:

`database/seeds`:		Contiene script per il popolamento delle tabelle

`public`:			Rappresenta la document root del progetto e contiene tutte le risorse statiche pubbliche (JS, CSS, immagini,fonts…)

`resources`:		Contiene file di logica ma non applicativi

`resources/assets`:	Contiene eventuali assets pubblici da compilare (Less, Sass, CoffeeScript, TypeScript...)

`resources/lang`:		Contiene i file per l'internazionalizzazione

`resources/views`:	Contiene le viste PHP o blade

`storage`:		Contiene file temporanei o cache

`storage/app`:		Contiene file temporanei legati all’applicazione

`storage/framework`:	Contiene file temporanei legati a Laravel

`storage/logs`:		Contiene i log applicativi

`tests`:			Contiene i file per i test automatici

`vendor`:			Contiene, come da specifiche, tutte le dipendenze

Nella directory Config (configurazioni dell'applicazione e moduli aggiuntivi installabili) i vari contesti sono configurati con file diversi: ad esempio, le configurazioni del database si troveranno in database.php, mentre quelli di invio delle mail in mail.php.
Alcune configurazioni possono differire tra i diversi ambienti; la libreria DotEnv prevede la creazione di un file di configurazione .env nella root del progetto, tutti i settaggi vengono caricati all'interno dell'array globale `$_ENV` e grazie alla funzione env è possibile impostarli all'interno del framework. L'applicationKey è una configurazione che permette un livello di sicurezza maggiore: è la chiave di criptazione di sessioni e altri dati sensibili.


E’ buona norma non condividere il file .env con i vari membri del team o tramite git o svn. La miglior pratica è invece quella di mantenere un file .env.example con una configurazione base ma lasciare al singolo sviluppatore l’onere di definire il proprio file. Per questo motivo il file .env viene inserito di default dentro il file .gitignore autogenerato da Laravel in fase di setup iniziale.


Esempio di una funzione di un controller che ritorna la grandezza di un testo in base all'ID dell'user:
```
public function get(Request $request) {

        $settings = SaveSettings::where('user_id', $request->user_id)->first();
  
        if($settings) {
            return response()->json([
                'success' => true,
                'text_size' => $settings->text_size
            ]);
        } else {
            return response()->json([
                'success' => false,
                'message' => 'Impostazioni non trovate'
            ], 404);
        }
    }
```

