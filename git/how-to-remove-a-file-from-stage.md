# Como remover um arquivo do stage no Git  

Se você adicionou um arquivo ao stage (área de preparação) com `git add`, mas ainda não fez o commit e deseja removê-lo sem deletá-lo do diretório de trabalho, use o comando `git restore --staged`.  

## Removendo um arquivo específico  

Para remover um arquivo do stage sem apagá-lo, execute:  

```shell
git restore --staged nome-do-arquivo
```  

Isso retorna o arquivo ao estado antes do `git add`, deixando-o como uma alteração não registrada.  

## Removendo todos os arquivos do stage  

Se quiser remover todos os arquivos do stage, use:  

```shell
git restore --staged .
```  

Isso desfaz a adição de todos os arquivos ao stage, sem afetar as mudanças no diretório de trabalho.  

### Caso especial: `fatal: could not resolve HEAD`  

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

Após isso, rode `git status` para confirmar que os arquivos foram removidos do stage.  

Se quiser evitar esse problema no futuro, faça um commit inicial vazio antes de começar a adicionar arquivos:  

```shell
git commit --allow-empty -m "Initial commit"
```  

Assim, `HEAD` será criado, e `git restore --staged` funcionará corretamente.  

## Referências  

- [Documentação oficial do Git sobre `restore`](https://git-scm.com/docs/git-restore)  
- [Documentação oficial do Git sobre `rm`](https://git-scm.com/docs/git-rm)