# Introduzione
La progettazione di software orientato agli oggetti é un'attivitá complessa.
Uno dei compiti piú difficili per un progettista é di individuare:
- Un insieme di oggetti ben definiti,
- Riusabili il piú possibili,
- Con relazioni e gerarchie chiare ed efficaci.

# Una lezione da imparare
>“Ogni pattern descrive un problema ricorrente nel nostro ambiente e ne propone il nucleo della soluzione, così che possa essere riutilizzata infinite volte, senza applicarla mai nello stesso modo.”
 — *Christopher Alexander*

# Design Pattern: Caratteristiche
- Offrono soluzioni a problemi che ritornano spesso nello sviluppo del software.
- Capitalizzano l'esperienza della progettazione OO e favoriscono il riuso.
- Evitano di reinventare soluzioni giá note.
- Creano un linguaggio condiviso tra sviluppatori.
- Spingono verso un codice strutturato in modo corretto.
- Non sono soluzioni universali: non risolvono qualsiasi problema

>[!riferimenti bibliografici]
>Gamma, Helm, Johnson, Vlissides — Design Patterns (GoF)
>Craig Larman — Applicare UML e i Pattern

# Classificazione
## Classificazione per scopo
I pattern si distinguono in tre categorie principali:
- **Creazionali:** Riguardano la creazione degli oggetti.
- **Strutturali:** Si concentrano sull'organizzazione di classi e oggetti
- **Comportamentali:** Descrivono come gli oggetti interagiscono e come si distribuiscono le responsabilitá

## Classificazione per Raggio d'Azione
- **A livello di classi:** Relazioni statistiche basate sull'ereditarietá, note a compile-time
- **A livello di oggetti:** Relazioni dinamiche che possono cambiare a runtime

## Catalogo GoF
Elenco dei 23 deign pattern definiti dal GoF

1. Adapter
2. Façade
3. Composite
4. Decorator
5. Bridge
6. Singleton
7. Proxy
8. Flyweight
9. Strategy
10. State
11. Command
12. Observer
13. Memento
14. Interpreter
15. Iterator
16. Visitor
17. Mediator
18. Template Method
19. Chain of Responsibility
20. Builder
21. Prototype
22. Factory Method
23. Abstract Factory

### Classificazione Completa
![[IMG_lvnc/Classificazione_Completa.png]]

# Descrizione dei design pattern
- Nome e Classificazione: Il nome illustra l'essenza di un pattern; la classificazione lo identifica in termini di scopo e raggio d'azione.
- Motivazione: Scenario che descrive in modo astratto il problema al quale applicare il pattern.
- Applicabilità: Applicazioni del pattern.
- Struttura: Descrive graficamente la configurazione di elementi che risolvono il roproblema.
- Partecipanti: Classi ed oggetti che fanno parte del pattern.
- Conseguenze: Risultati dopo l'applicazione del pattern.
- Implementazione: Tecniche e suggerimenti per applicare il pattern.
- Codice di esempio: Frammenti di codice che illustrano come implementare in un certo linguaggio di programmazione il pattern.
- Usi noti: Esempi di applicazioni in sistemi reali.
- Pattern collegati: Altri pattern.

# Framework
Un framework non é una semplice libreria; rappresenta il design riutilizzabile di una intera porzione di sistema.

## Caratteristiche principali
- Definiscono lo scheletro dell'applicazione
- Permettono il riuso del codice e del design
- Sono basati su classi astratte, che fungono da modello per implementazioni specifiche;
- Molti pattern costituiscono i "Mattoni" fondamentali dei framework.

# Abstract Factory
- **Scopo:** Fornire un'interfaccia per creare famiglie di oggetti correlati, senza specificare le concrete classi da usare.

>**Esempio:**
>Generazione di UI con look&feel differenti
>+ Look&Feel1 -> Window1 e ScrollBar1
>+ Look&Feel2 -> Window2 e ScrollBar2

Usiamo una **Abstract Factory:**
![[IMG_lvnc/Ab_Factory.png]]

Struttura della **Abstract Factory:**
![[IMG_lvnc/Ab_Factory_Struttura.png]]

## Vantaggi
- Isolamento delle classi complete.
- Facile sostituzione dell'intera famiglia dei prodotti.

## Svantaggi
- Aggiungere nuove famiglie richiede modifiche all'interfaccia della factory.

# Factory method
**Scopo:** Definire un metodo che rimanda alle sottoclassi la decisione su quale oggetto istanziare.
**Tipico nei framework:**
- La classe astratta fornisce il flusso operativo.
- Le sottoclassi decidono cosa creare
**Benefici:** disaccoppia il codice dal tipo concreto degli oggetti.

>**Esempio:**
>Si consideri un framework di gestione di documenti di tipo diverso
>Le due astrazioni chiave sono Application e Document
>Gli utilizzatori devono definire delle sottoclassi per ottenere delle implementazioni adatte all'applicazione specifica.
>Application contiene la logica per sapere quando un nuovo documento sará creato, ma non per sapere quale tipo di documento creare.
>Il Pattern Factory incapsula la conoscenza della specifica classe da creare al di fuori del framework
![[IMG_lvnc/Factory_Method_es.png]]

## Struttura
![[IMG_lvnc/Factory_Method_Struttura.png]]

# Adapter
**Scopo:** Convertire l'interfaccia di una classe esistente incompatibile con un client, in una compatibile.

>**Esempio:**
>Supponiamo di voler integrare il componente Circle nell'editor che giá supporta le forme Triangle e Rectangle
![[IMG_lvnc/Adapter_Ex1.png]]

