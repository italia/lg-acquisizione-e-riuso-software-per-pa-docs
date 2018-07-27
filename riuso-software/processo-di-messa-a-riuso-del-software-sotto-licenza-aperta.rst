Processo di messa a riuso del *software* sotto licenza aperta
-------------------------------------------------------------

Il processo di messa a riuso è il seguente:

1. L'amministrazione individua uno strumento di **strumento di code
   hosting**. Una volta identificato lo strumento, può essere utilizzato
   per tutto il *software* che deve essere messo a riuso (:ref:`scelta-code-hosting`).
2. L'amministrazione sceglie una licenza aperta da utilizzare
   (:ref:`licenze`).
3. L'amministrazione, utilizzando proprie risorse oppure tramite un
   appalto, pubblica il codice sorgente completo del *software* e la
   relativa documentazione tecnica sullo strumento di code hosting.
   Questo processo tecnologico è descritto in :ref:`guida-pubblicazione`,
   allegata a queste linee guida. La guida è scritta in modo da poter
   essere allegata ad un capitolato tecnico di gara, per facilitare
   l'acquisizione di un servizio demandando al fornitore gli adempimenti
   richiesti dalle presenti linee guida.
4. L'amministrazione "registra" il *software* sulla piattaforma Developers
   Italia, così che sia indicizzato dal motore di ricerca e reso
   visibile alle altre amministrazioni che cercano *software* in riuso.

Il processo qui delineato è valido sia per il *software* esistente di
proprietà delle amministrazioni (:ref:`rilascio-software-esistente`), sia
per il *software* che verrà realizzato in futuro (:ref:`sviluppo-nuovo-software`).

.. _scelta-code-hosting:

Scelta di uno strumento di code hosting
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il rilascio di un *software* deve avvenire mediante uno strumento di code
hosting, specializzato nell'ospitare e mettere a disposizione il
software distribuito sotto licenza aperta. Esistono numerose soluzioni
sul mercato, sia gratuite sia commerciali.

Poiché il fine del comma 1 dell'articolo 69 è quello di favorire il
riuso tra amministrazioni, è necessario che lo strumento segua le
best-practice in termini di funzionalità per la pubblicazione del codice
sorgente, onde non causare costi aggiuntivi alle amministrazioni che
vogliano trovare ed utilizzare il software.

In particolare, lo strumento dovrà necessariamente avere almeno le
seguenti funzionalità:

-  Accesso libero in lettura al codice sorgente, senza autenticazione;
-  Registrazione gratuita e libera, aperta al pubblico;
-  Interfaccia web per la lettura e navigazione del codice e della
   relativa documentazione;
-  Utilizzo di un sistema di controllo di versione con la funzionalità
   di gestione di rami paralleli di sviluppo (*branch)*;
-  Sistema di segnalazioni (*issue tracker*) aperto al pubblico in
   lettura senza autenticazione e in scrittura dietro autenticazione;
-  Implementazione di almeno un flusso di invio modifiche, revisione del
   codice (*code review*), e integrazione della modifica, completamente
   gestito dallo strumento, aperto al pubblico;
-  Sistema di gestione dei rilasci;
-  Disponibilità di API per interfacciarsi con lo strumento ed estrarre
   dati e metadati relativi ai repository.

Per semplificare la scelta, in :ref:`guida-pubblicazione`
è possibile trovare un elenco non esaustivo delle principali piattaforme
sul mercato che corrispondono ai requisiti richiesti.

Alcune piattaforme completamente aderenti ai parametri minimi sono
disponibili in modalità SaaS (cioè possono essere usate direttamente via
Internet senza doverne installare una copia su un server), senza alcun
costo di licenza, e senza la necessità di sottoscrivere contratti o
convenzioni; la scelta di una di queste piattaforme SaaS è quindi da
considerarsi preferenziale, nel caso non ci siano altri vincoli tecnici
(es: requisiti di integrazione), in modo da non causare costi diretti o
indiretti all'amministrazione.

L'amministrazione deve scegliere uno strumento (o più strumenti, in
caso di motivate ragioni organizzative) sul quale effettuare i rilasci
di tutto il *software* di cui è titolare. In alternativa,
in :ref:`guida-pubblicazione` è delineato un processo
alternativo per demandare la scelta al soggetto incaricato di effettuare
lo sviluppo del *software* e/o il rilascio dello stesso per conto
dell'amministrazione (sia nel caso che questo soggetto corrisponda ad
una risorsa interna o esterna all'amministrazione).

Una volta eletto uno o più strumenti di code hosting, l'amministrazione
deve dare adeguata visibilità agli strumenti nella propria pagina
istituzionale, come dettagliato sempre all'interno della medesima
guida (:ref:`registrazione-repository`).

Registrazione del *software* aperto su Developers Italia
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il *software* rilasciato dalla amministrazione deve essere "registrato"
all'interno del motore di ricerca di Developers Italia, per agevolare la
consultazione alle altre amministrazioni che cercano un *software* in
riuso.

Il processo tecnico preciso per effettuare la registrazione è indicato
nella sezione :ref:`registrazione-repository`.

Responsabilità connesse al rilascio
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

L'amministrazione titolare del *software* non contrae alcun obbligo
specifico legato al rilascio: non è infatti necessario fornire alcuna
garanzia sul software, supporto tecnico o a livello utente, né tantomeno
supportare economicamente le amministrazioni che riusano il *software* nei
costi o nelle procedure di adozione.

