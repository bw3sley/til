---
title: "Usar props para passar dados para um componente"
author: "bw3sley"
slug: "use-props-to-pass-data-into-components"
tags:
  - react
  - props
created_at: "2022-07-01"

---

# Usar props para passar dados para um componente

Props são os valores recebidos nos parâmetros do componente. Elas permitem configurar comportamento e conteúdo sem acoplar tudo dentro do mesmo bloco.

```tsx
function Button({ title }: { title: string }) {
  return <button>{title}</button>;
}

<Button title="Curtir" />
```

A prop `title` muda o conteúdo sem mudar o componente.
