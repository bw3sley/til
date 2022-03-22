# Mensagens de Status HTTP

## Introdução

Quando um navegador solicita um serviço de um servidor web, pode ocorrer um erro, e o servidor pode retornar um código de erro, como "404 Not Found". Comumente, esses erros são chamados de mensagens de erro HTML. No entanto, essas mensagens são, na verdade, chamadas de mensagens de status HTTP. Na verdade, o servidor sempre retorna uma mensagem para cada requisição, sendo a mensagem mais comum "200 OK".

## 100 - Código de Informação

| Código | Mensagem              | Descrição                                                                                  |
| :----: | :-------------------: | :----------------------------------------------------------------------------------------: |
|  100   | Continue              | O servidor recebeu os cabeçalhos da requisição, e o cliente deve prosseguir para enviar o corpo da requisição. |
|  101   | Switching Protocols   | O solicitante pediu ao servidor para trocar de protocolos.                                  |
|  103   | Early Hints           | Usado com o cabeçalho Link para permitir que o navegador comece a pré-carregar recursos enquanto o servidor prepara uma resposta. |

## 200 - Código de Sucesso

| Código | Mensagem                    | Descrição                                                                                     |
| :----: | :-------------------------: | :-------------------------------------------------------------------------------------------: |
|  200   | OK                          | A requisição foi bem-sucedida (esta é a resposta padrão para requisições HTTP bem-sucedidas).  |
|  201   | Created                     | A requisição foi bem-sucedida e um novo recurso foi criado.                                    |
|  202   | Accepted                    | A requisição foi aceita para processamento, mas o processamento não foi concluído.             |
|  203   | Non-Authoritative Information | A requisição foi processada com sucesso, mas está retornando informações que podem ser de outra fonte. |
|  204   | No Content                  | A requisição foi processada com sucesso, mas não está retornando nenhum conteúdo.              |
|  205   | Reset Content               | A requisição foi processada com sucesso, mas não está retornando nenhum conteúdo e requer que o solicitante redefina a visualização do documento. |
|  206   | Partial Content             | O servidor está entregando apenas parte do recurso devido a um cabeçalho de intervalo enviado pelo cliente. |

## 300 - Código de Redirecionamento

| Código | Mensagem              | Descrição                                                                                   |
| :----: | :-------------------: | :-----------------------------------------------------------------------------------------: |
|  300   | Multiple Choices      | Uma lista de links. O usuário pode selecionar um link e ir para aquele local. Máximo de cinco endereços. |
|  301   | Moved Permanently     | A página solicitada foi movida para uma nova URL permanentemente.                           |
|  302   | Found                 | A página solicitada foi movida temporariamente para uma nova URL.                           |
|  303   | See Other             | A página solicitada pode ser encontrada em uma URL diferente.                               |
|  304   | Not Modified          | Indica que a página solicitada não foi modificada desde a última solicitação.               |
|  307   | Temporary Redirect    | A página solicitada foi movida temporariamente para uma nova URL.                           |
|  308   | Permanent Redirect    | A página solicitada foi movida permanentemente para uma nova URL.                           |

## 400 - Código de Erro do Cliente

| Código | Mensagem                    | Descrição                                                                                   |
| :----: | :-------------------------: | :-----------------------------------------------------------------------------------------: |
|  400   | Bad Request                 | A requisição não pode ser atendida devido à sintaxe incorreta.                              |
|  401   | Unauthorized                | A requisição foi legal, mas o servidor se recusa a respondê-la. Usado quando a autenticação é possível, mas falhou ou ainda não foi fornecida. |
|  402   | Payment Required            | Reservado para uso futuro.                                                                  |
|  403   | Forbidden                   | A requisição foi legal, mas o servidor se recusa a respondê-la.                             |
|  404   | Not Found                   | A página solicitada não pôde ser encontrada, mas pode estar disponível novamente no futuro.  |
|  405   | Method Not Allowed          | Uma requisição foi feita a uma página usando um método de requisição não suportado por essa página. |
|  406   | Not Acceptable              | O servidor só pode gerar uma resposta que não é aceita pelo cliente.                        |
|  407   | Proxy Authentication Required | O cliente deve primeiro se autenticar com o proxy.                                           |
|  408   | Request Timeout             | O servidor esgotou o tempo limite de espera pela requisição.                                 |
|  409   | Conflict                    | A requisição não pôde ser concluída devido a um conflito na requisição.                      |
|  410   | Gone                        | A página solicitada não está mais disponível.                                               |
|  411   | Length Required             | O "Content-Length" não está definido. O servidor não aceitará a requisição sem ele.         |
|  412   | Precondition Failed         | A pré-condição dada na requisição foi avaliada como falsa pelo servidor.                    |
|  413   | Request Too Large           | O servidor não aceitará a requisição, porque a entidade da requisição é muito grande.        |
|  414   | Request-URI Too Long        | O servidor não aceitará a requisição, porque o URI é muito longo. Ocorre quando você converte uma requisição POST para uma requisição GET com uma longa informação de consulta. |
|  415   | Unsupported Media Type      | O servidor não aceitará a requisição, porque o tipo de mídia não é suportado.                |
|  416   | Range Not Satisfiable       | O cliente solicitou uma parte do arquivo, mas o servidor não pode fornecer essa parte.       |
|  417   | Expectation Failed          | O servidor não pode atender aos requisitos do campo do cabeçalho de requisição Expect.       |

## 500 - Código de Erro do Servidor

| Código | Mensagem                    | Descrição                                                                                   |
| :----: | :-------------------------: | :-----------------------------------------------------------------------------------------: |
|  500   | Internal Server Error       | Uma mensagem de erro genérica, fornecida quando nenhuma mensagem mais específica é adequada. |
|  501   | Not Implemented             | O servidor não reconhece o método de requisição ou não possui a capacidade de atender à requisição. |
|  502   | Bad Gateway                 | O servidor estava atuando como um gateway ou proxy e recebeu uma resposta inválida do servidor upstream. |
|  503   | Service Unavailable         | O servidor está temporariamente indisponível (sobrecarregado ou fora do ar).                 |
|  504   | Gateway Timeout             | O servidor estava atuando como um gateway ou proxy e não recebeu uma resposta a tempo do servidor upstream. |
|  505   | HTTP Version Not Supported  | O servidor não suporta a versão do protocolo HTTP usada na requisição.                       |
|  511   | Network Authentication Required | O cliente precisa se autenticar para obter acesso à rede.                                    |
