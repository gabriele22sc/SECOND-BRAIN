## #MySQL: le basi

Nato nel 1996 dall'azienda svedese Tcx, MySQL è un RDBMS open source e libero diffusissimo nel mondo dell'IT. Viene eseguito come servizio o deamon(demone), ovvero un programma in esecuzione continua nel sistema operativo con il compito di rimanere in attesa di richieste finalizzate alla fruizione di alcune funzionalità. Tutto lo scambio di dati con il demone avrà lo scopo di gestire il database.

Il demone alla base del DBMS viene chiamato MYSQLD, con esso vengono forniti programmi per l'avvio del server, tra i più noti: mysqld_safe, per un avvio sicuro del server, e mysqld_multi, per l'avvio di più server installati.

alcuni esempi di query:
```
SELECT nome, data_assunzione, stipendio
FROM dipendenti
WHERE stipendio >1800
```

```
SELECT, FROM e WHERE: sono parole chiave;
nome, data_assunzione, stipendio…: sono campi;
stipendio>1800: è una condizione;
```


[SINTASSI E ALTRO](https://cs.unibg.it/savo/didattica/files/GuidaMySQLWindow.pdf)

[REFERENCE1](https://www.w3schools.com/sql/default.asp)
[REFERENCE2](https://www.tutorialrepublic.com/sql-tutorial/sql-get-started.php)


# Query annidate

Una costante in una clausola WHERE può essere rimpiazzata con l'interrogazione che genera tale costante:

```
SELECT Nome, Cognome, Dipartimento
FROM Impiegati
WHERE Stipendio = (SELECT MAX(Stipendio) FROM Impiegati);
```

La sotto-interrogazione deve essere racchiusa tra () è ha un solo ; perché l'interrogazione è solo una.