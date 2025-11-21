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