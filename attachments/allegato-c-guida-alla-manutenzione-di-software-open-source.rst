
Allegato C: Guida alla manutenzione di software open source
===========================================================

*Contesto: questo documento è pensato per essere allegato, insieme alla
“Guida alla pubblicazione di software open source” alle specifiche
tecniche per la manutenzione correttiva e/o evolutiva di software
rilasciato sotto licenza aperta (incluso software non di proprietà
dell’Amministrazione). In caso di appalto, può essere allegato come
documento di gara.*

1. Obbligo di rilascio
----------------------

Quando, nell’ambito delle attività di manutenzione, il Fornitore apporta
modifiche al codice originale, anche di carattere minore, si configura
l’obbligo di rilascio ex art. 69 del Codice dell’Amministrazione
Digitale.

Qualora l’Amministrazione sia già titolare di un repository destinato al
software oggetto della manutenzione, creato secondo le indicazioni della
*Guida alla pubblicazione di software open source*, il rilascio delle
modifiche andrà effettuato mediante aggiornamento di tale repository
prima che le stesse vengano immesse in collaudo o in produzione (MUST).
Al fine di gestire tali flussi di rilascio e collaudo, distinguendo la
versione già in produzione da quella in sviluppo o in collaudo, il
Fornitore può usare le funzionalità di branching offerte dal sistema di
controllo di versione prescelto (MAY).

Qualora invece l’Amministrazione non sia già titolare di un repository
per il software oggetto della manutenzione, dovrà procedere a crearne
uno seguendo le indicazioni della *Guida alla modifica di software open
source di terzi*.

2. Obblighi relativi alla manutenzione di software per il quale l’Amministrazione disponga già di un repository
---------------------------------------------------------------------------------------------------------------

Le disposizioni successive si applicano solo a partire dal momento in
cui l’Amministrazione sia titolare di un repository.

2.1. Aggiornamento delle dipendenze
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Per tutta la durata dell’incarico di manutenzione, il Fornitore è tenuto
a monitorare i rilasci delle eventuali dipendenze incorporate nel
software e a recepire eventuali aggiornamenti (MUST). Se il software è
derivato da altro software, tale obbligo di monitoraggio e recepimento
si applica anche al software originale (c.d. *upstream*).

Eventuali incompatibilità o problemi di sicurezza insorti nel tempo
dovranno essere documentati tempestivamente attraverso l’apertura di
issue dedicate, da tenere aperte fino alla risoluzione, ed eventualmente
anche nel file README. Nel caso di nuove versioni che risolvono problemi
di sicurezza, l’aggiornamento delle dipendenze deve avere priorità
assoluta.

2.2. Descrizione del ruolo di maintainer
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Per tutta la durata dell’attività di manutenzione connessa al software
sviluppato, il Fornitore dovrà svolgere il ruolo di *maintainer* del
progetto open source, inserendo il nome della propria azienda nei file
*README* e *publiccode.yml* del repository, con l’eventuale data di
termine dell’incarico. Il maintainer è incaricato di gestire l’attività
sul progetto derivante dalle interazioni con gli utenti esterni.

2.3. Interazione sul repository/issue tracker
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Tutte le interazioni avviate da utenti esterni all’interno della
piattaforma di code hosting, e in particolare attraverso il suo issue
tracker, dovranno essere esaminate dal *maintainer* entro due giorni
lavorativi (SHOULD), ed entro tale termine è necessario (MUST) fornire
una risposta. La risposta può non essere esaustiva, e laddove non sia
possibile rispondere approfonditamente subito è comunque opportuno dare
un cortese riscontro con delle prime considerazioni.

2.3.1. Risoluzione di bug
^^^^^^^^^^^^^^^^^^^^^^^^^

