
Consiste nell'applicare i principi della programmazione ad oggetti ma per definire **cosa** un prodotto software deve fare (l'Object Oriented Design - OOD definisce, con un approccio ad oggetti, **come** un prodotto software deve fare quanto specificato durante l'OOA).

OOA e OOD devono fornire, ciascuno dal proprio punto di vista, una rappresentazione corretta, completa e consistente:
- degli aspetti statici e strutturali relativi ai dati (**modello dei dati**).
- degli aspetti funzionali del sistema (**modello comportamentale**).
- degli aspetti di "controllo" e di come le funzioni del modello comportamentale modificano i dati introdotti nel modello dei dati (**modello dinamico**).
# Metodi di OOA

Un **metodo di OOA** è l'insieme delle procedure, tecniche e strumenti usati per un approccio sistematico alla gestione e allo sviluppo della fase di OOA.

L'**input** di un metodo di OOA è l'**insieme dei requisiti utente**, mentre l'**output** è l'**insieme dei modelli del sistema** che definiscono le specifiche del prodotto software, entrambi sono contenuti nel documento di analisi dei requisiti.

I metodi di OOA usano **notazioni visuali** (**diagrammi**), ma possono essere affiancati da metodi per la definizione dei requisiti di sistema di tipo testuale tipo il linguaggio naturale strutturato.

Lo sviluppo dei modelli di OOA **non è sequenziale**, ma avviene in parallelo. Ciascun modello (dei dati, comportamentale e dinamico) fornisce informazioni utili per gli altri modelli. Usando un **approccio iterativo**, con aggiunta di dettagli per raffinamenti successivi (**iterazioni**).
# Alcuni Metodi di OOA e OOD

1. **Catalysis**: indicato per lo sviluppo di sistemi software a componenti distribuiti.
2. **Objectory**: ideato da I. Jacobson che fonda lo sviluppo di prodotti software ad oggetti sull’individuazione dei casi d’uso utente (use case driven).
3. **Shlaer/Mellor**: metodo OO particolarmente indicato per lo sviluppo di sistemi software real-time.
4. **OMT (Object Modeling Technique)**: metodo sviluppato da J. Rumbaugh basato su tecniche di modellazione del software iterative. Pone in particolare risalto la fase di OOA.
5. **Booch**: metodo basato su tecniche di modellazione del software iterative. Pone in particolare risalto la fase di OOD.
6. **Fusion**: metodo sviluppato dalla HP a metà degli anni novanta. Rappresenta il primo tentativo di standardizzazione per lo sviluppo di software orientato agli oggetti. Si basa sulla fusione dei metodi OMT e Booch.

Di particolare importanza sono i metodi: **Objectory**, **OMT** e **Booch**.
# UML

L'**UML (Unified Modeling** **Language)** è una notazione per la descrizione di sistemi software (orientati agli oggetti). Si compone di nove formalismi di base (diagrammi con semantica e notazione data) e di un insieme di estensioni. È stato introdotto per unificare le notazioni di OOA e OOD che prima erano separate. Grazie all'**OMG** viene adottato universalmente.

**Unified Software Development Process** (in breve **Unified Process**) è un tentativo di standardizzazione di processo di sviluppo di sistemi orientati agli oggetti basato sull’uso di UML.

## Diagrammi UML

![[Pasted image 20251124053143.png]]
## Formalismi UML

I **nove** formalismi di base dello UML sono:
1. **Use case diagram**: evidenziano la modalità (caso d’uso) con cui gli utenti (attori) utilizzano il sistema. Possono essere usati come supporto per la definizione dei requisiti utente.
2. **Class diagram**: consentono di rappresentare le classi con le relative proprietà (attributi, operazioni) e le associazioni che le legano.
3. **State diagram**: rappresentano il comportamento dinamico dei singoli oggetti di una classe in termini di stati possibili e transizioni di stato per effetto di eventi.
4. **Activity diagram**: sono particolari state diagram, in cui gli stati rappresentati rappresentano azioni in corso di esecuzione. Sono particolarmente indicati per la produzione di modelli di work-flow.
5. **Sequence diagram**: evidenziano le interazioni (messaggi) che oggetti di classi diverse si scambiano nell’ambito di un determinato caso d’uso, ordinate in sequenza temporale. A differenza dei diagrammi di collaborazione, non evidenziano le relazioni tra oggetti.
6. **Collaboration diagram**: descrivono le interazioni (messaggi) tra oggetti diversi, evidenziando le relazioni esistenti tra le singole istanze.
7. **Object diagram**: permettono di rappresentare gli oggetti e le relazioni tra essi nell’ambito di un determinato caso d’uso.
8. **Component diagram**: evidenziano la strutturazione e le dipendenze esistenti tra componenti software.
9. **Deployment diagram**: evidenziano le configurazioni dei nodi elaborativi di un sistema real- time ed i componenti, processi ed oggetti assegnati a tali nodi.
# Primo Step: Il Modello dei Dati

