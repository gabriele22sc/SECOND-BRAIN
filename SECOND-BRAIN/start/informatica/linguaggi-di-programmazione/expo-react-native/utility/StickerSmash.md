
[StickerSmash](https://github.com/expo/examples/tree/master/stickersmash/app)

## 📂 **Struttura di base di StickerSmash con TypeScript**

```
StickerSmash/
│-- assets/             # Contiene immagini, font e altri file statici
│-- components/         # Contiene i componenti riutilizzabili (.tsx)
│-- hooks/              # Contiene custom hooks per la logica (.tsx)
│-- navigation/         # Configurazione della navigazione tra schermate (.tsx)
│-- screens/            # Contiene le varie schermate dell'app (.tsx)
│-- types/              # Definizioni dei tipi TypeScript (facoltativo)
│-- App.tsx             # File principale dell'app (entry point)
│-- package.json        # Configurazione del progetto e dipendenze
│-- app.json            # Configurazione Expo (icone, splash screen, ecc.)
│-- tsconfig.json       # Configurazione di TypeScript
│-- babel.config.js     # Configurazione per Babel
│-- metro.config.js     # Configurazione di Metro Bundler
```


## 📜 **Dettaglio delle cartelle**

### 📂 **1. `components/`**

Qui trovi i componenti riutilizzabili scritti in TypeScript.

> 💡 **Esempio di un bottone tipizzato (`components/Button.tsx`)**

```
import { Pressable, Text } from 'react-native';

type ButtonProps = {
  title: string;
  onPress: () => void;
};

export default function Button({ title, onPress }: ButtonProps) {
  return (
    <Pressable onPress={onPress} style={{ padding: 10, backgroundColor: 'blue' }}>
      <Text style={{ color: 'white' }}>{title}</Text>
    </Pressable>
  );
}
```

🔹 **Vantaggio**: Se provi a passare una `string` al posto di `onPress`, TypeScript ti avviserà dell'errore.

---

### 📂 **2. `hooks/`**

Qui trovi i **custom hooks** tipizzati per la logica dell’app.

> 💡 **Esempio di custom hook (`hooks/usePermissions.tsx`)**

```
import { useEffect, useState } from 'react';
import * as ImagePicker from 'expo-image-picker';

export function usePermissions() {
  const [hasPermission, setHasPermission] = useState<boolean>(false);

  useEffect(() => {
    (async () => {
      const { status } = await ImagePicker.requestMediaLibraryPermissionsAsync();
      setHasPermission(status === 'granted');
    })();
  }, []);

  return hasPermission;
}
```


### 📂 **3. `navigation/`**

Qui trovi la **navigazione** con TypeScript.

> 💡 **Esempio di navigazione in `navigation/StackNavigator.tsx`**

```
import { createStackNavigator } from '@react-navigation/stack';
import { NavigationContainer } from '@react-navigation/native';
import HomeScreen from '../screens/HomeScreen';
import EditorScreen from '../screens/EditorScreen';

export type RootStackParamList = {
  Home: undefined;
  Editor: undefined;
};

const Stack = createStackNavigator<RootStackParamList>();

export default function StackNavigator() {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Editor" component={EditorScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}
```


### 📂 **4. `screens/`**

Qui trovi le schermate tipizzate.

> 💡 **Esempio di schermata (`screens/HomeScreen.tsx`)**


```
import { View, Text, Button } from 'react-native';
import { StackNavigationProp } from '@react-navigation/stack';
import { RootStackParamList } from '../navigation/StackNavigator';

type HomeScreenProps = {
  navigation: StackNavigationProp<RootStackParamList, 'Home'>;
};

export default function HomeScreen({ navigation }: HomeScreenProps) {
  return (
    <View>
      <Text>Benvenuto in StickerSmash!</Text>
      <Button title="Modifica Immagine" onPress={() => navigation.navigate('Editor')} />
    </View>
  );
}
```



### 📂 **5. `types/`**

Alcuni progetti creano questa cartella per raccogliere i tipi TypeScript in un unico posto.  
Esempio di `types/index.ts`:

```
export type Sticker = {
  id: number;
  image: string;
  x: number;
  y: number;
};
```

oppure in un altro file:

```
import { Sticker } from '../types';
const newSticker: Sticker = { id: 1, image: 'sticker.png', x: 50, y: 50 };
```

