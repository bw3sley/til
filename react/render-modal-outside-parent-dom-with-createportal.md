---
title: "Renderizar modal fora do DOM pai com `createPortal`"
author: "bw3sley"
slug: "render-modal-outside-parent-dom-with-createportal"
tags:
  - react
  - portal
  - dom
created_at: "2026-07-09"

---

# Renderizar modal fora do DOM pai com `createPortal`

`createPortal` renderiza um filho em outro nó do DOM, mesmo que ele continue fazendo parte da mesma árvore React. Isso costuma ser usado em modal, dialog e tooltip.

```tsx
import { createPortal } from "react-dom";

function Dialog({ open }: { open: boolean }) {
  if (!open) return null;

  return createPortal(
    <div role="dialog">Conteúdo do modal</div>,
    document.body,
  );
}
```
