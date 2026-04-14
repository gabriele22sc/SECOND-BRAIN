# Link
[[React Native Reanimated]]



**React Native** è un framework open-source sviluppato da Facebook che permette di costruire applicazioni mobili **nativamente** per iOS e Android utilizzando JavaScript e React. Basta scrivere una sola base di codice che funziona su entrambe le piattaforme, riducendo i tempi di sviluppo. 
React Native ti permette di utilizzare componenti già predefiniti per costruire interfacce utente, ma anche di scrivere codice nativo (in Swift per iOS o Java per Android) se necessario per ottenere funzionalità avanzate.

[Multi-factor Auth](https://rnfirebase.io/auth/multi-factor-auth)
# Concetti principali

1. **COMPONENTI**: i componenti possono essere "**completi**", ovvero gestiscono una schermata intera oppure "**atomic**" (piccole unità come pulsanti, input di testo, ecc.). è possibile utilizzare componenti nativi (View, Text, Button...);

2. **JSX**: sintassi simile ad HTML, ma con il potere di utilizzare JS. Permette di scrivere l'interfaccia utente similmente all'HTML ma integrando la logica di React;

3. Stato e [[PROPS]]: **State** rappresenta lo stato interno di un componente, mentre le **Props** sono le proprietà che vengono passate a un componente da un altro componente superiore;

4. **Navigazione**: React Native ha bisogno di una libreria di navigazione per passare tra diverse schermate (esempio: `react-navigation`). Non c'è un sistema di navigazione integrato come in altre piattaforme mobili, quindi è necessario installare librerie di navigazione esterne.

5. **API Native**: React Native consente di utilizzare molte delle API native del dispositivo (come la fotocamera, il GPS, i sensori) tramite librerie di terze parti, o tramite la scrittura di codice nativo (Java/Kotlin per Android, Swift/Objective-C per iOS) se necessario.



# Componenti e Librerie per funzionalità specifiche

Di seguito alcune librerie utili per l'<u>autenticazione</u>, i <u>pagamenti</u> e la <u>gestione delle sessioni</u>:
## 1. **Autenticazione**: 

- **Firebase Authentication**: implementazione facile per l'autenticazione tramite email, social media o autenticazione anonima;
- **Auth0**: piattaforma d'identità che supporta vari metodi di autenticazione, inclusi login social, SSO(Single Sing-on) e altro;
- **React Navigation + Auth Context**: per gestire il flusso di navigazione, utilizza un contesto, React Context API, per memorizzare lo stato di autenticazione e modificare la navigazione in base allo stato dell'utente.
## 2. **Pagamenti**:

- **Stripe**: soluzione più popolare per i metodi di pagamento, basta utilizzare la libreria **react-native-stripe-sdk** per integrare i pagamenti, [React-Native-Stripe-SDK](https://github.com/stripe/stripe-react-native);
- **Razorpay**: alternativa a Stripe [Razorpay](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://razorpay.com/&ved=2ahUKEwidyfSuvvaLAxWs-wIHHXqJBgkQFnoECCIQAQ&usg=AOvVaw0ePhs7pjyQBoNeUL2S57Pl);
- **Paypal**: [SDK per i pagamenti](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.npmjs.com/package/react-native-paypal&ved=2ahUKEwjri9fOvvaLAxWm1QIHHeTxJPMQFnoECBcQAQ&usg=AOvVaw15-CV-NeaAnxjcP4Zv3Gc9).

## 3. **Gestione delle sessioni**

- **React Context API + AsyncStorage**: Puoi utilizzare la React Context API per gestire lo stato dell'app e **AsyncStorage** per persistere i dati (come i token di autenticazione), [React Context + AsyncStorage](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://reactnative.dev/docs/asyncstorage&ved=2ahUKEwj9lu6lv_aLAxVn2QIHHQadADwQFnoECBUQAQ&usg=AOvVaw2UXNxFI6h7dD1hBBtgfF2H);
- **React Query**: Ottimo per la gestione dei dati di sessione e per sincronizzare automaticamente le informazioni utente da un'API remota, [TanStack](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://tanstack.com/query&ved=2ahUKEwi__Pvqv_aLAxVxxQIHHeHbEtkQFnoECBYQAQ&usg=AOvVaw3qn0WJezFr3GISPoAk5Ocg), [React Query](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://handsonreact.com/docs/react-query&ved=2ahUKEwi__Pvqv_aLAxVxxQIHHeHbEtkQFnoECBUQAQ&usg=AOvVaw3hMwe0nbuaPj6yQdvD2kPE).