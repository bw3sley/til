# Usando Wildcards (`*` e `?`)

Os coringas permitem selecionar arquivos de maneira flexível.

Mover todos os arquivos que começam com log para outra pasta:

```bash
mv log* backups/
```

Selecionar arquivos com apenas um caractere variável:

```bash
ls file?.txt
```

Isso listaria `file1.txt`, `file2.txt`, mas não `file10.txt`.