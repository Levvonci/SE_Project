
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

