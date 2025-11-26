È la serie di attività necessaria alla realizzazione del prodotto software nei tempi, con i costi e con le desiderate caratteristiche di qualità.

Nel suo contesto:
- Si applicano metodi, tecniche e strumenti.
- Si creano prodotti (sia intermedi che finali).
- Si stabilisce il controllo gestionale del progetto.
- Si garantisce la qualità.
- Si governano le modifiche.

# Fasi del processo
Si divide in **3 stadi:**
- **Sviluppo**
- **Manutenzione**
- **Dismissione**. 

Nello stadio di <u>Sviluppo</u> si possono riconoscere **due tipi di fasi**:
- **Fasi di definizione**: si occupano di "cosa" il software deve fornire. Si definiscono i requisiti e si producono le specifiche.
- **Fasi di produzione**: definiscono "come" realizzare quanto ottenuto con le fasi di definizione. Si progetta il software, si codifica, si integra e si rilascia al cliente.

Lo stadio di <u>Manutenzione</u> è a supporto del software realizzato e prevede fasi di definizione e/o produzione al suo interno.

Durante ogni fase si procede ad effettuare il *testing* di quanto prodotto, mediante opportune tecniche di *verifica e validazione* (V&V) applicate sia ai prodotti intermedi che al prodotto finale.

## Tipi di manutenzione
- **Manutenzione correttiva**: ha lo scopo di eliminare i difetti che producono guasti del software.
- **Manutenzione adattativa**: ha lo scopo di adattare il software a cambiamenti riguardanti l’ambiente operativo per cui é stato sviluppato
- **Manutenzione perfettiva**: ha lo scopo di estendere il software per accomodare funzionalità aggiuntive.
- **Manutenzione preventiva (o software reengineering)**: consiste nell'effettuare modifiche che rendano più semplici le correzioni, gli adattamenti e le migliorie.

# Definizione di ciclo di vita
**Intervallo di tempo tra l’istante di creazione del software e l’istante di dismissione**

Include le fasi di:
- Definizione dei requisiti 
- Specifica 
- Pianificazione 
- Progetto preliminare
- Progetto dettagliato 
- Codifica 
- Integrazione 
- Testing 
- Uso 
- Manutenzione 
- Dismissione.

>[!nb]
>Tali fasi possono sovrapporsi o essere eseguite in modo iterativo.

## Modelli di ciclo di vita
Specifica le fasi attraverso le quali il software progredisce e l’ordine di esecuzione di quest’ultime.

La scelta del modello dipende da:
1. natura dell'applicazione
2. maturità dell’organizzazione
3. metodi e tecnologie usate
4. eventuali vincoli dettati dal cliente.

L'assenza di un modello del ciclo di vita *implica* la modalità di sviluppo **build & fix**, dove il prodotto software viene sviluppato e successivamente rilavorato fino a soddisfare le necessità del cliente.
### Modello Build & Fix
![[Build_Fix.png|center|600]]

### Modello Waterfall
![[Waterfall.png|center|600]]
### V&V nel Waterfall
![[VV_Water.png|center|600]]
Il prodotto software non può essere certificato.

## Modello Rapid Prototyping
![[RPM.png|center|600]]
La differenza principale consiste nell'uso di un prototipo per definire i requisiti. Limita al massimo il numero di errori durante la raccolta dei requisiti che possono avere conseguenze disastrose per lo sviluppo del software. Attraverso il prototipo si possono fare verifiche e validazioni migliori rispetto ad un controllo visuale.

# Software Prototyping
Il principale uso é quello di aiutare i clienti e gli sviluppatori nel capire i requisiti del software:

- **Requirements elicitation**: Gli utenti possono sperimentare tramite un prototipo e verificare se tale progetto sia appropriato per il loro lavoro
- **Requirements validation**: Il prototipo puó rivelare errori e omissioni nei requisiti

La prototipazione puó essere considerata una pratica di riduzione di rischi nei requisiti

**Benefits**:
- Chiarire incomprensioni tra utente e sviluppatore
- Identificare servizi mancanti o errati
- Disponibilitá di un sistema funzionante nella fase iniziale
- Potrebbe servire come base per derivare specifiche software
- Il prototipo può supportare la formazione degli utenti e test del prodotto

## Prototyping process
![[P_Process.png|center|600]]