Rappresenta da un punto di vista statico e strutturale, l'organizzazione logica dei dati da elaborare. Le strutture dati sono definite mediante lo stato degli oggetti, che viene determinato dal valore assegnato ad attributi e associazioni. Il modello dei dati viene specificato mediante il formalismo dei class diagram che permette di definire:

- Classi.
- Attributi di ciascuna classe.
- Operazioni di ciascuna classe.
- Associazioni tra classi.

È di fondamentale importanza, visto che, secondo l'approccio ad oggetti, un sistema software è costituito da un insieme di oggetti (classificati) che collaborano.

Il modello viene costruito in modo iterativo ed incrementale. Si tratta di un processo creativo, in cui giocano un ruolo importante sia l'esperienza dell'analista che la comprensione del dominio applicativo. 

Durante la fase iniziale di costruzione del modello dei dati occorre concentrarsi sulle cosiddette **entity classes**, ovvero quelle classi che definiscono il dominio applicativo e che sono rilevanti per il sistema.

Le **control classes** (che gestiscono la “logica” del sistema) e **boundary classes** (che rappresentano l'interfaccia utente) vengono introdotte successivamente, usando le informazioni del modello comportamentale. 

Le operazioni di ciascuna classe vengono identificate a partire dal modello comportamentale, per cui vengono inizialmente trascurate.
## Approcci per l'Identificazione delle Classi

### Approccio Noun Phrase

È l'approccio più usato. Una **noun phrase** è una frase in cui il sostantivo ha una prevalenza sulla parte verbale (sono frasi di tipo assertivo). I sostantivi delle frasi nominali usate per la stesura dei
requisiti utente sono considerati **candidate classes**. La lista delle candidate classes viene suddivisa in tre gruppi:

- **Irrelevant** (non appartengono al dominio applicativo e quindi possono essere scartate).
- **Relevant** (evidenziano caratteristiche di entity classes).
- **Fuzzy** (non si hanno sufficienti informazioni per classificarle come relevant o irrelevant, vanno analizzate successivamente).

Si assume che l'insieme dei requisiti utente sia completo e corretto.
### Approccio Common Class Patterns

Basato sulla teoria della classificazione. Le candidate classes vengono identificate a partire da
gruppi (pattern) di classi predefinite:
- **Concept** (es. Reservation)
- **Events** (es. Arrival)
- **Organization** (es. AirCompany)
- **People** (es. Passenger)
- **Places** (es. TravelOffice)

Non è un approccio sistematico, ma può rappresentare una utile guida. A differenza dell'approccio noun phrase, non si concentra sul documento dei requisiti utente. Può causare **problemi di interpretazione** dei nomi delle classi.

### Approccio Use Case Driven

Si assume che:
- Siano già stati sviluppati gli use case diagram ( e possibilmente anche i sequence diagram più significativi).
- Per ogni use case sia fornita una descrizione testuale dello scenario di funzionamento.

Simile all'approccio noun phrase (si considera l'insieme degli use case come insieme dei requisiti utente). Si assume che l'insieme degli use case sia completo e corretto. Approccio function-driven (o problem-driven secondo la terminologia object oriented).
### Approccio CRC

L'approccio **CRC** (**Class** - **Responsibility** – **Collaborators**) è basato su riunioni in cui si fa uso di apposite card. Ciascuna card rappresenta una classe, e contiene tre compartimenti, che identificano:

- Il nome della classe
- Le responsabilità assegnate alla classe
- Il nome di altre classi che collaborano con la classe.

Le classi vengono identificate analizzando come gli oggetti collaborano per svolgere le funzioni di sistema.

Approccio utile per:
- Verifica di classi identificate con altri metodi.
- Identificazione di attributi e operazioni di ciascuna classe.

Esempio di card:
![[Pasted image 20251124061937.png]]
### Approccio Mixed

È un mix di elementi presenti in ciascuno degli approcci precedenti. 

**Esempio**:
1. L'insieme iniziale delle classi viene identificato in base all'esperienza dell'analista, facendosi eventualmente guidare dall'approccio common class patterns.
2. Altre classi possono essere aggiunte usando sia l'approccio noun phrase che l'approccio use case driven (se gli use case diagram sono disponibili).
3. Infine l'approccio **CRC** può essere usato per verificare l'insieme delle classi identificate.

## Linee guida per l'identificazione delle Entity Classes

1. Ogni classe deve avere un ben preciso **statement of purpose**.
2. Ogni classe deve prevedere un **insieme di istanze** (oggetti) – le cosiddette singleton classes (per la quali si prevede una singola istanza) non sono di norma classificabili come entity classes.
3. Ogni classe deve prevedere un **insieme di attributi** (non un singolo attributo).
4. Distinguere tra elementi che possono essere modellati come classi o come attributi.
5. Ogni classe deve prevedere un **insieme di operazioni** (anche se inizialmente le operazioni vengono trascurate, i servizi che la classe mette a disposizione sono implicitamente derivabili dallo statement of purpose).

