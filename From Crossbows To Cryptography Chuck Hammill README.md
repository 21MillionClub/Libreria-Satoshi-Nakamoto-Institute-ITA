# Libreria-Satoshi-Nakamoto-Institute-ITA
From Crossbows To Cryptography: Techno-Thwarting The State

Chuck Hammill, November 1987

Presentato alla Future of Freedom Conference, novembre 1987.

La tecnologia, e in particolare la tecnologia informatica, ha spesso ricevuto una cattiva reputazione nei circoli libertari. Si tende a pensare a 1984 di Orwell, o a Brazil di Terry Gilliam, o ai rilevatori di prossimità che tenevano gli schiavi/cittadini di Berlino Est dalla loro parte del confine, o ai sofisticati dispositivi di intercettazione che Nixon usava per molestare coloro che erano sulla sua "lista dei nemici". Oppure, riconosciamo che per il prezzo di un biglietto del Concorde possiamo volare al doppio della velocità del suono, ma solo se prima passiamo attraverso un magnetometro gestito da un poliziotto governativo e gli permettiamo di frugare tra i nostri effetti personali se emette un segnale acustico.

Ma credo che questa mentalità sia un errore. Prima che esistessero i pungoli, i governi torturavano i loro prigionieri con mazze e tubi di gomma. Prima che esistessero i laser per le intercettazioni, i governi usavano binocoli e lettori di labbra. Sebbene il governo utilizzi certamente la tecnologia per opprimere, il male non risiede negli strumenti, ma in chi li utilizza.

In effetti, la tecnologia rappresenta una delle vie più promettenti per riconquistare le nostre libertà da coloro che le hanno rubate. Per sua stessa natura, favorisce i brillanti (che possono usarla) rispetto agli ottusi (che non possono farlo). Favorisce gli adattabili (che sono veloci a vedere i meriti del nuovo) rispetto ai pigri (che si aggrappano a metodi collaudati nel tempo). E quali sono le parole migliori per descrivere la burocrazia governativa se non "ottuso" e "lento"?

Uno dei più chiari e classici trionfi della tecnologia sulla tirannia è l'invenzione della balestra portatile. Con essa, un contadino non addestrato poteva ora colpire in modo affidabile e letale un bersaglio fino a cinquanta metri, anche se questo bersaglio era un cavaliere montato e munito di cotta. A differenza dell'arco lungo, che era indubbiamente più potente e poteva sparare più colpi per unità di tempo, la balestra non richiedeva un addestramento formale per essere utilizzata. Mentre la balestra lunga richiedeva un'elaborata coordinazione visiva, tattile e cinestesica per raggiungere un qualsiasi grado di precisione, chi la impugnava poteva semplicemente appoggiare l'arma alla spalla, mirare lungo la freccia stessa ed essere ragionevolmente sicuro di colpire il bersaglio.

Inoltre, dato che gli unici cavalieri a cavallo che potevano fare visita al contadino medio erano i soldati del governo e gli esattori delle tasse, l'utilità del dispositivo era evidente: Con esso, la plebe comune poteva difendersi non solo l'uno dall'altro, ma anche dai propri padroni governativi. Era l'equivalente medievale del proiettile perforante e, di conseguenza, re e sacerdoti (l'equivalente medievale di un Ufficio per l'alcool, il tabacco e le balestre) minacciavano rispettivamente la morte e la scomunica per il suo possesso illegale.

Guardando agli sviluppi successivi, vediamo come la tecnologia come l'arma da fuoco - in particolare il fucile a ripetizione e la pistola, seguiti poi dal cannone Gatling e dalle mitragliatrici più avanzate - abbia alterato radicalmente l'equilibrio del potere interpersonale e intergruppi. Non a caso la Colt .45 era chiamata "l'equalizzatore". Una fragile hostess di una sala da ballo, con una Colt in suo possesso, era ora in grado di difendersi dal più forte scavezzacollo di qualsiasi saloon. Anche le pubblicità dell'epoca riflettono la commercializzazione del fucile a cartuccia a ripetizione, dichiarando che "un uomo a cavallo, armato con uno di questi fucili, non può essere catturato". E, finché i suoi rapitori si affidavano agli acciarini o ai fucili a colpo singolo, la citazione è senza dubbio vera.

