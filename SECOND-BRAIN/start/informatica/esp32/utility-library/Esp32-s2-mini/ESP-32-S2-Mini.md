![[Pasted image 20260319214849.png]]

# 1. Pin di alimentazione
Servono a dare energia alla scheda o a prenderla dai componenti:
- **5V**: ingresso/uscita a 5 volt;
- **3V3**: uscita a 3.3 volt regolata(tensione a cui lavora il chip, NON COLLEGARE IL 5V);
- **G(GND)**: polo negativo, per chiudere i circuiti.
# 2. Pin di controllo 
- **RST(reset)**: se lo colleghi a GND, la scheda si riavvia;
- **BOOT**: serve per mettere la scheda in modalità programmazione se l’invio del codice fallisce.
# 3. Pin digitali(GPIO)
Quasi tutti i pin della scheda sono **Multi-funzione**. Possono essere usati come:
- **Digital I/O**: pinMode(x,OUTPUT) o INPUT;
- **PWM**: per variare l’intensità di un LED o muovere un servomotore;
- **ADC(Analogico)**: per leggere valori da un potenziamento

# 4. Altri Pin
### Pin di Boot
Questi determinano cosa fa la scheda nel momento in cui riceve corrente:
- **GPIO 0**: se è collegato a massa(GND) all’accensione la scheda entra in modalità “Firmware Download”. Se ci colleghi un pulsante o un sensore che lo tiene basso, il tuo codice non partirà mai;
- **GPIO 45 e 46**: sono pin di configurazione interna, il GPIO 46 è solo entrata in molte versioni della S2. Sconsigliati come uscite per LED o relè.

### LED RGB di sistema
Il quadrato bianco, **LED Neopixel(WS2812B)**, è collegato al **GPIO 18**. 

**NB**: essendo un LED Smart richiede una libreria(Adafruit NeoPixel) per cambiare colore. È perfetto per feedback visivi.

### Pin di comunicazione 
Per collegare sensori di pressione, schermi o comunicare con il PC, userai questi:
- **I2C(PIN 33 e 35)**: i pin standard per il protocollo I2C sono il **33(SDA)** e il **35(SCL)**. Usati per collegare i display OLED e i sensori moderni;
- **UART(TX e RX)**: per la comunicazione seriale, ma si possono utilizzare come normali GPIO, se vengono occupati non potrai mai utilizzare il serial.print() per vedere i messaggi sul PC durante il debug;
- **USB nativa(PIN 19 e 20)**: i pin 19(D-) e pin 20(D+) sono quelli che permettono alla scheda di comportarsi come una tastiera o un mouse se collegata da un PC.

### Convertitori Analogico-Digitali(ADC)
Per leggere un valore che varia(potenziometro o sensore di luce):
- **Pin da 1 a 10**: sono collegati all’**ADC1**. I migliori da usare perchè funzionano anche quando il Wi-Fi è acceso;
- **Pin da 11 a 20**: sono collegati all’**ADC2**. A volte smettono di leggere correttamente i valori analogici se utilizzi il wi-fi contemporaneamente.