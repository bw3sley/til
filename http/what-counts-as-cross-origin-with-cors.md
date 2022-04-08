# O que vale como Cross-Origin With CORS?

Quando se trata de HTTP, uma [origem](https://developer.mozilla.org/en-US/docs/Glossary/origin) é definida por vários aspectos diferentes da URL. Isso é importante para entender o que qualifica como _mesma_ origem (same-origin) ou _origem cruzada_ (cross-origin) ao lidar com [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) (Compartilhamento de Recursos de Origem Cruzada).

Para algo ser considerado de _mesma origem_, ele deve ter o mesmo _scheme_ (HTTP/HTTPS), o mesmo host e a mesma porta. Se qualquer um desses elementos — _scheme_, host (incluindo subdomínios) ou porta — for diferente, então não é de _mesma origem_.

Aqui estão alguns exemplos de origens diferentes:

- `https://example.com` vs `http://example.com` (esquema diferente)
- `https://example.com` vs `https://sub.example.com` (host diferente)
- `https://example.com:3000` vs `https://example.com:5000` (porta diferente)

Enquanto o _scheme_, o host e a porta corresponderem, eles são considerados de mesma origem. O caminho (tudo o que segue a origem) não influencia na questão da mesma origem.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)