Aggiornando al presente, il cifrario a chiave pubblica (con un personal computer per farlo funzionare) rappresenta un salto di qualità equivalente in un'arma difensiva. Questa tecnica non solo può essere usata per proteggere i dati sensibili in proprio possesso, ma può anche permettere a due sconosciuti di scambiarsi informazioni su un canale di comunicazione insicuro - una linea telefonica intercettata, ad esempio, o una scrittura in cielo, se è per questo - senza essersi mai incontrati prima per scambiarsi le chiavi di cifratura. Con un computer da mille dollari, si può creare un cifrario che un CRAY X-MP da svariati megabuoni non può decifrare in un anno. Entro pochi anni dovrebbe essere economicamente possibile criptare in modo analogo le comunicazioni vocali e, subito dopo, le immagini video digitalizzate a colori. La tecnologia non solo avrà reso obsolete le intercettazioni, ma avrà completamente demolito il controllo del governo sul trasferimento delle informazioni.

Vorrei soffermarmi un attimo sulla matematica che rende possibile questo principio. Questo algoritmo è chiamato algoritmo RSA, dal nome di Rivest, Shamir e Adleman che lo hanno creato insieme. La sua sicurezza deriva dal fatto che, se un numero molto grande è il prodotto di due primi molto grandi, è estremamente difficile ottenere i due fattori primi dall'analisi del loro prodotto. "Estremamente" nel senso che se i primi p e q hanno 100 cifre ciascuno, il loro prodotto di 200 cifre non può essere fattorizzato in meno di 100 anni dal più potente computer attualmente esistente.

La parte "pubblica" della chiave consiste in (1) il prodotto pq dei due grandi primi p e q, e (2) un fattore, chiamato x, del prodotto xy dove xy=(p-1)(q-1)+1. La parte "privata" della chiave è costituita dall'altro fattore y.

Ogni blocco di testo da crittografare viene innanzitutto trasformato in un numero intero, utilizzando l'ASCII o anche una semplice rappresentazione A=01, B=02, C=03, ..., Z=26. Questo numero intero viene poi elevato alla potenza x mod(pq) e il numero intero risultante viene inviato come messaggio crittografato. Il destinatario decodifica portando questo intero alla potenza (segreta) y mod(pq). È possibile dimostrare che questo processo produrrà sempre il numero originale da cui è partito.

Ciò che rende questo sviluppo innovativo, e il motivo per cui si chiama crittografia a "chiave pubblica", è che posso pubblicare apertamente il prodotto pq e il numero x, mantenendo segreto il numero y: chiunque può inviarmi un messaggio criptato, cioè ax mod(pq), ma solo io posso recuperare il messaggio originale a, prendendo ciò che mi invia, elevandolo alla potenza y e prendendo il risultato mod(pq). Il passaggio rischioso (incontrarsi per scambiarsi le chiavi di cifratura) è stato eliminato. In questo modo, persone che potrebbero non fidarsi abbastanza l'una dell'altra da volersi incontrare, possono comunque scambiarsi messaggi cifrati in modo affidabile: ciascuna parte ha selezionato e diffuso la propria pq e la propria x, mantenendo la segretezza della propria y.

Un altro vantaggio di questo schema è la nozione di "firma digitale", che consente di autenticare la fonte di un determinato messaggio. Normalmente, se voglio inviarti un messaggio, elevo il mio testo in chiaro a alla tua x e prendo il risultato mod(la tua pq) e lo invio.

