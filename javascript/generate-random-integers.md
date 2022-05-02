# Gerar Números Inteiros Aleatórios

O módulo `Math` do JavaScript possui uma função embutida chamada `random`.

```javascript
> Math.random();
0.4663311937101857
```

Ela pode ser usada para gerar números flutuantes aleatórios entre 0 e 1.

Se você quiser gerar números inteiros, no entanto, será necessário criar sua própria função.

```javascript
function getRandomInt(max) {
  return Math.floor(Math.random() * Math.floor(max));
}

> getRandomInt(10);
1
> getRandomInt(10);
7
> getRandomInt(10);
2
```

Essa função permite gerar números aleatórios entre `0` (inclusivo) e `max`, um número que você especificar (exclusivo).

# Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
- [Documentação MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)