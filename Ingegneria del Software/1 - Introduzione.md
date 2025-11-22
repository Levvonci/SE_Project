# Informazioni sul Corso

**Docente**: Prof. Andrea D’Ambrogio.
**Obiettivi**: 
- Fornire i metodi e le tecnologie per inquadrare la produzione del software all'interno di una disciplina ingegneristica.
- Presentare il processo software e le più moderne tecniche di produzione.
**Esami**:
- 2 appelli a fine di ogni semestre.
- 2 appelli a settembre.
**Testo consigliato**: I. Sommerville, Software Engineering, Addison-Wesley (anche in italiano).
**Materiale didattico**: distribuito su piattaforma MS Teams.

# Cos'è il Software Engineering

È la disciplina per lo sviluppo del software secondo i principi ingegneristici della **progettazione** e **validazione**. Senza si rischia:
1. **Scarsa qualità del prodotto**: ovvero non svolge le funzioni per il quale è stato ideato.
2. **Scarsa competitività**: causata da **Cost** & **Time Overrun** (I costi di tempo e denaro effettivi superano di molto i preventivi).

# Problemi nel Software Engineering

Si dividono in due categorie:

## Accidentali

Superabili col progresso della tecnologia:

- di attitudine: Tendenza da parte dell'utente a trattare il software in maniera diversa da tutti gli altri prodotti. Il software è facilmente modificabile.
- di manutenzione: attività principale durante la vita di un software.
- di specifica e progetto: 
- di teaming: legato agli aspetti organizzativi nel caso di team con molti sviluppatori.

## Essenziali

Non sono superabili col progresso dei mezzi e conoscenze:

1. **Complessità**: 
2. **Conformità**:
3. **Cambiabilità**:
4. **Invisibilità**:

DI COSTO del prodotto sw

• costo verso dimensione (size)
• costo verso repliche
• costo verso ampiezza di mercato
# Le Fasi di vita del Software

La produzione di un software si divide in 3 stadi:

1. **Sviluppo**: Si divide in 6 fasi:
	1. **Raccolta dei Requisiti**: Cosa deve fare il software
	2. **Specifiche** (o analisi dei requisiti): Come implementare i requisiti
	3. **Pianificazione**: analisi delle tempistiche di sviluppo, stime dei costi per il committente.
	4. **Progetto** (preliminare e dettagliato):
	5. **Codifica**
	6. **Integrazione**
2. **Manutenzione**: copre circa il 60% dei costi del ciclo di vita
3. **Dismissione**.
# Il Costo delle Modifiche

Il costo di una modifica aumenta in maniera esponenziale all'avanzare delle fasi di sviluppo, indicativamente:

1. Definizione dei requisiti: 1X.
2. Sviluppo: 1.5X - 6X.
3. Rilascio: 60X - 100X.
# Testing

Attività che idealmente viene svolta alla fine di ogni fase per controllare che la fase sia stata ben svolta (**Verifica**: are we building the product right?), ed alla fine dello sviluppo per controllare che il prodotto finale sia buono (**Validazione**: are we building the right product?).
# Defect Removal Efficiency - DRE

È il rapporto fra il numero di bug trovati prima del rilascio del prodotto software ed il numero di bug totali:

**Esempio**: Se il team di sviluppo trova 900 bug prima del rilascio e gli utenti trovano 100 bug in un intervallo temporale standard a partire dalla data di rilascio (tipicamente 90 giorni) allora il valore di DRE è pari al 90%.

$$DRE = \frac{Errori\ trovati\ prima\ del\ rilascio}{Errori\ totali}$$

Nel 2016 il DRE medio negli USA è stato di 92% (i valori cambiano in base al modello di ciclo di vita).

# Costi di Sviluppo


Indicativamente il costo di un software è il quadrato del suo **size** ($C=aS^2$) inteso come numero di righe di codice. Fare due prodotti di size $\frac{S}{2}$ costa meno che farne uno di size S. Idealmente quindi lo sviluppo di un software va partizionato in tanti sottoprodotti che vanno poi integrati fra loro. Esistono dei limiti però, integrare le parti ha un **costo d'integrazione**.

Vendere un prodotto di size doppio per il mercato richiede:
1. Un prezzo 4 volte superiore a parità di dimensione di mercato.
2. Un mercato 4 volte più grande a parità di prezzo

Nota: produrre una replica non costa niente.

# Definizioni Utili

**Prodotto Software**: È composto dal codice e la documentazione inerente.
**Artefatto**: È un prodotto software intermedio, composto da:
- Documento requisiti.
- Documento delle specifiche.
- Documento di progetto.
**Codice**: Prodotto Software finale.
**Sistema Software**: È insieme organizzato di prodotti software compresi i componenti hardware.

