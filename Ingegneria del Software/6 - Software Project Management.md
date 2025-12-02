
Il **Software Project Management** consiste nella **pianificazione**, il **monitoraggio** ed il **controllo** di persone, processi ed eventi durante lo sviluppo del prodotto software.

Il **Software Project Management Plan** (**SPMP**) è il documento che guida la gestione di un progetto software.

Perché il **Software Project Management** è importante?

Percentuale di progetti on-time, ritardati o cancellati del tutto a causa di costi/ritardi eccessivi o scarsa qualità

![[Pasted image 20251126164250.png]]

Statistica elaborata su progetti USA dal 1984 al 2016.
# Le 4 P

La gestione efficace di un progetto software si fonda sulle **4 P**:
1. **Persone**: sono l'elemento più importante di un progetto software di successo (il SEI ha elaborato il P**eople Management - Capability Maturity Model**)
2. **Prodotto**: sono le caratteristiche del software che deve essere sviluppato (obiettivi, dati, funzioni, comportamenti principali, alternative, vincoli)
3. **Processo**: che definisce il quadro di riferimento entro cui si stabilisce il piano complessivo di sviluppo del prodotto software.
4. **Progetto**: che definisce l'insieme delle attività da svolgere, identificando persone, compiti, tempi e costi

# Organizzazione dei Team

Problema: sviluppare un prodotto software in 3 mesi con un impegno pianificato di 1 anno/uomo.

Soluzione immediata: 4 sviluppatori che si suddividono il lavoro.

Realtà: i 4 sviluppatori potrebbero impiegare un anno ottenendo un prodotto di qualità inferiore a quello risultante dal lavoro di un singolo sviluppatore.

Motivi:
- Alcuni compiti non possono essere condivisi.
- Necessità di frequenti interazioni.

L'aggiunta di uno sviluppatore potrebbe ritardare ulteriormente il progetto, a causa del periodo di formazione e dell'aumento delle interazioni (legge di Brooks, 1975).

## Approccio Democratico

Introdotto da Weinberg (1971) si basa sul concetto di **egoless programming**, secondo cui
ogni sviluppatore valuta la scoperta di fault nel proprio codice come un attacco alla propria
persona e non come un evento usuale.

Punta ad organizzare team che lavorino con un obiettivo comune, senza un singolo leader. Il codice appartiene al team come entità e non al singolo sviluppatore.

**Vantaggi**:
- Atteggiamento positivo verso la ricerca di fault.
- Molto produttivo in caso di problemi difficili da risolvere (es. ambienti di ricerca).

**Svantaggi**:
- L'approccio non può essere imposto dall'esterno ma deve nascere spontaneamente.
- Gli sviluppatori più anziani non desiderano essere valutati dai più giovani.

## Approccio con Capo-Programmatore

Basato su:
- **Specializzazione**: ogni partecipante svolge i compiti per i quali è stato formato.
- **Gerarchia**: ogni sviluppatore comunica esclusivamente con il capo-programmatore, che dirige le attività ed è responsabile dei risultati.

**Vantaggi**:
- Meno canali di comunicazione. 

**Svantaggi**:
- Richiede personale molto esperto per ricoprire gli incarichi di:
	- **Capo-programmatore**: sia un manager che un tecnico, sviluppa il progetto architetturale e le parti di codice critiche.
	- **Programmatore di back-up**: sostituisce il capo-programmatore ed è responsabile delle attività di testing.
	- **Segretario di programmazione**: responsabile della documentazione e dell'archivio di produzione.

## Evoluzione degli Approcci

Il capo-programmatore, essendo sia manager che tecnico, risulta essere il valutatore di se stesso.
Viene dunque sostituito con due figure:
- **Team Leader**: responsabile aspetti tecnici.
- **Team Manager**: responsabile aspetti gestionali

**Problema**: il team manager concede le ferie al programmatore senza contattare il team leader
che invece è di parere contrario.

