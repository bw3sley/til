# Verificar Classes em um Elemento DOM

Você pode usar a propriedade [`classList`](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList) para verificar quais classes foram atribuídas a um elemento DOM.

Supondo o seguinte elemento DOM:

```html
<div id="auth-modal" class="modal hidden">...</div>
```

Uma vez que você tenha uma referência a esse elemento, usando o seu método preferido (por exemplo, [`Document.getElementById`](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById)), você pode começar a inspecionar a lista de classes:

```javascript
> element.classList.contains("modal")
true

> element.classList.contains("hidden")
true

> element.classList.contains("taco")
false

> element.classList.toString()
"modal hidden"
```

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)