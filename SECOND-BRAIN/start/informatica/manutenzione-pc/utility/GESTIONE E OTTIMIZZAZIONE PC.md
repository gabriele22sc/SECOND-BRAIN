# Ottimizzazione delle prestazioni del sistema

Per attivare la modalità prestazioni elevate:
- Windows: 
	1. Vai in **Pannello di Controllo** -> **opzioni risparmio energia**;
	2. Seleziona **Prestazioni elevate**;

Ridurre gli effetti visivi:
1. Apri **Esegui(Win+R)** -> digita `sysdm.cpl` e premi **Invio**;
2. Vai su **Avanzate** -> **Prestazioni** -> **Impostazioni**;
3. Seleziona Regola per ottenere le prestazioni migliori.

# Liberare risorse e ottimizzare il disco

- Disinstalla software inutili: vai su Pannello di controllo -> Programmi e funzionalità e rimuovi ciò che non serve;
- Elimina i file temporanei(Windows):

	1. Premi `Win+R`, digita `%temp%`, premi Invio e cancella tutto;
	2. Apri nuovamente `Win+R`, digita `temp` e cancella anche qui;
	3. Apri ancora `Win+R`, digita `prefetch` e cancella i file;

- Deframmenta il disco (solo per HDD, non SSD):

	1. Apri **Esplora file**, clic destro su `C:` -> Proprietà;
	2. Vai su **Strumenti** -> **Ottimizza e deframmenta unità**.

- Attiva il TRIM per SSD(Windows):
	1. Apri il Prompt dei comandi come amministratore;
	2. Digita `fsutil behavior query DisableDeleteNotify`;
	3. Se il valore è `0` allora il TRIM è attivo; se è `1` per attivarlo:

```
fsutil behavior set DisableDeleteNotify 0
```

# Gestione della RAM e della CPU

Aumenta la memoria virtuale(Windows):
1. Apri **Esegui**(`Win+R`) -> digita `sysdm.cpl` e premi **Invio**;
2. Vai su **Avanzate** -> **Prestazioni** -> **Impostazioni**;
3. Nella scheda Avanzate, sotto **Memoria virtuale**, clicca su **Cambia**;
4. Imposta un valore manuale(minimo=quantità di RAM installata, massima=il doppio della RAM);
5. Riavvia il PC.

Usa un programma di gestione della RAM(opzionale):
- **Windows**: RAMMap, Mem Reduct;
- **Mac**: Memory clean.


# Overclock (opzionale)

Se possiedi un buon sistema di raffredamento, puoi overcloccare CPU/GPU per prestazioni extra:
- **CPU**: usa BIOS o software come **Intel XTU** o **AMD Ryzen Master**;
- **GPU**: usa **MSI Afterburner**.

