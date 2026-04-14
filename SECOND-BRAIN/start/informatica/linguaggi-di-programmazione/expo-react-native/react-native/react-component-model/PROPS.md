Vengono utilizzate per passare dati ai componenti e renderli più dinamici e riutilizzabili. Funzionano nello stesso modo di React, ma applicate a componenti nativi.

Per esempio:

```
import React from "react";
import { Text, View } from "react-native";

type Props = {
  name: string;
  age: number;
};

const UserInfo: React.FC<Props> = ({ name, age }) => {
  return (
    <View>
      <Text>Nome: {name}</Text>
      <Text>Età: {age}</Text>
    </View>
  );
};

export default UserInfo;
```

```
import React from "react";
import { SafeAreaView } from "react-native";
import UserInfo from "./UserInfo";

const App = () => {
  return (
    <SafeAreaView>
      <UserInfo name="Gabriele" age={30} />
    </SafeAreaView>
  );
};

export default App;
```