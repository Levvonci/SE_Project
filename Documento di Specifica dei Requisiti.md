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

### 1.1 Gestione Sala
**RF001 - Prenotazione Tavoli**
- L'utente deve poter prenotare un tavolo specificando: data, ora, numero persone, note speciali
- Deve visualizzare la disponibilità in tempo reale
- Deve poter modificare/cancellare prenotazioni

**RF002 - Presa Comanda**
- Il cameriere deve poter creare una nuova comanda per un tavolo
- Selezione multipla di piatti e bevande in una singola operazione
- Deve poter applicare modifiche ai piatti (es. "senza glutine")
- Possibilità di specificare quantità per ogni voce ordinata
- Sistema deve calcolare automaticamente il totale parziale

**RF003 - Modifica Comanda**
- Aggiunta di nuovi items a comanda esistente
- Rimozione/cancellazione di voci già inserite
- Modifica quantità di voci già ordinare    
- Tracciamento storico delle modifiche

**RF004 - Gestione Ordini Cucina**
- Invio automatico comanda alla cucina con timestamp
- Suddivisione automatica ordini per categoria (antipasti, primi, secondi, etc.)
- Possibilità di priorità/urgenza su specifiche voci

**RF005 - Gestione Conti**
- Deve essere possibile dividere il conto per persone
- Applicazione automatica del coperto
- Stampa/sinvio email dello scontrino

### 1.2 Gestione Cucina
**RF006 - Visualizzazione Comande**
- Display comande in arrivo con dettagli completi
- Organizzazione per tipo di piatto e ordine cronologico
- Evidenziazione modifiche speciali (allergie, preferenze)

### 1.3 Gestione Magazzino
**RF007 - Controllo Giacenze**
- Avviso automatico quando le scorte sono basse.
- Tracciamento dei consumi per ogni voce del menù.

## 2. REQUISITI NON FUNZIONALI

### 2.1 Prestazioni
**RNF001 - Tempi di Risposta**
- Risposta < 2 secondi per operazioni comuni (ordini, prenotazioni)
- Sistema disponibile 24/7 con uptime > 99.5%

**RNF002 - Concurrent Users**
- Supporto fino a 50 utenti contemporanei
- 10 dispositivi in sala + 5 in cucina + amministrazione

### 2.2 Usabilità
**RNF003 - Interfaccia Intuitiva**
- Formazione base < 30 minuti per nuovo personale
- Interfaccia touch-friendly per tablet sala

### 2.3 Affidabilità
**RNF004 - Backup Automatico**
- Backup giornaliero automatico dei dati
- Ripristino sistema < 1 ora in caso di guasto

## 3. SCENARI D'USO PRINCIPALI

### Scenario 1: Prenotazione Telefonica
**Attore:** Addetto reception
**Pre-condizione:** Cliente chiama per prenotare
**Flusso principale:**
1. Sistema mostra disponibilità tavoli
2. Inserimento dati prenotazione
3. Conferma e invio SMS di riepilogo
**Post-condizione:** Prenotazione registrata nel calendario

### Scenario 2: Ordinazione al Tavolo
**Attore:** Cameriere
**Pre-condizione:** Cliente seduto al tavolo
**Flusso principale:**
1. Scan codice tavolo
2. Selezione piatti dal menu
3. Invio ordine alla cucina
4. Conferma avvenuta stampa
**Post-condizione:** Ordine in lavorazione in cucina

## 4. VINCOLI PROGETTUALI

### 4.1 Tecnologici
- Compatibilità con dispositivi mobile (tablet)
- Integrazione con registratore di cassa telematico
- Supporto stampanti di cucina, pasticceria e bar esistenti

### 4.2 Operativi
- Multilingua (Italiano, Inglese)
- Conformità normativa privacy GDPR
- Adesione standard fiscali italiani

## 5. CRITERI DI ACCETTAZIONE

### Per RF001 - Prenotazione Tavoli
- [ ] Il sistema impedisce doppie prenotazioni stesso tavolo/ora
- [ ] Invio SMS conferma automatico
- [ ] Alert per prenotazioni che non si presentano

### Per RF002 - Gestione Ordini
- [ ] Tempo medio inserimento ordine < 1 minuto
- [ ] Errori di inserimento < 2%
- [ ] Sync immediato con cucina

**Stakeholder Coinvolti:**
- Proprietario/General Manager
- Maître/Sala
- Executive Chef
- Cassiere
- Addetto alle Prenotazioni

**Priorità:**
- Alta: Gestione ordini, conti, prenotazioni
- Media: Reportistica, gestione magazzino
- Bassa: Funzioni avanzate di marketing

## Class Diagram
![[class_Diagram.png | center | 600]]

## Use Case Diagram
![[use_case_diagram.png | center | 400]]

## Activity Diagram Prenotazioni
![[activity_diagram_prenotazione.png | center | 400]]