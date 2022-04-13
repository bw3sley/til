# Exportar um Banco de Dados para um Arquivo

O cliente `mysqldump` é uma ferramenta prática para criar um backup ou snapshot de um banco de dados MySQL. O uso padrão deste comando gera uma série de instruções em ordem alfabética que compõem a estrutura e os dados do banco de dados especificado. Ele direciona todo esse conteúdo para o `stdout`. Você provavelmente vai querer redirecioná-lo para um arquivo.

```bash
$ mysqldump my_database > my_database_backup.sql
```

A saída incluirá comentários especiais com diretivas MySQL que desabilitam coisas como a verificação de restrições. Isso permite que a saída esteja em ordem alfabética sem necessariamente violar quaisquer restrições de chave estrangeira.

Se você precisar exportar vários bancos de dados, inclua a opção `--databases` com uma lista de nomes de banco de dados separados por espaço. Ou exporte todos eles com `--all-databases`.

Consulte `man mysqldump` para mais detalhes.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)