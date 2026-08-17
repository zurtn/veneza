# Super Veneza — deploy na Vercel

Site estático, um arquivo só. Não tem build, não tem dependência, não precisa de Node.

## Opção 1 — arrastar e soltar (mais rápido)

1. Acesse https://vercel.com/new
2. Arraste esta pasta (`deploy/`) inteira para a área de upload.
3. Framework Preset: **Other**. Build Command: deixe vazio. Output Directory: deixe vazio.
4. Clique em **Deploy**.

Em ~20 segundos você recebe uma URL `*.vercel.app`.

## Opção 2 — pela CLI

```bash
npm i -g vercel
cd deploy
vercel --prod
```

## Opção 3 — via GitHub

1. Crie um repositório e suba o conteúdo desta pasta na raiz.
2. Na Vercel: **Add New → Project → Import** o repositório.
3. Framework Preset **Other**, sem build command.

## Domínio próprio

Depois do deploy: **Project → Settings → Domains → Add**. Aponte o DNS conforme a Vercel indicar
(`A` para `76.76.21.21` ou `CNAME` para `cname.vercel-dns.com`).

## Sobre as imagens

As fotos dos produtos, a logo e os ícones são carregados direto da biblioteca de mídia do
WordPress atual (`https://superveneza.com/wp-content/uploads/...`). Funciona imediatamente,
mas cria uma dependência do site antigo ficar no ar.

Antes de desligar o WordPress, baixe as imagens e troque as URLs por caminhos locais
(ex.: `/img/arroz-parbolizado.jpg`). Peça que eu faça essa troca quando quiser.

## Arquivos

- `index.html` — o site completo (HTML, CSS, JS e fontes embutidos)
- `vercel.json` — URLs limpas e headers de segurança
