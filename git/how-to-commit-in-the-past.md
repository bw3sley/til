# Como fazer commit no passado

Às vezes, você pode precisar alterar a data de um commit no Git, seja para corrigir um erro ou ajustar a cronologia dos commits. Com o Git, você pode usar a opção `--date` para fazer isso.

Para realizar um commit no passado, use o comando:

```shell
git commit --date="1 year ago" -m "🎉: initial commit"
```

Esse comando cria um commit com a data de um ano atrás em relação à data atual. A data exata do commit dependerá da data em que você executar o comando.

### Exemplo Prático

Se você fizer um commit com `--date="2 days ago"`, ele será registrado como se tivesse sido feito dois dias antes da data atual:

```shell
git commit --date="2 days ago" -m "Corrigindo bug"
```

Este comando ajusta a data do commit para refletir dois dias no passado, útil para manter um histórico de commits mais organizado.

## Referências

- [Questão do StackOverflow sobre commits no passado](https://stackoverflow.com/questions/3895453/how-do-i-make-a-git-commit-in-the-past)