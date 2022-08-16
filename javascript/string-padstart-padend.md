# String.prototype.padStart() | padEnd()
The `padStart()` and the `padEnd()` methods pad the string until the resulting string matches the given length.

Eg: 
```js
    "abc".padStart(10);         // "       abc"
    'abc'.padStart(10, "foo");  // "foofoofabc" 

    'abc'.padEnd(10);          // "abc       "
    'abc'.padEnd(10, "foo");   // "abcfoofoof"
```

See more details at [MDN Docs - padStart](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/padStart) and [MDN Docs - padEnd](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/padEnd)