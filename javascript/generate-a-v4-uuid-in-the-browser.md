# Gerar um UUID V4 no Navegador

A [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API) fornece a função [`randomUUID`](https://developer.mozilla.org/en-US/docs/Web/API/Crypto/randomUUID) para gerar valores UUID v4 que são criptograficamente aleatórios.

Funciona assim:

```javascript
> crypto.randomUUID()
'f2050c5e-af52-4ca2-b4d6-23758b3396c9'
> crypto.randomUUID()
'079d5186-84d4-41d6-a660-edafb6a74c86'
```

Nenhum UUID será igual ao outro. Essa é uma excelente maneira de gerar IDs que são garantidamente únicos ou se você precisar de um valor que seja praticamente impossível de adivinhar.

Fiquei surpreso ao ver que, no momento da escrita, essa função tem um ótimo suporte nos navegadores. As versões modernas de todos os navegadores, exceto o Internet Explorer, já implementaram `randomUUID`.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)