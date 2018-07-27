.. _guida-licenze:

Allegato C: Guida alle licenze Open Source
==========================================

Le licenze Open Source possono essere molteplici, con lievi differenze
che possono presentare, al momento del riuso del software,
incompatibilità importanti. Questa guida ha lo scopo di fornire al
lettore una breve introduzione alle diverse licenze adottabili, e
suggerire l'adozione di alcune licenze specifiche. Limitare il numero di
licenze in uso nel parco *software* ha infatti il vantaggio di
semplificare di molto l'integrazione, dunque permettendo un risparmio da
parte della Pubblica Amministrazione.

Versionamento delle licenze
---------------------------

Ogni licenza riportata di seguito citata dispone di un numero di
versione, che garantisce agli enti redattori la possibilità di
aggiornarla. Ai fini di garantire una compatibilità e riutilizzabilità
del codice in futuro, in particolare per le licenze copyleft, si
consiglia rilasciare ogni *software* secondo l'ultima versione disponibile
della licenza, esplicitando la compatibilità con qualunque modificazione
successiva.

Public Domain
-------------

Una licenza di pubblico dominio è una licenza nella quale il detentore
dei diritti rinuncia ai diritti di proprietà intellettuale.

È la licenza consigliata per il rilascio di banche dati in Open Data,
ove non ci si occupi di banche dati originali per scelta o disposizione
di opere. Si ricorda che i diritti sui singoli elementi contenuti in una
banca dati sono comunque coperti da una loro licenza individuale, che
non è pregiudicata dal loro inserimento in una banca dati.

Questa licenza infatti offre ai riutilizzatori una flessibilità totale e
riduce le complicazioni collegate all'operatività su varie e diverse
licenze con il potenziale conflitto di disposizioni che comporta.

La più diffusa licenza in questo senso è la Creative Commons Zero
(Codice SPDX: ``CC0-1.0``).

Licenze non-copyleft
--------------------

Le licenze non-copyleft sono licenze aperte che garantiscono molta
libertà e flessibilità di riutilizzo da parte degli utenti.

Con queste licenze il detentore dei diritti richiede infatti solamente
una frase che identifica la fonte del documento e, ove fattibile, un
collegamento alle pertinenti informazioni sulla licenza, non ponendo
limitazioni all'utilizzo o alla modifica dell'opera di ingegno.

Queste licenze vengono utilizzate per componenti *software* che
implementano adattatori o componenti che nascono per essere integrati in
applicativi di terze parti. Il focus principale di queste licenze è
posto sul riutilizzo nel maggior numero di programmi possibili.

A differenza delle licenze copyleft, non esiste un obbligo di chi adatta
questi componenti a rilasciare eventuali modifiche e miglioramenti, ma
solo un riferimento per ottenere copia del codice sorgente originale.

Esempi di queste licenze sono la licenza BSD, la licenza MIT e la
licenza Apache - codici SPDX: ``BSD-3-Clause``, ``MIT`` e ``Apache-2.0``.

**Nota:** l'utilizzo della licenza Apache è sconsigliato in quanto
incompatibile con la licenza GNU GPL versione 2 (codice SPDX:
``GPL-2.0-or-later``).

Licenze copyleft
----------------

Le licenze copyleft sono licenze che richiedono un'attribuzione
all'autore originale ma che aggiungono le cosiddette clausole "virali".
Il concetto di viralità impone a ogni successiva modifica di essere
rilasciata sotto una licenza che non imponga ulteriori restrizioni
all'utente.

Si utilizzano per preservare la libertà del *software* a ogni successiva
modifica, imponendo il rilascio in riuso di ogni eventuale modifica
migliorativa da parte di terze parti.

Si noti che è indispensabile fornire copia del codice sorgente solo
all'atto della distribuzione o concessione in licenza del software, non
al momento dello sviluppo.

Questo tipo di licenza è consigliato per tutti gli applicativi software
completi.

La licenza più diffusa in questo senso è la GNU GPL (codice SPDX:
``GPL-3.0-or-later``) o la GNU AGPL, sua modificazione che copre anche
l'ambito di *software* distribuiti via rete (codice SPDX:
``AGPL-3.0-or-later``).

Licenze copyleft - per le librerie
----------------------------------

Ai fini di garantire flessibilità nel riutilizzo, ovvero permettere
l'utilizzo di un componente *software* in un applicativo sotto qualunque
licenza, la clausola di viralità può essere indebolita. Queste licenze
vengono anche dette "a copyleft debole".