## Prototypes as specifications
- Alcune parti dei requisiti potrebbero risultare impossibili da prototipare e quindi non compaiono nelle specifiche
- Un’implementazione non ha validitá legale come contratto
- I requisiti non funzionali non possono essere testati a pieno nel prototipo
## Throw-away prototyping
Un prototipo, di solito una versione pratica e semplificata del prodotto, viene realizzato per individuare eventuali problemi nei requisiti, e successivamente scartato. Il prodotto vero e proprio viene poi sviluppato utilizzando un processo diverso.

• Questo approccio serve a ridurre il rischio legato alla definizione dei requisiti.  
• Il prototipo viene creato partendo da requisiti iniziali, consegnato per essere testato e poi eliminato.  
• Il prototipo “usa e getta” **non deve essere considerato un prodotto finale** perché:  
- Alcune caratteristiche potrebbero non essere state incluse.  
- Non esiste una specifica per la manutenzione a lungo termine. 
- La struttura del prototipo è spesso improvvisata, quindi il risultato sarebbe difficile da mantenere.

### Throw-away prototyping process
![[Throw_Away.png|center|600]]

### Throw-away prototype delivery
Gli sviluppatori possono essere messi sotto pressione affinché consegnino un prototipo “usa e getta” come se fosse il prodotto finale.  
Questo **non è consigliato**, perché:  
- Potrebbe essere impossibile adattare il prototipo per soddisfare i requisiti non funzionali.  
- Il prototipo, quasi sempre, non è documentato.  
- La sua struttura interna tende a deteriorarsi a causa delle modifiche fatte durante lo sviluppo.  
- Gli standard di qualità normalmente adottati nell’organizzazione potrebbero non essere stati applicati.

## Prototyping key points
- Un prototipo può essere utilizzato per dare agli utenti finali un’idea concreta delle capacità del prodotto.  
- Il prototipaggio è sempre più diffuso nello sviluppo di prodotti in cui la rapidità è fondamentale.  
- Il prototipaggio “usa e getta” serve a comprendere meglio i requisiti del prodotto.  
- È essenziale poter sviluppare prototipi rapidamente, il che può richiedere di omettere alcune funzionalità o di allentare i vincoli non funzionali.  
- La programmazione visuale è una componente fondamentale della maggior parte dei metodi di sviluppo di prototipi.

# Visual programming
- Linguaggi di scripting come Visual Basic supportano la programmazione visuale: il prototipo viene sviluppato creando l’interfaccia utente tramite elementi standard e collegando a questi gli appositi componenti.  
- Esiste un’ampia libreria di componenti pensata per facilitare questo tipo di sviluppo.  
- Questi componenti possono essere personalizzati per adattarsi alle esigenze specifiche dell’applicazione.
Esempio:
![[Es_Visual_Programming.png|center|600]]

## Problems with visual development
- È difficile coordinare lo sviluppo quando il lavoro è suddiviso tra più membri del team.  
- Non è presente un’architettura software esplicita.  
- Le dipendenze complesse tra le varie parti del programma possono creare problemi di manutenibilità.


# Process iteration

I requisiti evolvono **SEMPRE** nel corso di un progetto, quindi lo sviluppo di grandi prodotti avviene in fasi in cui gli stage precedenti sono rielaborati.

Lo sviluppo è suddiviso in iterazioni più piccole e gestibili, con due approcci:
- Incremental development.
- Spiral development.
# Incremental development

![[Pasted image 20251121123643.png]]

L'**incremental development** consiste nello sviluppo del software in "pezzi", detti *incrementi* (build), ognuno dei quali aggiunge nuove funzionalità a quelle già esistenti e alla fine l'insieme degli incrementi costituisce il prodotto finale. 

- Efficace quando il cliente vuole continuamente verificare i progressi nello sviluppo del prodotto e quando i requisiti subiscono modifiche.
- Include aspetti tipici del modello basato su rapid prototyping (l’utente può sperimentare l’utilizzo del prodotto contenente gli incrementi consegnati, mentre i restanti sono ancora in fase di sviluppo).

- Può essere realizzato in due versioni:
	- Versione con overall architecture.
	- Versione senza overall architecture (più rischiosa).

## Versione con overall architecture

![[Pasted image 20251121124248.png]]
## Versione senza overall architecture

