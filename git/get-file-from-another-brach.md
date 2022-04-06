# Pegar um arquivo de outra branch

Para pegar um arquivo específico de outro branch no Git sem fazer o checkout completo daquele branch, podemos fazer isso com o comando `git checkout` seguido do nome do branch e do caminho do arquivo.


```bash
git checkout nome-do-branch -- caminho/para/o/arquivo
```

Por exemplo, para pegar o arquivo `config.yml` do branch `feature-branch`:

```bash
git checkout feature-branch -- config.yml
```

Este comando traz a versão do arquivo `config.yml` do branch `feature-branch` para o branch atual. O arquivo será atualizado no branch em que você está sem a necessidade de trocar completamente para o outro branch.