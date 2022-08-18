---
title: "Entender por que um componente renderiza de novo"
author: "bw3sley"
slug: "know-when-a-component-rerenders"
tags:
  - react
  - rendering
  - components
created_at: "2022-06-24"

---

# Entender por que um componente renderiza de novo

Um componente renderiza de novo quando seu estado muda, quando recebe novas props ou quando um contexto usado por ele muda.

Por padrão, quando um componente pai renderiza, React também renderiza os filhos recursivamente. Só com otimizações como `memo` esse filho pode pular render quando as props continuam iguais.

```tsx
function Parent() {
  const [count, setCount] = useState(0);

  return (
    <>
      <button onClick={() => setCount(count + 1)}>Incrementar</button>
      <Child title="Oi" />
    </>
  );
}

function Child({ title }: { title: string }) {
  console.log("renderizou");

  return <p>{title}</p>;
}
```

Ao atualizar `count`, `Parent` renderiza de novo. Como `Child` faz parte dessa árvore, ele também renderiza de novo, mesmo recebendo `title="Oi"` outra vez.
