# Aplicar Classes do Tailwind a uma Classe CSS Existente

Digamos que eu tenha algum HTML no meu aplicativo que não controlo totalmente — pode ser um componente de terceiros ou algo renderizado por um transformador de Markdown. Independentemente disso, acabo com algum HTML onde as tags têm nomes de classes que gostaria de estilizar.

```html
<div class="code-block">
  <!-- ... -->
</div>
```

Se fosse HTML (ou JSX) que eu estivesse escrevendo, poderia adicionar qualquer classe do Tailwind que quisesse nas várias tags para obter o estilo perfeito. Mas, como não controlo o HTML diretamente, preciso encontrar outra maneira de _aplicar_ essas classes do Tailwind.

É aí que entra a [diretiva `@apply` do Tailwind](https://tailwindcss.com/docs/functions-and-directives#apply). Com ela, posso direcionar um seletor de classe existente usando qualquer classe utilitária do Tailwind. Adicione linhas como as seguintes ao seu arquivo raiz `tailwind.css`.

```css
@tailwind base;
@tailwind components;
@tailwind utilities;

/* estilos adicionais aqui 👇 */
.code-block {
  @apply bg-gray-200 rounded-md p-4;
}
```

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)