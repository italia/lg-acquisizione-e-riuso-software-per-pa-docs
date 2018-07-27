.. _licenze:

Licenze aperte e scelta di una licenza
--------------------------------------

Per effettuare il rilascio del codice sorgente di un *software* sotto
licenza aperta, l'amministrazione deve scegliere un testo di licenza
appropriata.

Contesto
~~~~~~~~

È necessario considerare che il legislatore, nel redigere l'articolo 69,
ha chiaramente indicato come obiettivo quello di **favorire il riuso**
del *software* stesso tra più amministrazioni. È dunque importante che la
prima considerazione in ordine di importanza nella scelta della licenza
sia quella di **valutare l'impatto che il testo della licenza ha sulla
possibilità di riuso** da parte di altre amministrazioni.

Fin dagli anni ‘80, il mondo della ricerca informatica e dell'industria
ha prodotto numerosi testi di licenza per il *software* Open Source, con
l'obiettivo di creare un modello di condivisione mondiale del software.
Con il progressivo aumento della complessità degli applicativi, si è
reso sempre più importante, a scopo anche esclusivamente economico e di
efficienza, lavorare integrando componenti già pronti, piuttosto che
cominciare ogni volta a sviluppare codice da capo.

.. _licenze-per-il-software-aperto:

Licenze per il *software* aperto
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Una licenza aperta, così come intesa nell'Art. 69 del CAD, è una licenza
che garantisca all'utente di un *software* le seguenti libertà:

-  Libertà di eseguire il *software* come si desidera, per qualsiasi
   scopo, senza ulteriori costi o restrizioni;
-  Libertà di studiare come funziona il *software* e di modificarlo in
   modo da adattarlo alle proprie necessità;
-  Libertà di ridistribuire copie del software;
-  Libertà di modificare il *software* e distribuirne pubblicamente le
   versioni modificate. [1]_

L'accesso al codice sorgente, o parimenti al formato necessario per
riprodurre e modificare un'opera, è un prerequisito per rispettare tali
libertà.

Open Source Initiative [2]_ (OSI) è un'organizzazione internazionale,
riconosciuta a livello mondiale per il proprio processo di
certificazione delle licenze *software* che rispettano detti requisiti. La
lista aggiornata delle licenze certificate da OSI è disponibile al
seguente indirizzo (indice alfabetico):
https://opensource.org/licenses/alphabetical

L'adempimento dell'Art. 69 del CAD, relativamente alla scelta della
licenza, deve essere effettuato **scegliendo una licenza tra quelle
certificate da Open Source Initiative**. In alternativa,
l'amministrazione che volesse provvedere in autonomia a redigere un
testo di una licenza d'uso, può usare tale testo solo previa
certificazione da Open Source Initiative, onde verificarne l'aderenza ai
principi del *software* aperto. Il processo di invio di una licenza per
approvazione è dettagliato all'indirizzo:
https://opensource.org/approval.

Si noti che per identificare univocamente un testo di licenza, è
possibile utilizzare la categorizzazione SPDX [3]_, che associa ad ogni
licenza (o combinazione) un codice e un'espressione univoci. Un elenco
aggiornato dei codici e dei rispettivi testi di licenza è disponibile
all'indirizzo: https://spdx.org/licenses/.

In allegato alle linee guida (:ref:`guida-licenze`) si trova una guida
per approfondire il tema delle licenze Open Source, che delinea una
categorizzazione dei principali tipi di licenza e delle loro
caratteristiche.

Scelta di una licenza
~~~~~~~~~~~~~~~~~~~~~

Una licenza di *software* libero consente l'utilizzo gratuito del codice
sorgente cui si riferisce, dettando però alcuni vincoli da rispettare.
Pertanto, l'integrazione di più componenti di *software* libero rilasciati
sotto licenze diverse richiede una analisi di compatibilità delle
stesse. Tale analisi può risultare eccessivamente complessa se le
licenze coinvolte sono molteplici, comportando costi aggiuntivi.

