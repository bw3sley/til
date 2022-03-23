# Como Fazer Commit no Passado

## Introdução

Neste artigo, você aprenderá como realizar um commit no passado utilizando a opção `--date` no Git. Esta técnica é útil quando você deseja alterar a data de um commit para uma data anterior, seja para corrigir um erro ou ajustar a cronologia do seu histórico de commits.

## Como funciona?

Você pode usar a opção `--date` ao realizar um commit para especificar uma data e hora diferentes da atual. Isso é feito usando o comando:

```shell
git commit --date="1 year ago" -m "🎉: initial commit"
```

Neste exemplo, o commit que fizemos será registrado com uma data de um ano atrás em relação à data atual. Se você fizer o push deste commit para algum branch, a data do commit será, por exemplo, 12/07/2021, dependendo da data em que o comando foi realizado.

## Conclusão

Assim, com esse artigo você consegui aprender a utilizar a opção `--date`, conseguindo assim manipular a data de um commit no Git, ajustando-a conforme necessário para suas necessidades de desenvolvimento.

## Recursos Adicionais

- [Questão do StackOverflow](https://stackoverflow.com/questions/3895453/how-do-i-make-a-git-commit-in-the-past) 