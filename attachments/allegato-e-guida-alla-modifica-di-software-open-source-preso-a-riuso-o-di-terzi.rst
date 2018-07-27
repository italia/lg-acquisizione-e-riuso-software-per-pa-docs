.. _guida-modifica:

Allegato D: Guida alla presa in riuso di software open source
=============================================================

Questa guida è rivolta alle Amministrazioni che vogliano prendere a riuso
un software o adottare un software open source di terzi, effettuando delle
modifiche allo stesso. La guida può essere utilizzata da chiunque sia incaricato di svolgere le
attività in essa descritte: le risorse interne dell'Amministrazione, società
in-house dell'Amministrazione, un fornitore di servizi individuato
dall'Amministrazione. Nel corso della descrizione delle attività si utilizza
il termine “Incaricato” indistintamente per tutte e tre queste categorie.

La guida è stata prodotta anche per poter essere allegata ad un capitolato
tecnico nell'ambito di un appalto; in questo caso l'Incaricato è tenuto a
svolgere le attività descritte nel presente documento come parte integrante
dell'appalto, in aggiunta a quanto specificato nel resto del capitolato.

Nel documento sarà adottata la seguente convenzione:

-  MUST/MUST NOT: prescrizioni obbligatorie che l'Incaricato è tenuto a
   rispettare;

-  SHOULD/SHOULD NOT: raccomandazioni che l'Incaricato è tenuto a
   valutare ed attuare qualora non vi siano documentabili ragioni
   ostative;

-  MAY/MAY NOT: scelte che l'Incaricato può attuare a propria
   discrezione.



1. Modifica di software open source adottato in riuso
-----------------------------------------------------

In caso di adozione di un *software open source* esistente, sia rilasciato da
altre Pubbliche Amministrazioni italiane sia sviluppato e mantenuto da
soggetti terzi, alle modifiche effettuate si applica integralmente quanto
disposto dalla :ref:`guida-pubblicazione`, con l'aggiunta delle prescrizioni
contenute nella presente guida.

Inoltre, le procedure descritte in questa guida si applicano anche alle
modifiche effettuati a componenti software distribuiti con licenza open source
che l'Incaricato dovesse decidere di integrare nel software in questione per
l'esecuzione delle attività.

In caso di adozione di software rilasciato da pubblica amministrazione, è
necessario notificare l'assunzione in riuso tramite l'apertura di un ticket
nel repository della PA che ha rilasciato, al fine di indicare il riuso
all'interno del file publiccode.yml nella apposita sezione.

2. Modifica del codice sorgente
-------------------------------

L'Incaricato deve (MUST) operare con attenzione al fine di minimizzare il
grado di divergenza tra il codice sorgente originale e quello modificato
risultante dal lavoro effettuato. Nell'operare le modifiche necessarie
all'adattamento non va infatti tenuto conto solo delle funzionalità richieste
ma bisogna tendere a mantenere compatta e unitaria la base di codice.

La modifica del codice sorgente deve (MUST) essere ridotta al minimo
indispensabile, preferendo invece i seguenti interventi:

-  laddove il software originale preveda un meccanismo di plugin le
   nuove funzionalità dovranno (MUST) essere sviluppate sotto forma di plugin
   senza modificare il *core* (ad esempio, nel caso di un Content
   Management System);

-  laddove sia possibile estendere le classi o in generale moduli esistenti senza modificarne
   il codice (cioè per *aggiunta*, sfruttando punti di estensione esistenti),
   è necessario (MUST) seguire questa strada.

Qualora non sia possibile realizzare tutte le funzionalità mediante i
sopra descritti meccanismi di estensione, ma sia necessario modificare
il codice sorgente originario, le modifiche devono essere ispirate al
minimalismo, ovvero in ordine di preferenza:

-  si deve implementare solo quanto necessario a poter operare secondo
   una delle modalità di estensione sopra descritte;

-  si devono implementare le nuove funzionalità non nell'ottica di
   specializzare il software originario al proprio contesto, ma al
   contrario concependole come un intervento di potenziamento e
   generalizzazione del software originario.

Non sono ammessi interventi di modifica che limitino le funzionalità o i
casi di uso del software originario (MUST NOT); ogni intervento deve
essere un miglioramento e deve essere concepito in modo che possa essere
recepito come contributo da parte dei maintainer del software originale
(SHOULD).

In ogni caso, nel README dovrà essere chiaramente spiegato cosa è stato
modificato rispetto al progetto originale.

Il repository pubblicato dovrebbe (SHOULD) contenere tutta la storia delle
modifiche dei “code commit” che l'Incaricato ha effettuato durante il processo
di sviluppo, preservando lo storico dell'operato dell'attività di sviluppo,
necessario e utile a tutti gli sviluppatori che vorranno contribuire per
ridurre la curva di apprendimento.


3. Interazione con il maintainer del progetto originale
-------------------------------------------------------

All'Incaricato è richiesto di massimizzare l'interazione con il maintainer
del progetto originale (SHOULD), con approccio collaborativo e con
l'obiettivo di consolidare il lavoro in una unica base di codice a
beneficio del successivo riuso.

Nel caso di correzioni di bug, l'Incaricato è tenuto (MUST) ad inviare
al maintainer originale la proposta di correzione usando gli strumenti
di collaborazione previsti dalla piattaforma di code hosting (ad es.
*pull request*).

Nel caso di modifiche necessarie per implementare le nuove funzionalità,
l'Incaricato è tenuto (MUST) a prendere contatto con il maintainer
attraverso i canali pubblici del repository (issue tracker) in modo da
presentare il nuovo caso d'uso, proporre la modifica ed ottenere
feedback sulle modalità da seguire soprattutto nell'ottica di scrivere
modifiche che possano essere incorporate dal maintainer originale. È
necessario concedere alcuni giorni al maintainer per rispondere;
tuttavia se l'Incaricato ravvisasse tempi di risposta non compatibili
con il proprio cronoprogramma di lavoro può procedere anche in autonomia
(MAY).

Al termine dello sviluppo, l'Incaricato è tenuto a proporre al
maintainer originale le proprie modifiche (MUST), con delle proposte di
codice (*pull request*) granulari, ovvero distinte per singole
funzionalità in modo da consentire al maintainer di valutarle
singolarmente.

l'Incaricato è inoltre tenuto (MUST) a tenere traccia di tutte le
contribuzioni al software inviate al maintainer del software originale,
documentandone lo stato di integrazione all'interno del file README
del repository.

4. Pubblicazione di codice open source non originato nel originato nel contesto della PA
----------------------------------------------------------------------------------------

In caso di modifica di un software open source non originato nel contesto della PA
il cui *maintainer* abbia recepito
integralmente le proposte di modifica inviate dall'Incaricato (v.
paragrafo precedente), l'Incaricato è comunque tenuto a pubblicare il
codice nello strumento di code-hosting dell'Amministrazione per metterlo a riuso,
specificando nel README che tale codice è stato recepito dal progetto
originale, con un *link* al *repository* dello stesso.

Come prescritto dalle Linee Guida, il "software a riuso" è il software
rilasciato da una Amministrazione in adempimento all’art 69 del CAD; se dunque
una Amministrazione adotta un software open source non originato nel contesto
della PA, è tenuta a metterlo a riuso, esplicitandone la provenienza.
