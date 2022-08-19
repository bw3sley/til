---
title: "Validar formulário com `zodResolver` no React Hook Form"
author: "bw3sley"
slug: "validate-form-with-zod-resolver-in-react-hook-form"
tags:
  - react
  - react-hook-form
  - zod
  - forms
created_at: "2026-07-09"

---

# Validar formulário com `zodResolver` no React Hook Form

Depois de instalar `react-hook-form`, `zod` e `@hookform/resolvers`, o `zodResolver` conecta schema e `useForm` na mesma configuração. O tipo do formulário pode vir do próprio schema.

```tsx
const schema = z.object({
  name: z.string(),
  age: z.number(),
});

type FormData = z.infer<typeof schema>;

const { register, handleSubmit } = useForm<FormData>({
  resolver: zodResolver(schema),
});

<form onSubmit={handleSubmit(console.log)}>
  <input {...register("name")} />
  <input type="number" {...register("age", { valueAsNumber: true })} />
</form>
```