Tuttavia, se nel mio messaggio prendo il testo in chiaro a e lo elevo alla mia potenza (segreta) y, prendo il risultato mod(la mia pq), poi elevo il risultato alla vostra x mod(la vostra pq) e lo invio, allora anche dopo che avrete normalmente "decrittato" il messaggio, sembrerà ancora spazzatura. Se invece lo innalzate alla mia potenza pubblica x e prendete il risultato mod(la mia pq pubblica), non solo recupererete il messaggio originale in chiaro, ma saprete che nessuno, a parte me, può avervelo inviato (poiché nessun altro conosce il mio segreto y).

Queste sono le preoccupazioni che oggi tormentano l'Unione Sovietica sulla questione dei personal computer. Da un lato, essi riconoscono che gli scolari americani stanno crescendo con i computer come un luogo comune, come lo erano gli sliderules, anzi di più, perché ci sono cose che i computer possono fare che interessano (e istruiscono) i bambini di 3 e 4 anni. E sono proprio questi studenti che, una generazione dopo, si troveranno faccia a faccia con le loro controparti sovietiche. Per i sovietici trattenersi potrebbe essere un suicidio come continuare a insegnare l'arte della spada mentre gli avversari imparano la balistica. D'altra parte, qualsiasi altra cosa possa essere un personal computer, è anche una macchina per copiare squisitamente efficiente: un floppy disk può contenere fino a 50.000 parole di testo e può essere copiato in un paio di minuti. Se questo non fosse abbastanza minaccioso, il computer che esegue la copia può anche criptare i dati in modo pressoché infrangibile. Ricordate che nella società sovietica le macchine Xerox accessibili al pubblico sono sconosciute. Le relativamente poche fotocopiatrici esistenti sono controllate più intensamente di quanto non lo siano le mitragliatrici negli Stati Uniti.

Ora, la posizione "conservatrice" è che non dovremmo vendere questi computer ai sovietici, perché potrebbero utilizzarli in sistemi d'arma. La posizione "liberale" è che dovremmo venderli, nell'interesse del commercio e della cooperazione reciproca - e comunque, se non li vendiamo noi, ci sarà sicuramente qualche altra nazione disposta a farlo.

Da parte mia, sono pronto a suggerire che la posizione libertaria dovrebbe essere quella di darli ai sovietici gratuitamente e, se necessario, costringerli a prenderli... e se non funziona, caricare un SR-71 Blackbird e lanciarli su Mosca nel cuore della notte. Naturalmente pagando con una sottoscrizione privata, non con le tasse...

Confesso che questa non è una posizione che ha ottenuto molto sostegno tra i membri dello spettro politico convenzionale destra-sinistra, ma, dopo tutto, per dirla con le parole di uno dei personaggi di Illuminatus, siamo politici non euclidei: La distanza più breve per raggiungere un determinato obiettivo può non assomigliare affatto a quella che la maggior parte delle persone considererebbe una "linea retta". Con una visione del mondo sufficientemente lunga, si può sostenere che la rottura del monopolio governativo sovietico sul trasferimento delle informazioni potrebbe portare più facilmente all'indebolimento e, di fatto, alla definitiva dissoluzione dell'impero sovietico che non la produzione di un'altra dozzina di missili puntati su Mosca.

Ma ecco il problema: una visione del mondo "abbastanza lunga" suggerisce che i malvagi, gli oppressivi, i coercitivi e i semplicemente stupidi "avranno ciò che si meritano", ma ciò che non è immediatamente chiaro è come il resto di noi possa sfuggire all'uccisione, alla schiavitù o all'impoverimento nel processo.

