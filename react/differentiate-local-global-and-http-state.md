---
title: "Diferenciar estado local, global e HTTP no React"
author: "bw3sley"
slug: "differentiate-local-global-and-http-state"
tags:
  - react
  - state
created_at: "2022-06-22"

---

# Diferenciar estado local, global e HTTP no React

Estado local vive dentro de um componente, normalmente com `useState`, e serve para controlar comportamento isolado da própria UI.

Exemplo de estado local:

```tsx
const [open, setOpen] = useState(false);
```

Estado global fica fora dos componentes e centraliza dados compartilhados pela aplicação, usando soluções como Zustand, Redux ou Jotai.

Exemplo de estado global:

```tsx
const user = useUserStore((state) => state.user);
```

Estado HTTP representa dados vindos de requisições, como listas, detalhes e status de carregamento retornados pela API.

Exemplo de estado HTTP:

```tsx
const { data, isLoading } = useQuery({
  queryKey: ["posts"],
  queryFn: fetchPosts,
});
```
