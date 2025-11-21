
# Specifiche formali con Finite State Machine (FSM)

![[Pasted image 20250517193553.png]]
# Specifiche formali con linguaggio Z

Consiste di un set di schemi, ogni schema Z ha il seguente formato:

![[Pasted image 20250517193628.png]]

## Linguaggio Z: esempio di specifica di stato

![[Pasted image 20250517193654.png]]
## Linguaggio Z: esempio di specifica di operazione

![[Pasted image 20250517193719.png]]
# Spec. semi-formali: modelli del sistema

Un modello del sistema è una **rappresentazione astratta del sistema** che facilita la comprensione delle proprietà e del  funzionamento del sistema, prima che esso venga costruito.

L'uso di modelli dei sistemi software è formalizzato all'interno di metodi di analisi dei requisiti (specifica) del software che fanno uso di tecniche semi-formali.

I metodi di analisi dei requisiti software sono di due tipi:

1. **Metodi di analisi strutturata (o procedurale)**.
2. **Metodi di analisi orientata agli oggetti**.

Per descrivere completamente un sistema è necessario costruire vari modelli che rappresentino il sistema da vari punti di vista (**informazioni**, **funzioni** e **comportamento dinamico**).
# Tipi di modelli del sistema

Per descrivere la specifica semi-formale di un sistema software esistono 3 tipi di modelli:

**Modello dei dati**: rappresenta gli aspetti statici e strutturali relativi ai dati (data requirements):
- ERD (not UML).
- Class diagram (UML).

**Modello comportamentale**: rappresenta gli aspetti funzionali del sistema (functional requirements):
- Data flow diagram (not UML).
- Use case diagram (UML).
- Activity diagram (UML).
- Interaction diagram (UML).

**Modello dinamico**: rappresenta gli aspetti di "controllo“ e di come le funzioni del modello comportamentale modificano i dati introdotti nel modello dei dati.
- State diagram (UML).

## Entity Relationship Diagram (ERD)

Relazioni uno-a-molti

![[Pasted image 20250517194713.png]]

Relazioni molti-a-molti

![[Pasted image 20250517194742.png]]
## Data Flow Diagram (DFD)

![[Pasted image 20250517194906.png]]

### Esempio di DFD: 1° raffinamento

![[Pasted image 20250517194956.png]]

### 2° raffinamento

![[Pasted image 20250517195026.png]]
# Structured System Analysis (SSA)

Introdotto da Gane and Sarson (1979) e basato sul concetto di step-wise refinement, è costituito da 9 step. 

Altri metodi di analisi strutturata sono:

- DeMarco (1978).
- Yourdon and Constantine (1979).
## Step 1: Draw the DFD

Use the requirements document (or the prototype) to:

- Identify data flows.
- Identify source and destinations of data (where data flows starts and ends, respectively).
- Identify processes that transform data.

Refine the DFD by adding new flows of data or by adding details to existing data flows.
## Step 2: Decide what Sections to Computerize and How

Use cost-benefits analysis to decide which sections of the DFD to automate.

Decide how to computerize:
- Batch operations.
- On-line processing.

Example:
- Automate order placement in batch.
- Automate order validation online.

The next 3 steps are the stepwise refinement of data flows, processes and data stores.
## Step 3: Determine the details of the data flows

Decide what data items must go into the various data flows. The data flow order can be refined as
follows:
- order_identification.
- customer_details.
- package_details.

Then, refine each flow stepwise:
- Order_identification is a 12-digit integer.
- Customer_details consists of customer_name, customer_address, etc.
## Step 4: Define the logic of processes

Example: build the decision tree for a give_educational_discount process.

![[Pasted image 20250517201358.png]]
## Step 5: Determine the data stores

Define the exact contents of each store and its representation (specific format in a given programming language). Define the level of access by use of data-immediate-access diagram (DIAD).

Example:

![[Pasted image 20250517201451.png]]
## Step 6: Define the physical resource

Examples:
- For each file, specify: file name, organization (sequential, indexed, etc.), storage medium, records, down to the field level.
- If a DBMS is to be used, then the relevant information for each table is specified.

## Step 7: Determine the Input/Output specifications

- The input forms must be specified (components and layout).
- The output screens must similarly be determined.
- The printed output also must be specified (estimated length and details).
## Step 8: Determine the sizing

Compute:
- volume of input (daily or hourly).
- frequency of each printed report and its deadline.
- size and number of records that are to pass between the CPU and mass storage.
- size of each file.
## Step 9: Determine the hardware requirements

From sizing information specified at step 8, determine:
- Mass storage requirements.
- Mass storage requirements for backup.
- Characteristics of user terminals.
- Characteristics of output devices.
- Adequacy of existing hardware.
- Costs of hardware to be purchased.
## SSA Output

Step 9 is the last step of SSA. After approval by the client, the resulting specification document is handed to the design team, and the software process continues.

Drawbacks:
- SSA cannot be used to determine response times.
- CPU size and timing cannot be determined with any degree of accuracy.


