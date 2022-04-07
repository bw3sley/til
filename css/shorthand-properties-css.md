# Propriedades abreviadas no CSS

As propriedades abreviadas (shorthand properties) no CSS permitem definir múltiplas propriedades relacionadas de forma concisa, economizando tempo e espaço no código.

### Exemplo de Propriedades de Background

Em vez de escrever várias declarações para definir a cor de fundo, imagem, repetição e posição, você pode usar uma única propriedade abreviada:

```css
background-color: #000;
background-image: url(images/bg.gif);
background-repeat: no-repeat;
background-position: left top;
```

Se torna:

```css
background: #000 url(images/bg.gif) no-repeat left top;
```

### Exemplo de Propriedades de Font

Você pode simplificar várias propriedades de fonte em uma única linha:

```css
font-style: italic;
font-weight: bold;
font-size: .8em;
line-height: 1.2;
font-family: Arial, sans-serif;
```

Se torna:

```css
font: italic bold .8em/1.2 Arial, sans-serif;
```

### Exemplo de Propriedades de Borda

As propriedades de borda também podem ser combinadas:

```css
border-width: 1px;
border-style: solid;
border-color: #000;
```

Se torna:

```css
border: 1px solid #000;
```

### Exemplo de Propriedades de Margem e Padding

Para `margin` e `padding`, você pode usar de uma a quatro declarações de valor:

```css
margin-top: 10px;
margin-right: 5px;
margin-bottom: 10px;
margin-left: 5px;
```

Se torna:

```css
margin: 10px 5px 10px 5px;
```

A regra é simples:
- **Um valor** aplica a todos os lados.
- **Dois valores** aplicam-se ao topo/baixo e esquerda/direita.
- **Três valores** aplicam-se ao topo, laterais e embaixo.
- **Quatro valores** seguem o sentido horário: topo, direita, baixo, esquerda.

## Referências

- [Documentação do MDN sobre Propriedades Abreviadas](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties)