# Entendendo o header `Strict-Transport-Security` (HSTS)

O cabeçalho `Strict-Transport-Security` (HSTS) é um mecanismo de segurança que instrui os navegadores a **forçarem conexões seguras via HTTPS** e impedirem comunicações em HTTP.

Quando um navegador recebe esse cabeçalho, ele **memoriza a regra** e garante que todas as futuras conexões para o domínio sejam feitas via HTTPS, mesmo que o usuário tente acessar por HTTP.

```http
Strict-Transport-Security: max-age=31536000; includeSubDomains; preload
```

### Parâmetros

- `max-age=31536000` → Define o tempo (em segundos) que o navegador deve forçar HTTPS (1 ano neste caso).
- `includeSubDomains` → Aplica a regra também a subdomínios.
- `preload` → Solicita inclusão na lista de pré-carregamento de HSTS dos navegadores.

### Benefícios

- Previne ataques de downgrade de protocolo (man-in-the-middle).  
- Garante que todas as conexões ocorram de forma segura.  
- Reduz a chance de exposição a ataques HTTP inseguros.  