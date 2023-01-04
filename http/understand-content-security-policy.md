# Entendendo o header `Content-Security-Policy` (CSP)

O cabeçalho `Content-Security-Policy` (CSP) é uma poderosa camada de segurança que ajuda a **prevenir ataques XSS (Cross-Site Scripting)** e outros tipos de injeção de conteúdo malicioso. Ele permite definir **quais fontes de conteúdo são confiáveis** para a aplicação.

Você define uma política declarando quais recursos podem ser carregados (scripts, imagens, fontes, estilos, etc.) e de quais origens. Qualquer recurso que não esteja autorizado na política será **bloqueado pelo navegador**.

```http
Content-Security-Policy: default-src 'self'; img-src 'self' https://cdn.exemplo.com; script-src 'self' https://apis.google.com
```

### Diretivas comuns

- `default-src` → Origem padrão para todos os recursos que não foram explicitamente listados.
- `script-src` → Define as fontes permitidas para scripts JavaScript.
- `style-src` → Define as fontes permitidas para folhas de estilo CSS.
- `img-src` → Define as fontes permitidas para imagens.
- `connect-src` → Controla as conexões de rede, como chamadas fetch, XHR, WebSocket, etc.
- `frame-src` → Define de onde conteúdos como `<iframe>` podem ser carregados.

### Valores úteis

- `'self'` → Permite recursos do mesmo domínio.
- `'none'` → Não permite nenhum recurso.
- `'unsafe-inline'` → Permite código inline (não recomendado por questões de segurança).
- `'unsafe-eval'` → Permite uso de `eval()` e similares.

## Benefícios

- Previne a execução de scripts maliciosos injetados na aplicação.
- Reduz a superfície de ataque contra XSS.
- Fornece controle granular sobre recursos externos utilizados.

## Cuidados

- É necessário testar bem a política para evitar que recursos legítimos da aplicação sejam bloqueados.
- Adotar o modo de relatório (`Content-Security-Policy-Report-Only`) é uma boa prática para avaliar os impactos antes de aplicar em produção.