# Mensagens de Status HTTP

## Introdução

Neste artigo, você aprenderá mais sobre os status HTTP, que são códigos numéricos retornados por servidores web para indicar o resultado de uma requisição HTTP. Cada código possui um significado específico que informa ao cliente (como um navegador ou aplicativo) sobre o sucesso ou a falha da requisição. Por exemplo, quando um navegador solicita um serviço de um servidor, pode ocorrer um erro, e o servidor pode retornar um código de status HTTP, como "404 Not Found". Além dos erros, existem códigos de status para indicar sucesso, redirecionamento, erros do cliente e erros do servidor.

## Como funciona?

Quando um cliente faz uma requisição a um servidor, o servidor responde com um código de status HTTP, que indica o resultado da requisição. Vamos explorar alguns dos códigos de status mais comuns e entender como eles funcionam:

### 100 - Código de Informação

| Código | Mensagem              | Descrição                                                                                  |
| :----: | :-------------------: | :----------------------------------------------------------------------------------------: |
|  100   | Continue              | O servidor recebeu os cabeçalhos da requisição, e o cliente deve prosseguir para enviar o corpo da requisição. |
|  101   | Switching Protocols   | O solicitante pediu ao servidor para trocar de protocolos.                                  |
|  103   | Early Hints           | Usado com o cabeçalho Link para permitir que o navegador comece a pré-carregar recursos enquanto o servidor prepara uma resposta. |

### 200 - Código de Sucesso

| Código | Mensagem                    | Descrição                                                                                     |
| :----: | :-------------------------: | :-------------------------------------------------------------------------------------------: |
|  200   | OK                          | A requisição foi bem-sucedida (esta é a resposta padrão para requisições HTTP bem-sucedidas).  |
|  201   | Created                     | A requisição foi bem-sucedida e um novo recurso foi criado.                                    |
|  202   | Accepted                    | A requisição foi aceita para processamento, mas o processamento não foi concluído.             |
|  203   | Non-Authoritative Information | A requisição foi processada com sucesso, mas está retornando informações que podem ser de outra fonte. |
|  204   | No Content                  | A requisição foi processada com sucesso, mas não está retornando nenhum conteúdo.              |
|  205   | Reset Content               | A requisição foi processada com sucesso, mas não está retornando nenhum conteúdo e requer que o solicitante redefina a visualização do documento. |
|  206   | Partial Content             | O servidor está entregando apenas parte do recurso devido a um cabeçalho de intervalo enviado pelo cliente. |

### Exemplos

Aqui está um exemplo de como você pode usar o comando `curl` para simular uma requisição HTTP e ver o código de status retornado:

```bash
# Fazendo uma requisição HTTP GET e visualizando o código de status
curl -I https://www.example.com

# Resultado esperado:
# HTTP/1.1 200 OK
```

## Conclusão

Os códigos de status HTTP são fundamentais para a comunicação entre clientes e servidores na web. Eles fornecem informações importantes sobre o sucesso ou falha de uma requisição, ajudando desenvolvedores e administradores a diagnosticar problemas e entender o comportamento das aplicações web. Compreender esses códigos é essencial para desenvolver, manter e melhorar sistemas web robustos e confiáveis.

## Recursos Adicionais

- [Documentação do MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)