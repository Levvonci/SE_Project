È la serie di attività necessaria alla realizzazione del prodotto software nei tempi, con i costi e con le desiderate caratteristiche di qualità.

Nel suo contesto:
- Si applicano metodi, tecniche e strumenti.
- Si creano prodotti (sia intermedi che finali).
- Si stabilisce il controllo gestionale del progetto.
- Si garantisce la qualità.
- Si governano le modifiche.

# Fasi del processo

Si divide in **3 stadi** (**sviluppo**, **manutenzione**, **dismissione**). Nel primo stadio si possono riconoscere **due tipi di fasi**:

- **Fasi di definizione**: si occupano di "cosa" il software deve fornire. Si definiscono i requisiti e si producono le specifiche.
- **Fasi di produzione**: definiscono "come" realizzare quanto ottenuto con le fasi di definizione. Si progetta il software, si codifica, si integra e si rilascia al cliente.

Lo stadio di manutenzione è a supporto del software realizzato e prevede fasi di definizione e/o produzione al suo interno.

Durante ogni fase si procede ad effettuare il testing di quanto prodotto, mediante opportune tecniche di verifica e validazione (V&V) applicate sia ai prodotti intermedi che al prodotto finale.
# Tipi di manutenzione

Sono 4:

- **Manutenzione correttiva**: ha lo scopo di eliminare i difetti che producono guasti del software.
- **Manutenzione adattativa**: ha lo scopo di adattare il software ad eventuali cambiamenti a cui è sottoposto l'ambiente operativo per cui è stato sviluppato.
- **Manutenzione perfettiva**: ha lo scopo di estendere il software per accomodare funzionalità aggiuntive.
- **Manutenzione preventiva (o software reengineering)**: consiste nell'effettuare modifiche che rendano più semplici le correzioni, gli adattamenti e le migliorie.

# Definizione di ciclo di vita

È l'intervallo di tempo che intercorre tra l’istante in cui nasce l’esigenza di costruire un software e l’istante in cui esso viene dismesso.

Include le fasi di definizione dei requisiti, specifica, pianificazione, progetto preliminare,
progetto dettagliato, codifica, integrazione, testing, uso, manutenzione e dismissione.

Tali fasi possono sovrapporsi o essere eseguite in modo iterativo.
# Modelli di ciclo di vita

Sono le fasi attraverso cui il prodotto software progredisce e l'ordine con cui vanno eseguite, dalla definizione dei requisiti alla dismissione.

La scelta del modello dipende da:
1. natura dell'applicazione
2. maturità dell’organizzazione
3. metodi e tecnologie usate
4. eventuali vincoli dettati dal cliente.

L'assenza di un modello del ciclo di vita causa la modalità di sviluppo **build & fix**, dove il prodotto software viene sviluppato e successivamente rilavorato fino a soddisfare le necessità del cliente.
## Modello Build & Fix

![[Pasted image 20250516071913.png]]
## Modello Waterfall
![[Pasted image 20250516072302.png]]

Static verification: lettura e controllo della documentazione.
Dynamic verification: testing attraverso l'esecuzione del codice.
### V&V nel Waterfall

![[Pasted image 20250516072325.png]]

Il prodotto software non può essere certificato.
## Modello Rapid Prototyping

![[Pasted image 20250516072359.png]]

La differenza principale consiste nell'uso di un prototipo per definire i requisiti. Limita al massimo il numero di errori durante la raccolta dei requisiti che possono avere conseguenze disastrose per lo sviluppo del software. Attraverso il prototipo si possono fare verifiche e validazioni migliori rispetto ad un controllo visuale.
# Software Prototyping

The principal use is to help customers and developers understand the software requirements:

- **Requirements elicitation**: users can experiment with a prototype to see how the system supports their work.
- **Requirements validation**: the prototype can reveal errors and omissions in the requirements.

Prototyping can be considered as a risk reduction activity which reduces requirements risks.

**Benefits**:

- Clarifies misunderstandings between software users and developers.
- Identifies missing or confusing services.
- A working system is available early in the process.
- It may serve as a basis for deriving a software specification.
- It can support user training and product testing.
## Prototyping process

![[Pasted image 20250516112323.png]]

## Prototypes as specifications

- Some parts of the requirements (e.g. safety critical functions) may be impossible to prototype and so do not appear in the specification.
- An implementation has no legal standing as a contract.
- Non-functional requirements cannot be adequately tested in a software prototype.
## Throw-away prototyping

A practical implementation of the product is produced to help discover requirements problems and then discarded. The product is then developed using some other development process.

It's used to reduce requirements risk and is developed from an initial requirement, delivered for experiment then discarded.

The throw-away prototype should NOT be considered as a final product:

- Some characteristics may have been left out.
- There is no specification for long-term maintenance.
- The product will be poorly structured and difficult to maintain.
### Throw-away prototyping process

![[Pasted image 20250516113249.png]]
### Throw-away prototype delivery

Developers may be pressed to deliver a throw-away prototype as a final product, this is not recommended because:

- It may be impossible to tune the prototype to meet non functional requirements.
- The prototype is inevitably undocumented.
- The structure will be degraded through changes made during development.
- Normal organizational quality standards may not have been applied.
## Prototyping key points

- A prototype can be used to give end-users a concrete impression of the product’s capabilities.
- Prototyping is becoming increasingly used for product development where rapid development is essential.
- Throw-away prototyping is used to understand the product requirements.
- Rapid development of prototypes is essential. This may require leaving out functionality or relaxing non-functional constraints.
- Visual programming is an inherent part of most prototype development methods.

# Visual programming

Per creare prototipi in tempi rapidi si usano linguaggi visuali tipo il visual basic.

Scripting languages such as **Visual Basic** support visual programming where the prototype is
developed by creating a user interface from standard items and associating components with
these items.

A large library of components exists to support this type of development.

These may be tailored to suit the specific application requirements

Example:
![[Pasted image 20250516113735.png]]
## Problems with visual development

- Difficult to coordinate team-based development.
- No explicit software architecture.
- Complex dependencies between parts of the program can cause maintainability problems.


