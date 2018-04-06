Allegato E: Guida alla modifica di software open source preso a riuso o di terzi
================================================================================

*Contesto: questo documento è pensato per essere allegato, insieme alla
“Guida alla pubblicazione open source di software realizzato per la PA”
alle specifiche tecniche per la presa in riuso di un software
open-source, con eventuali modifiche. In caso di appalto, può essere
allegato come documento di gara.*

1. Modifica di software open source preso a riuso o di terzi
------------------------------------------------------------

Se il Fornitore ritiene di adottare un software open source esistente,
sia rilasciato da altre Pubbliche Amministrazioni italiane sia
sviluppato e mantenuto da soggetti terzi, o lo richiede
l'Amministrazione committente, si applica integralmente quanto disposto
dalla *Guida alla pubblicazione open source di software realizzato per
la PA*, con l’aggiunta delle prescrizioni contenute nella presente
guida.

2. Modifica del codice sorgente
-------------------------------

È necessario operare con attenzione al fine di minimizzare il grado di
divergenza tra il codice sorgente originale e quello modificato
risultante dal lavoro del Fornitore. Nell'operare le modifiche
necessarie all'adattamento non va infatti tenuto conto solo delle
funzionalità richieste ma bisogna tendere a mantenere compatta e
unitaria la base di codice. Uno dei principi fondamentali dell’open
source è che un software adottato da più parti, e dunque
sufficientemente generalizzato, è più robusto di un software molto
specializzato utilizzato da pochi utenti o addirittura da un singolo
utente. La compresenza di più utilizzatori e di più sviluppatori, con
fini eterogenei, garantisce la qualità del software dal punto di vista
della sicurezza e della robustezza; a tale scopo deve essere messo in
campo ogni sforzo al fine di mettere a fattor comune la maggior parte
delle porzioni di codice.

Nella scelta della base di codice da adottare devono essere privilegiati
dunque i progetti che risultano più maturi, ovvero con più utenti o
sviluppatori, o con la maggiore attività di manutenzione evolutiva e/o
interazioni da parte della community.

La modifica del codice sorgente deve essere ridotta al minimo
indispensabile, preferendo invece i seguenti interventi:

-  laddove il software originale preveda un meccanismo di plugin le
   nuove funzionalità dovranno essere sviluppate sotto forma di plugin
   senza modificare il *core* (ad esempio, nel caso di un Content
   Management System);

-  laddove sia possibile estendere le classi esistenti senza modificarne
   il codice è necessario seguire questa strada.

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

3. Interazione con il maintainer del progetto originale
-------------------------------------------------------

Al Fornitore è richiesto di massimizzare l'interazione con il maintainer
del progetto originale (SHOULD), con approccio collaborativo e con
l'obiettivo di consolidare il lavoro in una unica base di codice a
beneficio del successivo riuso.

Nel caso di correzioni di bug, il Fornitore è tenuto (MUST) ad inviare
al maintainer originale la proposta di correzione usando gli strumenti
di collaborazione previsti dalla piattaforma di code hosting (ad es.
*pull request*).

Nel caso di modifiche necessarie per implementare le nuove funzionalità,
il Fornitore è tenuto (MUST) a prendere contatto con il maintainer
attraverso i canali pubblici del repository (issue tracker) in modo da
presentare il nuovo caso d'uso, proporre la modifica ed ottenere
feedback sulle modalità da seguire soprattutto nell'ottica di scrivere
modifiche che possano essere incorporate dal maintainer originale. È
necessario concedere alcuni giorni al maintainer per rispondere;
tuttavia se il Fornitore ravvisasse tempi di risposta non compatibili
con il proprio cronoprogramma di lavoro può procedere anche in autonomia
(MAY).

Al termine dello sviluppo, il Fornitore è tenuto a proporre al
maintainer originale le proprie modifiche (MUST), con delle proposte di
codice (*pull request*) granulari, ovvero distinte per singole
funzionalità in modo da consentire al maintainer di valutarle
singolarmente.

4. Pubblicazione di codice open source non già a riuso
------------------------------------------------------

In caso di modifica di un software open source di terzi (non preso a
riuso da un’altra Amministrazione) il cui maintainer abbia recepito
integralmente le proposte di modifica inviate dal Fornitore (v.
paragrafo precedente), il Fornitore è comunque tenuto a pubblicare il
codice nel repository dell’Amministrazione per metterlo a riuso,
specificando nel README che tale codice è stato recepito dal progetto
originale, con un link al repository dello stesso.

Si ricorda infatti che, come prescritto dalle Linee Guida, il “software
a riuso” è il software rilasciato da una Amministrazione in adempimento
all’art 69 del CAD; se dunque una Amministrazione adotta un software
open source di terzi, è tenuta a metterlo a riuso, pubblicandola essa
stessa perché sia chiaro ad altre Amministrazioni la provenienza di tale
software.

.. discourse::
   :topic_identifier: 2865
