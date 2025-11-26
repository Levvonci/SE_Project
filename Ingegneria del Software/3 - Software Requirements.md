
Sono le funzionalità che un sistema software deve fornire, ed i vincoli che esso deve rispettare sia in fase di sviluppo che durante la fase operativa.

Vengono generati applicando il **requirements engineering**.

**Funzionamento**: se un'azienda vuole appaltare un progetto di sviluppo software: 

1. Definisce i requisiti del software in maniera generica tale da non predefinire una soluzione. Ciò permette a più appaltatori di competere per il contratto, offrendo soluzioni diverse per soddisfare le esigenze del cliente.
2. Una volta assegnato l'appalto, lo sviluppatore deve redigere una definizione dettagliata del sistema, per permettere al cliente di capire e convalidarne le funzionalità. Entrambi questi documenti possono essere definiti come "il documento dei requisiti" del sistema.
# Tipi di requisiti

Sono due:
1. **Requisiti Utente**.
2. **Requisiti di Sistema.

## Requisiti Utente

È la descrizione in linguaggio naturale con l'aggiunta di diagrammi, dei requisiti funzionali e non funzionali che il sistema deve fornire. Devono essere comprensibili agli utenti del sistema sprovvisti di conoscenze tecniche.

Linee guida:
1. Usare un formato standard per tutti i requisiti.
2. Il linguaggio naturale dev'essere consistente (es. uso di "deve" per requisiti necessari e "dovrebbe" per requisiti desiderabili).
3. Evidenziare le parti fondamentali di un requisito.
4. Evitare l'uso di termini tecnici.
### Esempio di Requisito Utente
![[Pasted image 20251120114052.png]]

## Requisiti di sistema (Specifiche)

Sono descritti attraverso la scrittura di un documento dettagliato che descrive i servizi che il sistema software deve fornire (**documento di specifica**). Usati come base per il progetto software, possono essere espressi usando notazioni differenti. Questo documento è un contratto tra cliente e fornitore.
## Notazioni

![[Pasted image 20251120114259.png]]
## Esempi di Specifiche

### Form in Linguaggio Naturale

![[Pasted image 20251120114518.png]]
### PDL (Java-like)

![[Pasted image 20251120114616.png]]
Specifica di interfaccia basata su PDL:

![[Pasted image 20251120114814.png]]
# Chi legge i requisiti?

![[Pasted image 20251120105935.png]]
# Categorie di requisiti

## Requisiti Funzionali

Descrivono le funzionalità ovvero i servizi che il sistema software deve fornire e come esso si comporta in situazioni particolari, ad esempio come il sistema software reagisce a specifici tipi di input.

**Esempi**:
1. Il sistema software deve fornire un appropriato visualizzatore per i documenti memorizzati.
2. L’utente deve essere in grado di effettuare ricerche sia sull'intero insieme di basi di dati che su un loro sottoinsieme.
3. Ad ogni nuovo ordine deve essere associato un identificatore unico (Order_ID).
## Requisiti non Funzionali

Descrivono vincoli relativi alle funzioni od al processo di sviluppo del sistema software:

**Esempi**:
- **Caratteristiche software**: efficienza, affidabilità, sicurezza, ecc.
- **Caratteristiche del processo di sviluppo**: standard di processo, uso di ambienti CASE, linguaggi di programmazione, metodi di sviluppo, ecc.
- **Caratteristiche esterne**: interoperabilità con sistemi di altre organizzazioni, vincoli legislativi, ecc.

**Esempi**:
1. Il tempo di risposta del sistema all'inserimento della password utente deve essere inferiore a 10 sec.
2. II documenti di progetto (deliverable) devono essere conformi allo standard XYZ-ABC-12345.
3. Il sistema software non deve rilasciare ai suoi operatori nessuna informazione personale relativa ai clienti, tranne nominativo e identificatore.
## Requisiti di Dominio

Non sono dati dagli utenti ma derivati dal dominio applicativo del sistema software. Solitamente sono dati da vincoli legali legati al dominio applicativo.

**Esempi**:
1. I documenti di rendiconto contabile, secondo la normativa XYZ.03, devono essere stampati alla ricezione e cancellati immediatamente.
2. L'interfaccia utente per l'accesso al database magazzino deve essere conforme allo standard ZX.01.
# Classificazione dei requisiti non funzionali

![[Pasted image 20251120112258.png]]
# Problemi con i requisiti software

1. **Ambiguità**: i requisiti possono essere interpretati in modo differente.
2. **Incompletezza**: i requisiti non includono la descrizione di tutte le caratteristiche richieste.
3. **Inconsistenza**: conflitti o contraddizioni nella descrizione delle caratteristiche del sistema.

**Esempi**:
1. Specificare un tempo senza fornire il riferimento al fuso orario in un applicazione che gestisce chiamate intercontinentali.
2. Significato di "appropriato visualizzatore".
	- Interpretazione utente: visualizzatore specifico per ogni tipo di documento.
	- Interpretazione sviluppatore: generico visualizzatore di testo che mostri il contenuto del documento.
3. Ogni forma di input non deve contenere più di 5 campi editabili dall'utente.
4. Nella form di input relativa all'inserimento dei dati anagrafici l'utente deve introdurre i seguenti dati: nome, cognome, anno di nascita, luogo di nascita, indirizzo, telefono, fax, e-mail.
# Verificabilità dei requisiti

I requisiti vanno espressi usando una unità di misura che permetta di verificare quantitativamente se essi verranno soddisfatti dal sistema software. Quelli espressi in modo generico dall'utente possono risultare non quantificabili e difficili da verificare.

**Esempio**: il sistema software dev'essere facile da usare.
## Esempi di misure per requisiti

![[Pasted image 20251120113305.png]]

# Il documento di analisi dei requisiti (o documento di specifica)

Documento ufficiale che descrive in dettaglio le caratteristiche del sistema Software. Include sia la **definizione** dei requisiti che la loro **specifica**. Descrive **cosa** il sistema deve fornire (dominio del problema) e non **come** il sistema deve essere sviluppato (dominio della soluzione).
# Utenti del documento di analisi dei requisiti

![[Pasted image 20251120115358.png]]
# Struttura del Documento delle Specifiche

Basata sullo standard IEEE 830-1998 (IEEE Recommended Practice for Software Requirements Specifications).

- **Prefazione**: pubblico di lettori previsto, cronologia delle versioni, riepilogo delle modifiche
- **Introduzione**: scopo, descrizione sintetica del sistema, interazione con altri sistemi, ambito di applicazione nel contesto aziendale
- **Glossario**: definizione dei termini tecnici utilizzati nel documento
- **Definizione dei requisiti utente**: requisiti funzionali e non funzionali dell'utente
- **Architettura del sistema**: panoramica di alto livello dei componenti del sistema
- **Specifica dei requisiti di sistema**: requisiti funzionali e non funzionali del sistema
- **Modelli di sistema**: descrizione delle relazioni tra i componenti del sistema e tra il sistema e il suo ambiente
- **Evoluzione del sistema**: presupposti su cui si basa il sistema e cambiamenti previsti (evoluzione hardware, modifiche alle esigenze utente, ecc.)
- **Appendici**: informazioni specifiche relative all'applicazione in sviluppo (es. descrizioni hardware e database)
- **Indice**: indice generale, indice analitico, elenco dei diagrammi, ecc.


