# ATOB
The `atob()` function decodes a string of data which has been encoded using Base64 encoding. You can use the btoa() method to encode and transmit data which may otherwise cause communication problems, then transmit it and use the atob() method to decode the data again. For example, you can encode, transmit, and decode control characters such as ASCII values 0 through 31.

Eg: 

```js
    const decodedData = atob(encodedData); // decode the string
```