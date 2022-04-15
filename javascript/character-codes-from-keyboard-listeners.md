# Códigos de Caracteres em Listeners de Teclado

Se eu criar os seguintes listeners de eventos de teclado para `keydown`, `keypress` e `keyup`:

```javascript
window.addEventListener('keydown', function(e) { console.log("Keydown: " + e.charCode + ", " + e.keyCode); });
window.addEventListener('keypress', function(e) { console.log("Keypress: " + e.charCode + ", " + e.keyCode); });
window.addEventListener('keyup', function(e) { console.log("Keyup: " + e.charCode + ", " + e.keyCode); });
```

e depois pressionar `A`, o console do navegador exibirá o seguinte:

```
Keydown: 0, 65
Keypress: 65, 65
Keyup: 0, 65
```

Se eu pressionar `a`, o console do navegador exibirá:

```
Keydown: 0, 65
Keypress: 97, 97
Keyup: 0, 65
```

O evento `keypress` parece ser o mais adequado para capturar o código do caractere. No entanto, parece haver bastante [incompatibilidade e falta de suporte](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent#Browser_compatibility) entre navegadores para vários aspectos dos eventos de teclado.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)