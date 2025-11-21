Il **Requirement Engineering** varia in base al dominio applicativo, alle persone coinvolte ed all'organizzazione che sviluppa il sistema software.

Esistono però delle attività comuni a tutti i processi:

1. **Studio di fattibilità** (feasibility study) è l'unica fase opzionale.
2. **Identificazione e analisi dei requisiti** (req. elicitation and analysis).
3. **Specifica dei requisiti** (req. specification).
4. **Convalida dei requisiti** (req. validation).
5. **Gestione dei requisiti** (req. management).
# Studio di fattibilità

È una **descrizione sommaria** del sistema software e delle necessità utente. Le informazioni vengono raccolte attraverso **colloqui** con:

- Client manager.
- Ingegneri del software con esperienza nello specifico dominio applicativo.
- Esperti delle tecnologie da utilizzare.
- Utenti finali del sistema.
## Report di fattibilità

Prodotto dallo studio di fattibilità, il report stabilisce l'opportunità o meno di procedere allo sviluppo del sistema software.

Domande tipiche dello studio di fattibilità:

1. In che termini il sistema software contribuisce al raggiungimento degli **obiettivi strategici** del cliente?
2. Può il sistema software essere sviluppato usando le **tecnologie** correnti e rispettando i **vincoli** di durata e costo complessivo?
3. Può il sistema software essere **integrato** con altri sistemi già in uso?

# Identificazione e analisi dei requisiti

Il team di sviluppo incontra il cliente e gli utenti finali al fine di identificare i requisiti utente, dalla cui analisi si generano i requisiti di sistema (specifiche). Questo processo coinvolge tipicamente personale di vari ruoli sia all'interno dell'organizzazione del cliente che in altre organizzazioni o tra gli utenti finali.

**Stakeholders**: sono coloro che hanno un interesse diretto o indiretto sui requisiti del sistema software da sviluppare.

**Task**:

1. **Comprensione del dominio**: l'analista deve comprendere il dominio applicativo (es. se il sistema software deve supportare un ufficio postale, l'analista deve comprendere il funzionamento di un ufficio postale).
2. **Raccolta dei requisiti**: mediante interazione con gli stakeholder si identificano i requisiti utente.
3. **Classificazione**: l'insieme dei requisiti raccolti viene suddiviso in sotto-insiemi coerenti di requisititi.
4. **Risoluzione dei conflitti**: eventuali contraddizioni e/o conflitti tra requisiti vanno identificati e risolti.
5. **Assegnazione delle priorità**: mediante interazione con gli stakeholder, ad ogni requisito o sotto-insiemi di requisiti va assegnata una classe di priorità.
6. **Verifica dei requisiti**: i requisiti vengono controllati per verificarne completezza e consistenza, in accordo a quanto richiesto dagli stakeholder.

## Tecniche di identificazione dei requisiti

- **Etnografia**: Osservazione di quello che succede nel dominio applicativo.
- **Casi d'uso**: basati su scenari reali.
- **Prototipazione**.

## Tecniche di analisi (e specifica) dei requisiti:

Si dividono in:
- **Semi-formali**: basate su modelli del sistema e usate dai metodi di analisi strutturata o analisi orientata agli oggetti.
- **Formali**: basate su Petri Net, FSM, Z, ecc.
# Convalida dei requisiti

La convalida dei requisiti ha l'obiettivo di controllare che il documento dei requisiti, ottenuto dalla fase di analisi, descriva accuratamente il sistema software che il cliente si aspetta. Scoprire gli errori in questa fase è fondamentale per evitare modifiche costose in fasi successive.

Alcuni controlli da effettuare:

1. Validità:
2. Consistenza:
3. Completezza:
4. Realizzabilità:
5. Verificabilità:

Tecniche di convalida dei requisiti:

- **Revisioni informali**: basate sul peer-review. Esempio 1 tester per X sviluppatori.
- **Revisioni formali**:
	- **Walkthrough**: si percorre l'intero documento in maniera organizzata per individuare punti deboli, solitamente attraverso delle riunioni.
	- **Ispezioni**:
- **Prototipazione**.
- **Generazione dei test-case**.
- **Analisi di consistenza automatizzata**: per requisiti formali.

# Gestione dei requisiti.

Consiste nell'identificazione e **controllo delle modifiche** subite dai requisiti di un sistema software durante il ciclo di vita. I requisiti di un sistema software possono essere classificati in termini della loro evoluzione come:

- **Requisiti stabili**: Con probabilità minima di essere modificati nel tempo.
- **Requisiti volatili**: Con probabilità elevata di essere modificati nel tempo, essi si dividono in:
	- **Mutabili**: modifiche legate a cambiamenti nell'ambiente operativo.
	- **Emergenti**: modifiche causate da una migliore comprensione del sistema software.
	- **Consequenziali**: modifiche legate all'introduzione di sistemi informatici nel flusso di lavoro.
	- **di compatibilità**: modifiche legate a cambiamenti nei sistemi e nei processi aziendali.
## Gestione delle modifiche di requisiti

Le modifiche dei requisiti vanno opportunamente pianificate mediante:
- Identificazione univoca dei requisiti.
- Gestione delle modifiche
	- Analisi dei costi.
	- Analisi dell'impatto.
	- Analisi della realizzazione.
- Politiche di tracciabilità: relazioni tra requisiti e tra requisiti e progetto del sistema software.
- Uso di tool CASE per il supporto alle modifiche.
## Specifiche formali vs. informali

![[Pasted image 20250517193334.png]]
## Specifiche formali con Petri Net

Usate in ambito di ingegneria delle comunicazioni. 

![[Pasted image 20250517193356.png]]
