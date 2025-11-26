Il **Requirement Engineering** varia in base al dominio applicativo, alle persone coinvolte ed all'organizzazione che sviluppa il sistema software.

Esistono però delle attività comuni a tutti i processi:

1. **Studio di fattibilità** (feasibility study) è l'unica fase opzionale.
2. **Identificazione e analisi dei requisiti** (req. elicitation and analysis).
3. **Specifica dei requisiti** (req. specification).
4. **Convalida dei requisiti** (req. validation).
5. **Gestione dei requisiti** (req. management).
# Studio di fattibilità

È una **descrizione sommaria** del sistema software e delle necessità utente. Le informazioni vengono raccolte attraverso **colloqui** con:

- Client manager.
- Ingegneri del software con esperienza nello specifico dominio applicativo.
- Esperti delle tecnologie da utilizzare.
- Utenti finali del sistema.
## Report di fattibilità

Prodotto dallo studio di fattibilità, il report stabilisce l'opportunità o meno di procedere allo sviluppo del sistema software.

Domande tipiche dello studio di fattibilità:

1. In che termini il sistema software contribuisce al raggiungimento degli **obiettivi strategici** del cliente?
2. Può il sistema software essere sviluppato usando le **tecnologie** correnti e rispettando i **vincoli** di durata e costo complessivo?
3. Può il sistema software essere **integrato** con altri sistemi già in uso?

# Identificazione e Analisi dei Requisiti

Il team di sviluppo incontra il cliente e gli utenti finali al fine di identificare i requisiti utente, dalla cui analisi si generano i requisiti di sistema (specifiche). Questo processo coinvolge tipicamente personale di vari ruoli sia all'interno dell'organizzazione del cliente che in altre organizzazioni o tra gli utenti finali.

**Stakeholders**: sono coloro che hanno un interesse diretto o indiretto sui requisiti del sistema software da sviluppare.

**Task**:

1. **Comprensione del dominio**: l'analista deve comprendere il dominio applicativo (es. se il sistema software deve supportare un ufficio postale, l'analista deve comprendere il funzionamento di un ufficio postale).
2. **Raccolta dei requisiti**: mediante interazione con gli stakeholder si identificano i requisiti utente.
3. **Classificazione**: l'insieme dei requisiti raccolti viene suddiviso in sotto-insiemi coerenti di requisititi.
4. **Risoluzione dei conflitti**: eventuali contraddizioni e/o conflitti tra requisiti vanno identificati e risolti.
5. **Assegnazione delle priorità**: mediante interazione con gli stakeholder, ad ogni requisito o sotto-insiemi di requisiti va assegnata una classe di priorità.
6. **Verifica dei requisiti**: i requisiti vengono controllati per verificarne completezza e consistenza, in accordo a quanto richiesto dagli stakeholder.

## Tecniche di identificazione dei requisiti

- **Etnografia**: Osservazione di quello che succede nel dominio applicativo.
- **Casi d'uso**: basati su scenari reali.
- **Prototipazione**.

## Tecniche di analisi (e specifica) dei requisiti:

Si dividono in:
- **Semi-formali**: basate su modelli del sistema e usate dai metodi di analisi strutturata o analisi orientata agli oggetti.
- **Formali**: basate su Petri Net, FSM, Z, ecc.
# Convalida dei Requisiti

La convalida dei requisiti ha l'obiettivo di controllare che il documento dei requisiti, ottenuto dalla fase di analisi, descriva accuratamente il sistema software che il cliente si aspetta. Scoprire gli errori in questa fase è fondamentale per evitare modifiche costose in fasi successive.

Alcuni controlli da effettuare:

1. Validità:
2. Consistenza:
3. Completezza:
4. Realizzabilità:
5. Verificabilità:

Tecniche di convalida dei requisiti:

- **Revisioni informali**: basate sul peer-review. Esempio 1 tester per X sviluppatori.
- **Revisioni formali**:
	- **Walkthrough**: si percorre l'intero documento in maniera organizzata per individuare punti deboli, solitamente attraverso delle riunioni.
	- **Ispezioni**:
- **Prototipazione**.
- **Generazione dei test-case**.
- **Analisi di consistenza automatizzata**: per requisiti formali.

# Gestione dei Requisiti.