Le segnalazioni di bug ricevute da utenti esterni attraverso l’issue
tracker dovranno essere analizzate al pari di quelle ricevute
dall’Amministrazione committente. Se la risoluzione fosse compatibile
(in quanto a tempi e costi) con le attività prevista dal contratto,
potrà essere eseguita senza necessità di ulteriore approvazione. Se
invece la risoluzione non fosse compatibile (in quanto a tempi e costi)
con le attività di manutenzione prevista dal contratto, la issue dovrà
essere mantenuta aperta, informando l’Amministrazione competente della
propria scelta.

Il processo di diagnosi e risoluzione dovrà essere documentato
pubblicamente all’interno dell’issue tracker, ad eccezione delle
informazioni che hanno implicazioni sulla sicurezza dei sistemi in
produzione, le quali dovranno essere mantenute riservate fino alla messa
in funzione delle correzioni (MUST) e solo successivamente pubblicate
(MUST), a beneficio di altri utenti del software. La issue di
segnalazione dovrà essere mantenuta aperta fino alla risoluzione (MUST)
ed è opportuno (SHOULD) chiedere all’utente originale di verificare in
prima persona la bontà della risoluzione prima di chiudere la issue. In
caso di mancata risposta dell’utente per trenta giorni, il Fornitore può
chiudere la issue, dopo aver documentato all’interno l’avvenuto collaudo
della modifica.

2.3.2. Richieste di nuove funzionalità
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Le richieste di nuove funzionalità dovranno essere valutate dal
maintainer, di concerto con l’Amministrazione, in relazione alla loro
pertinenza al progetto. Se non ritenute pertinenti dovranno essere
chiuse (SHOULD) fornendo una motivazione al proponente.

Se ritenute pertinenti dovranno essere lasciate aperte fino
all’eventuale implementazione (MUST), dando tuttavia rapido riscontro al
proponente (MUST) con una valutazione sulla fattibilità tecnica della
richiesta e suggerimento su eventuali altri modi per raggiungere
l’obiettivo dichiarato. Il maintainer può chiedere al proponente, se
necessario, maggiori dettagli sul caso d’uso che motiva la richiesta
(MAY).

L’implementazione delle funzionalità richieste dovrà essere approvata
dall’Amministrazione (MUST) nel caso che questo comporti degli oneri per
la stessa (es: in caso il contratto sia strutturato con un modello a
consumo).

In alternativa, il maintainer può decidere in autonomia di dare seguito
alla richiesta implementandola nel codice (MAY), senza causare oneri
aggiuntivi all’Amministrazione e nel rispetto dei tempi del contratto
(per esempio, in virtù di altri accordi commerciali sullo stesso
software).

2.3.3. Richieste di informazioni o supporto
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Le richieste di informazioni sul progetto dovranno essere evase a cura
del maintainer entro 2 giorni lavorativi (SHOULD). Le risposte dovranno
limitarsi alle caratteristiche tecniche del software e alle domande
poste dagli sviluppatori o da altre Amministrazioni per finalità di
comprensione del funzionamento tecnico, riuso, collaborazione o
sviluppo. Il Fornitore non è tenuto a rispondere ad altri soggetti o
fornire assistenza sull’utilizzo del software o dare risposte sull’uso
che l’Amministrazione fa del software o in generale su altri argomenti
di competenza dell’Amministrazione.

2.3.4. Contributi di codice
^^^^^^^^^^^^^^^^^^^^^^^^^^^

I contributi di codice inviati attraverso i meccanismi di collaborazione
previsti dalla piattaforma di code hosting scelta (ad es. attraverso una
*pull request*) dovranno essere valutati dal maintainer (MUST) che
provvederà a dare un riscontro all’utente con considerazioni sulla
fattibilità dell’integrazione (MUST). Il maintainer è tenuto ad
incorporare tutti i contributi di codice (SHOULD) che non presentano
incompatibilità con gli obiettivi della fornitura, fornendo al
contributore adeguata spiegazione in caso di diniego.

.. discourse::
   :topic_identifier: 2863
