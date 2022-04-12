# Obter um Arquivo de Outro Branch

Se você precisa pegar um arquivo específico de outro branch no Git sem fazer o checkout completo daquele branch, pode fazer isso com o comando `git checkout` seguido do nome do branch e do caminho do arquivo.

Aqui está como fazer isso:

```bash
git checkout nome-do-branch -- caminho/para/o/arquivo
```

Por exemplo, para pegar o arquivo `config.yml` do branch `feature-branch`:

```bash
git checkout feature-branch -- config.yml
```

Este comando traz a versão do arquivo `config.yml` do branch `feature-branch` para o branch atual. O arquivo será atualizado no branch em que você está sem a necessidade de trocar completamente para o outro branch.

### Dicas

- **Confirme as mudanças:** Após pegar o arquivo, você pode querer verificar as alterações usando `git status` e `git diff`.
- **Commit:** Se tudo estiver correto, você pode commitar a nova versão do arquivo no branch atual.

Esse método é útil para pegar arquivos específicos sem ter que mudar de contexto.

## Referências

- [💡 thoughtbot/til](https://github.com/thoughtbot/til/blob/main/git/grab-a-file-from-another-branch.md)