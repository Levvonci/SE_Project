
**Definizione IEEE (Std 1061-1998, Standard for a Software Quality Metrics Methodology)**:

> La qualità del software è il grado in cui il software possiede una combinazione desiderata di attributi.

• **Punti di vista:**
  – **Trascendente**
    • Eccellenza innata.
  – **Utente**
    • Adatto all'uso (soddisfa le esigenze dell'utente), piacevole da usare, soddisfazione dell'utente.
  – **Prodotto**
    • Attributi desiderati del software (affidabilità, correttezza, ecc.).
    • Conformità ai requisiti.
  – **Organizzazione**
    • Costi e profitti (maggiore efficienza, maggiore efficacia, valore aggiunto per l'organizzazione, prodotto commerciabile).
# Il Triangolo della Qualità (Modello di qualità di McCall)

![[Pasted image 20251202160525.png]]

# Indici di Qualità

## Operativi

*   **i₁ Correttezza** (Correctness)
    – Misura in cui un prodotto soddisfa le specifiche e adempie agli obiettivi dell'utente. *(Fa quello che voglio?)*
*   **i₂ Affidabilità** (Reliability)
    – Misura in cui ci si può aspettare che un prodotto svolga la sua funzione intesa con la precisione richiesta. *(Lo fa accuratamente ogni volta?)*
*   **i₃ Efficienza** (Efficiency)
    – Quantità di risorse computazionali e di codice richieste da un prodotto per eseguire una funzione. *(Girerà sul mio hardware nel modo più ottimale possibile?)*
*   **i₄ Integrità** (Integrity)
    – Misura in cui è possibile controllare l'accesso al software o ai dati da parte di persone non autorizzate. *(È sicuro?)*
*   **i₅ Usabilità** (Usability)
    – Sforzo richiesto per apprendere, operare, preparare l'input e interpretare l'output di un prodotto. *(Posso usarlo?)*
## Revisione

*   **i₆ Manutenibilità** (Maintainability)
    – Sforzo richiesto per localizzare e correggere un errore in un programma operativo. *(Posso ripararlo?)*
*   **i₇ Testabilità** (Testability)
    – Sforzo richiesto per testare un prodotto per assicurarsi che svolga la sua funzione intesa. *(Posso testarlo?)*
*   **i₈ Flessibilità** (Flexibility)
    – Sforzo richiesto per modificare un prodotto operativo. *(Posso modificarlo?)*

## Transizione

*   **i₉ Portabilità** (Portability)
    – Sforzo richiesto per trasferire un prodotto da un ambiente hardware e/o software a un altro. *(Sarò in grado di usarlo su un'altra macchina?)*
*   **i₁₀ Riusabilità** (Reusability)
    – Misura in cui un prodotto (o sue parti) può essere riutilizzato in altre applicazioni. *(Sarò in grado di riutilizzare parte del software?)*
*   **i₁₁ Interoperabilità** (Interoperability)
    – Sforzo richiesto per interfacciare un prodotto con un altro. *(Sarò in grado di interfacciarlo con un altro sistema?)*
*   **i₁₂ Evolubilità** (Evolubility)
    – Sforzo richiesto per aggiornare il prodotto per soddisfare nuovi requisiti. *(È facile aggiornarlo quando i requisiti cambiano?)*

# Indici e Attributi della Qualità del Software

- La qualità del software è definita in termini di **indici di qualità**.
- Ogni indice di qualità può a sua volta essere definito in termini di **attributi di qualità**.
- Ogni attributo può a sua volta essere definito in termini di **sotto-attributi**, che vengono misurati per ottenere il valore dell'attributo.
- I valori degli attributi contribuiscono a quantificare gli indici di qualità rilevanti.
- La valutazione degli indici di qualità consente di verificare la capacità del sistema di soddisfare i livelli di qualità desiderati (per gli indici di interesse).

# Attributi di Qualità

*   **a₁ Complessità**
    Livodo di comprensibilità e verificabilità degli elementi del software e delle loro interazioni.
*   **a₂ Accuratezza**
    Precisione dei calcoli e degli output.
*   **a₃ Completezza**
    Implementazione completa delle funzionalità richieste.
*   **a₄ Coerenza**
    Uso di tecniche e notazioni di progettazione e implementazione uniformi.
*   **a₅ Tolleranza agli errori**
    Continuità operativa garantita in condizioni avverse.
*   **a₆ Tracciabilità**
    Grado in cui è possibile stabilire una relazione tra due o più prodotti del processo di sviluppo.
*   **a₇ Estendibilità**
    Capacità di espandere la memoria o le funzioni.
*   **a₈ Generalità**
    Ampiezza delle potenziali applicazioni.
*   **a₉ Modularità**
    Presenza di moduli altamente indipendenti.
*   **a₁₀ Auto-documentazione**
    Documentazione in linea (nel codice).

# Checklist Method

Il livello di qualità di ogni attributo viene valutato mediante l'uso di tecniche basate su **checklist**.

*   Il risultato della checklist viene elaborato secondo **algoritmi appropriati** per ottenere un **punteggio normalizzato**, che indica il livello di qualità di ciascun attributo.

*   Una volta valutato il punteggio di ogni attributo, i valori rilevanti vengono **raggruppati per ogni attributo**, **riassunti** e **normalizzati** per ottenere il livello di qualità per ciascun indice. L'attributo deve essere considerato con il suo proprio **segno** (positivo o negativo).
## Checklist Evaluation

Una **checklist** è composta da diverse domande, e per ogni domanda sono previste quattro risposte con un dato valore.

*   Il calcolo **non terrà conto** delle domande identificate come **Non Applicabili**.
*   Se la domanda è **Non Valutabile**, allora il punteggio assegnato a quella domanda sarà il più basso tra quelli possibili.
*   Il team di valutazione della checklist è composto da **almeno quattro persone**, con competenze diverse in modo che vari punti di vista possano essere confrontati e la valutazione finale sia la più precisa possibile.
*   La composizione raccomandata del team è:
    *   Uno **Specialista dell'Assicurazione della Qualità**
    *   Un **Responsabile di Progetto**
    *   Un **Ingegnere dei Sistemi**
    *   Un **Analista Software**

# Calculation of the Score of Attributes

Per ogni attributo (eccetto la Modularità), il calcolo del punteggio viene eseguito secondo la seguente formula:

$$ S_A = \frac{\sum_{i=1}^{n} V_i}{\sum_{i=1}^{n} M_i} \times 10 $$

dove:
*   $V_i$ è il valore dato alla risposta scelta per la domanda $i$.
*   $M_i$ è il suo **valore massimo** possibile.
*   $n$ è il numero di domande considerate (escluse quelle "Non Applicabili").
*   Il punteggio $S_A$ per l'attributo $A$ è normalizzato su una scala fino a 10.
# Evaluation of the Quality Index

**Valutazione dell'indice di qualità**

Utilizzando i risultati del calcolo dei punteggi degli attributi e l'impatto di ciascun attributo sull'indice corrispondente, è possibile calcolare il livello di qualità dell'indice come segue:

$$ S_I = \frac{\sum V_{\text{attribute(+)} } - \sum V_{\text{attribute(-)}}}{\text{numero di attributi associati all'indice}} $$

dove:
*   $V_{\text{attribute(+)}}$ è il punteggio degli attributi che impattano **positivamente** sull'indice.
*   $V_{\text{attribute(-)}}$ è il punteggio degli attributi che impattano **negativamente** sull'indice.
*   Il denominatore è il **numero totale di attributi** associati a quell'indice.

Il punteggio risultante $S_I$ per l'indice di qualità $I$ è quindi normalizzato in base al numero di attributi che lo influenzano.
# Acceptance Level Scale

L'output della formula che restituisce $V_{indice}$ è un valore compreso tra 0 e 1.

*   Il seguente schema può essere utilizzato per identificare i valori di soglia per l'accettazione della qualità:

| $V_{indice}$        | **Livello di Qualità** |
| :------------------ | :--------------------- |
| $0.66 < V \le 1$    | **Alto**               |
| $0.33 < V \le 0.66$ | **Medio**              |
| $0 < V \le 0.33$    | **Basso**              |
# Example Checklists

Supponiamo che si debba valutare il livello di qualità dell'architettura di un sistema (nella fase di progettazione architetturale).

*   Nei prossimi lucidi verranno illustrate checklist di esempio per assegnare un punteggio ai seguenti attributi:
    *   **a₁ Complessità**
    *   **a₈ Generalità**
    *   **a₉ Modularità**
## Checklist per la Complessità

**Aspetti generali**

1.  I nomi di moduli, procedure e strutture sono significativi o conformi a uno standard, se presente?
    *   0: Sì, quasi sempre
    *   1: Abbastanza spesso
    *   2: Raramente
    *   3: No

2.  Il formalismo utilizzato per descrivere l'architettura del sistema è unico, o sono presenti più formalismi?
    *   0: Formalismo unico, standard e scelto correttamente
    *   1: Pochi formalismi, standard e scelti correttamente
    *   2: Pochi formalismi, qualcuno fuori standard
    *   3: Molti formalismi, alcuni fuori standard

3.  La progettazione globale del sistema è strutturata correttamente e di facile comprensione per persone senza conoscenze specifiche del sistema?
    *   0: Sì
    *   1: Quasi positivo
    *   2: Non propriamente strutturata
    *   3: Strutturata male, e di difficile comprensione

4.  È possibile dedurre la classe di informazione di ogni singolo dato presente nel modello logico? Tutti gli utilizzi di questo dato sono dichiarati nella documentazione e realizzati con lo scopo di leggere o scrivere quella classe di informazione?
    *   0: No
    *   1: Raramente
    *   2: Abbastanza spesso
    *   3: Quasi sempre.

**Applicazione delle metriche**

5.  Se è possibile eseguire misurazioni sulla complessità del programma, basandosi sul grafo delle chiamate, utilizzare le metriche definite di seguito.
    5.1) **Complessità gerarchica**: è il numero medio di moduli per livello dell'albero delle chiamate, cioè il numero totale di moduli diviso per il numero di livelli dell'albero.
    *   0: Da 0 a 4
    *   1: Da 4 a 8
    *   2: Da 8 a 12
    *   3: Minore di 2 o maggiore di 12

    5.2) **Complessità strutturale**: è il numero medio di chiamate per ciascun modulo, cioè il numero di chiamate intermodulari diviso per il numero di moduli.
    *   0: Minore di 2
    *   1: Da 2 a 4
    *   2: Da 4 a 8
    *   3: Maggiore di 8
## Checklist per la Generalità

1.  Tutte le funzioni offerte dai moduli (e le loro interfacce) sono adeguatamente progettate in modo che sia possibile riutilizzarle in alcune implementazioni non previste all'inizio del progetto? (Ad es.: una specifica percentuale [18%], o qualsiasi percentuale di qualsiasi valore)
    *   0: No
    *   1: Raramente
    *   2: Abbastanza spesso
    *   3: Sempre

2.  Per quanto riguarda i moduli che non hanno sufficiente generalità, è possibile renderli più generici con uno sforzo ridotto (circa il 10% dello sforzo globale per ottenerli ciascuno)?
    *   0: No
    *   1: Raramente
    *   2: Abbastanza spesso
    *   3: Sempre

3.  Tutte le manipolazioni delle strutture dati sono combinate in moduli specificamente dedicati a questo scopo?
    *   0: No
    *   1: Raramente
    *   2: Abbastanza spesso
    *   3: Sempre
## Checklist per la Modularità

**Coesione**

1.  Qual è la distribuzione percentuale dei moduli del sistema secondo i seguenti quattro tipi?
    1A Moduli con **coesione coincidentale** (accidentale)
    1B Moduli con **coesione logica o temporale**
    1C Moduli con **coesione procedurale o comunicazionale**
    1D Moduli con **coesione informazionale o funzionale**

**Accoppiamento**

2.  Qual è la distribuzione percentuale delle modalità di comunicazione (accoppiamento) tra moduli secondo i seguenti quattro tipi?
    2A Coppie di moduli con **accoppiamento per contenuto**
    2B Coppie di moduli con **accoppiamento comune** (globale)
    2C Coppie di moduli con **accoppiamento di controllo**
    2D Coppie di moduli con **accoppiamento per stampo o per dati**

**Aspetti generali**

3.  La decomposizione del sistema è organizzata in modo gerarchico?
    *   0: No
    *   1: Raramente
    *   2: Sì, sufficientemente
    *   3: Sì

4.  Qual è la percentuale di strutture gerarchiche (ogni programma contiene un numero paragonabile di moduli)?
    *   0: Meno del 70%
    *   1: Tra il 70% e l'80%
    *   2: Tra l'80% e il 90%
    *   3: Più del 90%
## Score for Cohesion and Coupling Questions

# Procedura per l'assegnazione del punteggio agli attributi

a)  La documentazione deve essere analizzata in profondità per ottenere una risposta sufficientemente precisa a ogni domanda contenuta nella checklist. Ogni domanda prevede quattro possibili risposte, e ciascuna di esse è associata a un punteggio.

b)  Ogni revisore appartenente al team di valutazione deve rispondere alle domande della checklist **indipendentemente**. Il revisore non deve conoscere le risposte degli altri prima di fornire le proprie.
    *   Le domande identificate come **Non Applicabili** devono essere esplicitamente segnalate in questo modo.
    *   Quando una domanda è stata identificata come **Non Valutabile**, viene analizzata più in dettaglio per verificare se sia applicabile o meno. Se alla fine dell'analisi la domanda è considerata applicabile, allora le viene assegnato il **punteggio più basso** tra quelli possibili. Questo evento fornisce anche un'indicazione di non conformità della documentazione esaminata.

