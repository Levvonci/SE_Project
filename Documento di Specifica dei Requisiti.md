<center><h1>Table Flow</h1></center>

![[TableFlow_Logo.png | center | 600]]

<center><p>Ascenzi Leonardo (0310858)<br> Folco Damiano (0310549)<br> Spadoni Nicoló (0311175)<br> Zheng Simone (0293045) </p>
</center>


# Prefazione

## Pubblico di Lettori Previsto

Il presente documento è redatto per soddisfare le esigenze informative di diversi stakeholder coinvolti nel ciclo di vita del sistema `TableFlow`:

- **Committente e Stakeholder Business**: Proprietari di ristoranti, food & beverage manager e investitori, per la valutazione delle funzionalità offerte e dell'aderenza ai requisiti operativi.
- **Team di Sviluppo e Progettisti**: Ingegneri del software, architetti sistemisti e sviluppatori, come linea guida per le attività di progettazione, implementazione e testing.
- **Team di Qualità e Testing**: Per la definizione dei piani di test e dei criteri di accettazione.
- **Docenti e Commissione d'Esame**: Per la valutazione del progetto nell'ambito del corso di Ingegneria del Software.
- **Utenti Finali**: Personale di sala, cucina e amministrazione, per la comprensione delle funzionalità a loro dedicate.

Il documento presuppone nel lettore una conoscenza di base dei processi di ristorazione e dei principi fondamentali dell'ingegneria del software.

## Cronologia delle Versioni

| Versione | Data       | Autori               | Descrizione                                           |
| -------- | ---------- | -------------------- | ----------------------------------------------------- |
| 0.1      | 15/11/2025 | L. Ascenzi, D. Folco | Bozza iniziale - Struttura documento e requisiti base |
| 0.2      | 25/11/2025 | N. Spadoni, S. Zheng | Ampliamento requisiti funzionali e casi d'uso         |
| 0.5      | 05/12/2025 | D. Folco, S. Zheng   | Prima versione completa per revisione interna         |
| 0.8      | 15/12/2025 | L. Ascenzi, S. Zheng | Integrazione glossario e requisiti non funzionali     |
| 0.9      | 20/12/2025 | D. Folco, N. Spadoni | Revisione finale e verifica consistenza               |
| 1.0      | 22/12/2025 | D. Folco, S. Zheng   | Versione finale approvata per la consegna             |

## Riepilogo delle Modifiche Principali

**Versione 0.1 → 0.2 (25/11/2025)**
- Aggiunta sezione "Definizione dei Requisiti Utente"
- Inserimento dei primi 5 requisiti funzionali
- Definizione degli scenari d'uso principali

**Versione 0.2 → 0.5 (05/12/2025)**
- Espansione del glossario con 15 nuovi termini
- Specifica dei requisiti non funzionali (prestazioni, usabilità, affidabilità)

**Versione 0.5 → 0.8 (15/12/2025)**
- Integrazione requisiti gestione magazzino
- Aggiunta figure professionali (Executive Chef, Sommelier, Runner)
- Specifica dell’architettura hardware
- Definizione dei requisti non funzionali

**Versione 0.8 → 0.9 (20/12/2025)**
- Revisione completa della consistenza terminologica
- Ottimizzazione della struttura documentale
- Correzione errori minori e refusi

**Versione 0.9 → 1.0 (22/12/2025)**
- Approvazione finale del team
- Allineamento con le specifiche del corso
- Preparazione per la consegna ufficiale

# Indice

