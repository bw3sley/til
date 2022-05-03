# Usando `getStaticPaths` no Next.js

No Next.js, `getStaticPaths` é uma função usada junto com `getStaticProps` para gerar páginas estáticas dinâmicas com base em rotas dinâmicas. Ele permite pré-renderizar páginas específicas no momento da construção, com caminhos definidos dinamicamente.

### Exemplo de Uso

Suponha que temos um blog com rotas dinâmicas para cada produto (`/products/[id]`). Podemos usar `getStaticPaths` para definir quais páginas de produtos serão geradas estaticamente no momento do build.

```tsx
export default function Product({ product }: ProductProps) {
    const { isFallback } = useRouter();

    if (isFallback) { 
      return <p>Loading...</p>;
    }

    const [isCreatingCheckoutSession, setIsCreatingCheckoutSession] = useState(false);

    async function handleBuyProduct() {
        try {
            setIsCreatingCheckoutSession(true);

            const response = await axios.post("/api/checkout", {
                priceId: product.defaultPriceId
            })

            const { checkoutUrl } = response.data;

            window.location.href = checkoutUrl;
        } 
        
        catch (error) {
            setIsCreatingCheckoutSession(false);

            alert("Falha ao redirecionar ao checkout!");   
        }
    }

    return (
        <>
            <Head>
                <title>{product.name} | Ignite Shop</title>
            </Head>

            <ProductContainer>
                <ImageContainer>
                    <Image src={product.imageUrl} width={520} height={480} alt="" />
                </ImageContainer>

                <ProductDetails>
                    <h1>{product.name}</h1>
                    <span>{product.price}</span>

                    <p>{product.description}</p>

                    <button type="button" disabled={isCreatingCheckoutSession} onClick={handleBuyProduct}>Comprar agora</button>
                </ProductDetails>
            </ProductContainer>
        </>
    )
}

export const getStaticPaths: GetStaticPaths = async () => {
    return {
        paths: [
            { params: { id: "prod_NBqy8M6sAaweNM" } }
        ],

        fallback: true
    }
}
```

### Explicação

- `getStaticPaths`: Retorna um objeto com os caminhos (`paths`) a serem pré-renderizados no momento do build.
- `paths`: Define quais IDs ou parâmetros serão usados para gerar páginas estáticas. Cada item em `paths` precisa conter um objeto `params` correspondente aos parâmetros da rota.
- `fallback`: Define o comportamento para rotas não especificadas em `paths`:
  - `false`: Retorna 404 para rotas não especificadas.
  - `true`: Permite gerar páginas sob demanda para rotas ausentes.
  - `"blocking"`: Faz o carregamento do conteúdo sem fallback visual.

### Quando Usar `getStaticPaths`?

Use `getStaticPaths` quando:

- Você possui rotas dinâmicas e deseja pré-renderizar algumas ou todas as páginas com antecedência.
- Precisa melhorar o desempenho e SEO ao pré-gerar conteúdo com rotas dinâmicas.

## Referências

Para mais detalhes, consulte a [documentação oficial do Next.js sobre `getStaticPaths`](https://nextjs.org/docs/basic-features/data-fetching/get-static-paths).