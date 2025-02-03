---
title: "Redirecionar HTTP para HTTPS com `return 301`"
author: "bw3sley"
slug: "redirect-http-to-https-with-return-301"
tags:
  - nginx
  - redirects
  - https
created_at: "2024-11-28"

---

# Redirecionar HTTP para HTTPS com `return 301`

No NGINX, um bloco escutando na porta `80` pode responder com `301` para forçar acesso pela versão HTTPS da URL.

```nginx
server {
    listen 80;
    server_name example.com www.example.com;
    return 301 https://$host$request_uri;
}
```
