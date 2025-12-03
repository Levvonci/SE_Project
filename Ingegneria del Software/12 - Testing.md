# Verifica e Validazione

Processo volto a garantire che un sistema software **conformi alle sue specifiche** e **soddisfi le esigenze dell'utente**.

- **Verifica (Verification):**  
    "**Stiamo costruendo il prodotto in modo corretto?**"  
    _Obiettivo:_ Accertare che il software sia sviluppato in conformità con le specifiche tecniche e i requisiti definiti.
- **Validazione (Validation):**  
    "**Stiamo costruendo il prodotto corretto?**"  
    _Obiettivo:_ Accertare che il software realizzato risponda effettivamente alle necessità e alle aspettative dell'utente finale.

## Tecniche di Verifica e Validazione (V&V)

1. Ispezione del Software (Software Inspection)
- **Focus:** Analisi delle **rappresentazioni statiche** del sistema (documenti, codice sorgente) per individuarne problemi, difetti o incongruenze.
- **Natura:** Tecnica **statica** (il sistema non viene eseguito).
- **Supporto:** Può essere integrata dall'analisi automatizzata di documenti e codice tramite strumenti dedicati (linter, analizzatori statici).

2. Test del Software (Software Testing)
- **Focus:** Esecuzione del prodotto software e osservazione del suo **comportamento dinamico** in risposta a input specifici.
- **Natura:** Tecnica **dinamica** (il sistema viene eseguito).
- **Metodo:** Il sistema viene eseguito utilizzando **dati di test**; il suo comportamento operativo (output, performance, stabilità) viene osservato e confrontato con i risultati attesi.

## Tipologie di Test

 1. Test di Validazione (Validation Testing)
- **Scopo:** Dimostrare che il sistema **soddisfa i requisiti utente** e le aspettative.
- **Successo:** Il sistema esegue correttamente i **casi di test di accettazione** definiti.
- **Domanda chiave:** "Il sistema fa ciò che l'utente si aspetta?"
    
 2. Test per la Rilevazione di Difetti (Defect Testing)
- **Scopo:** Scoprire **difetti, errori o malfunzionamenti** nel sistema.
- **Successo:** Il test **rivela la presenza** di uno o più difetti (un test che non trova errori _non_ è necessariamente "riuscito" nel suo scopo primario).
- **Domanda chiave:** "Dove si annidano gli errori nel sistema?"

3. Test Statistici (Statistical Testing)

- **Scopo:** Stimare l'**affidabilità** (reliability) del sistema in condizioni d'uso realistiche.
- **Metodo:** I dati di test sono progettati per **riflettere la frequenza** e la distribuzione degli input tipici dell'utente finale.
- **Risultato:** Fornisce una **misura probabilistica** (es. MTBF - Mean Time Between Failures) della prontezza operativa del sistema.

## Defect Testing

> **I test dimostrano la presenza, non l'assenza, di difetti.**

Ha come obiettivo quello di scoprire i bugall'interno dei programmi. Ha successo quando provoca un comportamento anomalo** nel programma, rivelando così un difetto sottostante

Si contrappone al **test di validazione**, il cui scopo è dimostrare che un sistema soddisfa i requisiti utente. Un test di validazione ha successo quando il sistema esegue correttamente i casi di test di accettazione forniti.

### Fasi del Defect Testing

![[Pasted image 20251202154426.png]]

1. Testing dei Componenti (Unit e Module Testing)
*   **Oggetto:** Test di singoli componenti software (unità o moduli).
*   **Responsabile:** Generalmente lo **sviluppatore** del componente stesso (fanno eccezione i sistemi critici, dove il test può essere indipendente).
*   **Base dei Test:** Derivata principalmente dall'**esperienza dello sviluppatore** e dalla conoscenza interna del codice.

 2. Testing di Integrazione (Sub-system e System Testing)
*   **Oggetto:** Test di gruppi di componenti integrati per formare un sottosistema o l'intero sistema.
*   **Responsabile:** Un **team di testing indipendente** dal team di sviluppo.
*   **Base dei Test:** Derivata dalla **specifica di sistema** (documenti di requisiti e design).

