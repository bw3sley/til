# Usando `getStaticProps` no Next.js

No Next.js, `getStaticProps` é uma função usada para gerar páginas estáticas com dados dinâmicos em tempo de construção (build time). Isso é ideal para páginas que precisam de dados em tempo de execução, mas que não mudam frequentemente.

### Exemplo de Uso

Abaixo, um exemplo básico de como usar `getStaticProps` para obter dados de uma API externa e renderizar uma página estática:

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

export const getStaticProps: GetStaticProps<any, { id: string }> = async ({ params }) => {
    const productId = params!.id;

    const product = await stripe.products.retrieve(productId, {
        expand: ["default_price"]
    })

    const price = product.default_price as Stripe.Price;

    return {
        props: {
            data
        },

        revalidate: 60 * 60 * 1 // 1 hours
    }
}
```

### Explicação

- `getStaticProps`: Função que é executada no lado do servidor durante a construção, nunca no cliente.
- `props`: O objeto retornado dentro de `props` será passado para o componente como propriedades.
- `revalidate`: (opcional) Define um tempo em segundos para revalidar a página de forma incremental, permitindo a atualização dos dados após o build inicial.

### Quando Usar `getStaticProps`?

Use `getStaticProps` quando:

- A página é gerada estaticamente com dados dinâmicos, mas que não mudam com frequência.
- Você quer desempenho e SEO aprimorados por meio de renderização estática.
- Precisa de revalidação incremental para atualizar os dados periodicamente.

## Referências

Para mais detalhes, consulte a [documentação oficial do Next.js sobre `getStaticProps`](https://nextjs.org/docs/basic-features/data-fetching/get-static-props).