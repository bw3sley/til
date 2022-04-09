# Desativar o _autocomplete_ para um Campo de Formulário

O navegador tenta ser útil ao fazer sugestões informadas sobre o que deve ser preenchido automaticamente nos campos de formulário.

No entanto, pode ser que não queiramos esse comportamento. Ele pode ser uma fonte de erros na entrada de dados, um incômodo ou simplesmente algo que não queremos que nossos usuários experimentem.

Podemos desativar essa funcionalidade em um nível individual de campo com o atributo `autocomplete`:

```html
<input type="email" id="email" name="email" autocomplete="off">
```

Nota: O valor é `off` e não algo como `false`.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
- [Documentação do MDN sobre Como desativar o autocomplete para um campo de formulário](https://developer.mozilla.org/en-US/docs/Web/Security/Securing_your_site/Turning_off_form_autocompletion)
