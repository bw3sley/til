# O seletor `:where()` no CSS

O seletor `:where()` no CSS é uma pseudo-classe que permite agrupar seletores sem adicionar especificidade extra ao conjunto de regras. Isso significa que ele pode ser útil para estilizar elementos de maneira flexível sem impactar a prioridade de outros estilos.

## Sintaxe

```css
:where(selector1, selector2, ...) {
  /* Estilos aplicados */
}
```

## Exemplo de Uso

Imagine que você queira aplicar um estilo comum a `<h1>`, `<h2>` e `<h3>`, mas sem aumentar a especificidade, permitindo que regras mais específicas possam sobrescrevê-lo facilmente.

```css
:where(h1, h2, h3) {
  color: blue;
  font-weight: bold;
}
```

Isso aplicará a cor azul e negrito para todos os `<h1>`, `<h2>` e `<h3>`, mas sem aumentar a especificidade desses seletores.

## Comparação com `:is()`

O `:where()` funciona de maneira semelhante ao `:is()`, mas com uma diferença fundamental: enquanto `:is()` mantém a especificidade do seletor mais forte dentro dele, `:where()` sempre tem especificidade zero.

```css
:is(h1, h2, h3) {
  color: blue;
}
```

Neste caso, a especificidade será igual ao seletor mais específico dentro de `:is()`. Já com `:where()`, a especificidade sempre será `0`, permitindo que outros estilos com seletores mais específicos possam sobrescrevê-lo facilmente.

## Quando Usar

- Para aplicar estilos padrões sem aumentar a especificidade.
- Para criar temas ou estilos globais sem interferir nos estilos mais específicos.
- Para agrupar seletores sem precisar se preocupar com conflitos de prioridade.

## Referências

- [MDN Web Docs: `:where()`](https://developer.mozilla.org/en-US/docs/Web/CSS/:where)