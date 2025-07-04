Certamente, ecco la trascrizione corretta e con la punteggiatura appropriata.

Io, in realtà, faccio soltanto una cosa molto rapida. Borruso lo conosciamo, è uno bravo, no? Ma quelli scarsi, che usano, cosa possono fare? Faccio vedere... i finti modesti sono terribili. No, io... io non sono... se lui, che non è uno sviluppatore... figuratevi io. Allora, vediamo se... ecco.

Allora, io per lavoro, tra le varie cose, mi occupo di progettazione: progettazione europea, bandi, bla bla bla e tutto questo mondo qui. Questo qui è un visualizzatore di tabelle, banalissimo HTML, in cui ci sono dati su progetti europei o bandi, cose, no? Io li devo monitorare, ce ne sono mille di fonti e quindi mi sono detto: «Ah, vediamo se è vero quello che dice Borruso. Provo a farne uno».

Sono andato su un portale, ho provato a usare l'LLM, mi sono fatto il mio scraper — adesso ve li faccio vedere. Alla fine ne ho fatti, cosa sono? Dieci. C'è un sito della Regione Emilia-Romagna, alcune fonti dati europee, in Italia One-Pass, INPAT... ci sono dei bandi, un sito che pubblica bandi sul mondo del giornalismo, Regione Lombardia e New Items, invece, è un filtro dei nuovi.

