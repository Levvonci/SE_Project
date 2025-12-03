La **fase OOD** (Object-Oriented Design) consiste nelle seguenti due sotto-fasi:

*   **OOD preliminare** (o architetturale, o di sistema): definisce la strategia complessiva per costruire una soluzione che risolva il problema specificato nella fase OOA (Object-Oriented Analysis). Vengono prese decisioni che riguardano l'organizzazione generale del software (architettura del sistema).
*   **OOD dettagliato** (o degli oggetti): fornisce la definizione completa delle classi e delle associazioni da implementare, nonché le strutture dati e l'algoritmo dei metodi che implementano le operazioni delle classi.
*   Secondo un approccio di sviluppo **iterativo e incrementale**, il modello OOA viene **"trasformato"** nel modello OOD, il quale aggiunge i dettagli tecnici della soluzione hardware/software che definisce **come** il software deve essere implementato.

# Architettura di sistema

Un'**architettura di sistema** definisce la struttura dei componenti del sistema software, insieme alle relazioni tra tali componenti e ai principi che guidano la progettazione e l'evoluzione del sistema.

**Evoluzione delle architetture di sistema:**
    1. Architetture basate su **mainframe**.
    2. Architetture di **condivisione file**.
    3. Architetture **client/server (C/S)**:
        3.1 a **due livelli** (thin client, fat client)
        3.2 a **tre livelli** (livello superiore, livello intermedio, livello inferiore)
    4. Architetture a **oggetti distribuiti**.
    5. Architetture **basate su componenti**.
    6. Architetture **orientate ai servizi**.

Le architetture dalla 3 alla 6 sono denominate **architetture distribuite**, o architetture di sistemi software distribuiti.

# Sistemi software distribuiti

- L'elaborazione di un sistema software distribuito è **distribuita** su un insieme di **host di esecuzione indipendenti**, connessi da un'infrastruttura di rete (di tipo locale o geografico).
- L'insieme degli host di esecuzione indipendenti è visto dagli utenti come un **singolo host di esecuzione**.
- La tecnologia **middleware** ha svolto un ruolo essenziale nella transizione dalle architetture centralizzate a quelle distribuite.
- Il middleware si riferisce allo **strato software** che fornisce la connettività.
    - Tale strato si colloca **tra il livello applicativo e quello del sistema operativo** e fornisce un insieme di servizi per stabilire l'interazione richiesta tra i vari processi applicativi eseguiti da host in rete (ad es., TP monitor, RPC, MOM, ORB).

## Esempio di sistema software distribuito

