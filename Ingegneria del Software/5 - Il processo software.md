# Il Modello Microsoft

Organizzazioni che sviluppano software commerciale, hanno dovuto affrontare, fin dalla metà degli anni 80, problemi di:

- Incremento della qualità dei prodotti software.
- Riduzione di tempi e costi di sviluppo

Per cercare di risolvere tali problemi si è adottato un processo che è **iterativo**, **incrementale** e **concorrente** e che permette di esaltare le doti di creatività delle persone coinvolte nello sviluppo di prodotti software.
# Approccio Synch & Stabilize

Approccio usato attualmente da Microsoft, si basa su:

- **Sincronizzazione giornaliera** del lavoro di persone singole o piccoli team, mediante assemblaggio dei componenti software completi o parziali in una **daily build** che viene testato e corretto.
- **Stabilizzazione** periodica del prodotto in vari **milestone**  durante lo sviluppo del progetto, piuttosto che un'unica volta alla fine.
# Ciclo di sviluppo a 3 fasi
Per quanto riguarda il ciclo di sviluppo è diviso in 3 fasi:

- **Planning phase**: Define product vision, specification and schedule.
- **Development phase**: Feature development in 3/4 sequential sub-projects, each resulting in a milestone release.
- **Stabilization phase**: Comprehensive internal and external testing, final product, stabilization and ship.
## Planning phase

- **Vision statement**: Product and program management use extensive customer input to identify and priority-order product features.
- **Specification document**: Based on vision statement, program management and development group define feature functionality, architectural issues, and component interdependencies.
- **Schedule and Feature Team Formation**: Based on specification document, program management coordinates schedule and arranges feature teams that each contain approximately 1 program manager, 3-8 developers, and 3-8 testers (who work in parallel 1:1 with developers).
## Development phase

Program managers coordinate evolution of specification. Developers design, code, and debug. Testers pair with developers for continuous testing.

- Subproject 1: first 1/3 of the features (Most critical features and shared components).
- Subproject 2: second 1/3 of the features.
- Subproject 3: final 1/3 of the features (Least critical features and shared components).
## Stabilization phase

Program managers coordinate OEMs and ISVs and monitor customer feedback. Developers perform final debugging and code stabilization. Testers recreate and isolate errors.

- **Internal testing**: Thorough testing of the complete product within the company.
- **External testing**: Thorough testing of the complete product outside the company by "beta" sites, such as OEMs, ISVs, and end users.
- **Release preparation**: Prepare final release of "golden master" disks and documentation for manufacturing.
# Strategie e Principi

**Strategia per definire prodotto e processo**: "considerare la creatività come elemento essenziale".

Principi di realizzazione:

1. Dividere il progetto in 3 o 4 milestone.
2. Definire una "product vision" e produrre una specifica funzionale che evolverà durante il progetto.
3. Selezionare le funzionalità e le relative priorità in base alle necessità utente.
4. Definire un'architettura modulare per replicare nel progetto la struttura del prodotto.
5. Assegnare task elementari e limitare le risorse.

**Strategia per lo sviluppo e la consegna dei prodotti**: "lavorare in parallelo con frequenti
sincronizzazioni".

Principi di realizzazione:

1. Definire team paralleli ed utilizzare daily build per la sincronizzazione.
2. Avere sempre un prodotto da consegnare, con versioni per ogni piattaforma e mercato.
3. Usare lo stesso linguaggio di programmazione all'interno dello stesso sito di sviluppo.
4. Testare continuamente il prodotto durante il suo sviluppo.
5. Usare metriche per il supporto alle decisioni.

Esempio di metriche collezionate:
![[Pasted image 20250517122407.png]]

# Milestones

![[Pasted image 20250517122431.png]]

# Modello del ciclo di sviluppo "synch and stabilize"

![[Pasted image 20250517122513.png]]

# Confronto tra modelli synch-and-stabilize e waterfall

![[Pasted image 20250517122542.png]]

# Il Modello Netscape

Anche Netscape ha adottato un modello di  synchronize-and-stabilize, con adattamenti per sviluppo di browser e prodotti server:

Dimensione dello staff: in media 1 tester ogni 3 sviluppatori (ma stessa produttività di Microsoft nello sviluppo di prodotti comparabili, ad es. IE vs. Communicator).

Processo
- scarso effort di pianificazione (tranne che su prodotti server).
- documentazione incompleta.
- scarso controllo sullo stato di avanzamento del progetto (lasciato all’esperienza e all’influenza dei project manager).
- scarso controllo su attività di ispezione del codice (code review).
- pochi dati storici per il supporto alle decisioni.

# Staffing

![[Pasted image 20250517122837.png]]

# Netscape Development Process

![[Pasted image 20250517122858.png]]