Faccio vedere che cosa ha fatto lui o lei, non so come chiamarlo. Questo era il sito dove ho messo tutto. Praticamente, facendo il gioco che ha fatto Andrea, cioè: lui è bravo, lo fa per strutturare i dati; io, invece, i dati non ce li ho, lo faccio per fare scraping. Quindi, banalmente, entri sulla pagina, copi il DOM (quindi l'HTML), lo prendi e lo dai all'LLM: «Voglio fare lo scraping di questi dati qui, di bandi che ci sono, che hanno questa caratteristica, no? Che hanno un titolo, eccetera». E lui mi ha creato — ve ne faccio vedere uno, ma, in realtà, poi mi ha guidato — mi ha creato lui da solo, personalizzato. Ovviamente c'erano dei bug che gli dovevo dire: «Questo non va bene, fai di là, eccetera». Mi ha creato 10 scraper in Python. Io non avevo mai scritto una riga di Python prima, tranne quando ho comprato il mini pocket, che ho fatto i primi giochetti, poi c'era da scaricare... Noi da Milano siamo veloci, solo fatturati, quindi 'sta cosa era da troppo lontano, poi dovevo studiare. Invece l'LLM me l'ha creato.

Quindi mi importa le librerie, mi definisce tutto, scritto soprattutto in modo che me lo commenta. Quindi quel poco che sapevo prima di Python l'ho anche un pochettino aumentato, perché oltre ad avere la soluzione, me l'ha anche spiegato. Quando dicono, no?, si leggono, si vedono 'ste interviste di gente che dice: «Eh, l'intelligenza artificiale può sviluppare software». Mistica. Nel mio caso, io ero a zero, cioè, facevo HTML eccetera, Python non l'avevo mai usato. E non solo. Poi io gli do insieme tutti gli script che ha creato e gli dico: «Voglio che lo standard... perché comunque leggo le cose che scrive Andrea... voglio che i dati in output abbiano lo stesso standard, no? Quindi che tutte le date siano formattate allo stesso modo», perché io poi li metterò in un sistema. E questo, quindi, è l'altro lato.

Poi il repo, se vi interessa, ve lo condivido. Comunque, in sostanza, partendo da zero, senza mai aver usato questo LLM, quindi semplicemente rompendo un po' le scatole come Dennis, ma niente di particolare, mi sono messo a studiare. Ho trovato un po' di tempo, ho dedicato un po' di tempo e mi sono creato tutto il mio sistema. Quindi, vabbè, con una paginetta HTML, uno script-ino che mi gestisce questi file, gli script Python che mi scaricano i file, faccio una &quot;run&quot; e mi scaricano tutti i dati quando voglio io. Quindi ogni mattina gli dico: «Fai, scarica tutto». Preferisco controllarla a mano, però, diciamo, ogni mattina premo un pulsante, fa tutto, mi aggiorna la pagina, aggiorno online la versione dei bandi e non ho bisogno di andare su tutti 'sti siti a cercarmi quali sono gli ultimi.

Quindi questa non è una versione, diciamo, narrativa, non dimostrativa, ma quello che ha fatto vedere lui prima non è che è la punta dell'iceberg. Molto banale.

Una domanda: quanto ci hai messo a costruire tutto questo?

All'inizio smadonnavo un po', perché, per quanto tu possa fare l'esperto e sentirti consapevole, in realtà entrare nelle dinamiche... ma banalmente, capire anche, che ne so, i path dell'XPath, del CSS, no? Adesso ci metto un'ora. Cioè, una cosa che prima non sapevo fare, per cui ci avrei messo un mese per imparare a fare uno script Python, adesso, dopo un po' di esercitazione, ci metto un'ora. Quindi io non so dove ci porta 'sta roba, però sicuramente ci sono tutta una serie di cose che prima era impensabile si potessero fare e oggi invece si possono fare. E io lo trovo allucinante.

Un altro caso d'uso banale: dovevo fare un'analisi di dati sul conto corrente. Incredibile, l'estratto conto di un anno. Ne parlo, ovviamente, come tutti noi italiani, scrivo ad Andrea. Lui comincia a dire, giustamente: «Guarda che ci sono delle librerie anche fighissime...». Poi le ho provate, e via dicendo. Modalità tradizionali, come si diceva prima. A un certo punto, però, lui giustamente dice: «Ma perché non lo facciamo fare all'AI?». C'è il tema dei dati personali, però con gli LLM puoi avere anche dei modelli in locale, più lenti, più leggeri. C'è tutto un dibattito tra locale e cloud, eccetera. Insomma, alla fine mi ha estratto, col formato che volevo io, 90 pagine di movimenti bancari di un anno, qualsiasi cosa, da questi PDF stranissimi, fatti in maniera schifosa, che anche i sistemi tradizionali non riuscivano a leggere perché c'erano i pattern sovrapposti. I PDF sono un po' complicati, diciamo. Me li ha estratti in, boh, 5 minuti. 5 minuti! Una roba che io... Quindi la potenzialità è effettivamente straordinaria, soprattutto, mi sembra, nella strutturazione del dato. Questa cosa qui mi sembra molto rilevante, cioè il fatto che tu gli butti dentro qualcosa, qualsiasi cosa, e guidato in un certo modo, con i &quot;guardrails&quot;, no?, come dicono quelli bravi, se tu gli dici &quot;se c'è questa cosa&quot; e gli dai una forma, un formato... non so come dirlo, però per me m'ha cambiato la vita.

Per esempio, io utilizzo, faccio interrogazioni alle API del portale nazionale e quando non lo butti giù... No, no, è una leggenda. [Musica] Ed è interessantissimo perché l'output JSON alle volte non mi serve, mi piace un output discorsivo perché voglio semplicemente ragionare su un'idea. Mi stoppo su 100 risultati per evitare problemi di token, ma è comodissimo. Diciamo, la prima analisi che noi facciamo, noi che lavoriamo con i dati, ti apre delle porte incredibili.

Altro intervento:

C'è tutta questa prima analisi di esplorazione con questi motori, che sono tanti, perché attenzione: OpenAI, Anthropic, Mistral, hanno tutti dei prodotti a riga di comando con cui fare cose, anche cose molto più avanzate. Però questo, secondo me, è uno strumento molto generalista, molto orizzontale, molto comodo, molto pronto all'uso. Io lo uso su Linux, ma è Python, quindi si installa anche... Sì, l'ho installato pure su Windows allo stesso modo. Non solo, puoi metterci dentro tutti i modelli che vuoi, è un wrapper di modelli. E io, il mio default, è Mistral, perché comunque io ancora ci vedo, nell'Europa, un pochettino... e per quanto siano francesi, il mio default anche sul telefono è Mistral. Quindi tutte le cose di base le faccio con Mistral, ma funziona anche perché l'approccio a schema è nativo su tutti gli LLM, su tutti i motori, e quindi lo puoi fare su Mistral, su Gemini o &quot;Gèmini&quot;, come lo chiamate voi.

Nuovo intervento:

Stef, vorrei chiedervi un'opinione, a parte il fatto che voi siete tutti scarsissimi, a partire da Borruso. Vabbè, ma che io sia più scarso di Borruso penso che sia ovvio, cioè, tautologico. A parte questo, volevo sapere, visto che comunque, dagli interventi che abbiamo visto precedentemente, no?, il problema è la produzione dei dati, il processo dei dati. Questo strumento, o comunque questi nuovi strumenti che avete illustrato, penso possa essere un acceleratore in questo senso. Poi, appunto, volevo sapere la vostra opinione se effettivamente possono essere un acceleratore nei confronti di una PA che, evidentemente, ha in quel punto lì il granello che fa bloccare tutto.

Risposta:

Dico la mia, poi secondo me Antonio e Giorgia sono meglio su questo. Secondo voi potrebbe essere questo, Andrea, un qualcosa che riesce a sbloccare? Ovviamente non sono strumenti per tutti, però io penso che con un'adeguata formazione e con adeguati fondi, magari, possano aprire possibilità anche a tutta una platea di persone che, con un'adeguata formazione, possono poi arrivare a fare cose che prima invece erano dedicate solo ai data scientist o comunque a persone che avessero un background tecnico-scientifico, che ovviamente non poteva essere appannaggio di chiunque nella Pubblica Amministrazione. Potrebbe essere questa una chiave di volta, secondo voi?

Altra risposta:

Secondo me, il punto prima è: &quot;lo vuoi fare?&quot;. E parlo di quella regione, nel senso, gli strumenti sono eccezionali. Se ti metti con obiettivo la qualità, l'automazione, i processi messi sotto controllo... per esempio, fare controlli automatici o scrivere codici per fare controlli automatici. L'oggettino che crea la descrizione &quot;frictionless&quot; poi puoi utilizzarlo per fare controllo, perché se il dato va fuori schema, quello schema te lo controlla. Quindi la risposta è sì, però, secondo me, il punto è se lo vuoi fare. E non vale solo per la PA, vale per tutti noi: aziende, cittadini. Quindi per me la risposta è questa, non so che ne pensano Giorgia e Antonio. Però, &quot;se lo vuoi fare&quot; e &quot;se c'è budget&quot; — l'altro punto che hai detto e non è da poco. Perché mi sembra che l'AgID, qui rappresentata... non so loro due, ma sembra di capire che lo staff sia poco rispetto agli obiettivi importantissimi che hanno.

Altro intervento:

Vorrei dare una risposta diversa. Diciamo, io sto facendo dei corsi sull'uso di questi strumenti di intelligenza artificiale da &quot;practitioner&quot;, diciamo così, tecnicamente, non certo dall'aspetto teorico, però studio l'argomento da un bel po', specificamente da oltre un anno e mezzo. Allora, dopo un corso, mando un messaggio alla classe, parliamo di LLM, e in Lombardia mi ha risposto un tizio. Mi ha detto — e guardate che quello che sta dicendo 'sto tizio è paro paro quello che diceva prima Andrea, no? — «Il manuale... mi si è rotto il forno». Mi ha trovato il manuale di fabbricazione, se l'è mangiato, gli ho detto cosa non funzionava, gli ho dato una foto del display, mi ha dato due possibili cause e tre soluzioni, dalla più soft alla più alta. Per ora funziona e non ho chiamato il tecnico. Cioè, io penso che questa cosa qua abiliti chiunque, potenzialmente. Dipende sempre da come usiamo gli strumenti.

Discussione finale:

* Voce 1: Però c'è un tema di budget. Nel senso che cinque anni fa fare queste cose significava formare del personale con determinate tecniche e con determinati strumenti che avevano una certa richiesta di conoscenza. Ora la richiesta di conoscenza c'è, ma con la voglia, la forbice si allarga un po' di meno.
* Voce 2: Penso che la formazione... la rampa è sicuramente... no, è come con la ricchezza: quando tutti diventano più poveri, i poveri sono più poveri e i ricchi sono meno poveri.
* Voce 1: La forbice si allarga! Perché se io ho voglia di imparare, allora mi metto là, come hai fatto tu, e imparo. Ma se io sono un dipendente di una Pubblica Amministrazione che non sono né incentivato, né premiato, né niente, a me chi me lo fa fare di ammazzarmi al lavoro? La forbice inevitabilmente si allarga.
* Voce 3: In questo momento la rapidità è tale, ragazzi, siamo tutti spiazzati, ma anche il mondo della ricerca è rimasto spiazzato. Posso garantire che dentro al nostro istituto, quando è venuto fuori OpenAI, c'è stato un momento di email tipo: «Oddio, cosa facciamo adesso del nostro futuro?», perché sembrava che avessero già fatto tutto. Chi sapeva fare la virgola si sentiva Dio, ora vede che quello che fa lui lo può fare tranquillamente un altro.
* Voce 4: Il lavoro che ha fatto Gabriele con la storia... ragazzi, si sono messi loro lì. È arrivato Squad, «Ciao, quella cosa che tu hai fatto, io gliela chiedo e lui mi risponde». Non è così, non è così! La devi pensare prima! Se non riesci a pensarla... Però vi invito davvero a cercare di capire quale genere di domande potremmo fare fra due anni per avere delle risposte, senza che stiamo lì a pensare a quello che non funziona, al sindaco, a quell'altro e all'utente giovane...
* Voce 5: Se ci pensate, è proprio il pane per la PA, perché la Pubblica Amministrazione, teoricamente, è regolata da norme che hanno una logica. Uno strumento così, che continuerà ad imparare chi siamo noi, come vogliamo sentirci dire le cose, quali tipi di problemi accogliamo e quali altri invece per noi sono dei vincoli che assolutamente devono essere superati... loro lo sapranno. Non c'è discorsività lì, è logica, e quindi diventerà sempre più semplice rispondere, per come noi vogliamo, pur ponendo malamente le domande.
* Voce 6: Sarà una giustificazione per la PA che non deve migliorare, perché tanto c'è il modello che migliora.
* Voce 7: Siamo ancora lontani, e questo ci tengo a dirlo, dal fatto che capiscano. Per ristrutturare il dato con una semantica, eccetera, tu puoi fare certe cose...
* Voce 8: No, secondo me no. Cioè, perché la gente pensa che arriveranno a capire come capiamo noi? Ma siete lontani da questa cosa, lontanissimo. Il problema è se arriveranno a capire come *non* capiamo noi. È anche peggio, perché magari vanno avanti e ci portano da un'altra parte. E già ce l'abbiamo il problema adesso.
* Voce 9: Copiare lo stile... la grande dicotomia nella storia dell'intelligenza artificiale è quella che diceva prima Giorgia, no? Simbolica o non simbolica. Quella roba che stiamo usando oggi non è simbolica, quindi la conoscenza non è formalizzata. È una costellazione di minchiate nel cielo che più o meno, probabilisticamente, funzionano. Io credo moltissimo nell'approccio formalizzato, perché se la legge dice che tu a 18 anni sei maggiorenne e io lo dico all'AI, è quella cosa lì, non è &quot;probabilmente&quot;.
* Voce 10: Parliamo, ad esempio, di stile, di creare lo stile di un determinato artista. Ha creato quello stile magari perché prima non esisteva, è andato al di là di ciò che è concepito come normale. E siccome comunque gli LLM vanno a pescare dalla cima della distribuzione normale, secondo me si rischia un po' di limitare la creatività. Si rischia che i nuovi artisti si possano appoggiare su questo comfort di dire: «Faccio un quadro uguale a questo stile» o «Scrivo in quest'altro stile», invece di pensare che le cose possano essere fatte in un modo totalmente diverso. Un po' quello che di solito fa l'arte: andare al di là di ciò che è concepito come normale. Anche a livello di codice, quando si utilizza tantissimo il co-pilota... la cosa che funziona magari non è la più bella, non è la più efficiente, però funziona. E magari si rischia che grandi società, anche le PA, si affidino a questa cosa che funziona e che magari apra tantissime falle che potrebbero essere gestite in maniera più efficiente, più bella. Questo è un grosso tema.
* Voce 11: Io ho studiato informatica: &quot;basta che funzioni&quot; è proprio una roba mia! [Applauso]