# Casi di studio

Da: MACIASZEK, L.A. (2001): Requirements Analysis and System Design. Developing Information Systems with UML, Addison Wesley.

## University Enrollment
### Problem statement

L'università offre
  - Corsi di laurea triennali e magistrali
  - A studenti full-time e part-time

La struttura universitaria
  - Dipartimenti raggruppati in facoltà
  - Ogni corso di laurea è amministrato da una singola facoltà
  - Il percorso di laurea può includere insegnamenti di altre facoltà

Sistema di iscrizione universitaria
  - Percorsi di studio personalizzati
  - Corsi propedeutici
  - Corsi obbligatori
  - Restrizioni varie

Problemi di sovrapposizione oraria
Numero massimo di studenti per classe, ecc.

Il sistema deve
  - Supportare le attività di pre-iscrizione
  - Gestire le procedure di iscrizione

Attività di pre-iscrizione
  - Invio per posta di:
    • I voti degli esami del semestre precedente agli studenti
    • Le istruzioni per l'iscrizione

Durante l'iscrizione
  - Accettare i piani di studio proposti dagli studenti
  - Verificare i requisiti propedeutici, le sovrapposizioni orarie, le dimensioni delle classi, le approvazioni speciali, ecc.

La risoluzione di alcuni problemi potrebbe richiedere
  la consultazione con tutor accademici o docenti responsabili dei corsi

### Esempio A.1

Il primo step consiste nel leggere i requisiti e trovare le classi candidate:

- Ogni laurea comprende un numero di corsi obbligatori e un numero di corsi a scelta.
- Ogni corso è di un determinato livello e ha un valore in crediti formativi
- Un corso può far parte di un numero qualsiasi di corsi di laurea
- Ogni laurea specifica il valore minimo totale di crediti formativi richiesto per il conseguimento del titolo
- Gli studenti possono combinare i corsi offerti in piani di studio adatti alle loro esigenze individuali e finalizzati al conseguimento della laurea per cui sono iscritti

| Relevant     | Fuzzy              |
| ------------ | ------------------ |
| Laurea       | Corso Obbligatorio |
| Corso        | Corso a Scelta     |
| Studente     | Piano di Studio    |
| Insegnamenti |                    |
### Esempio A.2

La seconda interazione si costruisce in maniera interattiva da A.1

Considera i seguenti requisiti aggiuntivi tratti dal Documento dei Requisiti:

- La scelta degli insegnamenti da parte di uno studente può essere limitata da sovrapposizioni di orario e da restrizioni sul numero di studenti che possono iscriversi all'offerta formativa corrente del corso.
- Il piano di studio proposto dallo studente viene inserito nel sistema di iscrizione online
- Il sistema verifica la coerenza del piano e segnala eventuali problemi
- I problemi devono essere risolti con l'aiuto di un tutor accademico
- Il piano di studio definitivo è soggetto all'approvazione accademica da parte del delegato del Capo Dipartimento e viene quindi inoltrato all'Ufficio della Segreteria Studenti
![[Pasted image 20251124201145.png]]
![[Pasted image 20251124201241.png]]

### Esempio A.3

Fai riferimento agli esempi A.1 e A.2 e considera i seguenti requisiti aggiuntivi:
- La carriera accademica dello studente deve essere disponibile su richiesta
- La carriera deve includere informazioni sui voti dello studente in ogni insegnamento a cui si è iscritto (e da cui non si è ritirato senza penalità)
- Ogni insegnamento ha un docente responsabile, ma altri docenti aggiuntivi possono insegnare in esso
- Potrebbe esserci un docente responsabile diverso per un insegnamento ogni semestre
- Potrebbero esserci docenti diversi per ogni insegnamento ogni semestre

![[Pasted image 20251125163349.png]]
### Esempio A.4

Mostra un diagramma degli oggetti con alcuni oggetti che rappresentano le classi dell'Esempio A.3.

![[Pasted image 20251125164526.png]]
### Esempio A.5

![[Pasted image 20251125180225.png]]
## Video Store

### Problem Statement

Il negozio di video noleggio
- Noleggio di videocassette e dischi ai clienti
- Tutte le videocassette e i dischi sono dotati di codice a barre
- Anche la tessera di membership del cliente avrà un codice a barre

I clienti esistenti possono prenotare video da ritirare in una data specifica

Gestione delle richieste dei clienti, comprese le richieste su film che il negozio non ha in stock (ma che può eventualmente ordinare su richiesta)

### Esempio B.1

Considera i seguenti requisiti per il sistema del Videonoleggio e identifica le classi candidate:

- Il videonoleggio mantiene in magazzino un'ampia libreria di titoli cinematografici attuali e popolari. Un determinato film può essere disponibile su videocassetta o disco. Ulteriori requisiti:
- Le videocassette sono disponibili in formato "Beta" o "VHS"
- I dischi video sono in formato DVD
- Ogni film ha un periodo di noleggio specifico (espresso in giorni), con un costo di noleggio associato a quel periodo
- Il videonoleggio deve essere in grado di rispondere immediatamente a qualsiasi richiesta sulla disponibilità in magazzino di un film e su quanti nastri e/o dischi sono disponibili per il noleggio
- Lo stato di conservazione di ogni videocassetta e disco deve essere conosciuto e registrato

| Relevant classes  | Fuzzy classes      |
| ----------------- | ------------------ |
| TitoloFilm        | CondizioniNoleggio |
| SupportoVideo     |                    |
| Videocassetta     |                    |
| DiscoDVD          |                    |
| VideocassettaBeta |                    |
| VideocassettaVHS  |                    |
### Esempio B.2

I requisiti aggiuntivi sono:
- Il costo del noleggio varia a seconda del supporto video: videocassetta o disco (ma è lo stesso per le due categorie di videocassette: Beta e VHS).
- Il sistema dovrebbe accogliere futuri formati di memorizzazione video, oltre alle videocassette VHS, Beta e ai dischi DVD
- Gli impiegati utilizzano frequentemente un codice del film, anziché il titolo, per identificare il film
- Lo stesso titolo di film può avere più di un'edizione (release) diretta da registi diversi

![[Pasted image 20251124201608.png]]

![[Pasted image 20251124201621.png]]

### Esempio B.3

Fare riferimento agli Esempi B.1 e B.2  
• Le classi identificate nell'Esempio 4.5 implicano una gerarchia di generalizzazione radicata nella classe SupportoVideo  
• Estendere il modello per includere le relazioni tra le classi e specificare le relazioni di generalizzazione  
• Si assuma che il Noleggio Video debba sapere se una Videocassetta è nuova di zecca o se è già stata registrata (ciò può essere catturato da un attributo `is_taped_over` - `è_riscritta`)  
• Si assuma inoltre che la capacità di archiviazione di un DiscoVideo consenta di contenere più versioni dello stesso film, ciascuna in una lingua diversa o con finali differenti

![[Pasted image 20251125164612.png]]

### Esempio B.4
![[Pasted image 20251125180358.png]]

![[Pasted image 20251125180426.png]]
![[Pasted image 20251125180452.png]]

![[Pasted image 20251125180513.png]]
### Esempio B.5

![[Pasted image 20251126145706.png]]

È un automa a stati finiti in pratica:
- Pallina piena: inizio
- Pallina dentro cerchio: fine

### Esempio B.6

![[Pasted image 20251126134214.png]]
## Contact Management
### Problem Statement

L'azienda di ricerche di mercato possiede una base clienti consolidata composta da organizzazioni che acquistano report di analisi di mercato  

L'azienda è costantemente alla ricerca di nuovi clienti  

Sistema di gestione dei contatti  
	– Clienti potenziali  
	– Clienti attuali  
	– Ex clienti  
Il nuovo sistema di gestione dei contatti verrà sviluppato internamente e sarà disponibile per tutti i dipendenti dell'azienda, ma con diversi livelli di accesso  
	– I dipendenti del Dipartimento Servizi Clienti avranno la responsabilità diretta del sistema  

Il sistema dovrà permettere una pianificazione flessibile e una riprogrammazione delle attività relative ai contatti, in modo che i dipendenti possano collaborare efficacemente per acquisire nuovi clienti e coltivare le relazioni esistenti

### Esempio C.1

Considera i seguenti requisiti per il sistema di Gestione dei Contatti e identifica le classi candidate:

- "Mantenere i contatti" con la base clienti attuale e potenziale
- Memorizzare i nomi, i numeri di telefono, gli indirizzi postali e corrieri, ecc. delle organizzazioni e delle persone di riferimento in queste organizzazioni
- Pianificare compiti ed eventi per i dipendenti in relazione alle persone di riferimento pertinenti
- I dipendenti possono pianificare compiti ed eventi per altri dipendenti o per se stessi
- Un compito è un gruppo di eventi che si svolgono per raggiungere un risultato (ad esempio, risolvere un problema del cliente)
- I tipi tipici di eventi sono: telefonata, visita, invio fax, organizzazione di formazione, ecc.

| Relevant classes | Fuzzy classes            |
| ---------------- | ------------------------ |
| Organizzazione   | OrganizzazioneAttuale    |
| Contatto         | OrganizzazionePotenziale |
| Dipendente       | IndirizzoPostale         |
| Compito          | IndirizzoCorriere        |
| Evento           |                          |
### Esempio C.2
Considera le seguenti informazioni aggiuntive:

- Un cliente è considerato attuale se esiste un contratto in essere con quel cliente per la fornitura dei nostri prodotti o servizi. La gestione dei contratti è, tuttavia, al di fuori dello scopo del nostro sistema.
- Report sui contatti basati sugli indirizzi postali e di corriere (ad esempio, trovare tutti i clienti per codice postale)
- La data e l'ora di creazione del compito vengono registrate
- Il "valore monetario" di un compito può essere memorizzato
- Gli eventi per il dipendente vengono visualizzati sullo schermo del dipendente in pagine simili a un calendario (una pagina per giorno).
- La priorità di ogni evento (bassa, media o alta) è distinta visivamente sullo schermo
- Non tutti gli eventi hanno un "orario di scadenza" - alcuni sono "senza orario"
- L'orario di creazione dell'evento non può essere modificato, ma l'orario di scadenza sì.
- La data e l'ora del completamento dell'evento vengono registrate
- Il sistema memorizza le identificazioni dei dipendenti che hanno creato i compiti e gli eventi, a cui è programmato di svolgere l'evento ("dipendente assegnato"), e che hanno completato l'evento.

![[Pasted image 20251124212656.png]]
![[Pasted image 20251124212714.png]]
### Esempio C.3

Fai riferimento agli esempi C.1 e C.2 e specifica le associazioni
Consideriamo il requisito: Il sistema consente di produrre vari report sui nostri contatti in base agli
indirizzi postali e di corriere.

![[Pasted image 20251125155059.png]]

#### Soluzione 1
![[Pasted image 20251125155116.png]]
#### Soluzione 2

![[Pasted image 20251125155413.png]]
### Esempio C.4

![[Pasted image 20251125180321.png]]
## Telemarketing

### Problem Statement

L'**associazione di beneficenza** vende biglietti della lotteria per raccogliere fondi.
- **Campagne** a sostegno di cause benefiche attualmente rilevanti
- Ex contribuenti (**sostenitori**) vengono contattati tramite telemarketing e/o invii postali diretti

**Programmi di ricompensa (campagne bonus speciali)**
- Per acquisti all'ingrosso
- Per attirare nuovi sostenitori

**Metodologia di contatto**
- L'associazione non contatta potenziali sostenitori in modo casuale utilizzando elenchi telefonici o metodi simili

**Applicazione di telemarketing**
- Supporto fino a cinquanta telemarketer che lavorano simultaneamente
- Pianificazione delle chiamate telefoniche in base a priorità predefinite e altri vincoli noti
- Effettuare automaticamente le chiamate programmate
- Ripianificazione delle connessioni non riuscite
- Organizzazione di richiamate per i sostenitori
- Registrazione degli esiti delle conversazioni, inclusi gli ordini di biglietti e qualsiasi modifica ai record dei sostenitori

### Esempio D.1

Considera la seguente descrizione testuale dei casi d'uso del sistema di Telemarketing e identifica le classi candidate:

- L'operatore di telemarketing richiede al sistema di programmare e comporre la chiamata telefonica a un sostenitore
- Una volta stabilita la connessione, l'operatore offre i biglietti della lotteria al sostenitore. Durante la conversazione, l'operatore potrebbe aver bisogno di accedere e modificare sia i dettagli della campagna che quelli del sostenitore (operazioni CRUD: creare - leggere - aggiornare - eliminare)
- Infine, l'operatore registra l'esito della conversazione, ovvero i risultati riusciti o non riusciti dell'azione di telemarketing

![[Pasted image 20251124200345.png]]
#### Business Use Case Diagram

![[Pasted image 20251124200304.png]]

### Esempio D.2

Considera le seguenti informazioni aggiuntive:
Ogni campagna:
  • Ha un titolo che viene generalmente utilizzato per riferirsi ad essa
  • Ha anche un codice univoco per riferimento interno
  • Si svolge in un periodo di tempo fissato
- Poco dopo la chiusura della campagna, i premi vengono estratti e i possessori dei biglietti vincenti vengono avvisati.

Ulteriori requisiti:
- I biglietti sono numerati in modo univoco all'interno di ogni campagna
- Il numero totale di biglietti in una campagna, il numero di biglietti venduti finora e lo stato corrente di ogni biglietto sono noti (ad esempio: disponibile, ordinato, pagato, vincitore di un premio)
- Per determinare la performance degli operatori di telemarketing dell'associazione, la durata delle chiamate e gli esiti positivi delle chiamate (cioè quelli che si traducono in biglietti ordinati) vengono registrati
- Vengono mantenute informazioni estese sui sostenitori
  • Dettagli di contatto (indirizzo, numero di telefono, ecc.)
  • Dettagli storici come le date del primo e più recente coinvolgimento del sostenitore in una campagna
  • Eventuali preferenze e vincoli noti del sostenitore (ad esempio, orari in cui non chiamare, numero di carta di credito abituale)
