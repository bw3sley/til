# Common errors
When executing JavaScript code, different errors can occur.

Errors can be coding errors made by the programmer, errors due to wrong input, and other unforeseeable things.

</br>

## Range Error
A **RangeError** is thrown if you use a number that is outside the range of legal values.

Eg:
```
    let number1 = 1;

    try {
        number1.toPrecision(500);   // A number cannot have 500 significant digits
    }

    catch(error) {
        document.getElementById("demo").innerHTML = error.name;
    }
```

## Reference Error
A **ReferenceError** is thrown if you use (reference) a variable that has not been declared.

Eg:
```
    let number1 = 5;
    
    try {
        number1x = number2 + 1;   // number2 cannot be used (referenced)
    }

    catch(error) {
        document.getElementById("demo").innerHTML = error.name;
    }
```

## Syntax Error
A **SyntaxError** is thrown if you try to evaluate code with a syntax error.

Eg:
```
    try {
        alert('Hello);   // Missing ' will produce an error
    }

    catch(error) {
        document.getElementById("demo").innerHTML = error.name;
    }
```

## Type Errors
A **TypeError** is thrown if you use a value that is outside the range of expected types.

Eg:
```
    let number1 = 1;

    try {
        number1.toUpperCase();   // You cannot convert a number to upper case
    }

    catch(error) {
        document.getElementById("demo").innerHTML = error.name;
    }
```