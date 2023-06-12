# I Database
## Le basi
I database nascono come alternativa ai precedenti **record**, a causa della poca flessibilità, dei priblemi di **accesso concorrente** e quindi di coerenza dei dati.<br>

Ogni database ha un sistema di gestione automatico, detto **DBMS** e tutte le operazioni, dette **transazioni** che permermettono di ottenere una **vista**.<br>

Ogni transazione deve:
- essere **atomica** ovvero non visibile dall'esterno e non può essere interrotta
- essere **consistente** ovvero dice che un database deve essere coerente
- essere **isolation** ovvero non si può vedere cosa succede durante una transazione
- essere **durabie** ovvero il suo effetto deve essere permanente
Tutto si racchiude nell'acronimo **ACID**.

Esiste anche un sistema di **rollback**, che permette far di tornare il database al momento prima della transazione.

---

## Lo schema ER (entità e relazione)
Esemprio di database con uno schema ER, con anche le relazioni

```mermaid
  erDiagram
    ALUNNO }o--|| CLASSE : HA
    ALUNNO {
        INT ID
        VARCHAR Nome
        VARCHAR Cognome
    }    
    CLASSE {
        INT ID
        INT Anno
        VARCHAR Sezione
    }
```
> leggenda delle cardinalità :
> - |o è (0,1)
> - || è (1,1)
> - }o è (0,N)
> - }| è (1,N) 

---

## Lo schema logico
Esempio del database soprastante con uno schema logico<br>
`Studente: ID, Nome, Cognome, IDClasse;`<br
`Classe: ID, Anno, Sezione;`<br

Con cardinalità si intende i valori minimi e massimi di un’associazione. In ogni associazione tra due
entità troviamo due minimi e due massimi; per trovare la cardinalità estraiamo i due massimi e li
mettiamo insieme, formando una nuova cardinalità. E’ fondamentale essere precisi nel definire i
minimi, poiché se definiti incorrettamente, potremmo non avere informazioni precise sulla natura
dell’entità e quindi non capire se potrebbe rivelarsi essere null o un qualunque numero nel minimo.
Quando parliamo di cardinalità troviamo varie casistiche:
- Cardinalità 1 a n: La chiave dell’entità con cardinalità minore viene inserita come Foreign Key
nell’entità con cardinalità maggiore
- Cardinalità 1 a 1: Gli attributi delle due entità vengono messi insieme creando un'unica entità
- Cardinalità n a n: L’associazione viene considerata un’entità assestante formata dalle due
chiavi primarie delle due entità allo scopo di inserire, se necessario, ulteriori attributi che
implementino ulteriori funzioni  

---

## La normalizzazione
Le 3 regole per la normalizzazione:
- **La prima regola**: non utilizzare campi multipli in una singola tabella per memorizzare dati simili.
- **La seconda regola**: tutti i campi di una tabella devono dipendere da tutta la chiave primaria.
- **La terza regola**: tutti i campi di una tabella che non sono relativi dalla chiave non appartengono alla tabella.

<br><br>
by ***Leonardo Canu*** *5B-IA*