Consiste nell'**identificazione e controllo delle modifiche** che i requisiti ricevono durante la vita del software. I requisiti possono essere classificati in base alla loro evoluzione come:

- **Requisiti stabili**: se hanno bassa probabilità di essere modificati nel tempo.
- **Requisiti volatili**: se hanno alta probabilità di essere modificati nel tempo, si dividono in:
	- **Mutabili**: se le modifiche sono legate a cambiamenti nell'ambiente operativo.
	- **Emergenti**: se le modifiche sono causate da una migliore comprensione del sistema software.
	- **Consequenziali**: se le modifiche sono legate all'introduzione di sistemi informatici nel flusso di lavoro.
	- **Di Compatibilità**: se le modifiche sono legate a cambiamenti nei sistemi e nei processi aziendali.
## Gestione delle modifiche di requisiti

Le modifiche dei requisiti vanno pianificate mediante:

1. **Identificazione univoca dei requisiti**.
2. **Gestione delle modifiche**: con
	- Analisi dei costi.
	- Analisi dell'impatto.
	- Analisi della realizzazione.
3. **Tracciabilità**: relazioni tra requisiti e tra requisiti e progetto del sistema software.
4. **Uso di tool CASE** per il supporto alle modifiche.
# Specifiche Formali vs. Informali

![[Pasted image 20251121150804.png]]

# Specifiche Formali con Petri Net

Sono usate in ambito di ingegneria delle comunicazioni. 

![[Pasted image 20251121151132.png]]

## Marked Petri Net 

![[Pasted image 20251121151215.png]]

after firing transition $t_1$:

![[Pasted image 20251121151249.png]]

after firing transition $t_2$:

![[Pasted image 20251121151318.png]]

## Esempio

![[Pasted image 20251121151351.png]]

# Specifiche Formali con Finite State Machine (FSM)

![[Pasted image 20251121151448.png]]
# Specifiche Formali con linguaggio Z

Consiste di un set di schemi, ogni schema Z ha il seguente formato:

![[Pasted image 20251121151535.png]]
## Esempio di Specifica di Stato

![[Pasted image 20251121151610.png]]

## Esempio di Specifica di Operazione

![[Pasted image 20251121151647.png]]

# Spec. Semi-Formali: Modelli del Sistema

Un modello del sistema è una **rappresentazione astratta del sistema** ottenuta attraverso linguaggi visuali (**UML**) che facilita la comprensione delle proprietà e del  funzionamento del sistema, prima che esso venga costruito.

L'uso di modelli nei sistemi software è formalizzato all'interno dei metodi di analisi dei requisiti del software che fanno uso di tecniche semi-formali.

I metodi di analisi dei requisiti software sono di due tipi:

1. **Metodi di analisi strutturata (o procedurale)**.
2. **Metodi di analisi orientata agli oggetti**.

I medoti di analisi sono nati come conseguenza dei metodi di programmazione.

Per descrivere completamente un sistema è necessario costruire vari modelli che rappresentino il sistema da vari punti di vista (**informazioni**, **funzioni** e **comportamento dinamico**).

# Tipi di modelli del sistema

Per descrivere la specifica semi-formale di un sistema software esistono 3 tipi di modelli:

1. **Modello dei dati**: rappresenta gli aspetti statici e strutturali relativi ai dati (data requirements):
	Notazioni usate:
	- ERD (not UML).
	- Class diagram (UML).
2. **Modello comportamentale**: rappresenta gli aspetti funzionali del sistema (functional requirements):
	Notazioni usate:
	- Data flow diagram (not UML).
	- Use case diagram (UML).
	- Activity diagram (UML).
	- Interaction diagram (UML).
3. **Modello dinamico**: rappresenta gli aspetti di "controllo“ e di come le funzioni del modello comportamentale modificano i dati introdotti nel modello dei dati.
	Notazioni usate:
	- State diagram (UML).

Le notazioni elencate erano utilizzate prima dell'introduzione dell'UML. Molti sono ora in disuso.
# Entity Relationship Diagram (ERD)

## Relazioni Uno-a-Molti

![[Pasted image 20251121152235.png]]

## Relazioni Molti-a-Molti

![[Pasted image 20251121152308.png]]
# Data Flow Diagram (DFD)

