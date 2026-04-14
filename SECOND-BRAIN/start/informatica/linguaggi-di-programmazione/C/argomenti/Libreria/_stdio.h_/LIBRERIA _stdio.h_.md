Tra le funzioni più utilizzate abbiamo:

# FGETS
```
char buff[100];
int n =10;

printf(”Enter a string: \n”);

// legge un input dall’utente
fgets(buff,n,stdin);
printf(”Hai inserito: %s”,buff);
```

1. `int n = 10`, non indica la dimensione dell’array ma il numero massimo di caratteri che `fgets` leggerà, incluso `\0`;
2. `fgets(buff,n,stdin)`:
	- `buff`$\to$ dove mettere la stringa letta;
	- `n`$\to$ massimo numero di caratteri da leggere, incluso `\0`;
	- `stdin`$\to$ indica che stai leggendo da input standard;
Quindi, legge al massimo `n-1` caratteri della tastiera. Qui `n = 10`, quindi leggerà fino a 9 caratteri utili. Aggiunge automaticamente il carattere `\0` alla fine per terminare la stringa. Se l’utente preme invio prima di arrivare a 9 caratteri, `fgets` include il carattere di nell’intento `\n` nella stringa letta.