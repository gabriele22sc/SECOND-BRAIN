# Link

[[StickerSmash]]
[expo-guide](https://docs.expo.dev/)

# Che cos'è e come funziona Expo

Expo è un **toolset** orientato su React Native(framework di JS e React), che semplifica lo sviluppo di app mobili, mentre Expo semplifica l'uso di React Native. Supporta OTA(Over-The-air updates), ovvero aggiorna la tua applicazione senza passare attraverso gli store(App Store/Google Play).

Quando programmi in **React Native**, utilizzi JavaScript come in React JS ma invece di renderizzare elementi HTML verranno renderizzati i componenti nativi. I due componenti più utilizzati sono `View` e `Text`. Es:
```
import React from 'react'
import {View, Text} from 'react-native'

const App = () => {
	return (
		<View>
			<Text>Hello World!</Text>
		</View>
	)}
```



## Componenti
I componenti sono indipendenti e riusano parti di codice. Hanno gli stessi scopi delle funzioni JS ma lavorano in un ambiente isolato e ritornano HTML o jsx.


## Vantaggi di Expo

✅ **Facile da configurare** (senza bisogno di Xcode o Android Studio)  
✅ **Hot Reload** per testare rapidamente le modifiche  
✅ **Supporto a molte API native senza codice nativo**  
✅ **Test su dispositivi reali con Expo Go**

## Limitazioni di Expo

❌ Le app possono essere più pesanti rispetto a quelle costruite con React Native puro  
❌ Alcune funzionalità avanzate richiedono l'**eject** da Expo (convertendo l'app in una normale app React


## Organizzazione di una FlatList

console.log():
```
import {View, Text, FlatList} from "react-native";

const Listdata = () => {
	const fruits = ["apple", "banana", "orange"];

	return (
		<View>
			<FlatList data={fruits} renderItem={({item}) => console.log({item})}/>
		</View>
	);
};
```

visualizzati come testo:
```
import {View, Text, FlatList} from "react-native";

const Listdata = () => {
	const fruits = ["apple", "banana", "orange"];

	return (
		<View>
			<FlatList data={fruits} renderItem={({item}) => {
			return <Text>{item}</Text>;
				}}
			/>
		</View>
	);
};
```

# Props

I Props, o Properties, sono argomenti passati ai componenti tramite attributi HTML

es:

```
const ChildComponent = (props: ChildProps) => {
	return (
		<View>
			<Text>Child Component</Text>
			<Text>{props.name}</Text>
			<Text>{props.age}</Text>
			<Text>{props.hobbies}</Text>
		</View>
	);
};
```

il componente verrà poi passato come argomento

```
const ParentComponent = () => {
	return (
		<View>
			<Text>Parent Component</Text>

			<ChildComponent
				name = "Gabriele"
				age = {22}
				hobbies = {["cantare", "programmare", "cucinare"]}
			/>
		</View>
	);
};
```



# State 

**State** è un oggetto React integrato utilizzato per contenere dati o informazioni sul componente. Lo stato di un componente può cambiare nel tempo; ogni volta che cambia, il componente viene nuovamente renderizzato.

# Hooks

Questa cartella contiene **Custom Hooks**, cioè funzioni che sfruttano gli hooks di React per incapsulare logiche riutilizzabili. ES:
- `useAuth.ts`: gestione dell'autenticazione dell'utente;
- `useFetch.ts`: per effettuare richieste API in modo più semplice;
- `useTheme.ts`: gestione del tema chiaro/scuro.

Esempio di file `Api.ts`:
```
export const API_BASE_URL = "https://api.example.com"; export const API_TIMEOUT = 5000;
```

Esempio di file `Colors.ts`:
```
export default {
  primary: "#ff6600",
  secondary: "#0066ff",
  background: "#f4f4f4",
};
```

Gli Hooks permetto di utilizzare State ed altre funzionalità di React senza scrivere una classe. #useState permette di tracciare lo stato di un componente funzionale. Di solito fa riferimento a dati o props che necessitano di essere tracciati nell'applicazione.


# Scripts

Contiene **script personalizzati** eseguibili dal CLI per l'automatizzazione di alcune operazioni. Esempi di script comuni:
- `build-and-upload.sh`: script shell per compilare e caricare l'app su Expo o negli store;
- `generate-icons.ts`: genera automaticamente le icone dell'app;
- `reset-cache.js`: pulisce la cache di Expo.

Esempio di `reset-cache.js`:
```
const { execSync } = require("child_process");

console.log("Pulizia della cache di Expo...");
execSync("expo r -c", { stdio: "inherit" });
console.log("Cache pulita con successo!");
```