- Le chiamate di telemarketing vengono effettuate in base alla loro priorità
- Le chiamate a cui non si risponde o in cui viene trovata una segreteria telefonica vengono ripianificate
  • Gli orari delle chiamate ripetute vengono alternati
  • Il numero di chiamate ripetute è limitato
- I limiti possono essere diversi per diversi tipi di chiamata (ad esempio, una normale chiamata di "sollecitazione" potrebbe avere un limite diverso rispetto a una chiamata per ricordare a un sostenitore un pagamento in sospeso)
- Gli esiti delle chiamate sono categorizzati: successo (cioè biglietti ordinati), nessun successo, richiamare più tardi, nessuna risposta, occupato, segreteria telefonica, apparecchio fax, numero errato, numero disattivato.

![[Pasted image 20251124215811.png]]
![[Pasted image 20251124215823.png]]

### Esempio D.3
![[Pasted image 20251125180743.png]]
## Linee Guida per la Specifica delle Classi

**Nomi di classe**:
- Associare ad ogni classe un nome significativo nello specifico dominio applicativo.
- Adottare uno standard per assegnare i nomi alle classi, ad esempio: nome singolare, parole multiple devono essere congiunte, con l'iniziale di ciascuna parola in carattere maiuscolo (es. PostalAddress).
- Definire una lunghezza massima per i nomi delle classi.

**Attributi e operazioni**:
- Considerare inizialmente solo attributi che caratterizzano possibili stati di interesse per gli oggetti.
- Adottare una convenzione standard per assegnare nomi agli attributi, ad esempio: le parole devono essere scritte in carattere minuscolo, separate da un carattere di underscore (es. street_name).
- Ritardare l'aggiunta di operazioni fino al momento in cui sia disponibile il modello comportamentale, da cui vanno derivate.

# Identificazione delle Associazioni

Ogni attributo di tipo non primitivo identificato con le classi dovrebbe essere modellato come un’associazione alla classe che rappresenta quel tipo di dato.

Le associazioni ternarie vanno sostituite con un ciclo di associazioni binarie per evitare problemi di interpretazione.

Nei cicli di associazioni almeno un’associazione potrebbe essere eliminata e gestita come
associazione derivata, anche se per problemi di efficienza spesso si introducono associazioni
ridondanti.

# Specifica delle Associazioni

1. I **nomi delle associazioni** vengono assegnati usando la stessa convenzione usata per gli attributi (le parole devono essere scritte in carattere minuscolo, separate da un carattere di underscore).
2. Assegnare **nomi di ruolo** (**rolename**) alle estremità dell’associazione. I rolename sono i nomi degli attributi nella classe all’estremità opposta dell’associazione.
3. Determinare la molteplicità delle associazioni ad entrambe le estremità.
# Aggregazione

Rappresenta una relazione di tipo **whole-part** (di **contenimento tra oggetti**) tra una classe composta (**superset class**) che contiene una o più classi componenti (**subset classes**).

Può assumere quattro differenti significati:
1. **ExclusiveOwns**: es. Libro ha Capitolo o Capitolo è parte di Libro 
	- **Existence-Dependency**: l'esistenza dei componenti dipende dall'esistenza del contenitore. Distruggere una superset class cancella le sue subset classes.
	- **Transitivity**: Se B contiene C e A contiene B allora A contiene C.
	- **Asymmetricity**: Se A contiene B allora B non può contenere A.
	- **Fixed Property**: Un istanza di B può essere contenuto in una sola istanza di A in maniera esclusiva.
2. **Owns**: es. Macchina ha Ruota
	- Non ha la **Fixed Property**: la ruota di una macchina può essere staccato da un auto e attaccato ad un altro.
3. **Has**: es. Divisione ha Dipartimento
	• Non ha la **Existence-Dependency**.
	• Non ha la **Fixed Property**.
4. **Member** es. Meeting ha Presidente
	• Non ha proprietà speciali apparte l'appartenenza.

Con UML possiamo specificare solo 2 relazioni di contenimento che sono:

1. **Aggregation**: 
	- Corrisponde a **Has** e **Member**, indica un contenimento debole.
	- Indicato col rombo vuoto.
2. **Composition**:
	 - Corrisponde a **ExclusiveOwns** e **Owns**, indica un contenimento forte.
	 - Indicato col rombo pieno.

Quale delle due usare dipende dalla proprietà di **Existence-dependency**, se sì si usa **Composition**, altrimenti **Aggregation**.

# Ereditarietà - Generalization

Serve a rappresentare la condivisione di **attributi ed operazioni** tra classi. Le caratteristiche comuni sono modellate in una classe più **generica** (**superclasse**). Essa viene **specializzata** in **sottoclassi** che **ereditano** attributi ed operazioni della superclasse.

Caratteristiche:
1. **Sostituibilità**: un oggetto della sottoclasse è un valore legale per una variabile avente come tipo la superclasse (es. una variabile di tipo `Frutta` può avere un oggetto di tipo `Mela` come suo valore)
2. **Polimorfismo**: un operazione può avere differenti implementazioni nelle sottoclassi

