# Enviar um Formulário com um Botão Fora do Formulário

Você pode vincular um botão de envio a um formulário em que o botão não está inserido. O truque é dar um `id` ao formulário e, em seguida, referenciar esse `id` com a propriedade `form` do botão.

```html
<div>
  <form id="meu-formulario">
    <label for="name">Nome:</label>
    <input type="text" name="name"></input>
  </form>

  <!-- ... -->

  <button type="submit" form="meu-formulario">Enviar</button>
</div>
```

Com essa configuração, clicar no botão _Enviar_ fará com que o formulário seja enviado.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
- [Documentação do MDN sobre o botão](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button) para mais detalhes.