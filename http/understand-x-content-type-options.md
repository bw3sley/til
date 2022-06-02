# Entendendo o header X-Content-Type-Options

O cabeçalho `X-Content-Type-Options` impede que o navegador tente **adivinhar o tipo de conteúdo de um arquivo**, evitando ataques como **MIME Sniffing**.

Ao definir esse cabeçalho, garantimos que o navegador respeite estritamente o **Content-Type** enviado pelo servidor.

```http
X-Content-Type-Options: nosniff
```

### **O que ele faz?**

- Impede que navegadores **modifiquem o tipo de mídia** com base no conteúdo.
- Evita que arquivos maliciosos sejam interpretados erroneamente como **código executável**.

### **Benefícios:**

- Protege contra ataques XSS baseados em MIME Sniffing.  
- Evita execução indevida de scripts disfarçados de outro tipo de arquivo.  