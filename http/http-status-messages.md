# Mensagens de Status HTTP

Os status HTTP são códigos numéricos retornados pelos servidores web para indicar o resultado de uma requisição. Cada código tem um significado específico que informa ao cliente (como um navegador ou aplicativo) se a requisição foi bem-sucedida, redirecionada ou se houve um erro.

### Códigos de Informação (100-199)

- **100 Continue**: O servidor recebeu os cabeçalhos da requisição e o cliente deve continuar a enviar o corpo da requisição.
- **101 Switching Protocols**: O servidor aceita mudar o protocolo conforme solicitado pelo cliente.
- **103 Early Hints**: Permite que o navegador comece a pré-carregar recursos enquanto o servidor prepara a resposta.

### Códigos de Sucesso (200-299)

- **200 OK**: A requisição foi bem-sucedida (resposta padrão).
- **201 Created**: A requisição foi bem-sucedida e um novo recurso foi criado.
- **202 Accepted**: A requisição foi recebida, mas o processamento não foi concluído.
- **203 Non-Authoritative Information**: A requisição foi bem-sucedida, mas a resposta contém dados de uma fonte diferente.
- **204 No Content**: A requisição foi bem-sucedida, mas não há conteúdo para retornar.
- **205 Reset Content**: A requisição foi bem-sucedida, mas o cliente deve redefinir a visualização do documento.
- **206 Partial Content**: O servidor está enviando apenas parte do recurso, conforme solicitado pelo cliente.

### Códigos de Redirecionamento (300-399)

- **300 Multiple Choices**: Há várias opções para o recurso solicitado, e o cliente pode escolher uma.
- **301 Moved Permanently**: O recurso solicitado foi movido permanentemente para uma nova URL.
- **302 Found**: O recurso foi temporariamente movido para uma URL diferente.
- **303 See Other**: O recurso deve ser acessado usando uma URL diferente.
- **304 Not Modified**: O recurso solicitado não foi modificado desde a última requisição.
- **307 Temporary Redirect**: O recurso foi temporariamente movido para uma nova URL, e o método da requisição não deve ser alterado.
- **308 Permanent Redirect**: O recurso foi movido permanentemente para uma nova URL, e o método da requisição não deve ser alterado.

### Códigos de Erro do Cliente (400-499)

- **400 Bad Request**: A requisição não pode ser processada devido à sintaxe incorreta.
- **401 Unauthorized**: A autenticação é necessária e falhou ou não foi fornecida.
- **403 Forbidden**: O servidor entendeu a requisição, mas se recusa a autorizá-la.
- **404 Not Found**: O recurso solicitado não foi encontrado.
- **405 Method Not Allowed**: O método da requisição não é suportado pelo recurso solicitado.
- **406 Not Acceptable**: O recurso solicitado só pode gerar conteúdo não aceitável pelo cliente.
- **407 Proxy Authentication Required**: O cliente deve se autenticar com um proxy.
- **408 Request Timeout**: O servidor não recebeu uma requisição completa a tempo.
- **409 Conflict**: A requisição não pode ser processada devido a um conflito com o estado atual do recurso.
- **410 Gone**: O recurso solicitado foi removido permanentemente e não está mais disponível.
- **411 Length Required**: O servidor rejeita a requisição porque o campo de comprimento do conteúdo não foi definido.
- **412 Precondition Failed**: A pré-condição enviada na requisição foi avaliada como falsa pelo servidor.
- **413 Payload Too Large**: A entidade da requisição é maior do que o servidor está disposto ou é capaz de processar.
- **414 URI Too Long**: O URI da requisição é muito longo para o servidor processar.
- **415 Unsupported Media Type**: O formato da mídia da requisição não é suportado pelo servidor.
- **416 Range Not Satisfiable**: O intervalo especificado na requisição não pode ser atendido.
- **417 Expectation Failed**: O servidor não pode atender aos requisitos do campo de cabeçalho Expect da requisição.

### Códigos de Erro do Servidor (500-599)

- **500 Internal Server Error**: O servidor encontrou uma situação inesperada que o impediu de atender à requisição.
- **501 Not Implemented**: O servidor não possui a funcionalidade necessária para atender à requisição.
- **502 Bad Gateway**: O servidor estava agindo como um gateway ou proxy e recebeu uma resposta inválida do servidor upstream.
- **503 Service Unavailable**: O servidor está atualmente indisponível (devido a sobrecarga ou manutenção).
- **504 Gateway Timeout**: O servidor estava agindo como um gateway ou proxy e não recebeu uma resposta a tempo do servidor upstream.
- **505 HTTP Version Not Supported**: O servidor não suporta a versão do protocolo HTTP usada na requisição.
- **511 Network Authentication Required**: O cliente precisa se autenticar para obter acesso à rede.

### Exemplo de Uso

Para verificar o código de status de uma resposta HTTP, você pode usar `curl`:

```bash
curl -I https://www.example.com
# Resultado esperado: HTTP/1.1 200 OK
```

## Referências

- [Documentação do MDN sobre Códigos de Status HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)