**Soluzioni**:
- Identificare aree di responsabilità condivise.
- Introdurre un ulteriore livello di gestione, con un **project leader** che è responsabile dell'intero progetto e che comunica con i team leader.

Si ottiene dunque un organizzazione scalabile dei team per progetti SW di dimensione medio-grande. Eventualmente con **decision-making decentralizzato**.

![[Pasted image 20251126164146.png]]

# Pianificazione di Progetti Software

L' obiettivo è quello di definire un quadro di riferimento per controllare, determinare l'avanzamento ed osservare lo sviluppo di un progetto software. Per sviluppare i prodotti software nei tempi e costi stabiliti, con le desiderate caratteristiche di qualità.

Componenti fondamentali:
- **Scoping** (raggio d'azione): comprendere il problema ed il lavoro che deve essere svolto.
- **Stime**: prevedere tempi, costi e effort.
- **Rischi**: definire le modalità per l'analisi e la gestione dei rischi
- **Schedule**: allocare le risorse disponibili e stabilire i punti di controllo nell'arco temporale del progetto
- **Strategia di controllo**: stabilire un quadro di riferimento per il controllo di qualità e per il controllo dei cambiamenti.

## Stime nei Progetti Software

La di stima di tempi, costi ed effort nei progetti software servono a:
- Ridurre al minimo il grado di incertezza.
- Limitare i rischi comportati da una stima.

Le tecniche di stima possono basarsi su:
- **Expert judgement by analogy**: ovvero stime su progetti simili già completati
- **Tecniche di scomposizione**: basati sul divide et impera, consistono in:
	- Stime dimensionali, ad es. **Lines Of Code** (**LOC**) o **Function Point** (**FP**).
	- Suddivisione dei task e/o delle funzioni con relativa stima di allocazione dell'effort.
- **Modelli algoritmici empirici** si basano su dati storici e su relazioni del tipo: $d=f(v_i)$ dove d è il valore da stimare (es. effort, costo, durata) e i $v_i$ sono le variabili indipendenti (es. LOC o FP stimati)

**Esempio di stima di LOC**:
![[Pasted image 20251127215524.png]]

### Function Point – FP

Un **Punto Funzione (PF)** è una misura pesata della funzionalità del software proposta da Albrecht (1979-1983).

I punti funzione misurano la quantità di funzionalità in un sistema basandosi sulle specifiche del sistema (stima prima dell'implementazione).

**Il calcolo dei PF** avviene in due fasi:
1. Calcolo di un Conteggio Punti Funzione Non Aggiustato (UFC - Unadjusted Function point Count)
2. Moltiplicazione dell'UFC per un Fattore di Complessità Tecnica (TCF - Technical Complexity
Factor)

La formula finale per i Punti Funzione (aggiustati) è: **PF = UFC × TCF**

Il testo di riferimento a riguardo è il Function Point Counting Practice Manual prodotto dall'International Function Point User Group


#### FP Components
![[Pasted image 20251127220508.png]]

#### Categorie di dati

**Conteggi per le categorie di dati**:
- **Numero di File Logici Interni (ILF)**: Un gruppo di dati o informazioni di controllo che viene generato, utilizzato o mantenuto dal sistema software.
- **Numero di File di Interfaccia Esterni (EIF)**: Un gruppo di dati o informazioni di controllo scambiati o condivisi tra applicazioni, ad esempio interfacce leggibili dalla macchina verso altri sistemi e/o verso l'utente.
- Il termine "file" **non** va inteso nel senso tradizionale dell'elaborazione dati. Si riferisce a un gruppo di dati logicamente correlati, e non all'implementazione fisica di tali gruppi di dati.

#### Categorie di transazioni

**Conteggi per le categorie di transazioni**:
- **Numero di Input Esterni (EI)**: Elementi forniti dall'utente che descrivono dati distinti orientati all'applicazione, informazioni di controllo (come nomi di file e selezioni di menu), o output di altri sistemi che entrano in un'applicazione e **cambiano lo stato** dei suoi file logici interni.
- **Numero di Output Esterni (EO)**: Tutti i dati unici o le informazioni di controllo prodotti dal sistema software, ad esempio report e messaggi.
- **Numero di Interrogazioni Esterne (EQ)**: Tutte le combinazioni input/output uniche, in cui un input causa e genera un output immediato **senza cambiare lo stato** di alcun file logico interno.

#### Esempio: Spell Checker
![[Pasted image 20251127220826.png]]

##### UFC

Si assumono pesi di complessità medi per ogni elemento: UFC = 55.

![[Pasted image 20251127221110.png]]


#### Fattori di Grado di Influenza

1. **Back-up e recupero affidabili**
2. **Comunicazioni dati**
3. **Elaborazione dati distribuita**
4. **Prestazioni**
5. **Configurazione intensamente utilizzata**
6. **Inserimento dati online**
7. **Facilità operativa**
8. **Aggiornamento online**
9. **Interfaccia complessa**
10. **Elaborazione complessa**
11. **Riutilizzabilità**
12. **Facilità di installazione**
13. **Siti multipli**
14. **Facilità di modifica**

Ogni componente viene valutato da 0 a 5, dove:

**0** - Assente, o nessuna influenza
**1** - Influenza incidentale
**2** - Influenza moderata
**3** - Influenza media
**4** - Influenza significativa
**5** - Influenza forte in tutto il sistema

Il TCF può quindi essere calcolato come:
$$TCF=0.65+0.01$$
• Il TCF varia da **0,65** (se tutti i $F_j$ sono impostati a 0) a **1,35** (se tutti i $F_j$ sono impostati a 5) , è una **regolazione del ±35%**

#### Esempio: TCP & FP

Assumiamo che:

![[Pasted image 20251128164003.png]]allora:
$$TCF = 0.65 + 0.01(18+10) = 0.93$$
e:
$$FP = 55 \times 0.93 ≈ 51$$

#### FP vs LOC

Diversi studi hanno tentato di mettere in relazione le metriche LOC e FP. Derivando il numero  medio d'istruzioni per punto funzione di numerosi linguaggi di programmazione.

Da ciò è stato poi costruito una classifica in base alla relazione tra LOC e FP.

![[Pasted image 20251128165140.png]]

### Modello Algoritmico

#### COCOMO

Il COCOMO (COnstructive COst MOdel) è il modello introdotto da Boehm (1981) per determinare il valore dell'effort, che viene successivamente utilizzato per determinare durata e costi di sviluppo.

Comprende 3 modelli:
1. **Basic** (per stime iniziali)
2. **Intermediate** (usato dopo aver suddiviso il sistema in sottosistemi)
3. **Advanced** (usato dopo aver suddiviso in moduli ciascun sottosistema)

La stima parte da:
1. Stima delle dimensioni del progetto in KLOC.
2. Stima del modo di sviluppo del prodotto, che misura il livello intrinseco di difficoltà nello sviluppo, tra:
	- **Organic** (per prodotti di piccole dimensioni)
	- **Semidetached** (per prodotti di dimensioni intermedie)
	- **Embedded** (per prodotti complessi)

Nel 1995 è stato introdotto COCOMO II, più flessibile e sofisticato rispetto alla versione precedente.

##### Esempio d'uso di COCOMO

Modello **Intermediate**, modo **Organic**:
1. Determinare l'effort nominale usando la formula: 
$$effort\ nominale= 3.2 × (KLOC)^{1.05} MM$$
Esempio: $3.2 × (33)^{1.05} = 126 MM$

2. Ottenere la stima dell'effort applicando un fattore moltiplicativo C basato su 15 cost drivers:
$$effort = effort\ nominale × C$$
Esempio: $126 × 1.15 = 145 MM$

C (cost driver multiplier) è una produttoria dei cost driver $c_i$. Ogni $c_i$ determina la complessità del fattore $i$ che influenza il progetto e può assumere uno tra più valori assegnati con variazioni intorno al valore unitario (valore nominale).

#### Tabella dei Cost Driver - Intermediate COCOMO

![[Pasted image 20251128170840.png]]
##### Cost Drivers Ratings
![[Pasted image 20251128170926.png]]

##### Complexity Ratings - CPLX

![[Pasted image 20251128171009.png]]
##### Esempio di Cost Drivers Ratings

Software di elaborazione delle comunicazioni basato su microprocessore

![[Pasted image 20251128171126.png]]
#### Time Schedule

È la stima del tempo T alla consegna (product delivery):
1. Modo Organic $T = 2.5 E^{0.38} (months\ M)$
2. Modo semi-detached $T = 2.5\ E^{0.38}\ (months\ M)$
3. Modo embedded $T = 2.5\ E^{0.32}$
#### Stima dei Costi di Sviluppo
I **Costi di sviluppo (C)** vengono stimati allocando lo sforzo di sviluppo (E) per fasi e attività del personale, ad esempio:

- **16%** Progettazione preliminare
  • 50% Project Manager
  • 50% Analista

- **62%** Progettazione dettagliata, codifica e testing
  • 75% Programmatore/Analista
  • 25% Programmatore

- **22%** Integrazione
  • 30% Analista
  • 70% Programmatore/Analista

• Il **costo per persona-mese** di ogni categoria del personale (es. project manager, analista, programmatore, ecc.) viene poi utilizzato per ottenere i costi di sviluppo totali.

## Pianificazione temporale

Dopo aver scelto il modello di processo, identificato i task da eseguire e stimato durata, costi ed effort, è necessario effettuare la pianificazione temporale ed il controllo dei progetti. La pianificazione temporale consiste nel definire una "rete di task" in base ai seguenti principi fondamentali:

1. **Ripartizione**: scomposizione di processo e prodotto in parti (task e funzioni) di dimensioni ragionevoli
2. **Interdipendenza**: identificazione delle dipendenze reciproche tra i task individuati
3. **Allocazione di risorse**: determinazione di numero di persone, effort e date di inizio/fine da assegnare ad ogni task
4. **Responsabilità definite**: individuazione delle responsabilità assegnate a ciascun task
5. **Risultati previsti**: definizione dei risultati prodotti al termine di ogni task
6. **Punti di controllo (milestone)**: identificazione dei punti di controllo della qualità da associare al singolo task o a gruppi di task

### Strumenti di Pianificazione

**Diagramma PERT** (**Program Evaluation and Review Technique**): grafo in cui ogni nodo rappresenta un task ed ogni arco un legame di precedenza. Consente di determinare:

1. Il cammino critico (sequenza di task che determina la durata minima di un progetto)
2. La stima del tempo di completamento di ciascun task, mediante applicazione di modelli statistici.
3. I limiti temporali di inizio e termine di ciascun task.

**Carta di Gantt**:  diagramma a barre che consente di visualizzare l'allocazione temporale dei task, non appare nessuna indicazione dei legami di precedenza, quindi viene integrato con un diagramma PERT.

![[Pasted image 20251128184244.png]]
# Software Project Management Plan (SPMP)

## Contenuti del SPMP

Da: Manager's Handbook for Software Development (NASA-SEL-84-101, 1990) pag 1/2

![[Pasted image 20251128184359.png]]![[Pasted image 20251128184418.png]]

UniRoma2 - ISW/SSW 43 IEEE Standard for Software Project Management Plans (IEEE Std. 1058-1998) pag. 1/3

![[Pasted image 20251128184813.png]]![[Pasted image 20251128184827.png]]
![[Pasted image 20251128184843.png]]