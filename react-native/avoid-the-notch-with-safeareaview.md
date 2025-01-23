# Evite o Notch com SafeAreaView

Dispositivos iOS, especialmente o iPhone X, possuem áreas da tela que são cortadas de maneiras que apresentam um grande desafio para os desenvolvedores. Uma das maneiras mais fáceis de lidar com cantos arredondados e o notch ao desenvolver para iOS é evitá-los completamente.

> O objetivo do `SafeAreaView` é renderizar o conteúdo dentro dos limites seguros de um dispositivo.

```javascript
import { SafeAreaView, View, Text } from 'react-native';

const App = () => {
  return (
    <SafeAreaView style={{ flex: 1, backgroundColor: "#e6e6e6" }}>
      <View>
        <Text>Renderizado com segurança na área visível do dispositivo!</Text>
      </View>
    </SafeAreaView>
  );
}
```

A área _unsafe_ pode ser estilizada como você quiser, e tudo dentro de `<SafeAreaView>` será movido para a área visível da tela.

Créditos: 

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
- [Documentação do React Native](https://reactnative.dev/docs/safeareaview.html)

- Dillon Hafer