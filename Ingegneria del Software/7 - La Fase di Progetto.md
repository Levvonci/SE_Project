**Fase in cui si decidono le modalità di passaggio** da "cosa" deve essere realizzato nel sistema software a **"come"** la realizzazione deve avere luogo.

Prende in input il documento di specifica (**analisi dei requisiti**) e produce un **documento di progetto** che guida la successiva fase di codifica. Può essere suddivisa in due sotto-fasi:

1. **Progetto architetturale (o preliminare)**, in cui il sistema software complessivo viene suddiviso in più sottosistemi (**decomposizione modulare**)
2. **Progetto dettagliato**, in cui ogni sottosistema identificato viene progettato in dettaglio, **scegliendo algoritmi e strutture dati specifiche**

# Principi di Progettazione

1. **Stepwise refinement** (utilizzato principalmente in fase di progettazione, ma applicabile anche durante l'analisi dei requisiti per raffinare la specifica)  
2. **Astrazione** (principio trasversale utilizzato sia in fase di analisi dei requisiti che di progettazione)  
3. **Decomposizione modulare** (tecnica di progettazione)  
4. **Modularità** (proprietà di un sistema scomposto in moduli)  
5. **Information hiding** (principio di progettazione)  
6. **Riusabilità** (attributo di qualità del software)
## Stepwise Refinement

Il procedere per **raffinamenti successivi** (stepwise refinement) è una strategia di progettazione top-down proposta da Wirth (1971) nell'ambito della programmazione strutturata.

Il raffinamento è un processo di elaborazione che parte dalla specifica di una funzione (o di dati) in cui *non* si descrive il funzionamento interno della funzione o la struttura interna dei dati. Ad ogni passo, il raffinamento elabora la specifica aggiungendo un livello di dettaglio maggiore.

L'importanza del raffinamento deriva dalla legge di Miller (1956): "In un dato momento, un essere umano può concentrarsi al massimo su 7 ± 2 unità d'informazione (chunk)".

Il raffinamento è un concetto complementare a quello di **astrazione**: mentre l'astrazione consente di nascondere i dettagli complessi, il raffinamento permette di introdurli progressivamente in modo controllato.
## Astrazione

**L'astrazione** consiste nel concentrarsi sugli aspetti essenziali di un'entità e nell'ignorare i dettagli secondari.

Il concetto di **livello di astrazione** è stato introdotto da Dijkstra (1968) nell'ambito dei sistemi operativi, al fine di descriverne l'architettura a strati (layered architecture).

Nell'ambito del processo software, ogni passo di progettazione rappresenta un raffinamento del livello di astrazione della soluzione. Ciò significa concentrarsi su _cosa è_ e _cosa fa_ un'entità del sistema software, prima di decidere _come_ debba essere realizzata.

**I principali tipi di astrazione sono:**

- **Astrazione procedurale** (es. funzioni in C) – focalizzata sull'operazione da compiere. 
- **Astrazione dei dati** (es. incapsulamento dei dati o _data encapsulation_) – focalizzata sulla struttura dei dati e sulle operazioni associate.

Con il termine **incapsulamento dei dati** (_data encapsulation_) si intende una struttura dati progettata insieme alle operazioni (azioni) che è possibile eseguire su di essa.  
Un classico esempio è lo **stack**, definito dalla sua struttura dati e dalle azioni che realizzano il meccanismo LIFO (_Last In, First Out_).

L'uso dell'incapsulamento dei dati in fase di progetto permette di ottenere significativi vantaggi sia nella fase di codifica che in quella di manutenzione del software.

### Tipi di Dati Astratti

Un **tipo di dato astratto (ADT - Abstract Data Type)** identifica un tipo di dato insieme alle operazioni (azioni) eseguibili sulle sue istanze.

Un tipo di dato astratto combina **astrazione procedurale** e **astrazione dei dati**, incapsulando sia la struttura dei dati che il comportamento ad esso associato.

L'uso dei tipi di dati astratti permette di migliorare significativamente la qualità del software, in particolare rispetto agli attributi di **riusabilità** e **manutenibilità**.

Una **classe in C++** è un esempio concreto di tipo di dato astratto che, oltre all'incapsulamento, supporta il meccanismo di **ereditarietà**.
#### Esempio di Abstract Data Type - (classe C++)

![[Pasted image 20251202135714.png]]
## Modularità

**Prodotti software** costituiti da un unico blocco di codice **monolitico** sono difficili da:

- manutenere
- correggere
- comprendere
- riutilizzare

Di conseguenza si tende a suddividere il prodotto software in **moduli**.

**Definizione di Modularità** (IEEE Std 610.12 - Standard Glossary of Software Engineering Technology):

> _"The extent to which software is composed of discrete components such that a change to one component has minimal impact on the other components."_

### Decomposizione Modulare

**Un modulo** è un elemento software che:
- Contiene istruzioni, logica di elaborazione e strutture dati
- Può essere compilato separatamente e memorizzato all'interno di una libreria software
- Può essere incluso in un programma
- Può essere utilizzato invocando segmenti di modulo identificati da un nome e da una lista di parametri
- Può utilizzare altri moduli

La suddivisione di un sistema software in moduli (**decomposizione modulare**) produce come risultato l'identificazione di un'**architettura dei moduli** (ad esempio, rappresentabile con uno _structure chart_).

L'**architettura dei moduli** di un sistema software descrive:

1. La struttura dei moduli
2. Il modo in cui i moduli interagiscono
3. La struttura dei dati manipolati

La decomposizione modulare si basa sul principio del **"divide et impera"**.  
Date due problemi **p₁** e **p₂**, dove **C** indica la complessità e **E** lo sforzo necessario (effort), valgono le seguenti relazioni:

1. Se **C(p₁) > C(p₂)** ⇒ **E(p₁) > E(p₂)**
2. **C(p₁ + p₂) > C(p₁) + C(p₂)** ⇒ **E(p₁ + p₂) > E(p₁) + E(p₂)**

### Criteri per una Buona Decomposizione

Una buona divisione di un prodotto software in moduli è quella che permette di **massimizzare la coesione (cohesion)** e **minimizzare il grado di accoppiamento (coupling)**.

Ciò aumenta la:

- Comprensibilità
- Manutenibilità
- Estensibilità
- Riusabilità

del prodotto software.
### Cohesion/Coupling Rispetto a Modularità
![[Pasted image 20251202141024.png]]
### Modularità e Costo del Software
![[Pasted image 20251202141303.png]]
### Coesione

Per eseguire una funzione sono necessarie varie istruzioni che possono essere **concentrate in un singolo modulo**, oppure **sparse tra più moduli**.

La **coesione di un modulo** misura il grado in cui il modulo espleta internamente al modulo _tutte_ le azioni necessarie a realizzare una data funzione, senza dover interagire con altri moduli.

#### Livelli di Coesione

1. **Coincidentale (Coincidental)** – Nessuna relazione logica tra gli elementi del modulo.    
2. **Logica (Logical)** – Elementi correlati, di cui uno viene selezionato dal modulo chiamante (ad esempio, un modulo per gestire diverse conversioni di formato).
3. **Temporale (Temporal)** – Relazione basata sull'ordine temporale tra gli elementi (es. funzioni di "inizializzazione").
4. **Procedurale (Procedural)** – Elementi correlati in base a una sequenza predefinita di passi da eseguire (es. una procedura di aggiornamento).
5. **Comunicazionale (Communicational)** – Elementi correlati in base a una sequenza predefinita di passi da eseguire sulla _stessa struttura dati_.
6. **Informazionale (Informational)** – Ogni elemento ha una porzione di codice indipendente, con un proprio punto di ingresso e uscita; tutti gli elementi agiscono sulla stessa struttura dati (prototipo di una classe). Ottimale per il paradigma OO.
7. **Funzionale (Functional)** – Tutti gli elementi sono correlati dal fatto di svolgere una **singola, ben definita funzione**. Questo è il livello di coesione _ideale_. Ottimale per il paradigma strutturato.
## Esempi
### Coincidental Cohesion

**Funzioni del Modulo:**
- `print_next_line()` – Stampa la prossima riga
- `invert_characters(second_string)` – Inverte i caratteri del secondo parametro di tipo stringa
- `add_to_parameter(fifth_parameter, 7)` – Aggiunge 7 al valore del quinto parametro
- `convert_int_to_double(fourth_parameter)` – Esegue la conversione da intero a double sul quarto parametro

### Logical Cohesion
![[Pasted image 20251202142848.png]]
### Temporal Cohesion

**Funzioni del Modulo:**
- `open_file(old_master_file)` – Apre il file master precedente
- `open_file(new_master_file)` – Apre il nuovo file master
- `open_file(transaction_file)` – Apre il file delle transazioni
- `open_file(print_file)` – Apre il file di stampa/log
- `initialize_table(sales_region_table)` – Inizializza la tabella delle regioni di vendita
- `read_record(transaction_file)` – Legge il primo record dal file delle transazioni
- `read_record(old_master_file)` – Legge il primo record dal file master precedente
### Procedural Cohesion

**Funzioni del Modulo:**

- `get_part_number_from_db()` – Legge il codice componente (`part_number`) dal database
- `update_maintenance_record(part_number)` – Utilizza il codice componente per aggiornare la scheda di riparazione (`repair_record`) nel file di manutenzione

### Communicational Cohesion

**Esempio 1: Funzioni del Modulo**

- `update_database_record(record_a)` – Aggiorna `record_a` nel database
- `write_to_file(record_a, trajectory_file)` – Scrive `record_a` nel file di traiettoria (`trajectory_file`)

**Esempio 2: Funzioni del Modulo**

- `calculate_new_trajectory()` – Calcola la nuova traiettoria (`new_trajectory`)
- `print_trajectory(new_trajectory)` – Invia `new_trajectory` alla stampante

### Informational Cohesion

![[Pasted image 20251202143119.png]]
## Example Structure Chart & Modules Cohesion

![[Pasted image 20251202143151.png]]

# Coupling

L'**accoppiamento** misura il grado di dipendenza e di interconnessione tra due o più moduli software.

**Livelli di Accoppiamento** (dal **peggiore**, 1, al **migliore**, 5):

1. **Accoppiamento per Contenuto (Content)** – Un modulo fa riferimento diretto al contenuto interno (es. variabili locali, codice) di un altro modulo. _(Massima dipendenza)_
2. **Accoppiamento per Dati Comuni (Common)** – Due o più moduli condividono e accedono alla stessa struttura dati globale.
3. **Accoppiamento di Controllo (Control)** – Un modulo controlla esplicitamente la logica di esecuzione di un altro modulo (es. passando un flag di controllo).
4. **Accoppiamento per Struttura (Stamp)** – Due moduli si scambiano una struttura dati complessa, ma ciascuno utilizza solo una parte dei suoi elementi.
5. **Accoppiamento per Dati (Data)** – Due moduli comunicano tramite parametri omogenei: argomenti semplici o strutture dati di cui vengono utilizzati **tutti** gli elementi. _(Accoppiamento ideale, minima dipendenza)_

## Factors affecting Coupling

La **forza dell'accoppiamento** (_strength of coupling_) dipende da:

1. **Numero di riferimenti** – Quante volte un modulo richiama o dipende da un altro modulo.
2. **Volume di dati** – La quantità di dati condivisi o passati tra i moduli.
3. **Complessità dell'interfaccia** – La complessità (struttura, numero di parametri) dei meccanismi di comunicazione tra i moduli.
4. **Grado di controllo** – Quanto un modulo influenza o controlla direttamente il flusso di esecuzione di un altro modulo.

## Esempi

### Content Coupling

`p → q`

- **Esempio 1:** Il modulo `p` modifica direttamente un'istruzione del codice del modulo `q`.
- **Esempio 2:** Il modulo `p` fa riferimento a dati locali del modulo `q` utilizzando uno scostamento numerico (offset) all'interno della memoria di `q`.
- **Esempio 3:** Il modulo `p` effettua un salto (`branch`) a un'etichetta (`label`) locale definita all'interno del modulo `q`.

### Common Coupling
![[Pasted image 20251202143723.png]]
### Control Coupling

Il modulo `p` chiama il modulo `q` e si verifica il seguente flusso:

1. `p` richiede a `q` di eseguire un'azione.
2. `q` restituisce a `p` un flag di controllo (es. "task non completato").
3. Sulla base di quel flag, `q` _chiede_ implicitamente o esplicitamente a `p` di eseguire un'ulteriore azione (es. "stampa un messaggio di errore").

In questo schema, `q` non solo restituisce un risultato, ma influenza attivamente il flusso di controllo del suo chiamante (`p`), creando un ciclo di dipendenza decisionale.
## Example Structure Chart & Modules Coupling

![[Pasted image 20251202143846.png]]

# Information hiding

I concetti di **astrazione procedurale** e **astrazione dei dati** derivano da un concetto più generale chiamato **information hiding**, introdotto da Parnas (1971).

L'**information hiding** consiste nel definire e progettare i moduli in modo che i dettagli implementativi (procedure e dati) **non siano accessibili** ad altri moduli che non abbiano necessità di conoscere tali dettagli.

I vantaggi della tecnica di information hiding si riscontrano principalmente quando è necessario apportare modifiche **nelle fasi di testing e manutenzione**.
## Esempio

Esempio di tipo di dato astratto (classe C++) realizzato con information hiding.

![[Pasted image 20251202133924.png]]

# Riusabilità

**La riusabilità** fa riferimento all'utilizzo di componenti sviluppati per un prodotto all'interno di **un prodotto diverso**.

Per **componente riusabile** si intende non solo un modulo o un frammento di codice, ma anche progetti, parti di documenti, insiemi di test data o stime di costi e durata.

**Vantaggi**:
  - **Netta diminuzione** di costi e tempi di produzione del software
  - **Incremento dell'affidabilità** dovuto all'uso di componenti già convalidati

La riusabilità nella fase di progetto si applica a:
1. **moduli software**
2. **application framework**, che incorpora la logica di controllo di un progetto
3. **design pattern**, che identifica una soluzione di progetto ricorrente in applicazioni dello stesso tipo
4. **architetture software** comprendenti (a), (b) e (c)

![[Pasted image 20251202133608.png]]