c)  Quando tutti i membri del team di valutazione forniscono risposte diverse a una data domanda, è necessario che raggiungano **una risposta comune concordata**.

d)  Alla fine della discussione, verrà compilata **una sola checklist ufficiale** con le risposte concordate dai membri del team di valutazione.

e)  Calcolare il punteggio del sotto-attributo (o attributo) secondo la **formula di calcolo** prevista.
## Template for Attribute Scoring

![[Pasted image 20251202181801.png]]
## Template for Index Evaluation

![[Pasted image 20251202181815.png]]

# Software Quality Assurance

L'**Assicurazione della Qualità del Software (SQA - Software Quality Assurance)** è un approccio pianificato e sistematico per garantire che sia il processo software sia il prodotto software siano conformi a standard, processi e procedure stabiliti.

*   Gli **obiettivi** della SQA sono migliorare la qualità del software monitorando sia il software che il processo di sviluppo, per garantire la piena conformità con standard e procedure stabiliti.

*   **Passi per stabilire un programma SQA:**
    1.  Ottenere il **consenso e il supporto del top management** sui suoi obiettivi (senza il supporto della direzione, la SQA non può essere efficace).
    2.  Identificare i **problemi SQA**, redigere un **piano SQA**, stabilire standard e procedure SQA, implementare il piano SQA e valutare il programma SQA.

