
# Process iteration

Requirements **always** evolve in the course of a project, so process iteration where earlier stages
are reworked is always part of the process for large products.

It can be applied to any of the generic process models and there are two related approaches:

- Incremental development.
- Spiral development.
# Incremental development

![[Pasted image 20250516114352.png]]

- The product is developed and delivered in increments after establishing an overall architecture.
- Requirements and specifications for each increment may be developed.
- Users may experiment with delivered increments while others are being developed. Therefore, these serve as a form of prototype.
- Intended to combine some of the advantages of prototyping but with a more manageable process and better structure.

- Il prodotto software viene sviluppato e rilasciato per incrementi (build) successivi.
- Include aspetti tipici del modello basato su rapid prototyping (l’utente può sperimentare l’utilizzo del prodotto contenente gli incrementi consegnati, mentre i restanti sono ancora in fase di sviluppo).
- Si rivela efficace quando il cliente vuole continuamente verificare i progressi nello sviluppo del prodotto e quando i requisiti subiscono modifiche.
- Può essere realizzato in due versioni:
	- Versione con overall architecture.
	- Versione senza overall architecture (più rischiosa).

## Versione con overall architecture

![[Pasted image 20250516114741.png]]

## Versione senza overall architecture

![[Pasted image 20250516114812.png]]

## Impatto sui costi del software

![[Pasted image 20250516114838.png]]

## Confronto con modello a cascata
### Modello a cascata 

- Requisiti “congelati” al termine della fase di specifica.
- Feedback del cliente solo una volta terminato lo sviluppo.
- Fasi condotte in rigida sequenza (l’output di una costituisce input per la successiva).
- Prevede fasi di progetto dettagliato e codifica dell’intero prodotto.
- Team di sviluppo costituito da un numero elevato di persone.
### Modello incrementale

- Requisiti suddivisi in classi di priorità e facilmente modificabili.
- Continuo feedback da parte del cliente durante lo sviluppo.
- Fasi che possono essere condotte in parallelo.
- Progetto dettagliato e codifica vengono effettuate sul singolo build.
- Differenti team di sviluppo, ciascuno di piccole dimensioni.
# Modello a spirale

![[Pasted image 20250516115706.png]]

## Modello a spirale semplificato (versione lineare)

![[Pasted image 20250516115741.png]]

## Modello a spirale semplificato

![[Pasted image 20250516115816.png]]

## Modello full-spiral [Boehm, 1988]

![[Pasted image 20250516115838.png]]

# Risk management

Risk management is concerned with identifying risks and drawing up plans to minimize their effect on a project.

A **risk** is a probability that some adverse circumstance will occur. There's 3 main categories of risk:
- **Project risks** affect schedule or resources.
- **Product risks** affect the quality or performance of the software being developed.
- **Business risks** affect the organization developing or procuring the software.
## Risks by category

| Risk                    | Risk Type         | Description                                                                 |
|-------------------------|-------------------|-----------------------------------------------------------------------------|
| Staff turnover          | Project            | Experienced staff will leave the project before it is finished.            |
| Management change       | Project            | There will be a change of organisational management with different priorities. |
| Hardware unavailability | Project            | Hardware which is essential for the project will not be delivered on schedule. |
| Requirements change     | Project and product| There will be a larger number of changes to the requirements than anticipated. |
| Specification delays    | Project and product| Specifications of essential interfaces are not available on schedule.      |
| Size underestimate      | Project and product| The size of the system has been underestimated.                            |
| CASE tool under-performance | Product        | CASE tools which support the project do not perform as anticipated.        |
| Technology change       | Business           | The underlying technology on which the system is built is superseded by new technology. |
| Product competition     | Business           | A competitive product is marketed before the system is completed.          |
## The risk management process

- **Identification**: Identify project, product and business risks.
- **Analysis**: Assess the likelihood and consequences of these risks.
- **Planning**: Draw up plans to avoid or minimize the effects of the risk.
- **Monitoring**: Monitor the risks throughout the project.

![[Pasted image 20250516160316.png]]

## Risk identification

| Risk Type          | Possible Risks                                                                                                                                                                          |
| ------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Technology**     | The database used in the system cannot process as many transactions per second as expected. Software components which should be reused contain defects which limit their functionality. |
| **People**         | It is impossible to recruit staff with the skills required. <br> Key staff are ill and unavailable at critical times. <br> Required training for staff is not available.                |
| **Organisational** | The organisation is restructured so that different management are responsible for the project. Organisational financial problems force reductions in the project budget.                |
| **Tools**          | The code generated by CASE tools is inefficient. <br> CASE tools cannot be integrated.                                                                                                  |
| **Requirements**   | Changes to requirements which require major design rework are proposed. <br> Customers fail to understand the impact of requirements changes.                                           |
| **Estimation**     | The time required to develop the software is underestimated. <br> The rate of defect repair is underestimated. <br> The size of the software is underestimated.                         |
Example of CASE tool: Visual Basic.
## Risk analysis

