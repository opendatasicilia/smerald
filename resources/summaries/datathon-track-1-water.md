# Dati sulle acque: le sfide per la salute e l'ambiente

Il gruppo di lavoro discute il [progetto WHOW (Water Health Open knoWledge)](https://whowproject.eu/) che si propone di promuovere la creazione del primo grafo della conoscenza europeo sulla qualità e il consumo dell'acqua, sui parametri di salute e sulla diffusione delle malattie. Vengono identificati diversi tipi di acque, tra cui quelle balneari, potabili e superficiali, e viene analizzato l'approccio alla gestione dei dati, evidenziando le sfide nell'ottenere dati aperti e aggiornati. 

La conversazione verte anche sull'importanza di arricchire semanticamente i dati esistenti (compresi [quelli estratti dalla community di Open Data Sicilia in relazione alla siccità](https://github.com/opendatasicilia/emergenza-idrica-sicilia/tree/main/risorse#readme)) e di collegare domini diversi, come quelli ambientali e sanitari, attraverso ontologie e pipeline di trasformazione.

Viene sottolineata l’importanza del catalogo [schema.gov.it](http://schema.gov.it) e la necessità di migliorare la qualità e la tempestività della pubblicazione dei dati, anche se non completamente validati.  Si riflette sull'utilizzo potenziale di LLM (Large Language Models) per automatizzare e semplificare i processi di conversione.

## 1\. Il Progetto WHOW

Il progetto WHOW è stato sviluppato con l'obiettivo di "identificare degli use case" e "una serie di dati relativi alla qualità delle acque e ai cosiddetti parametri della salute." Erano previsti questi use case specifici:

- **Acque balneari**: Riguardanti il mare, con il coinvolgimento di ISPRA (per le aree costiere) e Regione Lombardia (per le acque interne).

- **Acque per il consumo umano (potabili)**: Questa si è rivelata la parte più complessa ("un bagno di sangue per tutta una serie di motivi: ci sono tanti gestori").

- **Acque superficiali (laghi e fiumi)**: Di particolare interesse per la Regione Lombardia che ne possiede molte.

- **Eventi estremi**: Considerato "lo use case molto più difficile in assoluto" perché include inondazioni e siccità, richiedendo anche "dati climatici, quindi dati relativi alle temperature, a appunto anche a livello di neve."

L'obiettivo primario era duplice: migliorare la qualità dei dati esistenti attraverso un arricchimento semantico e stabilire connessioni tra set di dati diversi, inclusi domini apparentemente distinti come l'ambiente e la salute. Si è tentato di correlare i dati relativi alla qualità dell'acqua con quelli sanitari (ad esempio, accessi al pronto soccorso per disturbi gastrointestinali); tuttavia, i dati del pronto soccorso erano "impossibili da trovare in formato aperto".

## 2\. Modello di rappresentazione dei dati e ontologie

Il progetto WHOW ha sviluppato un "modello di rappresentazione del monitoraggio delle qualità delle acque" che è "basato interamente su uno standard del [W3C: semantic sensor network](https://www.w3.org/TR/vocab-ssn/)". Questo modello si basa sui concetti di:

- "osservo" (il dispositivo, es. un idrometro);  
- "caratteristica osservata" (es. altezza dell'acqua);  
- "risultato dell'osservazione";  
- "caratteristica di interesse" (es. la diga X o il fiume Y).

Tali concetti vengono indicati con l’acronimo **SOSA (Sensor, Observation, Sample, and Actuator).** Questo "modello generale si può adattare di fatto a diversi contesti."

Si è evidenziata la possibilità di "armonizzare i dati usando gli LLM, al fine di snellire un processo intrinsecamente lungo. Questo approccio potrebbe sfruttare i file CSV già estratti dai PDF e si basa sulla mappatura esistente nel modello ontologico. Inoltre, è stata sviluppata e resa disponibile pubblicamente una [pipeline per la trasformazione da CSV a RDF](https://github.com/whow-project/architecture), impiegando il linguaggio di mappatura RML (RDF Mapping Language).

## 3\. Dati di ISPRA e del portale acque

I [dati sulla qualità delle acque balneari](https://www.portaleacque.salute.gov.it/PortaleAcquePubblico/mappa.do), sono stati oggetto di discussione perché vengono estratti e  riutilizzati dal progetto [MareSì](https://maresi.app/) di Gabriele Scalici. Inizialmente, il sito del Ministero della Salute da cui venivano estratti i dati aveva una licenza chiusa e non permetteva il download in blocco. Grazie all'intervento di onData, la licenza è stata aperta, ma il download in blocco rimane un problema.

ISPRA ha elaborato i dati europei trasformandoli in Linked Data, seguendo i modelli sviluppati nel progetto. Questi dati sono consultabili sulla piattaforma lod.ispra.it. Si segnala inoltre che Arpa Puglia rilascia bollettini mensili contenenti dati selezionati.

## 4\. Il problema della tempestività e validazione dei dati

Un problema fondamentale riscontrato è la **carenza di dati in tempo reale sulla qualità dell'acqua**, poiché "noi ragioniamo sempre su dati relativi all'anno o a due anni precedenti, mai attuali". Questo ritardo è attribuibile al lungo processo di validazione: "ci vuole circa un anno per completare tutti i passaggi, dal prelievo del campione (andare al fiume con la bottiglia, raccogliere l'acqua), all'invio al laboratorio che esegue i test e deve validare i risultati con attenzione agli errori, fino alla restituzione dei dati e, solo a quel punto, alla pubblicazione".

La distinzione tra dati di quantità (come il livello dell'acqua nelle dighe) e dati di qualità è fondamentale, poiché i secondi richiedono la validazione in laboratorio, a differenza dei primi.

## 5\. Soluzioni proposte

- **Pubblicazione di dati non validati**: Si propone di "pubblicare il dato il dato non validato subito". Questo permetterebbe agli utenti di avere accesso immediato alle informazioni, pur essendo consapevoli del loro stato di validazione. Il Ministero della Salute si è opposto a questa idea per timore di "scatenare la psicosi delle persone".

- [**Vocabolario per la qualità dei dati (DQV):**](https://www.w3.org/TR/vocab-dqv/) È stato menzionato il "data quality vocabulary" del W3C, che che propone un framework per la descrizione della qualità dei dataset. Questo vocabolario può essere usato per indicare lo stato di validazione o completezza di un dato.Quindi puoi anche dire, guarda, questo dato non è completo, per esempio.”

- **Metadati sulla qualità**: Aggiungere "metadati per dare indicazioni agli utenti di un certo livello di qualità di quel dato." Questo include informazioni sulla completezza del dataset (es. quanti comuni copre una certa anagrafe).

- **Appiglio normativo**: Viene citato il Decreto Trasparenza (D.lgs. 33/2016, Articolo 6, comma 2): "l'esigenza di assicurare adeguata qualità delle informazioni diffuse non può in ogni caso costituita motivo per l'omessa o ritardata pubblicazione dei dati delle informazioni del documenti." Viene specificato che ciò comporta la pubblicazione dei dati, anche se le caratteristiche di qualità richieste non sono garantite, purché vengano indicati i motivi di tale mancanza.

- **Tracciabilità del Dato (PROV-O Ontology):** Esiste un altro standard del W3C, "[PROV ontology](https://www.w3.org/TR/prov-o/)", che permette di "indicare nella metadatazione tutti i passaggi del ciclo di vita di quel dato, indicando le attività che vengono fatte su quel dato, chi le fa, quando le fa". Questo aumenta notevolmente la qualità e la tracciabilità del dato.

- **Automazione con LLM e Workflow Management**: Il progetto WOW aveva sviluppato un ["tool kit" (disponibile su GitHub, open source con licenza MIT)](https://github.com/whow-project/architecture) che "ti consente di eh definire tu le varie fasi del processo... attraverso un workflow management system". Questo include la localizzazione e trasformazione dei dati, la pubblicazione e la validazione. Si suggerisce che gli LLM potrebbero "aiutarci in alcune fasi del processo" e soprattutto nella validazione e nell'arricchimento dei metadati.

## 6\. Nuovi sviluppi normativi e armonizzazione

È stato menzionato un "[decreto legislativo 18/2023](https://www.normattiva.it/eli/id/2023/03/06/23G00025/CONSOLIDATED) in cui veniva introdotto un nuovo processo di comunicazione dei dati relativi alla qualità dell'acqua", con l'obiettivo di costruire "un sistema informativo centralizzato" a partire dal 2026\. Si suggerisce che il modello ontologico del progetto WHOW, una volta "confluito in [schema.gov.it](http://schema.gov.it)", potrebbe essere riutilizzato da questi nuovi enti o sistemi, "forzando Arera a usare" tale standard.

## Conclusione

Il progetto WHOW ha gettato le basi per una gestione più efficace e trasparente dei dati sulla qualità dell'acqua attraverso l'uso di ontologie e Linked Data. Le sfide principali riguardano la tempestività della pubblicazione e la validazione dei dati. Tuttavia, esiste un solido quadro normativo (Decreto Trasparenza) e strumenti tecnici (DQV, PROV-O, workflow automatizzati) che possono facilitare la pubblicazione di dati di qualità, anche se non completamente validati, aumentando la fiducia dei cittadini e supportando decisioni informate. L'armonizzazione dei dati e l'adozione di standard condivisi (come schema.gov.it) sono passi fondamentali per il futuro.  