Quando i liberali e gli altri collettivisti hanno iniziato ad attaccare la libertà, possedevano un'economia ragionevolmente stabile, sana e funzionante, e un tempo quasi illimitato per procedere a ostacolarla e smantellarla. Una politica di gradualità politica era almeno concepibile. Ora, invece, abbiamo un'economia patchwork e folle tenuta insieme da fili di ferro e sputi. Lo Stato non solo ci tassa per "sfamare i poveri", inducendo al contempo gli agricoltori a macellare le mucche da latte e a far salire i prezzi dei prodotti alimentari, ma allo stesso tempo si gira e sovvenziona la ricerca sui prodotti chimici per l'agricoltura, progettati per aumentare la resa del latte delle mucche rimaste in vita. Oppure il fatto che un calo del prezzo del petrolio sia considerato potenzialmente spaventoso quanto un aumento analogo di qualche anno fa. Quando il prezzo saliva, si diceva, l'economia rischiava il collasso per mancanza di energia. L'aumento del prezzo è stato definito "l'equivalente morale di una guerra" e i federali sono entrati in azione. Per la prima volta nella storia americana, la velocità con cui si guida l'auto per andare al lavoro la mattina è diventata una questione di interesse federale. Ora, quando il prezzo del petrolio scende, rischiamo di nuovo di avere problemi, questa volta perché le compagnie petrolifere americane e le nazioni del Terzo Mondo che vendono petrolio potrebbero non essere in grado di pagare i loro debiti con le nostre banche, che hanno un eccesso di credito. La panacea suggerita è che il governo dovrebbe ora rialzare i prezzi del petrolio che l'OPEC ha abbassato, attraverso una nuova tassa sul petrolio. Dal momento che il governo sta cercando di aumentare i prezzi del petrolio più o meno nella stessa misura in cui lo ha fatto l'OPEC, come possiamo chiamarlo se non "l'equivalente morale di una guerra civile - il governo contro il suo stesso popolo?".

E, classicamente, nel commercio internazionale, riuscite a immaginare qualsiasi entità al mondo, a parte un governo, che si rivolge a un tribunale sostenendo che un venditore gli sta vendendo merci a prezzi troppo bassi e chiedendo non solo che quel venditore cattivo sia obbligato dal tribunale ad aumentare i suoi prezzi, ma anche che sia punito per l'atto di abbassarli in primo luogo? Quindi, mentre gli statalisti possono permettersi di impiegare un paio di centinaia di anni per distruggere la nostra economia e le nostre libertà, noi non possiamo certo contare su un periodo equivalente di stabilità in cui reclamarle. Io sostengo che esiste quasi un effetto "buco nero" nell'evoluzione degli Stati nazionali, proprio come nell'evoluzione delle stelle. Una volta che la libertà si contrae oltre una certa misura minima, lo Stato deforma il tessuto del continuum politico su se stesso al punto che il successivo riemergere della libertà diventa quasi impossibile. Una buona illustrazione di ciò può essere vista nell'ambito dei cosiddetti pagamenti del "welfare". Quando coloro che si abbeverano alla mangiatoia pubblica sono più numerosi (e quindi votano di più) di coloro le cui tasse devono rifornire la mangiatoia, quale altra scelta ha una democrazia se non quella di perpetuare ed espandere il prelievo da parte di pochi a beneficio non meritato di molti? Andate all'ufficio del "welfare" più vicino, trovate solo due persone che ricevono il sussidio... e riconoscete che tra loro formano un blocco di voti che può mettere in minoranza per sempre la questione di chi possiede la vostra vita e i frutti del vostro lavoro.

Quindi, essenzialmente, coloro che amano la libertà hanno bisogno di una sorta di "vantaggio" se vogliamo prevalere. Ovviamente non possiamo usare l'"orientamento all'altro" degli altruisti: "lavorare, schiavizzare, soffrire, sacrificarsi, in modo che la prossima generazione di un miliardo di sconosciuti a caso possa vivere in un mondo migliore". Riconoscete che, per quanto immorale possa essere, questo appello è comunque estremamente potente nella cultura di oggi. Se riuscite a convincere le persone a lavorare energicamente per una "causa", preoccupandosi solo del loro benessere personale per rimanere abbastanza vivi e sani da continuare a lavorare, allora avete un serbatoio di energia davvero enorme a cui attingere. È altrettanto chiaro che questo è proprio il tipo di appello che, tautologicamente, non può essere utilizzato per obiettivi egoistici o libertari. Se stasera mi alzassi di fronte a voi e vi dicessi qualcosa del tipo: "Ascoltate, seguitemi mentre vi enuncio la mia nobile "causa", contribuite con il vostro denaro a sostenere la "causa", rinunciate al vostro tempo libero per lavorare per la "causa", impegnatevi disinteressatamente per realizzarla e poi (dopo che voi e i vostri figli sarete morti) forse i figli dei vostri figli vivranno davvero sotto l'egoismo", pensereste tutti che sono impazzito. E naturalmente avreste ragione. Perché il punto che sto cercando di fare è che il libertarismo e/o l'egoismo si diffonderanno se, quando e come i singoli libertari e/o egoisti troveranno redditizio e/o piacevole farlo. E probabilmente solo allora.

