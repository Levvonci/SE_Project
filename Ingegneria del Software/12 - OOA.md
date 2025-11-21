# Identificazione delle associazioni

Alcuni attributi identificati con le classi rappresentano associazioni (ogni attributo di tipo
non primitivo dovrebbe essere modellato come un’associazione alla classe che rappresenta quel tipo di dato).

**Esempio**:
Se una classe Ordine ha un attributo cliente, e Cliente è una classe, allora “cliente” non è solo un campo, ma un riferimento a un oggetto Cliente, quindi va rappresentato come un’associazione tra Ordine e Cliente.

Ogni associazione ternaria dovrebbe essere rimpiazzata con un ciclo di associazioni binarie,
per evitare problemi di interpretazione.

**Esempio**:
Una relazione ternaria tra Studente, Corso, e AnnoAccademico può essere modellata con una classe Iscrizione associata singolarmente a ciascuna delle tre.

Nei cicli di associazioni almeno un’associazione potrebbe essere eliminata e gestita come
associazione derivata, anche se per problemi di efficienza spesso si introducono associazioni
ridondanti.

**Esempio**:
Se Cliente è associato a Ordine, e Ordine è associato a Fattura, potresti derivare un’associazione indiretta Cliente → Fattura. Tuttavia, potresti comunque mantenerla esplicitamente nel diagramma per semplicità o per esigenze tecniche.
# Specifica delle associazioni

Per **assegnare nomi alle associazioni** adottare la stessa convenzione usata per gli attributi (le
parole devono essere scritte in carattere minuscolo, separate da un carattere di underscore).

Assegnare nomi di ruolo (rolename) alle estremità dell’associazione (i rolename diventano i nomi
degli attributi nella classe all’estremità opposta dell’associazione).

Determinare la molteplicità delle associazioni (ad entrambe le estremità).
# Example C.3 – Contact Management

# Aggregazione

Rappresenta una relazione di tipo “whole-part” (contenimento) tra una classe composta (superset class) e l’insieme di una o più classi componenti (subset classes).

Può assumere quattro differenti significati:
- ExclusiveOwns (e.g. Book has Chapter, or Chapter is part of a Book).
	- Existence-dependency.
	- Transitivity.
	- Asymmetricity.
	- Fixed property
- Owns (e.g. Car has Tire)
	- No fixed property.
Has (e.g. Division has Department)
	• No existence dependency
	• No fixed property
Member (e.g. Meeting has Chairperson)
• No special properties except membership