# Politiche di Testing

Criteri e linee guida che definiscono la strategia, l'approccio e le regole per pianificare, progettare, eseguire e valutare le attività di test all'interno di un progetto o di un'organizzazione

- Solo un **testing esaustivo** potrebbe dimostrare che un programma è privo di difetti. Tuttavia, il testing esaustivo è **impossibile** nella pratica.
- Il testing deve quindi basarsi su un **sottoinsieme** di tutti i possibili casi di test, selezionato secondo criteri (**policy**) che dovrebbero essere definiti dal **team di Verifica e Validazione (V&V)** e non dal team di sviluppo.
- I test dovrebbero **esercitare le capacità** (funzionalità) del sistema nel suo complesso, piuttosto che concentrarsi sui singoli componenti in isolamento.
- **Testare situazioni tipiche** (casi d'uso comuni) è generalmente più importante che testare esclusivamente i casi limite (_boundary value cases_).

# Casi di Test e Dati di Test

#### **Casi di Test (Test Cases)**

- **Definizione:** Coppie di **input** forniti al sistema e **output attesi** corrispondenti, presupponendo che il sistema operi in conformità alla sua specifica.
- **Generazione:** Solitamente creata **manualmente**, poiché è complesso derivare automaticamente l'output atteso da specifiche informali o non formali.
#### **Dati di Test (Test Data)**

- **Definizione:** Gli **input** specifici che sono stati progettati per testare il sistema.
- **Generazione:** Possono essere **generati automaticamente** (ad esempio, per test di carico, casuali o di mutazione).

# The Defect Testing Process
![[Pasted image 20251202155018.png]]
# Black-Box Testing

Un approccio al testing in cui il programma è considerato come una **"black box"**.

- **Origine dei Test:** I casi di test sono derivati dalla **specifica di sistema** (requisiti funzionali).
- **Procedura:** Il tester fornisce **input** al componente o al sistema e osserva gli **output** corrispondenti, senza conoscere la logica interna di implementazione.
- **Successo del Test:** Se gli output osservati **non corrispondono** a quelli specificati, il test ha rilevato con successo un problema nel software.
- **Sinonimo:** Chiamato anche **testing funzionale**, poiché il tester si concentra esclusivamente sulla **funzionalità** esterna, non sull'implementazione interna del software.

![[Pasted image 20251202155122.png]]

# Equivalence Partitioning
I dati di input e i risultati di output spesso ricadono in **classi diverse**, in cui tutti i membri di una classe sono correlati dal punto di vista funzionale.

Ogni classe costituisce una **partizione di equivalenza**: si presuppone che il programma si comporti in modo **equivalente** (o produca lo stesso tipo di elaborazione/errore) per ogni membro appartenente alla stessa partizione.

![[Pasted image 20251202155344.png]]

#### **Metodo di Applicazione**

1. **Partizionare** gli input e gli output del sistema in partizioni di equivalenza.
    - _Esempio:_ Se l'input è un intero a 5 cifre compreso tra 10.000 e 99.999, le partizioni di equivalenza sono:
        - `< 10.000`
        - `10.000 – 99.999` (valido)
        - `> 99.999`
2. **Scegliere i casi di test**:
    - **Ai confini** di ogni partizione (valori limite).
    - Un valore **valido** vicino al punto medio della partizione valida.
    - _Esempio dallo scenario sopra:_ `09999`, `10000`, `50000`, `99999`, `100000`
## Equivalence Partitions

![[Pasted image 20251202155415.png]]

# Search Routine Specification

# White-Box Testing

Chiamato anche **structural testing** (testing strutturale).

- **Origine dei Test:** I casi di test sono derivati dalla **struttura interna** (codice sorgente) del programma.
- **Approccio:** La conoscenza dettagliata dell'implementazione è utilizzata per identificare casi di test aggiuntivi, mirando a coprire elementi strutturali specifici.
- **Obiettivo Primario:** **Esercitare tutte le istruzioni** (o decisioni, percorsi di base) del programma. L'obiettivo non è testare tutte le possibili combinazioni di percorsi (che sarebbero troppe), ma garantire una copertura strutturale significativa.
# Path Testing

L'obiettivo del **path testing** è garantire che l'insieme dei casi di test sia tale che **ogni percorso** attraverso il programma (e quindi ogni sua istruzione) venga **eseguito almeno una volta**.

- **Complessità:** Il numero di percorsi in un programma è solitamente **proporzionale alla sua dimensione**. Quando i moduli vengono integrati in sistemi più ampi, diventa **impraticabile** utilizzare tecniche di path testing esaustivo. Pertanto, queste tecniche sono prevalentemente impiegate nelle fasi di **unit** o **module testing**.
- **Strumento Fondamentale:** Il punto di partenza per il path testing è un **grafo di flusso del programma** (_program flow graph_), dove:
    - I **nodi** rappresentano le decisioni del programma (es. istruzioni `if`, `while`).
    - Gli **archi** rappresentano il **flusso di controllo** tra un'istruzione e l'altra.

# Integration Testing
I test di integrazione riguardano sistemi completi o sottosistemi composti da componenti integrate. Questi test dovrebbero essere di tipo **black-box** con casi di test derivati dalla specifica del sistema. La principale difficoltà risiede nella **localizzazione degli errori**, problema che può essere attenuato mediante un approccio incrementale.

## Incremental Integration Testing
L'integrazione incrementale riduce la complessità della localizzazione degli errori. Vengono definite sequenze di test progressivi in cui i componenti vengono integrati gradualmente:
![[Int_Test.png]]

## Approcci all'Integration Testing
### Top-Down Testing
Si inizia dal sistema di alto livello e si integra procedendo dall'alto verso il basso, sostituendo i singoli componenti con **stub** quando appropriato. Gli **stub** sono componenti fittizie che simulano il comportamento dei componenti non ancora implementati.

**Vantaggi:**
- Validazione dell'architettura del sistema fin dalle prime fasi.
- Possibilità di dimostrare il sistema in modo limitato già in fase iniziale.

**Sfide**:
- Osservazione dei test può richiedere codice aggiuntivo.

![[TopDown_Testing.png]]

### Bottom-Up Testing
Si integrano i singoli componenti in livelli fino a creare il sistema completo. Ogni livello viene testato utilizzando driver di test che simulano i componenti di livello superiore.

**Vantaggi:**
- Implementazione del test spesso più semplice.
- Locale per il controllo dei componenti di base.

**Sfide:**
- Validazione dell'architettura più difficile.
- Nessuna dimostrazione anticipata del sistema.

![[BottomUp_Testing.png]]

## Testing Approaches
| Aspetto                    | Top-Down                                            | Bottom-Up                             |
| -------------------------- | --------------------------------------------------- | ------------------------------------- |
| Validazione Architetturale | Migliore nel scoprire errori dell'architettura      | Meno efficace per l'architettura      |
| Dimostrazione di Sistema   | Consente dimostrazioni limitate in fase iniziale    | Dimostrazioni solo nella fase finale  |
| Implementazione Test       | Può richiedere codice aggiuntivo per l'osservazione | Spesso più semplice da implementare   |
| Osservazione Test          | Problematica, richiede infrastruttura aggiuntiva    | Problematica, richiede driver di test |

# Interface testing
Quando moduli o sottosistemi vengono integrati per creare sistemi più grandi, è fondamentale testare le interfacce. Gli obiettivi sono rilevare difetti dovuti a errori di interfaccia o assunzioni non valide riguardanti le interfacce. Questo è particolarmente importante nello sviluppo orientato agli oggetti, dove gli oggetti sono definiti dalle loro interfacce.

![[Interface_Testing.png]]

## Interfaces Types
- **Interfacce di parametro:** Dati passati da una procedura a un'altra
- **Interfacce di memoria condivisa**: Un blocco di memoria è condiviso tra procedure
- **Interfacce procedurali:** Un sottosistema incapsula un insieme di procedure che possono essere richiamate da altri sottosistemi
- **Interfacce di passaggio di messaggi:** I sottosistemi richiedono servizi da altri sottosistemi attraverso il passaggio di messaggi

## Interface Errors
- **Uso errato dell'interfaccia:** Un componente chiamante chiama un altro componente e commette un errore nel suo utilizzo, come parametri in ordine sbagliato, di tipo errato o in numero errato.
- **Fraintendimento dell'interfaccia:** Un componente chiamante incorpora assunzioni errate sul comportamento del componente chiamato.
- **Errori di tempistica:** Il componente chiamato e il componente chiamante operano a velocità diverse e vengono accesse informazioni obsolete.

## Interface testing guidelines
- Progettare test in modo che i parametri di una procedura chiamata siano agli estremi dei loro intervalli.
- Testare sempre i parametri puntatore con puntatori nulli.
- Progettare test che causino il fallimento del componente.
- Utilizzare stress testing nei sistemi di passaggio di messaggi.
- Nei sistemi di memoria condivisa, variare l'ordine di attivazione dei componenti.

# Stress testing
Lo stress testing esercita il sistema oltre il suo carico di progettazione massimo. Sottoporre a stress il sistema spesso fa emergere difetti. Lo stress testing verifica il comportamento di fallimento: i sistemi non dovrebbero fallire catastroficamente e il fallimento non dovrebbe causare una perdita inaccettabile di servizio o dati.

Questo approccio è particolarmente rilevante per i sistemi distribuiti, che possono mostrare un degrado grave quando la rete si sovraccarica.

# Object-Oriented Testing
Nello sviluppo orientato agli oggetti, i componenti da testare sono classi di oggetti che vengono istanziate come oggetti. Poiché sono granularità più grandi rispetto alle singole funzioni, gli approcci ai test white-box devono essere estesi. Inoltre, non c'è un ovvio "top" del sistema per l'integrazione e il test top-down.

## Testing Levels
- Testing di metodi associati agli oggetti.
- Testing di classi di oggetti.
- Testing di cluster di oggetti cooperanti.
- Testing del sistema OO completo.

# Object Class Testing
La copertura completa del test di una classe comporta:

- Testare tutte le operazioni associate all'oggetto
- Impostare e interrogare tutti gli attributi dell'oggetto
- Esercitare l'oggetto in tutti i possibili stati

L'ereditarietà complica la progettazione dei test di classe di oggetto, poiché le informazioni da testare non sono localizzate in un'unica classe.

## Weather station class and state diagram
![[Weather_Station.png]]

I **diagrammi di stato** identificano le transizioni di stato per il testing. Ad esempio, per una stazione meteo si potrebbero testare sequenze come:

- Da Shutdown a Waiting a Shutdown.
- Da Waiting a Calibrating a Testing a Transmitting a Waiting.
- Da Waiting a Collecting a Waiting a Summarising a Transmitting a Waiting.

## Object Integration
I livelli di integrazione sono meno distinti nei sistemi orientati agli oggetti. Il cluster testing riguarda l'integrazione e il test di cluster di oggetti cooperanti, identificati utilizzando la conoscenza del funzionamento degli oggetti e delle caratteristiche del sistema implementate da questi cluster.

### Approaches to cluster testing
- **Test basato su casi d'uso o scenari:** Il testing si basa sull'interazione dell'utente con il sistema, testando le caratteristiche del sistema come sperimentate dagli utenti
- **Thread testing:** Testa la risposta del sistema agli eventi come thread di elaborazione attraverso il sistema
- **Test di interazione tra oggetti:** Testa sequenze di interazioni tra oggetti che si fermano quando un'operazione di un oggetto non richiama servizi da un altro oggetto

### Scenario-Based testing
Per il test basato su scenario si identificano scenari dai casi d'uso e si integrano con diagrammi di interazione che mostrano gli oggetti coinvolti nello scenario (ad esempio diagrammi di sequenza).
![[Weather_Data.png]]

# Testing Workbenches
Il testing è una fase costosa del processo di sviluppo. I workbench di test forniscono una gamma di strumenti per ridurre il tempo richiesto e i costi totali di test. La maggior parte dei workbench di test sono sistemi aperti perché le esigenze di testing sono specifiche dell'organizzazione.

## Esempio
![[Workbench_Testing.png]]
