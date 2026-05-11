# Float — Os cinco caminhos do cartão de loja

Página de conteúdo. Estática. Tudo num único `index.html`.

## O que tem aqui

- `index.html` — a página
- `og.png` — preview 1200×630 que aparece quando o link é compartilhado no WhatsApp, LinkedIn, Twitter
- `favicon-*.png` — ícone da aba do navegador em várias resoluções

## Deploy — caminho mais rápido (drag-and-drop, 1 minuto)

1. Abre **https://vercel.com/new** no navegador
2. Faz login (mesma conta que você usa pra Floataceleradora)
3. **Arrasta esta pasta `deploy/` inteira** pra dentro da página
4. Vercel detecta como projeto estático. Clica **Deploy**
5. Em ~30 segundos sai uma URL tipo `cartao-loja-xxxx.vercel.app`

## Deploy via GitHub (auto-deploy em cada push)

Se quiser que cada edição no arquivo gere um deploy novo automaticamente:

```bash
cd deploy
git init
git add .
git commit -m "Initial deploy"
git branch -M main
git remote add origin git@github.com:Floataceleradora/cartao-loja.git
git push -u origin main
```

Depois, em vercel.com/new, importa o repo. Cada `git push` redeploya.

## Subdomínio próprio (opcional)

Pra usar `cartao.floatbrasil.com` em vez do `.vercel.app`:

1. Em Vercel → Settings do projeto → Domains → adiciona `cartao.floatbrasil.com`
2. Vercel mostra um CNAME pra apontar (ex.: `cname.vercel-dns.com`)
3. No painel do HostGator (DNS do floatbrasil.com), adiciona um registro CNAME:
   - Tipo: `CNAME`
   - Nome: `cartao`
   - Valor: o que a Vercel mostrou
4. Propagação leva alguns minutos. Vercel emite o SSL automático.

## Atualizar depois

Edita o `index.html` direto. Se estiver via GitHub, `git commit` + `git push` → Vercel redeploya. Se estiver via drag-and-drop, vai em vercel.com/new → arrasta a pasta de novo → escolhe "redeploy".
