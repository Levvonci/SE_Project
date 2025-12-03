# Misure del Design Preliminare
**Misure intermodulari**, che tengono conto delle dipendenze tra i moduli, secondo l'architettura di sistema sviluppata nella fase di progettazione.

- Le misure degli attributi dei singoli moduli sono chiamate **misure intramodulari** (utilizzate durante la progettazione dettagliata e l'implementazione).
* Un **modulo** è una sequenza contigua di istruzioni di programma, delimitata da elementi di confine, dotata di un identificatore aggregato (Yourdon e Constantine, 1979).
* Durante la fase di progettazione preliminare, le decisioni riguardanti l'architettura del sistema hanno un impatto significativo su molte qualità importanti del software risultante, come la facilità di implementazione, l'affidabilità e la manutenibilità.
* Le **misure di progettazione preliminare** hanno il potenziale per fornire il feedback necessario sulle caratteristiche del sistema in fase di sviluppo.
# Relazioni tra Pre-Design e Codice

La relazione tra la progettazione preliminare e il codice (implementato a partire dalla progettazione) include relazioni uno-a-uno tra:

- i moduli indicati nella progettazione e i moduli nel codice
- le connessioni intermodulari indicate nella progettazione e i riferimenti intermodulari nel codice
- le interfacce dati intermodulari indicate nella progettazione e i dati condivisi intermodulari nel codice
# Architettura a Moduli

L'architettura a moduli di un sistema software può essere rappresentata da un grafo, S = {N, R}

• Ogni nodo **n** nell'insieme dei nodi (**N**) corrisponde a un modulo.
• Ogni arco **r** nell'insieme delle relazioni (**R**) indica una relazione (ad esempio, chiamata di procedura, flusso di dati, ecc.) tra due sottosistemi.

![[Pasted image 20251202163203.png]]
## Modularità
Def. (IEEE Standard Glossary of Software Engineering Technology):

la misura in cui il software è composto da componenti discreti, tali che una modifica a un componente abbia un impatto minimo sugli altri componenti.

Un'elevata modularità è desiderabile perché si ritiene che i programmi con bassa modularità siano più soggetti a errori, meno mantenibili, meno riusabili, ecc.
### Attributi della Modularità

La modularità è un attributo di qualità che può essere misurato in termini dei seguenti sotto-attributi:

1. **Coesione**: La misura in cui un singolo modulo esegue un compito singolo e ben definito.
2. **Accoppiamento**: Il grado di interdipendenza tra i moduli.
3. **Morfologia**: La forma della struttura complessiva del sistema.
4. **Flusso di Informazioni**: Le interconnessioni che un modulo ha con altri moduli in un sistema, cioè il *fan-in* e il *fan-out* del modulo.
### Morfologia

La **morfologia** si riferisce alla forma complessiva dell'architettura del sistema software.

* È caratterizzata da:
  * **Dimensione**: numero di nodi e archi
  * **Profondità**: percorso più lungo dal nodo radice a un nodo foglia
  * **Ampiezza**: numero massimo di nodi a qualsiasi livello
  * **Rapporto archi-nodi**: misura della densità di connettività

#### Esempio

**Dimensione:**
*   Nodi: 12
*   Archi: 15

**Profondità:** 4
**Ampiezza:** 6
**Rapporto e/n:** 1.25

![[Pasted image 20251202164224.png]]

# Impurezza dell'Albero

L'**impurezza dell'albero** m(G) misura quanto il grafo G differisce da un albero (ipotesi: un buon design dovrebbe essere il più possibile "simile a un albero").

* Più piccolo è il valore di m(G), migliore è considerato il design.

L'impurezza dell'albero può essere definita come:

$$ m(G) = \frac{e - (n - 1)}{2n - 5} $$

Dove:
*   `e` = numero di archi nel grafo
*   `n` = numero di nodi nel grafo
*   `(n - 1)` = numero di archi in un albero di copertura (il numero minimo di archi per connettere tutti i nodi)
*   `2n - 5` = il numero massimo di archi in eccesso rispetto a un albero che il grafo può avere (per `n ≥ 4`)

Il numeratore `(e - (n - 1))` conta quanti archi in più ci sono rispetto a una struttura ad albero minima. Il denominatore `(2n - 5)` normalizza questo valore nel range `[0, 1]`.

**Esempio**

Per un dato grafo G:
*   $m(G_1) = 0$
*   $m(G_2) = 0.1$ 
*   $m(G_3) = 0.2$
*   $m(G_4) = 1$
*   $m(G_5) = 1$
*   $m(G_6) = 1$
# Riutilizzo Interno
Il **riutilizzo interno** è una misura, proposta da Yin e Winchester, che indica l'entità del riutilizzo di moduli all'interno dello stesso prodotto (diverso dal riutilizzo esterno).

$$ r(G) = e - n + 1 $$

Dove:
*   `e` = numero di archi nel grafo
*   `n` = numero di nodi nel grafo

*   Un valore **più piccolo** di `r(G)` indica un minore riutilizzo (una struttura più simile a un semplice albero).
*   **Critiche**: questa misura non è in grado di tenere conto delle **chiamate ripetute** (più archi tra gli stessi due nodi) e non considera la **dimensione del modulo riutilizzato**.

**Esempio:**
*   $r(G_1) = 0$
*   $r(G_2) = 1$
*   $r(G_3) = 2$
*   $r(G_4) = 1$
*   $r(G_5) = 3$
*   $r(G_6) = 6$

![[Pasted image 20251202164619.png]]
# Flusso di Informazioni
Le **misure del flusso di informazioni** presuppongono che la complessità di un modulo dipenda da 2 fattori:
- la complessità del codice del modulo
- la complessità delle interfacce del modulo, cioè le sue connessioni con l'ambiente circostante

* Il **livello totale di flusso di informazioni** attraverso un sistema, in cui i moduli sono visti come componenti atomiche, è un attributo **inter-modulare**.

* Il **livello totale di flusso di informazioni** tra un singolo modulo e il resto del sistema è un attributo **intra-modulare**.
## Misure del Flusso di Informazioni

Le **misure del flusso di informazioni** sono conteggi basati sulle interconnessioni che un modulo ha con altri moduli in un sistema, cioè il *fan-in* e il *fan-out* di un modulo.

* Le misure del flusso di informazioni si basano su:
  * **Flusso di informazioni locale:**
    * *Diretto*: un modulo chiama un altro modulo
    * *Indiretto*: flusso derivante dai valori di ritorno
  * **Flusso di informazioni globale**: informazioni che vengono passate tra moduli tramite una struttura dati globale

* Le misure del flusso di informazioni:
  * Possono essere utilizzate per identificare le parti critiche di un sistema software
  * Si pensa che identifichino i punti di stress nel sistema
  * Forniscono una visione dei potenziali problemi di progettazione
# Fan-in e Fan-out

*   Il **Fan-in** di un modulo M è il numero di flussi locali (diretto + indiretto) che terminano in M, più il numero di flussi globali (strutture dati) da cui M recupera informazioni.

*   Il **Fan-out** di un modulo M è il numero di flussi locali (diretto + indiretto) che iniziano in M, più il numero di flussi globali (strutture dati) aggiornati da M.

![[Pasted image 20251202170601.png]]
## Valori di Fan-in e Fan-out

*   Un **fan-out elevato** in un modulo indica che esso influenza/controlla molti altri moduli.
*   Un **fan-in elevato** in un modulo indica che esso è influenzato/controllato da molti altri moduli.
*   Un modulo con **fan-in e fan-out elevati** si trova normalmente al cuore del sistema.
*   Un modulo con **fan-in e fan-out bassi** si trova normalmente alla periferia del sistema.

Un **fan-in e fan-out elevati** indicano un modulo spesso complesso che può essere incline agli errori perché:

*   **I moduli svolgono più di una funzione**. Se la struttura del design deve essere modificata, l'aspetto da cambiare non si troverà in un unico luogo ma in più punti, e tutto ciò che lo riguarda non è all'interno di un modulo specifico ma distribuito tra diversi moduli interconnessi (e quindi con fan-in e fan-out elevati). Di conseguenza, sarà necessario modificare molti moduli.
*   **I moduli sono raffinati in modo inadeguato**, cioè la struttura del sistema potrebbe mancare di un livello di astrazione (se la struttura è troppo ampia e poco profonda, o viceversa, si può dire che i moduli non siano stati sufficientemente raffinati).
# Misura del Flusso di Informazioni
Il **flusso di informazioni (IF)** per il modulo Mᵢ [Henry-Kafura, 1981] è:
$$ IF(M_i) = [ fan\text{-}in(M_i) \times fan\text{-}out(M_i) ]^2 $$

* L'IF per un sistema con n moduli è la somma dei flussi dei singoli moduli.

* La misura IF originale di Henry-Kafura include sia i **flussi di controllo** che i **flussi di informazioni** nel conteggio del fan-in e del fan-out.

* La variante di Shepperd include **solo i flussi di informazioni**.
## Esempio

![[Pasted image 20251202170851.png]]

# Misurazione Strutturale

(a livello di design dettagliato e implementazione)

La struttura può avere 3 componenti:
  * **Struttura del flusso di controllo**: sequenza di esecuzione delle istruzioni del programma.
  * **Flusso dei dati**: tracciamento dei dati mentre vengono creati o elaborati dal programma.
  * **Struttura dei dati**: organizzazione dei dati in sé, indipendentemente dal programma.

La misurazione strutturale è utilizzata in strumenti software per:
  * **Reverse engineering**
  * **Testing** (copertura dei percorsi)
  * **Ristrutturazione del codice**
  * **Analisi del flusso dei dati**

## Obiettivi & Domande

Come rappresentare la "struttura" di un programma?
*   Mediante un **grafo del flusso di controllo** (o semplicemente *flowgraph*).

Come definire la "complessità" in termini della struttura?
*   Tramite la **complessità ciclomatica**.

# Strutture di Controllo di Base

Le **Strutture di Controllo di Base (BCS)** sono un insieme di meccanismi essenziali del flusso di controllo utilizzati per costruire la struttura logica del programma.

Tipi di BCS:
    *   **Sequenza**: ad esempio, una lista di istruzioni senza altre BCS coinvolte.
    *   **Selezione**: ad esempio, `if … then … else`.
    *   **Iterazione**: ad esempio, `do … while`; `repeat ... until`.

Esistono altri tipi di strutture di controllo, o **Strutture di Controllo Avanzate (ACS)**:
    *   Chiamata di procedura/funzione/agente
    *   **Ricorsione** (auto-chiamata)
    *   **Interruzione**
    *   **Concorrenza**

## Flowgraph

La struttura del flusso di controllo è solitamente modellata da un **grafo del flusso (flowgraph)** FG, cioè un grafo orientato (di-grafo):
$$ FG = \{N, E\} $$

Ogni nodo **n** nell'insieme dei nodi (**N**) corrisponde a un'istruzione del programma.

Ogni arco orientato **e** nell'insieme degli archi (**E**) indica il flusso di controllo da un'istruzione del programma a un'altra.

*   **Nodi di procedura**: nodi con *out-degree* = 1 (hanno un solo arco uscente).
*   **Nodi predicato**: nodi con *out-degree* diverso da 1 (hanno zero o più di un arco uscente).
*   **Nodo di inizio**: nodi con *in-degree* = 0 (nessun arco entrante).
*   **Nodi terminali (fine)**: nodi con *out-degree* = 0 (nessun arco uscente).

Dove:
*   **Out-degree** è il numero di archi che escono da un nodo.
*   **In-degree** è il numero di archi che entrano in un nodo.
### Esempio

![[Pasted image 20251202172236.png]]

## Costrutti del Flowgraph
![[Pasted image 20251202172337.png]]
## Modelli di Programma Comuni nel Flowgraph

![[Pasted image 20251202172426.png]]
## Sequenziamento

Siano F1 e F2 due flowgraph. Allora, il **sequenziamento** di F1 e F2 (indicato con F1; F2) è un flowgraph formato fondendo il nodo terminale di F1 con il nodo di inizio di F2.

![[Pasted image 20251202173153.png]]
## Annidamento

Siano F1 e F2 due flowgraph. Allora, l'**annidamento** di F2 in F1 nel nodo x, indicato con F1(F2), è un flowgraph formato a partire da F1 sostituendo l'arco uscente da x con l'intero flowgraph F2.

![[Pasted image 20251202173313.png]]
## Flowgraph Primi

I **flowgraph primi** sono flowgraph che non possono essere decomposti in modo non banale mediante sequenziamento e annidamento.

*   Primi comuni:
    *   **P₁** (struttura base, spesso una singola istruzione o un blocco indivisibile)
    *   **D₀** (corrisponde tipicamente a una sequenza)
    *   **D₁** (corrisponde tipicamente a una selezione `if-then-else`)
    *   **D₂** (corrisponde tipicamente a un ciclo `while-do` o `repeat-until`)
    *   **D₃** (corrisponde tipicamente a una selezione a scelta multipla come `case`/`switch`)

**Strutture-D**
(tipiche della programmazione strutturata; la "D" è l'iniziale di **Edsger Dijkstra**, che fu un pioniere della programmazione strutturata).

### Scomposizione in Primi

**Teorema di Scomposizione in Primi (Fenton-Whitty)**: Ogni flowgraph ha una **scomposizione unica** in una gerarchia di flowgraph primi, chiamata **"albero di scomposizione"**.

![[Pasted image 20251202173500.png]]
### Decomposizione – Passo 1
![[Pasted image 20251202173606.png]]

### Decomposizione – Passo 2a

![[Pasted image 20251202173658.png]]

### Decomposizione – Passo 2b

![[Pasted image 20251202173727.png]]

### Decomposizione – Passo 3

![[Pasted image 20251202173818.png]]
# Misurazione Gerarchica

La **misurazione gerarchica** è un metodo per definire misure di un flowgraph utilizzando il suo albero di scomposizione.

Si basa sull'idea che possiamo misurare un attributo di un flowgraph attraverso i seguenti passi:
    1.  Definire la misura per i **flowgraph primi** (i mattoni atomici).
    2.  Descrivere come l'operazione di **sequenziamento** influisca sull'attributo.
    3.  Descrivere come l'operazione di **annidamento** influisca sull'attributo.

Esempi di misure di flowgraph che possono fornire informazioni sulla complessità della struttura del codice sono:
    *   **Profondità di annidamento (Depth of nesting)**
    *   **D-strutturatezza (D-structuredness)**

## Depth of nesting

La **profondità di annidamento** n(F) per un flowgraph F può essere misurata in base alle seguenti regole:

*   **Per i flowgraph primi:**
    *   n(P₁) = 0
    *   n(P₂) = n(P₃) = … = n(Pₖ) = 1
    *   n(D₀) = n(D₁) = n(D₂) = n(D₃) = 1
*   **Per l'operazione di sequenziamento:**
    *   n(F₁; F₂; …; Fₖ) = max{ n(F₁), n(F₂), …, n(Fₖ) }
*   **Per l'operazione di annidamento:**
    *   n(F(F₁, F₂, …, Fₖ)) = 1 + max{ n(F₁), n(F₂), …, n(Fₖ) }

### Esempio

![[Pasted image 20251202174015.png]]
## D-structuredness

Le definizioni più diffuse di **programmazione strutturata** affermano che un programma è strutturato se può essere composto utilizzando solo un piccolo numero di costrutti consentiti (ad esempio, sequenza, selezione e iterazione).

*   Considerando il **flowgraph** di un programma, possiamo decidere se esso è strutturato o meno.
*   A questo scopo può essere utilizzata la misura della **D-strutturatezza**.
*   La definizione informale di programmazione strutturata può essere espressa formalmente affermando che un programma è strutturato **se e solo se** è **D-strutturato**.

### Esempio

![[Pasted image 20251202174239.png]]
# Complessità Cyclomatica

La complessità di un programma può essere misurata dal **numero ciclomatico** del suo flowgraph.

* Il numero ciclomatico può essere calcolato in 2 modi diversi:
  1.  **Basato sul flowgraph**
  2.  **Basato sul codice**

Per un programma con flowgraph F, la **complessità ciclomatica** v(F) è misurata come:

**Formula 1 (Basata su archi e nodi):**
$$ v(F) = e - n + 2 $$
dove:
*   `e` è il numero di **archi** (che rappresentano rami e cicli), e
*   `n` è il numero di **nodi** (che rappresentano blocchi di codice sequenziale).

**Formula 2 (Basata sui nodi predicato):**
$$ v(F) = 1 + d $$
dove `d` è il numero di **nodi predicato** (cioè nodi con *out-degree* maggiore di 1), che rappresenta il numero di punti decisionali nel programma.

* Il numero ciclomatico misura in effetti il numero di **percorsi linearmente indipendenti** attraverso F (un insieme di percorsi è linearmente indipendente se nessun percorso nell'insieme è una combinazione lineare di altri percorsi).

* La complessità dei flowgraph primi dipende solo dai predicati in essi contenuti.
* v(F) può essere definita anche come una **misura gerarchica**.

## Domande

**1. Qual è la complessità dei flowgraph primi?**
La complessità dei primi è il numero di predicati più uno.
$$ v(F) = 1 + d $$

**2. Qual è la complessità del sequenziamento?**
La complessità di una sequenza è uguale alla somma delle complessità dei componenti meno il numero dei componenti più uno.
$$ v(F_1; F_2; \ldots; F_n) = \sum_{i=1}^{n} v(F_i) - n + 1 $$

**3. Qual è la complessità dell'annidamento in un dato flowgraph primo F?**
La complessità dell'annidamento di componenti in un flowgraph primo F è uguale alla complessità di F più la somma delle complessità dei componenti meno il numero dei componenti.
$$ v(F(F_1, F_2, \ldots, F_n)) = v(F) + \sum_{i=1}^{n} v(F_i) - n $$
## Esempi
### Basato su Flowgraph

Per il flowgraph fornito:

**Calcolo con la prima formula (e - n + 2):**
*   Numero di archi (e) = 7
*   Numero di nodi (n) = 6
*   v(F) = 7 - 6 + 2
*   **v(F) = 3**

**Calcolo con la seconda formula (1 + d):**
*   Numero di nodi predicato (d) = 2
*   v(F) = 1 + 2
*   **v(F) = 3**

Entrambi i metodi confermano che la **complessità ciclomatica** del flowgraph è **3**.

![[Pasted image 20251202174628.png]]

### Basato su Codice

**v(F) = 1 + d = 1 + 2 = 3**

![[Pasted image 20251202174714.png]]

# Complessità Essenziale di McCabe

La **complessità essenziale** di un programma con flowgraph F è data da:

$$ ev(F) = v(F) - m $$

dove:
*   **v(F)** è la complessità ciclomatica di F.
*   **m** è il numero di **sotto-flowgraph D₀, D₁, D₂ e D₃** (strutture D) in F.

*   **Esempio:**
    *   v(F) = 5
    *   m = 1
    *   ev(F) = 5 – 1 = 4

*   La complessità essenziale indica **fino a che punto il flowgraph può essere ridotto** decomponendo tutti i suoi sotto-flowgraph strutturati D (D₀, D₁, D₂, D₃).
*   Per un programma **D-strutturato** (cioè composto solo da sequenze e strutture D), ev(F) = 1. Un valore più alto indica la presenza di logica di controllo più complessa e meno strutturata.

![[Pasted image 20251202175415.png]]

## Complessità Ciclomatica: Critiche

**Vantaggi:**
    *   Misurazione **oggettiva** della complessità strutturale.

**Svantaggi/Limitazioni:**
    *   Può essere utilizzata **solo a livello di componente** (modulo/funzione), non per sistemi interi.
    *   Due programmi con lo **stesso numero di complessità ciclomatica** possono richiedere uno **sforzo di programmazione diverso** (non cattura la complessità semantica o algoritmica).
    *   Richiede la **piena visibilità** del design o del codice per costruire il flowgraph.