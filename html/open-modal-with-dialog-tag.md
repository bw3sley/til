---
title: "Usar `<dialog>` para abrir uma caixa modal nativa"
author: "bw3sley"
slug: "open-modal-with-dialog-tag"
tags:
  - html
  - dialog
  - ui
created_at: "2022-03-28"

---

# Usar `<dialog>` para abrir uma caixa modal nativa

`<dialog>` cria uma caixa de diálogo nativa no HTML. Para abrir como modal, use `showModal()`.

```html
<dialog id="modal">
  <p>Este é um diálogo.</p>
</dialog>

<script>
  document.getElementById("modal").showModal();
</script>
```

// Abre uma caixa modal com o texto "Este é um diálogo".
