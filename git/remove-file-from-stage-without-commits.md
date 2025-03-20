# Removendo um arquivo do stage sem commits

Se o repositório ainda não tem commits, o comando `git restore --staged` pode falhar com a mensagem:  

```shell
fatal: could not resolve HEAD
```  

Isso acontece porque `HEAD` ainda não existe. Nesse caso, use `git rm --cached`:  

```shell
git rm --cached nome-do-arquivo
```  

Para remover todos os arquivos do stage:  

```shell
git rm --cached -r .
``` 