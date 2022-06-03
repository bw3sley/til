# Entendo o cabeçalho X-Frame-Options

O cabeçalho `X-Frame-Options` protege contra ataques de **Clickjacking**, impedindo que um site seja carregado dentro de um `<iframe>` malicioso.

Esse cabeçalho define **se e como** uma página pode ser carregada dentro de um `iframe`.

```http
X-Frame-Options: DENY
```

### **Opções possíveis:**

- `DENY` → Impede que a página seja carregada dentro de qualquer `<iframe>`.
- `SAMEORIGIN` → Permite o carregamento do site dentro de `<iframe>` **apenas no mesmo domínio**.
- `ALLOW-FROM https://exemplo.com` → Permite carregar o site dentro de `<iframe>` apenas do domínio especificado.

### **Benefícios:**

- Protege contra Clickjacking, onde um usuário clica em algo sem perceber.  
- Impede que sua página seja carregada dentro de **iframes de terceiros**.  