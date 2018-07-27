.. _guida-modifica:

Allegato D: Guida alla presa in riuso di *software* open source
===============================================================

Questa guida è rivolta alle Amministrazioni che vogliano prendere a riuso
un *software* o adottare un *software* open source di terzi, effettuando delle
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



Modifica di *software* open source adottato in riuso
----------------------------------------------------

Nel caso di riuso di il *software* open source, la cui titolarità sia di
una Pubblica Amministrazione, si applica quanto disposto da :ref:`guida-pubblicazione`,
unitamente alle prescrizioni contenute nella presente guida.

Inoltre, le procedure descritte in questa guida possono essere applicate
anche alle modifiche effettuate a componenti *software* distribuiti con licenza
open source la cui titolarità non sia delle Pubbliche Amministrazioni, di cui
sia necessaria l'integrazione in *software* di proprietà della Pubblica
Amministrazione.

In caso di adozione di *software* rilasciato da Pubblica Amministrazione, è
necessario notificare l'adozione in riuso tramite l'apertura di un ticket (o
analogo meccanismo quale una *pull request*) nel repository della Pubblica
Amministrazione titolare, così che questa possa indicare i riferimenti al
riuso all'interno del file *publiccode.yml* nella apposita sezione.

Modifica del codice sorgente
----------------------------

L'Incaricato deve (MUST) operare con attenzione al fine di minimizzare il
grado di divergenza tra il codice sorgente originale e quello modificato
risultante dal lavoro effettuato. Nell'operare le modifiche necessarie
all'adattamento non va infatti tenuto conto solo delle funzionalità richieste
ma bisogna tendere a mantenere compatta e unitaria la base di codice.

La modifica del codice sorgente deve (MUST) essere ridotta al minimo
indispensabile, preferendo invece i seguenti interventi:

-  laddove il *software* originale preveda un meccanismo di plugin le
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
   specializzare il *software* originario al proprio contesto, ma al
   contrario concependole come un intervento di potenziamento e
   generalizzazione del *software* originario.

Non sono ammessi interventi di modifica che limitino le funzionalità o i
casi di uso del *software* originario (MUST NOT); ogni intervento deve
essere un miglioramento e deve essere concepito in modo che possa essere
recepito come contributo da parte dei maintainer del *software* originale
(SHOULD).

In ogni caso, nel README dovrà essere chiaramente spiegato cosa è stato
modificato rispetto al progetto originale.

Il repository pubblicato dovrebbe (SHOULD) contenere tutta la storia delle
modifiche dei “code commit” che l'Incaricato ha effettuato durante il processo
di sviluppo, preservando lo storico dell'operato dell'attività di sviluppo,
necessario e utile a tutti gli sviluppatori che vorranno contribuire per
ridurre la curva di apprendimento.


Interazione con il maintainer del progetto originale
----------------------------------------------------

All'Incaricato è richiesto di massimizzare l'interazione con il *maintainer*
del progetto originale (SHOULD), con approccio collaborativo e con
l'obiettivo di consolidare il lavoro in una unica base di codice a
beneficio del successivo riuso.

Nel caso di correzioni di bug, l'Incaricato è tenuto (MUST) ad inviare
al *maintainer* originale la proposta di correzione usando gli strumenti
di collaborazione previsti dalla piattaforma di code hosting (ad es.
*pull request*).

Nel caso di modifiche necessarie per implementare le nuove funzionalità,
l'Incaricato è tenuto (MUST) a prendere contatto con il *maintainer*
attraverso i canali pubblici del repository (*issue tracker*) in modo da
presentare il nuovo caso d'uso, proporre la modifica ed ottenere feedback
sulle modalità da seguire soprattutto nell'ottica di scrivere modifiche che
possano essere incorporate dal *maintainer* originale. È necessario concedere
alcuni giorni al *maintainer* per rispondere; tuttavia, qualora i tempi di
risposta si dovessero protrarre eccessivamente, si potrà procedere anche in
autonomia (MAY).

Al termine dello sviluppo, l'Incaricato è tenuto a proporre al
*maintainer* originale le proprie modifiche (MUST), con delle proposte di
codice (*pull request*) granulari, ovvero distinte per singole
funzionalità in modo da consentire al *maintainer* di valutarle
singolarmente.

l'Incaricato è inoltre tenuto (MUST) a tenere traccia di tutte le
contribuzioni al *software* inviate al *maintainer* del *software* originale,
documentandone lo stato di integrazione all'interno del file README
del repository.

Pubblicazione di codice open source non originato nel originato nel contesto della PA
-------------------------------------------------------------------------------------

Nel caso in cui il *maintainer* di un *software* open source la cui titolarità non
sia attribuita ad una Pubblica Amministrazione, il cui abbia recepito
integralmente le proposte di modifica (v. paragrafo precedente) presentate del
l'Incaricato, quest'ultimo è comunque tenuto a pubblicare il codice nello
strumento di code hosting dell'Amministrazione per metterlo a riuso,
specificando nel *README* che tale codice è stato recepito dal progetto
originario, con un *link* al *repository* dello stesso.

Come prescritto dalle Linee Guida, il "software a riuso" è il software
rilasciato da una Pubblica Amministrazione in adempimento all'art 69 del CAD.
Quindi l'Amministrazione Pubblica che adotta un *software* open source non
originato nel contesto della PA, è tenuta a metterlo a riuso, indicando la sua
provenienza.
