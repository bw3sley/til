# Usando Tailwind Typography Prose no Modo Escuro

O Tailwind CSS pode ser configurado para fornecer estilos padrão tanto para o modo padrão (claro) quanto para o modo escuro. Uma vez configurado, você pode adicionar um mecanismo de alternância para mudar entre o modo claro e o modo escuro. [Este post](https://egghead.io/blog/tailwindcss-dark-mode-nextjs-typography-prose) explora todos esses detalhes.

Isso pode ser usado até mesmo com o plugin de [tipografia do Tailwind](https://github.com/tailwindlabs/tailwindcss-typography). O plugin `typography` fornece estilos padrão, o que é ótimo se você não controla o markup que está sendo renderizado ou se deseja aplicar alguns estilos padrão a um bloco de markup.

Um bloco de markup que usa tipografia ficará minimamente assim:

```jsx
<div className="prose">
  <h1>{title}</h1>
  {markdownAsHtml}
</div>
```

Para aplicar estilos padrão razoáveis para o modo escuro, você precisará adicionar uma classe de modo escuro. Usando o prefixo `dark`, você pode aplicar a classe `prose-dark` à div de nível superior.

```jsx
<div className="prose dark:prose-dark">
  <h1>{title}</h1>
  {markdownAsHtml}
</div>
```

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)