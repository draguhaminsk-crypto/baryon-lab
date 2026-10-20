# Baryon Lab — site de portfólio

Site simples em Astro para mostrar trabalhos de impressão 3D e receber solicitações pelo WhatsApp.

## O que instalar no Linux

Você já tem o VS Code. Falta apenas Node.js + npm.

### Opção recomendada: NVM

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```

Feche e abra o terminal. Depois:

```bash
nvm install --lts
node -v
npm -v
```

## Rodar o projeto

Entre na pasta do projeto e rode:

```bash
npm install
npm run dev
```

Abra no navegador o endereço que aparecer no terminal, normalmente:

```text
http://localhost:4321
```

## Primeira coisa para editar

Abra:

```text
src/data/site.ts
```

Troque o número em `whatsapp` pelo seu número real no formato DDI + DDD + número, somente números.

Exemplo:

```ts
whatsapp: '5541999999999',
```

## Colocar fotos reais no portfólio

1. Coloque as fotos em `public/portfolio/`.
2. Abra `src/data/site.ts`.
3. Em cada projeto, troque:

```ts
image: '',
```

por algo assim:

```ts
image: '/portfolio/minha-peca.jpg',
```

## Arquivos principais

- `src/pages/index.astro` — estrutura da página.
- `src/styles/global.css` — visual do site.
- `src/data/site.ts` — textos, WhatsApp e projetos.
- `src/components/RequestForm.astro` — formulário que abre o WhatsApp.
- `public/logo-baryon-lab.png` — logo enviada por você.

## Build de produção

```bash
npm run build
```

O Astro gera a versão final na pasta `dist/`.
