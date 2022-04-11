# Selecionar um Elemento com um Atributo que Contém uma String Específica no CSS

No CSS, você pode usar seletores de atributo para selecionar elementos com base em uma string contida em um atributo específico. Isso é útil quando você quer estilizar elementos que possuem uma substring específica em um atributo.

### Exemplo de Uso

Para selecionar elementos cujo atributo `data-type` contém a string `"produto"`, você pode usar o seletor `*=` no CSS:

```css
[data-type*="produto"] {
  background-color: #f0f8ff;
  border: 1px solid #333;
}
```

Esse seletor `[data-type*="produto"]` aplicará os estilos a qualquer elemento que tenha `data-type` com o valor que contém `"produto"` em qualquer parte da string.

### Outros Seletores de Atributo

Além de `*=` (contém a substring), existem outros seletores de atributo:
- `^=`: Seleciona elementos cujo atributo começa com a substring.
- `$=`: Seleciona elementos cujo atributo termina com a substring.

### Exemplo Prático

```html
<div data-type="produto-novo">Produto Novo</div>
<div data-type="produto-usado">Produto Usado</div>
<div data-type="servico">Serviço</div>
```

Com o CSS acima, apenas os elementos `produto-novo` e `produto-usado` terão o estilo aplicado.

## Referências

- [💡 khanhicetea/today-i-learned](https://github.com/khanhicetea/today-i-learned)