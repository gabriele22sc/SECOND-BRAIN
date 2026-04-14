## **PROCEDURA CREAZIONE PROGETTO UTILIZZANDO ESP-IDF:**

[Per documentazione, installazione e debugging](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html&ved=2ahUKEwjJ3dPzn9yLAxXh9rsIHY_RJkQQFnoECB4QAQ&usg=AOvVaw3rlKiQNPlN-BLJMQgnfbeg)

1. Crea la directory del progetto:
```
idf.py create-project my_project_name
```

1. Modifica il codice	->	`my_project_name.c`

2. Flasha il codice nell'esp:

```
idf.py build
```

3. E monitora l'output seriale:

```
idf.py -p COM5 flash monitor
```

4. Per cancellare il file caricato sull'esp(N.B. chiudi il cmd dove hai runnato il monitor prima):

```
idf.py -p COMx erase_flash 
```

oppure dal cmd normale:

```
esptool.exe --port COMx erase_flash
```
