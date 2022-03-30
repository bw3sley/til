# Prevenir Motores de Busca de Indexar uma Página

O arquivo `robots.txt` é comumente usado para informar aos rastreadores (bem-comportados), como motores de busca, para não visitar uma página. No entanto, se outra página tiver um link para sua página, ela ainda poderá ser indexada. Para instruir os motores de busca a não indexarem uma determinada página, é necessário usar meta tags de robots.

> Se você deseja bloquear uma página de aparecer nos resultados de pesquisa de forma confiável, é necessário usar uma meta tag `noindex` de robots. Isso significa que, para encontrar a tag `noindex`, o motor de busca precisa conseguir acessar essa página, então não a bloqueie com `robots.txt`.
> [fonte](https://yoast.com/ultimate-guide-robots-txt/)

Para prevenir a indexação, adicione a seguinte meta tag à seção `<head>` de qualquer página relevante.

```html
<meta name="robots" content="noindex">
```

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
- [Developers Google](https://developers.google.com/search/docs/advanced/crawling/block-indexing)