Assesses the probability and seriousness of each risk. Risk probability may be:

- **Very low** (<10%)
- **Low** (10-25%)
- **Moderate** (25-50%)
- **High** (50-75%)
- **Very** high (>75%)

Risk effects might be:

- **Catastrophic**
- **Serious**
- **Tolerable**
- **Insignificant**

| Risk                                                                 | Probability | Effects       |
|----------------------------------------------------------------------|-------------|----------------|
| Organisational financial problems force reductions in the project budget. | Low         | Catastrophic   |
| It is impossible to recruit staff with the skills required for the project. | High        | Catastrophic   |
| Key staff are ill at critical times in the project.                 | Moderate    | Serious        |
| Software components which should be reused contain defects which limit their functionality. | Moderate    | Serious        |
| Changes to requirements which require major design rework are proposed. | Moderate    | Serious        |
| The organisation is restructured so that different management are responsible for the project. | High        | Serious        |
| The database used in the system cannot process as many transactions per second as expected. | Moderate    | Serious        |
| The time required to develop the software is underestimated.       | High        | Serious        |
| CASE tools cannot be integrated.                                   | High        | Tolerable      |
| Customers fail to understand the impact of requirements changes.   | Moderate    | Tolerable      |
| Required training for staff is not available.                      | Moderate    | Tolerable      |
| The rate of defect repair is underestimated.                       | Moderate    | Tolerable      |
| The size of the software is underestimated.                        | High        | Tolerable      |
| The code generated by CASE tools is inefficient.                   | Moderate    | Insignificant  |
Identify the main risks by considering:

- All catastrophic risks.
- All serious risks that have more than a moderate probability of occurrence.

Rank such risks by order of importance.

## Risk planning

Consider each risk and develop a strategy to manage that risk:
- **Avoidance strategies**: The probability that the risk will arise is reduced.
- **Minimization strategies**: The impact of the risk on the project or product will be reduced.
- **Contingency plans**: If the risk arises, contingency plans are strategies to deal with that risk.

## Risk management strategies

| Risk                            | Strategy                                                                 |
|---------------------------------|--------------------------------------------------------------------------|
| Organisational financial problems | Prepare a briefing document for senior management showing how the project is making a very important contribution to the goals of the business. |
| Recruitment problems            | Alert customer of potential difficulties and the possibility of delays, investigate buying-in components. |
| Staff illness                   | Reorganise team so that there is more overlap of work and people therefore understand each other’s jobs. |
| Defective components            | Replace potentially defective components with bought-in components of known reliability. |
| Requirements changes            | Derive traceability information to assess requirements change impact, maximise information hiding in the design. |
| Organisational restructuring    | Prepare a briefing document for senior management showing how the project is making a very important contribution to the goals of the business. |
| Database performance            | Investigate the possibility of buying a higher-performance database. |
| Underestimated development time | Investigate buying in components, investigate use of a program generator. |
## Risk monitoring

Assess each identified risks regularly to decide whether or not it is becoming less or more probable. To perform assessment look at **risk factors**.

Also assess whether the effects of the risk have changed (in such case go back to risk analysis). Each key risk should be discussed at management progress meetings.
## Risk factors

| Risk Type      | Potential Indicators                                                                 |
|----------------|----------------------------------------------------------------------------------------|
| Technology     | Late delivery of hardware or support software, many reported technology problems       |
| People         | Poor staff morale, poor relationships amongst team members, job availability           |
| Organisational | Organisational gossip, lack of action by senior management                             |
| Tools          | Reluctance by team members to use tools, complaints about CASE tools, demands for higher-powered workstations |
| Requirements   | Many requirements change requests, customer complaints                                 |
| Estimation     | Failure to meet agreed schedule, failure to clear reported defects                     |
# Altri modelli
## Modello object-oriented

![[Pasted image 20250517040718.png]]

1. Minori costi di manutenzione
## Modello di ingegneria Concorrente

Ha come obiettivo la riduzione di tempi e costi di sviluppo, mediante un approccio sistematico al progetto integrato e concorrente di un prodotto software e del processo ad esso associato.

Le fasi di sviluppo coesistono invece di essere eseguite in sequenza.
## Modello basato su metodi formali

Comprende una serie di attività che conducono alla specifica formale matematica del software, al fine di eliminare ambiguità, incompletezze ed inconsistenze e facilitare la verifica dei programmi mediante l'applicazione di tecniche matematiche.

La Cleanroom Software Engineering (1987) ne rappresenta un esempio di realizzazione, in cui viene
enfatizzata la possibilità di rilevare i difetti del software in modo più tempestivo rispetto ai modelli tradizionali.

