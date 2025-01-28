---
title: "Diferenciar pensamento declarativo e imperativo na UI"
author: "bw3sley"
slug: "compare-declarative-and-imperative-thinking-in-ui"
tags:
  - react
  - patterns
created_at: "2022-06-20"

---

# Diferenciar pensamento declarativo e imperativo na UI

Na abordagem declarativa, você descreve as condições para o resultado final. Na imperativa, você detalha o passo a passo do que precisa acontecer.

No React, o mais comum é declarar como a interface deve ficar para cada estado da aplicação.

Exemplo declarativo:

```tsx
return isLoading ? <p>Carregando...</p> : <PostsList posts={posts} />;
```

Exemplo imperativo:

```ts
if (isLoading) {
  screen.innerHTML = "<p>Carregando...</p>";
} else {
  renderPostsList(posts);
}
```
