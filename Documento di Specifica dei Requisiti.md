# Table Flow
![[TableFlow_Logo.png | center | 600]]
- Ascenzi Leonardo (0310858)
- Folco Damiano (0310549)
- Spadoni Nicoló (0311175)
- Zheng Simone (0293045)

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
- Introduzione dei criteri di accettazione
- Definizione dei vincoli progettuali

**Versione 0.5 → 0.8 (15/12/2025)**
- Integrazione requisiti gestione magazzino
- Aggiunta figure professionali (Executive Chef, Sommelier, Runner)
- Specifica delle interfacce con sistemi esterni
- Definizione delle metriche di performance

**Versione 0.8 → 0.9 (20/12/2025)**
- Revisione completa della consistenza terminologica
- Verifica tracciabilità requisiti-casi d'uso
- Ottimizzazione della struttura documentale
- Correzione errori minori e refusi

**Versione 0.9 → 1.0 (22/12/2025)**
- Approvazione finale del team
- Allineamento con le specifiche del corso
- Preparazione per la consegna ufficiale

Il documento rappresenta lo stato completo dei requisiti per la versione 1.0 del sistema TableFlow e costituisce la base di riferimento per lo sviluppo e la validazione del progetto.

*Il Team TableFlow*  
*Dicembre 2025*

# Indice

