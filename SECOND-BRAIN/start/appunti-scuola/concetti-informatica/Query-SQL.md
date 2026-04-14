setup DB dal cmd di XAMPP:
XAMPP shell -> cd mysql/bin -> mysql -u root -> create database nome_db; -> use nome_db; -> popola con tabelle.

**OPERATORI**:
`AND` -> filtra record basati su più di una condizione
`OR` -> filtra i record in base a due o più condizioni
`NOT` -> serve per ritornare il contrario 
`IS NULL` e `IS NOT NULL` -> non si possono usare con =,<,> o <>;  di solito vengono utilizzati per testare valori nulli ex: `SELECT CustomerName, ContactName, Address  FROM Customers WHERE Address IS NULL;`
`LIKE` -> è usato dopo `WHERE` e serve a cercare parole che iniziano con una lettera specifica. ex: `...WHERE CustomerName LIKE 'a%'`


**FUNZIONI DI AGGREGAMENTO**:
`MIN()` -> ritorna il valore minore di una colonna selezionata
`MAX()` -> ritorna il valore maggiore di una colonna selezionata
`COUNT()` -> ritorna il numero di righe o record in una colonna
`SUM()` -> ritorna la somma totale di una colonna numerica 
`AVG()` -> ritorna il valore più alto di una colonna numerica



**CARICAMENTO/MODIFICA DEI DATI**:
`SELECT` -> estrae dati dal database
`SELECT DISTINCT` -> estrae dati dal database eliminando i duplicati
`UPDATE` -> carica dati in un database
`DELETE` -> elimina dati da un database
`ORDER BY` -> ordina gli elementi di una Select secondo un record specifico




**OPERAZIONI CON TABELLE/DATABASE**:
`INSERT INTO` -> inserisce dati all'interno di un database
`CREATE DATABASE` -> crea un nuovo database
`ALTER DATABASE` -> modifica un database
`CREATE TABLE` -> crea una nuova tabella
`ALTER TABLE` -> modifica una tabella
`DROP TABLE` -> elimina una tabella
`JOIN` -> combina righe di due o più tabelle
`SELECT TOP` -> seleziona un numero di record da ritornare
`ADD` -> serve ad aggiungere una nuova colonna in una tabella. ex: `ALTER TABLE Customers ADD Email varchar(255);` 