Questa clausola aggiuntiva mantiene intatta la viralità per quanto
riguarda modifiche sul codice del componente, ma permette l'integrazione
esterna da parte di un *software* distribuito sotto qualunque licenza.

Si noti che queste licenze contengono la cosiddetta "clausola di
riproducibilità": deve essere sempre possibile per l'utente di un
software di terze parti sostituire il componente rilasciato sotto
licenza LGPL con una sua versione modificata, senza modificare le
funzionalità del *software* di terze parti. Questa clausola può essere
problematica e non soddisfabile in alcuni ambienti embedded, ad esempio
iOS.

La versione più utilizzata è la licenza GNU LGPL (codice SPDX:
``LGPL-3.0-or-later``), versione modificata della licenza GNU GPL.

Licenze non comprese nella classificazione appena introdotta
------------------------------------------------------------

-  La Mozilla Public License (codice SPDX: ``MPL-2.0``) è una licenza
   copyleft, equiparabile alla licenza GNU GPL, che garantisce la libera
   distribuzione del codice ma impone di non poter riutilizzare,
   all'occorrenza di modifiche, loghi, nomi, o altri marchi registrati
   del detentore dei diritti, salvo ulteriore autorizzazione.

-  La European Union Public License (EUPL) è una licenza copyleft di
   tipo debole, sviluppata dalla Commissione europea, e tradotta
   ufficialmente in tutte le lingue dell'Unione. Questa licenza allega
   una tabella di compatibilità con alcune delle licenze aperte più
   comuni. Codice SPDX: ``EUPL-1.2`` .

Le licenze Creative Commons
---------------------------

Esistono molte versioni delle licenze Creative Commons. Queste licenze,
così come suggerito da Creative Commons stesso, non sono utilizzabili
per proteggere software, ma solo altre opere di ingegno (ad esempio
documentazione o testo).

Le uniche licenze Creative Commons che possono intendersi licenze
aperte, secondo quanto descritto in 3.3, sono:

-  Creative Commons Zero - dominio pubblico (codice SPDX: ``CC0-1.0``).

-  Creative Commons Attribution (versione 4 e successive) - una licenza
   non copyleft (codice SPDX: ``CC-BY-4.0``)

-  Creative Commons Attribution-Share Alike (versione 4 e successive) -
   una licenza copyleft (codice SPDX: ``CC-BY-SA-4.0``)

Licenza applicabile alla documentazione e allegati del software
---------------------------------------------------------------

Tutti gli allegati al puro codice sorgente del *software* quali commenti
nel codice sorgente, documentazione, esempi, schermate dimostrative,
video, ecc. si considerano inclusi sotto la stessa licenza del software
stesso. In generale, non è quindi necessario determinare licenze diverse
per questi contenuti, se rilasciate contestualmente al *software* e parte
integrante di esso.

Nel caso di rilascio di documentazione a sé stante rispetto al software,
o nel caso questa sia particolarmente corposa (oltre una decina di
pagine stampate), si consiglia di attribuire comunque una licenza
all'opera. Si rimanda a 4.4 per una guida nella scelta della licenza
migliore.

Compatibilità tra le licenze
----------------------------

La compatibilità delle licenze dipende dalla cessione dei diritti
intellettuali da parte dell'autore. Le licenze che in questo senso
cedono meno diritti, al fine di preservare maggiormente nel tempo la
libertà e riutilizzabilità del *software* creato, sono le licenze
copyleft.

Quando si parla di compatibilità occorre distinguere due casi:

-  La creazione di una nuova opera a partire da componenti già
   esistenti, con licenza unica

-  L'assemblaggio e la distribuzione di più componenti interagenti,
   ognuna con licenza differente.

Per quanto riguarda il caso di creazione di una nuova opera sotto una
licenza unica, la matrice di compatibilità è la seguente:

-  Opere rilasciate sotto dominio pubblico sono rilasciabili con
   qualunque altra licenza

-  Opere rilasciate sotto licenze non-copyleft sono rilasciabili con
   licenze copyleft

-  Opere rilasciate sotto licenze copyleft possono essere solo
   rilasciate con licenze copyleft, a condizione che le due licenze
   siano compatibili

Nel secondo caso invece:

-  Opere rilasciate sotto licenza di pubblico dominio, non-copyleft o
   copyleft debole possono interagire come componenti a sé stanti con
   qualunque altro applicativo, pur rispettando le eventuali clausole
   riguardo riferimenti al codice originali e la distribuzione di
   eventuali modifiche.

-  Opere rilasciate sotto licenza copyleft possono interagire come
   componenti a sé stanti solo con altri componenti rilasciati con
   licenza copyleft compatibile.

