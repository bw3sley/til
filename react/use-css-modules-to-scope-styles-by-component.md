---
title: "Usar CSS Modules para limitar escopo de estilos"
author: "bw3sley"
slug: "use-css-modules-to-scope-styles-by-component"
tags:
  - react
  - css-modules
created_at: "2026-07-05"

---

# Usar CSS Modules para limitar escopo de estilos

CSS Modules aplicam estilos só ao componente importador, evitando colisão entre classes com o mesmo nome em arquivos diferentes.

```tsx
import styles from "./button.module.css";

export function Button() {
  return <button className={styles.container}>Curtir</button>;
}
```

```css
.container {
  background: #8257e6;
}
```

A classe `container` fica isolada neste componente.
