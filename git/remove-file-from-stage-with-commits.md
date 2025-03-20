# Removendo um arquivo do stage com commits

Caso tenha adicionado um arquivo ao stage com `git add`, mas ainda não fez o commit e deseja removê-lo sem deletá-lo do diretório de trabalho, use o comando `git restore --staged`. 

Para remover um arquivo do stage sem apagá-lo, executamos:  

```shell
git restore --staged nome-do-arquivo
```

Isso retorna o arquivo ao estado antes do `git add`, deixando-o como uma alteração não registrada.  

Se quiser remover todos os arquivos do stage, usamos:  

```shell
git restore --staged .
```

Isso desfaz a adição de todos os arquivos ao stage, sem afetar as mudanças no working directory. 