- [[#Introduzione]]
	- [[#1. Scopo del Documento]]
	- [[#2. Descrizione Sintetica del Sistema]]
	- [[#3. Interazione con Altri Sistemi]]
	- [[#4. Ambito di Applicazione nel Contesto Aziendale]]
- [[#Glossario]]
	- [[#A]]
	- [[#B]]
	- [[#C]]
	- [[#D]]
	- [[#E]]
	- [[#F]]
	- [[#G]]
	- [[#I]]
	- [[#M]]
	- [[#O]]
	- [[#P]]
	- [[#R]]
	- [[#S]]
	- [[#T]]
	- [[#U]]
	- [[#V]]
- [[#Definizione dei Requisiti Utente]]
	- [[#1. REQUISITI FUNZIONALI]]
		- [[#1.1 Gestione Prenotazioni]]
		- [[#1.2 Gestione Ordinazioni]]
		- [[#1.3 Gestione Produzione]]
		- [[#1.4 Gestione Pagamenti]]
		- [[#1.5 Gestione Magazzino]]
		- [[#1.6 Gestione Finanziaria e Reportistica]]
	- [[#2. REQUISITI NON FUNZIONALI]]
		- [[#RNF01 - PERFORMANCE TEMPI REALI]]
		- [[#RNF02 - AFFIDABILITÀ OPERATIVA CONTINUA]]
		- [[#RNF03 - SICUREZZA E TRACCIABILITÀ]]
		- [[#RNF04 - USABILITÀ E FORMAZIONE]]
		- [[#RNF05 - SCALABILITÀ E CARICO]]
		- [[#BONUS RNF06 - MANUTENIBILITÀ OPERATIVA]]
	- [[#3. REQUISITI DI DOMINIO]]
		- [[#3.1 Legali e Fiscali]]
		- [[#3.2 Hardware]]
	- [[#4. SCENARI D'USO]]
		- [[#RF001 - Prenotazione Tavoli]]
		- [[#RF002 - Presa Comanda]]
		- [[#RF003 - Modifica Comanda]]
		- [[#RF004 - Invio Cucina]]
		- [[#RF005 - Comunicazione Cucina-Sala]]
		- [[#RF006 - Gestione Intestazione]]
		- [[#RF007 - Gestione Conto]]
		- [[#RF008 - Controllo Giacenze]]
		- [[#RF009 - Analisi Finanziaria]]
- [[#Analisi Dei Requisiti]]
	- [[#Class Diagram]]
- [[#Modello Comportamentale]]
	- [[#Diagramma dei casi d’uso]]
	- [[#Activity Diagrams]]
		- [[#Prenotazione Tavoli]]
		- [[#Presa Comanda]]
		- [[#Modifica Comanda]]
		- [[#Invio Cucina]]
		- [[#Gestione Intestazione]]
		- [[#Comunicazione Cucina Sala]]
		- [[#Gestione Conto]]
		- [[#Controllo Giacenze]]
		- [[#Analisi Finanziaria]]
	- [[#Sequence Diagrams]]
		- [[#Prenotazione Tavoli]]
		- [[#Presa Comanda]]
		- [[#Modifica Comanda]]
		- [[#Invio Cucina]]
		- [[#Gestione Intestazione]]
		- [[#Comunicazione Cucina-Sala]]
		- [[#Gestione Conto]]
		- [[#Controllo Giacenza]]
		- [[#Analisi Finanziaria]]
- [[#Architettura di Sistema]]
	- [[#1. Struttura Generale]]
	- [[#2. Componenti Principali]]
		- [[#Backend (Server)]]
		- [[#Client (Dispositivi)]]
	- [[#3. Comunicazione]]
	- [[#4. Modalità Operativa]]
	- [[#5. Sicurezza Base]]
- [[#Design Pattern]]
	- [[#Pattern Selezionati ed Applicazione]]
		- [[#1. Factory Method]]
		- [[#2. Observer]]
		- [[#3. Decorator]]
		- [[#4. Composite]]
		- [[#5. Template Method]]
- [[#Evoluzione del sistema]]
	- [[#Estensibilità verso Camerieri Robot e Droni di Consegna]]
- [[#Appendice]]
	- [[#A. Riferimenti Normativi]]
	- [[#B. Matrice di Tracciabilità Requisiti]]
	- [[#C. Acronimi e Terminologia Tecnica]]

# Introduzione

## 1. Scopo del Documento

Questo documento costituisce la *Specifica dei Requisiti Software* per il sistema di automazione e gestione di ristoranti/pasticcerie/bar **TableFlow**. Lo scopo è definire in modo chiaro, completo e non ambiguo i requisiti funzionali e non funzionali del sistema, servendo come fonte di riferimento univoca per:

*   **Il Committente**: per convalidare che il sistema rispecchi le esigenze operative e strategiche.
*   **Il Team di Sviluppo**: come linea guida per la progettazione, l'implementazione e i test del sistema.
*   **Il Project Management**: per pianificare le attività e garantire che la consegna del prodotto finale sia allineata con quanto concordato.

## 2. Descrizione Sintetica del Sistema

`TableFlow` è un sistema software integrato progettato per ottimizzare e digitalizzare l'intero flusso operativo di un ristorante/pasticceria/bar moderno. La piattaforma centralizza le seguenti aree critiche:

* **Front-of-House**: Gestione delle ordinazioni tramite terminale d'ordine (POS) e tramite tablet per il servizio al tavolo.
* **Back-of-House**: Comunicazione digitale e in tempo reale con l'area cucina, l'area bar e l'area pasticceria con gestione degli ordini e degli stati di preparazione.
* **Amministrazione**: Controllo completo del magazzino, gestione del personale, analisi delle vendite e reportistica finanziaria.

L'obiettivo primario è creare un ecosistema che aumenti l'efficienza, migliori l'esperienza cliente e fornisca dati per supportare le decisioni gestionali.

## 3. Interazione con Altri Sistemi
Il sistema `TableFlow` dovrà interfacciarsi e integrarsi con i seguenti sistemi esterni:
* **Sistemi di Pagamento Elettronico**: per l'elaborazione di transazioni con carte di credito/debito e servizi di pagamento digitale (es. Visa, MasterCard, Satispay, SumUp).
* **Sistema di Contabilità**: per l'esportazione automatica dei dati delle vendite e IVA.

### Future Integrazioni:
* **Piattaforme di Food Delivery Aggregator**: per ricevere e gestire ordinativi da piattaforme terze come Just Eat, Deliveroo e Glovo.
* **Sistemi di Prenotazione Online**: per sincronizzare la disponibilità dei tavoli con servizi come TheFork.

## 4. Ambito di Applicazione nel Contesto Aziendale
Questo progetto si inserisce nella strategia di innovazione digitale e miglioramento della redditività di un azienda di somministrazione di cibi e bevande (ristoranti/pasticcerie/bar). Il sistema supporterà direttamente le seguenti figure professionali:
*   **Proprietario/General Manager**: Per il monitoraggio delle performance e la gestione centralizzata.
*   **Camerieri**: Per l'assunzione degli ordini e la gestione dei tavoli.
*   **Personale di Cucina**: Per la visualizzazione e preparazione degli ordini.
*   **Cassiere/Maitre**: Per la gestione delle entrate e uscite.

# Glossario

## A
**Allergene**
- Sostanza che può provocare reazioni allergiche (glutine, lattosio, frutta a guscio, ecc.)
- Nel sistema: categoria associata agli ingredienti e ai piatti

**Articolo**
- Qualsiasi prodotto venduto dal ristorante (piatto, bevanda, extra)
- Sinonimo: Voce di menu

## B
**Backoffice**
- Area riservata al personale per la gestione amministrativa
- Opposta al front-end cliente

## C
**Conto**
- Documento riepilogativo dell'ordine di un tavolo
- Sinonimo: Scontrino, Ricevuta

**Coperto**
- Costo fisso applicato per persona per servizio e pane
- Nel sistema: voce aggiuntiva automatica nel conto

**Corso**
- Fase del pasto (Antipasto, Primo, Secondo, Dolce)
- Nel sistema: categoria per organizzare i piatti nel menu

## D
**Dashboard**
- Schermata principale con indicatori prestazioni (KPI)
- Mostra: incassi, tavoli occupati, tempi medi, ecc.

## E
**Executive Chef**
- Responsabile supremo della cucina e della creazione del menu
- Nel sistema: utente con permessi per modificare menu e costi piatti
## F
**Fattura**
- Documento fiscale per acquisti da fornitori o vendite a clienti business    
- Distinta dalla ricevuta per clienti finali

**Food & Beverage Manager**
- Responsabile dell'intera operatività di ristorante e bar    
- Nel sistema: utente con accesso completo a report e analisi

**Fornitore**
- Azienda che rifornisce il ristorante (alimenti, bevande, materiali)
- Nel sistema: anagrafica per gestione acquisti

## G
**General Manager**
- Direttore generale del ristorante, responsabile delle operazioni complessive
- Nel sistema: super-user con tutti i privilegi amministrativi

**Giacenza**
- Quantità di prodotto disponibile in magazzino
- Sinonimo: Scorta, Stock

## I
**Ingrediente**
- Componente base di un piatto
- Nel sistema: associato a allergeni e giacenze

## M
**Menu**
- Insieme organizzato di piatti e bevande offerti
- Tipologie: à la carte, fisso, degustazione, giornaliero

**Modifica Piatto**
- Variazione alla preparazione standard di un piatto
- Esempi: "senza cipolla", "piccante", "ben cotto"

## O
**Ordine**
- Richiesta di uno o più piatti/bevande per un tavolo
- Stati: Inserito, In Preparazione, Pronto, Servito

## P
**Prenotazione**
- Richiesta di riservare un tavolo per una data/ora
- Nel sistema: associata a cliente e note particolari

## R
**Ricetta**
- Elenco ingredienti e quantità per preparare un piatto
- Nel sistema: base per calcolo costi e consumo scorte

**Runner**
- Addetto al trasporto dei piatti dalla cucina al tavolo
- Nel sistema: può avere accesso limitato allo stato ordini

## S
**Fattura Elettronica**
- Documento fiscale emesso dal sistema secondo normativa
- Associato al numero di matricola del registratore di cassa

**Sommelier**
- Esperto di vini responsabile della cantina e abbinamenti
- Nel sistema: utente con permessi per gestione carta vini e vendite

**Stampa Cucina**
- Ordine inviato automaticamente alla cucina
- Può essere: stampante fisica o terminale video

## T
**Tavolo**
- Postazione fisica del ristorante
- Nel sistema: identificato da numero e con stati (Libero, Occupato, Prenotato)

**Turno**
- Periodo di lavoro del personale (pranzo, cena)
- Nel sistema: definisce orari e assegnazione personale

## U
**Utente**
- Persona abilitata all'uso del sistema
- Ruoli: Amministratore, Cassiere, Cameriere, Cuoco

## V
**Voce di Menu**
- Singolo elemento vendibile (piatto, bevanda, extra)
- Caratteristiche: prezzo, descrizione, categoria, allergeni, giacenza

# Definizione dei Requisiti Utente

## 1. REQUISITI FUNZIONALI

### 1.1 Gestione Prenotazioni
**RF001 - Prenotazione Tavoli**
**Attori:** Receptionist, Cliente
**Descrizione:** Sistema di prenotazione tavoli con conferma automatica.

**Receptionist deve poter:**
- Creare prenotazioni specificando: data, ora, numero persone, note speciali (allergie, celebrazioni).
- Visualizzare disponibilità tavoli in tempo reale.
- Modificare/cancellare prenotazioni esistenti.

**Software deve:**
- Bloccare sovrapposizioni di prenotazioni sullo stesso tavolo

### 1.2 Gestione Ordinazioni
**RF002 - Creazione Comanda**
**Attori:** Cameriere, Maitre
**Descrizione:** Creazione e gestione comande tavolo.

**Cameriere deve poter:**
- Creare nuova comanda associata a tavolo specifico
- Selezionare articoli (piatti/bevande) dal menù
- Applicare modifiche ai piatti (es. "senza coriandolo", "al sangue")
- Specificare quantità per ogni articolo
- Salvare comanda parziale/in sospeso

**Software deve:**
- Calcolare automaticamente totale parziale con IVA inclusa
- Visualizzare disponibilità articoli in tempo reale (collegamento magazzino)
- Gestire gli ordini d'asporto in maniera separata dagli ordini ai tavoli.

**RF003 - Modifica Comanda**
**Attori:** Cameriere, Maitre, Titolare
**Descrizione:** Modifica comande esistenti e tracciamento storico.

**Cameriere/Maitre devono poter:**
- Aggiungere nuovi articoli a comanda esistente
- Rimuovere articoli già inseriti
- Modificare quantità articoli esistenti

**Titolare/Manager deve poter:**
- Visualizzare storico completo modifiche per ogni comanda
- Tracciare chi ha effettuato ogni modifica (audit trail)
- Annullare modifiche in caso di errore

### 1.3 Gestione Produzione
**RF004 - Invio Ordini a Cucina/Bar**
**Descrizione:** Comunicazione automatica ordini alle aree produzione.

**Software deve:**
- Inviare automaticamente comanda a cucina/bar con timestamp
- Suddividere ordini per categoria (antipasti, primi, secondi, bevande)
- Supportare flag priorità/urgenza su voci specifiche
- Gestire ordini fuori menù con note speciali per la cucina

**RF005 - Comunicazione Cucina/Bar - Sala**
**Descrizione:** Sistema per la segnalazione dello stato della preparazione

**Chef deve:**
- Segnalare ai camerieri quando articoli sono "pronti al ritiro" oppure allertare ritardi.

**Software deve:**
- Permettere marcatura ordini come "completati/consegnati"
- Gestire annullamenti produzione (cambiamenti post-invio)

### 1.4 Gestione Pagamenti
**RF006 – Gestione Intestazione**
**Attori:** Receptionist
**Descrizione:** Sistema per la gestione dell’intestazione dei clienti che richiedono la fattura per il pagamento.

**Receptionist deve poter:**
- Inserire una nuova intestazione cliente per la fatturazione  
- Cercare il cliente tramite Partita IVA
- Inserire manualmente i dati se non recuperabili automaticamente dai server dell'Agenzia delle Entrate
- Verificare e modificare i dati dell’intestazione prima del salvataggio  

**Software deve:**
- Permettere l'invio della Partita IVA all’Agenzia delle Entrate per ottenere i dati dell’intestazione e compilare automaticamente i campi dell’intestazione in caso di riscontro positivo
- Segnalare eventuali errori o dati mancanti  
- Salvare l’intestazione cliente nel registro clienti  
- Rendere l’intestazione disponibile per l’emissione della fattura elettronica

**RF007 - Gestione Conto**
**Attori:** Receptionist
**Descrizione:** Sistema completo gestione pagamenti.

**Receptionist deve poter:**
- Dividere conto per numero persone/gruppi
- Emettere fattura/scontrino fiscale elettronico
- Stornare/annullare pagamenti errati

**Software deve:**
- Calcolare automaticamente IVA
- Inviare fatture elettroniche
- Generare scontrino o fattura
- Applicare mance (se in uso)

### 1.5 Gestione Magazzino
**RF008 - Controllo Giacenze**
**Attori:** Chef, Sommelier, Titolare/Manager
**Descrizione:** Sistema tracciamento inventario e scorte.

**Personale autorizzato deve poter:**
- Aggiornare quantità disponibili per ogni articolo (durante i rifornimenti)
- Segnalare danni/perdite/avarie

**Software deve:**
- Mostrare articoli non disponibili in tempo reale su terminali sala
- Calcolare costo ingredienti per piatto

### 1.6 Gestione Finanziaria e Reportistica
**RF009 - Analisi Finanziaria**
**Attori:** Titolare/Manager
**Descrizione:** Sistema reportistica avanzata per analisi business.

**Titolare/Manager deve poter visualizzare durante la chiusura fiscale giornaliera:**
- Fatturato totale.
- Numero totale fatture.
- Contributo percentuale di ogni articolo/categoria al fatturato.

## 2. REQUISITI NON FUNZIONALI

### RNF01 - PERFORMANCE TEMPI REALI
**Descrizione:** Il sistema deve garantire sincronizzazione in tempo reale tra tutti i dispositivi per operazioni critiche.

**Specifiche:**
- Sincronizzazione comande sala/cucina: **< 1 secondi**
- Aggiornamento disponibilità articoli su tutti i terminali: **< 1 secondi**
- Calcolo conto complesso (divisione per 8+ persone): **< 1 secondi**

### RNF02 - AFFIDABILITÀ OPERATIVA CONTINUA
**Descrizione:** Il sistema deve garantire continuità operativa anche in condizioni parzialmente degradate.

**Specifiche:**
- **Disponibilità:** > 99.7% durante orario apertura (12:00-24:00)
- **Modalità offline limitata:** Funzionalità base devono rimanere operative anche in caso di assenza di internet.
- **MTTR (Mean Time to Repair):** < 30 minuti per guasti software
- **Ripristino dati:** < 15 minuti di perdita dati in caso di crash

### RNF03 - SICUREZZA E TRACCIABILITÀ
**Descrizione:** Sistema di autorizzazioni granulari e tracciamento completo per compliance.

**Specifiche:**
- **Autenticazione:** Login univoco per ogni utente
- **Autorizzazioni:** Almeno 5 livelli distinti (cameriere, maitre, chef, receptionist, titolare)
- **GDPR:** Eliminazione automatica dati clienti dopo 24 mesi di inattività

### RNF04 - USABILITÀ E FORMAZIONE
**Descrizione:** Interfaccia ottimizzata per ambienti ad alto stress con curva apprendimento rapida.

**Specifiche:**
- **Tempo formazione base:** < 30 minuti per ruolo operativo (cameriere, receptionist)
- **Operazioni frequenti:** Massimo 3 tap/clic per:
    - Creare nuova comanda (RF002)
    - Applicare modifiche piatto (RF002)
    - Stampare conto (RF007)
- **Interfaccia tablet:** Ottimizzata per uso con guanti da cucina (minimo elementi 44x44px)
- **Contrasto schermi cucina:** Rapporto 7:1 per ambienti luminosi/affumicati
- **Fallback linguistico:** Terminologia standard italiana settore ristorazione

### RNF05 - SCALABILITÀ E CARICO
**Descrizione:** Sistema deve gestire picchi di carico tipici della ristorazione.

**Specifiche:**
- **Utenti concorrenti:** Supporto fino a:
    - 50 dispositivi sala contemporaneamente attivi
    - 15 terminali cucina/bar
    - 1000 prenotazioni attive in stesso servizio
- **Comande simultanee:** Gestione fino a 500 comande aperte contemporaneamente
- **Performance under load:** Degrado massimo 20% dei tempi di risposta con:
    - 300+ tavoli occupati
    - 100+ comande in preparazione contemporanea
- **Storage:** Capacità minima 100.000 comande/storico senza degradazione performance
- **Backup:** Incrementale notturno senza impatto performance diurna

### BONUS: RNF06 - MANUTENIBILITÀ OPERATIVA
**Descrizione:** Il personale non tecnico deve poter gestire configurazioni quotidiane.

**Specifiche:**
- **Modifica menù:** Operatore autorizzato può modificare prezzi/articoli senza riavvio sistema
- **Aggiornamenti:** Patch e aggiornamenti applicabili in orario di chiusura (03:00-06:00) automaticamente

## 3. REQUISITI DI DOMINIO

### 3.1 Legali e Fiscali
**RV001 - Conformità Legale**
- Integrazione registratore di cassa telematico (obbligo di legge)
- Tracciabilità IVA per categoria prodotto
- Conservazione documenti fiscali: 10 anni
- Conformità GDPR per dati clienti

**RV002 - Gestione Allergeni**
- Sistema segnalazione allergeni per ogni piatto (Reg. UE 1169/2011)
- Stampa automatica avvertenze su comande cucina
- Blocco ordinazioni in caso di allergie gravi segnalate

### 3.2 Hardware
**RV003 - Specifiche Minime Dispositivi**
- Tablet: Android 9.0+, 4GB RAM, schermo 10"
- Server: Windows 10/Server 2019+, 8GB RAM, 250GB SSD
- Connessione internet: banda minima 10 Mbps in download

## 4. SCENARI D'USO

### RF001 - Prenotazione Tavoli
*Scenario:* Cliente Rossi chiama vuole prenotare un tavolo di 6 persone per un compleanno
Receptionist Marco seleziona sala 1, visualizza che il tavolo 12 é disponibile, Marco crea la prenotazione data/ora/6 persone/note compleanno.
Marco conferma.

### RF002 - Presa Comanda  
*Scenario:* Cameriere Luca al tavolo 7. Sul tablet: seleziona tavolo → aggiunge "Carbonara" → modifica "senza pancetta" → aggiunge "Vino rosso" x2. Sistema calcola totale parziale €44. Comanda salvata.

### RF003 - Modifica Comanda
*Scenario:* Cliente chiede di aggiungere insalata e togliere patate. Maître Andrea modifica comanda esistente → sistema registra modifica nello storico. Giorno dopo, titolare controlla storico per reclamo: vede che patate furono rimosse ma riapparvero in conto per bug.

### RF004 - Invio Cucina
*Scenario:* Sara invia comanda tavolo 3 con bistecca urgente (cliente ha treno). Sistema: priorità ALTA, bordi rossi. In cucina, appare in cima a "SECONDI" con timer countdown.

### RF005 - Comunicazione Cucina-Sala
*Scenario:* Chef completa risotto → clicca "PRONTO". Sistema segnala a tablet camerieri: "Tavolo 5 - Risotto pronto". Dopo 20 minuti se non ritirato → sistema avvisa maître: "RITARDO - Risotto tavolo 5 in attesa".

### RF006 - Gestione Intestazione
*Scenario:* Un nuovo cliente conclude il pagamento e richiede la fattura. Il receptionist inserisce la Partita IVA. Il sistema invia la richiesta all’Agenzia delle Entrate per ricevere i dati dell’azienda. Se il sistema non riceve risposta dall’Agenzia delle Entrate, il receptionist inserisce manualmente i dati dell’intestazione e li verifica. L’intestazione viene salvata e memorizzata nel registro clienti ed è subito disponibile per l’emissione della fattura elettronica.

### RF007 - Gestione Conto
*Scenario:* Tavolo 8 persone, conto €320. Receptionist divide per 4 coppie: sistema separa automaticamente gli ordini di ogni coppia. Stampa scontrino separato per ciascuna coppia + fattura per chi la richiede.

### RF008 - Controllo Giacenze
*Scenario:* Arriva fornitura pomodori. Cuoco aggiorna magazzino: +50kg. Sistema ricalcola totale. A fine giornata, controlla soglie: burro sotto minimo (3kg vs 5kg) → invia alert a titolare. Nel frattempo, "Pizza margherita" mostra "NON DISP." sui tablet.

### RF009 - Analisi Finanziaria
_Scenario:_ Titolare/Manager chiude fiscalmente la cassa a fine giornata, il sistema deve calcolare il fatturato totale, l'IVA totale, il numero dei scontrini emessi ed il numero di fatture emesse. Successivamente deve inviare i corrispettivi all'Agenzia delle Entrate ed una volta ricevuta conferma di ricezione, stampare lo Scontrino di Chiusura Fiscale.

# Analisi Dei Requisiti
## Class Diagram
![[class_diagram_unrefined.png|center]]
# Modello Comportamentale

## Diagramma dei casi d’uso
![[use_case_diag.jpg|center|600]]
## Activity Diagrams
### Prenotazione Tavoli
![[Prenotazioni.jpg | center | 300]]

### Presa Comanda
![[Presa_Comanda.jpg| center | 600]]

### Modifica Comanda
![[img_document/Activity_Diagrams/Modifica_Comanda.jpg| center | 600]]

### Invio Cucina
![[Invio_Cucina.jpg | center | 300]]

### Gestione Intestazione
![[Nuovo_Cliente.jpg | center | 600]]

### Comunicazione Cucina Sala
![[Comunicazione_Cucina_Sala.jpg| center | 300]]

### Gestione Conto
![[Gestione_Conto.jpg | center | 600]]

### Controllo Giacenze
![[Controllo_Giacenze.jpg| center | 600]]

### Analisi Finanziaria
![[Gestione_Finanziaria.jpg| center | 600]]

## Sequence Diagrams
### Prenotazione Tavoli
![[Crea_Prenotazione.jpg| center | 660]]

### Presa Comanda
![[Crea_Comanda.jpg | center | 600]]

### Modifica Comanda
![[img_document/Sequence_Diagrams/Modifica_Comanda.jpg| center | 600]]

### Invio Cucina
![[Invia_Comanda.jpg|center|600]]

### Gestione Conto
![[Paga_Comanda.png | center | 600]]

### Gestione Intestazione
![[Nuovo_Cliente.png | center | 700]]

### Comunicazione Cucina-Sala
![[Comunicazione_Sala_Bar.png | center | 600]]

### Controllo Giacenza
![[Gestione_Magazzino.jpg| center | 660]]

### Analisi Finanziaria
![[Gestione_Finanziaria.png | center | 600]]
# Architettura di Sistema

## 1. Struttura Generale
TableFlow usa un'architettura **client-server** moderna:
- **Backend centrale** in cloud o server locale
- **Client leggeri** su vari dispositivi (tablet, PC, monitor cucina)
- **Database unico** sincronizzato per tutti

## 2. Componenti Principali

### Backend (Server)
- **API Centrali:** Gestiscono tutte le operazioni
- **Database:** PostgreSQL per dati strutturati (ordini, prenotazioni, magazzino)
- **Servizio Notifiche (Eventualmente in futuro)**

### Client (Dispositivi)
- **Tablet Sala:** App per camerieri
- **Monitor Cucina:** Interfaccia web semplice per chef
- **PC Reception:** Applicazione desktop per gestione
- **Mobile Manager:** App per titolare (iOS/Android)

## 3. Comunicazione
```
Tablet → WiFi/LTE → Server → Database
  ↓                    ↓
Cucina ← WebSocket ← Notifiche
```

## 4. Modalità Operativa
- **Online principale:** Tutti i dispositivi connessi a internet
- **Offline limitato:** Tablet salvano ordini localmente se internet cade
- **Sincronizzazione automatica** quando connessione ritorna

## 5. Sicurezza Base
- Login con username/password per ogni ruolo
- Accessi separati: camerieri vedono solo loro funzioni, titolare vede tutto
- Backup automatico giornaliero


# Design Pattern

Questa sezione descrive i design pattern selezionati per la progettazione e implementazione del sistema TableFlow. La scelta è motivata dalla necessità di garantire modularità, manutenibilità, estendibilità e conformità ai requisiti non funzionali specificati, in particolare RNF06 (Manutenibilità Operativa). I pattern individuati sono applicabili a diversi livelli dell'architettura e risolvono problemi specifici del dominio ristorativo.

## Pattern Selezionati ed Applicazione

### 1. Factory Method
**Problema risolto:** Creazione flessibile e centralizzata delle diverse tipologie di utenti del sistema, ciascuna con permessi, interfacce e comportamenti specifici.

**Applicazione in TableFlow:**
- **Creazione Utenti:** Implementazione di un metodo factory per istanziare oggetti `Utente` in base al ruolo (Cameriere, Cuoco, Maître, Receptionist, Titolare/General Manager). Ciascun ruolo possiede un set distinto di autorizzazioni definite in RNF03.
- **Configurazione Dinamica:** Il pattern permette di aggiungere nuovi ruoli futuri (es. Sommelier, Runner, Executive Chef) senza modificare il codice client esistente.
- **Esempio di Utilizzo:** Il sistema di autenticazione, dopo aver validato le credenziali, invoca `UserFactory.createUser(role, userData)` per ottenere l'istanza corretta con il profilo autorizzativo configurato.

**Vantaggi per il Sistema:**
- Isolamento della logica di creazione
- Aderenza al principio Open/Closed
- Supporto alla configurabilità richiesta in RNF06

### 2. Observer
**Problema risolto:** Sincronizzazione in tempo reale e segnalazione automatica di eventi critici a multipli componenti del sistema, come richiesto da RNF01 (Performance Tempi Reali).

**Applicazione in TableFlow:**
- **Segnalazione Stato Ordini:** La cucina (Subject) segnala automaticamente tutti i camerieri (Observers) quando un piatto passa allo stato "PRONTO", come descritto in RF007.
- **Aggiornamento Giacenze:** Il modulo magazzino (Subject) segnala i terminali di sala e il sistema di ordinazione (Observers) quando la disponibilità di un articolo cambia (RF006, RNF01).
- **Sistema di Alert:** Generazione di alert per soglie magazzino (RF008), ritardi di ritiro ordini (RF005).

**Vantaggi per il Sistema:**
- Accoppiamento debole tra produttori e consumatori di eventi
- Scalabilità nella gestione di alert
- Implementazione efficiente dei requisiti di tempo reale

### 3. Decorator
**Problema risolto:** Gestione dinamica e flessibile delle modifiche e personalizzazioni dei piatti ordinati, senza creare un'esplosione di sottoclassi.

**Applicazione in TableFlow:**
- **Modifiche ai Piatti:** Ogni modifica richiesta dal cliente (es. "senza pancetta", "ben cotto", "aggiunta formaggio") viene rappresentata come un Decorator che avvolge l'oggetto `PiattoBase`, aggiungendo o sovrascrivendo attributi (RF002).
- **Calcolo Costi Aggiornato:** I decoratori possono modificare il prezzo finale del piatto in base alla modifica applicata.
- **Comunicazione in Cucina:** Le modifiche decorate vengono visualizzate in modo evidenziato sui monitor cucina (RF004).

**Vantaggi per il Sistema:**
- Estensibilità delle funzionalità a runtime
- Struttura a composizione anziché ereditarietà
- Supporto a combinazioni complesse di modifiche

### 4. Composite
**Problema risolto:** Gestione uniforme di strutture gerarchiche parte-tutto, in particolare per la divisione dei conti e l'organizzazione del menu.

**Applicazione in TableFlow:**
- **Divisione Conti:** Gestione della suddivisione del conto totale in sotto-conti per gruppi o singoli clienti (RF005). Sia `ContoSingolo` che `ContoComposto` implementano la stessa interfaccia `Conto`, permettendo operazioni uniformi come `calcolaTotale()`.
- **Struttura Menu:** Rappresentazione gerarchica del menu con categorie (es. "Antipasti", "Primi") che contengono voci di menu (Composite Pattern ricorsivo).

**Vantaggi per il Sistema:**
- Trattamento uniforme di oggetti singoli e compositi
- Semplificazione del codice client
- Supporto naturale a operazioni ricorsive

### 5. Template Method
**Problema risolto:** Definizione dello scheletro di algoritmi complessi con passaggi variabili delegati alle sottoclassi.

**Applicazione in TableFlow:**
- **Flusso di Prenotazione:** La classe astratta `PrenotazioneProcess` definisce la sequenza fissa: verifica disponibilità → creazione prenotazione → invio conferma. 
- **Processo di Ordinazione:** Scheletro comune per la creazione di comande (RF002) con passaggi specifici per tipologie diverse (asporto vs tavolo).

**Vantaggi per il Sistema:**
- Eliminazione di duplicazione di codice
- Controllo centralizzato della struttura dell'algoritmo
- Flessibilità nei punti di variazione
# Evoluzione del sistema

## Estensibilità verso Camerieri Robot e Droni di Consegna
Il sistema è progettato con un'architettura API-first e modulare per permettere l'integrazione futura di camerieri robotici e droni per la consegna a domicilio. Le interfacce di gestione ordini e comande sono già strutturate per supportare dispositivi autonomi, con protocolli di comunicazione standardizzati che potranno essere estesi per includere comandi di navigazione, gestione tray robotizzati e coordinamento multi-agente. L'infrastruttura di gestione ordini a domicilio include già hook per l'integrazione con sistemi di delivery autonomo, prevedendo API specifiche per la pianificazione rotte drone, monitoraggio stato consegne in tempo reale e gestione autonoma degli slot di ricarica. L'astrazione dei layer di business logic dalla presentation layer consentirà di sostituire progressivamente le interfacce umane con controller per robot e flotte drone, mantenendo invariata la logica operativa mentre si evolve l'implementazione fisica del servizio.

# Appendice

## A. Riferimenti Normativi 
**Regolamento UE 1169/2011** - Obblighi informativi in materia di alimenti: gestione allergeni obbligatoria su comande cucina (RF002, RV002).
**D.Lgs. 127/2015** - Registratore di cassa telematico (RCF): integrazione plug-and-play per scontrini/fatture (RF007, RNF05).
**GDPR Reg. UE 2016/679** - Anonimizzazione dati clienti dopo 24 mesi inattività; audit trail 10 anni operazioni finanziarie (RNF03).

## B. Matrice di Tracciabilità Requisiti

| **RF/RNF ID** | **Use Case/Scenario** | **Test Case Proposto**            | **Status**   |
| ------------- | --------------------- | --------------------------------- | ------------ |
| RF001         | Prenotazione Tavoli   | TC001: Conferma WhatsApp          | Implementato |
| RF002         | Creazione Comanda     | TC002: Modifiche piatto           | Implementato |
| RF007         | Gestione Conto        | TC007: Divisione conto            | Implementato |
| RF009         | Gestione Turni        | TC009: Conflitti turni            | Da Testare   |
| RNF01         | Performance <1s       | TC_NF01: Load test 50 comande     | Da Testare   |
| RNF03         | Audit Trail           | TC_NF03: Traccia modifiche prezzi | Implementato |

## C. Acronimi e Terminologia Tecnica

| **Acronimo** | **Definizione**                       | **Riferimento**             |
| ------------ | ------------------------------------- | --------------------------- |
| RCF          | Registratore Cassa Fiscale Telematico | RF007, RV001                |
| MTTR         | Mean Time To Repair                   | RNF02 (<30 minuti)          |
| KPI          | Key Performance Indicator             | RF010 DashBoard             |
| POS          | Point of Sale                         | Introduzione Front-Of-House |
| 2FA          | Two Factor Authentication             | RNF03 Amministratori        |
