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