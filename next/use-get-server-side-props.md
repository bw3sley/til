# Usando `getServerSideProps` no Next.js

No Next.js, `getServerSideProps` é uma função usada para renderizar páginas no lado do servidor em tempo de requisição. Isso significa que os dados são obtidos e a página é gerada a cada requisição, tornando-a ideal para conteúdo que precisa ser atualizado em tempo real.

### Exemplo de Uso

Abaixo, um exemplo de como usar `getServerSideProps` para buscar dados de uma API externa a cada requisição:

```javascript
export async function getServerSideProps() {
  const res = await fetch('https://api.example.com/data');
  const data = await res.json();

  return {
    props: {
      data,
    },
  };
}

export default function HomePage({ data }) {
  return (
    <div>
      <h1>Dados Atualizados em Tempo Real</h1>
      <pre>{JSON.stringify(data, null, 2)}</pre>
    </div>
  );
}
```

### Explicação

- `getServerSideProps`: Executa no lado do servidor a cada requisição, garantindo que os dados estejam sempre atualizados.
- `props`: O objeto retornado dentro de `props` será passado para o componente como propriedades, permitindo que ele receba os dados atualizados em tempo real.

### Quando Usar `getServerSideProps`?

Use `getServerSideProps` quando:

- Os dados mudam frequentemente e precisam ser atualizados a cada requisição.
- A página depende de dados específicos do usuário ou informações que variam por sessão.
- SEO é importante, e você quer renderizar o conteúdo atualizado no lado do servidor para melhorar a indexação.

## Referências

Para mais detalhes, consulte a [documentação oficial do Next.js sobre `getServerSideProps`](https://nextjs.org/docs/basic-features/data-fetching/get-server-side-props).