**Sistema di controllo del traffico**: composto da più processi che vengono eseguiti su diversi processori (potrebbero essere eseguiti anche su un singolo processore – è l'insieme dei processi separati che rende distribuito un sistema software

![[Pasted image 20251202204312.png]]

## Caratteristiche principali dei sistemi distribuiti

*   **Condivisione di dati e risorse**
*   **Apertura** (capacità di gestire risorse eterogenee)
*   **Concorrenza**
*   **Scalabilità**
*   **Bilanciamento del carico**
*   **Tolleranza ai guasti**
*   **Trasparenza**
*   **Adattabilità agli scenari di enterprise computing**

**Fattori critici**
*   **Qualità del servizio** (prestazioni, affidabilità, ecc.)
*   **Interoperabilità**
*   **Sicurezza**

## Architetture Client/Server (C/S)

* Ogni processo svolge il ruolo di **client** o di **server**.
* Il processo **client** interagisce con l'utente nel modo seguente:
	* Fornisce l'**interfaccia utente** per raccogliere le richieste dell'utente.
    * Inoltra le richieste ai server, utilizzando la tecnologia middleware.
    * Visualizza le risposte del server all'utente attraverso l'interfaccia utente.
* Il processo **server** (o l'insieme di processi eseguiti da un determinato host) fornisce servizi ai client, come segue:
    *   Risponde alle richieste dei client (non è il server ad avviare la conversazione con il client).
    *   Nasconde la complessità dell'intero sistema C/S all'utente (un determinato server può a sua volta agire come client che inoltra la richiesta iniziale a un server secondario, senza rendere il client e l'utente consapevoli della catena di inoltro).

* Un'architettura C/S **partiziona** le applicazioni software in termini di un insieme di processi separati, ciascuno dei quali agisce come client, server o entrambi.

![[Pasted image 20251202204538.png]]

Un'architettura C/S **partiziona** le applicazioni software in un insieme di processi separati che vengono eseguiti sullo stesso host (processore) o su un gruppo di host in rete.

![[Pasted image 20251203104309.png]]
# Livelli dell'applicazione

**Livello di presentazione**  
  Si occupa di raccogliere gli input degli utenti e presentare i risultati di un'elaborazione agli utenti del sistema.  

**Livello di elaborazione applicativa**: Fornisce funzionalità specifiche dell'applicazione, ad esempio, in un sistema bancario, funzioni come aprire un conto, chiudere un conto, ecc.  

**Livello di gestione dei dati**: Gestisce l'accesso ai dati dell'applicazione.

![[Pasted image 20251203104529.png]]

## Architetture client-server a due livelli

- **Modello thin-client**: tutta l'elaborazione applicativa e la gestione dei dati viene eseguita sul server; il client è semplicemente responsabile dell'esecuzione del software di presentazione.

- **Modello fat-client**: il server è responsabile solo della gestione dei dati; il software sul client implementa la logica applicativa e il software di presentazione.

![[Pasted image 20251203104705.png]]

## Architetture client-server a tre livelli

- Ogni livello dell'architettura applicativa viene eseguito su un processore separato.
- Consente prestazioni migliori rispetto all'approccio **thin-client a due livelli** ed è più semplice da gestire rispetto all'approccio **fat-client a due livelli**.
- Un'architettura più scalabile: con l'aumentare della domanda, è possibile aggiungere server aggiuntivi.

![[Pasted image 20251203104731.png]]
### Esempio

Internet Banking System:

![[Pasted image 20251203104825.png]]

# Architetture a oggetti distribuiti

- Nessuna distinzione tra client e server.
- Ogni oggetto distribuito agisce sia da client (inviando messaggi di richiesta, ovvero invocando metodi) che da server (fornendo messaggi di risposta, ovvero eseguendo il metodo invocato).
- La comunicazione remota tra oggetti viene resa trasparente mediante l'uso di middleware basato sul concetto di *software bus* (indicato come **object request broker**):
  - *Bus astratto*: specifica dell'interfaccia che fornisce servizi di comunicazione e scambio dati (modello di trasferimento del controllo e modello di tipo per i valori scambiati).
  - *Implementazione del bus*: implementazione del bus astratto per una specifica piattaforma hardware/software (separazione tra interfaccia e implementazione).
- Le applicazioni basate su architetture a oggetti distribuiti sono costituite da un insieme di oggetti eseguiti su piattaforme distribuite ed eterogenee, che comunicano tramite invocazione remota di metodi.

![[Pasted image 20251203104932.png]]
## Esempio

![[Pasted image 20251203104959.png]]

# Architetture basate su componenti

- Le architetture basate su componenti definiscono prodotti software assemblati da un insieme di componenti software, progettati per funzionare insieme all'interno di un framework di componenti.
- Un framework di componenti utilizza architetture software generiche per formalizzare classi specifiche di applicazioni.
- I sistemi software basati su componenti supportano lo sviluppo efficiente di sistemi software i cui requisiti presentano livelli significativi di variabilità.
- È quindi necessario identificare e implementare astrazioni software che incapsulino soluzioni efficienti e affidabili a problemi standard di coordinamento e sintesi.
- Queste astrazioni, o "componenti", vengono utilizzate per costruire sistemi più grandi, nascondendo i dettagli implementativi della struttura più piccola.
- Un componente può essere utilizzato in molte applicazioni diverse e può essere riconfigurato quando i requisiti dell'applicazione cambiano.

Un elemento essenziale per costruire sistemi software basati su componenti è il **riuso a scatola chiusa** del software.

- Assemblaggio dei componenti è semplice, poiché ogni componente ha un numero limitato di "connettori" con regole fisse che specificano come può essere collegato ad altri componenti.
- Invece di dover adattare la struttura di un pezzo di software per modificarne le funzionalità, un utente collega il comportamento desiderato ai parametri del componente.

Aspetti importanti dei componenti:
- **Incapsulamento** delle strutture software come componenti astratti (variabilità)
- **Composizione** dei componenti collegando i loro parametri a valori specifici o ad altri componenti (adattabilità)

**Oggetti vs. componenti:**
- Gli oggetti incapsulano servizi, mentre i componenti sono astrazioni (che possono essere utilizzate per costruire sistemi orientati agli oggetti).
- Gli oggetti hanno identità, stato e comportamento, e sono sempre entità in fase di esecuzione; i componenti, invece, sono generalmente entità statiche necessarie durante la costruzione del sistema (e non necessariamente esistono in fase di esecuzione).
- I componenti possono avere granularità più fine o più grossolana rispetto agli oggetti: ad esempio, classi, template, mix-in, moduli; i componenti devono avere un'interfaccia di composizione esplicita, che sia verificabile a livello di tipi.

![[Pasted image 20251203105238.png]]

# Framework di componenti

Un framework di componenti è un'infrastruttura software che fornisce un ambiente standardizzato per lo sviluppo, l'assemblaggio, l'esecuzione e la gestione di applicazioni costruite a partire da componenti software riutilizzabili e intercambiabili. Definisce le regole, le convenzioni e i servizi che governano come i componenti interagiscono e vengono integrati.

![[Pasted image 20251203105343.png]]

# Sviluppo di Framework vs. Sviluppo di Applicazioni

![[Pasted image 20251203110333.png]]

# Componenti UML

Una parte modulare di un sistema che nasconde il proprio contenuto e il cui aspetto è sostituibile all'interno del proprio ambiente.

* Definisce il proprio comportamento in termini di interfacce fornite e richieste, che possono essere collegate tra loro.
* Può essere sostituita, in fase di progettazione o di esecuzione, da un componente che offra funzionalità equivalenti sulla base della compatibilità delle sue interfacce.

![[Pasted image 20251203110913.png]]

What is a Subsystem?

Una parte di un sistema che incapsula un comportamento, espone un insieme di interfacce e contiene altri elementi del modello.

* Modellato come un componente.

# Architettura Orientata ai Servizi (SOA)

* Una SOA è un'architettura software distribuita composta da più servizi autonomi.
* I servizi sono distribuiti in modo da poter essere eseguiti su nodi diversi con fornitori di servizi diversi.
* Con una SOA, l'obiettivo è sviluppare applicazioni software composte da servizi distribuiti, in modo che i singoli servizi possano essere eseguiti su piattaforme diverse e implementati in linguaggi diversi.

## Protocolli SOA

Vengono forniti protocolli standard basati su Internet per consentire ai servizi di comunicare tra loro e scambiare informazioni.

* Ogni servizio possiede una **descrizione del servizio**, che consente alle applicazioni di individuarlo e comunicare con esso.
* La descrizione del servizio definisce il nome del servizio, la sua posizione (URL/endpoint) e i suoi requisiti per lo scambio di dati.

### Fornitori e consumatori di servizi

* Un **fornitore di servizi** supporta servizi utilizzati da molteplici client.
* A differenza delle architetture client/server, le SOA si basano sul concetto di servizi **a basso accoppiamento** che possono essere individuati e collegati dai client (anche detti **consumatori di servizi** o **richiedenti di servizi**) con l'assistenza di **broker di servizi**.

## Concetti di progettazione SOA

* Un obiettivo importante della SOA è progettare i servizi come componenti autonomi e riutilizzabili.
* I servizi sono concepiti per essere autosufficienti e **a basso accoppiamento**, il che significa che le dipendenze tra servizi sono ridotte al minimo.
* Invece di far sì che un servizio dipenda da un altro, vengono forniti **servizi di coordinamento** nelle situazioni in cui è necessario accedere a più servizi e la loro sequenza di accesso deve essere gestita.
* Per le applicazioni orientate ai servizi sono descritti diversi pattern architetturali software:
  * **Pattern di brokeraggio**, inclusi Registrazione del Servizio, Brokeraggio del Servizio e Scoperta del Servizio.
  * **Pattern di transazione**, inclusi Transazione in Due Fasi, Transazione Composta e Transazione di Lunga Durata.
  * e **Pattern di negoziazione**.

## Principi di Progettazione dei Servizi

* **Basso accoppiamento (Loose coupling)**
* **Contratto del servizio (Service contract)**
* **Autonomia (Autonomy)**
* **Astrazione (Abstraction)**
* **Riutilizzabilità (Reusability)**
* **Componibilità (Composability)**
* **Assenza di stato (Statelessness)**
* **Rintracciabilità (Discoverability)**

## Pattern Architetturali Software di Brokeraggio

* In una SOA, i **broker di oggetti** fungono da intermediari tra client e servizi.
* Nel **pattern Broker** (noto anche come pattern *Object Broker* o *Object Request Broker*), il broker agisce da intermediario tra i client e i servizi.
* I servizi si **registrano** presso il broker.
* I client **individuano** i servizi attraverso il broker.
* Dopo che il broker ha **mediato la connessione** tra client e servizio, la comunicazione tra i due può avvenire **direttamente** o **attraverso il broker stesso**.

## Trasparenza

* Il broker fornisce sia **trasparenza di localizzazione** che **trasparenza di piattaforma**.
* La **trasparenza di localizzazione** significa che se un servizio viene spostato in una posizione diversa, i client non se ne accorgono e solo il broker deve essere notificato del cambio.
* La **trasparenza di piattaforma** significa che ogni servizio può essere eseguito su una piattaforma hardware/software diversa e non deve mantenere informazioni sulle piattaforme su cui vengono eseguiti gli altri servizi.

## Comunicazione tramite broker

* Con la comunicazione tramite broker, invece di dover conoscere l'indirizzo di un determinato servizio, il client interroga il broker per trovare i servizi disponibili.
* In primo luogo, il servizio deve **registrarsi presso un broker**, come descritto dal **pattern di Registrazione del Servizio**.

## Pattern di Registrazione del Servizio

* Il servizio deve registrare le proprie informazioni presso il broker, inclusi il nome del servizio, una descrizione del servizio e l'indirizzo (location) in cui è fornito.
* Sequenza dei messaggi:
  1. Il servizio invia una **richiesta di registrazione** al broker.
  2. Il broker registra il servizio nel **registro dei servizi** e invia un **messaggio di conferma di registrazione** al servizio.

![[Pasted image 20251203114920.png]]

## Pattern di Inoltro del Broker (Pagina Bianca)

1. Un client invia un messaggio che identifica il servizio richiesto – ad esempio, per prelevare contanti da una determinata banca.
2. Il broker riceve la richiesta del client, determina la posizione del servizio (l'ID del nodo su cui risiede il servizio) e inoltra il messaggio al servizio in quella specifica posizione.
3. Il messaggio arriva al servizio e il servizio richiesto viene invocato.
4. Il broker riceve la risposta del servizio e la inoltra al client.

![[Pasted image 20251203115024.png]]

## Pattern del Riferimento (Handle) del Broker (Pagina Bianca)

* Il *Broker Handle pattern* mantiene il vantaggio della trasparenza di localizzazione, aggiungendo il beneficio di ridurre il traffico di messaggi.
* Invece di inoltrare ogni messaggio del client al servizio, il broker restituisce al client un **riferimento (handle)** del servizio, che viene poi utilizzato per la comunicazione diretta tra client e servizio.
* Questo pattern è particolarmente utile quando client e servizio sono destinati a instaurare un dialogo e a scambiare diversi messaggi tra loro.

![[Pasted image 20251203115112.png]]

# Pattern di Scoperta del Servizio (Pagina Gialla)

* Nella mediazione a "pagina bianca", il client conosce il servizio richiesto ma non la sua posizione.
* Un pattern di mediazione diverso è quello a **"pagina gialla"**, analogo alle pagine gialle della guida telefonica, in cui il client conosce il *tipo* di servizio richiesto ma non il servizio specifico.
* Noto anche come **Service Discovery pattern** perché consente al client di scoprire nuovi servizi.

**Sequenza:**

1. Il client invia una **richiesta di query** al broker, richiedendo tutti i servizi di un determinato tipo.
2. Il broker risponde con un **elenco di tutti i servizi** che corrispondono alla richiesta del client.
3. Il client, eventualmente dopo aver consultato l'utente, **seleziona un servizio specifico**.
4. Il broker restituisce il **riferimento (handle)** del servizio, che il client utilizza per comunicare direttamente con il servizio.

![[Pasted image 20251203115204.png]]

# Supporto Tecnologico per la SOA

* Sebbene le SOA siano concettualmente indipendenti dalla piattaforma, attualmente sono implementate con grande successo su piattaforme tecnologiche di **Servizi Web**.
* Un **servizio web** è un servizio a cui si accede utilizzando protocolli standard basati su **Internet** e **XML**.

# Protocolli dei Servizi Web

* I client e i servizi applicativi necessitano di un **protocollo di comunicazione** per la comunicazione tra componenti.
* L'**Extensible Markup Language (XML)** è una tecnologia che consente a sistemi diversi di interagire attraverso lo scambio di dati e testo.
* Il **Simple Object Access Protocol (SOAP)**, un protocollo leggero sviluppato dal **World Wide Web Consortium (W3C)**, si basa su XML e HTTP per consentire lo scambio di informazioni in un ambiente distribuito.
* SOAP definisce un approccio unificato per l'invio di dati codificati in XML e consiste di tre parti:
  * Una **busta (envelope)** che definisce una struttura per descrivere il contenuto di un messaggio e come elaborarlo.
  * Un **insieme di regole di codifica** per esprimere istanze di tipi di dati definiti dall'applicazione.
  * Una **convenzione** per rappresentare chiamate di procedure remote e relative risposte.

# Servizi Web

* Le applicazioni forniscono servizi ai client.
* Un esempio di servizi applicativi sono i **Servizi Web**, che utilizzano il World Wide Web per la comunicazione applicazione-a-applicazione.
* Da una prospettiva software, i Servizi Web sono le **interfacce di programmazione delle applicazioni (API)** che forniscono un mezzo standard di comunicazione tra diverse applicazioni software sul World Wide Web.
* Da una prospettiva di applicazione aziendale, un Servizio Web è una **funzionalità di business** fornita da un'azienda sotto forma di un servizio esplicito su Internet, destinato all'utilizzo da parte di altre aziende o programmi.
* Un Servizio Web è fornito da un **fornitore di servizi** e può essere composto da altri servizi per formare nuovi servizi e applicazioni.

## Esempio

![[Pasted image 20251203121351.png]]

# Servizi di Registrazione

* Viene fornito un **servizio di registrazione** per consentire ai servizi di rendere disponibili le proprie funzionalità ai client.
* I servizi **registrano** i propri servizi presso un servizio di registrazione – un processo denominato **pubblicazione** o **registrazione** del servizio.
* La maggior parte dei broker, come quelli di CORBA e dei Servizi Web, forniscono un servizio di registrazione.
* Per i Servizi Web, viene fornito un **registro dei servizi** per consentire la pubblicazione e l'individuazione dei servizi tramite il World Wide Web.
* I fornitori di servizi registrano i propri servizi insieme alle relative descrizioni in un registro dei servizi.
* I client in cerca di un servizio possono **consultare** il registro dei servizi per trovare un servizio adatto.
* Il **Web Services Description Language (WSDL)** è un linguaggio basato su XML utilizzato per descrivere cosa fa un servizio, dove risiede e come invocarlo.

# Servizi di Brokeraggio e Scoperta

* In un ambiente distribuito, un **object broker** è un intermediario nelle interazioni tra client e servizi.
* Un esempio di tecnologia di brokeraggio è un **broker per Servizi Web**.
* Le informazioni su un Servizio Web possono essere definite dal framework **Universal Description, Discovery, and Integration (UDDI)** per l'integrazione dei Servizi Web.
* Una specifica UDDI consiste in diversi documenti correlati e in uno **schema XML** che definisce un protocollo basato su SOAP per la registrazione e la scoperta dei Servizi Web.
* Un broker per Servizi Web può utilizzare il framework UDDI per fornire un meccanismo che consenta ai client di **trovare dinamicamente** i servizi sul Web.

## Esempio di Broker per Servizi Web

![[Pasted image 20251203121554.png]]

# Protocolli e Standard dei Servizi Web

1. Il **client interroga il registro UDDI** per individuare il servizio.
2. Il **registro rimanda il client al documento WSDL**.
3. Il **client accede al documento WSDL**.
4. Il **WSDL fornisce i dati necessari per interagire con il servizio web**.
5. Il **client invia una richiesta tramite messaggio SOAP**.
6. Il **servizio web restituisce una risposta tramite messaggio SOAP**.

![[Pasted image 20251203121635.png]]

# WSDL

![[Pasted image 20251203121754.png]]
# REST

**REST** sta per **Representational State Transfer** (Trasferimento di Stato Rappresentazionale).

* REST è un termine coniato da Roy T. Fielding per descrivere uno **stile architetturale** per sistemi in rete.
* **API RESTful**
  * Un'**API basata su risorse** che utilizza il protocollo **HTTP**.

## Caratteristiche di una rete basata su REST

* **Client-Server**: uno stile di interazione basato sul "pull" (richiesta).
* **Senza stato (Stateless)**: la comunicazione client-server è vincolata dall'assenza di contesto client memorizzato sul server.
* **Cache**: client e intermediari possono memorizzare in cache le risposte.
* **Interfaccia uniforme**: tutte le risorse sono accessibili tramite un'interfaccia generica (ad es., HTTP GET, POST, PUT, DELETE), semplificando e disaccoppiando così l'architettura.
* **Risorse denominate**: il sistema è composto da risorse denominate tramite un URL (o URI).
* **Rappresentazioni interconnesse delle risorse**: le rappresentazioni delle risorse sono interconnesse tramite URL, consentendo così a un client di passare da uno stato a un altro.

# Risorse

* ogni entità distinguibile è una risorsa.
* una risorsa può essere un sito web, una pagina HTML, un documento XML, un servizio web, un dispositivo fisico, ecc.

**Gli URL identificano le risorse**

* Le risorse sono identificate in modo univoco da un URL (Assioma 0 del Web Design di Tim Berners-Lee).

![[Pasted image 20251203121926.png]]

# API RESTful

* L'API RESTful utilizza i verbi HTTP disponibili per eseguire operazioni CRUD in base al "contesto":
  * **Collezione (Collection)**: Un insieme di elementi (es.: `/users`)
  * **Elemento (Item)**: Uno specifico elemento all'interno di una collezione (es.: `/users/{id}`)

![[Pasted image 20251203122048.png]]

# Progettazione Convenzionale vs. Basata su REST

* **Scenario di esempio**
  * Una compagnia aerea vuole fornire un servizio di prenotazione web per consentire ai clienti di effettuare prenotazioni di voli tramite il Web.
  * La compagnia aerea vuole garantire che i suoi membri premium ricevano un servizio immediato, che i membri frequent flyer ricevano un servizio prioritario e che tutti gli altri ricevano un servizio standard.

* **Due approcci principali per progettare e implementare il servizio di prenotazione web**
  * **Approccio a URL singolo**: basato sulla progettazione convenzionale di servizi web.
  * **Approccio a URL multipli**: sfrutta la progettazione basata su REST.

## Approccio a URL singolo

* Il servizio Web è responsabile di esaminare le richieste in arrivo dai client per determinarne la priorità e di elaborarle di conseguenza.

![[Pasted image 20251203122152.png]]

### Svantaggi dell'approccio a URL singolo

* I client devono conoscere la regola per esprimere le priorità e l'applicazione del servizio Web deve essere scritta per comprendere tale regola.
* Si basa sul presupposto errato che un URL sia una risorsa "costosa" e che il suo uso debba essere razionato.
* Il servizio Web rappresenta un **singolo punto di guasto** e un **collo di bottiglia**.
  * Il bilanciamento del carico risulta una sfida.
* Viola l'**Assioma 0 del Web Design di Tim Berners-Lee**.

## Approccio a URL multipli

* Un URL per i membri premium, un URL diverso per i frequent flyer e un altro ancora per i clienti regolari.

![[Pasted image 20251203142542.png]]
### Multiple URLs approach advantages

È facile capire cosa fa ogni servizio semplicemente esaminando l'URL.

* Non c'è bisogno di introdurre regole complesse:
  * Le priorità sono elevate al livello di un URL. "Quello che vedi è quello che ottieni".
* È facile implementare un'alta priorità:
  * basta semplicemente assegnare una macchina veloce all'URL dei membri premium.
* Non ci sono colli di bottiglia né singoli punti di guasto.
* È coerente con l'**Assioma 0** (di Tim Berners-Lee).

# Pattern Architetturali Software per le Transazioni

* Un servizio spesso incapsula dati o fornisce accesso a dati che devono essere letti o aggiornati dai client.
* Molti servizi devono fornire operazioni di aggiornamento coordinate.
* Una **transazione** è una richiesta da parte di un client a un servizio che consiste di **due o più operazioni** che eseguono una singola funzione logica e che devono essere completate **nella loro interezza o per niente**.

## Proprietà delle transazioni

* Le transazioni hanno le seguenti proprietà, talvolta indicate come proprietà **ACID**:
  * **Atomicità (A)**: Una transazione è un'unità di lavoro indivisibile. Viene completata interamente (confermata/commit) oppure annullata (ripristinata/rollback).
  * **Consistenza (C)**: Dopo l'esecuzione della transazione, il sistema deve trovarsi in uno stato consistente.
  * **Isolamento (I)**: Il comportamento di una transazione non deve essere influenzato da altre transazioni.
  * **Durabilità (D)**: Le modifiche sono permanenti dopo il completamento di una transazione. Queste modifiche devono sopravvivere a eventuali guasti del sistema. Questa proprietà è anche chiamata **persistenza**.

### Esempio di Transazione Bancaria (Prelievo)

* Una transazione di prelievo può essere gestita in una singola operazione.
* È necessario un **semaforo** per la sincronizzazione, al fine di garantire che l'accesso al record del conto del cliente sia **mutualmente esclusivo**.
* Il processore delle transazioni **blocca** il record del conto per questo cliente, esegue l'aggiornamento e infine **sblocca** il record.

### Esempio di Transazione Bancaria (Bonifico)

* Consideriamo una transazione di bonifico tra due conti – ad esempio, da un conto di risparmio a un conto corrente – in cui i conti sono gestiti da due banche (servizi) separate.
* In questo caso, è necessario **addebitare** il conto di risparmio e **accreditare** il conto corrente.
* Pertanto, la transazione di bonifico consiste di **due operazioni che devono essere atomiche** – un'operazione di addebito e un'operazione di accredito – e la transazione di bonifico deve essere **confermata o annullata**:
  * **Confermata (Committed)**: avvengono sia l'operazione di accredito che quella di addebito.
  * **Annullata (Aborted)**: non avviene né l'operazione di accredito né quella di addebito.

# Protocollo di Conferma in Due Fasi (Two-Phase Commit Protocol)

* Il *Two-Phase Commit Protocol pattern* affronta il problema di gestire transazioni atomiche in sistemi distribuiti, sincronizzando gli aggiornamenti su nodi diversi.
* Il coordinamento della transazione è fornito dal **CommitCoordinator** (Coordinatore di Conferma).
* Esiste un **servizio partecipante** per ciascun nodo.
* Nel caso della transazione di bonifico bancario ci sono due partecipanti:
  * **firstBankService**, che gestisce il conto dal quale vengono trasferiti i fondi (conto "Da" / from Account), e
  * **secondBankService**, che gestisce il conto al quale vengono trasferiti i fondi (conto "A" / to Account).

## Fase 1

![[Pasted image 20251203145759.png]]
## Fase 2

![[Pasted image 20251203145818.png]]

# Pattern di Transazione Composta

* La precedente transazione di bonifico bancario è un esempio di **transazione piatta** (flat transaction), che ha una caratteristica "tutto-o-niente".
* Una **transazione composta** (compound transaction), al contrario, potrebbe richiedere solo un **ripristino parziale** (rollback parziale).
* Il *Compound Transaction pattern* può essere utilizzato quando l'esigenza transazionale del cliente può essere scomposta in transazioni atomiche piatte più piccole, dove ogni transazione atomica può essere eseguita e ripristinata separatamente.
* Ad esempio, se un'agenzia di viaggi effettua una prenotazione aerea, seguita da una prenotazione alberghiera e una prenotazione di un'auto a noleggio, è più flessibile trattare questa prenotazione come composta da **tre transazioni piatte**. Trattare la transazione come composta consente di modificare o annullare una parte della prenotazione senza che le altre parti ne siano influenzate.

## Esempio di Pattern di Transazione Composta
![[Pasted image 20251203154221.png]]

# Pattern di Transazione a Lunga Durata

* Una transazione a lunga durata è una transazione che coinvolge **un essere umano nel ciclo** e che potrebbe richiedere un tempo lungo e potenzialmente indefinito per essere eseguita, poiché il comportamento umano individuale è imprevedibile.
* Il *Long-Living Transaction pattern* suddivide una transazione a lunga durata in **due o più transazioni separate** (solitamente due) in modo che il processo decisionale umano avvenga tra le coppie successive (ad esempio, prima e seconda) di transazioni.

## Esempio di Pattern di Transazione a Lunga Durata

![[Pasted image 20251203154728.png]]

# Pattern di Negoziazione

* In alcune SOA, il coordinamento tra servizi coinvolge **negoziazioni tra agenti software** in modo che possano prendere decisioni in modo cooperativo.
* Nel **Negotiation pattern** (noto anche come *Agent-Based Negotiation* o *Multi-Agent Negotiation pattern*), un **agente client** agisce per conto dell'utente e presenta una proposta a un **agente servizio**.
* L'agente servizio tenta di soddisfare la proposta del client, il che potrebbe comportare la comunicazione con altri servizi.
* Dopo aver determinato le opzioni disponibili, l'agente servizio offre quindi all'agente client una o più opzioni che si avvicinano maggiormente alla proposta originale dell'agente client.
* L'agente client può quindi richiedere una delle opzioni, proporre ulteriori opzioni o rifiutare l'offerta.
* Se l'agente servizio può soddisfare la richiesta dell'agente client, **accetta** la richiesta; in caso contrario, la **rigetta**.

## Servizi di Negoziazione

* L'**agente client**, che agisce per conto del client, può fare una delle seguenti cose:
  * **Proporre un servizio.** L'agente client propone un servizio all'agente servizio. Questo servizio proposto è **negoziabile**, nel senso che l'agente client è disposto a considerare controfferte.
  * **Richiedere un servizio.** L'agente client richiede un servizio dall'agente servizio. Questo servizio richiesto è **non negoziabile**, nel senso che l'agente client non è disposto a considerare controfferte.
  * **Rifiutare un'offerta di servizio.** L'agente client rifiuta un'offerta fatta dall'agente servizio.

* L'**agente servizio**, che agisce per conto del servizio, può fare una delle seguenti cose:
  * **Offrire un servizio.** In risposta a una proposta del client, un agente servizio presenta una controproposta.
  * **Rifiutare una richiesta/proposta del client.** L'agente servizio rifiuta il servizio proposto o richiesto dall'agente client.
  * **Accettare una richiesta/proposta del client.** L'agente servizio accetta il servizio proposto o richiesto dall'agente client.

# Progettazione dell'Interfaccia del Servizio in SOA

* I nuovi servizi vengono inizialmente progettati utilizzando criteri di strutturazione delle classi.
* Durante la **modellazione dinamica delle interazioni**, viene determinata l'interazione tra gli oggetti client e gli oggetti servizio.
* L'approccio adottato per la progettazione delle operazioni del servizio è simile a quello utilizzato nella progettazione dell'interfaccia di una classe.
* I **messaggi** che arrivano a un servizio costituiscono la base per la progettazione delle sue operazioni. I messaggi vengono analizzati per determinare il **nome dell'operazione**, così come per determinare i **parametri di input e output**.

## Coordinamento dei Servizi in SOA

* Nelle applicazioni SOA che coinvolgono più servizi, di solito è necessario il **coordinamento** di questi servizi.
* Per garantire un **basso accoppiamento** tra i servizi, è spesso meglio separare i dettagli del coordinamento dalla funzionalità dei singoli servizi.
* Nella SOA, vengono forniti diversi tipi di coordinamento, tra cui **orchestrazione** e **coreografia**.

# Orchestrazione e Coreografia

* **Orchestrazione** consiste in una **logica di coordinamento del flusso di lavoro controllata centralmente** per coordinare più servizi partecipanti.
  * Ciò consente il **riuso di servizi esistenti** incorporandoli in nuove applicazioni di servizio.
* **Coreografia** fornisce un **coordinamento distribuito** tra i servizi e può essere utilizzata quando è necessario coordinare diverse organizzazioni aziendali.
  * Pertanto, la coreografia può essere utilizzata per la **collaborazione tra servizi** provenienti da diversi fornitori di servizi, appartenenti a diverse organizzazioni aziendali.
  * Mentre l'orchestrazione è **controllata centralmente**, la coreografia coinvolge un **controllo distribuito**.

# Coordinamento

* Poiché i termini **orchestrazione** e **coreografia** sono spesso usati in modo intercambiabile, il termine più generale **coordinamento** viene utilizzato per descrivere il **controllo e la sequenzializzazione** dei diversi servizi richiesti da un'applicazione SOA, siano essi controllati centralmente o coinvolgano un controllo distribuito.
* Anche i **pattern di transazione** possono essere utilizzati per il coordinamento dei servizi.**

* Poiché i termini **orchestrazione** e **coreografia** sono spesso usati in modo intercambiabile, il termine più generale **coordinamento** viene utilizzato per descrivere il **controllo e la sequenzializzazione** dei diversi servizi richiesti da un'applicazione SOA, siano essi controllati centralmente o coinvolgano un controllo distribuito.
* Anche i **pattern di transazione** possono essere utilizzati per il coordinamento dei servizi.

## Progettazione Orientata agli Oggetti Dettagliata (Detailed OOD)

* La **Progettazione Orientata agli Oggetti Preliminare (Preliminary OOD)** fornisce la piattaforma di esecuzione HW/SW alla quale la sottofase di progettazione dettagliata deve conformarsi.
* La parte principale della sottofase di **Detailed OOD** è dedicata a **raffinare** quanto prodotto nella fase di **Analisi Orientata agli Oggetti (OOA)**.
* L'obiettivo è trasformare i **modelli OOA**, definiti nel dominio del problema, in **modelli definiti nel dominio della soluzione**, che a loro volta saranno utilizzati nella fase di codifica.
* La sottofase di Detailed OOD fornisce la **progettazione dettagliata** delle unità architetturali identificate nella sottofase di Preliminary OOD, attraverso l'**aggiunta di dettagli tecnici** (o producendo modelli aggiuntivi a un livello di astrazione inferiore).
* La sottofase di Detailed OOD definisce la **collaborazione tra oggetti**, che è alla base di ogni programma orientato agli oggetti.
* Tale collaborazione viene definita attraverso la **realizzazione dei casi d'uso e delle operazioni**.
* Le **collaborazioni** stanno alla Detailed OOD come i **casi d'uso** stanno alla OOA:
  * se i casi d'uso guidano l'OOA, allora le collaborazioni guidano la Detailed OOD.

# Realizzazione dei casi d'uso

* I casi d'uso introdotti nella fase di OOA vengono realizzati attraverso **collaborazioni** nella fase di OOD.
* Un singolo caso d'uso viene tipicamente realizzato da un **insieme di collaborazioni**, a causa del diverso livello di astrazione.
* Una collaborazione ha:
  * **Una parte comportamentale**:
    * Rappresenta la dinamica che mostra come gli elementi statici collaborano.
    * Viene definita utilizzando **diagrammi di comunicazione**.
  * **Una parte strutturale**:
    * Rappresenta gli aspetti statici della collaborazione.
    * Viene definita elaborando il **diagramma delle classi OOA** con i dettagli implementativi, portando a **diagrammi di struttura composita**.

# Collaborazione – Gestione del controllo

**Sistema di Iscrizione Universitaria**

* **Esempio**
  * Aggiungere uno studente (`Student`) a un'offerta formativa (`CourseOffering`).
* **Azioni da eseguire**
  1. Identificare i corsi prerequisiti per l'offerta formativa.
  2. Verificare se lo studente soddisfa i prerequisiti.
* Si consideri che:
  * Il messaggio `enrol()` è inviato dall'oggetto di confine `:EnrolmentWindow`.
  * Sono coinvolte tre classi entità – `CourseOffering`, `Course` e `Student`.
* Sono possibili **almeno quattro soluzioni** (con diverse caratteristiche di accoppiamento tra classi).

## Soluzione 1

![[Pasted image 20251203155625.png]]
## Soluzione 2
![[Pasted image 20251203155644.png]]

## Soluzione 3

![[Pasted image 20251203155708.png]]

## Soluzione 4

![[Pasted image 20251203155728.png]]

# Problemi di accoppiamento

* L'approccio BCE specifica **tre livelli di classi**.
* Gli oggetti comunicano **all'interno di un livello** e **tra i livelli adiacenti**.
* **Accoppiamento intra-livello**:
  * Desiderabile.
  * Localizza la manutenzione e l'evoluzione del software a singoli livelli.
* **Accoppiamento inter-livello**:
  * Da minimizzare.
  * Le interfacce di comunicazione devono essere definite con attenzione.
* La **Legge di Demeter** può essere utilizzata per ridurre l'accoppiamento inter-livello tra le classi.

# Legge di Demeter

* Il destinatario di un messaggio (nei metodi di una classe) può essere solo uno dei seguenti oggetti:
  1. L'oggetto stesso a cui appartiene il metodo (cioè `this` in C++ e Java, `self` e `super` in Smalltalk).
  2. Un oggetto che è un **argomento nella firma del metodo**.
  3. Un oggetto a cui si riferisce un **attributo dell'oggetto stesso** (legge forte: gli attributi ereditati non possono essere usati per identificare l'oggetto destinatario).
  4. Un oggetto **creato dal metodo**.
  5. Un oggetto a cui si riferisce una **variabile globale**.

* Nota anche come **"non parlare con estranei"**.

# Classe Strutturata UML

* Una classe strutturata contiene **ruoli** o **parti** che ne formano la struttura e ne realizzano il comportamento.
  * Descrive la **struttura di implementazione interna**.
* Le parti stesse possono a loro volta essere **classi strutturate**.
  * Consente una **struttura gerarchica** per esprimere chiaramente modelli multilivello.
* Un **connettore** viene utilizzato per rappresentare un'associazione in un contesto specifico.
  * Rappresenta i **percorsi di comunicazione** tra le parti.

## Utilizzo della Classe Strutturata

* Può essere utilizzata come **blocco costitutivo primario** di un'applicazione.
  * Fornisce una rappresentazione grafica degli elementi di progetto.
  * Può nascondere i dettagli implementativi.
* Potente strumento di **astrazione**: lo stesso costrutto si applica a più livelli semantici.
* Favorisce una comunicazione e comprensione chiara dell'**architettura del sistema**.
  * **Incapsulamento rigoroso** del comportamento.
* Le interazioni sono limitate a **comunicazioni basate su messaggi** passati attraverso interfacce esterne (**porte/ports**).

## Classe Strutturata: Vista Concettuale

![[Pasted image 20251203160050.png]]

## Classe Strutturata: Comportamento

* Macchina a stati gerarchica opzionale
  * Gestore di segnali basato su stati.
![[Pasted image 20251203160117.png]]

## Classe Strutturata: Unità di Progettazione Autonoma

* Il rigido **incapsulamento** garantisce che l'implementazione sia **indipendente dall'ambiente**.
  * Le **porte** possono svolgere un ruolo di mediazione **bidirezionale**.
* L'ambiente vede solo la **porta** della classe strutturata.
* Il comportamento interno è costruito in base alle "specifiche" fornite dalla sua **interfaccia**.
  * Le classi strutturate possono essere **progettate e testate in modo indipendente** (unit test).

![[Pasted image 20251203160358.png]]

### Esempio: Diagramma di Struttura Composita UML

![[Pasted image 20251203160420.png]]

# Configurazione della Piattaforma

* Una configurazione della piattaforma descrive la **soluzione hardware/software** che definisce come la funzionalità del sistema può essere distribuita tra nodi fisici.
  * Spiega la **relazione tra gli elementi del modello e la loro implementazione**, nonché il loro **deployment** (distribuzione).
* Si ottiene attraverso:
  * La **definizione della configurazione della piattaforma** mediante l'uso di un **diagramma di deployment**.
  * L'**allocazione degli elementi del sistema (artefatti)** ai nodi dei diagrammi di deployment.

# Elementi di Modellazione del Modello di Deployment

* **Nodo**
  * Risorsa computazionale fisica in esecuzione (run-time).
  * **Nodo processore** - Esegue software di sistema.
  * **Nodo dispositivo**
    * Dispositivo di supporto.
    * Tipicamente controllato da un processore.
* **Connessione**
  * Meccanismo di comunicazione.
  * Mezzo fisico.
  * Protocollo software.

![[Pasted image 20251203160558.png]]

## Cos'è un Nodo?

* Rappresenta una **risorsa computazionale in esecuzione (run-time)** e generalmente dispone almeno di memoria e spesso di capacità di elaborazione.
* **Tipi**:
  * **Dispositivo (Device)** - Risorsa computazionale fisica con capacità di elaborazione. I dispositivi possono essere nidificati.
  * **Ambiente di Esecuzione (Execution Environment)** - Rappresenta una specifica piattaforma di esecuzione (es. un sistema operativo, un server applicativo, un motore di database) ospitata su un dispositivo.

![[Pasted image 20251203160754.png]]

## Cos'è un Connettore?

* Un connettore rappresenta un **meccanismo di comunicazione** descritto da:
  * **Mezzo fisico** (es. cavo Ethernet, fibra ottica, connessione wireless).
  * **Protocollo software** (es. TCP/IP, HTTP, SOAP, CORBA IIOP).

![[Pasted image 20251203160816.png]]

## Esempio: Diagramma di Deployment
![[Pasted image 20251203160850.png]]

## Considerazioni per l'Allocazione di Processi ai Nodi

* **Pattern di distribuzione** (es. client-server, peer-to-peer, a tre livelli).
* **Tempo di risposta e throughput del sistema** (carico computazionale e latenza).
* **Minimizzazione del traffico di rete** (località dei dati e delle comunicazioni).
* **Capacità del nodo** (CPU, memoria, archiviazione).
* **Larghezza di banda del mezzo di comunicazione**.
* **Disponibilità dell'hardware e dei collegamenti di comunicazione** (affidabilità, ridondanza).
* **Requisiti di reindirizzamento** (failover, bilanciamento del carico).

### Esempio: Diagramma di Deployment con Processi

![[Pasted image 20251203161353.png]]

## Cos'è il Deployment (Distribuzione)?

* Il **deployment** è l'**assegnazione**, o **mappatura**, di **artefatti software** a **nodi fisici** durante l'esecuzione.
  * Gli **artefatti** sono le entità che vengono distribuite sui nodi fisici.
* I **processi** vengono assegnati a computer.
* Gli **artefatti** modellano entità fisiche:
  * File, eseguibili, tabelle di database, pagine web, e così via.
* I **nodi** modellano risorse computazionali:
  * Computer, unità di archiviazione.

# Esempio: Distribuzione di Artefatti sui Nodi

![[Pasted image 20251203161444.png]]


# Cos'è la Manifestazione?

* L'**implementazione fisica** di un elemento del modello sotto forma di un artefatto.
  * Una **relazione** tra l'elemento del modello e l'artefatto che lo implementa.
* Gli elementi del modello sono tipicamente implementati come un **insieme di artefatti**.
* Esempi di **Elementi del modello** sono file sorgente, file eseguibili, file di documentazione.
* Esempi di **Artefatti** corrispondenti sono `.java` (sorgente), `.class` o `.jar` (eseguibile), `.pdf` (documentazione).

## Example: Manifestation


![[Pasted image 20251203161609.png]]

# Cos'è una Specifica di Deployment (Deployment Specification)?

* Una **specifica dettagliata dei parametri** per la distribuzione di un artefatto su un nodo.
  * Può definire i **valori che parametrizzano l'esecuzione** dell'artefatto sul nodo target.

![[Pasted image 20251203164750.png]]