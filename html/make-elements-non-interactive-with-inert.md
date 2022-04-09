# Tornar Elementos Não Interativos com Inert

O atributo global [`inert`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/inert) é um booleano que pode ser aplicado a um elemento ou a uma seção de conteúdo em um documento HTML. Quando ele é `true`, esses elementos e qualquer coisa aninhada dentro deles não serão interativos.

```html
<div class="fancy-animation" inert>
  <!-- ... -->
</div>
```

Isso tem algumas implicações diferentes:

1. Eventos de clique não são disparados nesses elementos.
2. Esses elementos não poderão ganhar foco.
3. Esses elementos e conteúdos ficam ocultos para tecnologias assistivas.

Isso é útil para várias situações. Em particular, é bom para acessibilidade quando uma parte do documento, como uma animação sofisticada, não deve ser percorrida por tecnologias assistivas.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
- [Documentação do MDN sobre o atributo inert](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/inert)