Formalismo non UML usato per formalizzare il modello comportamentale. Utilizza le seguenti notazioni:

![[Pasted image 20251121152325.png]]

## Esempio di DFD

### 1° raffinamento

![[Pasted image 20251121152349.png]]

### 2° raffinamento

![[Pasted image 20251121152412.png]]
# Structured System Analysis (SSA)

Analizzeremo un modello procedurale per capire le principali differenze con un modello ad oggetti.

Introdotto da Gane and Sarson (1979) e basato sul concetto di step-wise refinement, è costituito da 9 step. Era in voga negli anni '80, oramai desueto.

Altri metodi di analisi strutturata sono:
- DeMarco (1978).
- Yourdon and Constantine (1979).
## 1 - Disegna il DFD (Diagramma di Flusso dei Dati)

Usando il documento dei requisiti (o il prototipo), identifica i flussi di dati, con le rispettive sorgenti e destinazioni (dove i dati iniziano e terminano il loro flusso) e i processi che li trasformano.

Affina poi il DFD (Diagramma di Flusso dei Dati) aggiungendo nuovi flussi di dati o dettagli a quelli esistenti.

## 2 - Decidi quali Sezioni Computerizzare e Come

Usando un'analisi dei costi e benefici decidi quali sezioni del DFD automatizzare e come, se con 
**operazioni batch** (in lotti) o **elaborazione online** (in tempo reale).

**Esempio**:
- **Inserimento degli ordini**: operazioni in batch.
- **Convalida degli ordini**: elaborazione online.

Le prossime 3 fasi costituiscono il raffinamento graduale dei flussi di dati, dei processi e degli archivi di dati.

## 3 - Determina i Dettagli dei Flussi di Dati

Decidi quali  dati devono andare  nei vari flussi.

**Esempio**: Il flusso di dati `ordine` può essere scomposto come segue:
- identificazione_ordine
- dati_cliente
- dati_pacchetto

Quindi, scomporre ogni flusso gradualmente:
- `identificazione_ordine` è un intero a 12 cifre.
- `dati_cliente` consiste in `nome_cliente`, `indirizzo_cliente`, ecc.

## 4 - Definisci la Logica dei Processi

Esempio: costruire l'albero decisionale per un processo `concedi_sconto_istruzione`.

![[Pasted image 20251121163219.png]]

## 5 - Determina gli Archivi di Dati

Definire il contenuto esatto di ogni archivio e la sua rappresentazione (formato specifico in un dato linguaggio di programmazione). Definire il livello di accesso utilizzando un diagramma di accesso immediato ai dati (**DIAD**).

Esempio:

![[Pasted image 20251121163323.png]]

## 6 - Definisci le Risorse Fisiche

Esempi:
- Per ogni file, specificare: nome del file, organizzazione (sequenziale, indicizzata, ecc.), supporto di memorizzazione, record, fino al livello del campo.
- Se si utilizza un DBMS, specificare le informazioni rilevanti per ogni tabella.

## 7 - Determina le Specifiche di Input/Output

- I form di input devono essere specificate (componenti e layout).
- Anche le schermate di output devono essere determinate allo stesso modo.
- L'output stampato deve essere specificato (lunghezza stimata e dettagli).

## 8 - Determina il Dimensionamento

Calcolare:
- il volume di input (giornaliero o orario).
- la frequenza di ogni report stampato e la sua scadenza.
- la dimensione e il numero di record che devono passare tra la CPU e la memoria di massa.
- la dimensione di ogni file.

## 9 - Determinare i Requisiti Hardware

Sulla base delle informazioni di dimensionamento specificate nella Fase 8, determinare:
- Requisiti di memoria di massa.
- Requisiti di memoria di massa per il backup.
- Caratteristiche dei terminali utente.
- Caratteristiche dei dispositivi di output.
- Adeguatezza dell'hardware esistente.
- Costi dell'hardware da acquistare.

## Output della SSA

La 9 è l'ultima fase della SSA. Dopo l'approvazione del cliente, il documento di specifica risultante viene consegnato al team di progettazione e il processo software prosegue.

**Svantaggi:**
- La SSA non può essere utilizzata per determinare i tempi di risposta.
- La dimensione e la tempistica della CPU non possono essere determinate con un grado di accuratezza sufficiente.

