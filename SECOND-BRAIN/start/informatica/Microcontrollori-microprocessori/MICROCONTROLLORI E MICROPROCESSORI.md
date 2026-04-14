I concetti di pull-up e pull-down sono fondamentali per evitare che. PIN di input si trovino in uno stato “indeterminato”.

# Resistenza di Pull-Up
La configurazione Pull-Up serve a mantenere il pin a un livello logico **ALTO(HIGH,1)** quando l’interruttore è aperto.
- **Collegamento**: una resistenza viene posta tra il pin del microcontrollore e l’alimentazione positiva(Vcc,3.3V o 5V);
- **Stato a riposo**: il pin legge Vcc, stato:1;
- **Pressione del tasto**: quando chiudi l’interruttore verso terra (GND), la corrente fluisce a massa e il pin legge 0.


# Resistenza di Pull-Down
La configurazione Pull-Down mantiene il pin a un livello logico BASSO(0) quanto l’interruttore è aperto.
- **Il collegamento**: la resistenza è posta tra il pin e la massa(GND);
- **Stato a riposo**: il pin è ”tirato giù” a 0V(stato logico 0);
- Pressione del tasto: Quando chiudi l’interruttore collegato a Vcc, la tensione sale e il microcontrollore legge 1.

