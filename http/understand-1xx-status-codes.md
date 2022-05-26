# Entendendo códigos HTTP 1xx (100 - 199)

Os códigos na faixa de **100 a 199** indicam respostas informativas, ou seja, que a requisição está em andamento.

### 100 Continue

O servidor recebeu os cabeçalhos da requisição e o cliente pode continuar enviando o corpo da requisição.

### 101 Switching Protocols

O servidor aceita mudar o protocolo conforme solicitado pelo cliente, como de HTTP para WebSocket.

### 103 Early Hints

Permite que o navegador comece a pré-carregar recursos enquanto o servidor prepara a resposta.