![[Pasted image 20250517122914.png]]

![[Pasted image 20250517122924.png]]
# Agile Methods

In the early 2000’s, there was a reaction against the importance of carefully planned
software processes, stating that such processes are too restrictive on the developers.

The term **agile method** was introduced to extend the original concept of iterative and incremental development to concepts such as intensive communication within the project, fast feedback, few external rules for the way of working, etc.
## The Agile Manifesto (2001)

It defines **agile values**.

“We are uncovering better ways of developing software by doing it and helping others do it. Through this work we have come to value:

- Individuals and interactions over processes and tools.
- Working software over comprehensive documentation.
- Customer collaboration over contract negotiation.
- Responding to change over following a plan.
- That is, while there is value in the items on the right, we value the items on the left more.”

In addition to values, the Agile Manifesto contains the twelve agile principles that provide additional guidance on the use of agile methods.

Together, these values and principles define the basic concepts that are today known as **agile development**.

## Scrum

Il metodo agile più famoso è il metodo SCRUM

![[Pasted image 20250517131926.png]]
## Scrum Roles

- **The Scrum master**: ensures that the methodology is understood and properly implemented by the development team and the product owner. He also supports the team by helping everyone else to interact with the team according to the Scrum rules.
- **The product owner**: manages and helps prioritizing the requirements to be implemented as documented in the product backlog.
- **The development team**: is responsible for developing the product, including all relevant tasks (e.g., designing, coding and testing).

### Sprints

Concetto fondamentale dello Scrum.

A **sprint** is carried out to deliver a new increment of working software, and typically takes 2 to 4 weeks. It is started with the **sprint planning** meeting where the Scrum team transfers the items to be developed from the product backlog into the sprint backlog.

During the sprint, the development team works on the increment, with short **daily Scrum** meetings (aka stand-up meeting) of the development team to synchronize work and address any problems.

At the end of a sprint, the increment is presented to the product owner and other stakeholders in a **sprint review**. 

Finally, the **sprint retrospective** meeting is performed to identify and plan any improvements for the next sprint.

### Definition of Done

Scrum requires the development team defines for itself what it means for a work item to be done (i.e., before it is allowed to be integrated into the main branch).

Typical minimum requirements included in this “definition of done” include an adequate number
of test cases, as well as checking the integration of the new code to ensure that it does not break
the main development branch.

The definition of done also requires that the code has been documented adequately, where the
team defines for itself what ”adequate” means.

### User Stories

A common practice, used in agile development, often in combination with Scrum (but not defined
in the Scrum Guide). 

A user story is a format for describing user requirements as a “story”. Is should be short, typically just one sentence, and described from the user point of view.

It uses a common template, such as As a **(role), I want (goal) so that (benefit)**.

Example: “As a process engineer, I want to see the dependencies between different process steps so that I can easily verify and validate them”.

Large user stories which are later broken down into smaller ones are often called **epics**.
# Capability Maturity Model (CMM)

ll **SEI** (**Software Engineering Institute**) ha predisposto un modello per determinare il livello di maturità del processo software di un'organizzazione (ovvero un indice dell'efficacia nell'applicare tecniche di ingegneria del software).

Il modello è basato su un questionario ed uno **schema valutativo a cinque livelli**.

Ogni livello comprende tutte le caratteristiche definite per il livello precedente.
## I 5 livelli del CMM

![[Pasted image 20250517134930.png]]
## Key Process Areas

Il CMM associa a ogni livello di maturità alcune **KPA** (Key Process Area), tra le 18 definite, che descrivono le funzioni che devono essere presenti per garantire l'appartenenza ad un certo livello.

Ogni KPA è descritta rispetto a:

- obiettivi.
- impegni e responsabilità da assumere.
- capacità e risorse necessarie per la realizzazione.
- attività da realizzare.
- metodi di "monitoring" della realizzazione.
- metodi di verifica della realizzazione

## CMM KPAs

![[Pasted image 20250517135055.png]]
## Statistiche a Febbraio 2000

La lista delle organizzazioni a livello 4 e 5 (maturità elevata) include:

71 organizzazioni negli USA:
- 44 organizzazioni a Livello 4 (tra cui Oracle, NCR, Siemens Info Systems, IBM Global Services).
- 27 organizzazioni a Livello 5 (tra cui Motorola, Lockeed-Martin, Boeing, Honeywell).

25 organizzazioni al di fuori degli USA:
- 1 organizzazione a Livello 4 in Australia.
- 14 organizzazioni a Livello 4 in India.
- 10 organizzazioni a Livello 5 in India.

## Number of appraisals by country (06/15)

![[Pasted image 20250517135244.png]]

## Trends (as of June 2015)

![[Pasted image 20250517135304.png]]