- [Introduzione](#introduzione)
  - [1. Scopo del Documento](#1-scopo-del-documento)
  - [2. Descrizione Sintetica del Sistema](#2-descrizione-sintetica-del-sistema)
  - [3. Interazione con Altri Sistemi](#3-interazione-con-altri-sistemi)
  - [4. Ambito di Applicazione nel Contesto Aziendale](#4-ambito-di-applicazione-nel-contesto-aziendale)
- [Glossario](#glossario)
- [Definizione dei Requisiti Utente](#definizione-dei-requisiti-utente)
  - [1. REQUISITI FUNZIONALI](#1-requisiti-funzionali)
    - [1.1 Gestione Prenotazioni](#11-gestione-prenotazioni)
      - [RF001 - Prenotazione Tavoli](#rf001---prenotazione-tavoli)
    - [1.2 Gestione Ordinazioni](#12-gestione-ordinazioni)
      - [RF002 - Creazione Comanda](#rf002---creazione-comanda)
      - [RF003 - Modifica Comanda](#rf003---modifica-comanda)
    - [1.3 Gestione Produzione](#13-gestione-produzione)
      - [RF004 - Invio Ordini a Cucina/Bar](#rf004---invio-ordini-a-cucinabar)
      - [RF005 - Visualizzazione Comande in Cucina/Bar](#rf005---visualizzazione-comande-in-cucinabar)
      - [RF006 - Comunicazione Cucina/Bar - Sala](#rf006---comunicazione-cucinabar---sala)
    - [1.4 Gestione Pagamenti](#14-gestione-pagamenti)
      - [RF007 - Gestione Conto](#rf007---gestione-conto)
    - [1.5 Gestione Magazzino](#15-gestione-magazzino)
      - [RF008 - Controllo Giacenze](#rf008---controllo-giacenze)
    - [1.6 Gestione Personale](#16-gestione-personale)
      - [RF009 - Gestione Turni](#rf009---gestione-turni)
    - [1.7 Gestione Finanziaria e Reportistica](#17-gestione-finanziaria-e-reportistica)
      - [RF010 - Analisi Finanziaria](#rf010---analisi-finanziaria)
  - [2. REQUISITI NON FUNZIONALI](#2-requisiti-non-funzionali)
    - [RNF01 - PERFORMANCE TEMPI REALI](#rnf01---performance-tempi-reali)
    - [RNF02 - AFFIDABILITÀ OPERATIVA CONTINUA](#rnf02---affidabilità-operativa-continua)
    - [RNF03 - SICUREZZA E TRACCIABILITÀ](#rnf03---sicurezza-e-tracciabilità)
    - [RNF04 - USABILITÀ E FORMAZIONE](#rnf04---usabilità-e-formazione)
    - [RNF05 - INTEGRAZIONE E INTEROPERABILITÀ](#rnf05---integrazione-e-interoperabilità)
    - [RNF06 - SCALABILITÀ E CARICO](#rnf06---scalabilità-e-carico)
    - [BONUS: RNF07 - MANUTENIBILITÀ OPERATIVA](#bonus-rnf07---manutenibilità-operativa)
  - [3. REQUISITI DI DOMINIO](#3-requisiti-di-dominio)
    - [3.1 Legali e Fiscali](#31-legali-e-fiscali)
      - [RV001 - Conformità Legale](#rv001---conformità-legale)
      - [RV002 - Gestione Allergeni](#rv002---gestione-allergeni)
    - [3.2 Hardware](#32-hardware)
      - [RV003 - Specifiche Minime Dispositivi](#rv003---specifiche-minime-dispositivi)
- [Use Case Diagram](#use-case-diagram)
- [Documentazione](#documentazione)
- [System Architecture](#system-architecture)
- [System Architectural Models](#system-architectural-models)
  - [Activity Diagrams](#activity-diagrams)
    - [Prenotazioni](#prenotazioni)
  - [Sequence Diagrams](#sequence-diagrams)
  - [Class Diagram](#class-diagram)
    - [Class diagram unrefined](#class-diagram-unrefined)
    - [Class diagram refined](#class-diagram-refined)
- [Design Pattern](#design-pattern)
- [Evoluzione del sistema](#evoluzione-del-sistema)
  - [Estensibilità verso Camerieri Robot e Droni di Consegna](#estensibilità-verso-camerieri-robot-e-droni-di-consegna)
- [Appendice](#appendice)

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
* **Piattaforme di Food Delivery Aggregator**: per ricevere e gestire ordinativi da piattaforme terze come Just Eat, Deliveroo e Glovo.
* **Sistema di Contabilità**: per l'esportazione automatica dei dati delle vendite e IVA.
* **Sistemi di Prenotazione Online**: per sincronizzare la disponibilità dei tavoli con servizi come TheFork.

## 4. Ambito di Applicazione nel Contesto Aziendale
Questo progetto si inserisce nella strategia di innovazione digitale e miglioramento della redditività di un azienda di somministrazione di cibi e bevande (ristoranti/pasticcerie/bar). Il sistema supporterà direttamente le seguenti figure professionali:
*   **Proprietario/General Manager**: Per il monitoraggio delle performance e la gestione centralizzata.
*   **Camerieri**: Per l'assunzione degli ordini e la gestione dei tavoli.
*   **Personale di Cucina**: Per la visualizzazione e preparazione degli ordini.
*   **Cassiere/Maitre**: Per la gestione delle entrate e uscite.

**Esclusioni dall'ambito**: Lo sviluppo di hardware customizzato, la gestione delle risorse umane (payroll, contratti) e il marketing attivo sui social media non fanno parte del presente progetto.

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
- Visualizzare disponibilità tavoli in tempo reale con calendario/planimetria.
- Modificare/cancellare prenotazioni esistenti.
- Gestire liste d'attesa automatiche.

**Software deve:**
- Inviare automaticamente conferma via WhatsApp/email al numero/indirizzo associato alla prenotazione
- Inviare promemoria 24 ore prima della prenotazione
- Bloccare sovrapposizioni di prenotazioni sullo stesso tavolo
- Generare report statistiche prenotazioni (tasso occupazione, no-show)

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

**Titolare/General Manager deve poter:**
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

**RF005 - Visualizzazione Comande in Cucina/Bar**
**Descrizione:** Sistema di visualizzazione ottimizzato per aree produzione.

**Software deve visualizzare:**
- Comande in arrivo con dettagli completi (note, priorità)
- Organizzazione per tipo piatto e ordine cronologico
- Evidenziazione modifiche speciali (allergie, preferenze)

**RF006 - Comunicazione Cucina/Bar - Sala**
**Descrizione:** Sistema notifiche per coordinamento produzione-servizio.

**Software deve:**
- Notificare ai camerieri quando articoli sono "pronti al ritiro"
- Implementare sistema allerta ritardi (oltre tempo atteso)
- Permettere marcatura ordini come "completati/consegnati"
- Gestire annullamenti produzione (cambiamenti post-invio)

### 1.4 Gestione Pagamenti
**RF007 - Gestione Conto**
**Attori:** Receptionist, Cliente
**Descrizione:** Sistema completo gestione pagamenti.

**Receptionist deve poter:**
- Dividere conto per numero persone/gruppi
- Applicare automaticamente coperto (se previsto)
- Emettere fattura/scontrino fiscale elettronico
- Stornare/annullare pagamenti errati

**Software deve:**
- Calcolare automaticamente IVA per categoria prodotto
- Integrarsi con registratore di cassa telematico
- Generare ricevuta digitale inviabile via email/WhatsApp
- Tracciare mance (se applicabili)

### 1.5 Gestione Magazzino
**RF008 - Controllo Giacenze**
**Attori:** Cuoco, Barman, Titolare, General Manager
**Descrizione:** Sistema tracciamento inventario e scorte.

**Personale autorizzato deve poter:**
- Aggiornare quantità disponibili per ogni articolo (rifornimenti)
- Registrare uscite/consumi giornalieri
- Segnalare danni/perdite/avarie

**Software deve:**
- Generare notifiche automatiche quando scorte scendono sotto soglia minima
- Mostrare articoli non disponibili in tempo reale su terminali sala
- Generare report consumi giornalieri/settimanali
- Calcolare costo ingredienti per piatto
- Suggerire ordini fornitori basati su consumi storici

### 1.6 Gestione Personale
**RF009 - Gestione Turni**
**Attori:** Titolare, General Manager
**Descrizione:** Sistema pianificazione e controllo risorse umane.

**Direttore deve poter:**
- Creare e modificare turni di lavoro
- Assegnare personale a zone specifiche (sale)
- Gestire richieste ferie/permessi

**Software deve:**
- Generare report ore lavorate per dipendente (periodo personalizzabile)
- Calcolare totale assenze/malattie/permessi
- Avvisare in caso di conflitti turni/sottodimensionamento

### 1.7 Gestione Finanziaria e Reportistica
**RF010 - Analisi Finanziaria**
**Attori:** Titolare, General Manager
**Descrizione:** Sistema reportistica avanzata per analisi business.

**Titolare/General Manager deve poter visualizzare:**
- Fatturato totale per periodo personalizzabile (giorno/settimana/mese/anno)
- Contributo percentuale di ogni articolo/categoria al fatturato
- Andamento prenotazioni e tasso occupazione
- Tempo medio permanenza cliente per tavolo

**Software deve generare:**
- Report performance camerieri (ordini gestiti, errori, feedback)
- Analisi vendite incrociate (piatti più abbinati)
- Previsioni di affluenza basate su dati storici
- Report fiscali per commercialista

## 2. REQUISITI NON FUNZIONALI

### RNF01 - PERFORMANCE TEMPI REALI

**Descrizione:** Il sistema deve garantire sincronizzazione in tempo reale tra tutti i dispositivi per operazioni critiche.

**Specifiche:**
- Sincronizzazione comande sala/cucina: **< 1 secondi**
- Aggiornamento disponibilità articoli su tutti i terminali: **< 1 secondi**
- Notifica "pronto al ritiro" a camerieri: **< 1 secondi** dalla marcatura in cucina
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
- **Autenticazione:** Login univoco per ogni utente con 2FA per ruoli amministrativi
- **Autorizzazioni:** 5 livelli distinti (cameriere, maitre, cuoco, receptionist, titolare)
- **Audit Trail:** Registrazione completa di:
    - Modifiche prezzi (RF007/IVA) - chi, quando, da quale valore a quale valore
    - Storno pagamenti (RF007) - con motivo obbligatorio
    - Modifiche giacenze (RF008) - differenza quantità, operatore
- **Retention log:** 10 anni per operazioni finanziarie (compliance fiscale)
- **GDPR:** Anonimizzazione automatica dati clienti dopo 24 mesi di inattività

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

### RNF05 - INTEGRAZIONE E INTEROPERABILITÀ

**Descrizione:** Sistema deve integrarsi con ecosistemi esterni senza richiedere intervento manuale.

**Specifiche:**
- **API Standard:** RESTful API documentata per:
    - Importazione/exportazione menù (RF002)
    - Sincronizzazione dati contabili (RF010)
    - Integrazione piattaforme delivery
- **Formati supportati:**
    - Import: CSV, Excel (xlsx), JSON
    - Export: PDF (scontrini), Excel (report), XML (fatture elettroniche)
- **Stampanti:** Supporto nativo per 10+ modelli comuni cucina/bar (Epson, Star)
- **RCF Telematico:** Integrazione plug-and-play con principali marchi (Datev, Zucchetti)
- **Notifiche:** Supporto multiplo (WhatsApp Business API, SMTP, SMS gateway)

### RNF06 - SCALABILITÀ E CARICO

**Descrizione:** Sistema deve gestire picchi di carico tipici della ristorazione.

**Specifiche:**
- **Utenti concorrenti:** Supporto fino a:
    - 50 dispositivi sala contemporaneamente attivi
    - 15 terminali cucina/bar
    - 300 prenotazioni attive in stesso servizio
        
- **Comande simultanee:** Gestione fino a 50 comande aperte contemporaneamente
- **Performance under load:** Degrado massimo 20% dei tempi di risposta con:
    - 30+ tavoli occupati
    - 10+ comande in preparazione contemporanea
- **Storage:** Capacità minima 10.000 comande/storico senza degradazione performance
- **Backup:** Incrementale notturno senza impatto performance diurna

### BONUS: RNF07 - MANUTENIBILITÀ OPERATIVA

**Descrizione:** Il personale non tecnico deve poter gestire configurazioni quotidiane.

**Specifiche:**
- **Modifica menù:** Operatore autorizzato può modificare prezzi/articoli senza riavvio sistema
- **Aggiornamenti:** Patch e aggiornamenti applicabili in orario di chiusura (01:00-06:00) automaticamente
- **Dashboard monitoraggio:** Stato sistema visibile in tempo reale (server, stampanti, connessioni)
- **Self-diagnostic:** Sistema rileva automaticamente:
    - Stampante cucina offline > 5 minuti
    - Soglia magazzino raggiunta (RF008)
    - Errori integrazione RCF
- **Rollback configurazione:** Ripristino ultima configurazione stabile con 1 clic

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
*Scenario:* Cliente Rossi chiama per prenotare. Receptionist Marco inserisce data/ora/6 persone/note compleanno. Sistema mostra tavolo 12 disponibile. Marco conferma → sistema invia WhatsApp automatico a Rossi: "Prenotazione confermata, tavolo 12, sabato 20:30".

### RF002 - Presa Comanda  
*Scenario:* Cameriere Luca al tavolo 7. Sul tablet: seleziona tavolo → aggiunge "Carbonara" → modifica "senza pancetta" → aggiunge "Vino rosso" x2. Sistema calcola totale parziale €44. Comanda salvata.

### RF003 - Modifica Comanda
*Scenario:* Cliente chiede di aggiungere insalata e togliere patate. Maître Andrea modifica comanda esistente → sistema registra modifica nello storico. Giorno dopo, titolare controlla storico per reclamo: vede che patate furono rimosse ma riapparvero in conto per bug.

### RF004 - Invio Cucina
*Scenario:* Sara invia comanda tavolo 3 con bistecca urgente (cliente ha treno). Sistema: timestamp 20:45, priorità ALTA, bordi rossi. In cucina, appare in cima a "SECONDI" con timer countdown.

### RF005 - Gestione Conto
*Scenario:* Tavolo 8 persone, conto €320. Receptionist divide per 4 coppie: sistema separa automaticamente gli ordini di ogni coppia. Stampa scontrino separato per ciascuna coppia + fattura per chi la richiede.

### RF006 - Visualizzazione Cucina
*Scenario:* In cucina, monitor mostra: a sinistra antipasti ordinati, centro primi, destra secondi. Ordine cronologico. Carbonara "senza pancetta" evidenziata in giallo. Allergia "glutine" in rosso lampeggiante.

### RF007 - Comunicazione Cucina-Sala
*Scenario:* Chef completa risotto → clicca "PRONTO". Sistema invia notifica a tablet camerieri: "Tavolo 5 - Risotto pronto". Dopo 20 minuti se non ritirato → sistema avvisa maître: "RITARDO - Risotto tavolo 5 in attesa".

### RF008 - Controllo Giacenze
*Scenario:* Arriva fornitura pomodori. Cuoco aggiorna magazzino: +50kg. Sistema ricalcola totale. A fine giornata, controlla soglie: burro sotto minimo (3kg vs 5kg) → invia alert a titolare. Nel frattempo, "Pizza margherita" mostra "NON DISP." sui tablet.

### RF010 - Gestione Turni
*Scenario:* Direttore pianifica turni settimana su calendario drag-drop. Sistema avvisa: "Mario supera 40 ore". Fine mese, titolare genera report: Mario 160 ore, 2 malattie, 1 permesso. Esporta Excel per paghe.
## Use Case Diagram o Diagrams
Chiedere se farne uno unico oppure farlo splittato
![[use_case_diagram.png | center | 400]]
## Documentazione 
Chiedere Prof

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
- **Servizio Notifiche:** Invia WhatsApp/email/SMS

### Client (Dispositivi)
- **Tablet Sala:** App React Native per camerieri
- **Monitor Cucina:** Interfaccia web semplice per chef
- **PC Reception:** Applicazione desktop per gestione
- **Mobile Manager:** App per titolare (iOS/Android)

## 3. Comunicazione
```
Tablet → WiFi/LTE → Server → Database
  ↓                    ↓
Cucina ← WebSocket ← Notifiche
```

## 4. Tecnologie Proposte
- **Backend:** Node.js o Python (API veloci)
- **Database:** PostgreSQL (affidabile, gratis)
- **Tablet App:** React Native (un codice per iOS/Android)
- **Monitor Cucina:** Web App semplice (HTML/JS)
- **Comunicazione:** REST API + WebSocket per notifiche

## 5. Modalità Operativa
- **Online principale:** Tutti i dispositivi connessi a internet
- **Offline limitato:** Tablet salvano ordini localmente se internet cade
- **Sincronizzazione automatica** quando connessione ritorna

## 6. Sicurezza Base
- Login con username/password per ogni ruolo
- Accessi separati: camerieri vedono solo loro funzioni, titolare vede tutto
- Backup automatico giornaliero

# System Architectural Models
## Activity Diagrams
### Prenotazioni
![[activity_diagram_prenotazione.png | center | 400]]
### + altri da aggiungere
Chiedere prof
## Sequence Diagrams
Chiedere Prof
## Class Diagram
### Class diagram unrefined
![[class_Diagram.png | center | 600]]
### Class diagram refined
Chiedere Prof

# Design Pattern
Chiedere Prof
# Evoluzione del sistema
## **Estensibilità verso Camerieri Robot e Droni di Consegna**
Il sistema è progettato con un'architettura API-first e modulare per permettere l'integrazione futura di camerieri robotici e droni per la consegna a domicilio. Le interfacce di gestione ordini e comande sono già strutturate per supportare dispositivi autonomi, con protocolli di comunicazione standardizzati che potranno essere estesi per includere comandi di navigazione, gestione tray robotizzati e coordinamento multi-agente. L'infrastruttura di gestione ordini a domicilio include già hook per l'integrazione con sistemi di delivery autonomo, prevedendo API specifiche per la pianificazione rotte drone, monitoraggio stato consegne in tempo reale e gestione autonoma degli slot di ricarica. L'astrazione dei layer di business logic dalla presentation layer consentirà di sostituire progressivamente le interfacce umane con controller per robot e flotte drone, mantenendo invariata la logica operativa mentre si evolve l'implementazione fisica del servizio.

# Appendice
Qualcosa