>Soluzione_1: Object Adapter
![[IMG_lvnc/Adapter_Ex1.png]]

>Class Adapter
![[IMG_lvnc/Adapter_Ex2.png]]

>Struttura:
![[IMG_lvnc/Adapter_Struttura.png]]

- **Object Adapter:** Usa la composizione.
- **Class Adapter:** Usa l'ereditarietá multipla.

# Composite
**Scopo:** Trattare oggetti semplici e strutture composte in maniera uniforme.

>**Esempio:**
>Consideriamo un editor grafico in grado di gestire forme elementari e figure composte. Gli oggetti elementari e quelli composti devono essere trattati in modo uniforme
![[IMG_lvnc/Composite_Ex1.png]]

>**Struttura:**
![[IMG_lvnc/Composite_Struttura.png]]

- Component (interfaccia comune),
- Leaf (oggetti semplici),
- Composite (oggetti composti).

## Vantaggi
- Semplifica il codice client,
- Facilita l’aggiunta di nuove forme.

## Svantaggi:
- Il sistema può risultare troppo generico.

# Decorator

Ha lo scopo di aggiungere dinamicamente delle funzionalità ad un oggetto senza modificarne la classe. Un esempio di applicazione è la realizzazione di interfacce utente, in cui funzionalità come lo scorrimento del testo o un bordo devono essere aggiunti a livello di singolo oggetto.

![[Pasted image 20251202170526.png]]

Il **decorator** è un oggetto contenitore che racchiude un oggetto elementare e aggiunge una particolare responsabilità. Il **decorator** trasferisce le richieste all'oggetto decorato ma può svolgere funzioni aggiuntive prima o dopo il trasferimento della richiesta.

Si applica quando è necessario aggiungere agli oggetti funzionalità a _runtime_ e quando il subclassing non è adatto (provocherebbe l'esplosione di sottoclassi per ogni funzionalità).

![[Pasted image 20251202171317.png]]

# Observer

Ha lo scopo di definire una dipendenza **uno a molti** tra oggetti. Quando più oggetti dipendono dallo stato di un altro oggetto, bisogna assicurarsi che questi oggetti si aggiornino automaticamente.

È necessario quando un oggetto (detto **Subject** o **Observable**) deve informare automaticamente altri oggetti (**Observer**) ogni volta che cambia stato.

Una possibile (errata) soluzione è quella di utilizzare attributi o metodi pubblici nell'oggetto osservato che leggono il valore di un attributo protetto. Non è una buona soluzione perché:

- non è scalabile (l'aumento di osservatori sovraccaricherebbe l'oggetto osservato di richieste)
    
- gli osservatori devono continuamente interrogare l'oggetto
    

Il pattern Observer prevede che gli osservatori si registrino presso l'oggetto osservato. In questo modo l'oggetto osservato notifica ogni cambiamento agli osservatori. Quando l'osservatore rileva la notifica può interrogare l'oggetto osservato o svolgere operazioni indipendenti dallo stato dell'osservato.

![[Pasted image 20251202172706.png]]

![[Pasted image 20251202172720.png]]

Si applica quando una azione può essere scomposta in due ambiti, ciascuno incapsulato in oggetti separati e quando bisogna gestire le modifiche di oggetti in seguito alla variazione di un altro oggetto.

L'accoppiamento tra **subject** e **observer** è astratto, il subject conosce solo la lista degli osservatori e la _notifica_ avviene in modalità broadcast, quindi il subject non si occupa di quanti sono gli observer registrati.

# Template Method

Ha lo scopo di definire la struttura di un algoritmo, delegando alle sottoclassi l'implementazione di passaggi specifici.

La classe base decide come è organizzato l'algoritmo Le sottoclassi decidono come implementare i passaggi variabili

Si usa:

- quando implementiamo algoritmi che condividono la stessa struttura ma differiscono in alcuni dettagli
    
- quando si vuole evitare duplicazioni di passaggi perché ci sono comportamenti comuni (vengono inseriti nel template)
    

![[Pasted image 20251202174049.png]]

La classe base (_AbstractClass_) contiene:

- templateMethod: definisce la sequenza di passi dell'algoritmo
    
- metodi astratti che le sottoclassi devono implementare
    
- metodi hook che hanno un comportamento standard, ma le sottoclassi possono anche ridefinire Il template Method crea una struttura di controllo invertito dove è la classe padre che richiama le operazioni ridefinite nelle sottoclassi.
    

Simile al factory method perché invoca metodi astratti tramite interfaccia e l'implementazione dei metodi rimandata a classi concrete.

Si utilizzano però in problemi diversi:

- il template method è il metodo che invoca i metodi astratti per generalizzare un algoritmo
    
- il factory method è un metodo astratto che deve creare e restituire l'istanza di classe concreta per sganciare il cliente dalla scelta del tipo specifico
    

# Strategy

Ha lo scopo di definire ed incapsulare una famiglia di algoritmi in modo da renderli intercambiabili indipendentemente dal client che li usa.

Pensiamo alla classe degli algoritmi di ordinamento, in cui ne esistono diversi (BucketSort, QuickSort ecc). Costruiamo un'applicazione che li supporti tutti e che permette una scelta rapida dell'algoritmo.

Molte classi differiscono solo per il comportamento. Il pattern **strategy** offre un modo per avere un interfaccia comune. Questo pattern è applicabile quando sono necessarie più varianti di uno stesso algoritmo, in base al tipo di dato in ingresso o a delle condizioni operative.

La strategy elimina i blocchi condizionali necessari se tutti i comportamenti fossero in un unica classe, ma i client devono conoscere le diverse strategie.

![[Pasted image 20251202181908.png]]