Pur non denigrando il concetto di azione politica, non credo che sia l'unica strada, e nemmeno necessariamente la più conveniente, per aumentare la libertà nel nostro tempo. Considerate che, per una frazione dell'investimento in tempo, denaro e sforzi che potrei fare per cercare di convincere lo Stato ad abolire le intercettazioni e tutte le forme di censura, posso insegnare a ogni libertario interessato come usare la crittografia per abolirle unilateralmente.

C'è una massima - un proverbio - generalmente attribuita agli eschimesi, che molto probabilmente la maggior parte dei libertari ha già sentito. E anche se probabilmente non avreste nulla da obiettare, potreste pensare di averla già sentita abbastanza spesso e che non abbia più nulla da insegnarci, e inoltre che forse siete persino stanchi di sentirla. Pertanto, lo ripeterò ora:

Se dai un pesce a un uomo, dice il proverbio, lo sfami per un giorno. Ma se insegni a un uomo a pescare, lo nutrirai per tutta la vita.

La citazione è stata probabilmente utilizzata in un contesto di "workfare" e "welfare", ovvero che se si vuole veramente aiutare qualcuno in difficoltà, bisogna insegnargli a guadagnarsi il proprio sostentamento, non semplicemente a chiedere l'elemosina. E naturalmente questo è vero, se non altro perché la prossima volta che avrà fame, potrebbe non esserci nessuno in giro disposto o addirittura in grado di dargli un pesce, mentre con le informazioni su come pescare sarà completamente autosufficiente.

Ma ritengo che questo esaurisca solo il contenuto di primo ordine della citazione e che, se non ci fosse altro da ricavarne, vi avrei fatto perdere tempo citandola di nuovo. Dopo tutto, sembra avere quasi un taglio cripto-altruista, come se volesse implicare che dovremmo strutturare le nostre attività in modo da massimizzare i benefici per i mendicanti affamati che possiamo incontrare.

Ma riflettete:

Supponiamo che questo eschimese non sappia pescare, ma sappia cacciare i trichechi. Voi, d'altra parte, avete spesso sofferto la fame durante i vostri viaggi nel paese dei trichechi perché non avevate idea di come catturarli e loro si mangiavano la maggior parte del pesce che riuscivate a prendere. E ora supponiamo che voi due decidiate di scambiarvi informazioni, barattando le conoscenze di pesca con quelle di caccia. La prima cosa da osservare è che una transazione di questo tipo confuta categoricamente e senza ambiguità la premessa marxista secondo cui ogni scambio deve avere un "vincitore" e un "perdente", ovvero l'idea che se una persona guadagna, deve necessariamente essere a "spese" di un'altra persona che perde. Chiaramente, in questo scenario, non è così. Ciascuna parte ha guadagnato qualcosa che prima non aveva, e nessuna delle due è stata sminuita in alcun modo. Quando si tratta di scambio di informazioni (piuttosto che di oggetti materiali) la vita non è più un gioco a somma zero. Si tratta di un concetto estremamente potente. La "legge dei rendimenti decrescenti", la "prima e la seconda legge della termodinamica" - tutte quelle "leggi" che limitano le nostre possibilità in altri contesti - non ci vincolano più! Questa sì che è anarchia!

Oppure consideriamo un'altra possibilità:

Supponiamo che questo eschimese affamato non abbia mai imparato a pescare perché il sovrano del suo Stato nazionale ha decretato la pesca illegale. Poiché i pesci contengono piccole lische pericolose e talvolta spine acuminate, ci dice, lo Stato ha decretato che il loro consumo e persino il loro possesso sono troppo pericolosi per la salute del popolo per essere consentiti... anche da adulti consapevoli e volenterosi. Forse perché si pensa che i corpi dei cittadini siano di proprietà del governo e che quindi sia compito dello Stato punire chi si prende cura in modo improprio di una proprietà del governo. O forse perché lo Stato estende generosamente agli adulti competenti i "benefici" che fornisce ai bambini e ai malati mentali: in particolare, una tutela a tempo pieno e onnipervasiva, in modo che non debbano preoccuparsi di fare scelte su comportamenti ritenuti fisicamente rischiosi o moralmente "cattivi". Ma, in ogni caso, voi restate a guardare stupefatti, mentre il vostro informatore eschimese vi racconta come questa legge sia presa così sul serio che un suo amico è stato recentemente incarcerato per anni per il reato di "possesso di nove once di trota con l'intento di distribuirle".

Ora potete concludere che una società così grottescamente oppressiva da applicare una legge di questo tipo è semplicemente un affronto alla dignità di tutti gli esseri umani. Potreste andare oltre e decidere di impegnare una parte del vostro tempo discrezionale e ricreativo specificamente nel compito di ostacolare l'obiettivo di questo tiranno. (La vostra motivazione può essere "altruistica", nel senso di voler liberare gli oppressi, o "egoistica", nel senso di dimostrare che siete in grado di superare in astuzia l'oppressore, o molto probabilmente una combinazione di queste o forse anche di altre motivazioni).

Ma poiché non avete alcun desiderio di diventare un martire della vostra "causa", non avete intenzione di organizzare una campagna militare, né di provare a far passare una barca di pesci attraverso il blocco. Tuttavia, è qui che la tecnologia, e in particolare l'informatica, può centuplicare letteralmente la vostra efficacia. Dico "letteralmente", perché per una frazione dello sforzo (e praticamente nessuno dei rischi) che comporta il contrabbando di un centinaio di pesci, si possono facilmente produrre un centinaio di copie Xerox delle istruzioni di pesca. Se il governo che ha come obiettivo, come l'America di oggi, permette almeno di discutere apertamente di argomenti la cui attuazione è limitata, allora questo dovrebbe essere sufficiente. Ma se il governo tenta di sopprimere anche il flusso di informazioni, allora dovrete fare un po' più di fatica e magari scrivere il vostro manuale di pesca su un floppy disk criptato secondo i parametri della chiave pubblica del vostro mitico eschimese. Ma per quanto riguarda l'aumento dell'accesso al pesce nel mondo reale, avete fatto dei veri e propri passi avanti, che possono continuare a crescere man mano che altri diffondono le informazioni che avete fornito. E non avete dovuto sprecare il vostro tempo per cercare di convertire gli avversari ideologici, e nemmeno per cercare di conquistare gli indecisi. Ricordate il detto di Harry Browne, tratto da "Freedom in an Unfree World", secondo cui il successo di qualsiasi impresa è in genere inversamente proporzionale al numero di persone la cui persuasione è necessaria per la sua realizzazione.

Se si guarda alla storia, non si può negare che sia stata drammaticamente plasmata da uomini con nomi come Washington, Lincoln, Nixon, Marcos, Duvalier, Gheddafi e i loro simili. Ma è stata anche plasmata da persone con nomi come Edison, Curie, Marconi, Tesla e Wozniak. E quest'ultima forma è stata almeno altrettanto pervasiva, e non altrettanto sanguinosa.

Ed è qui che sto cercando di portare il progetto LiberTech. Piuttosto che implorare lo Stato di non schiavizzarci, saccheggiarci o costringerci, propongo una rete libertaria che diffonda le tecnologie con cui possiamo conquistare la libertà per noi stessi.

