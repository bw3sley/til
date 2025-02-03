---
title: "Usar `SafeAreaView` para evitar notch e bordas inseguras"
author: "bw3sley"
slug: "avoid-notch-with-safe-area-view"
tags:
  - react-native
  - ios
  - layout
created_at: "2022-05-06"

---

# Usar `SafeAreaView` para evitar notch e bordas inseguras

`SafeAreaView` mantém o conteúdo dentro da área visível e segura do dispositivo, evitando notch, cantos arredondados e barras do sistema.

```tsx
import { SafeAreaView, Text, View } from "react-native";

export const App = () => {
  return (
    <SafeAreaView style={{ flex: 1, backgroundColor: "#e6e6e6" }}>
      <View>
        <Text>Renderizado com segurança.</Text>
      </View>
    </SafeAreaView>
  );
};
```