È usato quanto in un documento dei requisiti leggiamo frasi come:
1. **can-be**: es. `Student` can be a `TeachingAssistant`.
2. **is-a-kind-of**: `TeachingAssistant` is a kind of `Student`

Supporta ad **ereditarietà multipla**, es. `TeachingAssistant` is also a kind of `Teacher`. È rappresentato in UML con una linea, che collega la sottoclasse con la superclasse, avente
una freccia diretta verso la superclasse.

# Object Diagram

È la rappresentazione grafica di istanze di classi. Sono usati per
1. Modellare **relazioni complesse** tra classi a scopo esemplificativo.
2. Mostrare le **modifiche ai singoli oggetti** durante l’evoluzione del sistema.
3. Illustrare la **collaborazione tra oggetti** durante l’evoluzione del sistema

# Secondo Step: Modello Comportamentale

Rappresenta gli aspetti funzionali del sistema da un **punto di vista operativo**, evidenziando come gli oggetti collaborano ed interagiscono al fine di offrire i servizi che il sistema mette a disposizione.

Fa uso di vari formalismi:
1. **Use case diagram**:per descrivere scenari di funzionamento.
2. **Activity diagram**: per descrivere il flusso di elaborazione.
3. **Sequence diagram**: per descrivere l'interazione tra gli oggetti.
4. **Collaboration diagram**: per descrivere l'interazione tra gli oggetti.

Viene costruito in modo **iterativo** ed **incrementale**, usando il modello dei dati, che a sua volta fa uso del modello comportamentale per identificare **operazioni** e **classi aggiuntive** come:
1. **Control classes**: che si occupano della logica del software.
2. **Boundary classes**: che si occupano dell'interfaccia utente.

## Use Case Diagram

È la rappresentazione grafica di attori, casi d'uso e relazioni. Può essere sviluppato con **differenti livelli di astrazione** sia in fase di OOA che OOD. Durante la fase di OOA, si concentra su **COSA** il sistema deve fare (**scenari di funzionamento**).