In altre parole, **una proliferazione di licenze diverse rende più
difficile e oneroso il riuso del software**, contravvenendo agli
obiettivi delineati dall'art. 69 del CAD.

Si propone quindi il seguente albero decisionale per la scelta di una
licenza aperta:

-  Se il rilascio del *software* si riferisce ad una modifica di software
   Open Source esistente (quindi *software* preso a riuso da un'altra
   amministrazione o di proprietà di terze parti), l'amministrazione
   utilizzerà la **stessa licenza** con la quale è stato originariamente
   distribuito il software, per favorire la massima interoperabilità e
   riuso con altri utilizzatori del medesimo software;
-  Se si tratta di un **software nuovo**, tranne per le eccezioni
   specificate sotto, utilizzare la licenza EUPL v1.2 (codice SPDX:
   ``EUPL-1.2``): https://spdx.org/licenses/EUPL-1.2.html. Questa
   licenza, scritta dalla Commissione europea, è stata scelta in quanto
   di tipo "copyleft", garantisce massima interoperabilità a livello
   europeo, ed è anche tradotta in italiano. Sono previste solo alcune
   eccezioni a questa indicazione generale:

   -  se il **software viene utilizzato principalmente via rete (es:
      tramite un browser)**, utilizzare la licenza "GNU Affero General
      Public License" versione 3 e successive (codice SPDX:
      ``AGPL-3.0-or-later``):
      https://spdx.org/licenses/AGPL-3.0-or-later.html;

      Questa licenza è stata scelta perché, oltre ad essere compatibile
      con la maggior parte delle licenze Open Source, obbliga chi
      modifica il codice a rilasciare i miglioramenti anche in caso esso
      venga utilizzato come parte di un servizio SaaS.

   -  se vengono rilasciati **componenti software** enucleati e con
      ampio campo applicativo (per esempio, le "\ **librerie
      software**\ " e gli "\ **SDK**\ "), utilizzare la licenza "BSD
      3-Clause" (codice SPDX: ``BSD-3-Clause``)
      https://spdx.org/licenses/BSD-3-Clause.html;

      Questa licenza è stata scelta per garantire un utilizzo da parte
      di tutti gli attori quanto più libero possibile, permettendo di
      realizzare applicativi basati su queste librerie, rilasciabili
      sotto qualunque licenza. Questo genere di componenti *software* è
      utilizzato normalmente per favorire l'interoperabilità con le
      Pubbliche Amministrazioni, e trovano beneficio nella nascita di
      ecosistemi che includono applicativi di terze parti, inclusi
      *software* proprietari.

-  Per la **documentazione tecnica** del software, utilizzare la licenza
   Creative Commons CC-BY 4.0 (codice SPDX: ``CC-BY-4.0``)
   https://spdx.org/licenses/CC-BY-4.0.html. Questa licenza è stata
   scelta in quanto permette un riutilizzo semplice della documentazione
   e degli esempi di codice in essa contenuta.

Si rimanda a :ref:`guida-pubblicazione` per i
dettagli tecnici su come apporre correttamente il testo di una licenza
al codice sorgente nel momento della pubblicazione.

Le licenze scelte hanno un vasto utilizzo nell'ecosistema Open Source,
dunque si massimizza la possibilità di poter integrare componenti di
terze parti rilasciate con licenze compatibili.

L'amministrazione che volesse operare una scelta di licenza diversa da
quella qui delineata deve motivarne le ragioni, analizzando la
compatibilità tra le licenze adottate e quelle qui proposte, escludendo
che la scelta limiti le opportunità di riuso ed assicurandosi che non
comporti oneri aggiuntivi per le amministrazioni in fase di riuso.

.. [1]
   Stallman, The Free *software* Definition -
   https://www.gnu.org/philosophy/free-sw.it.html
.. [2]
   https://www.opensource.org/
.. [3]
   https://spdx.org

