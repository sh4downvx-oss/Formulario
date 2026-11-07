# WitherCraft — Formulário de Cadastro (Bedrock)

Formulário estático de cadastro de players para servidor Minecraft Bedrock.  
Envia os dados automaticamente para um canal do Discord via webhook.

## Como usar

1. Abra o arquivo `index.html` no editor.
2. Role até o bloco **★ CONFIG ★** (perto do final, no `<script>`).
3. Ajuste se precisar:
   - `SERVER_NAME` — nome do servidor
   - `WEBHOOK_URL` — URL do webhook do Discord (já está configurado)
   - `LOGO_URL` — (opcional) link de uma logo externa
   - `RULES_URL` — (opcional) link das regras completas
   - `EMBED_COLOR` — cor do card no Discord

## Subir no GitHub

```bash
# Na pasta do projeto
git init
git add .
git commit -m "Formulário de cadastro WitherCraft"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPO.git
git push -u origin main
```

## Deploy no Vercel

### Opção A — pelo site
1. Acesse [vercel.com](https://vercel.com) e faça login com GitHub.
2. **Add New Project** → importe o repositório.
3. Framework Preset: **Other** (é HTML estático).
4. Clique em **Deploy**.

### Opção B — pela CLI
```bash
npm i -g vercel
vercel
```

Depois de publicar, o link fica no formato:
`https://seu-projeto.vercel.app`

## Segurança do webhook

A URL do webhook fica no código do site (visível no “Ver código-fonte”).  
Qualquer pessoa que tiver o arquivo ou o site no ar pode enviar mensagens nesse canal.

**Recomendações:**
- Use um canal só de cadastros (não o geral).
- Se houver spam, delete o webhook no Discord e crie outro.
- Atualize o `WEBHOOK_URL` no `index.html` e faça novo deploy.

## Estrutura

```
withercraft-form/
├── index.html    ← página completa (CSS + JS embutidos)
├── README.md
└── .gitignore
```

Não precisa de Node, npm, build ou backend. É só HTML.
