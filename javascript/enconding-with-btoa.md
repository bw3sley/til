# BOTA
The `btoa()` method creates a Base64-encoded ASCII string from a binary string (i.e., a string in which each character in the string is treated as a byte of binary data).

You can use this method to encode data which may otherwise cause communication problems, transmit it, then use the atob() method to decode the data again. For example, you can encode control characters such as ASCII values 0 through 31.

Eg:
```js
    const encodedData = btoa("Hello, world");
```