---
title: "Comparar formulário controlled com `useState` e uncontrolled com React Hook Form"
author: "bw3sley"
slug: "compare-controlled-form-with-usestate-and-uncontrolled-form-with-react-hook-form"
tags:
  - react
  - forms
  - react-hook-form
  - zod
created_at: "2026-07-09"

---

# Comparar formulário controlled com `useState` e uncontrolled com React Hook Form

No formulário controlled, a gente mantém os dados dos campos em tempo real no estado da aplicação. No uncontrolled, o valor costuma ser buscado quando algum evento acontece, como o submit do formulário; com `react-hook-form`, isso pode ser feito junto da validação com `zod`.

```tsx
// controlled
const [name, setName] = useState("");
const [email, setEmail] = useState("");

<form>
  <input value={name} onChange={(e) => setName(e.target.value)} />
  <input value={email} onChange={(e) => setEmail(e.target.value)} />
</form>

// uncontrolled com react-hook-form + zod
const schema = z.object({
  name: z.string(),
  email: z.string().email(),
});

type FormData = z.infer<typeof schema>;

const { register, handleSubmit } = useForm<FormData>({
  resolver: zodResolver(schema),
});

<form onSubmit={handleSubmit(console.log)}>
  <input {...register("name")} />
  <input {...register("email")} />
</form>
```
