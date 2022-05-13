# Erros Comuns em JavaScript

Ao executar código JavaScript, diferentes tipos de erros podem ocorrer.

Os erros podem ser causados por falhas de codificação feitas pelo programador, entradas incorretas ou outras situações imprevisíveis.

</br>

## RangeError

Um **RangeError** é lançado quando um número está fora do intervalo de valores permitidos.

Exemplo:

```javascript
let numero = 1;

try {
    numero.toPrecision(500); // Um número não pode ter 500 dígitos significativos
} catch (erro) {
    document.getElementById("demo").innerHTML = erro.name;
}
```

## ReferenceError

Um **ReferenceError** é lançado quando você tenta usar (referenciar) uma variável que não foi declarada.

Exemplo:

```javascript
let numero = 5;

try {
    numeroX = numeroY + 1; // numeroY não foi declarado
} catch (erro) {
    document.getElementById("demo").innerHTML = erro.name;
}
```

## SyntaxError

Um **SyntaxError** é lançado quando o código contém um erro de sintaxe.

Exemplo:

```javascript
try {
    alert('Olá); // Falta de aspas fechará um erro
} catch (erro) {
    document.getElementById("demo").innerHTML = erro.name;
}
```

## TypeError

Um **TypeError** é lançado quando você usa um valor que está fora do tipo esperado.

Exemplo:

```javascript
let numero = 1;

try {
    numero.toUpperCase(); // Não é possível converter um número para maiúsculas
} catch (erro) {
    document.getElementById("demo").innerHTML = erro.name;
}
```