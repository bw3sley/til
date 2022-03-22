# Como Fazer Commit no Passado

## Introdução

Neste artigo, você aprenderá como realizar um commit no passado utilizando a opção `--date` no Git. Esta técnica é útil quando você deseja alterar a data de um commit para uma data anterior, seja para corrigir um erro ou ajustar a cronologia do seu histórico de commits.

## O que é?

No Git, um commit é um ponto na história do seu código, que possue uma mensagem e guarda automaticamente a data e hora em que a alteração foi realizada. Porém podem existir casos em que você vai querer definir manualmente uma data.

## Como funciona?

Você pode usar a opção `--date` ao realizar um commit para especificar uma data e hora diferentes da atual. Isso é feito usando o comando:

```shell
git commit --date="1 year ago" -m "🎉: initial commit"
```

Neste exemplo, o commit que fizemos será registrado com uma data de um ano atrás em relação à data atual. Se você fizer o push deste commit para algum branch, a data do commit será, por exemplo, 12/07/2021, dependendo da data em que o comando foi realizado.

## Aplicações Práticas

Alterar a data de um commit pode ser útil em vários cenários, como:

- Corrigir a cronologia dos commits em um projeto quando os commits foram feitos fora de ordem.
- Simular um fluxo de trabalho histórico para demonstrações ou tutoriais.
- Ajustar a data de commits feitos offline para refletir a data real de trabalho.

## Conclusão

Assim, com esse artigo você consegui aprender a utilizar a opção `--date`, conseguindo assim manipular a data de um commit no Git, ajustando-a conforme necessário para suas necessidades de desenvolvimento.

## Recursos Adicionais

- [Documentação oficial do Git](https://git-scm.com/doc) 