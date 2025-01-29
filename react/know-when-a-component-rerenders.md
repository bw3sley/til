---
title: "Entender quando um componente renderiza novamente"
author: "bw3sley"
slug: "know-when-a-component-rerenders"
tags:
  - react
  - rendering
  - components
created_at: "2022-06-24"

---

# Entender quando um componente renderiza novamente

Um componente renderiza de novo quando seu estado muda, quando alguma prop muda ou quando o componente pai renderiza novamente.

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

Ao atualizar `count`, `Parent` renderiza de novo e `Child` também.
