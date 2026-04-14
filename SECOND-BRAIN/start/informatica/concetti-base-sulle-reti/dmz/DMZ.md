Una **DMZ (Demilitarized Zone)** è una sottorete, fisica o logica, che funge da area cuscinetto tra una rete interna sicura e una rete esterna non affidabile, come Internet. 

# Scopi ed utilità

Il suo scopo principale è esporre servizi accessibili pubblicamente, come server web, server di posta elettronica o server DNS, riducendo il rischio che attacchi esterni compromettano la rete interna. Tale configurazione viene normalmente utilizzata per permettere ai server posizionati sulla DMZ di fornire servizi all’esterno senza compromettere la sicurezza della rete aziendale interna, per esempio:
- posta elettronica;
- Application Server.

# Tipi di DMZ

### Modalità vicolo cieco

![[dmz-vicolo-cieco.png]]

### Modalità cuscinetto

![[dmz-cuscinetto.png]]

# Applicazioni

- **posta elettronica**: l’installazione di un server mail all’interno della rete aziendale comporta la pubblicazione del servizio SMTP. In pratica, il server che pubblica il servizio SMTP viene collocato in DMZ ed eventualmente anche la webmail, l’antispam e l’antivirus; in LAN restano il server che ospita il database delle caselle e gli altri servizi;
- **Application Server**: che isolano un database residente in LAN ma ne offrono un’interfaccia verso l’esterno;
- Generalmente in DMZ si installano i server detti front-end, a cui corrispondono i relativi back-end in LAN.