Ma qui dobbiamo essere un po' cauti. Sebbene non sia (al momento) illegale criptare le informazioni quando il governo vuole spiarci, non c'è alcuna garanzia di ciò che il futuro potrebbe riservarci. Ad esempio, sono state presentate proposte di legge che avrebbero reso un crimine indossare un giubbotto antiproiettile quando il governo vuole spararvi. In altre parole, se si dovessero commettere determinati crimini indossando un giubbotto di kevlar, questo fatto costituirebbe un crimine federale a sé stante. Che io sappia, questa legge non è ancora passata... ma indica come la pensa il governo.

Altre applicazioni tecnologiche, tuttavia, comportano effettivamente dei rischi legali. Riconosciamo, ad esempio, che chiunque abbia aiutato uno schiavo a fuggire sulla "ferrovia sotterranea" prima della Guerra Civile stava facendo un uso chiaramente illegale della tecnologia, poiché il governo sovrano degli Stati Uniti d'America a quel tempo considerava la compravendita di esseri umani accettabile quanto la compravendita di bestiame. Allo stesso modo, durante il proibizionismo, chiunque usasse la propria vasca da bagno per far fermentare lievito e zucchero nella droga psicoattiva illegale, l'alcol - la sostanza controllata, il vino - usava la tecnologia in un modo che poteva essere ucciso dagli agenti federali per il suo "crimine" - sfortunatamente per non essere restituito alla vita quando il Congresso fece marcia indietro e autorizzò nuovamente l'uso di questa droga.

Quindi, per citare un ex presidente, cospiratore non accusato e criminale graziato: "Lasciatemi chiarire una cosa". Il Progetto LiberTech non sostiene, non partecipa e non cospira alla violazione di alcuna legge, per quanto oppressiva, incostituzionale o semplicemente stupida possa essere. Si impegna a descrivere (solo a scopo educativo e informativo) i processi tecnologici, e alcuni di questi processi (come pilotare un aereo o fabbricare un'arma da fuoco) potrebbero richiedere una licenza appropriata per essere eseguiti legalmente. Fortunatamente, non è necessaria alcuna licenza per la distribuzione o la ricezione delle informazioni in sé.

Quindi, la prossima volta che guardate la scena politica e vi disperate, pensando: "Beh, se il 51% della nazione e il 51% di questo Stato e il 51% di questa città devono diventare libertari prima che io sia libero, allora qualcuno potrebbe anche tagliare la mia dannata gola ora e porre fine alle mie sofferenze" - riconoscete che non è così. Esistono modi per rendersi liberi.

Se desiderate esplorare tali tecniche attraverso il Progetto, siete invitati a darmi il vostro nome e indirizzo - o un nome e un indirizzo di posta falsi, se è per questo - e sarete inseriti nella mailing list della mia newsletter pubblicata in modo irregolare. Anche gli amici o i conoscenti che pensate possano essere interessati sono i benvenuti. Non vi chiedo nemmeno buste affrancate e autoindirizzate, poiché la mia tipografia è in grado di gestire le etichette postali e le spese postali effettive non sono così alte rispetto agli altri sforzi per far uscire un numero. Se avete un'idea da condividere, o anche un prodotto utile da pubblicizzare, sarò lieto di farvelo scrivere per la pubblicazione. Anche se volete essere il proverbiale "free rider" e beneficiare solo di ciò che gli altri contribuiscono, siete sempre i benvenuti: Tutto sarà di dominio pubblico; sentitevi liberi di copiarlo o di regalarlo (o di venderlo, se riuscite a guadagnarci mentre io mi faccio pubblicità a tutta pagina cercando di regalarlo, avete certamente diritto al vostro profitto capitalistico...). In ogni caso, ogni applicazione di questi principi dovrebbe rendere il mondo un po' più libero, e sono certamente disposto a sostenerlo, almeno per il prossimo futuro.

Vi lascio con un'ultima riflessione: Se non imparate a trasformare i vostri vomeri in spade prima che mettano fuori legge le spade, allora dovrete sicuramente imparare prima che mettano fuori legge anche i vomeri.

-Chuck Hammill