![[Pasted image 20251121124301.png]]
## Impatto sui costi del software

![[Pasted image 20251121124312.png]]
## Confronto con modello a cascata


| **Modello a cascata                                                         | Modello incrementale                                                |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| Requisiti "congelati" alla fine della fase di specifica                     | Requisiti suddivisi in classi di priorità e facilmente modificabili |
| Feedback del cliente solo dopo il termine dello sviluppo                    | Feedback del cliente continuo durante lo sviluppo                   |
| Fasi condotte in sequenza (l'output di una diventa input per la successiva) | Fasi che possono essere condotte in parallelo                       |
| Prevede fasi di progetto dettagliato e codifica dell'intero prodotto        | Progetto dettagliato e codifica sono fatte sul singolo *build*      |
| Team di sviluppo con numero elevato di persone                              | Team di sviluppo differenti, ciascuno di piccole dimensioni         |
# Modello a spirale

![[Pasted image 20251121124736.png]]
## Modello a spirale semplificato (versione lineare)

![[Pasted image 20251121124747.png]]
## Modello a spirale semplificato

![[Pasted image 20251121124806.png]]
## Modello full-spiral [Boehm, 1988]

![[Pasted image 20251121124819.png]]
# Risk management

Il **Risk management** è il processo di identificazione, analisi e gestione dei rischi che potrebbero influenzare l'esito e la qualità del progetto

**Def.**
Un *rischio* è un evento potenziale che potrebbe avere un impatto negativo. Ci sono tre categorie principali:
- **Project risks** influenzano la pianificazione o le risorse.
- **Product risks** influenzano la qualità e le prestazioni del software in sviluppo.
- **Business risks** influenzano l'organizzazione che sviluppa o acquista il software.
## Risks by category

| Risk                        | Risk Type           | Description                                                                            |
| --------------------------- | ------------------- | -------------------------------------------------------------------------------------- |
| Staff turnover              | Project             | Lo staff esperto lascerà il progetto prima del termine.                                |
| Management change           | Project             | Cambiamento nel management dell'organizzazione con nuove priorità.                     |
| Hardware unavailability     | Project             | L'hardware essenziale per il progetto non è consegnato nei tempi previsti.             |
| Requirements change         | Project and product | Ci sarà un numero maggiore di cambiamenti ai requisiti rispetto a quanto previsto.     |
| Specification delays        | Project and product | Le specifiche delle interfacce essenziali non saranno disponibili nei tempi previsti.  |
| Size underestimate          | Project and product | La dimensione del sistema è stata sottostimata.                                        |
| CASE tool under-performance | Product             | I tool CASE che supportano il progetto non performano come previsto.                   |
| Technology change           | Business            | La tecnologia su cui si basa il sistema viene superata da una nuova tecnologia.        |
| Product competition         | Business            | Un prodotto concorrente viene immesso sul mercato prima che il sistema sia completato. |
## Fasi del risk management

- **Identificazione**: identificare i possibili rischi del progetto.
- **Analisi**: Si valuta ogni rischio in base alla probabilità che accada e l'impatto che può avere.
- **Pianificazione**: si definiscono dei piani per evitare o ridurre gli effetti del rischio
- **Monitoring**: Durante il progetto si monitorano i rischi.

![[Pasted image 20251121130202.png]]
### Risk identification

| Risk Type          | Possible Risks                                                                                                                                                                                                          |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Technology**     | - Il database utilizzato nel sistema non può processare il numero di transazioni al secondo previsto.<br>- I componenti software che dovrebbero essere riutilizzati contengono difetti che ne limitano la funzionalità. |
| **People**         | - È impossibile reclutare personale con le competenze richieste.<br>- Il personale chiave è malato o non disponibile in momenti critici.<br>- La formazione necessaria per il personale non è disponibile.              |
| **Organisational** | - L’organizzazione viene ristrutturata, con conseguente cambio di management responsabile del progetto.<br>- Problemi finanziari dell’organizzazione impongono riduzioni nel budget del progetto.                       |
| **Tools**          | - Il codice generato dai tool CASE è inefficiente.<br>- I tool CASE non possono essere integrati.                                                                                                                       |
| **Requirements**   | - I cambiamenti ai requisiti richiedono un’ampia revisione del design.<br>- I clienti non comprendono l’impatto dei cambiamenti ai requisiti.                                                                           |
| **Estimation**     | - Il tempo necessario per sviluppare il software è sottostimato.<br>- Il tasso di riparazione dei difetti è sottostimato.<br>- La dimensione del software è sottostimata.                                               |
Visual Basic è un esempio di CASE (Computer-Aided Software Engineering) tool
### Risk analysis

Valutà la probabilità e la conseguenza di ogni rischio. 
La probabilità dei rischi può essere:
- **Very low** (<10%)
- **Low** (10-25%)
- **Moderate** (25-50%)
- **High** (50-75%)
- **Very** high (>75%)

Le conseguenze possono essere:
- **Catastrofiche**
- **Serie**
- **Tollerabili**
- **Insignificanti**

| Risk                                                                                                    | Probability | Effects       |
| ------------------------------------------------------------------------------------------------------- | ----------- | ------------- |
| Problemi finanziari nell'organizzazione forzano la riduzione del project budget.                        | Low         | Catastrophic  |
| Impossibile trovare staff con le skill richieste per il progetto                                        | High        | Catastrophic  |
| Il personale importante è malato nei punti critici del progetto.                                        | Moderate    | Serious       |
| Componenti software da riutilizzare contengono difetti che limitano le loro funzionalità                | Moderate    | Serious       |
| Proposta di cambiamento di requisiti che richiedono una grande rielaborazione                           | Moderate    | Serious       |
| L'organizzazione è rivista e nuovi dirigenti sono responsabili del progetto                             | High        | Serious       |
| Il database utilizzato nel sistema non può elaborare il numero di transazioni al secondo come previsto. | Moderate    | Serious       |
| Il tempo necessario per sviluppare il software è sottovalutato.                                         | High        | Serious       |
| I CASE tools non sono utilizzabili.                                                                     | High        | Tolerable     |
| I clienti non comprendono l'impatto dei cambiamenti nei requisiti.                                      | Moderate    | Tolerable     |
| La formazione obbligatoria per il personale non è disponibile.                                          | Moderate    | Tolerable     |
| Il tasso di riparazione dei difetti è sottostimato.                                                     | Moderate    | Tolerable     |
| La dimensione del software è sottovalutata.                                                             | High        | Tolerable     |
| Il codice generato dagli strumenti CASE è inefficiente.                                                 | Moderate    | Insignificant |

Si identificano i rischi principali considerando:
- tutti i rischi catastrofici
- tutti i rischi seri che hanno probabilità di accadere oltre la moderata

Si classificano i rischi in ordine di importanza

### Risk planning

Si considera ogni rischio e si sviluppa una strategia per gestirlo:
- **Avoidance strategies**: ridurre la probabilità che il rischio si presenti.
- **Minimization strategies**: ridurre l'impatto del rischio sul progetto.
- **Contingency plans**: se si verifica il rischio, si utilizza un piano di emergenza per affrontare il rischio

### Risk management strategies

| Risk                                                                     | Strategy                                                                                                                                                        |
| ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Problemi finanziari dell'organizzazione / ristrutturazione organizzativa | Si prepara un documento informativo per il senior management che mostra come il progetto stia dando un contributo molto importante agli obiettivi dell'azienda. |
| Problemi di reclutamento                                                 | Si avvisa il cliente delle potenziali difficoltà e possibili ritardi; si verificano componenti acquistabili per ridurre il carico di sviluppo.                  |
| Malattia del personale                                                   | Si riorganizza il team per aumentare la sovrapposizione delle attività e fare in modo che le persone svolgano il compito degli altri                            |
| Componenti difettosi                                                     | Sostituire i componenti difettosi con componenti nuovi e affidabili                                                                                             |
| Cambio ai requisiti                                                      | Derivare informazione di tracciabilità per valutare l'impatto del cambio dei requisiti; massimizzare l'information hiding nella progettazione                   |
| Database performance                                                     | Valutare la possibilità di comprare un database con performance migliori                                                                                        |
| Tempo di sviluppo sottovalutato                                          | Valutare l'acquisto di componenti già pronti; valutare l'uso di un generatore di programmi                                                                      |
### Risk monitoring

Valutare regolarmente ogni rischio per decidere se sta diventando più o meno probabili da verificarsi. Per la valutazione si considerano i fattori di rischio

Valutare anche se gli effetti del rischio sono cambiati (e nel caso rivalutarli). Ogni rischio principale dovrebbe essere discusso durante riunioni di gestione del progresso del progetto.
#### Risk factors

| Risk Type     | Potential Indicators                                                                                                       |
| ------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Teconologia   | Consegna tardiva di hardware o software di supporto; molti hanno segnalato problemi tecnologici                            |
| People        | Basso morale del personale; scarsi rapporti tra i membri del team; disponibilità di lavoro                                 |
| Organizzativa | Gossip organizzativi, mancanza di azione da parte della direzione                                                          |
| Tools         | Riluttanza dei membri del team a usare gli strumenti, lamentele sugli strumenti CASE, richieste di workstation più potenti |
| Requirements  | Molte richieste di cambiamento dei requisiti, reclami dei clienti                                                          |
| Stima         | Mancato rispetto del calendario concordato, mancata risoluzione dei difetti segnalati                                      |
# Altri modelli
## Modello object-oriented

![[Pasted image 20251121133754.png]]
1. Minori costi di manutenzione
## Modello di ingegneria Concorrente

Ha come obiettivo la riduzione di tempi e costi di sviluppo, mediante un approccio sistematico al progetto integrato e concorrente di un prodotto software e del processo ad esso associato.

Le fasi di sviluppo coesistono invece di essere eseguite in sequenza.
## Modello basato su metodi formali

Comprende una serie di attività che conducono alla specifica formale matematica del software, al fine di eliminare ambiguità, incompletezze ed inconsistenze e facilitare la verifica dei programmi mediante l'applicazione di tecniche matematiche.

La Cleanroom Software Engineering (1987) ne rappresenta un esempio di realizzazione, in cui viene
enfatizzata la possibilità di rilevare i difetti del software in modo più tempestivo rispetto ai modelli tradizionali.

# Il Modello Microsoft
Le organizzazioni che sviluppano software commerciale, fin dalla metà degli anni ’80, hanno dovuto affrontare problemi legati a:

- Incremento della qualità dei prodotti software.
- Riduzione dei tempi e dei costi di sviluppo.

Per affrontare tali sfide è stato adottato un processo **iterativo**, **incrementale** e **concorrente**, che valorizza la creatività delle persone coinvolte nello sviluppo.

# Approccio Synch & Stabilize
L’approccio attualmente utilizzato da Microsoft si basa su:

- **Sincronizzazione giornaliera** del lavoro di singoli sviluppatori o piccoli team mediante una **daily build**, ottenuta assemblando componenti software completi o parziali, successivamente testati e corretti.
- **Stabilizzazione** periodica del prodotto in diversi **milestone** durante lo sviluppo, invece che un’unica stabilizzazione finale. 

# Ciclo di sviluppo a 3 fasi
Il ciclo di sviluppo è suddiviso in tre fasi:

- **Planning phase**: definizione della visione del prodotto, della specifica e della pianificazione.
- **Development phase**: sviluppo delle funzionalità in 3/4 sotto-progetti sequenziali, ciascuno dei quali produce una milestone release.
- **Stabilization phase**: test interno ed esterno, stabilizzazione finale e rilascio del prodotto. 

## Planning phase
- **Vision statement**: il product e il program management utilizzano il feedback degli utenti per identificare e ordinare per priorità le funzionalità del prodotto.
- **Specification document**: basandosi sulla visione, il program management e il gruppo di sviluppo definiscono funzionalità, architettura e interdipendenze dei componenti.
- **Schedule and Feature Team Formation**: il program management pianifica e organizza team funzionali, composti da circa 1 program manager, 3–8 sviluppatori e 3–8 tester (in rapporto 1:1 con gli sviluppatori).  

## Development phase
I program manager coordinano l’evoluzione della specifica. Gli sviluppatori progettano, codificano e fanno debug. I tester lavorano in parallelo con gli sviluppatori.

- Sottoprogetto 1: primo terzo delle funzionalità (le più critiche e componenti condivisi).
- Sottoprogetto 2: secondo terzo delle funzionalità.  
- Sottoprogetto 3: ultimo terzo delle funzionalità (le meno critiche e componenti condivisi).

## Stabilization phase
I program manager coordinano OEM e ISV e monitorano il feedback degli utenti. Gli sviluppatori completano debug e stabilizzazione. I tester replicano e isolano gli errori.

- **Internal testing**: test approfonditi interni all’azienda.
- **External testing**: test approfonditi da parte di beta tester, OEM, ISV e utenti finali.
- **Release preparation**: preparazione della versione finale (golden master) e della documentazione. 

# Strategie e Principi
**Strategia per definire prodotto e processo**: considerare la creatività come elemento fondamentale.

Principi:
1. Suddividere il progetto in 3 o 4 milestone.
2. Definire una visione del prodotto e una specifica funzionale che evolverà nel tempo.
3. Selezionare funzionalità e priorità basandosi sulle esigenze degli utenti.
4. Definire un’architettura modulare coerente con la struttura del prodotto.
5. Assegnare task piccoli e limitare le risorse.

**Strategia per sviluppo e consegna**: lavorare in parallelo con frequenti sincronizzazioni.

Principi:
1. Creare team paralleli e utilizzare daily build.
2. Avere sempre una versione consegnabile.
3. Utilizzare lo stesso linguaggio di programmazione per sito di sviluppo.
4. Testare continuamente il prodotto.
5. Utilizzare metriche per supportare le decisioni.

# Milestones
![[Milestone.png|center|600]]

# Modello del ciclo di sviluppo "synch and stabilize"
![[Ciclo_S&S.png|center|600]]

# Confronto tra synch-and-stabilize e waterfall
![[S&S_VS_Waterfall.png|center|600]]

# Il Modello Netscape
Anche Netscape adottò un modello di synchronize-and-stabilize, con adattamenti per browser e prodotti server.

Caratteristiche:
- Dimensione dello staff: in media 1 tester ogni 3 sviluppatori (produttività simile a Microsoft su prodotti comparabili).

Processo:
- Pianificazione limitata (eccetto prodotti server).
- Documentazione incompleta.
- Controllo limitato dell’avanzamento, basato sull’esperienza dei project manager.
- Scarso controllo sulle code review.
- Pochi dati storici per decisioni.

# Staffing
![[Staffing.png|center|600]]

# Netscape Development Process
**Step 1**: Raccolta requisiti e proposta di progetto**

- Si tiene un _Advance Planning Meeting (APM)_ per generare idee e discutere obiettivi (coinvolgendo marketing, sviluppo ed executive).
- Viene definita una prima visione del prodotto, inizialmente elaborata dagli ingegneri senior, poi principalmente dai product manager.
- Gli ingegneri iniziano attività preliminari di design e prototipazione per esplorare tecnologie alternative o nuove funzionalità.
- I product manager, con il supporto degli sviluppatori, redigono il documento dei requisiti.
- Gli ingegneri eseguono una revisione informale della specifica preliminare.
- Viene redatta una specifica funzionale da parte degli ingegneri, talvolta con l’aiuto dei product manager.
- Marketing e ingegneria compilano un piano iniziale di tempi e budget, che viene poi discusso informalmente con i dirigenti.
---
**Step 2: Prima revisione esecutiva**

- Gli executive valutano il documento dei requisiti, la pianificazione e la proposta di budget.
- Se necessario, il piano viene corretto e aggiornato.
---
**Step 3: Avvio della fase di sviluppo**

- Gli sviluppatori iniziano la progettazione e la codifica delle funzionalità previste, modificando l’architettura quando necessario.
- I componenti vengono integrati quotidianamente tramite _build_ continue.
- Si generano liste di bug e si avviano le prime attività di correzione.
---
**Step 4: Revisione esecutiva intermedia (se necessaria)**

- A questo punto la specifica funzionale dovrebbe essere completa.    
- Vengono eventualmente introdotte modifiche a metà percorso, sia nella specifica sia nella gestione delle risorse, ove necessario.
- Si coordinano eventuali dipendenze con altri prodotti o progetti.
- Lo sviluppo procede normalmente.
---
**Step 5: Prima release interna (alpha) – circa 6 settimane**

- Lo sviluppo viene momentaneamente sospeso. 
- Si esegue un ciclo intensivo di debug e test del codice esistente.
- La versione _alpha_ viene distribuita internamente per ottenere feedback (talvolta come _developer’s release_).
- Lo sviluppo riprende successivamente.
- Il feedback ricevuto viene integrato nel progetto.
- L’obiettivo delle funzionalità principali viene raggiunto (nei server questo requisito è particolarmente importante).
- È prevista circa una settimana per stabilizzare la versione _beta_.
---
**Step 6: Public beta 1 o field test 1 (circa sei settimane)**

- Si ripetono le attività di sviluppo e test già svolte nello Step 5. 
- Per i prodotti server si passa a _field test_ con un gruppo ristretto di clienti, invece delle classiche beta pubbliche.
---
**Step 7: Public beta 2 e 3 (ognuna dura circa sei settimane)**

- Si ripetono le attività di sviluppo e verifica come nello Step 5.    
- Avviene il _UI freeze_, cioè nessun cambiamento significativo all’interfaccia utente è più consentito.
- Lo stato _feature-complete_ è obbligatorio: tutte le funzionalità devono essere implementate, anche se sono ancora permesse piccole modifiche o rifiniture.
---
**Step 8: Code complete**

- Da questo momento non viene aggiunto nuovo codice, eccetto quello necessario per correggere bug.    
- Tutte le funzionalità sono considerate complete a livello implementativo.
---
**Step 9: Test finale e rilascio**

- Ultima fase di debugging e stabilizzazione della _release candidate_.    
- Incontri di certificazione con i dirigenti senior per approvare la decisione di rilascio.
- Preparazione della versione destinata alla produzione (_Release to Manufacturing - RTM_) e rilascio commerciale.
---
# Agile Methods
All’inizio degli anni 2000 si sviluppò una reazione ai processi troppo pianificati, considerati vincolanti.

Il termine **agile method** estende l’idea di sviluppo iterativo e incrementale includendo comunicazione intensa, feedback rapido e poche regole esterne.

## The Agile Manifesto (2001)

Definisce i valori agili.

> "Stiamo scoprendo modi migliori di sviluppare software…"

Valori:

- Individui e interazioni più dei processi e strumenti.
- Software funzionante più della documentazione completa.
- Collaborazione con il cliente più della negoziazione contrattuale.
- Risposta al cambiamento più del seguire un piano.

Sono inoltre definiti dodici principi agili.

## Scrum
Il metodo agile più diffuso.
![[Scrum.png|center|600]]

## Scrum Roles
- **Scrum master**: garantisce la corretta applicazione del metodo.
- **Product owner**: gestisce e prioritizza i requisiti nel product backlog.
- **Development team**: sviluppa il prodotto (design, coding, testing).

### Sprints
Gli sprint durano tipicamente 2–4 settimane.
Attività:

- **Sprint planning**: selezione elementi dal product backlog.
- **Daily Scrum**: meeting quotidiano di sincronizzazione.
- **Sprint review**: presentazione dell’incremento.
- **Sprint retrospective**: analisi e miglioramento del processo.

### Definition of Done
Il team definisce cosa significa che un’attività è completata.  
Requisiti tipici:

- Test sufficienti.
- Integrazione verificata.
- Documentazione adeguata.

### User Stories
Formato comune per descrivere requisiti nello sviluppo agile.
Template: **Come (ruolo), voglio (obiettivo) in modo da (beneficio)**.

Storie grandi che successivamente verranno splittate in piú storie piccole → **epic**.

# Capability Maturity Model (CMM)
Il **SEI** ha sviluppato un modello per valutare la maturità dei processi software di un’organizzazione.

Il modello utilizza un questionario e uno schema a **cinque livelli**.

## I 5 livelli del CMM
![[CMM_5lvl.png|center|600]]

## Key Process Areas
Ogni livello include alcune **KPA**, definite secondo:
- obiettivi;
- responsabilità;
- risorse;
- attività richieste;
- metodi di monitoraggio;
- metodi di verifica.

## CMM KPAs
![[CMM_KPA.png|center|600]]

## Statistiche a Febbraio 2000
Organizzazioni ai livelli più alti:

- USA (71):
	- 44 a Livello 4 (Oracle, NCR, Siemens Info Systems, IBM Global Services).
	- 27 a Livello 5 (Motorola, Lockeed-Martin, Boeing, Honeywell).

- Fuori USA (25):
	- 1 a Livello 4 in Australia.
	- 14 a Livello 4 in India.
	- 10 a Livello 5 in India. 

## Number of appraisals by country (06/15)
![[by_Country.png|center|600]]

## Trends (as of June 2015)
![[Trends.png|center|600]]