Un caso d'uso rappresenta:
1. una funzionalità completa (flusso principale, sottoflussi e alternative)
2. una funzionalità visibile dall'esterno
3. un comportamento ortogonale (ogni use case viene eseguito in modo indipendente dagli altri)
4. una funzionalità originata da un attore del sistema (una volta originato, il caso d'uso può interagire con altri attori)
5. una funzionalità che produce un risultato significativo per un attore.

### Identificazione dei Casi d'Uso

Si parte da:
- L'insieme dei requisiti utente
- Gli attori del sistema (insieme ai relativi obiettivi)

Domande utili:
- Quali sono i compiti principali svolti da ciascun attore?
- Un attore accede o modifica l’informazione nel sistema?
- L'attore rappresenta il tramite mediante cui il sistema viene informato di modifiche apportate in altri sistemi?
- L'attore deve essere informato di eventuali cambiamenti avvenuti nel sistema?

Durante la fase di OOA, i casi d'uso identificano le **necessità degli attori** del sistema.

### Specifica di Use Case Diagram

Si possono rappresentare quattro tipi di relazioni:
1. **Associazione**: lega attori e caso d'uso, se attiva il caso d'uso o è coinvolto nel caso d'uso. Per ogni caso d'uso deve esistere almeno un attore che lo attiva.
2. **Include**: identificato dallo stereotype: «include», lega casi d'uso ad altri casi d'uso. Un caso d'uso included è sempre attivato per completare il caso d'uso che lo include.
3. **Extend**: identificato dallo stereotype : «extend», lega casi d'uso ad altri casi d'uso. Un caso d'uso extended può attivare il caso d'uso dal quale viene esteso ma tale attivazione non è necessaria per completare il caso d’uso extended.
4. **Generalizzazione**: tra gli attori può esistere la stessa ereditarietà che esiste tra classi.

Fare riferimento ad esempio A.5

## Activity Diagram

Rappresenta a vari livelli di astrazione il **flusso di esecuzione**, che sia sequenziale o concorrente, in una applicazione object-oriented.

Variante degli **state diagram**, in cui gli stati rappresentano l’esecuzione di azioni e le transizioni sono attivate dal completamento di tali azioni.

Usato principalmente in fase di OOD per rappresentare il flusso di esecuzione delle operazioni definite nel class diagram.

In fase di OOA, viene usato per rappresentare il flusso delle attività nell'esecuzione di un caso d’uso (un caso d’uso può essere associato ad uno o più activity diagram).

Poichè non vengono mostrati gli oggetti che eseguono le attività, può essere costruito anche in **assenza** del class diagram.

In presenza del class diagram, ogni **attività** può essere associata ad **una o più operazioni** appartenenti ad una o più classi.

### Specifica di Activity Diagram

Un evento (esterno) che origina un caso d’uso viene modellato come un evento che causa l’esecuzione di un activity diagram

Gli **action state** vengono **identificati** a partire dalla descrizione testuale dello scenario di funzionamento di un caso d’uso, ed associati mediante **transition lines** (che possono essere controllate da **guard conditions**)

Un action state viene completato quando la sua elaborazione termina, si percorre poi una delle trasizioni in uscita per procedere all'action state successivo.

**Flussi concorrenti** vengono modellati con barre di sincronizzazione (barre fork-join).

**Flussi alternativi** vengono modellati con nodi decisionali (branch/merge diamonds)

Eventi esterni non sono generalmente modellati

## Diagrammi di Interazione

**Sequence Diagram**: descrive lo scambio di messaggi tra oggetti in ordine temporale. Viene usato principalmente in fase di OOA.

**Collaboration Diagram**: descrive lo scambio di messaggi tra oggetti mediante relazioni tra gli oggetti stessi. Usato principalmente in fase di OOD.

Permettono di identificare le operazioni delle classi nel class diagram, sono
rappresentazioni equivalenti e possono essere generati in modo automatico l’uno dall’altro.

### Specifica di Sequence Diagram

Le **attività** dell’activity diagram vengono mappate come **messaggi** (di tipo “richiesta esecuzione attività”) in un sequence diagram.

Un messaggio può rappresentare:
- Un **Signal** che denota una chiamata di tipo asincrono, l’oggetto mittente continua l’esecuzione dopo aver inviato il messaggio asincrono.
- Una **call**: che denota una chiamata di tipo sincrono, ovvero l'oggetto mittente blocca l’esecuzione dopo aver inviato il messaggio, in attesa della risposta da parte dell’oggetto destinatario (che può o meno contenere valori di ritorno).

### Notazione per Sequence Diagram

# Interfaccia Pubblica di Classe
# Identificazione delle Operazioni


# Modello Dinamico

Rappresentano il comportamento dinamico degli oggetti di una singola classe, in termini di stati possibili, eventi e condizioni che originano transizioni di stato (assieme alle eventuali azioni da svolgere a seguito dell’evento verificatosi). Fa uso degli **State Diagrams**.

![[Pasted image 20251126133956.png]]

Viene costruito per ogni **classe di controllo** per le quali è interessante descrivere il comportamento dinamico.

Viene usato principalmente per applicazioni scientifiche e real-time (meno frequentemente nello sviluppo di applicazioni gestionali).

Vedi esempio B.5
# Gestione della Complessità nei Modelli di OOA

Durante l'OOA nei sistemi software di grandi dimensioni va gestita in modo opportuno la complessità dei modelli. In quanto i cammini delle **reti d'interconnessione** tra classi nel modello dei dati crescono in modo esponenziale all'aumentare delle classi

Le **gerarchie di classi** permettono di ridurre la complessità da esponenziale a polinomiale, grazie
all'introduzione di opportuni **strati di classi** che vincolano la comunicazione tra classi appartenenti allo stesso strato o a strati adiacenti.

## Esempio: Class Diagram non Stratificato

$\frac{n(n-1)}{2}$ possibili connessioni tra $n$ classi.

![[Pasted image 20251126132548.png]]

## Esempio: Class Diagram Stratificato
![[Pasted image 20251126132719.png]]
# UML Package

In UML un **package** rappresenta un gruppo di classi o di altri elementi (ad esempio casi
d'uso). Essi possono essere **annidati** (il package esterno ha accesso ad ogni classe contenuta nei package in esso annidati)

Una classe può **appartenere** ad un solo package, ma può comunicare con classi appartenenti ad altri package.

La comunicazione tra classi appartenenti a package differenti viene controllata mediante dichiarazione di **visibilità** (private, protected, o public) delle classi all'interno dei package
## Package Diagram

In UML non esiste il concetto di **package diagram**. I package possono essere creati all'interno di:
- Class diagram.
- Use case diagram.

Si possono specificare due tipi di relazioni tra package:
1. **Generalization**: che implica anche dependency.
2. **Dependency**: che si divide in: 
	-  Usage dependency
	- Access dependency
	- Visibility dependency
## Approccio BCE

**Boundary package - B**: Descrivono le classi i cui oggetti gestiscono l'interfaccia tra un attore ed il sistema. Le classi catturano una porzione dello stato del sistema e la presentano all'utente in forma visuale.

**Control package - C**: Descrivono le classi i cui oggetti intercettano l'input dell'utente e controllano l'esecuzione di uno scenario di funzionamento del sistema. Le classi rappresentano azioni ed attività di uno use case.

**Entity package - E**: Descrivono classi i cui oggetti gestiscono l'accesso alle entità fondamentali del sistema. –Le classi corrispondono alle strutture dati gestite dal sistema

### Gerarchia dei Package BCE

![[Pasted image 20251126131434.png]]

# Esercizi