# Entendendo como remover a versão do header `Server`

Para ocultar ou modificar esse cabeçalho no NGINX, você pode editar a configuração global do servidor.

Geralmente localizado em `/etc/nginx/nginx.conf`, adicione (ou descomente) a seguinte linha dentro do bloco `http`:

```nginx
http {
    server_tokens off;
    ...
}
```