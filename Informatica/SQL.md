# COMANDI DDL E DML DEL LINGUAGGIO SQL

## CREATE
Tale comando viene utilizzato per creare oggetti del database. Come possono essere tabelle (come abbiamo visto), ma anche indici, viste ecc...

#### ESEMPIO:

```sql
CREATE TABLE nome_tabella (
  colonna1 tipo_dato1,
  colonna2 tipo_dato2,
);
```

## ALTER
Esso viene utilizzato per modificare(alterare) degli oggetti già esistenti nel database( esempio tipico le tabelle).

#### ESEMPI:

(Aggiunta di una colonna)
```sql
ALTER TABLE nome_tabella
ADD colonna tipo_dato;
```

(Modifica di una colonna)
```sql
ALTER TABLE nome_tabella
ALTER COLUMN colonna tipo_dato;
```

(Eliminazione di una colonna)
```sql
ALTER TABLE nome_tabella
DROP COLUMN colonna;
```

## DROP
Viene utilizzato per eliminare oggetti del database. Come possono essere tabelle (come abbiamo visto), ma anche indici, viste ecc...

#### ESEMPIO:
```sql
DROP TABLE nome_tabella;
```

## INSERT
Viene utilizzato per inserire nuove righe di dati di una specifica tabella.

Il caso specifico che abbiamo visto è stato per inserire valori **specifici** per tutte le colonne di una precisa tabella.

#### ESEMPIO:
```sql
INSERT INTO nome_tabella (colonna1, colonna2, ...)
VALUES (valore1, valore2, ...);
```

## UPDATE
Viene utilizzato per modificare i dati esistenti in una o più righe di una tabella. Consente di aggiornare tali valori attraverso determinate condizioni.

#### ESEMPIO:
```sql
UPDATE nome_tabella
SET colonna1 = nuovo_valore1, colonna2 = nuovo_valore2, ...
WHERE condizione;
```

## DELETE
Esso viene utilizzato per eliminare una o più righe di una certa tabella(non come **drop** che la elimina per intera). Anche qui è possibile specificare delle condizioni per tale eliminazione.

#### ESEMPI:

(Eliminare righe da una tabella)
```sql
DELETE FROM nome_tabella
WHERE condizione;
```

(Eliminare una singola riga in base a una condizione)
```sql
DELETE FROM persone
WHERE id = 1;
```

# COMANDI SQL

## SELECT
Viene utilizzato per recuperare dei dati da una oppure più tabelle.
E' possibile specificare quali colonne e quali tabelle selezionare, ed anche specificare le condizioni per il filtramento dei dati. 

#### ESEMPI:

(Esempio generico)
```sql
SELECT colonna1, colonna2, ...
FROM nome_tabella
WHERE condizione;
```

(Esempio per selezionare tutte le colonne di una tabella)
```sql
SELECT *
FROM nome_tabella;
```

### Funzioni di aggregazione
- COUNT: Restituisce il numero di righe che soddisfano una determinata condizione.
#### Esempio: 
```sql
SELECT COUNT(*) FROM tabella;
```

- SUM: Restituisce la somma dei valori di una colonna numerica.
#### Esempio: 
```sql
SELECT SUM(colonna) FROM tabella;
```

- AVG: Restituisce la media dei valori di una colonna numerica.
#### Esempio: 
```sql
SELECT AVG(colonna) FROM tabella;
```

- MAX: Restituisce il valore massimo di una colonna.
#### Esempio: 
```sql
SELECT MAX(colonna) FROM tabella;
```

- MIN: Restituisce il valore minimo di una colonna.
#### Esempio:
```sql
SELECT MIN(colonna) FROM tabella;
```

## JOIN 
Viene utilizzato per combinare dati da due o più tabelle in base a una condizione di correlazione tra le colonne delle tabelle coinvolte.
Ne esistono diversi tipi, noi abbiamo vistro l' **Inner Join**.<br>
**Inner Join:** restituisce solo le righe che hanno una corrispondenza nelle due tabelle coinvolte.

### ESEMPI:

(Esempio di Join generico)
```sql
SELECT *
FROM tabella1
JOIN tabella2 ON tabella1.colonna = tabella2.colonna;
```

(Esempio di Inner Join)
```sql
SELECT *
FROM tabella1
INNER JOIN tabella2 ON tabella1.colonna = tabella2.colonna;
```

## GROUP BY
Viene utilizzato per raggruppare le righe di una tabella in base ai valori di una o più colonne. Esso consente di eseguire le funzioni di aggregazioni elencate prima.

#### ESEMPIO:
```sql
SELECT colonna1, colonna2, ..., funzione_aggregazione(colonna)
FROM nome_tabella
GROUP BY colonna1, colonna2, ...;
```
Un'altra funzione di aggregazone, utilizzate insieme al **group by** è

#### HAVING: 
Utilizzato insieme a GROUP BY per filtrare i risultati in base a una condizione aggregata.
#### ESEMPIO: 
```sql
SELECT colonna FROM tabella GROUP BY colonna HAVING COUNT(*) > 2;
```

<br><br>
by ***Enrico Marinelli*** *5B-IA*