## SQA Role

Il ruolo della SQA è fornire al management la garanzia che il processo ufficialmente stabilito venga effettivamente implementato.

*   La SQA assicura che:
    *   Una **metodologia di sviluppo appropriata** sia in atto.
    *   I progetti utilizzino **standard e procedure** nel loro lavoro.
    *   Vengano condotte **revisioni e audit**.
    *   Vengano prodotti **documenti** a supporto della manutenzione e dell'evoluzione.
    *   Venga istituita la **gestione della configurazione software** per controllare i cambiamenti.
    *   Venga eseguito e superato il **testing**.
    *   Le **deficienze e le deviazioni** vengano identificate, documentate e portate all'attenzione del management.
## SQA Goals

Gli obiettivi della SQA sono ridurre i rischi attraverso:
*   Il **monitoraggio appropriato** del software e del processo di sviluppo.
*   La garanzia della **piena conformità** con standard e procedure per il software e il processo.
*   L'assicurazione che le **inadeguatezze** nel prodotto, nel processo o negli standard vengano portate all'attenzione del management in modo che possano essere risolte.

*   La SQA **non è responsabile della produzione di prodotti di qualità**. È responsabile del **controllo** (cioè dell'esaminare in profondità il prodotto, confrontandolo con standard e procedure stabiliti) delle azioni sulla qualità e dell'**avvisare il management** di eventuali deviazioni.
## SQA Standards and Procedures

Gli **standard** sono i criteri a cui i prodotti software vengono confrontati (cioè, gli standard definiscono **cosa** deve essere fatto).

*   Requisiti minimi per gli standard includono:
    *   **Standard di Documentazione**: specificano forma e contenuto per la pianificazione, il controllo e la documentazione del prodotto, garantendo coerenza durante un progetto.
    *   **Standard di Progettazione (Design)**: specificano forma e contenuto del prodotto di design. Forniscono regole per tradurre i requisiti software nel design e per rappresentarlo nella documentazione di progetto.
    *   **Standard di Codice**: specificano il linguaggio in cui il codice deve essere scritto e definiscono eventuali restrizioni sull'uso delle funzionalità del linguaggio. Definiscono la struttura linguistica consentita, convenzioni di stile, regole per le strutture dati e la documentazione interna del codice.

Le **procedure** sono i criteri a cui i processi di sviluppo e controllo vengono confrontati (cioè, le procedure definiscono **come** il lavoro deve essere effettivamente svolto, da chi, quando e cosa viene fatto con i risultati).
## SQA Plan

Il **piano SQA** specifica gli obiettivi della SQA, le attività da svolgere e gli standard e le procedure rispetto ai quali il lavoro di sviluppo deve essere misurato.

*   Lo standard IEEE per la preparazione di un piano SQA (730-1998) include le seguenti sezioni:
    1.  **Management** (Gestione)
    2.  **Documentation** (Documentazione)
    3.  **Standards, Practices, and Conventions** (Standard, Pratiche e Convenzioni)
    4.  **Reviews and Audits** (Revisioni e Audit)
    5.  **Software Configuration Management** (Gestione della Configurazione Software)
    6.  **Problem Reporting and Corrective Action** (Segnalazione dei Problemi e Azioni Correttive)
    7.  **Tools, Techniques, and Methodologies** (Strumenti, Tecniche e Metodologie)
    8.  **Code Control** (Controllo del Codice)
    9.  **Media Control** (Controllo dei Supporti)
    10. **Supplier Control** (Controllo dei Fornitori)
    11. **Records Collection, Maintenance, and Retention** (Raccolta, Manutenzione e Conservazione dei Record)