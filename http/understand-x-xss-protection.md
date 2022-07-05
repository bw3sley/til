# Entendendo o header X-XSS-Protection

O cabeçalho `X-XSS-Protection` ativa o **filtro de proteção contra ataques XSS** nos navegadores.

Os navegadores modernos possuem um filtro embutido para prevenir ataques **Cross-Site Scripting (XSS)**. Esse cabeçalho instrui o navegador a ativá-lo.

```http
X-XSS-Protection: 1; mode=block
```

### Parâmetros:

- `0` → Desativa a proteção contra XSS.
- `1` → Ativa a proteção contra XSS.
- `1; mode=block` → Ativa a proteção e **bloqueia** a página se um ataque for detectado.

### Benefícios:

- Evita ataques de **injeção de scripts** em páginas vulneráveis.  
- Melhora a segurança para usuários em navegadores antigos.  