**Cliente**: è chi ordina il prodotto software.
**Sviluppatore**: è chi produce il prodotto software.
**Utente**: è chi usa il prodotto software.

**Software interno**: Quando il prodotto finale è utilizzato/ordinato dal sviluppatore stesso.
**Software a contratto**: Quando cliente e sviluppatore sono soggetti differenti.

**Defect**: anomalia presente in un prodotto software.
**Failure**: comportamento anomalo del prodotto software dovuto alla presenza di un difetto.
**Errore**: azione errata di chi per ignoranza, distrazione, ecc. introduce un difetto nel prodotto software.
# Cos'è la Software Reliability

L'affidabilità di un software è la probabilità che il prodotto software funzioni correttamente per un certo intervallo temporale chiamato **mission time**. Dipende dal numero di difetti dentro al prodotto e dall'uso che ne fa l'utente.

Per ottenere un prodotto affidabile dobbiamo minimizzare il numero di difetti, ma la relazione tra il numero di difetti e l'affidabilità non è semplice.

Eliminare difetti da parti del prodotto poco usate influisce poco sull'affidabilità.

**La regola 10-90**:  secondo alcuni studi il 90% del tempo di esecuzione di un software è speso eseguendo il 10% delle istruzioni. Questo 10% è chiamato **core del programma**. 

La quantità di miglioramento dell’affidabilità a seguito dell’eliminazione di un difetto dipende se esso appartiene o meno al core del programma.

Questo nucleo di istruzioni varia però da come viene utilizzato il prodotto dall'utente, in termini tecnici, dal suo **operational profile**. 

## Differenze fra Hardware e Software Reliability

I guasti software sono principalmente dovuti alla presenza di difetti nei programmi,  mentre i guasti hardware sono causati da difetti di conformità o deterioramento dei componenti. Per riparare il difetto basta sostituire il componente. Mentre i difetti software richiedono una modifica al codice cambiando il funzionamento del prodotto.

A causa di queste differenze, le metriche usate per l'affidabilità hardware non sono applicabili all'affidabilità software.

Dopo una riparazione l'affidabilità hardware torna ai livelli precedenti, mentre una riparazione software può sia migliorare che peggiorare l'affidabilità del prodotto.

L'**obiettivo dell’affidabilità hardware** è quello della **stabilità**, cioè tenere la frequenza di
guasto costante nel tempo.

L'**obiettivo dell’affidabilità software** è invece quello della **crescita di affidabilità**, cioè far
decrescere la frequenza di guasto.

Andamento della frequenza di un guasto hardware:
![[andamento-guasto-hw.png]]

Andamento della frequenza di un guasto software:
![[andamento-guasto-sw.png]]

# Cos'è la Software Availability

La disponibilità software è la percentuale di tempo che il software è risultato usabile nel corso della sua vita. Dipende dal numero di guasti bloccanti che si verificano e dal tempo necessario a ripararli.

# L'importanza della Software Reliability/Availability

Essi sono metriche particolarmente importanti per i sistemi in cui la caduta del servizio crea gravi perdite economiche e sociali.

Esempi:
1. Sistemi di trasporto
2. Sistemi di governo del traffico aereo
3. Sistemi di governo del volo
4. Sistemi di produzione e distribuzione di energia
5. Sistemi di comunicazione
6. Ecc.

# Conclusioni

Nel corso degli anni la produzione del software ha seguito varie fasi:
- Fase di **abilità** - in cui prevalgono gli aspetti di lavoro individuale e creativo
- Fase **artigianale** - in cui il software viene prodotto da piccoli gruppi specializzati di alto livello professionale
- Fase **industriale** - in cui l'attività di sviluppo e manutenzione del software viene pianificata e coordinata, il lavoro svolto dal progettista inoltre viene sempre più supportato da strumenti automatici.

Il software è considerato come un insieme di elementi che formano una "configurazione" che include:
- Programmi
- Documenti
- Dati multimediali

Inoltre questo viene realizzato dall'ingegnere del software che applica un processo per ottenere risultati di qualità elevata. Si applica al software quindi un approccio ingegneristico.

Caratteristiche del software:
1. Il software va "ingegnerizzato"
2. Il software non si consuma
3. Il software è complesso, invisibile, si conforma, si cambia.

# I miti da sfatare del software
- In caso di ritardo, basta aumentare il numero di programmatori
- Una descrizione generica è sufficiente a scrivere programmi. Eventuali modifiche si possono modificare in seguito con facilità.
- Una volta messo in opera il programma, il lavoro è finito.
- Non c'è modo di valutare la qualità fino a quando non si ha a disposizione il prodotto finale.
- L'ingegneria del software è costosa e rallenta la produzione.