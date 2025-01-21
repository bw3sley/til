---
title: "Usar `<slot>` para receber conteúdo em Web Components"
author: "bw3sley"
slug: "use-slot-to-render-content-in-web-components"
tags:
  - html
  - web-components
  - slot
created_at: "2022-04-07"

---

# Usar `<slot>` para receber conteúdo em Web Components

`<slot>` define um ponto de inserção dentro de um Web Component para conteúdo vindo de fora do componente.

```html
<template id="my-component">
  <p><slot>Texto padrão</slot></p>
</template>
```

// Sem conteúdo externo, o componente renderiza "Texto padrão".
